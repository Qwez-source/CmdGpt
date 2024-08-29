![logo](https://i.ibb.co/VDsbfq6/photo-2024-08-28-20-27-11.jpg)
# CmdGpt
## About
The most simplified analogue of gpt4free
## Using ChatGPT
```python
from CmdGpt import CmdGpt_lib

promt = """

hello,
my dear ai

"""

print(CmdGpt_lib.ask(promt, bot_id=0))
# id - 0, 1, 2
```
### Parameters:
- message: The message string you want to send to ChatGPT.
- bot_id: An integer (0, 1, 2) that specifies which ChatGPT instance to use.
- - 0: GPT 3
- - 1: GPT 3.5
- - 2: Transformer
## Using Image Generation
```python
from CmdGpt import CmdGenerate_lib

# generating image in base64 string
image_data = CmdGenerate_lib.generate("cat", 1024, 1024, "negative promt", "style") #styles - KANDINSKY, DEFAULT, UHD, ANIME. You can see styles on https://cdn.fusionbrain.ai/static/styles/key
# decrypt
if image_data:
    CmdGenerate_lib.save_image(image_data, "name.png", "Path") # If you do not specify a saving path, the file will be saved in the same directory
```
### generate Function Parameters:
- prompt: A string that specifies what kind of image to generate.
- width: The width of the generated image in pixels (max - 1024).
- height: The height of the generated image in pixels (max - 1024).
- negative_prompt: A string to exclude certain elements from the image. Further details are recommended for clarity.
- style: Specifies the style of the image. Options are:
- - KANDINSKY
- - DEFAULT
- - UHD
- - ANIME

### save_image Function Parameters:
- image_data: The base64 string data of the image generated by the generate function.
- filename: The name under which the image file will be saved.
- path: The directory path where the image will be saved. If not specified, the image will be saved in the current directory

## Credits
- Kandinsky [image generator] - https://fusionbrain.ai/
- ChatGPT [0 id] - https://chatgptis.org/
- ChatGPT [1 id] - https://seoschmiede.at/en/aitools/chatgpt-tool/
- ChatGPT [2 id] - https://www.blackbox.ai/

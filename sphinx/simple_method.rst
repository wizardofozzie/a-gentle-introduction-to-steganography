Simple method
-------------


.. code-block:: python

    import urllib
    from PIL import Image
    
    def decode_image(img):
        width, height = img.size
        msg = ""
        index = 0
        for row in range(height):
            for col in range(width):
                r, g, b = img.getpixel((col, row))
                if row == 0 and col == 0:
                    msg_length = r
                elif index <= msg_length:
                    msg += chr(r)
                index += 1
        return msg

        urllib.urlretrieve("http://cedric.bonhomme.free.fr/images/Lenna_Simple_Method.png", "Lenna.png")
        img = Image.open("Lenna.png")
        print decode_image(img)

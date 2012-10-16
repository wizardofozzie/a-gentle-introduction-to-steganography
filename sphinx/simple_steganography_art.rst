Simple steganography art
------------------------

In computer scinece a well known method of hiding data (message) is to
concatenate these data to an archive. For example, if I want to hide a
text file in a music file:

.. code-block:: bash

    $ zip text-to-hide.zip text-to-hide.txt
    $ cat Stop_And_Stare.ogg test-to-hide.zip > OneRepublic_-_Stop_And_Stare-1.ogg

Now you can still listen the song. If you want to recover the text, you just have to unzip the song. 

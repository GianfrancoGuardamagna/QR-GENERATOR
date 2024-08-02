#Parameters of the object

Version : Controls the size of the QR code (version 1 is a 21x21 code, and each version increases the size by 4 modules per side). If set to None, the size will be adjusted automatically based on the amount of data.

Error_correction : Controls the error correction level. Possible values are:

- qrcode.constants.ERROR_CORRECT_L (7% error correction)
- qrcode.constants.ERROR_CORRECT_M (15% error correction)
- qrcode.constants.ERROR_CORRECT_Q (25% error correction)
- qrcode.constants.ERROR_CORRECT_H (30% error correction)

Box_size : The size of each box (module) of the QR code in pixels.

Border : The size of the border (the white space around the QR code), measured in boxes (modules). The minimum value is 4, as per the QR code specification.

-----------------------------------------------------------------------------------------------

'qr.make(fit=True)'

Purpose: The fit parameter controls whether the size of the QR code should be automatically adjusted to fit the amount of data it contains.

Behavior:

When fit=True, the QR code library calculates the smallest possible version of the QR code that can accommodate the provided data. This means the QR code will not be larger than necessary, ensuring an optimal and efficient size.

If fit=False, the QR code will be generated with the size specified by the version parameter, regardless of whether it's too large or too small for the data.
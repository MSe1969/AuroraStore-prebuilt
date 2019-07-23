# AuroraStore-prebuilt

Prebuilt AuroraStore - taken from https://gitlab.com/AuroraOSS/AuroraStore/tags

This is the work of https://gitlab.com/whyorean

I have only taken the APK file from above link, added a priv-app permission whitelisting and Android.mk to 
include it as a prebuilt into Custom ROMs

Please visit https://gitlab.com/AuroraOSS/AuroraStore to learn about the app and also its license (GPLv3)

## How to include into your Custom ROM build
- Include this repo into your local manifest (path does not matter, suggest prebuilts/AuroraStore)
- Specify `PRODUCT_PACKAGES += AuroraStore AuroraServices` in a 'product' .mk file (**not** in an Android.mk file)
- An 'elegant' way to do so without having to fork and track any specific device or vendor repository is to simply create an own product.mk file in directory vendor/extras (or to add the above statement into an existing one)

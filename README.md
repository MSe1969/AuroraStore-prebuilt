# AuroraStore-prebuilt

Prebuilt AuroraStore & AuroraDroid - taken from 
    https://gitlab.com/AuroraOSS/AuroraStore/tags
    https://gitlab.com/AuroraOSS/AuroraDroid/tags
    https://gitlab.com/AuroraOSS/AuroraServices/tags

This is the work of https://gitlab.com/whyorean

I have only taken the APK files from above links, added a priv-app permission whitelisting and Android.mk to 
include it as a prebuilt into Custom ROMs

Please visit https://gitlab.com/AuroraOSS to learn about the apps and also its license (GPLv3)

## How to include into your Custom ROM build
- Include this repo into your local manifest (path does not matter, suggest prebuilts/AuroraStore)
- Specify `PRODUCT_PACKAGES += AuroraDroid AuroraStore AuroraServices` in a 'product' .mk file (**not** in an Android.mk file)
- Depending on what you wish to include or not, leave out from above statement, what you don't want to include
- An 'elegant' way to do so without having to fork and track any specific device or vendor repository is to simply create an own product.mk file in directory vendor/extras (or to add the above statement into an existing one)

## Branches
Use branch 'master' up to Android 11, use branch '12L' from Android 12 onwards

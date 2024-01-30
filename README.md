# Android Text to Image Library

A wrapper Android library/AAR that allows creating an image from a meaningful prompt text received from the user.

In its basic usage flow, the library takes a meaningful string as input and returns the ByteArray equivalent of the created image as output.

## Test Records

<details><summary> Show tests </summary>

https://github.com/zekierciyas/android-text-to-image/assets/71823127/c40e492b-a337-44c4-86f4-7e0c628d1a10

https://github.com/zekierciyas/android-text-to-image/assets/71823127/024da6e4-9f40-4259-bbfa-434cd26b629b

https://github.com/zekierciyas/android-text-to-image/assets/71823127/bfe6d151-320e-4c03-b99c-ac0ee3b17224

https://github.com/zekierciyas/android-text-to-image/assets/71823127/808a985a-ec0f-44b6-ae45-fc8e0a3efd0e

</details>


## Gradle

<details><summary>Kotlin DSL</summary>

```gradle
implementation ("com.github.zekierciyas:android-text-to-image:1.0.4")
```

</details>

<details><summary>Groovy DSL</summary>
    
```gradle
implementation 'com.github.zekierciyas:android-text-to-image:1.0.4'
```

</details>



## Library Usage
``` kotlin
    TextToImage.instance().process(
        input = "Photo of a cat making cake",
        dispatcher = Dispatchers.IO,
        callback = object : TextToImage.TextToImageCallback {
            override fun onSuccess(byteArray: ByteArray) {
              //Process done
              //Convert ByteArray to Bitmap/ImageBitmap
            }

            override fun onError(error: Throwable) {
              //Error happened during process
            }
        }
    )
```

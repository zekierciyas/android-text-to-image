# Android Text to Image Library

A wrapper Android library/AAR that allows creating an image from a meaningful prompt text received from the user.

In its basic usage flow, the library takes a meaningful string as input and returns the ByteArray equivalent of the created image as output.



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

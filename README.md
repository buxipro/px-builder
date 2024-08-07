# PX Builder

Px Builder is AppInventor extension aix builder tool, It's support all command line tools like `Termux` and Supported all features of `java 8` also `lambda expression`.

To get started, place the all source files under the `src/` like `src/com/example/Example.java`, place the all helpers source file under the `src/com/example/helpers/Dropdown.java` more details is here [READ](https://docs.google.com/document/u/0/d/10kdXhSKlNBylE9mu2bago76jZVEj4R7H7pe0RKwoLAg/mobilebasic#heading=h.j2gi06bgd9sf).
Any libraries `"(.jar)"` you need should be placed under
`lib/deps/` like `lib/deps/example.jar`.

## Add Libraries and Permissions in source code

- Includes library references in `@UsesLibraries`

- Defines permissions in `@UsesPermissions`

## Requirements

You will need:

* java 8
* download jdk-8 for Termux [DOWNLOAD](https://github.com/itsaky/openjdk-8-android/releases/tag/2021-12-26).
* ant 1.10 or higher
* git 2.3.10 or higher

For cloning this repository, use the following command:

```shell
git clone https://github.com/buxipro/px-builder
```

Example extension code:

>      package com.example; 
>      import com.google.appinventor.components.runtime.*; 
>      import com.google.appinventor.components.runtime.util.*;
>      import com.google.appinventor.components.annotations.*;
>      import com.google.appinventor.components.common.*;
>      import com.google.appinventor.components.scripts.*;
>      import com.google.appinventor.components.annotations.androidmanifest.*;
>      import android.*;
>      import android.app.*;
>     @DesignerComponent(
>         version = 1,
>         description = "Example Extension",
>         category = ComponentCategory.EXTENSION,
>         nonVisible = true,
>         iconName = "https://res.cloudinary.com/dtmmagyep/image/upload/v1720274870/hlbiq7sgv8fhfxgt9wi5.jpg",
> 		androidMinSdk = 26
>     )
>     @SimpleObject(external = true)
>     //Libraries
>     @UsesLibraries(libraries = "example.jar") //add libraries
>     @UsesPermissions(permissionNames = "android.permission.WRITE_EXTERNAL_STORAGE,android.permission.ACCESS_DOWNLOAD_MANAGER,android.permission.ACCESS_FINE_LOCATION,android.permission.RECORD_AUDIO, android.permission.MODIFY_AUDIO_SETTINGS, android.permission.CAMERA,android.permission.VIBRATE,android.webkit.resource.VIDEO_CAPTURE,android.webkit.resource.AUDIO_CAPTURE,android.launcher.permission.INSTALL_SHORTCUT,android.permission.ACTION_MANAGE_OVERLAY_PERMISSION,android.permission.CLEAR_APP_CACHE,android.permission.SYSTEM_ALERT_WINDOW,android.permission.HIDE_OVERLAY_WINDOWS,android.permission.QUERY_ALL_PACKAGES,android.permission.INTERNET,android.permission.MANAGE_EXTERNAL_STORAGE,android.permission.REQUEST_DELETE_PACKAGES,android.permission.REQUEST_INSTALL_PACKAGES,com.android.launcher.permission.INSTALL_SHORTCUT")
>     public class Extension extends AndroidNonvisibleComponent implements Component{
>         private ComponentContainer container;
>         private Activity activity;
> 
>         public Extension(ComponentContainer container) {
>             super(container.$form());
>             this.activity = container.$context();
>             this.container = container;
>         }
> 	      @SimpleFunction
>         public void ExampleFunction() {
>         }
>       	@SimpleEvent
>         public void ExampleEvent() {
>         }
>     
>          @SimpleProperty( category = PropertyCategory.BEHAVIOR)
>          @DesignerProperty(defaultValue = "true", editorType = "boolean")
>          public void ExampleProperty(boolean property) {
>          }
>          public boolean property(){
>               return true;
>          }
>     }

## Contributing

We welcome contributions from the community! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
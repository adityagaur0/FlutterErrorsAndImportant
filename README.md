# FlutterErrorsAndImportant

## 1. Error Commiting to git
![image](https://github.com/adityagaur0/FlutterErrorsAndImportant/assets/112656570/32b7ced2-d408-417a-8e16-f560d6c9244c)

We are looking at a more ideal solution for this through Desktop, but in the mean time. For those unfamiliar with using the Command Line Interface (CLI).

From GitHub Desktop, you can press Ctrl + ` (Also available from the "Repository" main menu as "Open in [Your set terminal]"). This should open up a CLI.

There you can type:

`git config --global  pull.ff true` (or any of the other options specified in the error hints).

Now when you attempt to pull it will use that configuration and allow you to continue.

There is the possibility that because you do not use the CLI, you may need to [download and install git](https://git-scm.com/downloads) for this to work.

Some explanation of choice above if interested:
I suggested pull.ff true simply because it attempts to fast forward your branch to be up to date with your remote before applying your local commits and if not it will preform a merge from the remote to your local branch. [Read docs here](https://git-scm.com/docs/git-pull). Typically when you pull a branch, add commits, and push. It is in the order assuming your local is up to date with remote. By merging when fast forwarding is not possible, you will see a merge commit informing you of how it was handled. (The other options are to rebase or always merge, many new users find rebase to be less intuitive, but really accomplishes the same thing)

I added the --global flag so that your choice will apply to all your repos and you won't see this error message again. Simply omit this if you want a different behavior per repository.


## 2. change minSDKversion
1. add to local.properties (flutter.minSdkVersion=22).
   <img width="1440" alt="Screenshot 2023-11-01 at 4 05 42 AM" src="https://github.com/adityagaur0/FlutterErrorsAndImportant/assets/112656570/02c45136-efa1-4e8f-870e-a14b57d14f6d">

2. go to build.Gradle
   
   `minSdkVersion localProperties.getProperty("flutter.minSdkVersion").toInteger();`


# flutter imp.

### 1. unfocus the keyboard while using text form field.
```
GestureDetector(
      onTap: () {
        FocusScope.of(context)
            .unfocus(); // Close the keyboard when tapping outside of a text field
      },
      child: Scaffold(
```

# flutter comments.
<img width="837" alt="Screenshot 2024-02-19 at 3 16 16 AM" src="https://github.com/adityagaur0/FlutterErrorsAndImportant/assets/112656570/e38c66c2-f032-4d4b-9750-1a93add6f7ae">

<img width="555" alt="Screenshot 2024-02-19 at 3 17 53 AM" src="https://github.com/adityagaur0/FlutterErrorsAndImportant/assets/112656570/6ce6e57b-b19e-42ea-a1d3-464ebe959442">


# sha keys
```
 keytool -list -v -alias androiddebugkey -keystore ~/.android/debug.keystore -storepass android -keypass android
```



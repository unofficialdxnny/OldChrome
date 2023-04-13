# OldChrome
How to build old Chrome?

# How to Build Older Chrome Versions from Chromium Binaries

Chrome, the popular web browser, is built on the open-source Chromium project. While the latest version of Chrome is often the most stable and secure, there may be times when you need to use an older version of the browser. For example, you may be testing a website or application that only works with a specific version of Chrome. In this case, you can build an older version of Chrome from the Chromium binaries. Here's how to do it.

## Step 1: Download the Chromium Source Code

The first step is to download the source code for the version of Chromium that you want to build. You can find the source code for all versions of Chromium on the Chromium project's GitHub page. 

For example, if you want to build Chrome version 72.0.3626.121, you can download the source code for that version by navigating to the following URL: https://github.com/chromium/chromium/tree/72.0.3626.121

Once you're on the page for the version you want to build, click the green "Code" button and select "Download ZIP". This will download a ZIP file containing the source code for the selected version.

## Step 2: Install Dependencies

Before you can build Chromium from the source code, you'll need to install the dependencies. The specific dependencies you need will depend on your operating system. 

For example, if you're using Ubuntu, you can install the necessary dependencies by running the following command in a terminal:

```cmd
sudo apt-get install build-essential git python python-dev
python-setuptools python-wheel python-sphinx libasound2-dev
libatk1.0-dev libatspi2.0-dev libbz2-dev libcups2-dev libdrm-dev
libexif-dev libgbm-dev libgconf2-dev libgl1-mesa-dev libgles2-mesa-dev
libglib2.0-dev libgnome-keyring-dev libgtk-3-dev libkrb5-dev libnspr4-dev
libnss3-dev libpci-dev libpulse-dev libsecret-1-dev libspeechd-dev
libsqlite3-dev libssl-dev libvpx-dev libxcomposite-dev libxcursor-dev
libxdamage-dev libxfixes-dev libxi-dev libxrandr-dev libxrender-dev
libxslt1-dev libxt-dev libxtst-dev mesa-common-dev yasm
```


Make sure to update the package manager before running the above command. You can do this by running:

```
sudo apt-get update
```



## Step 3: Build Chromium

Now that you've downloaded the source code and installed the dependencies, it's time to build Chromium. Here's how to do it:

1. Extract the ZIP file containing the Chromium source code to a directory of your choice.
2. Open a terminal and navigate to the directory where you extracted the source code.
3. Run the following command to set up your build environment:

```
./build/install-build-deps.sh
```


4. Run the following command to generate the build files:

```
gn gen out/Release --args='target_os="linux" is_debug=false'
```


Replace "linux" with your operating system if you're not using Linux.

5. Run the following command to build Chromium:

```
ninja -C out/Release chrome
```


This command will build the Chrome browser from the source code you downloaded. Once the build process is complete, you'll have an executable file that you can use to run the older version of Chrome.

That's it! Now you know how to build older versions of Chrome from the Chromium binaries. Happy browsing!

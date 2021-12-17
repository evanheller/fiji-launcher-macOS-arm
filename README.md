# fiji-launcher-macOS-arm
Modified version of the ImageJ launcher script for Fiji for compatibility
with ARM-native JREs on Apple Silicon. 

To run Fiji natively on Apple Silicon, the suggested route would be:
- Download the "No JRE" version of [Fiji](https://downloads.imagej.net/fiji/latest/fiji-nojre.zip)
- Obtain an ARM-native version of the JRE from [Oracle](https://www.oracle.com/java/technologies/downloads/#jdk17-mac), or install OpenJDK from [Homebrew](https://brew.sh)
- The installers above will install the JREs system-wide, but you can also package them locally in the **Fiji.app/java** subdirectory.
- Copy the **Info.plist** and **ImageJ-macosx** launcher provided in this repository into the **Fiji.app/Contents** and **Fiji.app/Contents/MacOS** respectively. 

As of December 2021, Fiji packages an Intel-only binary of [imagej-launcher](https://github.com/imagej/imagej-launcher).
While this can be compiled as an ARM64 binary (see [this thread](https://github.com/imagej/imagej-launcher/issues/82 ), the launcher is not compatible with
recent ARM-native versions of the JRE provided by Oracle or OpenJDK. An alternative solution
would be to use an ARM-native JRE known to work with imagej-launcher, such as [Azul](https://www.azul.com/newsroom/azul-announces-support-of-java-builds-of-openjdk-for-apple-silicon/). 



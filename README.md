# 🌟 **Pinou GLB Viewer** 🌟

Welcome to **Pinou GLB Viewer**! 🎉 This GLB file viewer is your new go-to tool for easily embedding 3D models into your websites. It is designed to be **simple**, **fast**, and **customizable** without requiring advanced technical knowledge. 🚀

## 🎨 **Features**

✨ **Easy Integration**: Add 3D to your web pages with just a few simple steps.

✨ **Unlimited Customization**: Configure the display of your 3D model with a wide range of settings.

✨ **Open Source**: Modify and use the code as you wish as long as you mention the author. You are free to adapt it to your needs! 💡

## 🛠️ **Installation and Setup**

### ⚠️ **Important Warning**

**Note that Pinou GLB Viewer must be used on a real server**. If you try to run it locally by simply opening the `index.html` file in your browser, it may not work correctly. To resolve this issue on Windows, you can install the **Go Live** extension in Visual Studio Code. We will show you how to do this in the tutorial below.

### 📥 **Downloading with Git**

1. **Clone the repository**:
   - Open a command line or terminal.
   - Execute the following command to clone the repository:
     ```
     gh repo clone Pinou007/GLB-Viewer
     ```

2. **Access the files**:
   - Navigate to the cloned directory with the command:
     ```
     cd pinou-glb-viewer
     ```

### 📂 **Preparing the GLB File**

Place your `.glb` 3D file in the same directory as your `index.html` or embedded page. This file should be named **`modeles3d.glb`**.

### 🎛️ **Customization**

Once the `.glb` file is in place, customize the display and options directly through the URL by following the instructions below.

## 🌍 **URL Structure**

The URL consists of two main parts:

1. **Base URL** 🏠: The address of the HTML page where the viewer is embedded.
2. **Configuration Parameters** ⚙️: These parameters follow the `?` symbol in the URL and control various aspects of the display.

### Example URL

Here’s an example of a URL with configuration parameters:

```
http://your-domain.com/index.html?x=0.08&y=3.41&z=7.59&far=10000&fov=72.78&shadowEnabled=true
```

In this example, several parameters are specified to set the camera position, field of view, and other graphical options.

## 📝 **Parameter Descriptions**

Here is a list of the main parameters you can use in the URL:

| 🗂️ **Category**                | 🛠️ **Parameter**        | 📄 **Description**                                     | 🎯 **Example Values** |
|-------------------------------|------------------------|--------------------------------------------------------|----------------------|
| **Camera Position**            | `x`                    | Sets the camera position on the X axis. This allows horizontal adjustment of the view relative to the 3D model. | `x=1.0`              |
|                               | `y`                    | Sets the camera position on the Y axis. This adjusts the height of the camera relative to the 3D model. | `y=2.0`              |
|                               | `z`                    | Sets the camera position on the Z axis. This changes the distance of the camera from the 3D model. | `z=3.0`              |
| **Clipping Plan**              | `far`                  | Determines the maximum distance at which objects will be rendered before being "clipped" by the clipping plane. A large `far` value allows seeing distant objects. | `far=10000`          |
|                               | `near`                 | Defines the minimum distance at which objects start to be rendered. Useful for avoiding artifacts near the camera. | `near=0.1`           |
| **Field of View**              | `fov`                  | Specifies the camera's field of view angle in degrees. A wider field of view gives a greater sense of depth but can distort the image. | `fov=90`             |
| **Effects and Graphics**       | `shadowEnabled`        | Enables or disables the rendering of shadows cast by objects. Shadows add realism but can reduce performance if enabled. | `true/false`         |
|                               | `shadowType`           | Determines the type of shadow used, such as soft shadows (PCFSoft) that offer a more realistic rendering. | `shadowType=2`       |
| **UI Customization**           | `guiWidth`             | Controls the width of the graphical user interface (GUI) where you can adjust settings in real time. | `guiWidth=800px`     |
|                               | `guiPadding`           | Sets the internal spacing of the graphical user interface, adjusting the distance between interface elements and the window edges. | `guiPadding=30px`    |
|                               | `guiBorderRadius`      | Adjusts the rounding of the corners of the graphical user interface, giving a more modern and smooth look to the interface. | `guiBorderRadius=30px`|
|                               | `guiFontSize`          | Controls the font size used in the graphical user interface, which can improve the readability of options. | `guiFontSize=19px`   |
| **Visual Effects**             | `filmEnabled`          | Enables or disables a film grain effect on the screen, adding a stylized texture to the display. | `true/false`         |
|                               | `glitchEnabled`        | Enables or disables a digital distortion effect, mimicking a glitchy visual effect for an artistic result. | `true/false`         |
|                               | `displacementEnabled`  | Enables or disables the displacement effect that modifies the model's geometry based on a displacement texture. | `true/false`         |
|                               | `dotScreenEnabled`     | Enables or disables a halftone effect, giving the image a pixelated or dot pattern look similar to comic book printing. | `true/false`         |
|                               | `asciiArtEnabled`      | Enables or disables a visual effect that transforms the display into ASCII art, rendering the image using only characters. | `true/false`         |
|                               | `psychedelicEnabled`   | Enables or disables a psychedelic effect that applies bright colors and distortions for a unique visual result. | `true/false`         |

### 🛠️ **Customization Example**

Suppose you want to disable shadows and use a wider field of view. You could set up your URL as follows:

```
http://your-domain.com/index.html?x=0.08&y=3.41&z=7.59&far=10000&fov=90&shadowEnabled=false&guiWidth=800px&guiPadding=30px
```

This URL will configure the application with these specific parameters. 🔧

## 🚀 **Tutorial: Running on Windows and Server**

### 📥 **Downloading and Running on Windows**

1. **Download the files**:
   - Clone or download the GitHub repository containing the `index.html` file and place it in a dedicated directory on your machine.

2. **Install Visual Studio Code** (if not already installed):
   - Download Visual Studio Code from [the official site](https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user).
   - Install it following the installation instructions.

3. **Install the Go Live extension**:
   - Open Visual Studio Code.
   - Go to the Extensions tab (icon of a square with a brick in the left sidebar).
   - Search for **"Live Server"** in the search bar.
   - Click "Install" to add the extension to your environment.

4. **Start the local server**:
   - Open the directory containing your `index.html` file in Visual Studio Code.
   - Click on "Go Live" in the status bar at the bottom of the screen.
   - A browser window will automatically open, running your project on a local server.

### 🌐 **Deploying on a Server**

1. **Upload the files to the server**:
   - Transfer your project files (including `index.html` and `modeles3d.glb`) to your server via FTP, Git, or a web admin interface.

2. **Configure settings**:
   - Adjust your server settings if necessary to properly serve `.glb` files, especially if you are using an HTTP server.

3. **Test access**:
   - Access your site via the domain or IP address provided by your hosting service and ensure everything works as expected.

## 🤝 **Contributing**

This project was developed by a passionate young developer. Feel free to modify and use this project for your own needs. However, please mention the original author if you redistribute or use this code in another project. 🛠️💻

---

Thank you for using **Pinou GLB Viewer**. If you have any suggestions, bugs to report, or improvements to propose, don't hesitate to open an issue or a pull request on GitHub! 🚀

---

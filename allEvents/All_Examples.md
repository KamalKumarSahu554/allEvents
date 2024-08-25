Sure, here is a simple JavaScript code snippet for each event, demonstrating how to add event listeners and handle each event.

### Mouse Events

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mouse Events</title>
  </head>
  <body>
    <button id="mouseButton">Mouse Button</button>
    <script>
      const mouseButton = document.getElementById("mouseButton");

      mouseButton.addEventListener("click", () => alert("Mouse Clicked"));
      mouseButton.addEventListener("dblclick", () =>
        alert("Mouse Double Clicked")
      );
      mouseButton.addEventListener("mousedown", () => alert("Mouse Down"));
      mouseButton.addEventListener("mouseup", () => alert("Mouse Up"));
      mouseButton.addEventListener("mouseover", () => alert("Mouse Over"));
      mouseButton.addEventListener("mouseout", () => alert("Mouse Out"));
      mouseButton.addEventListener("mousemove", () =>
        console.log("Mouse Moving")
      );
      mouseButton.addEventListener("mouseenter", () => alert("Mouse Entered"));
      mouseButton.addEventListener("mouseleave", () => alert("Mouse Left"));
      mouseButton.addEventListener("contextmenu", (event) => {
        event.preventDefault();
        alert("Right Click");
      });
    </script>
  </body>
</html>
```

### Keyboard Events

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Keyboard Events</title>
  </head>
  <body>
    <input type="text" id="keyboardInput" placeholder="Type here" />
    <script>
      const keyboardInput = document.getElementById("keyboardInput");

      keyboardInput.addEventListener("keydown", () => console.log("Key Down"));
      keyboardInput.addEventListener("keypress", () =>
        console.log("Key Press")
      );
      keyboardInput.addEventListener("keyup", () => console.log("Key Up"));
    </script>
  </body>
</html>
```

### Form Events

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Form Events</title>
  </head>
  <body>
    <form id="form">
      <input type="text" id="textInput" placeholder="Change me" />
      <input type="submit" value="Submit" />
      <input type="reset" value="Reset" />
    </form>
    <script>
      const form = document.getElementById("form");
      const textInput = document.getElementById("textInput");

      form.addEventListener("submit", (event) => {
        event.preventDefault();
        alert("Form Submitted");
      });
      textInput.addEventListener("change", () => alert("Input Changed"));
      textInput.addEventListener("input", () => console.log("Input Event"));
      textInput.addEventListener("focus", () => console.log("Input Focused"));
      textInput.addEventListener("blur", () => console.log("Input Blurred"));
      form.addEventListener("reset", () => alert("Form Reset"));
      textInput.addEventListener("select", () => console.log("Text Selected"));
    </script>
  </body>
</html>
```

### Window Events

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Window Events</title>
  </head>
  <body>
    <script>
      window.addEventListener("load", () => console.log("Page Loaded"));
      window.addEventListener("unload", () => console.log("Page Unloaded"));
      window.addEventListener("resize", () => console.log("Window Resized"));
      window.addEventListener("scroll", () => console.log("Window Scrolled"));
    </script>
  </body>
</html>
```

### Clipboard Events

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Clipboard Events</title>
  </head>
  <body>
    <textarea
      id="clipboardArea"
      placeholder="Copy, cut, or paste here"></textarea>
    <script>
      const clipboardArea = document.getElementById("clipboardArea");

      clipboardArea.addEventListener("copy", () => alert("Copied"));
      clipboardArea.addEventListener("cut", () => alert("Cut"));
      clipboardArea.addEventListener("paste", () => alert("Pasted"));
    </script>
  </body>
</html>
```

### Media Events

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Media Events</title>
  </head>
  <body>
    <video id="video" width="320" height="240" controls>
      <source src="movie.mp4" type="video/mp4" />
    </video>
    <script>
      const video = document.getElementById("video");

      video.addEventListener("play", () => console.log("Video Playing"));
      video.addEventListener("pause", () => console.log("Video Paused"));
      video.addEventListener("ended", () => console.log("Video Ended"));
      video.addEventListener("volumechange", () =>
        console.log("Volume Changed")
      );
      video.addEventListener("timeupdate", () => console.log("Time Updated"));
    </script>
  </body>
</html>
```

### Touch Events

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Touch Events</title>
  </head>
  <body>
    <div
      id="touchArea"
      style="width: 100px; height: 100px; background-color: lightblue;"></div>
    <script>
      const touchArea = document.getElementById("touchArea");

      touchArea.addEventListener("touchstart", () =>
        console.log("Touch Start")
      );
      touchArea.addEventListener("touchmove", () => console.log("Touch Move"));
      touchArea.addEventListener("touchend", () => console.log("Touch End"));
      touchArea.addEventListener("touchcancel", () =>
        console.log("Touch Cancel")
      );
    </script>
  </body>
</html>
```

### Drag and Drop Events

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Drag and Drop Events</title>
  </head>
  <body>
    <div
      id="dragItem"
      draggable="true"
      style="width: 100px; height: 100px; background-color: lightcoral;"></div>
    <div
      id="dropZone"
      style="width: 200px; height: 200px; background-color: lightgreen;"></div>
    <script>
      const dragItem = document.getElementById("dragItem");
      const dropZone = document.getElementById("dropZone");

      dragItem.addEventListener("dragstart", () => console.log("Drag Start"));
      dragItem.addEventListener("drag", () => console.log("Dragging"));
      dropZone.addEventListener("dragenter", () => console.log("Drag Enter"));
      dropZone.addEventListener("dragover", (event) => {
        event.preventDefault();
        console.log("Drag Over");
      });
      dropZone.addEventListener("dragleave", () => console.log("Drag Leave"));
      dropZone.addEventListener("drop", (event) => {
        event.preventDefault();
        console.log("Dropped");
      });
      dragItem.addEventListener("dragend", () => console.log("Drag End"));
    </script>
  </body>
</html>
```

### Miscellaneous Events

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Miscellaneous Events</title>
  </head>
  <body>
    <img id="image" src="invalid-url.jpg" alt="Image" />
    <div
      id="animation"
      style="width: 100px; height: 100px; background-color: red; transition: width 2s;"></div>
    <script>
      const image = document.getElementById("image");
      const animation = document.getElementById("animation");

      image.addEventListener("error", () => console.log("Image Load Error"));
      animation.addEventListener("transitionend", () =>
        console.log("Transition Ended")
      );
      animation.addEventListener("animationend", () =>
        console.log("Animation Ended")
      );
      window.addEventListener("wheel", () => console.log("Mouse Wheel"));
      window.addEventListener("pointerdown", () => console.log("Pointer Down"));
      window.addEventListener("pointerup", () => console.log("Pointer Up"));
      window.addEventListener("pointermove", () => console.log("Pointer Move"));
      window.addEventListener("pointerenter", () =>
        console.log("Pointer Enter")
      );
      window.addEventListener("pointerleave", () =>
        console.log("Pointer Leave")
      );

      // Trigger a transition for demonstration
      setTimeout(() => {
        animation.style.width = "200px";
      }, 1000);
    </script>
  </body>
</html>
```

These examples cover the basic usage of various JavaScript events. You can expand these examples by adding more complex event handlers as needed.

<style>
body {
  background-color: black;
  color: rgb(136, 136, 136);
  font-family: 'Input Sans', sans-serif;
}

img, video {
  max-width: 100%;
}

h2 {
  color: #2a9fd6;
}

h3 {
 color: white;
}

h4 {
 color: white;
}

li {
  list-style-image: url(img/bullet.png);
}

.responsive-container { position: relative; padding-bottom: 56.25%; padding-top: 30px; height: 0; overflow: hidden; }
.responsive-container iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }

</style>

![Audulus Logo](img/logo.png)

Welcome to **Audulus**! With Audulus you can build synthesizers
from first principles, design new sounds, or process audio. All with
real-time low-latency processing suitable for live performance.
    
To get started, view the UI Basics video for your platform (<a href="#ui-basics-ipadiphone">iOS</a> or <a href="#ui-basics-mac">Mac</a>).

Be sure to sign up [here](http://eepurl.com/-8vkP) for the Audulus mailing list.

If you need help or have found a bug, please contact us at:

![Support Email Address](img/support.png)

We're here to help!

---

## UI Basics (iPad/iPhone)

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/89969814" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
</div>

The iPad/iPhone Audulus UI at a glance:

-   Pinch with two fingers to zoom in and out of your patch.
-   Drag on the background or with two fingers to pan.
-   Double-tap on a node to zoom in for editing.
-   Double-tap on the background to zoom out and see your entire patch.
-   Many operations use context menus - tap and hold to bring up the
-   context menu.
-   To create a new node, tap and hold on the background.
-   To make a connection, zoom in and drag from an output to an input.
-   To disconnect, drag from an input.
-   Use connection mode to make connections even while zoomed out.
-   Tap the keyboard button to bring up the on-screen keyboard.
-   Audulus will automatically detect your MIDI keyboard or control
    surface.

### Patch Editor Buttons

-   ![Delete Button](img/Delete.png) **Delete** - Deletes selected nodes.
-   ![Lock Mode Button](img/Lock.png) **Lock Mode** - Locks the nodes in
    place. This is useful for performing.
-   ![Timing Mode Button](img/Stopwatch.png) **Timing Mode** - Toggles
    timing mode. Timing Mode shows the percentage of CPU time each node
    in your patch takes to compute. The Timing Mode button is only shown
    if the Timing Mode upgrade has been purchased.
-   ![Show Keyboard Button](img/ShowKeyboard.png) **Show Keyboard** - Shows
    the on-screen keyboard.
-   ![Help Button](img/help.png) **Help** - Shows the Audulus documentation.

### Patch Browser Buttons

-   **"+"** - Creates a new patch.
-   ![Collapse Button](img/CollapseButton.png) **Collapse** - Collapses the
    patch thumbnails down to just their names, for browsing large
    collections of patches by name.
-   **"Select"** - Toggles the Path Browser's **Selection Mode** - When
    in selection mode, tapping on a patch thumbnail will select the
    patch and activate the Share, Duplicate, and Delete buttons.
    Multiple patches may be selected.
-   ![Share Patch Button](img/share.png).**Share** - Shares selected patches
    via email when in selection mode.
-   ![Duplicate Patch Button](img/duplicate.png) **Duplicate** - Duplicates
    selected patches when in selection mode.
-   ![Delete Patch Button](img/Delete.png) **Delete** - Deletes selected
    patches when in selection mode.
-   ![Help Button](img/help.png) **Help** - Shows the Audulus documentation.
-   ![Settings Button](img/settings.png) **Settings** - Shows the Audulus
    settings.
-   **"Store"** - Shows the Audulus store.

---

## UI Basics (Mac/Windows)

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/41123473" width="600" height="400" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
</div>

The Desktop Audulus UI at a glance:

-   many operations use right-click context menus (control click if you
    have one button)
-   to create a new node, right-click on the background, and select "Create"
-   to zoom use the mouse wheel or two fingers on your trackpad
-   to pan, drag the background
-   to select a node just click on it
-   to select multiple nodes, hold shift while clicking
-   to select all the nodes required to compute a node's output,
    command-click on the node
-   to make a connection between nodes, drag from an output to an input
-   to disconnect, drag from an input
-   to get help on a node, right click and select "Help"

---

## Building a Synth from Scratch

This Audulus tutorial video shows how to build a subtractive synthesizer
with some interesting modulations.

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/45484364" width="480" height="270" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
</div>

---

## Getting Help

If you need help or have found a bug, contact us at:

![Support Email Address](img/support.png)

We're here to help!

---

## Audulus Mailing List

Sign up [here](http://eepurl.com/-8vkP) for the Audulus mailing list. You'll get:

*  Updates for new versions of Audulus
*  Tutorials
*  New Patches
*  And more!

---

## Presets (Mac Only)

**Note: Mac only.**

Presets enable rapid switching between different networks. You might use
presets for switching between sounds during a performance or
experimenting with different ideas within a single patch.

To store a preset, hold the option key and press one of the number keys.
To load a preset press one of the number keys.

Because connections in Audulus fade in/out when connected/disconnected,
you can set up your patch so there are no clicks or pops when changing
presets.

Also, sharing nodes between presets enables things like delay spillover.

A MIDI program change message will call up a preset, so presets can be
used with your MIDI foot controller. This is particularly useful for
guitar rigs.

---

## Polyphony

Polyphonic processing in Audulus works seamlessly. A connection between
nodes is polyphonic if it is rendered thicker. Nodes are automatically
capable of polyphonic processing. So for example, feed a **Distortion**
node with a polyphonic connection and the distortion will be applied
separately to each voice in the connection.

A good example of polyphonic processing is the **Subtractive** example.
Set the [**Keyboard**](/nodes/#keyboard) node to "poly" and note the
thicker polyphonic connections. That is, up until the voices are mixed
down by the [**PolyToMono**](/nodes/#polytomono) node.

---

## Custom Nodes

Using the **Custom Nodes** upgrade, you can design your own node user interfaces.

After purchasing the upgrade, use the following steps to create your own node UI.

1. Create a sub-patch using the Patch Node (Utilities -> Patch)
2. Enter the sub-patch by double-tapping (or double-clicking) on the Patch Node
3. Create a node such as a Constant node (Level -> Constant)
4. Open the context menu on the Constant Node's knob and Select Expose
5. Exit the sub-patch and you'll see your knob on the front panel.
6. Open the context menu on the Patch Node and select Edit UI
7. Drag the knob to where you'd like it.
8. Open the Path Node's context menu again and select Lock UI to finish editing the UI.

Knobs aren't the only widgets that can be exposed. You can also expose inputs, outputs,
ADSR evenlopes, filter graphs (Filter node), mapper curves (Mapper node), triggers, lights, and
splines (Spline Node).

To quickly see what widget on the patch node corresponds to a sub-patch widget, use the
**Show Exposed** command in the widget's context menu.

---

## Audulus Audio Unit (Mac Only)

[Download Audio Unit](http://content.audulus.com/Audulus%20Audio%20Unit%202.9.pkg)

To install Audulus as an Audio Unit plugin, download the installer
package above.

The installer package will install the Audio Anit to either a
user-specific (`~/Library/Audio/Plug-Ins/Components`) or a system-wide
(`/Library/Audio/Plug-Ins/Components`) location.

The Audulus Audio Unit will appear under the manufacturer name
"Subatomic". Both 32-bit and 64-bit versions are included in the plugin.

The Audulus Audio Unit needs to know the location of the purchased
Audulus.app. By default it will look in the Applications folder. If
Audulus.app is not in the Applications folder, you will see a button to
locate it in the plugin window.

---

## Video Release Notes

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/110303345" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/101362651" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/92587625" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/85982395" width="500" height="281" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/81630224" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/78110412" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/74346514" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/71547753" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/67608824" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/65361327" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/64264072" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<div class="responsive-container">
<iframe src="http://player.vimeo.com/video/59208826" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

## ActionScript 3 (AS3) Scrolling List for Android and iOS mobile devices.  

### Features

* Cross-platform list for iOS and Android
* List Item Events broadcast when items touched.
* List Item Renderers for changing appearance of list items

#### TouchList

The TouchList class creates the list, adds items and handles touch events dispatched by the item renderers. You might notice that I didn’t use any actual TouchEvent listeners in the list. This is because a TouchEvent is essentially a MouseEvent. The TouchList class has a built in delay to differentiate between a scrolling and touch action. Like the Android phone, you can’t select an item while scrolling and pressed items are deselected if you scroll while pressed.

#### TouchListItemRenderer

TouchListItemRenderer implements ITouchListItemRenderer and renders the display of the items in the list data. This renderer can be customized to show whatever type of data you want in the list. List items can also be variable height.

#### ITouchListItemRenderer

If you want to create an item renderer for the list, then it must implement the ITouchListItemRenderer interface. This interface gives the renderer basic functionality to interact with user selection and touch events used by the list.

#### ListItemEvent

The list item event is a custom custom ListItemEvent dispatched when a list item renderer is pressed. The event contains the event payload and a instance of the item renderer selected.

### Installation

Included in the GitHub repository is the working project files created in Flash Builder 4. This file handles adding the list to the stage, screen orientation on the device, stage resize, and other functions for an Android AIR application. To install, just checkout the project file and import it into Flash Builder. I have also included Android .apk file if you want to deploy it directly to your Android phone.

### License
Released under the [MIT license](http://www.opensource.org/licenses/mit-license.php).
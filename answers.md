Github Repository

https://github.com/gonzalesjoecel-ux/flutter_basics_lab.git

The last three build() called lines from Activity 2.
- The final three build() called lines in the Debug Console in Activity 2 occurred as follows: first, when the application launched and the widget tree was drawn for the first time; second, when I pressed the button and updated _glasses inside setState(), which caused a rebuild; and third, when I pressed the button again for another state change, which caused the widget tree to rebuild once more.

Your observation from the experiements in Activity 2, 3, and 5.
-   


Review Questions:

1. What is the difference between a StatelessWidget and a StatefulWidget? Give one example of each
from this lab.
- A StatelessWidget does not change once it is built, like the ProfileCard in Activity 1, while a StatefulWidget can change its UI when the state updates, like the ThemeDemoApp in Activity 5.

2. Why is a StatefulWidget written as two classes? What does each class do?
- A StatefulWidget is written as two classes because the first class only describes the widget, and the second State class handles the data and logic that rebuilds the UI when something changes.

3. In Activity 2, what happened when you changed _glasses outside setState()? Why?
- In Activity 2, when I changed _glasses outside setState(), the number updated in memory but the screen did not refresh because setState() is the one that tells Flutter to rebuild the widget.

4. Looking at the Debug Console in Activity 2, when is build() called?
- In the Debug Console of Activity 2, the build() method is called every time the state changes or when Flutter needs to redraw the widget tree.

5. Explain the main axis and the cross axis of a Row and of a Column.
- In a Row, the main axis is horizontal and the cross axis is vertical, while in a Column the main axis is vertical and the cross axis is horizontal.

6. In Activity 3, what happened when you removed Expanded from a StatBox? What does Expanded do?
- In Activity 3, when I removed Expanded from a StatBox, the box size became smaller and not equal to the others because Expanded makes the children share the available space equally.

7. Why do we use GridView.builder for the menu instead of a Column with many children?
- We use GridView.builder for the menu instead of a Column because it is more efficient and can build items only when needed, while a Column with many children would load everything at once and be harder to manage.

8. How do Stack and Positioned create the Best seller badge in Activity 4?
- In Activity 4, the Stack places widgets on top of each other, and the Positioned widget puts the Best Seller badge at the exact spot over the menu item.

9. What is the difference between customizing with ThemeData and with a style on one widget? Give
one example of each from Activity 5.
- Customizing with ThemeData changes the style for the whole app, like setting a global color scheme in Activity 5, while styling one widget only affects that widget, like giving a single button a different color.

10. When you flip the dark-mode switch in Activity 5, which widget holds the state, and how does the
change reach MaterialApp?
- When I flip the dark‑mode switch in Activity 5, the Switch widget holds the state, and the change reaches MaterialApp because the State class calls setState() and rebuilds the app with the new theme.

 
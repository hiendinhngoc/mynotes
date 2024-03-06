# mynotes

A new Flutter project.

## Registration

## Login

### Firebase Authentication, currentUser

https://pub.dev/documentation/firebase_auth/latest/firebase_auth/FirebaseAuth/currentUser.html

### Navigation

- named routes vs. anonymous routes

  - [named routes](https://docs.flutter.dev/cookbook/navigation/named-routes)
    named routes used to navigate to screens by specifying their names exactly(calling `pushNamed` method):

    ```dart
      MaterialApp(
        routes: {
          '/home': (context) => HomeScreen(),
          '/about': (context) => AboutScreen(),
          '/settings': (context) => SettingsScreen(),
        },
        // Other properties...
      )

      Navigator.of(context).pushNamed('/about');
    ```

  - [anonymous routes](https://docs.flutter.dev/cookbook/navigation/navigation-basics)
    are used to navigate to a page back and forth with `pop` and `push` methods
    ```dart
      Navigator.of(context).push(
        MaterialPageRoute(
          builder: (context) => MyScreen(),
        ),
      );
    ```

- CircularProgressIndicator() https://api.flutter.dev/flutter/material/CircularProgressIndicator-class.html
  - A Material Design circular progress indicator, which spins to indicate that the application is busy.
  - A widget that shows progress along a circle.

## Logout

- NotesView
- AppBar https://api.flutter.dev/flutter/material/AppBar-class.html
  AppBar is usually the topmost component of the app (or sometimes the bottom-most), it contains the toolbar and some other common action buttons.
- PopupMenuButton vs PopupMenuItem
  - PopupMenuButton are used in AppBar to display some quick menu options https://api.flutter.dev/flutter/material/PopupMenuButton-class.html
  - PopupMenuItem are used in PopupMenuButton to display the menu options items https://api.flutter.dev/flutter/material/PopupMenuItem-class.html
- MenuAction
  MenuAction enum is used to define a set of actions that can be associated with the items in the PopupMenuButton within the AppBar of the NotesView widget. The action is triggered in `itemBuilder` callback the pass to `onSelected` callback to handle logout logic inside it.
- Alias for imported method

  - `as` is the keyword to alias an imported package, that mean you can rename the long and ambiguous name from the libary.

  ```dart
  import 'package:flutter/material.dart' as material;

  void main() {
    material.runApp(
      material.MaterialApp(
        home: material.Scaffold(
          body: material.Center(
            child: material.Text('Using Alias in Flutter'),
          ),
        ),
      ),
    );
  }
  ```

  - `show` (AKA whitelist) is the keyword to get specific methods from a package

  ```dart
  import 'package:flutter/services.dart' show PlatformException;

  void main() {
    // You can use PlatformException directly without importing the entire package.
    PlatformException exception = PlatformException(code: '404', message: 'Not found');
  }
  ```

  - `hide` (AKA blacklist) is to exclude methods from a package

  ```dart
  import 'package:flutter/widgets.dart' hide Alignment;

  void main() {
    // You can use widgets from the package except the 'Alignment' class.
  }
  ```

- Display dialog(show, alert)
- Logout from firebase
- Navigate back to login view

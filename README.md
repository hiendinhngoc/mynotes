# mynotes

A new Flutter project.

## Registration

## Login

### Firebase Authentication, currentUser

https://pub.dev/documentation/firebase_auth/latest/firebase_auth/FirebaseAuth/currentUser.html

### Navigation

- named routes vs. anonymous routes
  + [named routes](https://docs.flutter.dev/cookbook/navigation/named-routes)
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
  + [anonymous routes](https://docs.flutter.dev/cookbook/navigation/navigation-basics)
    are used to navigate to a page back and forth with `pop` and `push` methods
    ```dart
      Navigator.of(context).push(
        MaterialPageRoute(
          builder: (context) => MyScreen(),
        ),
      );
    ```
- CircularProgressIndicator() https://api.flutter.dev/flutter/material/CircularProgressIndicator-class.html
  + A Material Design circular progress indicator, which spins to indicate that the application is busy.
  + A widget that shows progress along a circle.

## Logout

- NotesView
- AppBar https://api.flutter.dev/flutter/material/AppBar-class.html
  AppBar is usually the topmost component of the app (or sometimes the bottom-most), it contains the toolbar and some other common action buttons.
- PopupMenuButton vs PopupMenuItem
  
- MenuAction
- Alias for imported method
- Display dialog(show, alert)
- Logout from firebase
- Navigate back to login view

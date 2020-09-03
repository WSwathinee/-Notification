# -Notification
==android>build.gradle==
add import ->
import io.invertase.firebase.messaging.RNFirebaseMessagingPackage;
import io.invertase.firebase.links.RNFirebaseLinksPackage;
import io.invertase.firebase.config.RNFirebaseRemoteConfigPackage;
import io.invertase.firebase.notifications.RNFirebaseNotificationsPackage;

After this line : List<ReactPackage> packages = new PackageList(this).getPackages();
packages.add(new RNFirebaseMessagingPackage());
packages.add(new RNFirebaseLinksPackage());
packages.add(new RNFirebaseRemoteConfigPackage());
packages.add(new RNFirebaseNotificationsPackage());

==android>app>bulid.gradle==
add following depencies

implementation project(‘:react-native-firebase’)
implementation “com.google.android.gms:play-services-base:16.1.0”
implementation “com.google.firebase:firebase-core:16.0.9”
implementation “com.google.firebase:firebase-config:17.0.0”
implementation “com.google.firebase:firebase-invites:17.0.0”
implementation “com.google.firebase:firebase-messaging:18.0.0”
implementation ‘me.leolin:ShortcutBadger:1.1.21@aar’

Here is your updated `path.md` — shortened to match what you actually have now.

---

```markdown
# Complete Beginner's Guide: From Nothing to Running Mobile App

## Step 1: Install VS Code

Go to `code.visualstudio.com` → Download → Install.

## Step 2: Install Node.js

Go to `nodejs.org` → Download the LTS version → Install.

## Step 3: Verify Installation

Open VS Code. Open Terminal: `Terminal` → `New Terminal` (or `Ctrl + `` `).

Type:
```bash
node --version
```
You should see `v20.x.x` or similar.

Type:
```bash
npm --version
```
You should see `10.x.x` or similar.

## Step 4: Create your app

```bash
npx create-expo-app my-app --template blank
```

## Step 5: Go into your app folder

```bash
cd my-app
```

## Step 6: Install web support

```bash
npx expo install react-dom react-native-web
```

## Step 7: Install navigation (for tabs)

```bash
npx expo install @react-navigation/native @react-navigation/bottom-tabs
npx expo install react-native-screens react-native-safe-area-context
```

## Step 8: Open the folder in VS Code

`File` → `Open Folder` → Select `my-app`

## Step 9: Write your first code

Delete everything in `App.js` and paste this:

```js
import { Text, View } from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createBottomTabNavigator } from '@react-navigation/bottom-tabs';

function HomeScreen() {
  return (
    <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center' }}>
      <Text>🏠 Home Screen</Text>
      <Text>Welcome to my first app!</Text>
    </View>
  );
}

function SettingsScreen() {
  return (
    <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center' }}>
      <Text>⚙️ Settings Screen</Text>
      <Text>Your preferences go here</Text>
    </View>
  );
}

const Tab = createBottomTabNavigator();

export default function App() {
  return (
    <NavigationContainer>
      <Tab.Navigator
        screenOptions={({ route }) => ({
          tabBarIcon: ({ focused, color, size }) => {
            if (route.name === 'Home') {
              return <Text style={{ fontSize: size }}>🏠</Text>;
            } else if (route.name === 'Settings') {
              return <Text style={{ fontSize: size }}>⚙️</Text>;
            }
          },
          tabBarActiveTintColor: '#007bff',
          tabBarInactiveTintColor: 'gray',
        })}
      >
        <Tab.Screen name="Home" component={HomeScreen} />
        <Tab.Screen name="Settings" component={SettingsScreen} />
      </Tab.Navigator>
    </NavigationContainer>
  );
}
```

Save: `Ctrl + S`

## Step 10: Run your app in a browser

```bash
npx expo start --web
```

## Step 11: (Optional) Run on your phone

```bash
npx expo start
```
Install Expo Go on your phone. Scan the QR code.

---

## Quick Reference

```bash
# Create
npx create-expo-app my-app --template blank
cd my-app

# Install
npx expo install react-dom react-native-web
npx expo install @react-navigation/native @react-navigation/bottom-tabs
npx expo install react-native-screens react-native-safe-area-context

# Run
npx expo start --web    # browser
npx expo start          # phone
```

You now have a working mobile app running on your computer and phone.
```

---

**That's it. Short. Clean. Only what you actually need.**
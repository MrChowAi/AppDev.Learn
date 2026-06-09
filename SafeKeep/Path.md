Complete Beginner's Guide: From Nothing to Running Mobile App
Prerequisites (Do This First)
Step 1: Install VS Code

Go to code.visualstudio.com → Download → Install. Click "Next" on everything.

Step 2: Install Node.js

Go to nodejs.org → Download the LTS version (left button) → Install. Click "Next" on everything. This installs npm automatically.

Step 3: Verify Installation

Open VS Code. Open Terminal: Terminal → New Terminal (or press Ctrl + ``).

Type:

bash
node --version
You should see v20.x.x or similar.

Type:

bash
npm --version
You should see 10.x.x or similar.

If you see numbers, you're ready. If you see errors, restart your computer and try again.

Create Your App
Step 4: Create the app folder

In the VS Code terminal, type:

bash
npx create-expo-app my-app --template blank
Wait 1-2 minutes.

Step 5: Enter the app folder

bash
cd my-app
Step 6: Install web support (one time only)

bash
npx expo install react-dom react-native-web
Step 7: Install navigation (for tabs)

bash
npx expo install @react-navigation/native @react-navigation/bottom-tabs
npx expo install react-native-screens react-native-safe-area-context
Step 8: Open the folder in VS Code

Either:

File → Open Folder → Select my-app

Or close VS Code and open the folder directly

Write Your First Code
Step 9: Replace App.js

In VS Code, click App.js in the left sidebar. Delete everything. Copy and paste this code:

js
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
Save the file (Ctrl + S).

Run Your App
Step 10: Start the app in browser

bash
npx expo start --web
A browser will open showing your app with two tabs: Home and Settings.

Step 11: Test on your phone (optional)

Stop the server (Ctrl + C). Then run:

bash
npx expo start
Install Expo Go on your iPhone or Android. Scan the QR code with the Expo Go app. Your app appears on your phone.

Push to GitHub
Step 12: Create a GitHub repository

Go to github.com → Sign in → Click the + icon → New repository

Repository name: my-app (or whatever you want)

Description: My first mobile app — learning React Native + Expo

Public (so others can see)

DO NOT check "Add a README" or ".gitignore" or "License" (we'll add them manually)

Click Create repository

Step 13: Initialize Git in your project

In your VS Code terminal (make sure you're in my-app folder), type:

bash
git init
Step 14: Create a .gitignore file

In VS Code, create a new file called .gitignore (exactly that name). Add this:

text
node_modules/
.expo/
.env
.env.local
.DS_Store
*.log
Step 15: Add and commit your code

bash
git add .
git commit -m "First commit: mobile app with bottom tabs"
Step 16: Connect to GitHub

Replace YOUR_USERNAME with your GitHub username and YOUR_REPO_NAME with the repo name you created:

bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git push -u origin main
Step 17: Verify

Go to your GitHub repository page. Refresh. Your code is there.

Summary of Commands (Quick Reference)
bash
# Install Node.js first (visit nodejs.org)

# Create app
npx create-expo-app my-app --template blank
cd my-app
npx expo install react-dom react-native-web
npx expo install @react-navigation/native @react-navigation/bottom-tabs
npx expo install react-native-screens react-native-safe-area-context

# Replace App.js with the code above

# Run in browser
npx expo start --web

# Run on phone (QR code)
npx expo start

# Push to GitHub
git init
git add .
git commit -m "First commit"
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git push -u origin main
What's Missing From Your path.txt
Missing	Add This
VS Code installation	Step 1
Node.js installation	Step 2
Verify installation	Step 3
GitHub repo creation	Step 12
Git init and .gitignore	Steps 13-14
Git add/commit/push	Steps 15-16
License selection	During GitHub repo creation (MIT)
Copy this into your path.txt file. Then run through each step yourself to verify it works. When it does, you have a resource you can share with anyone starting from zero.

give it all in one copy box. I am not asking for steps I am creating steps to where I am not.
markdown
# Complete Beginner's Guide: From Nothing to Running Mobile App

## Prerequisites (Do This First)

**Step 1: Install VS Code**

Go to `code.visualstudio.com` → Download → Install. Click "Next" on everything.

**Step 2: Install Node.js**

Go to `nodejs.org` → Download the LTS version (left button) → Install. Click "Next" on everything.

**Step 3: Verify Installation**

Open VS Code. Open Terminal: `Terminal` → `New Terminal` (or press `Ctrl + `` `).

Type:
```bash
node --version
You should see v20.x.x or similar.

Type:

bash
npm --version
You should see 10.x.x or similar.

Create Your App
Step 4: Create the app folder

bash
npx create-expo-app my-app --template blank
Step 5: Enter the app folder

bash
cd my-app
Step 6: Install web support

bash
npx expo install react-dom react-native-web
Step 7: Install navigation (for tabs)

bash
npx expo install @react-navigation/native @react-navigation/bottom-tabs
npx expo install react-native-screens react-native-safe-area-context
Step 8: Open folder in VS Code

File → Open Folder → Select my-app

Write Your First Code
Step 9: Replace App.js

Delete everything in App.js and paste this:

js
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
Save: Ctrl + S

Run Your App
Step 10: Start in browser

bash
npx expo start --web
Step 11: Test on phone (optional)

bash
npx expo start
Install Expo Go on your phone. Scan QR code.

Push to GitHub
Step 12: Create GitHub repository

Go to github.com → New repository

Name: my-app

No README, no .gitignore, no license (add manually)

Click Create repository

Step 13: Initialize Git

bash
git init
Step 14: Create .gitignore

Create file .gitignore and add:

text
node_modules/
.expo/
.env
.env.local
.DS_Store
*.log
Step 15: Commit your code

bash
git add .
git commit -m "First commit: mobile app with bottom tabs"
Step 16: Connect to GitHub

Replace YOUR_USERNAME and YOUR_REPO_NAME:

bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git push -u origin main
Step 17: Add license (optional but recommended)

On GitHub repo page → Add file → Create new file → Name LICENSE → Choose MIT License → Commit.

Quick Reference (All Commands)
bash
# Create and setup
npx create-expo-app my-app --template blank
cd my-app
npx expo install react-dom react-native-web
npx expo install @react-navigation/native @react-navigation/bottom-tabs
npx expo install react-native-screens react-native-safe-area-context

# Run
npx expo start --web    # browser
npx expo start          # QR code for phone

# Git
git init
git add .
git commit -m "First commit"
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git push -u origin main
You now have a working mobile app running on your computer and phone, with code saved to GitHub.
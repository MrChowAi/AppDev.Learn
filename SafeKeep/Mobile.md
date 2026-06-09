# Mobile App Structure Template

## What is "cloning"?

Cloning means downloading an entire project folder from GitHub to your computer. You get every file, every folder, and the entire history of the project.

## The command

```bash
git clone https://github.com/sajithmym/React-Native-Init
What this does:

Creates a folder called React-Native-Init on your computer

Inside that folder is a complete React Native project with folders already set up for components, screens, navigation, utilities, types, assets, and settings

You don't have to create those folders yourself

After cloning (getting the project onto your computer)
bash
cd React-Native-Init
What this does: Moves you into the newly created folder so you can work inside it.

bash
npm install
What this does: Reads the package.json file and downloads all the external code the project needs (libraries like React, React Native, Expo). Without this step, the app won't run.

bash
npm start
What this does: Starts the development server. You'll see a QR code. Scan it with the Expo Go app on your phone to see the app running.

Why this template is useful
The folder structure is already organized the way professional developers do it:

Folder	What goes in it
src/components/	Reusable pieces like buttons, cards, headers
src/screens/	Full pages like HomeScreen, ProfileScreen
src/navigation/	Code that controls moving between screens
src/utils/	Helper functions (format dates, clean up text)
src/types/	TypeScript definitions (what data looks like)
src/settings.ts	One file with all colors, spacing, and font sizes
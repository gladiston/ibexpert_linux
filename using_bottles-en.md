# IBExpert Installation on Linux Using Bottles

## **INSTALLATION**
Install the **Bottles** software on Linux using any repository (Flathub is recommended).

---

## **CREATE A NEW BOTTLE**
Create a custom bottle with the following specs:

- **Name**: `IBExpert-x32`  
- **Architecture**: 32-bit  
- **Version**: Windows 10/11  
- **Runner**: `soda-9.0.1` (or `sys-wine-10`)

Then select the newly created `IBExpert-x32` bottle, go to the **Dependencies** section, and add:

- `allfonts` (includes essential Microsoft and Adobe fonts)
- `consolas`
- `lucon`
- `vcredist2008`

> ⚠️ **Important**: Avoid installing the following dependencies, as they can break your bottle:
> - `mdac28`
> - another copy of `vcredist2008` like `vcredist2005`, `vcredist2010`,...   
> 
> If you want to test other dependencies, **make a backup** of your bottle first.

Your bottle will be located at: `~/.var/app/com.usebottles.bottles/data/bottles/bottles/IBExpert-x32`.

You can now close the bottle.

---

## **DOWNLOADING**
Place the following installers in your `~/Downloads` folder:

- Firebird Database Client (32-bit version)  
- IBExpert installer  

> ⚠️ Note: Sometimes the Windows installer window opens *behind* the main Bottles window — check carefully.

---

## **INSTALLING INSIDE THE BOTTLE**
Reopen Bottles, select `IBExpert-x32`, and click **Start Program**.

Install the following packages from the `~/Downloads` folder:

1. **Firebird Database Client (x86)**
   - Install to: `C:\fb5`
   - Uncheck “Server Components”
   - Check “Don’t create a Start Menu Folder”
   - Uncheck “Show What’s New after installation”

2. **IBExpert**
   - Use the default installation or install it to your preferred location.

---

## **IBEXPERT - FIRST TIME SETUP**
The first time you run IBExpert, it will ask you to choose between MDI and SDI mode.  
**Choose MDI**, as SDI may not work well on Linux.

Once everything is working, go to **Preferences** in Bottles and enable **“Close bottle after starting program”**.  
This will save you from manually closing the bottle every time.

---

## **CONCLUSION**
After everything is installed and working in the `IBExpert-x32` bottle, **do not change** its settings or add more dependencies.

If you want to test changes, **use the “Clone” option** and modify the cloned bottle instead.

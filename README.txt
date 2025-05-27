# Project:Progetto_BookRecommender

REQUIREMENTS

- Java 11 or newer
- Maven
- PostgreSQL
- JavaFX SDK (version 21) (if you are a macOS user you dont have to preinstall the JavaFX beacuse it is included in the project. (only work for macOS user) 

INSTALLATION & EXECUTION

Option 1: Windows Users

1. Open Command Prompt(cmd) and move to project directory
example: cd Downloads/mavensample/

2. Build the project with Maven:
   mvn clean package

Option 2: Linux / macOS Users

1. Open Command Prompt(cmd) and move to project directory
example: cd ~/Downloads/mavensample/


2. Build the project with Maven:
   mvn clean package

   Or use the provided batch files (you must make sure to change you directory of the .bat / .sh for the javaFX:
	Example:set JAVAFX_PATH=C:\Users\rahul\Desktop\javafx-sdk-21.0.7\lib
	
	(If this .sh dont work and there is permission problem you have to go to the terminal
	and write this command for give the permission.
	xattr -d com.apple.quarantine ./clientMvn.sh
	xattr -d com.apple.quarantine ./client.sh
	xattr -d com.apple.quarantine ./server.sh

   - clientMVN.sh to build and run the client
   - client.sh to run the prebuilt client
   - server.sh to start the server

   Make the scripts executable:
   chmod +x client*.sh server.sh

Beacuse of the modularity introduced in JavaFX starting from Java 11, the client application must be launched with specific module options.
For this reason, the Server.bat/Client.bat scripts for Windows users and Server.sh / Client.sh for macOS users act as launchers for the executable .jar files, respecting of the project's requirements
   Or use the provided batch files:
   - clientMVN.bat to build and run the client
   - client.bat to run the prebuilt client
   - server.bat to start the server

3. Run the JAR manually if needed:
   java --module-path "/path/to/javafx-sdk-21.0.7/lib" \
        --add-modules javafx.controls,javafx.fxml \
        -jar bin/client.jar

To find your JavaFX PATH:
Linux/MacOS: find / -name javafx.base.jar 2>/dev/null
Windows: dir C:\ /s /b javafx.base.jar

DATABASE CONFIGURATION

Host (es. localhost): localhost
Porta (es. 5432): 5432
Nome Database: progetto
Username: your_username
Password: your_password

Make sure PostgreSQL is running and the credentials are correct.

Example:
java --module-path "/Users/mariorossi/javafx-sdk-21.0.7/lib" --add-modules javafx.controls,javafx.fxml -jar bin/progettoLabB-1.0-SNAPSHOT-shaded.jar

NOTES

- Verify the JavaFX path points to the lib directory.
- No JavaFX installation is required for macOS.
- Make sure PostgreSQL is installed and accessible before running the application.



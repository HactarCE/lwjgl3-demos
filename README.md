# HactarCE Libinput bug reproduction demonstration

1. Ensure you have the Java Development Kit installed (e.g. `jdk8-openjdk` in Arch repositories).
2. Clone this repository: `git clone https://github.com/HactarCE/lwjgl3-demos && cd lwjgl3-demos`
2. Build the project: `mvn package`
3. Run the game/demonstration: `java -jar target/lwjgl3-demos.jar`

Game instructions are printed to stdout; here are instructions specifically for testing the cursor jumping bug:

1. Using `xinput`, Xorg configuration, or some other means, set a non-default Coorindate Tranformation Matrix for your mouse device; e.g. `1 0 0 0 1 0 0 0 2`
2. Run the demonstration: `java -jar target/lwjgl3-demos.jar`
3. Press `z` to "disable" the cursor, `x` to "hide" the cursor, and `c` to return the cursor to normal.

Below is the original README.

---

# lwjgl3-demos
Demo suite for LWJGL 3

## Building

    mvn package
    
To override main class

    mvn package -Dclass=opengl.UniformArrayDemo

## Running

    java -jar target/lwjgl3-demos.jar

To override main class

    java -cp target/lwjgl3-demos.jar org.lwjgl.demo.opengl.UniformArrayDemo

# 💾☕️🐧 How to install OpenJDK on Linux

1. Download OpenJDK ([OpenJDK](https://openjdk.org/), [Production and Early-Access OpenJDK Builds, from Oracle](https://jdk.java.net/), [OpenJDK Archive](https://jdk.java.net/archive/))
2. Create directory `/usr/java`
    ```sh
    sudo mkdir -p /usr/java
    ```
3. Move to Downloads
4. Unpack archive
    ```sh
    sudo tar -xzvf openjdk-XXX.tar.gz -C /usr/java
    ```
5. Set environment variables
   1. Open `/etc/profile`
   2. Add lines:
        ```sh
        JAVA_HOME=/usr/java/jdk-XXX
        PATH=$PATH:$HOME/bin:$JAVA_HOME/bin
        export JAVA_HOME
        export JRE_HOME
        export PATH
        ```
6. Check Java version
    ```sh
    java -version
    ```

# 💾☕️🍏 How to install OpenJDK on Mac

1. Download OpenJDK ([OpenJDK](https://openjdk.org/), [Production and Early-Access OpenJDK Builds, from Oracle](https://jdk.java.net/), [OpenJDK Archive](https://jdk.java.net/archive/))
2. Move to Downloads
3. Unpack archive
    ```sh
    sudo tar -xzvf openjdk-XXX.tar.gz -C /Library/Java/JavaVirtualMachines/
    ```
4. Set environment variables
   1. Open `nano ~/.zshrc`
   2. Add line:
        ```sh
        export JAVA_HOME="/Library/Java/JavaVirtualMachines/jdk-XXX/Contents/Home"
        ```
   3. Reload the configuration
        ```sh
        source ~/.zshrc
        ```
5. Check Java version
    ```sh
    java -version
    ```

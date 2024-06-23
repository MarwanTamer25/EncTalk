# EncTalk
Where Your Words Stay Secret and Secure.

![logo](logo.png)

## Abstract

In today's digital era, secure communication channels are paramount for ensuring privacy and confidentiality. This project presents a real-time chat application implemented using Python and the PyQt5 framework, allowing users to exchange text and audio messages securely over the network. The application employs end-to-end encryption based on AES-CFB mode to protect the confidentiality of messages. Additionally, user authentication and password management functionalities are integrated to ensure secure access to the platform. The project utilizes advanced cryptographic techniques and modern networking protocols to provide a seamless and secure communication experience.

## Introduction

With the proliferation of online communication platforms, ensuring the security of sensitive information exchanged between users has become increasingly important. In response to this demand, our project aims to develop a real-time chat application that prioritizes security and privacy without compromising on usability and functionality.

The core features of our chat application include text and audio messaging functionalities, user authentication, and end-to-end encryption of messages. We leverage the PyQt5 framework to create an intuitive and visually appealing user interface, providing a seamless communication experience for our users.

To guarantee the confidentiality of messages, we utilize the AES-CFB encryption algorithm, ensuring that only the intended recipients can decipher the contents of the messages. User authentication mechanisms are implemented to prevent unauthorized access to the application, enhancing overall security.

Through this project, we aim to showcase the importance of incorporating robust security measures into communication applications, thereby safeguarding user privacy in an increasingly interconnected world.

## Libraries Usage in Chatting Application

### PyQt5
PyQt5 serves as the primary framework for building the graphical user interface (GUI) of the real-time chat application. It provides a comprehensive set of tools and modules for designing interactive desktop applications with rich graphical elements and responsive user interfaces.

- **Modules Used**:
  - `PyQt5.QtCore`: Core functionalities such as event handling, timers, and signals/slots. This module enables the application to respond to user interactions and events, ensuring smooth and interactive behavior.
  - `PyQt5.QtGui`: Tools for graphical operations, including drawing shapes, handling colors, managing fonts, and processing input events like mouse clicks and keyboard inputs. This module enhances the visual appeal and interactivity of the application.
  - `PyQt5.QtWidgets`: Components for building GUI elements such as buttons, text fields, labels, layouts, and containers. These widgets provide the building blocks for creating intuitive user interfaces and organizing content effectively.

### Requests
The requests library is employed for making HTTP requests to the server, enabling communication between the client-side application and the backend server. It facilitates tasks such as user authentication, data retrieval, and interaction with the server's API endpoints.

- **Modules Used**:
  - `requests`: The main module for sending HTTP requests with various methods like GET, POST, PUT, DELETE, etc. This module is used to interact with the server's RESTful API endpoints by sending JSON payloads and handling responses.
  - `requests.exceptions`: Contains exception classes for handling errors that may occur during network operations, such as connection timeouts, DNS resolution failures, and HTTP errors. Exception handling ensures robust error management and graceful recovery from network-related issues.
  - `requests.RequestException`: Base class for all exceptions in the requests module. It serves as a catch-all for network-related exceptions during HTTP requests, providing a unified interface for handling errors in the application.

### Cryptography
The cryptography library is utilized for implementing encryption and decryption of messages, ensuring the security and confidentiality of communication between clients and the server. It provides cryptographic primitives and algorithms for secure data transmission.

- **Modules Used**:
  - `cryptography.hazmat.primitives.ciphers`: Contains implementations of cryptographic cipher algorithms such as AES (Advanced Encryption Standard). This module is used for encrypting and decrypting messages using symmetric-key encryption.
  - `cryptography.hazmat.primitives.kdf.pbkdf2`: Provides the PBKDF2-HMAC key derivation function for deriving cryptographic keys from passwords. Key derivation ensures secure handling of passwords and strengthens the security of encryption.
  - `cryptography.hazmat.primitives.hashes`: Implements cryptographic hash functions such as SHA-256 for hashing passwords and generating random salts. Hashing is used to securely store passwords and generate unique identifiers for cryptographic operations.
  - `cryptography.hazmat.backends.default_backend`: Provides access to the default cryptographic backend for the system. It abstracts away the underlying cryptographic implementation details and ensures compatibility across different platforms and environments.

### Socketio
socketio enables real-time bidirectional communication between clients and the server using WebSockets, facilitating instant messaging and updates in the chat application. It provides a reliable and efficient communication mechanism for delivering messages in real-time.

- **Modules Used**:
  - `socketio.Client`: The main class for creating WebSocket clients, allowing bidirectional communication with the server. This module establishes and manages WebSocket connections, sends and receives messages, and handles various events such as connection status changes and incoming messages.
  - `socketio.exceptions`: Contains exception classes for handling errors specific to the socketio library. Exception handling ensures robust error management during socket-related operations, such as connection failures or server-side errors.

### Base64
The base64 module is utilized for encoding and decoding binary data in a URL-safe format. It ensures the safe transmission of encrypted messages over network protocols by encoding binary data in a format that is compatible with URL encoding and decoding.

- **Modules Used**:
  - `base64.urlsafe_b64encode`, `base64.urlsafe_b64decode`: Functions for encoding and decoding binary data in a URL-safe manner. These functions are used to encode encrypted messages before transmission and decode received messages for decryption, ensuring data integrity and compatibility with network protocols.

### SoundDevice
The sounddevice library is used for capturing audio input from the microphone.

- **Modules Used**:
  - `sd.InputStream`: This class is used to create an input stream for recording audio. The stream is started and stopped to manage the recording session.
  - `sd.InputStream(callback=self.audio_callback)`: An instance of InputStream is created with a callback function `audio_callback` to handle the audio data as it is captured.

### scipy.io.wavfile
The scipy.io.wavfile library is used for writing the recorded audio data to a .wav file.

- **Modules Used**:
  - `write(filename, rate, data)`: This function writes the audio data to a file with the given sample rate.

### pygame
The pygame library is used for playing back audio files.

- **Modules Used**:
  - `pygame.mixer.init()`: Initializes the mixer module.
  - `pygame.mixer.music.load(filename)`: Loads the audio file specified by filename.
  - `pygame.mixer.music.play()`: Starts playing the loaded audio file.
  - `pygame.mixer.music.stop()`: Stops the currently playing audio.

## Installation

To install and run this application, follow these steps:

1. **Clone the repository**:
   ```sh
   git clone https://github.com/yourusername/realtime-secure-chat.git
   cd realtime-secure-chat
   ```

2. **Create a virtual environment**:
   ```sh
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```

3. **Install dependencies**:
   ```sh
   pip install -r requirements.txt
   ```

4. **Run the application**:
   ```sh
   python main.py
   ```

## Usage

Once the application is running, you can:

1. **Register** as a new user or **log in** with existing credentials.
2. **Send text messages** to other users in real-time.
3. **Send and receive audio messages**.
4. Enjoy **end-to-end encryption** for all messages to ensure privacy and confidentiality.

## Contributing

Contributions are welcome! To contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/your-feature-name`.
3. Make your changes and commit them: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature/your-feature-name`.
5. Open a pull request.

Please make sure your code adheres to our coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

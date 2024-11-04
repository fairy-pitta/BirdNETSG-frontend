# BirdNETSG-frontend

## Overview
This app is designed to identify bird calls specific to Singapore. Users can record bird sounds in real-time, view spectrograms, receive species identification with confidence intervals, playback recordings, and store recordings offline if there’s a connectivity issue. The app offers three model options: a whole offline model, a student lite model, and a completely online model, allowing users to choose based on device capacity and internet connectivity.

## Functional Requirements

### Core Features
1. **Real-time Spectrogram Generation**
   - As soon as recording starts, a real-time spectrogram should be generated and displayed, providing visual feedback on the audio being recorded.

2. **Species Identification with Confidence Interval**
   - Once recording is complete, the app will identify the bird species and show the result along with a confidence interval. The identification will utilize one of the three model options chosen by the user:
     - **Whole Offline Model**: Full model for high accuracy, running entirely on the device.
     - **Student Lite Model**: Smaller, optimized model with reduced accuracy, running on the device.
     - **Completely Online Model**: Full identification process occurs via API on the backend server.

3. **Audio Playback**
   - Users can play back the recorded audio within the app immediately after recording or later from saved files.

4. **In-App Recording**
   - Users can record audio directly within the app. External recording apps are not needed, making the experience seamless.

5. **Offline Storage of Recordings**
   - In case of connectivity issues, recordings should be saved locally for later processing or upload.

### User Interface (UI) and User Experience (UX)
- **Simple, Intuitive UI**: The app should have a clean and straightforward interface that guides the user through the steps of recording, identifying, and viewing results.
- **Settings Screen**: Allow users to easily access settings for model choice, notifications, and recording quality.
- **Feedback Mechanism**: Display visual progress indicators during recording and spectrogram generation for real-time user feedback.

### Model Choice and Configuration
- **Model Selection Wizard**: On first launch, guide users in choosing the best model based on device specifications and storage.
- **Switching Models**: Allow users to easily switch between offline, lite, and online models from the settings menu.
- **Automatic Fallback**: In cases where the offline model is slow or not supported by the device, suggest switching to a lite or online model.

## Technical Requirements

### Performance Optimization
- **Device Compatibility**: The app should dynamically adjust to device specifications to ensure smooth performance, particularly on low-spec devices.
- **Battery Efficiency**: Optimize real-time spectrogram generation and model inference to minimize battery drain.
- **Latency Minimization**: Ensure minimal latency in spectrogram generation and identification, even on older devices.

### Data Management and Privacy
- **Recording Management**: Users should have control over recording storage, with options to save, delete, or back up locally or on the cloud.
- **Data Privacy**: Ensure data privacy for online model users by clearly explaining how data is handled and obtaining user consent for data uploads.

### Notifications and Alerts
- **Identification Completion Notification**: Notify users when identification is complete.
- **Connection Status Alerts**: Notify users if internet connectivity is unstable when using the online model.

### Error Handling and Debugging
- **Error Messaging**: Display clear error messages and retry options if identification fails or if recording encounters issues.
- **Logging and Diagnostics**: Enable local logging for debugging purposes, allowing users to send logs (with consent) for issue resolution.

## Testing and Quality Assurance

### Device Testing
- Test the app across a range of devices to ensure performance consistency, especially for low-spec devices using the student lite model.
  
### User Feedback Collection
- Include a feedback mechanism for beta testers to submit usability issues or model accuracy concerns.

## Future Considerations
- **Model Updates**: Enable remote updates for the online model to improve accuracy as new data becomes available.
- **Hybrid Model Mode**: For users who go offline intermittently, consider developing a hybrid mode that allows temporary offline functionality with automatic upload when online.

## Additional Notes
- Ensure compliance with app store guidelines for data privacy and permissions.
- Prioritize accessibility features for inclusive user experience.

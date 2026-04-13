# UNITH Head Video Upload Dashboard

A web-based dashboard for uploading custom head videos to UNITH.ai accounts with authentication and API integration.

## Features

- **Authentication**: Secure login using UNITH email and secret key to obtain Bearer tokens
- **File Upload**: Drag-and-drop or browse file selection for video uploads
- **Progress Tracking**: Real-time upload progress with visual indicators
- **Processing Status**: Monitor the status of uploaded videos
- **Responsive Design**: Works on desktop and mobile devices
- **UNITH Branding**: Consistent styling with UNITH's dark blue theme

## Usage

1. **Authentication**:
   - Enter your UNITH account email
   - Enter your secret key (obtained from UNITH interface)
   - Click "Authenticate & Get Token"

2. **Upload Video**:
   - Drag and drop a video file or click "Browse Files"
   - Supported formats: MP4, MOV, AVI
   - Maximum file size: 1000MB
   - Click "Upload Video" to start the upload

3. **Monitor Progress**:
   - Watch the upload progress bar
   - View processing status in the dashboard
   - Check status messages for success/error notifications

## Technical Details

- **Frontend**: HTML5, Tailwind CSS, Vanilla JavaScript
- **API Integration**: UNITH Platform API
- **Authentication**: Bearer token-based
- **File Handling**: XMLHttpRequest with progress tracking
- **Styling**: Dark theme with glassmorphism effects

## API Endpoints Used

- `POST /auth/token` - Obtain Bearer token
- `POST /head-visuals/upload` - Upload video file

## File Requirements

- **Format**: MP4, MOV, or AVI
- **Size**: Maximum 1000MB
- **Content**: Head/face video for digital human creation
- **Quality**: High resolution recommended (1080p or higher)

## Security Notes

- Secret keys are not stored locally
- Bearer tokens are kept in memory only
- All API calls use HTTPS
- Files are uploaded directly to UNITH servers

## Browser Support

- Modern browsers with ES6+ support
- File API support required
- XMLHttpRequest with progress events

## Development

To run locally:
```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/upload-dashboard.html` in your browser.
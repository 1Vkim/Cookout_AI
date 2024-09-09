
# Meal suggestion and Video Generation using Kling and Luma API

This project demonstrates how to generate a meal suggestion,instructions and cooking videos using the Gemini,Kling and Luma API. The script takes ingredients available then churns out cooking instructions which are then sent as request to the Kling API, and polls for the video status until the video is ready.

## Features
- Get meal suggestion from Gemini through ingredients available.
- Generate a video based on cooking instructions.
- Uses Kling API for authentication and Luma API for video generation.
- Polls the server for video status and retrieves the generated video once ready.

## Requirements

1. Python 3.x
2. `http.client` and `json` libraries (pre-installed with Python)
3. A valid Kling API key

## Setup

1. Clone the repository or copy the script files.
   
   ```bash
   git clone https://github.com/1Vkim/Cookout_AI.git
   cd Cookout_AI
   ```

2. Set your API key.

   Replace `KLING_API_KEY` in the script with your Kling API key.

   ```python
   KLING_API_KEY = 'your-api-key-here'
   ```

## How to Run

1. Run the script using Python:

   ```bash
   python Cookout_AI.py
   ```

2. The script will prompt you to enter ngredients you have:

   ```bash
   Enter ingredients: .
   ```
3. The script will send a request for a meal suggestions and instructions to follow.
4. The script will then send a request to generate the video and poll for its status every 5 seconds until the video is ready.

5. Once the video is generated, the URL to the video will be printed in the console.

## Example

```bash
$ python video_generation.py
Enter ingredients: "".
Task ID: abc123
Polling response: {'status': 'pending', ...}
Polling response: {'status': 'completed', 'generation': {'video': 'http://example.com/video.mp4'}}
Video URL: http://example.com/video.mp4
```

## Troubleshooting

- If the script returns `"Error: Video generation timed out. Try again later."`, it means the video took too long to generate. You can increase the polling duration or try again later.
- Ensure you have a valid API key by visiting the [Kling API Documentation](https://api.piapi.ai/docs).

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
```

### Steps:
1. Update the `KLING_API_KEY` placeholder with your actual API key.
2. Rename the script file (e.g., `video_generation.py`).
3. Add this README file to your repository.

Feel free to adjust the instructions or project name as needed!

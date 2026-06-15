# caption-tool
Caption Tool
# Caption Tool App

Build a web app that lets users upload an MP4 video, automatically generate captions, customize caption styling, translate non-English captions into English, and export a final MP4 with captions burned into the video.

Use Next.js, React, TypeScript, Tailwind CSS, FFmpeg, Local Whisper or faster-whisper, and Remotion or FFmpeg for final video rendering.

The user should be able to upload an MP4 file, preview the uploaded video, choose Landscape or Vertical Social Media format, automatically transcribe the video audio, detect the spoken language, generate timed captions, edit the caption text, customize the caption style, move captions around the video preview, resize captions, and export a final MP4 with captions burned into the video while preserving the original audio.

Caption timing should use this format:

[
  {
    "word": "Hello",
    "start": 0.0,
    "end": 0.4
  },
  {
    "word": "world",
    "start": 0.4,
    "end": 0.8
  }
]

If the detected spoken language is not English, show this message:

"This video appears to contain non-English speech. Would you like to translate the captions to English?"

If the user chooses yes, translate the captions into English while keeping the original caption timing.

For landscape videos, use this default caption style:

{
  fontFamily: "Bebas Neue",
  fontColor: "#FFFFFF",
  fontSize: 54,
  textTransform: "uppercase",
  textAlign: "center",
  positionX: 50,
  positionY: 85,
  shadowColor: "rgba(0,0,0,0.9)",
  shadowBlur: 8,
  outlineColor: "rgba(0,0,0,0.9)",
  outlineWidth: 2
}

Landscape captions should have white fill, Bebas Neue font, soft black outline, soft black shadow, 90% shadow opacity, and should sit at the bottom center of the frame. Keep captions beneath the speaker while preserving clean white space and making sure the speaker remains the visual focus. The user must still be able to move the captions and increase or decrease caption size.

For vertical social media videos, captions should default to the lower bottom third, centered, with the ability to move and resize them. Vertical captions should support word-by-word highlighting as the speaker says each word.

Include these five vertical caption presets:

Clean White: white text with black shadow.

Yellow Pop: white inactive words, yellow active word, black outline.

Creator Bold: large uppercase white text with thick black outline.

News Lower Third: white text over a subtle translucent dark background box.

High Contrast: black text over a white rounded background box.

The app should include an upload screen with MP4 upload, video preview, Landscape or Vertical selector, and Generate Captions button.

The app should include a caption editor screen with video preview, caption overlay, editable caption text, font dropdown, text color picker, highlight color picker, outline width slider, shadow opacity slider, font size slider, position X slider, position Y slider, style preset buttons, and translation option if language is not English.

The app should include an export screen with Render Final Video button, loading/progress state, and Download MP4 button.

Keep the code simple and beginner-friendly. Add comments explaining what each important file does. Do not require an OpenAI API key. The first version should work locally. Make sure npm run dev starts the app. Make sure uploaded MP4 preview works. Make sure captions can be edited and styled before export. Make sure the final exported MP4 includes burned-in captions.

Suggested build approach: first create the upload and preview flow, then add mock captions, then add caption styling and positioning, then add local Whisper transcription, then add language detection and translation, then add final MP4 export.

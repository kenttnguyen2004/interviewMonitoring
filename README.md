# Interview Studio & Screen Focus Research

**Python · OpenCV · MediaPipe · faster-whisper · ReportLab · pytest**

A local research prototype that combines webcam-based head and iris measurements with interview recording, timestamped transcription, question markers, and session reports.

**Repository status:** This repository is a demo and report showcase. The application source and test suite are not currently included here.

## Explore the project

- [Watch the interview-monitoring demo](Kent-InterviewMonitoring.mp4)
- [Watch the question-transcription test](Kent%20Nguyen%20-%20IM%20Testing.mp4) — Kent reads generic interview questions for the transcript and question-detection workflow.
- [Read the sample project report](KentInterviewMonitoringReport.pdf)

If GitHub does not play a video inline, download the file to view it locally.

## What I built

### Interview Studio
- A desktop interface for webcam preview and microphone selection.
- Threaded audio/video recording with a shared session clock.
- Local English speech transcription using faster-whisper.
- Manual question markers and optional rule-based detection of question-like caption openings.
- Timestamped transcripts, descriptive per-question summaries, and HTML/PDF reports.
- Debug views for landmarks, head angles, iris ratios, and tracking availability.

### Screen Focus Research
- Coarse head-orientation estimates using OpenCV and MediaPipe facial landmarks.
- Personal head-center calibration, smoothing, and persistent direction labels.
- A separate five-target gaze-calibration and validation workflow.
- Controlled exercises comparing eye movement, head movement, and natural movement.

## Engineering approach

The local implementation separates camera capture, landmark processing, head-pose estimation, gaze calibration, recording, session data, question detection, and report generation into Python modules. Its pytest suite covers tracking, calibration, question detection, recording, and report generation.

Claude supports architecture, coding, debugging, and documentation during development. Speech transcription runs through faster-whisper; automatic question markers use English text heuristics.

## Scope and limitations

This is an experimental prototype, not a validated attention or cheating detector. Head orientation and iris offset do not establish attention, honesty, engagement, or candidate suitability. Lighting, glasses, camera placement, and ordinary movement can affect measurements.

Captions are English-only and do not separate speakers. Automatic question markers can miss questions or create incorrect boundaries and should be checked against the recording.

Interview Studio processes recordings locally after model setup and saves media and reports when recording is started. The separate research interface exports aggregate PDF/JSON reports without recording audio or video.

## Author

[Kent Nguyen](https://github.com/kenttnguyen2004) · [LinkedIn](https://www.linkedin.com/in/kent-nguyen-369a1823b/)

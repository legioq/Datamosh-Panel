
Project Workflow – DatamoshPanel macOS App

For this project, I created a complete macOS application called DatamoshPanel, which allows users to apply datamosh effects to video files with an interactive GUI. Here is the step-by-step summary of my work:
	1.	Project Setup:
	•	I structured the project as a Swift Package so it can be easily opened in Xcode.
	•	I created necessary folders for sources, resources (including Metal shaders), scripts, and packaging.
	2.	User Interface (GUI):
	•	I designed a GUI using AppKit with buttons, progress bar, drag-and-drop support, checkboxes, and a popup menu to select export formats.
	•	The GUI allows users to select a video, apply effects, and monitor progress.
	3.	Metal Shader Integration:
	•	I implemented a basic Metal shader (glitch.metal) to apply pixelation and glitch effects to the video preview.
	•	The shader rounds UV coordinates for pixelation and adds a sine-based color shift for glitch effects.
	4.	FFmpeg Integration:
	•	I created a helper script (ffmpeg_datamosh.sh) to handle video processing with FFmpeg.
	•	The workflow splits the video into two parts, applies long GOP encoding for the datamosh effect, and then concatenates the parts.
	5.	Datamosh Functionality:
	•	The application supports datamosh effects with options like pixelation, glitch shader, long GOP, and sharp I-frame breaks.
	•	Users can export videos in different formats (MOV, MP4, MKV).
	6.	Packaging and Installer:
	•	I included a make_pkg.sh script to create a .pkg installer for easy installation on macOS.
	•	Instructions and scripts were added for building a universal .app that works on both Apple Silicon and Intel Macs.
	7.	Documentation:
	•	I provided a README explaining installation, usage, and building steps.
	•	All scripts and resources were included to ensure the app is functional and ready for compilation.

Summary:
The project combines Swift, AppKit, Metal, and FFmpeg to provide a fully functional datamosh application for macOS. The GUI, shader effects, and FFmpeg automation create a user-friendly tool for experimental video editing. The project is packaged with scripts to build a universal .app and installer .pkg.

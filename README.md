<p align="center">
  <img src="assets/icon.png" alt="ListenMe Logo" width="140" height="140">
</p>

<h1 align="center">ListenMe Player — Open Edition</h1>

<p align="center">
  Advanced Flutter audio player focused on precise playback control,
  modular architecture and performance-oriented UI design.<br>
  Precision navigation • Silence analysis • Fully customizable UI
</p>

<p align="center">
  <!-- Badges -->
  <img src="https://img.shields.io/badge/Flutter-3.x-blue?logo=flutter&logoColor=white" alt="Flutter">
  <img src="https://img.shields.io/badge/Platform-Android-green?logo=android&logoColor=white" alt="Platform Android">
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="MIT License">
  <img src="https://img.shields.io/badge/Open%20Edition-Source%20Code-lightgrey" alt="Open Edition">
</p>

---

> Open Edition of ListenMe Player.  
> Original project repository: https://github.com/fliteIn/flitein

---

**ListenMe Player** is a cross-platform Flutter audio player designed for users
who require fine-grained control over audio playback.
The application combines precise navigation tools, silence analysis
and a deeply customizable UI.


This repository contains an **open (reduced) edition** of the project.  
Some private modules (premium logic, ads, Firebase configuration, service keys) are intentionally excluded.

> 🎯 **Goal of the Open Edition**  
> To showcase architectural decisions, state modeling, UI/UX trade-offs,
> audio processing techniques and performance-oriented engineering.



## ✨ Features

The feature list below highlights the functional scope of the application.  
The primary focus of this repository, however, is the underlying architecture,
state management and custom UI engineering.

<table> 
  <tr> 
    <!-- Левая колонка (фичи) --> 
    <td style="vertical-align: top; width: 60%"> 
      <h3>🎧 Playback & Navigation</h3> 
      <ul> 
        <li>Segment playback between markers with fine adjustment</li> 
        <li>Jump between silence regions</li> 
        <li>Playback with skip functions and smooth scrubbing</li> 
        <li>Jog wheel with precise rewind buttons (continuous speed control)</li> 
        <li>Fully configurable playback speed</li> 
      </ul> 
      <h3>🔍 Silence & PCM Analysis</h3> 
      <ul> 
        <li>Local audio analysis</li> 
        <li>PCM level map generation</li> 
        <li>Silence detection</li> 
        <li>Adjustable silence threshold</li> 
        <li>Real-time loudness visualization</li> 
      </ul> <h3>🎛 UI Customization</h3> 
      <ul> 
        <li>Full theme editor</li> 
        <li>Adjustable colors, gradients, and shadows</li> 
        <li>Configurable widget layout with drag-and-drop</li> 
        <li>Customizable speed ranges (playback + seek)</li> 
        <li>Background image support</li> </ul> <h3>📁 Playlists</h3> 
      <ul> <li>Folder-based playlist with subfolder navigation</li> 
        <li>Manual playlist with drag-and-drop reordering</li> <li>Audio tag metadata parsing</li> 
        <li>Persistent playlist source memory</li> 
        <li>Playback modes: singleOnce, singleLoop, playlistOnce, playlistLoop, shuffle</li> 
      </ul> 
      <h3>💾 Cache</h3> 
      <ul> <li>Adjustable cache size</li> 
        <li>Custom retention time</li> 
        <li>Clear cache function</li> 
      </ul> 
      <h3>🎚 Equalizer</h3> 
      <ul> 
        <li>Full equalizer with presets</li> 
        <li>Custom user-defined settings</li> 
      </ul> 
      <h3>📖 Help</h3> 
      <ul> 
        <li>Built-in help section describing each UI element and screen</li> 
      </ul> 
    </td> <!-- Правая колонка (GIF) --> 
    <td style="vertical-align: top; text-align: center; width: 40%"> 
      <table>
        <tr>
          <td align="center">
            <h3>Jog</h3>
            <img src="assets/Jog.gif" width="220" style="border-radius: 12px; margin: 4px;">
          </td>
          <td align="center">
            <h3>Markers</h3>
            <img src="assets/Markers.gif" width="220" style="border-radius: 12px; margin: 4px;">
          </td>
        </tr>
        <tr>
          <td align="center">
            <h3>Screen edit</h3>
            <img src="assets/Screen_edit.gif" width="220" style="border-radius: 12px; margin: 4px;">
          </td>
          <td align="center">
            <h3>Playlist</h3>
            <img src="assets/Playlist.gif" width="220" style="border-radius: 12px; margin: 4px;">
          </td>
        </tr>
      </table>
    </td> 
  </tr> 
</table>


## 🧱 Architecture

The application is built around explicit state models and a clear separation
of responsibilities, with a single root coordinator and domain-specific models.

State models:

- **AppModel** — root coordinator
- **PlaybackModel** — playback logic and just_audio integration
- **PlaylistModel** — playlist and source management
- **AudioToLevelsModel** — PCM & silence analysis
- **AppThemeColors** — theming system
- **DisplayWidgetConfig** — UI layout configuration

Modular UI:

- **widgets/** — jog wheel, sliders, control panels
- **ui/** — app screens
- **utils/** — helpers
- **l10n/** — localization
- **assets/** — images and backgrounds

---

## ⚠️ Open Edition Status

As this is an Open Edition, some commercial and confidential modules
(monetization, ads, Firebase configuration) are excluded.

The repository focuses on **architecture, state management and UI implementation**,
rather than providing a fully production-ready build.

---

## 🗣 Feedback

If you have questions about the architecture, audio processing, state management, or UI,  
feel free to open an **Issue** or start a **Discussion** in the repository.

---

## 📲 Install the App

The full application is available on Google Play:

[<img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png"
alt="Get it on Google Play" height="80">](https://play.google.com/store/apps/details?id=com.listenme.player)

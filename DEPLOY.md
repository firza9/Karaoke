# Karaoke Studio — setup

This is a **static website**. No npm install or build command is needed.

## Deploy with Netlify
1. In Netlify, choose **Add new project → Import an existing project → GitHub**.
2. Select **firza9/Karaoke**, branch **main**.
3. Leave **Build command** and **Publish directory** blank (or use `.` as publish directory if required).
4. Deploy the site. Open the **same HTTPS Netlify URL** on your laptop.
5. Scan the QR code with your iPhone, tap **Start microphone**, allow Safari microphone access, and press **Accept mic** on the laptop.
6. Open YouTube in a separate laptop tab and play a karaoke track.

## Effects
The laptop browser mixes live microphone audio with volume, bass, treble, reverb, and echo. YouTube music plays separately through the same selected laptop speaker/output.

## Important limitations
- Keep the microphone page open and the phone awake.
- Wired speakers usually have lower latency than Bluetooth; Wi-Fi/WebRTC can still introduce a delay.
- Use low speaker volume first and keep the phone away from speakers to avoid acoustic feedback.
- Both devices need working internet access because the free PeerJS signaling service is used for pairing.
- This proof of concept uses public PeerJS signaling and has **not** been end-to-end tested with a physical iPhone/laptop. It is not a production-grade or authenticated system.
- If the phone microphone does not connect through a restrictive network, the connection may require a TURN relay; this version does not configure one.

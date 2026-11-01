# huroof-voices

Recorded narration voices for the Huroof (حروفي) iPad app, which teaches
children to write Arabic and English letters.

The app downloads one `<voice>.pack` when the parent picks that voice in
settings, then plays it without internet. `voices.json` lists the voices
that are ready, with their size and version.

A pack is `HRV1`, the length of a JSON index (4 bytes, little-endian), the
index `{key: [offset, length]}`, then the MP3 clips. A clip's key is the
first 32 hex digits of SHA-256 of `"<lang>|<sentence>"`.

The voices were made with ElevenLabs; this repository holds audio only.

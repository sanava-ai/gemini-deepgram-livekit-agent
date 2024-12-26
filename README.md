<a href="https://livekit.io/">
  <img src="./.github/assets/livekit-mark.png" alt="LiveKit logo" width="100" height="100">
</a>

# Python Voice Agent

<p>
  <a href="https://cloud.livekit.io/projects/p_/sandbox"><strong>Deploy a sandbox app</strong></a>
  •
  <a href="https://docs.livekit.io/agents/overview/">LiveKit Agents Docs</a>
  •
  <a href="https://livekit.io/cloud">LiveKit Cloud</a>
  •
  <a href="https://blog.livekit.io/">Blog</a>
</p>

This Voice AI assistant is completely free to use.⁣
⁣
𝐇𝐨𝐰 𝐢𝐬 𝐭𝐡𝐢𝐬 𝐩𝐨𝐬𝐬𝐢𝐛𝐥𝐞?⁣

👉 It’s hosted on LiveKit, which offers 5,000 free minutes per month.⁣</a>

👉 It uses Gemini 2.0 Flash as the LLM, which is currently free.⁣</a>

👉 For TTS and STT, it relies on Deepgram, which provides a $200 credit that practically lasts forever—pretty cool, right?⁣</a>

It also uses LiveKit's new transformer model, which intelligently determines when a user is done speaking and when the AI can respond without unintentionally interrupting. 

Unlike conventional voice agents that rely on Voice Activity Detection (VAD) models—often oblivious to the context of pauses—the transformers model takes conversational nuances into account for a smoother experience.
⁣
Sure, the latency and voice quality aren’t perfect, but hey, it gets the job done without costing a dime!⁣

Demo here: https://www.linkedin.com/feed/update/urn:li:activity:7278023588362747904/
⁣

## Dev Setup

Clone the repository and install dependencies to a virtual environment:

```console
cd gemini-deepgram-livekit-agent
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Set up the environment by copying `.env.example` to `.env.local` and filling in the required values:

- `LIVEKIT_URL`
- `LIVEKIT_API_KEY`
- `LIVEKIT_API_SECRET`
- `DEEPGRAM_API_KEY`
- `GOOGLE_APPLICATION_CREDENTIALS`
- `GOOGLE_CLOUD_PROJECT`

You can also do this automatically using the LiveKit CLI:

```console
lk app env
```

Run the agent:

```console
python3 agent.py dev
```

This agent requires a frontend application to communicate with. You can use one of our example frontends in [livekit-examples](https://github.com/livekit-examples/), create your own following one of our [client quickstarts](https://docs.livekit.io/realtime/quickstarts/), or test instantly against one of our hosted [Sandbox](https://cloud.livekit.io/projects/p_/sandbox) frontends.

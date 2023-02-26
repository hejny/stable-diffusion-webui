`--data-dir` base path where all user data is stored

`--config` path to config which constructs model

`--ckpt` path to checkpoint of stable diffusion model; if specified, this checkpoint will be added to the list of checkpoints and loaded

`--ckpt-dir` Path to directory with stable diffusion checkpoints

`--vae-dir` Path to directory with VAE files

`--gfpgan-dir` GFPGAN directory

`--gfpgan-model` GFPGAN model file name

`--no-half` do not switch the model to 16-bit floats

`--no-half-vae` do not switch the VAE model to 16-bit floats

`--no-progressbar-hiding` do not hide progressbar in gradio UI (we hide it because it slows down ML if you have hardware acceleration in browser)

`--max-batch-count` maximum batch count value for the UI

`--embeddings-dir` embeddings directory for textual inversion (default: embeddings)

`--textual-inversion-templates-dir` directory with textual inversion templates

`--hypernetwork-dir` hypernetwork directory

`--localizations-dir` localizations directory

`--allow-code` allow custom script execution from webui

`--medvram` enable stable diffusion model optimizations for sacrificing a little speed for low VRM usage

`--lowvram` enable stable diffusion model optimizations for sacrificing a lot of speed for very low VRM usage

`--lowram` load stable diffusion checkpoint weights to VRAM instead of RAM

`--always-batch-cond-uncond` disables cond/uncond batching that is enabled to save memory with --medvram or --lowvram

`--unload-gfpgan` does not do anything.

`--precision` evaluate at this precision

`--upcast-sampling` upcast sampling. No effect with --no-half. Usually produces similar results to --no-half with better performance while using less memory.

`--share` use share=True for gradio and make the UI accessible through their site

`--ngrok` ngrok authtoken, alternative to gradio --share

`--ngrok-region` The region in which ngrok should start.

`--enable-insecure-extension-access` enable extensions tab regardless of other options

`--codeformer-models-path` Path to directory with codeformer model file(s).

`--gfpgan-models-path` Path to directory with GFPGAN model file(s).

`--esrgan-models-path` Path to directory with ESRGAN model file(s).

`--bsrgan-models-path` Path to directory with BSRGAN model file(s).

`--realesrgan-models-path` Path to directory with RealESRGAN model file(s).

`--clip-models-path` Path to directory with CLIP model file(s).

`--xformers` enable xformers for cross attention layers

`--force-enable-xformers` enable xformers for cross attention layers regardless of whether the checking code thinks you can run it; do not make bug reports if this fails to work

`--xformers-flash-attention` enable xformers with Flash Attention to improve reproducibility (supported for SD2.x or variant only)

`--deepdanbooru` does not do anything

`--opt-split-attention` force-enables Doggettx's cross-attention layer optimization. By default, it's on for torch cuda.

`--opt-sub-quad-attention` enable memory efficient sub-quadratic cross-attention layer optimization

`--sub-quad-q-chunk-size` query chunk size for the sub-quadratic cross-attention layer optimization to use

`--sub-quad-kv-chunk-size` kv chunk size for the sub-quadratic cross-attention layer optimization to use

`--sub-quad-chunk-threshold` the percentage of VRAM threshold for the sub-quadratic cross-attention layer optimization to use chunking

`--opt-split-attention-invokeai` force-enables InvokeAI's cross-attention layer optimization. By default, it's on when cuda is unavailable.

`--opt-split-attention-v1` enable older version of split attention optimization that does not consume all the VRAM it can find

`--disable-opt-split-attention` force-disables cross-attention layer optimization

`--disable-nan-check` do not check if produced images/latent spaces have nans; useful for running without a checkpoint in CI

`--use-cpu` use CPU as torch device for specified modules

`--listen` launch gradio with 0.0.0.0 as server name, allowing to respond to network requests

`--port` launch gradio with given server port, you need root/admin rights for ports < 1024, defaults to 7860 if available

`--show-negative-prompt` does not do anything

`--ui-config-file` filename to use for ui configuration

`--hide-ui-dir-config` hide directory configuration from webui

`--freeze-settings` disable editing settings

`--ui-settings-file` filename to use for ui settings

`--gradio-debug` launch gradio with --debug option

`--gradio-auth` set gradio authentication like "username:password"; or comma-delimit multiple like "u1:p1,u2:p2,u3:p3"

`--gradio-img2img-tool` does not do anything

`--gradio-inpaint-tool` does not do anything

`--opt-channelslast` change memory type for stable diffusion to channels last

`--styles-file` filename to use for styles

`--autolaunch` open the webui URL in the system's default browser upon launch

`--theme` launches the UI with light or dark theme

`--use-textbox-seed` use textbox for seeds in UI (no up/down, but possible to input long seeds)

`--disable-console-progressbars` do not output progressbars to console

`--enable-console-prompts` print prompts to console when generating with txt2img and img2img

`--vae-path` Checkpoint to use as VAE; setting this argument disables all settings related to VAE, default=None

`--disable-safe-unpickle` disable checking pytorch models for malicious code

`--api` use api=True to launch the API together with the webui (use --nowebui instead for only the API)

`--api-auth` Set authentication for API like "username:password"; or comma-delimit multiple like "u1:p1,u2:p2,u3:p3"

`--api-log` use api-log=True to enable logging of all API requests

`--nowebui` use api=True to launch the API instead of the webui

`--ui-debug-mode` Don't load model to quickly launch UI

`--device-id` Select the default CUDA device to use (export CUDA_VISIBLE_DEVICES=0,1,etc might be needed before)

`--administrator` Administrator rights

`--cors-allow-origins` Allowed CORS origin(s) in the form of a comma-separated list (no spaces)

`--cors-allow-origins-regex` Allowed CORS origin(s) in the form of a single regular expression

`--tls-keyfile` Partially enables TLS, requires --tls-certfile to fully function

`--tls-certfile` Partially enables TLS, requires --tls-keyfile to fully function

`--server-name` Sets hostname of server

`--gradio-queue` Uses gradio queue; experimental option; breaks restart UI button

`--skip-version-check` Do not check versions of torch and xformers
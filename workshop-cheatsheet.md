# Workshop cheetsheat

0. Intro
   * Show ilab GH page, show latest release
   * Commands
     * `nvidia-smi`
     * `ilab system info`
     * Explain why `ilab` command is so slow.
     * `ilab model list`

1. Config
   * `ilab config init`
   * We would have done this but we already have config.
   * `vi ~/.config/instructlab/config.yaml`  

2. Taxonomy
   * `ilab data diff`
   * `cd ~/.local/share/instructlab/taxonomy/`
   * `git status`
   * `vi **/qna.yaml`

3. Generate
   * `ilab data generate --pipeline full --enable-serving-output`
   * Explain the arguments.
   * `cd ~/.local/share/instructlab/datasets/`
   * It took ~50 minutes with the one above.

4. Train
   * `ilab model train ...`

5. Serve
   * `ilab model serve`
   * `ilab model chat`


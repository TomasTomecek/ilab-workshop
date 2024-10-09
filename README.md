# InstructLab workshop supporting materials

Materials for Czech InstructLab workshop for [Dny AI](https://dny.ai/).

[Grant Shipley](https://www.youtube.com/@gshipley21) did an amazing demo of what we'll do here: https://www.youtube.com/watch?v=H_dUADNfQxg
He's using [this config](https://github.com/rhai-code/backToTheFuture/blob/main/L4_x4.yaml) for training with quantized mistral 8x7B.

## Official workshop

TBD

## Workshop steps (internal)

These are meant for organizers.

### Prerequisites

`cd /var/home/instruct/.local/share/instructlab/taxonomy`  
Overwrite `knowledge/science/animals/birds/black_capped_chickadee/qna.yaml` with `black_capped_chickadee-knowledge.qna.yaml`  
`rm compositional_skills/grounded/linguistics/inclusion/qna.yaml compositional_skills/grounded/linguistics/writing/rewriting/qna.yaml compositional_skills/linguistics/synonyms/qna.yaml`  
Overwrite `/var/home/instruct/.config/instructlab/config.yaml` with `instructlab-config.yaml`  
Download models.  

#### Users

Create users, sudoers (podman only), ilab config.

### TL;DR workshop

0. `nvidia-smi`  
   `ilab system info`  
   Explain why `ilab` command is so slow.  
   Maybe show Image Mode if someone is interested?  

1. `ilab config init`  
   We would have done this but we already have config.  
   `vi ~/.config/instructlab/config.yaml`  

2. `ilab data diff`  
   `cd ~/.local/share/instructlab/taxonomy/`  
   `git status`  

3. `ilab data generate --pipeline full --enable-serving-output`  
   Explain the arguments.  
   `cd ~/.local/share/instructlab/datasets/`  
   It took ~50 minutes with the one above.  

4. Train

5. Serve  
   Let people SSH only at this point.  

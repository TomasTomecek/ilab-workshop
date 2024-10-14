# InstructLab workshop supporting materials

Materials for Czech InstructLab workshop for [Dny AI](https://dny.ai/).

[Grant Shipley](https://www.youtube.com/@gshipley21) did an amazing demo of what we'll do here: https://www.youtube.com/watch?v=H_dUADNfQxg
He's using [this config](https://github.com/rhai-code/backToTheFuture/blob/main/L4_x4.yaml) for training with quantized mixtral 8x7B.
We have the complete InstructLab config here as `instructlab-config.yaml`.

There are 2 great official resources that you can follow:
1. The official [README of InstructLab](https://github.com/instructlab/instructlab?tab=readme-ov-file#-getting-started).
2. [Knowledge to the open source Granite model using
   InstructLab](https://developer.ibm.com/tutorials/awb-contributing-knowledge-instructlab-granite/)
   article at IBM Developer portal.
3. [Official RHEL AI documentation](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux_ai/1.1).

## Workshop steps

We will be using the official InstructLab README.

### Prerequisites

Training a model requires a lot GPU memory, requirements can be found [here](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux_ai/1.1/html/getting_started/hardware_requirements_rhelai).

Please clone this repo:
```
$ git clone https://github.com/TomasTomecek/ilab-workshop
```

If you don't have a ilab config, create it:
```
$ ilab config init
```

Locate your local taxonomy, it can be here:
```
$ cd ~/.local/share/instructlab/taxonomy
```

We have a knowledge here we'll use for sake of the workshop:
```
$ cp $THIS_REPO/black_capped_chickadee-knowledge.qna.yaml knowledge/science/animals/birds/black_capped_chickadee/qna.yaml
```

We have an ilab config in this repo that's optimized for 4x T4 GPU instance.

Make sure that all models that ilab uses are present, [more info here](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux_ai/1.1/html/building_your_rhel_ai_environment/downloading_ad_models#downloading_ad_models).

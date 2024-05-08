# optml_proj
way to use ##model.py##:
replace loss_landscape_anim/model.py with the provided version, then call:
```sh
loss_landscape_anim(
    n_epochs,
    datamodule=MNISTDataModule(),
    model = ResNet(input_channels=1, num_classes=10, learning_rate=0.001, \
                   num_blocks=5, optimizer="adam", gpus=1 if torch.cuda.is_available() else 0),
    optimizer="adam",
    reduction_method="pca", # "pca", "random", "custom" are supported
    custom_directions=None,
    model_dirpath="checkpoints/",
    model_filename="model.pt",
    gpus=1,
    load_model=False,
    output_to_file=True,
    output_filename="sample.gif",
    giffps=15,
    sampling=False,
    n_frames=300,
    seed=None,
    return_data=False,
)
```

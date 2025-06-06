Device Info: 
- M4 Pro Mac Chip
- Memory 24GB
- Version 15.5 (24F74)
- Serial number CWQVL2M9C0


- Had to downgrade: torchvision==0.17.2 torch==2.2.2

- Added numpy==1.26.4 to dependencies

- When running the pipeline i need to add PYTORCH_ENABLE_MPS_FALLBACK=1 before the terminal command

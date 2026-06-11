Every time you reboot, do this before running the app:
Step 1 — Mount the data drive:


sudo mkdir -p /media/riccardo/DATA

sudo mount -t ntfs3 -o force /dev/nvme0n1p2 /media/riccardo/DATA

(The mkdir is only needed once; -o force handles the dirty-flag issue)

Step 2 — Launch the app:


cd ~/Desktop/"V-JEPA 2-AC ~ Cosmos 2.5-2B Robot"

./app/launch.sh

Wait ~30 seconds for the model to load, then open http://localhost:7860.

To stop the app:
Press Ctrl+C in the terminal running it, or:

pkill -f experiment_runner.py

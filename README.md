# OccupantDetectionDL


list of tasks:

Dataset creation: Cvat will be used to perform data annotation. Steps are described in Dataset_Annotation.md
Since Cvat only dumps annotations frames will be extracted using ffmpeg,the same tool used by cvat to extract frames.
The following command is used to extract frames. 

Here iq, is the frame resolution quality which is a field in the cvat tool for image quality.

tq = 96 - iq

tq = round((((tq - 1) * (31 - 2)) / (95 - 1)) + 2)

ffmpeg -i '/pathtovideo' -start_number 0 -b:v 10000k -vsync 0 -an -y -q:v tq -vf "select=not(mod(n\,10))" %d.jpg



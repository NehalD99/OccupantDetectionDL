## Annotation rules in CVAT

[Labels field]

Categories: 

1)Head
2)Arm
3)Torso
4)Feet

[Frame filter:step=25] to skip every 25 frames

[Image quality:50] to compress upto 50 percent

Select [Mode:Interpolation]

There is no need to create bounding box for every frame.
Create bounding box for the object every few frames.
That frame is starred automatically.Frames are interpolated between key frames by default.

### Cases: Object out of frame

Select eye so that its tracking is stopped.
When object comes back in frame, annotate it with a bbox again.
To merge the bboxes before and after(merging tracks that is), select merge shape. Then select one bbox before dissappearance and select bbox after reappearance. Select apply merge.










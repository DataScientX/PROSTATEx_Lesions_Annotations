# PROSTATEx Lesions Annotations

We propose two folders containing radiological annotations on the 328 PROSTATEx cases included in the PICAI challenge cohort (see https://github.com/DIAGNijmegen/picai_labels/blob/main/additional_resources/ProstateX-mapping.json for PROSTATEx/PICAI mapping). The proposed masks are in the T2w sequence space provided by the PICAI challenge.

- The directory 'labels_PX_PIRADS_P345' contains binary masks representing lesions identified with PI-RADS scores 3, 4, and 5.

- In the directory 'labels_PX_PIRADS_P45', only PI-RADS 4 and 5 lesions are included in the binary masks, excluding those with a PI-RADS score of 3.

Some T2-w sequences from the PI-CAI challenge underwent slight affine transformations compared to the original T2-w sequences from PROSTATEx. To ensure compatibility between T2-w PI-CAI lesion masks and T2-w PROSTATEx sequence space, we identified 65 cases where the normalized mutual information between T2-w images from PROSTATEx and PI-CAI was not 1. Subsequently, an affine registration was performed from the PI-CAI T2-w sequence space to PROSTATEx T2-w sequence space for these cases. The resulting transformation was then applied to the PI-CAI lesion annotation masks, ensuring a robust alignment between sequences from the PROSTATEx challenge and PI-CAI lesion masks.

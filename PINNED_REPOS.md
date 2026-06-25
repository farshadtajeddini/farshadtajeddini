# Suggested GitHub Structure

This profile will look strongest if the pinned repositories show both research depth and engineering execution. The goal is to make your GitHub read like: "I can build real AI and scientific-computing systems, not only write papers."

## Recommended Pinned Repositories

1. `nii-to-stl-aorta-pipeline`
   - Based on the current `nii_label_to_stl.py` workflow.
   - Show conversion from NIfTI label maps to STL meshes.
   - Include a small synthetic example, CLI usage, dependencies, and screenshots of generated meshes.
   - Do not include real patient NIfTI, STL, dates, identifiers, or clinical folders.

2. `aortic-geometry-processing-toolkit`
   - Present your geometry preparation pipeline: cut planes, centerlines, diameter/area profiles, and CFD-ready surfaces.
   - Include synthetic or anonymized demo outputs only.
   - Add diagrams or screenshots from safe generated examples.

3. `cardiovascular-risk-stratification-ml`
   - Show the ML workflow behind PLS-DA, SVM, cross-validation, and AUC/sensitivity reporting.
   - Use synthetic data or a public dataset with the same structure.
   - Highlight leakage prevention and small-sample validation.

4. `4d-mri-pinn-super-resolution`
   - Position this as scientific ML: physics-informed constraints plus neural networks.
   - A toy flow example is enough if research data cannot be shared.
   - Include model architecture, loss terms, and validation plots.

5. `medical-image-segmentation-experiments`
   - Show PyTorch segmentation workflows with U-Net/CNN/MedSAM-style experiments.
   - Use open datasets or synthetic image examples.
   - Include training, inference, metrics, and visualization scripts.

6. `clinical-ml-validation-toolkit`
   - Package reusable utilities for LOOCV, stratified CV, nested validation, sensitivity/specificity, AUC, calibration, and confusion matrices.
   - This is recruiter-friendly because it shows engineering around reliable ML, not only modeling.

## Repositories to Avoid Making Public Directly

- Any folder containing real patient `.nii`, `.nii.gz`, DICOM, STL, VTP, JSON landmarks, dates, medical record-like labels, or scan names.
- Raw `Archive`, `Archive_STL`, `Archive_STL_cut`, or `Archive_STL_dicom_station_cut` folders.
- Manuscript-private data, unpublished clinical data, or anything tied to institutional agreements.

## Suggested `.gitignore` for Medical Imaging Repos

```gitignore
# Patient or clinical data
*.nii
*.nii.gz
*.dcm
*.stl
*.vtp
*.vtk
*.obj
Archive/
Archive_STL/
Archive_STL_cut/
Archive_STL_dicom_station_cut/

# Derived clinical metadata
*points.json
*cut_planes.json
*dicom_station_cut.json
*patient*
*MR*
*PETMR*
*MRAorta*

# Python
__pycache__/
*.pyc
.venv/
venv/

# Notebooks
.ipynb_checkpoints/
```

## Profile Setup Steps

1. Create a GitHub repository with the exact same name as your GitHub username.
2. Add the `README.md` from this folder to that repository.
3. Replace `YOUR_GITHUB_USERNAME` in all project links.
4. Create the six public-facing repositories above, starting with `nii-to-stl-aorta-pipeline`.
5. Pin the six repositories from your GitHub profile settings.

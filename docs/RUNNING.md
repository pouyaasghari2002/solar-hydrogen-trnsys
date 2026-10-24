# Reproducing the simulation

1. Preserve the supplied `trnsys/` folder as an archive and make a working copy elsewhere. A new run can overwrite logs and output files.
2. Open `HW2.tpf` in a compatible TRNSYS Simulation Studio installation. The supplied deck references TRNSYS18 paths.
3. Confirm that all required component implementations and proformas are installed. The deck uses hydrogen-system components as well as PV, weather, control, plotting, printing, and integration components.
4. Locate compatible copies of `US-AZ-Phoenix-23183.tm2` and `Type160-Electrolyzer.dat`. These data files were not in the supplied archive.
5. Update the external data-file assignments to your local paths. If Simulation Studio regenerates the deck, make the corresponding changes in the project interface as well.
6. Check component output units and volume-reference conditions before accepting either hydrogen mass conversion. The saved post-compression indicator does not demonstrate increased mass production.
7. Review the PV cell count, area, temperature coefficients, storage pressure band, tank volume, and polarization current sweep against the intended design and component documentation.
8. Run the working copy and review warnings, convergence, component validity ranges, and mass balance.
9. Save new outputs separately with the application/component versions and settings. Compare them with the archive only after establishing the same units and model configuration.

The original `.dck`, `.tpf`, `.PTI`, `.log`, `.lst`, and `.out` files are unchanged. They have not been executed during this preparation. The log includes low-voltage warnings in the polarization branch.

The two output files have the same printed column label, `Daily_gen`, despite representing different source equations. Use their filenames and deck connections to distinguish them. Their final values at 8760 hours are approximately 4.9163755574 and 126.8602392138, respectively.

Do not treat the source's PV sizing as a certified optimum or its approximate 5 kg/day result as independently verified performance. The report's editorial appendix explains the limitations without modifying the historical model.

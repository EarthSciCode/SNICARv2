# SNICARv2
Cenlin He (cenlinhe@ucar.edu), Mark G. Flanner (flanner@umich.edu)

Updated SNICAR snow model codes (for educational and research purposes only)

This is an updated stand-alone version of SNICAR. This version does not include dynamic snow aging processes (coupled with CLM). 


The references for the model:

(1) Flanner et al. 2007: Flanner, M. G., C. S. Zender, J. T. Randerson, and P. J. Rasch (2007), Present-day climate forcing and response from black carbon in snow, J. Geophys. Res., 112, D11202, doi:10.1029/2006JD008003.

(2) He et al. 2018: He, C., Flanner, M. G., Chen, F., Barlage, M., Liou, K.-N., Kang, S., Ming, J., and Qian, Y.: Black carbon-induced snow albedo reduction over the Tibetan Plateau: Uncertainties from snow grain shape and aerosol-snow mixing state based on an updated SNICAR model, Atmos. Chem. Phys. Discuss., doi:10.5194/acp-2018-476, in review, 2018.

(3) He et al. 2017: He, C., Takano, Y., Liou, K.-N., Yang, P., Li, Q., and Chen, F. (2017). Impact of snow grain shape and black carbon-snow internal mixing on snow optical properties: Parameterizations for climate models. Journal of Climate, 30, 10019–10036, https://doi.org/10.1175/JCLI-D-17-0300.1.


Original version: written by Mark Flanner (flanner@umich.edu), see Flanner et al. 2007 JGR. The original model codes are available at: http://snow.engin.umich.edu/snicarcode/ . It assumes aerosol externally mixed with spherical snow grains.

Current version: updated by Cenlin He (cenlinhe@ucar.edu), see He et al. 2018 ACP. It includes nonspherical snow grain & Black carbon (BC)-snow internal mixing based on parameterizations from He et al. 2017 (J. Climate).

Currently, this model version can only deal with BC-snow internal mixing; Internal mixing between snow and other aerosols will be added later.

Please download the "SNICARv2.zip" for model codes and "ice_optical_properties" folder for snow/ice input data.

The SNICARv2.zip includes a "main code" folder and a "readme.txt" file.

The “main code” folder includes:

(1) Driver routine for SNICAR: snicar_driver8d.m (more model descriptions in this file)

(2) Main SNICAR model routine: snicar8d_v2.m (more model descriptions in this file)

(3) Look-up table for ice optical properties: “ice_optical_properties” folder

(4) Look-up table for aerosol optical properties: 
    Dust: “aer_dst_bln_xx.nc”;
    Black carbon: “mie_sot_ChC90_dns_1317.nc” (uncoated),”miecot_slfsot_ChC90_dns_1317.nc” (coated)
    Volcano ash: “volc_ash_mtsthelens_20081011.nc”

(5) Downward surface solar radiative spectra: “mlw_sfc_flx_frc_cld.txt” (cloudy-sky), “mlw_sfc_flx_frc_clr.txt” (clear-sky)


This MATLAB code should work "out of the box" with all releases of Matlab including and following R2012.

To run the code:

1) Unpack/unzip the files

2) Launch Matlab

3) Run the driver routine snicar_driver8d.m


To enable a larger number of ice effective radii to be used with the model, also download the “ice_optical_properties” folder, and put those files either in your “ice_optical_properties” folder within the run directory or in a data directory specified by variable “wrkdir” in "snicar8d.m" file. The ice optical properties data is also available at: http://snow.engin.umich.edu/snicarcode/.


=====

Updated on May 22, 2018.

# SNICARv2.1
Contact: Julian Gelman Constantin (juliangelman@cnea.gov.ar), Cenlin He (cenlinhe@ucar.edu), Mark G. Flanner (flanner@umich.edu)

For educational and research purposes only

We further updated the standalone version of the SNICAR snow model codes to be version 2.1 based on our version 2.

This version 2.1 (SNICAR_v2.1.zip) includes the following major updates compared with version 2:

1) The possibility to input clear sky direct and diffuse solar spectrum, and by the simple modification of a parameter (Npt, cloud opacity factor),calculation of direct and diffuse spectra for partly cloudy sky conditions. This allows to calculate pure direct and pure diffuse spectral and broadband albedo, and a weighted averaged albedo (considering the fraction of direct and diffuse incoming solar radiation).

2) The possibility of easily varying (through a simple loop) some of the parameters of the model, in order to assess the effect of the uncertainties of different field measurements of snow properties.

3) The ice optical properties are the same as used in the previous version.

See version 2 below for other details and features.

Reference for this version 2.1 model:

Julián Gelman Constantin, Lucas Ruiz, Gustavo Villarosa, Valeria Outes, Facundo Bajano, Cenlin He, Hector Bajano, and Laura Dawidowski (2020), Measurements and modeling of snow albedo at Alerce Glacier, Argentina: effects of volcanic ash, snow grain size and cloudiness, The Cryosphere, in review.



=====

Updated on Apr 2, 2020.



# SNICARv2
Contact: Cenlin He (cenlinhe@ucar.edu), Mark G. Flanner (flanner@umich.edu)

Updated SNICAR snow model codes (for educational and research purposes only)

This is an updated stand-alone version of SNICAR. This version does not include dynamic snow aging processes (i.e. coupled with CLM). 


The references for the model:

(1) Flanner et al. 2007: Flanner, M. G., C. S. Zender, J. T. Randerson, and P. J. Rasch (2007), Present-day climate forcing and response from black carbon in snow, J. Geophys. Res., 112, D11202, doi:10.1029/2006JD008003.

(2) He et al. 2018: He, C., Flanner, M. G., Chen, F., Barlage, M., Liou, K.-N., Kang, S., Ming, J., and Qian, Y.: Black carbon-induced snow albedo reduction over the Tibetan Plateau: uncertainties from snow grain shape and aerosol–snow mixing state based on an updated SNICAR model, Atmos. Chem. Phys., 18, 11507-11527, https://doi.org/10.5194/acp-18-11507-2018, 2018.

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

Updated on Aug 3, 2018.

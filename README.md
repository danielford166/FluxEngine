FluxEngine
==========

The FluxEngine is an open source atmosphere-ocean gas flux data processing toolbox. The toolbox has so far contributed to 13 different journal publications, resulting in 5 press releases, contributed to 2 completed PhDs and 1 ongoing PhD, has been used within 5 UK and EU research projects and has been used in undergraduate and masters level teaching. It is now being used within the European Integrated Carbon Observing System (ICOS).  This work collectively identifies and quantifies the importance of the oceans in regulating and storing carbon. 

Known issues with v4.0.7
----
01 Sep 2022 - There is a known error with calculating fluxes using concentration data (thanks Silvie Lainela for finding this error and Tom Holding for identify the work around). With this option you have to set and use conca and concw as the main inputs. But the tools incorrectly request pgas_air and pgas_sw inputs (which are not used in the flux calculation when you use concentration data). To overcome this simply define and pass pgas_air and pgas_sw data as an additional input i.e. create a file containing NaN or 0s and add the information into the configuration file. This will allow the calculations to complete and the pgas data will not be used in the calculation. This error will be fixed in the next release of the fluxengine.


Version 4.0.
----
v4.0.7 released May 2022 - Small update adding flexibility to custom gas transfer velocity parameterisations.

v4.0.2 released July 2020 - released as major FluxEngine v4 release - Small updates for re-analysis tool compatbility with SOCATv2020 release.

v4.0.1 released May 2020.

Version 4.0.7 uses Python 3 (but still contains all of the functionality of FluxEngine v3.0). Version 4.0 is available to install from PyPi (https://pypi.org/project/fluxengine/) or GitHub (https://github.com/oceanflux-ghg/FluxEngine). This update means that the FluxEngine is now a standard Python package and this has simplified the installation process. For example, you can now install the FluxEngine by using the Python Package Installer, pip, using the command 'pip install fluxengine'.  Whilst providing this update we also removed some functionality that was no longer needed which resulted in the FluxEngine configuration file format changing slightly and a new commandline tool is provided to update old configuration files (fe_update_config.py). Version 4.0 has been verified against reference runs using SOCATv4 pCO2 and Takahashi et al (2009) data sets, as described in Shutler et al. (2016) http://journals.ametsoc.org/doi/abs/10.1175/JTECH-D-14-00204.1. All results were consistent with those produced using v3.0. The description of all FluxEngine functionality can be found in Shutler et al., (2016) and Holding et al., (2019) https://doi.org/10.5194/os-15-1707-2019 and full documentation/usage instructions are included as a PDF documentation on the GitHub page.

Please reference these journal publications when using this toolbox and presenting its output in any publications.

Re-analysed SOCAT datasets
----
Each year we used the FluxEngine to reanalyse the latest version of the Surface Ocean CO2 Atlas (SOCAT) database (https://www.socat.info).  We provide this service for free and typically provide links to the reanalysed data a few weeks after the new release of the SOCAT database. The original SOCAT data are all sampled from different depths and each measurement is tied to a temperature values, but the sources of the temperature data varies. This makes these data less ideal for global air-sea flux analyses. To enable an accurate air-sea flux calculation they need to be reanalysed to a common depth and temperature dataset. The reanalysed SOCAT data that we provide are all referenced to a common sampling depth and temperature dataset and the pairing between CO2 data and temperature is retained.  The tools and methods that perform the reanalysis are detailed within the FluxEngine publications. The reanalysed datasets contain the individual cruise version of the SOCAT database and the gridded SOCAT data. 

Please read the dataset metadata when using these data and please follow the guidelines in the metadata when referencing and acknowleging their use. 

Sims, R., Holding T, Ashton I, Shutler, J (2021) Reanalysed (depth and temperature consistent) surface ocean CO₂ atlas (SOCAT) version 2021

Holding T, Ashton I, Shutler, J (2020) Reanalysed (depth and temperature consistent) surface ocean CO₂ atlas (SOCAT) version 2020, ICOS carbon portal, https://doi.org/10.18160/vmt4-4563

Holding T, Ashton I, Shutler, J (2019). Reanalysed (depth and temperature consistent) surface ocean CO₂ atlas (SOCAT) version 2019, Pangaea, https://doi.pangaea.de/10.1594/PANGAEA.905316



Example news articles (resulting from research performed using the FluxEngine)
----
1. The Daily Mail 'World's oceans soak up 900 million tonnes of CO2 a year MORE than previously thought — the amount emitted by 2.2 billion petrol cars' https://www.dailymail.co.uk/sciencetech/article-8698067/Worlds-oceans-soak-carbon-previously-thought.html

2. Phys.org (2019) 'Satellites are key to monitoring ocean carbon' https://phys.org/news/2019-11-satellites-key-ocean-carbon.html

3. ESA news (2019), 'Can oceans turn the tide on the climate crisis' https://www.esa.int/Our_Activities/Observing_the_Earth/Can_oceans_turn_the_tide_on_the_climate_crisis

4. The Guardian (2018), 'Invisible scum on sea cuts CO2 exchange with air by up to 50%' https://www.theguardian.com/environment/2018/may/28/invisible-scum-on-sea-cuts-co2-exchange-with-air-by-up-to-50

5. BBC News (2016), 'How Northern European waters soak up carbon dioxide' https://www.bbc.co.uk/news/science-environment-35654938


Animation 
----
A short animation explaining the concepts of atmosphere-ocean gas exchange, why this is important, and what the FluxEngine enables 
http://due.esrin.esa.int/stse/videos/page_video013.php


Journal publications (which use FluxEngine and/or FluxEngine outputs)
----
Gutiérrez Loza, L., Wallin, M. B., Sahlée, E., Holding, T., Shutler, J. D., Rehder, G. & Rutgersson, A. (2021). Air–sea CO2 exchange in the Baltic Sea—A sensitivity analysis of the gas transfer velocity. Journal of Marine Systems, 222, https://www.sciencedirect.com/science/article/pii/S0924796321001007

Friedlingstein et al, (2021), Global Carbon Budget 2020, Earth Syst. Sci. Data, 12, 3269–3340, https://doi.org/10.5194/essd-12-3269-2020.  

Watson, A.J., Schuster, U., Shutler, J.D. et al. Revised estimates of ocean-atmosphere CO2 flux are consistent with ocean carbon inventory. Nature Communications 11, 4422 (2020). https://doi.org/10.1038/s41467-020-18203-3 

Kitidis, V., Shutler, JD., Ashton, I. et al (2020) Winter weather controls net influx of atmospheric CO2 on the north-west European shelf, Scientific Reports, 9(20153), https://www.nature.com/articles/s41598-019-56363-5

Shutler, JD, Wanninkhof, R, Nightingale, PD, Woolf, DK, Bakker, DCE, Watson, A, Ashton, I, Holding, T, Chapron, B, Quilfen, Y, Fairall, C, Schuster, U, Nakajima, M, Donlon, D (2019) Satellites are critical for addressing critical science priorities for quantifying ocean carbon, Frontiers in Ecology and the Environment,  https://doi.org/10.1002/fee.2129

Woolf DK, Shutler JD, Goddijn‐Murphy L, Watson AJ, Chapron B, Nightingale PD, Donlon CJ, Piskozub J, Yelland MJ, Ashton I, et al (2019). Key Uncertainties in the Recent Air‐Sea Flux of CO2. Global Biogeochemical Cycles, https://doi.org/10.1029/2018GB006041

Holding, T., Ashton, I. G., Shutler, J. D., Land, P. E., Nightingale, P. D., Rees, A. P., Brown, I., Piolle, J.-F., Kock, A., Bange, H. W., Woolf, D. K., Goddijn-Murphy, L., Pereira, R., Paul, F., Girand-Ardhuin, F., Chapron, B., Rehder, G., Ardhuin, F., Donlon, C. J. (2019) The FluxEngine air–sea gas flux toolbox: simplified interface and extensions for in situ analyses and multiple sparingly soluble gases, Ocean Sci., https://doi.org/10.5194/os-15-1707-2019

Henson SA, Humphreys MP, Land PE, Shutler JD, Goddijn-Murphy L, Warren M (2018). Controls on open-ocean North Atlantic ΔpCO2 at seasonal and interannual timescales are different. Geophysical Research Letters, doi:10.1029/2018GL078797

Pereira R, Ashton, I, Sabbaghzadeh, B, Shutler, JD and Upstill-Goddard RC (2018). Reduced air–sea CO2 exchange in the Atlantic Ocean due to biological surfactants. Nature Geoscience, 1. doi: 10.1038/s41561-018-0136-2

Holding T, Ashton I, Woolf DK, Shutler JD (2018): FluxEngine v2.0 and v3.0 reference and verification data, PANGAEA, doi: 10.1594/PANGAEA.890118

Wrobel, I. (2017) Monthly dynamics of carbon dioxide exchange across the sea surface of the Arctic Ocean in response to changes in gas transfer velocity and partial pressure of CO2 in 2010. Oceanologia, 59(4), 445-459, doi: 10.1016/j.oceano.2017.05.001.

Ashton IG, Shutler JD, Land PE, Woolf DK, Quartly GD (2016), A Sensitivity Analysis of the Impact of Rain on Regional and Global Sea-Air Fluxes of CO2. PLoS ONE 11(9): e0161105. doi: 10.1371/journal.pone.0161105.

Wrobel I, Piskozub J (2016) Effect of gas-transfer velocity parameterization choice on air–sea CO2 fluxes in the North Atlantic Ocean and the European Arctic, Ocean Science, 12, 1091-1103, doi: 10.5194/os-12-1091-2016.

Shutler JD, Land PE, Piolle J-F, Woolf DK, Goddijn-Murphy L, Paul F, Girard-Ardhuin F, Chapron B, Donlon CJ (2016), FluxEngine: a flexible processing system for calculating atmosphere-ocean carbon dioxide gas fluxes and climatologies, Journal of Atmospheric and Oceanic Technology, doi: 10.1175/JTECH-D-14-00204.1

Rödenbeck C, Bakker DCE, Gruber N, Iida Y, Jacobson AR, Jones S, Landschützer P, Metzl N, Nakaoka S, Olsen A, Park G-H, Peylin P, Rodgers KB, Sasse TP, Schuster U, Shutler JD, Valsala V, Wanninkhof R, and Zeng J (2015) Data-based estimates of the ocean carbon sink variability – first results of the Surface Ocean pCO2 Mapping intercomparison (SOCOM), Biogeosciences, 12, 7251-7278, doi: 10.5194/bg-12-7251-2015.



Information about older versions of the FluxEngine toolbox
----

Version 3.0 (static as of 02 August 2019).
----
v3.0 (first release April 2018, updated September 2018, February 2019, April 2019, June 2019, July 2019, static 02 August 2019)

Version 3 (v3.0) uses Python 2.7 and has been verified against reference runs using SOCATv4 pCO2 and all results were identical to those produced using FluxEngine v2.0. A more comprehensive verification has been performed using references runs of the Takahashi et al. (2009) dataset as described in Shutler et al. (2016) http://journals.ametsoc.org/doi/abs/10.1175/JTECH-D-14-00204.1. All results were identical to those produced using v1.0 and v2.0. A journal paper describing the v3.0 updates is now available, Holding et al., (2019) and can be found here https://doi.org/10.5194/os-15-1707-2019. 

Please reference these journal publications when using this toolbox and presenting its output in any publications.

The FluxEngine v3.0 updates and extensions were funded by the European Space Agency (ESA) research projects (OceanFlux Evolution, SKIM SciSoc) and two European Union (EU) research projects (Ringo and Integral). The two EU studies are preparatory projects for the European Integrated Carbon Observing System (ICOS). v3.0 additions to the toolbox include:

    •   A more flexible way of specifying input data in the configuration files.
    •   Data pre-processing options (e.g. unit conversion).
    •   Python is used for all tools, allowing a more streamlined workflow.
    •   A move toward an API-like toolkit, beyond a simple set of commandline tools.
    •   A more modularised structure to the code including modular k parameterisation and data pre-processing options.
    •   Metadata and default options specified in an xml file (settings.xml).
    •   Automatic verification scripts that use SOCATv4 and Takahashi09 reference datasets.
    •   Tools for simplifying analysis of in situ data (e.g. SOCAT format data from research cruises and fixed stations).
    •   Improvements for calculating N2O and CH4 gas fluxes (now using MOMENTO data format).

v2.0 (July 2016)
----
These updates have been verified against Takahashi (2009) using the verification options within the code. All results were identical to those derived from v1.0.
The updates included contribute to further publications in preparation and further details will be posted here following publication.
The updates include improved:

    •   handling for irregular grids,
    •   handling for different gases including O2, N2O and CH4, 
    •   handling for in-situ data.

Specifically, data on irregular grids can now be handled through the main flux calculations. Note: the ofluxghg-flux-budgets.py tool is only valid for regular (1deg x 1deg) grids. 
In-situ data should be put in separate netCDF files and the last two digits of the filename needs to represent the month of interest as a two digit number. e.g. January -> ’01’. 
To operate the system with different gases, the appropriate switch should be changed in ofluxghg-flux-calc.py. Please use ofluxghg-flux-calc.py --help for further information.


v1.0 (09 March 2016)
----
The FluxEngine open source atmosphere-ocean gas flux data processing tools. The license for this software toolbox can be found within this github repository.
Please reference the publication linked below when using this toolbox and presenting its output in any publications.
A journal paper describing the toolbox has been published here: Shutler et al., (2016) http://journals.ametsoc.org/doi/abs/10.1175/JTECH-D-14-00204.1
Please send any feedback and comments to Jamie Shutler, email: j.d.shutler@exeter.ac.uk
The FluxEngine software was originally developed by The European Space Agency OceanFlux Greenhouse Gases and Evolution project teams.


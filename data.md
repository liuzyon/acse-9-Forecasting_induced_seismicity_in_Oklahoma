项目介绍：

Do human activities cause earthquakes in tectonically active areas? A big data approach to understanding induced seismicity in California.



It is well established that humans can cause earthquakes through fluid extraction (e.g. oil, gas, groundwater) and injection (e.g. wastewater disposal and hydraulic fracturing). Such cases of induced seismicity have been well-documented and established in Oklahoma, where there has been a dramatic increase in seismicity since 2010 (Ellsworth, 2013). In cases like Oklahoma, it is easier to establish the fundamental causes of induced seismicity because the rate of earthquakes prior to high-rate wastewater injection was very low. So due to the low background stress in intraplate regions, the human triggering signatures are clearly identifiable. However, distinguishing between natural and triggered seismicity in tectonically-active areas is more challenging. Large-scale big-data and statistical approaches are one approach to predict the locations where human triggered seismicity may be expected (e.g. Hincks et al., 2018; Ries et al., 2020; Wozniakowska & Eaton, 2020). In tectonically active regions in the US, such as California, although oil and gas extraction has taken place for many decades, only a handful of studies have been published with a focus on these areas (e.g. Hough et al., 2017). Big-data and statistical approaches will be  crucial in separating natural causes from potential human triggering factors in these areas.

In this project, you will use a unique and rich dataset of industrial activities from regions in California  to statistically evaluate and retrospectively forecast possible signatures of human-induced seismicity from existing high-quality earthquake catalogues in these regions. The database you will use includes borehole locations & geological metadata; monthly injection and extraction volumes.  To test the existence of correlations between oil and gas activity and seismicity, you will use and develop Machine Learning techniques to generate a model with predictive capabilities. To produce a simple model of earthquake occurrence, one starting point could be Linear Regression and Logistic Regression. You will have regular meetings with the main supervisor (Hicks), as well as joining in with discussions with the larger research team, who are currently carrying out similar analyses for earthquakes in Texas. You will be expected to do your own Python coding , including using specific Python libraries such as Pandas, Scikit-Learn, statsmodels, matplotlib, and some GIS modules.

Further reading

Ellsworth, W. L. (2013). Injection-Induced Earthquakes. Science, 341(6142). https://doi.org/10.1126/science.1225942
Hincks, T., Aspinall, W., Cooke, R., & Gernon, T. (2018). Oklahoma’s induced seismicity strongly linked to wastewater injection depth. Science, 359(6381), 1251–1255. https://doi.org/10.1126/science.aap7911
Hough, S. E., Tsai, V. C., Walker, R., & Aminzadeh, F. (2017). Was the Mw 7.5 1952 Kern County, California, earthquake induced (or triggered)? Journal of Seismology, 21(6), 1613–1621. https://doi.org/10.1007/s10950-017-9685-x
Ries, R., Brudzinski, M. R., Skoumal, R. J., & Currie, B. S. (2020). Factors Influencing the Probability of Hydraulic Fracturing‐Induced Seismicity in Oklahoma. Bulletin of the Seismological Society of America, 110(5), 2272–2282. https://doi.org/10.1785/0120200105
Wozniakowska, P., & Eaton, D. W. (2020). Machine Learning-Based Analysis of Geological Susceptibility to Induced Seismicity in the Montney Formation, Canada. Geophysical Research Letters, 47(22), e2020GL089651. https://doi.org/10.1029/2020GL089651



地图网址：

https://www.odot.org/hqdiv/p-r-div/maps/shp-files/



数据：

OCC_injection_data：注射数据

Volume_BPD: 流量



HydraulicFracturingData：水力压裂数据



Well Workbook_Header

Surface Latitude

Surface Longitude



I have checked the dataset. Because I don't have the background knowledge of this relevant application domain, I have a lot of questions about the dataset which are list below. I'm sorry to bother you this time.

So the OCC_injection_data is the injection data  I should focus on which you mentioned in Project Introduction, is it right? Does this mean I don't need to use the data in ProductionData instead? Of course, I would appreciate it if you could tell me in more detail what the data in this folder are because there are too mant files in ProductionData(If I need use these data).

In the Well Data, there are two files, Well Workbook_Header and Well Workbook_Location. Both miss the header information. I can infer that Well Workbook_Location is the information about wells' locations. But I am a little confused about Well Workbook_Header, due to lack in header information, I can not infer that what data this is.

You also add a director called HydraulicFracturingData, do I need to use this data? Does the hydraulic fracturing data related to injection data?

Thanks!





It is well  established that humans can cause earthquakes through fluid extraction (e.g.  oil, gas, groundwater) and injection (e.g. wastewater disposal and hydraulic  fracturing). Such cases of induced seismicity have been well-documented and  established in Oklahoma, where there has been a dramatic increase in  seismicity since 2010 (Ellsworth, 2013). In cases like Oklahoma, it is easier  to establish the fundamental causes of induced seismicity because the rate of  earthquakes prior to high-rate wastewater injection was very low. So due to  the low background stress in intraplate regions, the human triggering  signatures are clearly identifiable. However, distinguishing between natural  and triggered seismicity in tectonically-active areas is more challenging.  Large-scale big-data and statistical approaches are one approach to predict  the locations where human triggered seismicity may be expected (e.g. Hincks  et al., 2018; Ries et al., 2020; Wozniakowska & Eaton, 2020). In  tectonically active regions in the US, such as California, although oil and  gas extraction has taken place for many decades, only a handful of studies  have been published with a focus on these areas (e.g. Hough et al., 2017).  Big-data and statistical approaches will be   crucial in separating natural causes from potential human triggering  factors in these areas.          

In this project, you will use a unique and rich dataset of industrial  activities from regions in California   to statistically evaluate and retrospectively forecast possible  signatures of human-induced seismicity from existing high-quality earthquake  catalogues in these regions. The database you will use includes borehole  locations & geological metadata; monthly injection and extraction  volumes. To test the existence of  correlations between oil and gas activity and seismicity, you will use and  develop Machine Learning techniques to generate a model with predictive  capabilities. To produce a simple model of earthquake occurrence, one  starting point could be Linear Regression and Logistic Regression. You will  have regular meetings with the main supervisor (Hicks), as well as joining in  with discussions with the larger research team, who are currently carrying  out similar analyses for earthquakes in Texas. You will be expected to do  your own Python coding , including using specific Python libraries such as  Pandas, Scikit-Learn, statsmodels, matplotlib, and some GIS modules.          Further reading          Ellsworth, W. L. (2013). Injection-Induced Earthquakes. Science, 341(6142).  https://doi.org/10.1126/science.1225942     Hincks, T., Aspinall, W., Cooke, R., & Gernon, T. (2018). Oklahoma’s  induced seismicity strongly linked to wastewater injection depth. Science,  359(6381), 1251–1255. https://doi.org/10.1126/science.aap7911     Hough, S. E., Tsai, V. C., Walker, R., & Aminzadeh, F. (2017). Was the  Mw 7.5 1952 Kern County, California, earthquake induced (or triggered)?  Journal of Seismology, 21(6), 1613–1621.  https://doi.org/10.1007/s10950-017-9685-x     Ries, R., Brudzinski, M. R., Skoumal, R. J., & Currie, B. S. (2020).  Factors Influencing the Probability of Hydraulic Fracturing‐Induced  Seismicity in Oklahoma. Bulletin of the Seismological Society of America,  110(5), 2272–2282. https://doi.org/10.1785/0120200105     Wozniakowska, P., & Eaton, D. W. (2020). Machine Learning-Based  Analysis of Geological Susceptibility to Induced Seismicity in the Montney  Formation, Canada. Geophysical Research Letters, 47(22), e2020GL089651.  https://doi.org/10.1029/2020GL089651



| 53   | Stephen Hicks | s.hicks@imperial.ac.uk | Imperial College |      | Do human  activities cause earthquakes in tectonically active areas? A big data  approach to understanding induced seismicity in California. | It is well  established that humans can cause earthquakes through fluid extraction (e.g.  oil, gas, groundwater) and injection (e.g. wastewater disposal and hydraulic  fracturing). Such cases of induced seismicity have been well-documented and  established in Oklahoma, where there has been a dramatic increase in  seismicity since 2010 (Ellsworth, 2013). In cases like Oklahoma, it is easier  to establish the fundamental causes of induced seismicity because the rate of  earthquakes prior to high-rate wastewater injection was very low. So due to  the low background stress in intraplate regions, the human triggering  signatures are clearly identifiable. However, distinguishing between natural  and triggered seismicity in tectonically-active areas is more challenging.  Large-scale big-data and statistical approaches are one approach to predict  the locations where human triggered seismicity may be expected (e.g. Hincks  et al., 2018; Ries et al., 2020; Wozniakowska & Eaton, 2020). In  tectonically active regions in the US, such as California, although oil and  gas extraction has taken place for many decades, only a handful of studies  have been published with a focus on these areas (e.g. Hough et al., 2017).  Big-data and statistical approaches will be   crucial in separating natural causes from potential human triggering  factors in these areas.          In this project, you will use a unique and rich dataset of industrial  activities from regions in California   to statistically evaluate and retrospectively forecast possible  signatures of human-induced seismicity from existing high-quality earthquake  catalogues in these regions. The database you will use includes borehole  locations & geological metadata; monthly injection and extraction  volumes. To test the existence of  correlations between oil and gas activity and seismicity, you will use and  develop Machine Learning techniques to generate a model with predictive  capabilities. To produce a simple model of earthquake occurrence, one  starting point could be Linear Regression and Logistic Regression. You will  have regular meetings with the main supervisor (Hicks), as well as joining in  with discussions with the larger research team, who are currently carrying  out similar analyses for earthquakes in Texas. You will be expected to do  your own Python coding , including using specific Python libraries such as  Pandas, Scikit-Learn, statsmodels, matplotlib, and some GIS modules.          Further reading          Ellsworth, W. L. (2013). Injection-Induced Earthquakes. Science, 341(6142).  https://doi.org/10.1126/science.1225942     Hincks, T., Aspinall, W., Cooke, R., & Gernon, T. (2018). Oklahoma’s  induced seismicity strongly linked to wastewater injection depth. Science,  359(6381), 1251–1255. https://doi.org/10.1126/science.aap7911     Hough, S. E., Tsai, V. C., Walker, R., & Aminzadeh, F. (2017). Was the  Mw 7.5 1952 Kern County, California, earthquake induced (or triggered)?  Journal of Seismology, 21(6), 1613–1621.  https://doi.org/10.1007/s10950-017-9685-x     Ries, R., Brudzinski, M. R., Skoumal, R. J., & Currie, B. S. (2020).  Factors Influencing the Probability of Hydraulic Fracturing‐Induced  Seismicity in Oklahoma. Bulletin of the Seismological Society of America,  110(5), 2272–2282. https://doi.org/10.1785/0120200105     Wozniakowska, P., & Eaton, D. W. (2020). Machine Learning-Based  Analysis of Geological Susceptibility to Induced Seismicity in the Montney  Formation, Canada. Geophysical Research Letters, 47(22), e2020GL089651.  https://doi.org/10.1029/2020GL089651 | No   | Saskia Goes;  Alex Whittaker | s.goes@imperial.ac.uk |
| ---- | ------------- | ---------------------- | ---------------- | ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ---- | ---------------------------- | --------------------- |
|      |               |                        |                  |      |                                                              |                                                              |      |                              |                       |





| Date       | Attendees                     | Type  | Subject                                                      |
| ---------- | ----------------------------- | ----- | ------------------------------------------------------------ |
| 2021/06/01 | Stephen P. Hicks, Zhiyong Liu | Email | Obtain Dataset                                               |
| 2021/06/05 | Stephen P. Hicks, Zhiyong Liu | Teams | Dataset correction and interpretation                        |
| 2021/06/09 | Stephen P. Hicks, Zhiyong Liu | Teams | Project progress report (dataset import and visualization)   |
| 2021/06/21 | Stephen P. Hicks, Zhiyong Liu | Teams | Project update and results presentation, next missions to do |


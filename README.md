# Inline Biosimulation Runner
This React project allows users to manipulate the initialAmounts of Species in a COMBINE (.omex) file.
The modified COMBINE file can then be run using the runBioSimulations API.
Lastly, the results are retrieved and then plotted using Charts.js.

![image](https://user-images.githubusercontent.com/12994749/112573536-be804980-8da9-11eb-9233-22ac3caa2ffe.png)


## CORS issues
Currently, the runBioSimulationsAPI does not include an `access-control-allow-origin` header, which prevents the tool from directly calling https://run.biosimulations.org/ APIs.
To temporarily work around this issue, you will need to run a CORS proxy and have the webtraffic go through this proxy.

You can run a local proxy by running `npm run corsProxy`, and will need to modify `const API_ENDPOINT` in index.js accordingly.

# chartjs-plugin-regression
Chart.js plugin to calculate and draw statistical linear, exponential, power, 
logarithmic, and polynomial regressions using chart datasets data.

The plugin, at the current version, uses the [regression](https://www.npmjs.com/package/regression)
npm package as its calculation engine.

## Demo
For a better understanding of the capabilities of this plugin, please see this 
[Live Demo](https://pomgui.github.io/chartjs-plugin-regression/demo/).

## Download
The [compressed](https://pomgui.github.io/chartjs-plugin-regression/dist/chartjs-plugin-regression.js)
version includes the regression package.

## Installation

    npm install --save chartjs-plugin-regression

## Usage
JavaScript
```JavaScript
new Chart(ctx, {
  type: type,
  plugins: [
    // This chart will use the plugin
    ChartRegressions
  ],
  data: {
    ...
    datasets: [
      {
        ...
        // Configuration of the plugin per dataset (only will be drawn the datasets with this property) 
        regressions: {
          type: 'linear',
          line: { color: 'red', width: 3},
          ...
        }
      }
    ] 
  },
  options: {
    plugins: {
      regressions: {
        // Global configuration of the plugin, these values will be used unless each dataset defines their own
        type, line, calculation, extendPredictions, copyOverData,
        // Callback function to know when the calculation have been completed for all the datasets.
        onCompleteCalculation: (chart)=> ...
      }
    }
  }
});
```

## License
The project is released under the [ISC license](https://github.com/pomgui/chartjs-plugin-regression/blob/master/LICENSE).

## Contact
Author: Wilfredo Pomier (wpomier@pomgui.com)

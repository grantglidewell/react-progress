# React Progress

A React progress bar component

## Installation

```
yarn add react-progress
npm i react-progress
```

## Usage

```javascript
import React, { useState } from 'react';
import ProgressBar from 'react-progress';

const App = () => {
  const [percent, updatePercent] = useState(25);

  const updatePercent = () => {
    // update the progress bar percentage
    updatePercent(percent === 100 ? 25 : percent + 25);
  };
  return (
    <div onClick={updatePercent}>
      <h3>I'm all the way up! (click me)</h3>
      <ProgressBar colorShift={true} fillColor="orange" percent={percent} />
    </div>
  );
};

export default App;
```

result:

![progress bar in action](/example.gif?raw=true)

## Options

- percent: number, Required
- height: string, default: '20px',
- width: string, default: '350px',
- radius: string, default: '50px',
- borderColor: string, default: '#eee',
- fillColor: string, default: 'lime',
- colorShift: string, default: false

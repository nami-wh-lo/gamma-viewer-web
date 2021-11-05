# React Gamma Viewer Component

Use the Gamma Viewer UI as a React component.

## Installing

Using npm:

```bash
$ npm install gamma-viewer-web
```

Using yarn:

```bash
$ yarn add gamma-viewer-web
```

## Usage
```javascript
import React, { useState, useEffect } from 'react';
import axios from 'axios';
import GammaViewer from 'gamma-viewer-web';

export default function AnswerViewer({ url }) {
    const [message, setMessage] = useState();
    
    useEffect(async () => {
        const res = await axios.get(url);
        setMessage(res);
    }, []);
    
    return message ? <GammaViewer data={message}/> : <div>Loading...</div>;
}
```
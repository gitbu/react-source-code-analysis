### 一言不合就上代码

```javascript
import React, { Component, Children }  from 'react';

const {
  count,
  map
} = Children;

export default class Parent extends Component {
  render() {
    const { children } = this.props;
    return (
      <div>
        <h5>孩子数量: {count(children)}</h5>
        {map(children, function (child, index) {
          return (
            <div style={{ height: 40, border: '1px solid red'}}>
              {child}
            </div>
          );
        })} 
      </div>
    );
  }
}
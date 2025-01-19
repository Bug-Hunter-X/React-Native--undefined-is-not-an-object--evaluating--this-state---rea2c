# React Native: undefined is not an object (evaluating 'this.state')

This repository demonstrates a common error in React Native: accessing component state or props before the component has mounted.  The `BuggyComponent.js` file shows the problematic code, while `FixedComponent.js` provides the corrected version.

The error typically manifests as `undefined is not an object (evaluating 'this.state')` or a similar message indicating that `this.state` or `this.props` is undefined.  This happens because React Native components are not fully initialized until `componentDidMount` is called.

**Solution:** Always access state and props within lifecycle methods like `componentDidMount`, `componentDidUpdate`, or within methods triggered by events after the component has mounted.
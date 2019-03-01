# React
1. 使用JSX指定属性： 1）如果值是字符串的话，直接指定给属性； 2）如果值是变量，包裹在花括号里面指定给属性；
2. JSX防止注入攻击：React DOM在渲染之前会转义JSX中嵌入的所有内容，确保永远不会注入未在应用程序中明确写入的任何内容。在渲染之前，会将所有内容转换为字符串，防止XSS(跨站脚本)攻击；
3. 创建一个JSX;
  1) const element = <h1 className="greeting">Hello, world!</h1>;
  2) const element = React.createElement("h1", {className: "greeting"}, "Hello, World!");
  3) const element = { type: "h1", props: { className: "greeting", children: "Hello, World!" } };
4. React元素不可变， 元素创建后，不可更改其子元素或属性。象征着某个时间点的UI; 更新UI的唯一方法是创建一个新的元素，并将其传递给React.render()。
5. React发现组件是用户自定义的组件的时候，会将JSX中的属性作为一个单一对象传递给组件（props）;
6. this.setState ({xxx: yyy})
   this.setState((state, props) => ({counter: state.counter + props.icrement})); state: 上一状态的state  props：上一状态的props

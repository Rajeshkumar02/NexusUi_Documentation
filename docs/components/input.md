---
id: input
title: Input Component
sidebar_label: Input
sidebar_position: 1
---

# Input Component

The `Input` component is a customizable input field designed for React Native applications. It provides a flexible and user-friendly way to handle user input with various features such as icons, password visibility toggling, and error handling.

### Usage

Make sure to include this component in your project, and then you can start using it by importing it as follows:

```javascript
import { Input } from "nexus-ui/component";

export default function App() {
  return (
    <Input
      label="Email"
      placeholder="Enter Email"
      inputtype="icon"
      iconfunc={() => {
        console.log("hi");
      }}
      onChange={(e) => {
        console.log(e);
      }}
      icon={
        <Icons icon="check" family="AntDesign" size={size(5)} color="#000" />
      }
      sx={{
        errorInputbox: {
          borderColor: "red",
        },
      }}
      iconPosition="left"
      error="Error Here!"
    />
  );
}
```

## Props

| Property       | Type                              | Description                                                                         |
| -------------- | --------------------------------- | ----------------------------------------------------------------------------------- |
| `value`        | any                               | The current value of the input field.                                               |
| `onChange`     | (e: any) => void                  | A callback function to handle input changes.                                        |
| `placeholder`  | string                            | A placeholder text displayed when the input field is empty.                         |
| `error`        | string                            | An error message to display when there is an input error.                           |
| `inputtype`    | 'default' \| 'icon' \| 'password' | Specifies the type of input field.                                                  |
| `icon`         | any                               | An optional icon to display in the input field when `inputtype` is set to `'icon'`. |
| `iconPosition` | 'left' \| 'right'                 | Determines the position of the icon when `inputtype` is set to `'icon'`.            |
| `iconfunc`     | () => void                        | A function to execute when the icon is clicked.                                     |
| `type`         | 'outlined' \| 'underline'         | Specifies the style of the input field (outlined or underline).                     |
| `label`        | string                            | A label for the input field, typically used to describe the input's purpose.        |
| `inputProps`   | InputPropsI                       | Additional props for the underlying `TextInput` component.                          |
| `sx`           | object                            | An object with optional styles for customizing the component's appearance.          |

### `sx` Prop

The `sx` prop allows you to customize the appearance of the `Input` component. It accepts an object with the following optional style properties:

| Property        | Type   | Description                                             |
| --------------- | ------ | ------------------------------------------------------- |
| `input`         | object | Custom styles for the input field.                      |
| `label`         | object | Custom styles for the label.                            |
| `errorText`     | object | Custom styles for the error text.                       |
| `errorInputbox` | object | Custom styles for the input box when there is an error. |

You can use the `sx` prop to apply custom styles to various parts of the `Input` component, including the input field, label, error text, and the input box when there is an error.

### `inputProps` Prop

| Property               | Type                                                                                      | Description                                                                  |
| ---------------------- | ----------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `keyboardType`         | 'default' \| 'number-pad' \| 'decimal-pad' \| 'numeric' \| 'email-address' \| 'phone-pad' | Sets the keyboard type.                                                      |
| `autoCapitalize`       | 'none' \| 'sentences' \| 'words' \| 'characters'                                          | Controls auto-capitalization of text input.                                  |
| `autoCorrect`          | boolean                                                                                   | Enables or disables auto-correction.                                         |
| `secureTextEntry`      | boolean                                                                                   | Determines if the input should be a secure text entry (e.g., for passwords). |
| `maxLength`            | number                                                                                    | Specifies the maximum number of characters allowed in the input.             |
| `multiline`            | boolean                                                                                   | Indicates whether the input can have multiple lines.                         |
| `numberOfLines`        | number                                                                                    | Specifies the number of lines for a multiline input.                         |
| `onFocus`              | () => void                                                                                | A function to execute when the input receives focus.                         |
| `onBlur`               | () => void                                                                                | A function to execute when the input loses focus.                            |
| `onSubmitEditing`      | () => void                                                                                | A function to execute when the user submits the input.                       |
| `returnKeyType`        | 'done' \| 'go' \| 'next' \| 'search' \| 'send'                                            | Sets the return key type on the keyboard.                                    |
| `placeholderTextColor` | string                                                                                    | Sets the color of the placeholder text.                                      |
| `editable`             | boolean                                                                                   | Determines if the input is editable.                                         |

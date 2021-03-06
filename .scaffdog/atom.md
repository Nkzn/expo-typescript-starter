---
name: "atom"
description: "Atom component template"
message: "Please enter the name of component to be created"
root: "./src/atoms"
output: "**/*"
ignore: []
---

# `{{ input }}.tsx`

```jsx
import * as React from 'react'
import { View, StyleSheet } from 'react-native'

const styles = StyleSheet.create({
  container: {
    flex: 1
  }
})

interface Props {}

const {{ input }} = ({}: Props) => (
<View style={styles.container}></View>
)

class {{ input }} extends React.Component<Props> {
  render() {
    return (
      <View style={styles.container}>
      </View>
    )
  }
}

export default {{ input }}

```

# `{{ input }}.story.tsx`

```jsx
import * as React from 'react';
import {View, StyleSheet} from 'react-native';
import { storiesOf } from '@storybook/react';
import {{ input }} from './{{input}}'

const styles = StyleSheet.create({
  container: {
    flex:1
  }
})

storiesOf("atoms", module).add("{{input}}", () => (
  <View style={styles.container}>
  <{{ input }} />
  </View>
));
```

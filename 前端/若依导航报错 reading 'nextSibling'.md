### 若依vue3 报错 reading 'nextSibling'

### 修改路径 
```html
src/layout/components/AppMain.vue
```

#### 原本代码
```html
<keep-alive :include="tagsViewStore.cachedViews">
  <component v-if="!route.meta.link" :is="Component" :key="route.path"/>
</keep-alive>
```

#### 修改后的代码
```html
<transition name="fade-transform" mode="out-in">
  <div :key="route.path">
    <keep-alive :include="tagsViewStore.cachedViews">
      <component v-if="!route.meta.link" :is="Component" :key="route.path"/>
    </keep-alive>
  </div>
</transition>
```

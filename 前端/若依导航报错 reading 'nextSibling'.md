### 若依vue3 报错 reading 'nextSibling'
### RuoYi点击菜单出现空白页面，无报错

前端使用若依框架(vue3版本)，在开发过程中有时会出现切换菜单或者tab，页面空白的情况，刷新页面后又恢复正常。出现这种情况一般是在页面停留了几分钟再操作或者短时间多次跳转，偶尔也会莫名奇妙的出现，

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

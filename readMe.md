1、Vue 3.0 性能提升主要是通过哪几方面体现的？

答: 1. Proxy, 响应式代理
    2. 编译优化
    3. 打包体积优化


2、Vue 3.0 所采用的 Composition Api 与 Vue 2.x使用的Options Api 有什么区别？

答: 1. Composition API 是按需引入方法来处理数据, Options API 需要将数据的操作挂载到特定的属性上去, 例如: data、methods、mounted
    2. Composition API 可以将单个数据的操作逻辑代码连成一片, Options API需要在不同的属性中去查找
    3. Composition API 可以更灵活的组织代码的逻辑、结构、提取公共内容


3、Proxy 相对于 Object.defineProperty 有哪些优点？

答: 1. Proxy 是代理整个对象, Object.defineProperty 需要对对象的属性挨个遍历增加监听
    2. Proxy 可以监听到对象属性的增加、删除
    3. Proxy 可以监听到数组的索引、length

4、Vue 3.0 在编译方面有哪些优化？

答: 1. 使用Fragments来组织代码, 不需要唯一静态根节点, 直接放入文本、多个同级标签也可
    2. 标记提升静态节点 
    3. diff时只处理动态节点, 跳过静态节点
    4. 缓存事件处理函数, 减少不必要的更新操作


5、Vue.js 3.0 响应式系统的实现原理？

答: 1. 通过 Proxy 来代理对象
    2. 通过 reactive/toRefs/ref/computed 等方法来转化响应式对象
    3. 通过 effect/track/trigger 来收集、触发依赖
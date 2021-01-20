createApp -> ensureRenderer -> createRenderer -> baseCreateRenderer

baseCreateRenderer:
packages/runtime-core/src/renderer.ts
一个特别大的文件，返回 { render, hydrate, createApp }
其中这个对象里面的 createAPP -> createAppAPI

createAppAPI:
packages/runtime-core/src/apiCreateApp.ts
返回一个对象，挂了一些东西在上面
{
  app: {
    _uid: uid++,
    _component: rootComponent as ConcreteComponent,
    _props: rootProps,
    _container: null,
    _context: context,
    version,
    config的 get 和 set 方法
    use, mixin, component, directive, mount, unmount, provide 方法
  },
  config: {
    isNativeTag: NO,
    performance: false,
    globalProperties: {},
    optionMergeStrategies: {},
    isCustomElement: NO,
    errorHandler: undefined,
    warnHandler: undefined
  },
  mixins: [],
  components: {},
  directives: {},
  provides: Object.create(null)
}

_createVNode:
创建 vnode ,也就是一个 js 对象

setupComponent:


# HiUI 文档

## alert 组件

### banner.stories.tsx

```typescript
import React from 'react'
import Alert from '@hi-ui/alert'

/**
 * @title Banner 公告
 */
export const Banner = () => {
  return (
    <>
      <h1>Banner 公告</h1>
      <div className="alert-banner__wrap">
        <Alert
          showIcon={false}
          closeable={false}
          type="primary"
          title="信息提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          showIcon={false}
          closeable={false}
          type="success"
          title="成功提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          showIcon={false}
          closeable={false}
          type="danger"
          title="错误提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          showIcon={false}
          closeable={false}
          type="warning"
          title="警示提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Alert from '@hi-ui/alert'

/**
 * @title 基础用法
 * @desc 根据用户的操作进行页面级或模块、区块级的提示
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="alert-basic__wrap">
        <Alert
          type="primary"
          title="信息提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          type="success"
          title="成功提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          type="danger"
          title="错误提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          type="warning"
          title="警示提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
      </div>
    </>
  )
}

```

### carousel.stories.tsx

```typescript
import React from 'react'
import { TextLoop } from 'react-text-loop-next'
import Marquee from 'react-fast-marquee'
import Alert from '@hi-ui/alert'

/**
 * @title 轮播通知
 */
export const Carousel = () => {
  return (
    <>
      <h1>轮播通知</h1>
      <div className="alert-Carousel__wrap">
        <Alert
          title={
            <TextLoop mask>
              <div>蒹葭苍苍，白露为霜。</div>
              <div>所谓伊人，在水一方。</div>
              <div>溯洄从之，道阻且长。</div>
              <div>溯游从之，宛在水中央。</div>
              <div>蒹葭凄凄，白露未晞。</div>
            </TextLoop>
          }
        />
        <br />
        <Alert
          title={
            <Marquee pauseOnHover gradient={false}>
              所谓伊人，在水之湄。溯洄从之，道阻且跻。溯游从之，宛在水中坻。蒹葭采采，白露未已。
            </Marquee>
          }
        />
      </div>
    </>
  )
}

```

### closable.stories.tsx

```typescript
import React from 'react'
import Alert from '@hi-ui/alert'

/**
 * @title 不可关闭
 * @desc 反馈信息较为重要，需要引导用户阅读或关注
 */
export const Closable = () => {
  return (
    <>
      <h1>不可关闭</h1>
      <div className="alert-closable__wrap">
        <Alert type="primary" title="信息提示的文案" closeable={false} />
        <br />
        <Alert type="success" title="成功提示的文案" closeable={false} />
        <br />
        <Alert type="danger" title="错误提示的文案" closeable={false} />
        <br />
        <Alert type="warning" title="警示提示的文案" closeable={false} />
      </div>
    </>
  )
}

```

### close-icon.stories.tsx

```typescript
import React from 'react'
import Alert from '@hi-ui/alert'

/**
 * @title 自定义关闭按钮
 */
export const CloseIcon = () => {
  return (
    <>
      <h1>自定义关闭按钮</h1>
      <div className="alert-close-icon__wrap">
        <Alert
          type="primary"
          title="信息提示的文案"
          closeIcon={<span style={{ fontSize: 12 }}>Close</span>}
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
      </div>
    </>
  )
}

```

### content.stories.tsx

```typescript
import React from 'react'
import Alert from '@hi-ui/alert'
import Button from '@hi-ui/button'

/**
 * @title 带内容
 * @desc 反馈给用户的信息较多，需要用户阅读更详细
 */
export const Content = () => {
  return (
    <>
      <h1>带内容</h1>
      <div className="alert-basic__wrap">
        <Alert
          type="primary"
          title="信息提示的文案"
          content={
            <span style={{ display: 'flex', justifyContent: 'space-between', marginRight: -24 }}>
              <span>文字说明文字说明文字说明</span>
              <Button type="secondary" appearance="link">
                操作按钮
              </Button>
            </span>
          }
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          type="success"
          title="成功提示的文案"
          content={
            <span style={{ display: 'flex', justifyContent: 'space-between', marginRight: -24 }}>
              <span>文字说明文字说明文字说明</span>
              <Button type="success" appearance="link">
                操作按钮
              </Button>
            </span>
          }
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          type="danger"
          title="错误提示的文案"
          content={
            <span style={{ display: 'flex', justifyContent: 'space-between', marginRight: -24 }}>
              <span>文字说明文字说明文字说明</span>
              <Button type="danger" appearance="link">
                操作按钮
              </Button>
            </span>
          }
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          type="warning"
          title="警示提示的文案"
          content={
            <span style={{ display: 'flex', justifyContent: 'space-between', marginRight: -24 }}>
              <span>文字说明文字说明文字说明</span>
              <Button appearance="link">操作按钮</Button>
            </span>
          }
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
      </div>
    </>
  )
}

```

### duration.stories.tsx

```typescript
import React from 'react'
import Alert from '@hi-ui/alert'

/**
 * @title 倒计时自动关闭
 * @desc 倒计时自动关闭反馈信息在出现一定时间后自动关闭，不打扰。注：最大值不能超过 2^31-1
 */
export const Duration = () => {
  return (
    <>
      <h1>自动关闭</h1>
      <div className="alert-Duration__wrap">
        <Alert
          duration={1000}
          type="primary"
          title="信息提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          duration={2000}
          type="success"
          title="成功提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          duration={3000}
          type="danger"
          title="错误提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          duration={4000}
          type="warning"
          title="警示提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Alert from '@hi-ui/alert'
import Button from '@hi-ui/button'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>Size</h1>
      <div className="alert-size__wrap">
        <h2>lg</h2>
        <Alert
          type="primary"
          title="信息提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          type="primary"
          title="信息提示的文案"
          content={
            <span style={{ display: 'flex', justifyContent: 'space-between', marginRight: -24 }}>
              <span>文字说明文字说明文字说明</span>
              <Button type="secondary" appearance="link">
                操作按钮
              </Button>
            </span>
          }
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <h2>md</h2>
        <Alert
          type="primary"
          size={'md'}
          title="信息提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          type="primary"
          size={'md'}
          title="信息提示的文案"
          content={
            <span style={{ display: 'flex', justifyContent: 'space-between', marginRight: -24 }}>
              <span>文字说明文字说明文字说明</span>
              <Button type="secondary" appearance="link">
                操作按钮
              </Button>
            </span>
          }
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <h2>sm</h2>
        <Alert
          type="primary"
          size={'sm'}
          title="信息提示的文案"
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
        <br />
        <Alert
          type="primary"
          size={'sm'}
          title="信息提示的文案"
          content={
            <span style={{ display: 'flex', justifyContent: 'space-between', marginRight: -24 }}>
              <span>文字说明文字说明文字说明</span>
              <Button type="secondary" appearance="link">
                操作按钮
              </Button>
            </span>
          }
          onClose={() => {
            console.log('alert关闭回调')
          }}
        />
      </div>
    </>
  )
}

```

## anchor 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Anchor, { AnchorItem } from '@hi-ui/anchor'

/**
 * @title 基础用法
 * @desc 通过滚动或点击触发锚点节点的切换，需要注意 href 设置的是元素的 id 属性 `#id`
 */
export const Basic = () => {
  const [containerElement, setContainerElement] = React.useState<HTMLDivElement | null>(null)

  const scrollAreaNode = (
    <div
      style={{
        backgroundColor: '#f5f7fa',
        textAlign: 'center',
        height: '400px',
        lineHeight: '400px',
        color: '#1f2733',
      }}
    >
      Scroll Area
    </div>
  )

  return (
    <>
      <h1>Basic</h1>
      <div className="anchor-basic__wrap" style={{ display: 'flex', minWidth: 660 }}>
        <Anchor style={{ width: 148 }} container={containerElement} offset={-20}>
          <AnchorItem href="#test-basic-h1-1" title="容器化部署"></AnchorItem>
          <AnchorItem href="#test-basic-h1-2" title="主要优点"></AnchorItem>
          <AnchorItem href="#test-basic-h1-3" title="部署前准备"></AnchorItem>
          <AnchorItem href="#test-basic-h1-4" title="发布模拟"></AnchorItem>
          <AnchorItem href="#test-basic-h1-5" title="其它部署方式"></AnchorItem>
        </Anchor>
        <div
          ref={setContainerElement}
          style={{
            overflow: 'scroll',
            maxHeight: 320,
            border: '1px solid #f5f7fa',
            padding: '0 24px',
            flex: 1,
          }}
        >
          <h2 id="test-basic-h1-1">容器化部署</h2>
          {scrollAreaNode}
          <h2 id="test-basic-h1-2">主要优点</h2>
          {scrollAreaNode}
          <h2 id="test-basic-h1-3">部署前准备</h2>
          {scrollAreaNode}
          <h2 id="test-basic-h1-4">发布模拟</h2>
          {scrollAreaNode}
          <h2 id="test-basic-h1-5">其它部署方式</h2>
          {scrollAreaNode}
        </div>
      </div>
    </>
  )
}

```

### children.stories.tsx

```typescript
import React from 'react'
import Anchor, { AnchorItem } from '@hi-ui/anchor'

/**
 * @title 多级树形锚点
 * @desc 作为 `AnchorItem` 的子节点传入，扩展树形锚点的层级
 */
export const Children = () => {
  const [containerElement, setContainerElement] = React.useState<HTMLDivElement | null>(null)

  const scrollAreaNode = (
    <div
      style={{
        backgroundColor: '#f5f7fa',
        textAlign: 'center',
        height: '400px',
        lineHeight: '400px',
        color: '#1f2733',
      }}
    >
      Scroll Area
    </div>
  )

  return (
    <>
      <h1>Children</h1>
      <div className="anchor-children__wrap" style={{ display: 'flex', minWidth: 660 }}>
        <Anchor style={{ width: 148 }} container={containerElement} offset={-20}>
          <AnchorItem href="#test-children-h1-1" title="容器化部署"></AnchorItem>
          <AnchorItem href="#test-children-h1-2" title="主要优点"></AnchorItem>
          <AnchorItem href="#test-children-h1-3" title="部署前准备">
            <AnchorItem href="#test-children-h1-4" title="申请部署空间"></AnchorItem>
            <AnchorItem href="#test-children-h1-5" title="CI变量配置"></AnchorItem>
          </AnchorItem>
          <AnchorItem href="#test-children-h1-6" title="发布模拟"></AnchorItem>
        </Anchor>
        <div
          ref={setContainerElement}
          style={{
            overflow: 'scroll',
            maxHeight: 320,
            border: '1px solid #f5f7fa',
            padding: '0 24px',
            flex: 1,
          }}
        >
          <h2 id="test-children-h1-1">容器化部署</h2>
          {scrollAreaNode}
          <h2 id="test-children-h1-2">主要优点</h2>
          {scrollAreaNode}
          <h2 id="test-children-h1-3">部署前准备</h2>
          {scrollAreaNode}
          <h3 id="test-children-h1-4">申请部署空间</h3>
          {scrollAreaNode}
          <h3 id="test-children-h1-5">CI变量配置</h3>
          <div style={{ height: 300 }}></div>
          <h2 id="test-children-h1-6">发布模拟</h2>
          {scrollAreaNode}
        </div>
      </div>
    </>
  )
}

```

### offset.stories.tsx

```typescript
import React from 'react'
import Anchor, { AnchorItem } from '@hi-ui/anchor'

/**
 * @title 设置滚动偏移量
 * @desc 通过 `offset` 指定锚点节点触发的滚动偏移量，负值表示提前触发
 */
export const Offset = () => {
  const [containerElement, setContainerElement] = React.useState<HTMLDivElement | null>(null)

  const scrollAreaNode = (
    <div
      style={{
        backgroundColor: '#f5f7fa',
        textAlign: 'center',
        height: '400px',
        lineHeight: '400px',
        color: '#1f2733',
      }}
    >
      Scroll Area
    </div>
  )

  return (
    <>
      <h1>Offset</h1>
      <div className="anchor-offset__wrap" style={{ display: 'flex', minWidth: 660 }}>
        <Anchor style={{ width: 148 }} container={containerElement} offset={-20}>
          <AnchorItem href="#test-offset-h1-1" title="容器化部署"></AnchorItem>
          <AnchorItem href="#test-offset-h1-2" title="主要优点" offset={-100}></AnchorItem>
          <AnchorItem href="#test-offset-h1-3" title="部署前准备"></AnchorItem>
          <AnchorItem href="#test-offset-h1-4" title="发布模拟"></AnchorItem>
          <AnchorItem href="#test-offset-h1-5" title="其它部署方式"></AnchorItem>
        </Anchor>
        <div
          ref={setContainerElement}
          style={{
            overflow: 'scroll',
            maxHeight: 320,
            border: '1px solid #f5f7fa',
            padding: '0 24px',
            flex: 1,
          }}
        >
          <h2 id="test-offset-h1-1">容器化部署</h2>
          {scrollAreaNode}
          <h2 id="test-offset-h1-2">主要优点</h2>
          {scrollAreaNode}
          <h2 id="test-offset-h1-3">部署前准备</h2>
          {scrollAreaNode}
          <h2 id="test-offset-h1-4">发布模拟</h2>
          {scrollAreaNode}
          <h2 id="test-offset-h1-5">其它部署方式</h2>
          {scrollAreaNode}
        </div>
      </div>
    </>
  )
}

```

### overflow.stories.tsx

```typescript
import React from 'react'
import Anchor, { AnchorItem } from '@hi-ui/anchor'

/**
 * @title 文本溢出
 * @desc 锚点文字不建议太长，超出会溢出展示
 */
export const Overflow = () => {
  const [containerElement, setContainerElement] = React.useState<HTMLDivElement | null>(null)

  const scrollAreaNode = (
    <div
      style={{
        backgroundColor: '#f5f7fa',
        textAlign: 'center',
        height: '400px',
        lineHeight: '400px',
        color: '#1f2733',
      }}
    >
      Scroll Area
    </div>
  )

  return (
    <>
      <h1>Overflow</h1>
      <div className="anchor-overflow__wrap" style={{ display: 'flex', minWidth: 660 }}>
        <Anchor style={{ width: 148 }} container={containerElement} offset={-20}>
          <AnchorItem href="#test-overflow-h1-1" title="一级目录1号"></AnchorItem>
          <AnchorItem href="#test-overflow-h1-2" title="一级目录2号"></AnchorItem>
          <AnchorItem href="#test-overflow-h1-3" title="一级目录3号"></AnchorItem>
          <AnchorItem href="#test-overflow-h1-4" title="一级目录4号字数较多字数较多"></AnchorItem>
          <AnchorItem href="#test-overflow-h1-5" title="一级目录5号"></AnchorItem>
        </Anchor>
        <div
          ref={setContainerElement}
          style={{
            overflow: 'scroll',
            maxHeight: 320,
            border: '1px solid #f5f7fa',
            padding: '0 24px',
            flex: 1,
          }}
        >
          <h2 id="test-overflow-h1-1">一级目录1号</h2>
          {scrollAreaNode}
          <h2 id="test-overflow-h1-2">一级目录2号</h2>
          {scrollAreaNode}
          <h2 id="test-overflow-h1-3">一级目录3号</h2>
          {scrollAreaNode}
          <h2 id="test-overflow-h1-4">一级目录4号字数较多字数较多</h2>
          {scrollAreaNode}
          <h2 id="test-overflow-h1-5">一级目录5号</h2>
          {scrollAreaNode}
        </div>
      </div>
    </>
  )
}

```

## avatar 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Avatar from '@hi-ui/avatar'

/**
 * @title 基础用法
 * @desc 提供基础的默认头像
 */
export const Basic = () => {
  return (
    <>
      <h1>Avatar</h1>
      <div
        className="avatar-basic__wrap"
        style={{ display: 'flex', flexWrap: 'wrap', gap: 24, alignItems: 'center' }}
      >
        <Avatar bordered />
      </div>
    </>
  )
}

```

### content.stories.tsx

```typescript
import React from 'react'
import Avatar from '@hi-ui/avatar'
import { EditOutlined, PlusOutlined } from '@hi-ui/icons'

/**
 * @title 不同内容
 * @desc 支持在头像容器中放置不同的内容元素
 */
export const Content = () => {
  return (
    <>
      <h1>不同内容</h1>
      <div
        className="avatar-content__wrap"
        style={{ display: 'flex', flexWrap: 'wrap', gap: 24, alignItems: 'center' }}
      >
        <Avatar />
        <Avatar initials="M" />
        <Avatar icon={<PlusOutlined />} />
        <Avatar>
          <EditOutlined />
        </Avatar>
        <Avatar initials="HiUI" />
        <Avatar src="https://avatars.githubusercontent.com/u/810438?v=4" initials="P" />
        <Avatar>
          <img
            alt="avatar"
            src="//p1-arco.byteimg.com/tos-cn-i-uwbnlip3yd/3ee5f13fb09879ecb5185e440cef6eb9.png~tplv-uwbnlip3yd-webp.webp"
          />
        </Avatar>
      </div>
    </>
  )
}

```

### custom-color.stories.tsx

```typescript
import React from 'react'
import Avatar from '@hi-ui/avatar'

/**
 * @title 自定义颜色
 * @desc 设置 style 自定义头像的背景色
 *
 */
export const CustomColor = () => {
  return (
    <>
      <h1>CustomColor</h1>
      <div
        className="avatar-custom-color__wrap"
        style={{ display: 'flex', flexWrap: 'wrap', gap: 24, alignItems: 'center' }}
      >
        <Avatar initials="M" style={{ backgroundColor: '#237ffa' }} />
        <Avatar initials="H" style={{ backgroundColor: '#9772fb' }} />
        <Avatar initials="Z" style={{ backgroundColor: '#0daeff' }} />
        <Avatar initials="Q" style={{ backgroundColor: '#38d677' }} />
        <Avatar initials="P" style={{ backgroundColor: '#fab007' }} />
        <Avatar initials="Y" style={{ backgroundColor: '#fe7940' }} />
      </div>
    </>
  )
}

```

### custom-size.stories.tsx

```typescript
import React from 'react'
import Avatar from '@hi-ui/avatar'

/**
 * @title 自定义尺寸
 * @desc 通过 size 传入数值自定义头像大小
 */
export const CustomSize = () => {
  return (
    <>
      <h1>CustomSize</h1>
      <div
        className="avatar-custom-size__wrap"
        style={{ display: 'flex', flexWrap: 'wrap', gap: 24, alignItems: 'center' }}
      >
        <Avatar size={20} initials="P" style={{ backgroundColor: '#237ffa' }} />
        <Avatar size={40} initials="P" style={{ backgroundColor: '#237ffa' }} />
      </div>
    </>
  )
}

```

### shape.stories.tsx

```typescript
import React from 'react'
import Avatar from '@hi-ui/avatar'

/**
 * @title 不同形状
 * @desc 通过 shape 指定头像的形状
 */
export const Shape = () => {
  return (
    <>
      <h1>不同形状</h1>
      <div
        className="avatar-basic__wrap"
        style={{ display: 'flex', flexWrap: 'wrap', gap: 24, alignItems: 'center' }}
      >
        <Avatar
          src="https://avatars.githubusercontent.com/u/810438?v=4"
          initials="P"
          shape="circle"
        />
        <Avatar
          src="https://avatars.githubusercontent.com/u/810438?v=4"
          initials="P"
          shape="square"
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Avatar from '@hi-ui/avatar'

/**
 * @title 不同尺寸
 * @desc 默认支持 5 种头像标准尺寸，通过 size 设置
 */
export const Size = () => {
  return (
    <>
      <h1>不同尺寸</h1>
      <div className="avatar-basic__wrap">
        <div
          style={{
            display: 'flex',
            flexWrap: 'wrap',
            gap: 24,
            alignItems: 'center',
            marginBottom: 20,
          }}
        >
          <Avatar src="https://avatars.githubusercontent.com/u/810438?v=4" initials="P" size="xs" />
          <Avatar src="https://avatars.githubusercontent.com/u/810438?v=4" initials="P" size="sm" />
          <Avatar src="https://avatars.githubusercontent.com/u/810438?v=4" initials="P" size="md" />
          <Avatar src="https://avatars.githubusercontent.com/u/810438?v=4" initials="P" size="lg" />
          <Avatar src="https://avatars.githubusercontent.com/u/810438?v=4" initials="P" size="xl" />
        </div>
        <div
          style={{
            display: 'flex',
            flexWrap: 'wrap',
            gap: 24,
            alignItems: 'center',
            marginBottom: 20,
          }}
        >
          <Avatar initials="P" size="xs" />
          <Avatar initials="P" size="sm" />
          <Avatar initials="P" size="md" />
          <Avatar initials="P" size="lg" />
          <Avatar initials="P" size="xl" />
        </div>
        <div
          style={{
            display: 'flex',
            flexWrap: 'wrap',
            gap: 24,
            alignItems: 'center',
            marginBottom: 20,
          }}
        >
          <Avatar
            src="https://avatars.githubusercontent.com/u/810438?v=4"
            initials="P"
            shape="square"
            size="xs"
          />
          <Avatar
            src="https://avatars.githubusercontent.com/u/810438?v=4"
            initials="P"
            shape="square"
            size="sm"
          />
          <Avatar
            src="https://avatars.githubusercontent.com/u/810438?v=4"
            initials="P"
            shape="square"
            size="md"
          />
          <Avatar
            src="https://avatars.githubusercontent.com/u/810438?v=4"
            initials="P"
            shape="square"
            size="lg"
          />
          <Avatar
            src="https://avatars.githubusercontent.com/u/810438?v=4"
            initials="P"
            shape="square"
            size="xl"
          />
        </div>
      </div>
    </>
  )
}

```

## back-top 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Tooltip from '@hi-ui/tooltip'
import { ArrowUpOutlined } from '@hi-ui/icons'
import BackTop from '@hi-ui/back-top'

/**
 * @title 基础用法
 * @desc 当滚动到设定高度时，会出现回到顶部按钮，点击回到最顶部
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="back-top-basic__wrap">
        <div style={{ position: 'relative', height: 400 }}>
          <BackTop
            style={{ position: 'absolute' }}
            container={() => document.getElementById('back-top_target')}
          />
          <div
            id="back-top_target"
            style={{ position: 'relative', height: 400, overflowY: 'scroll' }}
          >
            {Array.from({ length: 10 }, (_, index) => (
              <div key={index} style={{ padding: 30, background: '#f2f3f7' }}>
                页面内容{index}
              </div>
            ))}
          </div>
        </div>
      </div>
      <BackTop>
        <Tooltip title="回到顶部" placement="left" disabledPortal={true}>
          <div
            style={{
              display: 'flex',
              alignItems: 'center',
              justifyContent: 'center',
              width: 40,
              height: 40,
              borderRadius: '50%',
              color: '#fff',
              background: '#237ffa',
            }}
          >
            <ArrowUpOutlined />
          </div>
        </Tooltip>
      </BackTop>
    </>
  )
}

```

### compose.stories.tsx

```typescript
import React from 'react'
import { ScanOutlined, MessageOutlined } from '@hi-ui/icons'
import BackTop from '@hi-ui/back-top'

/**
 * @title 组合使用
 * @desc 和其他元素组合使用
 */
export const Compose = () => {
  return (
    <>
      <h1>组合用法</h1>
      <div className="back-top-basic__wrap">
        <div style={{ position: 'relative', height: 400 }}>
          <div
            style={{
              position: 'absolute',
              right: 32,
              bottom: 88,
              width: 40,
              zIndex: 9,
            }}
          >
            <div
              style={{
                display: 'flex',
                alignItems: 'center',
                justifyContent: 'center',
                width: 40,
                height: 40,
                borderRadius: '50%',
                background: '#fff',
                color: '#5f6a7a',
                fontSize: 20,
                boxShadow: '0 12px 24px 8px rgba(31, 39, 51, 0.1)',
              }}
            >
              <ScanOutlined />
            </div>
            <div
              style={{
                display: 'flex',
                alignItems: 'center',
                justifyContent: 'center',
                width: 40,
                height: 40,
                borderRadius: '50%',
                background: '#fff',
                color: '#5f6a7a',
                fontSize: 20,
                boxShadow: '0 12px 24px 8px rgba(31, 39, 51, 0.1)',
                marginTop: 16,
              }}
            >
              <MessageOutlined />
            </div>
          </div>
          <BackTop
            shape="circle"
            style={{ position: 'absolute' }}
            container={() => document.getElementById('back-top_compose')}
          />
          <div
            id="back-top_compose"
            style={{ position: 'relative', height: 400, overflowY: 'scroll' }}
          >
            {Array.from({ length: 10 }, (_, index) => (
              <div key={index} style={{ padding: 30, background: '#f2f3f7' }}>
                页面内容{index}
              </div>
            ))}
          </div>
        </div>
      </div>
    </>
  )
}

```

### custom.stories.tsx

```typescript
import React from 'react'
import Tooltip from '@hi-ui/tooltip'
import { ToTopOutlined } from '@hi-ui/icons'

import BackTop from '@hi-ui/back-top'

/**
 * @title 自定义按钮位置和内容
 * @desc 给组件传入样式和children
 */
export const Custom = () => {
  return (
    <>
      <h1>自定义按钮位置和内容</h1>
      <div className="back-top-basic__wrap">
        <div style={{ position: 'relative', height: 400 }}>
          <Tooltip title="回到顶部" placement="left">
            <BackTop
              style={{ position: 'absolute', right: 50, bottom: 112 }}
              container={() => document.getElementById('back-top_custom')}
            >
              <div
                style={{
                  display: 'flex',
                  alignItems: 'center',
                  justifyContent: 'center',
                  width: 40,
                  height: 40,
                  borderRadius: '50%',
                  color: '#fff',
                  background: '#237ffa',
                }}
              >
                <ToTopOutlined />
              </div>
            </BackTop>
          </Tooltip>
          <div
            id="back-top_custom"
            style={{ position: 'relative', height: 400, overflowY: 'scroll' }}
          >
            {Array.from({ length: 10 }, (_, index) => (
              <div key={index} style={{ padding: 30, background: '#f2f3f7' }}>
                页面内容{index}
              </div>
            ))}
          </div>
        </div>
      </div>
    </>
  )
}

```

### settings.stories.tsx

```typescript
import React, { useState } from 'react'
import Space from '@hi-ui/space'
import Select from '@hi-ui/select'
import Input from '@hi-ui/input'
import BackTop from '@hi-ui/back-top'

/**
 * @title 参数设置
 * @desc 设置按钮形状、主题、滚动时间、滚动到多高时显示
 */
export const Settings = () => {
  const [shape, setShape] = useState<any>('circle')
  const [duration, setDuration] = useState<any>(400)
  const [visibleHeight, setVisibleHeight] = useState<any>(400)

  return (
    <>
      <h1>设置按钮形状、主题、滚动时间、滚动到多高时显示</h1>
      <div className="back-top-basic__wrap">
        <Space style={{ marginBottom: 20 }}>
          <span>形状</span>
          <Select
            style={{ width: 110, marginRight: 20 }}
            clearable={false}
            value={shape}
            onChange={setShape}
            data={[
              { id: 'circle', title: '圆形' },
              { id: 'square', title: '圆角矩形' },
            ]}
          />
          <span>滚动时间(ms)</span>
          <Input
            value={duration}
            onChange={(data) => setDuration(data.target.value)}
            style={{ width: 110, marginRight: 20 }}
          />
          <span>visibleHeight</span>
          <Input
            value={visibleHeight}
            onChange={(data) => setVisibleHeight(data.target.value)}
            style={{ width: 110 }}
          />
        </Space>
        <div style={{ position: 'relative', height: 400 }}>
          <BackTop
            shape={shape}
            duration={duration}
            visibleHeight={visibleHeight}
            style={{ position: 'absolute' }}
            container={() => document.getElementById('back-top_setting')}
          />
          <div
            id="back-top_setting"
            style={{ position: 'relative', height: 400, overflowY: 'scroll' }}
          >
            {Array.from({ length: 10 }, (_, index) => (
              <div key={index} style={{ padding: 30, background: '#f2f3f7' }}>
                页面内容{index}
              </div>
            ))}
          </div>
        </div>
      </div>
    </>
  )
}

```

## badge 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Badge from '@hi-ui/badge'
import { Button } from '@hi-ui/button'
import { BellOutlined } from '@hi-ui/icons'

/**
 * @title 基础用法
 * @desc 标识是否有新消息
 */
export const Basic = () => {
  return (
    <>
      <h1>红点</h1>
      <div className="badge-basic__wrap">
        <Badge type="dot">
          <Button type="default">最新报表</Button>
        </Badge>
        <br />
        <br />
        <Badge type="dot">
          <BellOutlined style={{ fontSize: '24px' }} />
        </Badge>
      </div>
    </>
  )
}

```

### bubble.stories.tsx

```typescript
import React from 'react'
import Badge from '@hi-ui/badge'
import { BellOutlined } from '@hi-ui/icons'

/**
 * @title 徽标
 * @desc 标识消息数或简洁描述
 */
export const Bubble = () => {
  return (
    <>
      <h1>徽标</h1>
      <div className="badge-basic__wrap">
        <div>
          <Badge content={8} style={{ marginRight: 20 }}>
            <BellOutlined style={{ fontSize: '24px' }} />
          </Badge>
          <Badge content={'new'} style={{ marginRight: 20 }}>
            <BellOutlined style={{ fontSize: '24px' }} />
          </Badge>
        </div>
      </div>
    </>
  )
}

```

### color.stories.tsx

```typescript
import React from 'react'
import { Button } from '@hi-ui/button'
import Badge from '@hi-ui/badge'

/**
 * @title 自定义颜色
 */
export const Color = () => {
  const colors = [
    'red',
    'yellow',
    'pink',
    'orange',
    'cyan',
    'blue',
    'green',
    'purple',
    'magenta',
    '#2db7f5',
    '#108ee9',
  ]

  return (
    <>
      <h1>自定义颜色</h1>
      <div className="badge-Color__wrap">
        {colors.map((color) => (
          <div key={color}>
            <Badge color={color} content="new">
              <Button>按钮</Button>
            </Badge>
            <br />
            <br />
          </div>
        ))}
      </div>
    </>
  )
}

```

### custom.stories.tsx

```typescript
import React from 'react'
import Badge from '@hi-ui/badge'
import { Button } from '@hi-ui/button'
import { BellOutlined } from '@hi-ui/icons'

/**
 * @title 自定义角标内容
 */
export const Custom = () => {
  return (
    <>
      <h1>自定义角标内容</h1>
      <div className="badge-Custom__wrap">
        <Badge content={<BellOutlined style={{ fontSize: 16, color: '#ff5959' }} />}>
          <Button type="default">最新报表</Button>
        </Badge>
        <br />
        <br />
        <Badge content={<BellOutlined style={{ fontSize: 16, color: '#ff5959' }} />} />
      </div>
    </>
  )
}

```

### independent.stories.tsx

```typescript
import React from 'react'
import Badge from '@hi-ui/badge'

/**
 * @title 独立使用
 */
export const Independent = () => {
  return (
    <>
      <h1>独立使用的</h1>
      <div className="badge-independent__wrap">
        <Badge type="dot" />
        <br />
        <br />
        <Badge content="16" />
      </div>
    </>
  )
}

```

### max.stories.tsx

```typescript
import React from 'react'
import Badge from '@hi-ui/badge'
import { Avatar } from '@hi-ui/avatar'

/**
 * @title 数值显示上限
 */
export const Max = () => {
  return (
    <>
      <h1>数值显示上限</h1>
      <div className="badge-max__wrap">
        <Badge content={2000} max={999}>
          <Avatar src="https://avatars.githubusercontent.com/u/810438?v=4" initials="P" />
        </Badge>
      </div>
    </>
  )
}

```

### offset.stories.tsx

```typescript
import React from 'react'
import Badge from '@hi-ui/badge'
import { Button } from '@hi-ui/button'

/**
 * @title 位置偏移
 */
export const Offset = () => {
  return (
    <>
      <h1>位置偏移</h1>
      <div className="badge-offset__wrap">
        <Badge type="dot" offset={[4, -4]}>
          <Button type="default">最新报表</Button>
        </Badge>
        <br />
        <br />
        <Badge content={8} offset={[8, -8]}>
          <Button type="default">最新报表</Button>
        </Badge>
      </div>
    </>
  )
}

```

## breadcrumb 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Breadcrumb from '@hi-ui/breadcrumb'

/**
 * @title 基础用法
 * @desc 明确访问路径的每一个节点
 */
export const Basic = () => {
  const [data] = React.useState([
    {
      title: '首页',
      href: '/home',
    },
    {
      title: '列表',
      href: '/list',
    },
    {
      title: '手机详情',
      href: '/phone',
    },
  ])

  return (
    <>
      <h1>基础用法</h1>
      <div className="breadcrumb-basic__wrap">
        <Breadcrumb
          data={data}
          onClick={(evt, item) => {
            console.log('get item: ', item)
          }}
        />
      </div>
    </>
  )
}

```

### custom-icon.stories.tsx

```typescript
import React from 'react'
import Breadcrumb from '@hi-ui/breadcrumb'
import { HomeOutlined } from '@hi-ui/icons'

/**
 * @title 前缀图标
 */
export const CustomIcon = () => {
  const [data] = React.useState([
    {
      icon: <HomeOutlined />,
      title: '首页',
      href: '/home',
    },
    {
      icon: <HomeOutlined />,
      title: '列表',
      href: '/list',
    },
    {
      icon: <HomeOutlined />,
      title: '手机详情',
      href: '/phone',
    },
  ])

  return (
    <>
      <h1>自定义 Icon </h1>
      <div className="breadcrumb-custom-icon__wrap">
        <Breadcrumb
          data={data}
          onClick={(evt, item) => {
            console.log('get item: ', item)
          }}
        />
      </div>
    </>
  )
}

```

### separator.stories.tsx

```typescript
import { RightOutlined } from '@hi-ui/icons'
import React from 'react'
import Breadcrumb from '@hi-ui/breadcrumb'

/**
 * @title 自定义分隔符
 */
export const Separator = () => {
  const [data] = React.useState([
    {
      title: '首页',
      href: '/home',
    },
    {
      title: '列表',
      href: '/list',
    },
    {
      title: '手机详情',
      href: '/phone',
    },
  ])

  return (
    <>
      <h1>自定义分隔符</h1>
      <div className="breadcrumb-separator__wrap">
        <Breadcrumb
          data={data}
          separator={<RightOutlined style={{ fontSize: 16 }} />}
          onClick={(evt, item) => {
            console.log('get item: ', item)
          }}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Breadcrumb from '@hi-ui/breadcrumb'

/**
 * @title 不同尺寸
 * @desc 通过 size 设置不同大小的面包屑
 */
export const Size = () => {
  const [data] = React.useState([
    {
      title: '首页',
      href: '/home',
    },
    {
      title: '列表',
      href: '/list',
    },
    {
      title: '手机详情',
      href: '/phone',
    },
  ])

  return (
    <>
      <h1>不同尺寸</h1>
      <div className="breadcrumb-size__wrap">
        <Breadcrumb
          data={data}
          size="sm"
          onClick={(evt, item) => {
            console.log('get item: ', item)
          }}
        />
        <br />
        <Breadcrumb
          data={data}
          size="md"
          onClick={(evt, item) => {
            console.log('get item: ', item)
          }}
        />
      </div>
    </>
  )
}

```

## button 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>不同类型</h1>
      <div className="button-basic__wrap">
        <Button type="primary">主要按钮</Button>
        <Button type="secondary">次要按钮</Button>
        <Button type="default">中性按钮</Button>
        <Button type="danger">危险按钮</Button>
        <Button type="success">成功按钮</Button>
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import { PlusOutlined } from '@hi-ui/icons'

/**
 * @title 禁用状态
 * @desc 暂不可操作的状态
 */
export const Disabled = () => {
  return (
    <>
      <h1>禁用</h1>
      <div className="button-basic__wrap">
        <div style={{ marginBottom: 24 }}>
          <Button type="primary" icon={<PlusOutlined />} disabled>
            面性按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} disabled />
          <Button type="secondary" icon={<PlusOutlined />} disabled>
            面性按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} disabled />
          <Button icon={<PlusOutlined />} disabled>
            面性按钮
          </Button>
          <Button icon={<PlusOutlined />} disabled />
          <Button type="danger" icon={<PlusOutlined />} disabled>
            面性按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} disabled />
          <Button type="success" icon={<PlusOutlined />} disabled>
            面性按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} disabled />
        </div>
        <div style={{ marginBottom: 24 }}>
          <Button type="primary" icon={<PlusOutlined />} appearance="line" disabled>
            线性按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} appearance="line" disabled />
          <Button type="secondary" icon={<PlusOutlined />} appearance="line" disabled>
            线性按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} appearance="line" disabled />
          <Button icon={<PlusOutlined />} appearance="line" disabled>
            线性按钮
          </Button>
          <Button icon={<PlusOutlined />} appearance="line" disabled />
          <Button type="danger" icon={<PlusOutlined />} appearance="line" disabled>
            线性按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} appearance="line" disabled />
          <Button type="success" icon={<PlusOutlined />} appearance="line" disabled>
            线性按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} appearance="line" disabled />
        </div>
        <div>
          <Button type="primary" icon={<PlusOutlined />} appearance="link" disabled>
            链接按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} appearance="link" disabled />
          <Button type="secondary" icon={<PlusOutlined />} appearance="link" disabled>
            链接按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} appearance="link" disabled />
          <Button icon={<PlusOutlined />} appearance="link" disabled>
            链接按钮
          </Button>
          <Button icon={<PlusOutlined />} appearance="link" disabled />
          <Button type="danger" icon={<PlusOutlined />} appearance="link" disabled>
            链接按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} appearance="link" disabled />
          <Button type="success" icon={<PlusOutlined />} appearance="link" disabled>
            链接按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} appearance="link" disabled />
        </div>
        {/* <div>
          <Button type="primary" icon={<PlusOutlined />} appearance="unset" disabled>
            无样式按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} appearance="unset" disabled />
          <Button type="secondary" icon={<PlusOutlined />} appearance="unset" disabled>
            无样式按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} appearance="unset" disabled />
          <Button icon={<PlusOutlined />} appearance="unset" disabled>
            无样式按钮
          </Button>
          <Button icon={<PlusOutlined />} appearance="unset" disabled />
          <Button type="danger" icon={<PlusOutlined />} appearance="unset" disabled>
            无样式按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} appearance="unset" disabled />
          <Button type="success" icon={<PlusOutlined />} appearance="unset" disabled>
            无样式按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} appearance="unset" disabled />
        </div> */}
      </div>
    </>
  )
}

```

### group.stories.tsx

```typescript
import React from 'react'
import { ButtonGroup, Button } from '@hi-ui/button'
import { EditOutlined } from '@hi-ui/icons'

/**
 * @title 按钮组
 * @desc 用于将有并列关系的一组动作，以组的形式展示
 */
export const Group = () => {
  return (
    <>
      <h1>按钮组</h1>
      <div className="button-basic__wrap" style={{ marginBottom: 20 }}>
        <ButtonGroup style={{ marginRight: 20 }}>
          <Button type="primary">主要按钮</Button>
          <Button type="primary">主要按钮</Button>
          <Button type="primary">主要按钮</Button>
        </ButtonGroup>

        <ButtonGroup>
          <Button>主要按钮</Button>
          <Button>主要按钮</Button>
          <Button>主要按钮</Button>
        </ButtonGroup>
      </div>
      <div className="button-basic__wrap" style={{ marginBottom: 20 }}>
        <ButtonGroup style={{ marginRight: 20 }}>
          <Button type="primary" icon={<EditOutlined />} />
          <Button type="primary" icon={<EditOutlined />} />
          <Button type="primary" icon={<EditOutlined />} />
        </ButtonGroup>

        <ButtonGroup>
          <Button icon={<EditOutlined />} />
          <Button icon={<EditOutlined />} />
          <Button icon={<EditOutlined />} />
        </ButtonGroup>
      </div>

      <div className="button-basic__wrap" style={{ marginBottom: 20 }}>
        <ButtonGroup style={{ marginRight: 20 }}>
          <Button type="primary">按钮</Button>
          <Button type="primary" icon={<EditOutlined />} />
        </ButtonGroup>

        <ButtonGroup>
          <Button>按钮</Button>
          <Button icon={<EditOutlined />} />
        </ButtonGroup>
      </div>
    </>
  )
}

```

### icon-link.stories.tsx

```typescript
import React from 'react'
import { PlusOutlined } from '@hi-ui/icons'
import Button from '@hi-ui/button'

/**
 * @title 带图标链接
 * @desc 强调动作含义或简化动作的操作区域
 */
export const IconLink = () => {
  return (
    <>
      <h1>Button</h1>
      <div className="button-basic__wrap">
        <Button type="primary" appearance="link" icon={<PlusOutlined />}>
          主要按钮
        </Button>
        <Button type="secondary" appearance="link" icon={<PlusOutlined />}>
          次要按钮
        </Button>
        <Button type="default" appearance="link" icon={<PlusOutlined />}>
          中性按钮
        </Button>
        <Button type="danger" appearance="link" icon={<PlusOutlined />}>
          危险按钮
        </Button>
        <Button type="success" appearance="link" icon={<PlusOutlined />}>
          成功按钮
        </Button>
      </div>
    </>
  )
}

```

### icon.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import { PlusOutlined } from '@hi-ui/icons'

/**
 * @title 带图标
 * @desc 图标能够明确表达按钮的动作含义，成组使用，与文字搭配，突出按钮的重要性
 */
export const Icon = () => {
  return (
    <>
      <h1>带图标</h1>
      <div className="button-basic__wrap">
        <div style={{ marginBottom: 24 }}>
          <Button type="primary" icon={<PlusOutlined />}>
            面性按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} />
          <Button type="secondary" icon={<PlusOutlined />}>
            面性按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} />
          <Button icon={<PlusOutlined />}>面性按钮</Button>
          <Button icon={<PlusOutlined />} />
          <Button type="danger" icon={<PlusOutlined />}>
            面性按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} />
          <Button type="success" icon={<PlusOutlined />}>
            面性按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} />
        </div>
        <div style={{ marginBottom: 24 }}>
          <Button type="primary" icon={<PlusOutlined />} appearance="line">
            线性按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} appearance="line" />
          <Button type="secondary" icon={<PlusOutlined />} appearance="line">
            线性按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} appearance="line" />
          <Button icon={<PlusOutlined />} appearance="line">
            线性按钮
          </Button>
          <Button icon={<PlusOutlined />} appearance="line" />
          <Button type="danger" icon={<PlusOutlined />} appearance="line">
            线性按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} appearance="line" />
          <Button type="success" icon={<PlusOutlined />} appearance="line">
            线性按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} appearance="line" />
        </div>
        <div>
          <Button type="primary" icon={<PlusOutlined />} appearance="link">
            链接按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} appearance="link" />
          <Button type="secondary" icon={<PlusOutlined />} appearance="link">
            链接按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} appearance="link" />
          <Button icon={<PlusOutlined />} appearance="link">
            链接按钮
          </Button>
          <Button icon={<PlusOutlined />} appearance="link" />
          <Button type="danger" icon={<PlusOutlined />} appearance="link">
            链接按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} appearance="link" />
          <Button type="success" icon={<PlusOutlined />} appearance="link">
            链接按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} appearance="link" />
        </div>
        {/* <div>
          <Button type="primary" icon={<PlusOutlined />} appearance="unset">
            链接按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} appearance="unset" />
          <Button type="secondary" icon={<PlusOutlined />} appearance="unset">
            链接按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} appearance="unset" />
          <Button icon={<PlusOutlined />} appearance="unset">
            链接按钮
          </Button>
          <Button icon={<PlusOutlined />} appearance="unset" />
          <Button type="danger" icon={<PlusOutlined />} appearance="unset">
            链接按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} appearance="unset" />
          <Button type="success" icon={<PlusOutlined />} appearance="unset">
            链接按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} appearance="unset" />
        </div> */}
      </div>
    </>
  )
}

```

### line.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'

/**
 * @title 线性风格
 */
export const Line = () => {
  return (
    <>
      <h1>Button</h1>
      <div className="button-basic__wrap">
        <Button type="primary" appearance="line">
          主要按钮
        </Button>
        <Button type="secondary" appearance="line">
          次要按钮
        </Button>
        <Button type="default" appearance="line">
          中性按钮
        </Button>
        <Button type="danger" appearance="line">
          危险按钮
        </Button>
        <Button type="success" appearance="line">
          成功按钮
        </Button>
      </div>
    </>
  )
}

```

### link.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'

/**
 * @title 文本链接
 * @desc 执行操作时发出页面请求，页面会给予明确的反馈
 */
export const Link = () => {
  return (
    <>
      <h1>Button</h1>
      <div className="button-basic__wrap">
        <Button type="primary" appearance="link">
          主要按钮
        </Button>
        <Button type="secondary" appearance="link">
          次要按钮
        </Button>
        <Button type="default" appearance="link">
          中性按钮
        </Button>
        <Button type="danger" appearance="link">
          危险按钮
        </Button>
        <Button type="success" appearance="link">
          成功按钮
        </Button>
      </div>
    </>
  )
}

```

### loading.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import { PlusOutlined } from '@hi-ui/icons'

/**
 * @title 加载中状态
 * @desc 请求服务器发生延迟时或缓冲状态，使用加载中进行状态说明
 */
export const Loading = () => {
  return (
    <>
      <h1>加载中</h1>
      <div className="button-basic__wrap">
        <div style={{ marginBottom: 24 }}>
          <Button type="primary" icon={<PlusOutlined />} loading>
            面性按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} loading />
          <Button type="secondary" icon={<PlusOutlined />} loading>
            面性按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} loading />
          <Button icon={<PlusOutlined />} loading>
            面性按钮
          </Button>
          <Button icon={<PlusOutlined />} loading />
          <Button type="danger" icon={<PlusOutlined />} loading>
            面性按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} loading />
          <Button type="success" icon={<PlusOutlined />} loading>
            面性按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} loading />
        </div>
        <div style={{ marginBottom: 24 }}>
          <Button type="primary" icon={<PlusOutlined />} appearance="line" loading>
            线性按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} appearance="line" loading />
          <Button type="secondary" icon={<PlusOutlined />} appearance="line" loading>
            线性按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} appearance="line" loading />
          <Button icon={<PlusOutlined />} appearance="line" loading>
            线性按钮
          </Button>
          <Button icon={<PlusOutlined />} appearance="line" loading />
          <Button type="danger" icon={<PlusOutlined />} appearance="line" loading>
            线性按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} appearance="line" loading />
          <Button type="success" icon={<PlusOutlined />} appearance="line" loading>
            线性按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} appearance="line" loading />
        </div>
        <div>
          <Button type="primary" icon={<PlusOutlined />} appearance="link" loading>
            链接按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} appearance="link" loading />
          <Button type="secondary" icon={<PlusOutlined />} appearance="link" loading>
            链接按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} appearance="link" loading />
          <Button icon={<PlusOutlined />} appearance="link" loading>
            链接按钮
          </Button>
          <Button icon={<PlusOutlined />} appearance="link" loading />
          <Button type="danger" icon={<PlusOutlined />} appearance="link" loading>
            链接按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} appearance="link" loading />
          <Button type="success" icon={<PlusOutlined />} appearance="link" loading>
            链接按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} appearance="link" loading />
        </div>
        {/* <div>
          <Button type="primary" icon={<PlusOutlined />} appearance="unset" loading>
            链接按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} appearance="unset" loading />
          <Button type="secondary" icon={<PlusOutlined />} appearance="unset" loading>
            链接按钮
          </Button>
          <Button type="secondary" icon={<PlusOutlined />} appearance="unset" loading />
          <Button icon={<PlusOutlined />} appearance="unset" loading>
            链接按钮
          </Button>
          <Button icon={<PlusOutlined />} appearance="unset" loading />
          <Button type="danger" icon={<PlusOutlined />} appearance="unset" loading>
            链接按钮
          </Button>
          <Button type="danger" icon={<PlusOutlined />} appearance="unset" loading />
          <Button type="success" icon={<PlusOutlined />} appearance="unset" loading>
            链接按钮
          </Button>
          <Button type="success" icon={<PlusOutlined />} appearance="unset" loading />
        </div> */}
      </div>
    </>
  )
}

```

### shape.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import { PlusOutlined } from '@hi-ui/icons'

/**
 * @title 不同形状
 */
export const Shape = () => {
  const btnRef = React.useRef(null)
  React.useEffect(() => {
    console.log(btnRef)
  }, [])
  return (
    <>
      <h1>不同形状</h1>
      <div className="button-basic__wrap">
        <div style={{ marginBottom: 24 }}>
          <Button type="primary" size="sm">
            小号按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} size="sm" />
          <Button type="primary">正常按钮</Button>
          <Button type="primary" icon={<PlusOutlined />} />
          <Button type="primary" size="lg">
            大号按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} size="lg" />
          <Button type="primary" size="xl">
            超大号按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} size="xl" />
        </div>
        <div style={{ marginBottom: 24 }}>
          <Button type="primary" shape="round" size="sm">
            小号按钮
          </Button>
          <Button type="primary" shape="round" icon={<PlusOutlined />} size="sm" />
          <Button type="primary" shape="round">
            正常按钮
          </Button>
          <Button type="primary" shape="round" icon={<PlusOutlined />} />
          <Button type="primary" shape="round" size="lg">
            大号按钮
          </Button>
          <Button type="primary" shape="round" icon={<PlusOutlined />} size="lg" />
          <Button type="primary" shape="round" size="xl">
            超大号按钮
          </Button>
          <Button type="primary" shape="round" icon={<PlusOutlined />} size="xl" />
        </div>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import { PlusOutlined } from '@hi-ui/icons'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  const btnRef = React.useRef(null)
  React.useEffect(() => {
    console.log(btnRef)
  }, [])
  return (
    <>
      <h1>不同尺寸</h1>
      <div className="button-basic__wrap">
        <div style={{ marginBottom: 24 }}>
          <Button type="primary" size="sm">
            小号按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} size="sm" />
          <Button type="primary">正常按钮</Button>
          <Button type="primary" icon={<PlusOutlined />} />
          <Button type="primary" size="lg">
            大号按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} size="lg" />
          <Button type="primary" size="xl">
            超大号按钮
          </Button>
          <Button type="primary" icon={<PlusOutlined />} size="xl" />
        </div>
        <div style={{ marginBottom: 24 }}>
          <Button type="primary" appearance="line" size="sm">
            小号按钮
          </Button>
          <Button type="primary" appearance="line" icon={<PlusOutlined />} size="sm" />
          <Button type="primary" appearance="line">
            正常按钮
          </Button>
          <Button type="primary" appearance="line" icon={<PlusOutlined />} />
          <Button type="primary" appearance="line" size="lg">
            大号按钮
          </Button>
          <Button type="primary" appearance="line" icon={<PlusOutlined />} size="lg" />
          <Button type="primary" appearance="line" size="xl">
            超大号按钮
          </Button>
          <Button type="primary" appearance="line" icon={<PlusOutlined />} size="xl" />
        </div>
        <div>
          <Button type="primary" appearance="link" size="sm">
            小号按钮
          </Button>
          <Button type="primary" appearance="link" icon={<PlusOutlined />} size="sm" />
          <Button type="primary" appearance="link">
            正常按钮
          </Button>
          <Button type="primary" appearance="link" icon={<PlusOutlined />} />
          <Button type="primary" appearance="link" size="lg">
            大号按钮
          </Button>
          <Button type="primary" appearance="link" icon={<PlusOutlined />} size="lg" />
          <Button type="primary" appearance="link" size="xl">
            超大号按钮
          </Button>
          <Button type="primary" appearance="link" icon={<PlusOutlined />} size="xl" />
        </div>
      </div>
    </>
  )
}

```

## card 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Card from '@hi-ui/card'

/**
 * @title 基础用法
 * @desc 用卡片封装独立的信息实体，如模块、功能、项目、应用等，或还原实际生活中的卡片应用
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="card-basic__wrap">
        <Card title="标题">
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
        <br />
        <br />
        <Card title="标题" showHeaderDivider>
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
      </div>
    </>
  )
}

```

### extra.stories.tsx

```typescript
import React from 'react'
import Card from '@hi-ui/card'
import Button from '@hi-ui/button'

/**
 * @title 带操作用法
 * @desc 可对卡片进行编辑、删除等操作
 */
export const Extra = () => {
  return (
    <>
      <h1>Extra</h1>
      <div className="card-extra__wrap">
        <Card title="标题" extra={<Button appearance="link">链接</Button>}>
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
        <br />
        <br />
        <Card title="标题" showHeaderDivider extra={<Button appearance="link">链接</Button>}>
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
      </div>
    </>
  )
}

```

### hoverable.stories.tsx

```typescript
import React from 'react'
import Card from '@hi-ui/card'

/**
 * @title hover 效果
 */
export const Hoverable = () => {
  return (
    <>
      <h1>Hoverable</h1>
      <div className="card-hoverable__wrap">
        <Card hoverable>
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
      </div>
    </>
  )
}

```

### img.stories.tsx

```typescript
import React from 'react'
import Card from '@hi-ui/card'

/**
 * @title 带头图
 * @desc 卡片中加入图片，增强识别性，常用于描述应用、项目等
 */
export const Img = () => {
  const [list] = React.useState(() => {
    return new Array(6).fill({
      image: 'http://i1.mifile.cn/f/i/hiui/docs/card/pic_9.png',
      title: '此处展示商品名称',
      content: '此处展示商品相关描述信息',
    })
  })
  return (
    <>
      <h1>Img</h1>
      <div className="card-img__wrap" style={{ display: 'flex', flexWrap: 'wrap', gap: 16 }}>
        {list.map((item, index) => {
          return (
            <Card
              key={index}
              style={{
                width: 256,
                // height: 398,
              }}
              title={item.title}
              coverUrl={item.image}
            >
              <span style={{ fontSize: 12, color: '#5F6A7A' }}>{item.content}</span>
            </Card>
          )
        })}
      </div>
    </>
  )
}

```

### loading.stories.tsx

```typescript
import Button from '@hi-ui/button'
import React from 'react'
import Card from '@hi-ui/card'

/**
 * @title 加载中状态
 */
export const Loading = () => {
  return (
    <>
      <h1>Loading</h1>
      <div className="card-loading__wrap">
        <Card title="标题" loading extra={<Button appearance="link">链接</Button>}>
          基础卡片
        </Card>
      </div>
    </>
  )
}

```

### no-border.stories.tsx

```typescript
import React from 'react'
import Card from '@hi-ui/card'

/**
 * @title 无边框
 */
export const NoBordered = () => {
  return (
    <>
      <h1>无边框</h1>
      <div
        className="card-no-header__wrap"
        style={{ padding: 32, backgroundColor: 'rgb(243, 244, 247)' }}
      >
        <Card bordered={false} title="我是标题">
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
      </div>
    </>
  )
}

```

### no-header.stories.tsx

```typescript
import React from 'react'
import Card from '@hi-ui/card'

/**
 * @title 无标题卡片
 */
export const NoHeader = () => {
  return (
    <>
      <h1>NoHeader</h1>
      <div className="card-no-header__wrap">
        <Card>
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import Button from '@hi-ui/button'
import React from 'react'
import Card from '@hi-ui/card'

/**
 * @title 不同尺寸
 * @desc 为卡片定义了 2 种尺寸，根据页面的实际空间选用紧凑程度
 */
export const Size = () => {
  return (
    <>
      <h1>Size</h1>
      <div className="card-size__wrap">
        <h2>常规</h2>
        <Card title="标题" size="md" extra={<Button appearance="link">链接</Button>}>
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
        <br />
        <h2>紧凑</h2>
        <Card title="标题" size="sm" extra={<Button appearance="link">链接</Button>}>
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
      </div>
    </>
  )
}

```

### subtitle.stories.tsx

```typescript
import Button from '@hi-ui/button'
import React from 'react'
import Card from '@hi-ui/card'

/**
 * @title 带副标题
 */
export const Subtitle = () => {
  return (
    <>
      <h1>Subtitle</h1>
      <div className="card-subtitle__wrap">
        <Card
          title="标题"
          extra={<Button appearance="link">链接</Button>}
          subtitle="这是一句简要的卡片副标题"
        >
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
        <br />
        <br />
        <Card
          title="标题"
          showHeaderDivider
          extra={<Button appearance="link">链接</Button>}
          subtitle="这是一句简要的卡片副标题"
        >
          <div
            style={{
              height: 174,
              backgroundColor: '#F5F7FA',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',
            }}
          >
            此处展示卡片内容
          </div>
        </Card>
      </div>
    </>
  )
}

```

## carousel 组件

### arrow-size.stories.tsx

```typescript
import React from 'react'
import Carousel from '@hi-ui/carousel'

/**
 * @title 不同箭头尺寸
 */
export const ArrowSize = () => {
  const generateContent = () => {
    return [
      <div
        key={'1'}
        style={{
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'center',
          width: '100%',
          height: '100%',
          position: 'relative',
        }}
      >
        <img
          src={
            'https://images.unsplash.com/photo-1451772741724-d20990422508?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80'
          }
          alt={'1'}
          onClick={() => console.error('1')}
        />
        <div
          style={{
            position: 'absolute',
            left: '50%',
            top: '50%',
            transform: 'translateX(-50%) translateY(-50%)',
            color: '#fff',
            fontSize: '36px',
            textShadow: '2px 2px 8px #fff',
          }}
        >
          Christmas
        </div>
      </div>,
      <img
        key={'2'}
        src={
          'https://images.unsplash.com/photo-1595923941716-39a9c58a9661?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80'
        }
        alt={'2'}
        onClick={() => console.error('2')}
      />,
      <img
        key={'3'}
        src={
          'https://images.unsplash.com/photo-1491466424936-e304919aada7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80'
        }
        alt={'3'}
        onClick={() => console.error('3')}
      />,
      <img
        key={'4'}
        src={
          'https://images.unsplash.com/photo-1640280056011-e1c0fda0fef5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=764&q=80'
        }
        alt={'4'}
        onClick={() => console.error('4')}
      />,
    ]
  }

  return (
    <>
      <h1>arrow size</h1>
      <h2>lg(large)</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel arrowSize={'lg'}>{generateContent()}</Carousel>
      </div>
      <h2>md(middle)</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel arrowSize={'md'}>{generateContent()}</Carousel>
      </div>
      <h2>sm(small)</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel arrowSize={'sm'}>{generateContent()}</Carousel>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Carousel from '@hi-ui/carousel'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const generateContent = () => {
    return [
      <div
        key={'1'}
        style={{
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'center',
          width: '100%',
          height: '100%',
          position: 'relative',
        }}
      >
        <img
          src={
            'https://images.unsplash.com/photo-1451772741724-d20990422508?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80'
          }
          alt={'1'}
          onClick={() => console.error('1')}
        />
        <div
          style={{
            position: 'absolute',
            left: '50%',
            top: '50%',
            transform: 'translateX(-50%) translateY(-50%)',
            color: '#fff',
            fontSize: '36px',
            textShadow: '2px 2px 8px #fff',
          }}
        >
          Christmas
        </div>
      </div>,
      <img
        key={'2'}
        src={
          'https://images.unsplash.com/photo-1595923941716-39a9c58a9661?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80'
        }
        alt={'2'}
        onClick={() => console.error('2')}
      />,
      <img
        key={'3'}
        src={
          'https://images.unsplash.com/photo-1491466424936-e304919aada7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80'
        }
        alt={'3'}
        onClick={() => console.error('3')}
      />,
      <img
        key={'4'}
        src={
          'https://images.unsplash.com/photo-1640280056011-e1c0fda0fef5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=764&q=80'
        }
        alt={'4'}
        onClick={() => console.error('4')}
      />,
    ]
  }

  return (
    <>
      <h1>Basic</h1>
      <div className="carousel-basic__wrap" style={{ minWidth: '660px', height: '320px' }}>
        <Carousel>{generateContent()}</Carousel>
      </div>
    </>
  )
}

```

### config.stories.tsx

```typescript
import React from 'react'
import Carousel from '@hi-ui/carousel'

/**
 * @title 显隐配置
 */
export const Config = () => {
  const generateContent = () => {
    return [
      <div
        key={'1'}
        style={{
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'center',
          width: '100%',
          height: '100%',
          position: 'relative',
        }}
      >
        <img
          src={
            'https://images.unsplash.com/photo-1451772741724-d20990422508?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80'
          }
          alt={'1'}
          onClick={() => console.error('1')}
        />
        <div
          style={{
            position: 'absolute',
            left: '50%',
            top: '50%',
            transform: 'translateX(-50%) translateY(-50%)',
            color: '#fff',
            fontSize: '36px',
            textShadow: '2px 2px 8px #fff',
          }}
        >
          Christmas
        </div>
      </div>,
      <img
        key={'2'}
        src={
          'https://images.unsplash.com/photo-1595923941716-39a9c58a9661?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80'
        }
        alt={'2'}
        onClick={() => console.error('2')}
      />,
      <img
        key={'3'}
        src={
          'https://images.unsplash.com/photo-1491466424936-e304919aada7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80'
        }
        alt={'3'}
        onClick={() => console.error('3')}
      />,
      <img
        key={'4'}
        src={
          'https://images.unsplash.com/photo-1640280056011-e1c0fda0fef5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=764&q=80'
        }
        alt={'4'}
        onClick={() => console.error('4')}
      />,
    ]
  }

  return (
    <>
      <h1>config</h1>
      <h2>showPages = true</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel showPages>{generateContent()}</Carousel>
      </div>
      <h2>showDot = false</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel showDots={false}>{generateContent()}</Carousel>
      </div>
      <h2>showArrows = false</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel showArrows={false}>{generateContent()}</Carousel>
      </div>
    </>
  )
}

```

### dot-position.stories.tsx

```typescript
import React from 'react'
import Carousel from '@hi-ui/carousel'

/**
 * @title 指示器位置
 */
export const dotPlacement = () => {
  const generateContent = () => {
    return [
      <div
        key={'1'}
        style={{
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'center',
          width: '100%',
          height: '100%',
          position: 'relative',
        }}
      >
        <img
          src={
            'https://images.unsplash.com/photo-1451772741724-d20990422508?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80'
          }
          alt={'1'}
          onClick={() => console.error('1')}
        />
        <div
          style={{
            position: 'absolute',
            left: '50%',
            top: '50%',
            transform: 'translateX(-50%) translateY(-50%)',
            color: '#fff',
            fontSize: '36px',
            textShadow: '2px 2px 8px #fff',
          }}
        >
          Christmas
        </div>
      </div>,
      <img
        key={'2'}
        src={
          'https://images.unsplash.com/photo-1595923941716-39a9c58a9661?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80'
        }
        alt={'2'}
        onClick={() => console.error('2')}
      />,
      <img
        key={'3'}
        src={
          'https://images.unsplash.com/photo-1491466424936-e304919aada7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80'
        }
        alt={'3'}
        onClick={() => console.error('3')}
      />,
      <img
        key={'4'}
        src={
          'https://images.unsplash.com/photo-1640280056011-e1c0fda0fef5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=764&q=80'
        }
        alt={'4'}
        onClick={() => console.error('4')}
      />,
    ]
  }

  return (
    <>
      <h1>dot position</h1>
      <h2>bottom(default)</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel>{generateContent()}</Carousel>
      </div>
      <h2>left</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel dotPlacement={'left'}>{generateContent()}</Carousel>
      </div>
      <h2>top</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel dotPlacement={'top'}>{generateContent()}</Carousel>
      </div>
      <h2>right</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel dotPlacement={'right'}>{generateContent()}</Carousel>
      </div>
      <h2>outer</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel dotPlacement={'outer'}>{generateContent()}</Carousel>
      </div>
    </>
  )
}

```

### dot-type.stories.tsx

```typescript
import React from 'react'
import Carousel from '@hi-ui/carousel'

/**
 * @title 指示器类型
 */
export const DotType = () => {
  const generateContent = () => {
    return [
      <div
        key={'1'}
        style={{
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'center',
          width: '100%',
          height: '100%',
          position: 'relative',
        }}
      >
        <img
          src={
            'https://images.unsplash.com/photo-1451772741724-d20990422508?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80'
          }
          alt={'1'}
          onClick={() => console.error('1')}
        />
        <div
          style={{
            position: 'absolute',
            left: '50%',
            top: '50%',
            transform: 'translateX(-50%) translateY(-50%)',
            color: '#fff',
            fontSize: '36px',
            textShadow: '2px 2px 8px #fff',
          }}
        >
          Christmas
        </div>
      </div>,
      <img
        key={'2'}
        src={
          'https://images.unsplash.com/photo-1595923941716-39a9c58a9661?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80'
        }
        alt={'2'}
        onClick={() => console.error('2')}
      />,
      <img
        key={'3'}
        src={
          'https://images.unsplash.com/photo-1491466424936-e304919aada7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80'
        }
        alt={'3'}
        onClick={() => console.error('3')}
      />,
      <img
        key={'4'}
        src={
          'https://images.unsplash.com/photo-1640280056011-e1c0fda0fef5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=764&q=80'
        }
        alt={'4'}
        onClick={() => console.error('4')}
      />,
    ]
  }

  return (
    <>
      <h1>dot type</h1>
      <h2>slider(default)</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel>{generateContent()}</Carousel>
      </div>
      <h2>line</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel dotType={'line'}>{generateContent()}</Carousel>
      </div>
      <h2>dot</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel dotType={'dot'}>{generateContent()}</Carousel>
      </div>
    </>
  )
}

```

### duration.stories.tsx

```typescript
import React from 'react'
import Carousel from '@hi-ui/carousel'

/**
 * @title 自动切换间隔
 */
export const Duration = () => {
  const generateContent = () => {
    return [
      <div
        key={'1'}
        style={{
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'center',
          width: '100%',
          height: '100%',
          position: 'relative',
        }}
      >
        <img
          src={
            'https://images.unsplash.com/photo-1451772741724-d20990422508?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80'
          }
          alt={'1'}
          onClick={() => console.error('1')}
        />
        <div
          style={{
            position: 'absolute',
            left: '50%',
            top: '50%',
            transform: 'translateX(-50%) translateY(-50%)',
            color: '#fff',
            fontSize: '36px',
            textShadow: '2px 2px 8px #fff',
          }}
        >
          Christmas
        </div>
      </div>,
      <img
        key={'2'}
        src={
          'https://images.unsplash.com/photo-1595923941716-39a9c58a9661?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80'
        }
        alt={'2'}
        onClick={() => console.error('2')}
      />,
      <img
        key={'3'}
        src={
          'https://images.unsplash.com/photo-1491466424936-e304919aada7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80'
        }
        alt={'3'}
        onClick={() => console.error('3')}
      />,
      <img
        key={'4'}
        src={
          'https://images.unsplash.com/photo-1640280056011-e1c0fda0fef5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=764&q=80'
        }
        alt={'4'}
        onClick={() => console.error('4')}
      />,
    ]
  }

  return (
    <>
      <h1>Duration</h1>
      <h2>0ms(default)(disabled)</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel>{generateContent()}</Carousel>
      </div>
      <h2>5000ms</h2>
      <div style={{ minWidth: '660px', height: '320px' }}>
        <Carousel duration={5000}>{generateContent()}</Carousel>
      </div>
    </>
  )
}

```

### resize.stories.tsx

```typescript
import React from 'react'
import Carousel from '@hi-ui/carousel'

/**
 * @title 自定义宽高
 */
export const Resize = () => {
  const generateContent = () => {
    return [
      <div
        key={'1'}
        style={{
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'center',
          width: '100%',
          height: '100%',
          position: 'relative',
        }}
      >
        <img
          src={
            'https://images.unsplash.com/photo-1451772741724-d20990422508?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80'
          }
          alt={'1'}
          onClick={() => console.error('1')}
        />
        <div
          style={{
            position: 'absolute',
            left: '50%',
            top: '50%',
            transform: 'translateX(-50%) translateY(-50%)',
            color: '#fff',
            fontSize: '36px',
            textShadow: '2px 2px 8px #fff',
          }}
        >
          Christmas
        </div>
      </div>,
      <img
        key={'2'}
        src={
          'https://images.unsplash.com/photo-1595923941716-39a9c58a9661?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80'
        }
        alt={'2'}
        onClick={() => console.error('2')}
      />,
      <img
        key={'3'}
        src={
          'https://images.unsplash.com/photo-1491466424936-e304919aada7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80'
        }
        alt={'3'}
        onClick={() => console.error('3')}
      />,
      <img
        key={'4'}
        src={
          'https://images.unsplash.com/photo-1640280056011-e1c0fda0fef5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=764&q=80'
        }
        alt={'4'}
        onClick={() => console.error('4')}
      />,
    ]
  }

  return (
    <>
      <h1>Resize</h1>
      <h2>760 X 320</h2>
      <div className="carousel-basic__wrap" style={{ minWidth: '660px', height: '320px' }}>
        <Carousel>{generateContent()}</Carousel>
      </div>
      <h2>760 X 469</h2>
      <div className="carousel-basic__wrap" style={{ minWidth: '660px', height: '469px' }}>
        <Carousel>{generateContent()}</Carousel>
      </div>
      <h2>760 X 200</h2>
      <div className="carousel-basic__wrap" style={{ minWidth: '660px', height: '200px' }}>
        <Carousel>{generateContent()}</Carousel>
      </div>
    </>
  )
}

```

### responsive.stories.tsx

```typescript
import React from 'react'
import Carousel from '@hi-ui/carousel'

/**
 * @title 响应式
 */
export const Responsive = () => {
  const generateContent = () => {
    return [
      <div
        key={'1'}
        style={{
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'center',
          width: '100%',
          height: '100%',
          position: 'relative',
        }}
      >
        <img
          src={
            'https://images.unsplash.com/photo-1451772741724-d20990422508?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80'
          }
          alt={'1'}
          onClick={() => console.error('1')}
        />
        <div
          style={{
            position: 'absolute',
            left: '50%',
            top: '50%',
            transform: 'translateX(-50%) translateY(-50%)',
            color: '#fff',
            fontSize: '36px',
            textShadow: '2px 2px 8px #fff',
          }}
        >
          Christmas
        </div>
      </div>,
      <img
        key={'2'}
        src={
          'https://images.unsplash.com/photo-1595923941716-39a9c58a9661?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80'
        }
        alt={'2'}
        onClick={() => console.error('2')}
      />,
      <img
        key={'3'}
        src={
          'https://images.unsplash.com/photo-1491466424936-e304919aada7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80'
        }
        alt={'3'}
        onClick={() => console.error('3')}
      />,
      <img
        key={'4'}
        src={
          'https://images.unsplash.com/photo-1640280056011-e1c0fda0fef5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=764&q=80'
        }
        alt={'4'}
        onClick={() => console.error('4')}
      />,
    ]
  }

  return (
    <>
      <h1>Responsive</h1>
      <div className="carousel-Responsive__wrap" style={{ display: 'flex' }}>
        <div style={{ flex: 1, overflow: 'hidden' }}>
          <Carousel>{generateContent()}</Carousel>
        </div>
        <div
          style={{
            width: '100px',
            flexBasis: '100px',
            height: '100%',
            flexShrink: 0,
            backgroundColor: '#237ffa',
          }}
        >
          模拟侧边栏定宽
        </div>
      </div>
    </>
  )
}

```

## cascader 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 基础用法
 * @desc 展示从多个收起的备选项中选出的一个选项
 */
export const Basic = () => {
  const [data] = React.useState([
    {
      id: '手机',
      title: '手机t',
      children: [
        {
          id: '小米',
          title: '小米t',
          children: [
            {
              id: '小米3',
              title: '小米3t',
            },
            {
              id: '小米4',
              title: '小米4t',
            },
          ],
        },
        {
          id: '红米',
          title: '红米t',
          children: [
            {
              id: '红米3',
              title: '红米3t',
            },
            {
              id: '红米4',
              title: '红米4t',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视t',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4At',
        },
        {
          id: '小米电视4C',
          title: '小米电视4Ct',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Basic</h1>
      <div className="cascader-basic__wrap">
        <Cascader
          style={{ width: 240 }}
          clearable
          placeholder="请选择品类"
          defaultValue={['手机', '红米', '红米4']}
          data={data}
          onChange={(...args) => {
            console.log('onChange', ...args)
          }}
        ></Cascader>
      </div>
    </>
  )
}

```

### custom-render.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'
import Input from '@hi-ui/input'

/**
 * @title 自定义触发器
 */
export const CustomRender = () => {
  const [data] = React.useState([
    {
      id: '手机',
      title: '手机t',
      children: [
        {
          id: '小米',
          title: '小米t',
          children: [
            {
              id: '小米3',
              title: '小米3t',
            },
            {
              id: '小米4',
              title: '小米4t',
            },
          ],
        },
        {
          id: '红米',
          title: '红米t',
          children: [
            {
              id: '红米3',
              title: '红米3t',
            },
            {
              id: '红米4',
              title: '红米4t',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视t',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4At',
        },
        {
          id: '小米电视4C',
          title: '小米电视4Ct',
        },
      ],
    },
  ])

  return (
    <>
      <h1>CustomRender</h1>
      <div className="cascader-custom-render__wrap">
        <Cascader
          style={{ width: 240 }}
          clearable
          placeholder="请选择品类"
          data={data}
          customRender={(data) => {
            return <Input value={!data ? '' : data.title + ''} placeholder="请选择" />
          }}
        ></Cascader>
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 禁用状态
 * @desc 暂不可操作的状态
 */
export const Disabled = () => {
  const [data] = React.useState([
    {
      id: '0',
      title: '0',
      children: [
        {
          id: '0-0',
          title: '0-0',
          children: [
            {
              id: '0-0-0',
              title: '0-0-0',
            },
            {
              id: '0-0-1',
              title: '0-0-1',
            },
            {
              id: '0-0-2',
              title: '0-0-2',
            },
          ],
        },
        {
          id: '0-1',
          title: '0-1',
          children: [
            {
              id: '0-1-0',
              title: '0-1-0',
            },
            {
              id: '0-1-1',
              title: '0-1-1',
            },
          ],
        },
        {
          id: '0-2',
          title: '0-2',
          disabled: true,
          children: [
            {
              id: '0-2-0',
              title: '0-2-0',
            },
            {
              id: '0-2-1',
              title: '0-2-1',
            },
          ],
        },
        {
          id: '0-3',
          title: '0-3',
          children: [
            {
              id: '0-3-0',
              title: '0-3-0',
            },
            {
              id: '0-3-1',
              title: '0-3-1',
            },
            {
              id: '0-3-2',
              title: '0-3-2',
            },
          ],
        },
        {
          id: '0-4',
          title: '0-4',
          children: [
            {
              id: '0-4-0',
              title: '0-4-0',
            },
            {
              id: '0-4-1',
              title: '0-4-1',
            },
          ],
        },
        {
          id: '0-5',
          title: '0-5',
          children: [
            {
              id: '0-5-0',
              title: '0-5-0',
            },
            {
              id: '0-5-1',
              title: '0-5-1',
            },
          ],
        },
      ],
    },
    {
      id: '1',
      title: '1',
      children: [
        {
          id: '1-0',
          title: '1-0',
          children: [
            {
              id: '1-0-0',
              title: '1-0-0',
            },
            {
              id: '1-0-1',
              title: '1-0-1',
              children: [
                {
                  id: '1-0-1-0',
                  title: '1-0-1-0',
                },
                {
                  id: '1-0-1-1',
                  title: '1-0-1-1',
                },
              ],
            },
            {
              id: '1-0-2',
              title: '1-0-2',
            },
          ],
        },
        {
          id: '1-1',
          title: '1-1',
        },
        {
          id: '1-2',
          title: '1-2',
        },
        {
          id: '1-3',
          title: '1-3',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Disabled</h1>
      <div className="cascader-disabled__wrap">
        <h2>整体禁用</h2>
        <Cascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          disabled
          searchPlaceholder="请输入搜索内容"
          data={data}
        />

        <h2>禁用某个选项</h2>
        <Cascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          searchPlaceholder="请输入搜索内容"
          data={data}
        />
      </div>
    </>
  )
}

```

### display-render.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 自定义回显展示
 */
export const DisplayRender = () => {
  const [data] = React.useState([
    {
      id: '手机',
      title: '手机t',
      children: [
        {
          id: '小米',
          title: '小米t',
          children: [
            {
              id: '小米3',
              title: '小米3t',
            },
            {
              id: '小米4',
              title: '小米4t',
            },
          ],
        },
        {
          id: '红米',
          title: '红米t',
          children: [
            {
              id: '红米3',
              title: '红米3t',
            },
            {
              id: '红米4',
              title: '红米4t',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视t',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4At',
        },
        {
          id: '小米电视4C',
          title: '小米电视4Ct',
        },
      ],
    },
  ])

  return (
    <>
      <h1>DisplayRender</h1>
      <div className="cascader-display-render__wrap">
        <Cascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          defaultValue={['手机', '红米', '红米4']}
          data={data}
          displayRender={(option) => {
            const titleArr = []
            while (option.parent) {
              titleArr.push(option.title)
              option = option.parent as any
            }
            return titleArr.reverse().join(' | ')
          }}
        ></Cascader>
      </div>
    </>
  )
}

```

### dropdown-column-render.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 自定义下拉菜单内容
 */
export const DropdownColumnRender = () => {
  const [data] = React.useState([
    {
      id: '手机',
      title: '手机t',
      children: [
        {
          id: '小米',
          title: '小米t',
          children: [
            {
              id: '小米3',
              title: '小米3t',
            },
            {
              id: '小米4',
              title: '小米4t',
            },
          ],
        },
        {
          id: '红米',
          title: '红米t',
          children: [
            {
              id: '红米3',
              title: '红米3t',
            },
            {
              id: '红米4',
              title: '红米4t',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视t',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4At',
        },
        {
          id: '小米电视4C',
          title: '小米电视4Ct',
        },
      ],
    },
    {
      id: '1',
      title: '小米1',
    },
    {
      id: '2',
      title: '小米2',
    },
    {
      id: '3',
      title: '小米3',
    },
    {
      id: '4',
      title: '小米4',
    },
    {
      id: '5',
      title: '小米5',
    },
    {
      id: '6',
      title: '小米6',
    },
    {
      id: '7',
      title: '小米7',
    },
  ])

  return (
    <>
      <h1>DropdownColumnRender</h1>
      <div className="cascader-dropdown-column-render__wrap">
        <Cascader
          style={{ width: 240 }}
          clearable
          placeholder="请选择品类"
          defaultValue={['手机', '红米', '红米4']}
          data={data}
          onChange={(...args) => {
            console.log('onChange', ...args)
          }}
          // 如果有样式不满足需求，可以给弹出层设置独有的 className 来进行样式覆写
          overlay={{ className: 'my-overlay' }}
          dropdownColumnRender={(menu, level) => {
            return level < 5 ? (
              <div
                className="custom-menu"
                style={{ overflow: 'hidden', borderRight: '1px solid #ebedf0' }}
              >
                <header
                  style={{
                    lineHeight: '20px',
                    padding: '0px 8px 8px',
                    borderBottom: '1px solid #ebedf0',
                  }}
                >
                  header
                </header>
                {React.cloneElement(menu, { style: { height: 186 } })}
                <footer
                  style={{
                    lineHeight: '20px',
                    padding: '8px 8px 0',
                    borderTop: '1px solid #ebedf0',
                  }}
                >
                  footer(level {level})
                </footer>
              </div>
            ) : (
              menu
            )
          }}
        ></Cascader>
      </div>
    </>
  )
}

```

### dynamic.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'
import Alert from '@hi-ui/alert'

/**
 * @title 异步加载数据
 */
export const Dynamic = () => {
  const [treeData] = React.useState([
    {
      id: 1,
      title: '小米',
      children: [
        {
          id: 2,
          title: '技术',
          children: [
            { id: 3, title: '后端' },
            { id: 4, title: '运维' },
            { id: 5, title: '前端' },
          ],
        },
        { id: 6, title: '产品' },
      ],
    },
    {
      id: 11,
      title: '小米',
      children: [
        { id: 22, title: '技术' },
        { id: 66, title: '产品' },
      ],
    },
  ])

  // 加载节点
  const loadChildren = async (node) => {
    return fetch(`https://my-json-server.typicode.com/hiui-group/db/conditiondata?id=${node.id}`)
      .then((res) => res.json())
      .then((data) => {
        if (data[0]) {
          data[0].id = Math.random()
        }

        // setTreeData((prev) => {
        //   const nextData = cloneTree(prev)
        //   const loadNode = findNode(node.id, nextData)
        //   loadNode.children = data
        //   console.log(loadNode, nextData)
        //   return nextData
        // })

        return data
      })
  }

  return (
    <>
      <h1>Dynamic for Cascader</h1>
      <div className="cascader-dynamic__wrap">
        <Alert
          type="danger"
          closeable={false}
          showIcon={false}
          title={
            '注意：对于异步加载子节点，可以配合 `node.isLeaf: true` 来表明是否为叶子结点。以此来告诉组件是否有下一级子面板'
          }
        ></Alert>
        <br />
        <Cascader
          style={{ width: 240 }}
          data={treeData}
          onLoadChildren={loadChildren}
          onChange={console.log}
        ></Cascader>
      </div>
    </>
  )
}

```

### field-names.stories.tsx

```typescript
import React from 'react'
import { Cascader } from '@hi-ui/cascader'

/**
 * @title 字段别名
 * @desc 数据中的字段名非title，id或disabled时使用
 */
export const FieldNames = () => {
  const [data] = React.useState([
    {
      value: '0',
      label: '0',
      kids: [
        {
          value: '0-0',
          label: '0-0',
          kids: [
            {
              value: '0-0-0',
              label: '0-0-0',
            },
            {
              value: '0-0-1',
              label: '0-0-1',
            },
            {
              value: '0-0-2',
              label: '0-0-2',
            },
          ],
        },
        {
          value: '0-1',
          label: '0-1',
          kids: [
            {
              value: '0-1-0',
              label: '0-1-0',
            },
            {
              value: '0-1-1',
              label: '0-1-1',
            },
          ],
        },
        {
          value: '0-2',
          label: '0-2',
          kids: [
            {
              value: '0-2-0',
              label: '0-2-0',
            },
            {
              value: '0-2-1',
              label: '0-2-1',
            },
          ],
        },
      ],
    },
    {
      value: '1',
      label: '1',
      kids: [
        {
          value: '1-0',
          label: '1-0',
        },
        {
          value: '1-1',
          label: '1-1',
        },
      ],
    },
    {
      value: '2',
      label: '2',
      kids: [
        {
          value: '2-0',
          label: '2-0',
        },
        {
          value: '2-1',
          label: '2-1',
        },
      ],
    },
  ])

  return (
    <>
      <h1>FieldNames</h1>
      <div className="cascader-field-names__wrap">
        <Cascader
          style={{ width: 240 }}
          fieldNames={{
            id: 'value',
            title: 'label',
            children: 'kids',
          }}
          defaultValue={['0', '0-0', '0-0-1']}
          data={data}
        />
      </div>
    </>
  )
}

```

### filter-options.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'
import { match } from 'pinyin-pro'

/**
 * @title 自定义搜索筛选规则
 * @desc 通过 filterOption 可自定义搜索条件的算法
 */
export const FilterOptions = () => {
  const [data] = React.useState([
    {
      id: '手机',
      title: '手机t',
      children: [
        {
          id: '小米',
          title: '小米t',
          children: [
            {
              id: '小米3',
              title: '小米3t',
            },
            {
              id: '小米4',
              title: '小米4t',
            },
          ],
        },
        {
          id: '红米',
          title: '红米t',
          children: [
            {
              id: '红米3',
              title: '红米3t',
            },
            {
              id: '红米4',
              title: '红米4t',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视t',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4At',
        },
        {
          id: '小米电视4C',
          title: '小米电视4Ct',
        },
      ],
    },
  ])

  // 注意 filterOption 是影响搜索渲染的，是完全受控的，useCallback 包裹可以减少无效的重渲染，提升性能
  const filterOptionMemo = React.useCallback((keyword: string, item: any) => {
    if (item.children) return false
    const _match = (node: any) =>
      typeof node.title === 'string' && !!match(node.title as string, keyword)

    const matchUp = (node: any) => {
      let found = _match(node)
      let { parent } = node

      if (parent && !found) {
        const ancestors = [] as any[]
        while (parent) {
          ancestors.push(parent)
          parent = parent.parent
        }

        found = ancestors.some((item: any) => _match(item))
        console.log(ancestors, found)
      }

      return found
    }

    const matchDown = (node: any) => {
      let found = _match(node)
      const { children } = node

      if (children && !found) {
        found = children.some((item: any) => matchDown(item))
      }

      return found
    }

    const result = matchUp(item) || matchDown(item)

    return result
  }, [])

  return (
    <>
      <h1>FilterOptions</h1>
      <div className="select-filter-options__wrap">
        <Cascader
          style={{ width: 240 }}
          clearable={false}
          data={data}
          searchPlaceholder="拼音检索"
          filterOption={filterOptionMemo}
        />
      </div>
    </>
  )
}

```

### footer.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 吸底内容条
 */
export const Footer = () => {
  const [data] = React.useState([
    {
      id: '手机',
      title: '手机t',
      children: [
        {
          id: '小米',
          title: '小米t',
          children: [
            {
              id: '小米3',
              title: '小米3t',
            },
            {
              id: '小米4',
              title: '小米4t',
            },
          ],
        },
        {
          id: '红米',
          title: '红米t',
          children: [
            {
              id: '红米3',
              title: '红米3t',
            },
            {
              id: '红米4',
              title: '红米4t',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视t',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4At',
        },
        {
          id: '小米电视4C',
          title: '小米电视4Ct',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Footer</h1>
      <div className="cascader-footer__wrap">
        <Cascader
          style={{ width: 240 }}
          clearable
          placeholder="请选择品类"
          defaultValue={['手机', '红米', '红米4']}
          data={data}
          onChange={(...args) => {
            console.log('onChange', ...args)
          }}
          renderExtraFooter={() => <div>custom footer</div>}
        ></Cascader>
      </div>
    </>
  )
}

```

### hover-expand.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title hover 展开次级菜单
 */
export const HoverExpand = () => {
  const [data] = React.useState([
    {
      id: '手机',
      title: '手机',
      children: [
        {
          id: '小米',
          title: '小米',
          children: [
            {
              id: '小米3',
              title: '小米3',
            },
            {
              id: '小米4',
              title: '小米4',
            },
          ],
        },
        {
          id: '红米',
          title: '红米',
          children: [
            {
              id: '红米3',
              title: '红米3',
            },
            {
              id: '红米4',
              title: '红米4',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4A',
        },
        {
          id: '小米电视4C',
          title: '小米电视4C',
        },
      ],
    },
  ])

  return (
    <>
      <h1>HoverExpand</h1>
      <div className="cascader-hover-expand__wrap">
        <Cascader
          style={{ width: 240 }}
          searchable
          clearable
          expandTrigger="hover"
          placeholder="请选择品类"
          defaultValue={['手机', '小米', '红米']}
          data={data}
        ></Cascader>
      </div>
    </>
  )
}

```

### search.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 带搜索
 * @desc 选项数量较大，不熟悉数据的结构关系情况下，用搜索关键词的方式快速定位
 */
export const Search = () => {
  const [data] = React.useState([
    {
      id: 'up-1',
      title: 'up',
      children: [
        {
          id: 'up-1-0',
          title: '小米',
          children: [
            {
              id: 'up-1-0-0',
              title: 'leaf',
            },
          ],
        },
        {
          id: 'up-1-1',
          title: 'up-1-1',
        },
      ],
    },
    {
      id: '0',
      title: 'up-0',
      children: [
        {
          id: '0-0',
          title: '0-0',
          children: [
            {
              id: '0-0-0',
              title: '0-0-0',
            },
            {
              id: '0-0-1',
              title: '0-0-1',
            },
            {
              id: '0-0-2',
              title: '0-0-2',
            },
          ],
        },
        {
          id: '0-1',
          title: '0-1',
          children: [
            {
              id: '0-1-0',
              title: '0-1-0',
            },
            {
              id: '0-1-1',
              title: '0-1-1',
            },
          ],
        },
        {
          id: '0-2',
          title: '0-2',
          children: [
            {
              id: '0-2-0',
              title: '0-2-0',
            },
            {
              id: '0-2-1',
              title: '0-2-1',
            },
          ],
        },
        {
          id: '0-3',
          title: '0-3',
          children: [
            {
              id: '0-3-0',
              title: '0-3-0',
            },
            {
              id: '0-3-1',
              title: '0-3-1',
            },
            {
              id: '0-3-2',
              title: '0-3-2',
            },
          ],
        },
        {
          id: '0-4',
          title: '0-4',
          children: [
            {
              id: '0-4-0',
              title: '0-4-0',
            },
            {
              id: '0-4-1',
              title: '0-4-1',
            },
          ],
        },
        {
          id: '0-5',
          title: '0-5',
          children: [
            {
              id: '0-5-0',
              title: '0-5-0',
            },
            {
              id: '0-5-1',
              title: '0-5-1',
            },
          ],
        },
        {
          id: '0-6',
          title: '0-6',
          children: [
            {
              id: '0-6-0',
              title: '0-6-0',
            },
            {
              id: '0-6-1',
              title: '0-6-1',
            },
            {
              id: '0-6-2',
              title: '0-6-2',
            },
          ],
        },
        {
          id: '0-7',
          title: '0-7',
          children: [
            {
              id: '0-7-0',
              title: '0-7-0',
            },
            {
              id: '0-7-1',
              title: '0-7-1',
            },
          ],
        },
        {
          id: '0-8',
          title: '0-8',
          children: [
            {
              id: '0-8-0',
              title: '0-8-0',
            },
            {
              id: '0-8-1',
              title: '0-8-1',
            },
          ],
        },
      ],
    },
    {
      id: '1',
      title: '1',
      children: [
        {
          id: '1-0',
          title: '1-0',
        },
        {
          id: '1-1',
          title: '1-1',
        },
      ],
    },
    {
      id: '2',
      title: '2',
      children: [
        {
          id: '2-0',
          title: '2-0',
        },
        {
          id: '2-1',
          title: '2-1',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Search</h1>
      <div className="cascader-search__wrap">
        <h2>展示搜索结果：拍平模式（默认）</h2>
        <Cascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          searchPlaceholder="请输入搜索内容"
          data={data}
          searchable
          onChange={console.log}
        />

        <h2>展示搜索结果：级联模式</h2>
        <Cascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          searchPlaceholder="请输入搜索内容"
          data={data}
          searchable
          flattedSearchResult={false}
          onChange={console.log}
        />
      </div>
    </>
  )
}

```

### select-change.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 选中任意层级
 */
export const SelectChange = () => {
  const [data] = React.useState([
    {
      id: '0',
      title: '0',
      children: [
        {
          id: '0-0',
          title: '0-0',
          children: [
            {
              id: '0-0-0',
              title: '0-0-0',
            },
            {
              id: '0-0-1',
              title: '0-0-1',
            },
            {
              id: '0-0-2',
              title: '0-0-2',
            },
          ],
        },
        {
          id: '0-1',
          title: '0-1',
          children: [
            {
              id: '0-1-0',
              title: '0-1-0',
            },
            {
              id: '0-1-1',
              title: '0-1-1',
            },
          ],
        },
        {
          id: '0-2',
          title: '0-2',
          disabled: false,
          children: [
            {
              id: '0-2-0',
              title: '0-2-0',
            },
            {
              id: '0-2-1',
              title: '0-2-1',
            },
          ],
        },
        {
          id: '0-3',
          title: '0-3',
          children: [
            {
              id: '0-3-0',
              title: '0-3-0',
            },
            {
              id: '0-3-1',
              title: '0-3-1',
            },
            {
              id: '0-3-2',
              title: '0-3-2',
            },
          ],
        },
        {
          id: '0-4',
          title: '0-4',
          children: [
            {
              id: '0-4-0',
              title: '0-4-0',
            },
            {
              id: '0-4-1',
              title: '0-4-1',
            },
          ],
        },
        {
          id: '0-5',
          title: '0-5',
          children: [
            {
              id: '0-5-0',
              title: '0-5-0',
            },
            {
              id: '0-5-1',
              title: '0-5-1',
            },
          ],
        },
      ],
    },
    {
      id: '1',
      title: '1',
      children: [
        {
          id: '1-0',
          title: '1-0',
          disabledCheckbox: true,
        },
        {
          id: '1-1',
          title: '1-1',
        },
      ],
    },
  ])

  return (
    <>
      <h1>SelectChange</h1>
      <div className="cascader-select-change__wrap">
        <Cascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          changeOnSelect
          expandTrigger="hover"
          searchPlaceholder="请输入搜索内容"
          data={data}
          onChange={console.log}
        />
      </div>
    </>
  )
}

```

### select-close.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 选择后是否关闭弹窗
 * @desc 用于 changeOnSelect 模式下控制点击父节点时是否关闭弹窗
 */
export const SelectClose = () => {
  const [data] = React.useState([
    {
      id: '0',
      title: '0',
      children: [
        {
          id: '0-0',
          title: '0-0',
          children: [
            {
              id: '0-0-0',
              title: '0-0-0',
            },
            {
              id: '0-0-1',
              title: '0-0-1',
            },
            {
              id: '0-0-2',
              title: '0-0-2',
            },
          ],
        },
        {
          id: '0-1',
          title: '0-1',
          children: [
            {
              id: '0-1-0',
              title: '0-1-0',
            },
            {
              id: '0-1-1',
              title: '0-1-1',
            },
          ],
        },
        {
          id: '0-2',
          title: '0-2',
          disabled: false,
          children: [
            {
              id: '0-2-0',
              title: '0-2-0',
            },
            {
              id: '0-2-1',
              title: '0-2-1',
            },
          ],
        },
        {
          id: '0-3',
          title: '0-3',
          children: [
            {
              id: '0-3-0',
              title: '0-3-0',
            },
            {
              id: '0-3-1',
              title: '0-3-1',
            },
            {
              id: '0-3-2',
              title: '0-3-2',
            },
          ],
        },
        {
          id: '0-4',
          title: '0-4',
          children: [
            {
              id: '0-4-0',
              title: '0-4-0',
            },
            {
              id: '0-4-1',
              title: '0-4-1',
            },
          ],
        },
        {
          id: '0-5',
          title: '0-5',
          children: [
            {
              id: '0-5-0',
              title: '0-5-0',
            },
            {
              id: '0-5-1',
              title: '0-5-1',
            },
          ],
        },
      ],
    },
    {
      id: '1',
      title: '1',
      children: [
        {
          id: '1-0',
          title: '1-0',
          disabledCheckbox: true,
        },
        {
          id: '1-1',
          title: '1-1',
        },
      ],
    },
  ])

  return (
    <>
      <h1>SelectClose</h1>
      <div className="cascader-select-close__wrap">
        <Cascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          changeOnSelect
          closeOnSelect={false}
          // expandTrigger="hover"
          searchPlaceholder="请输入搜索内容"
          data={data}
          onChange={console.log}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  const [data] = React.useState([
    {
      id: '手机',
      title: '手机t',
      children: [
        {
          id: '小米',
          title: '小米t',
          children: [
            {
              id: '小米3',
              title: '小米3t',
            },
            {
              id: '小米4',
              title: '小米4t',
            },
          ],
        },
        {
          id: '红米',
          title: '红米t',
          children: [
            {
              id: '红米3',
              title: '红米3t',
            },
            {
              id: '红米4',
              title: '红米4t',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视t',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4At',
        },
        {
          id: '小米电视4C',
          title: '小米电视4Ct',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Size</h1>
      <div className="cascader-size__wrap">
        <h2>sm</h2>
        <Cascader
          style={{ width: 240 }}
          size="sm"
          clearable
          placeholder="请选择品类"
          defaultValue={['手机', '红米', '红米4']}
          data={data}
          onChange={(...args) => {
            console.log('onChange', ...args)
          }}
        ></Cascader>
        <h2>md</h2>
        <Cascader
          style={{ width: 240 }}
          size="md"
          clearable
          placeholder="请选择品类"
          defaultValue={['手机', '红米', '红米4']}
          data={data}
          onChange={(...args) => {
            console.log('onChange', ...args)
          }}
        ></Cascader>
        <h2>lg</h2>
        <Cascader
          style={{ width: 240 }}
          size="lg"
          clearable
          placeholder="请选择品类"
          defaultValue={['手机', '红米', '红米4']}
          data={data}
          onChange={(...args) => {
            console.log('onChange', ...args)
          }}
        ></Cascader>
      </div>
    </>
  )
}

```

### title-render.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 自定义选项展示
 */
export const TitleRender = () => {
  const [data] = React.useState([
    {
      id: '1',
      title: '手机t',
      children: [
        {
          id: '1-1',
          title: '小米t',
          children: [
            {
              id: '1-1-1',
              title: '小米3t',
            },
            {
              id: '1-1-2',
              title: '小米4t',
            },
          ],
        },
        {
          id: '1-2',
          title: '红米t',
          children: [
            {
              id: '1-2-1',
              title: '红米3t',
            },
            {
              id: '1-2-2',
              title: '红米4t',
            },
          ],
        },
      ],
    },
    {
      id: '2',
      title: '电视t',
      children: [
        {
          id: '2-1',
          title: '小米电视4At',
        },
        {
          id: '2-2',
          title: '小米电视4Ct',
        },
      ],
    },
  ])

  return (
    <>
      <h1>TitleRender</h1>
      <div className="cascader-basic__wrap">
        <Cascader
          style={{ width: 240 }}
          searchable={true}
          clearable
          placeholder="请选择品类"
          defaultValue={['手机', '红米', '红米4']}
          data={data}
          render={(item, keyword) => {
            console.log(item, keyword)
            if (keyword) {
              // 自定义搜索结果展示：可以自定义控制关键词高亮，夹带 icon 等场景
              return <span>{`${keyword}: ${item.title}`}</span>
            }
            return <span>{`${item.title}(${item.id})`}</span>
          }}
          onChange={(...args) => {
            console.log('onChange', ...args)
          }}
        ></Cascader>
      </div>
    </>
  )
}

```

### visible.stories.tsx

```typescript
import React from 'react'
import Cascader from '@hi-ui/cascader'

/**
 * @title 受控显隐
 * @desc 自定义控制下拉选项菜单显隐
 */
export const Visible = () => {
  const [visible, setVisible] = React.useState(true)
  const [data] = React.useState([
    {
      id: '手机',
      title: '手机t',
      children: [
        {
          id: '小米',
          title: '小米t',
          children: [
            {
              id: '小米3',
              title: '小米3t',
            },
            {
              id: '小米4',
              title: '小米4t',
            },
          ],
        },
        {
          id: '红米',
          title: '红米t',
          children: [
            {
              id: '红米3',
              title: '红米3t',
            },
            {
              id: '红米4',
              title: '红米4t',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视t',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4At',
        },
        {
          id: '小米电视4C',
          title: '小米电视4Ct',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Visible</h1>
      <div className="cascader-visible__wrap">
        <Cascader
          style={{ width: 240 }}
          visible={visible}
          onOpen={() => setVisible(true)}
          overlay={{ onOutsideClick: () => setVisible(false) }}
          clearable
          placeholder="请选择品类"
          defaultValue={['手机', '红米', '红米4']}
          data={data}
          onChange={(...args) => {
            console.log('onChange', ...args)
          }}
        />
      </div>
    </>
  )
}

```

## check-cascader 组件

### addon.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'
import { AppStoreOutlined, InfoCircleOutlined } from '@hi-ui/icons'
/**
 * @title 前后内置元素
 * @desc 将选择框与内置的其他元素组合使用
 */
export const Addon = () => {
  const [dataOnlyLeafCheckable] = React.useState(() => {
    const data = [
      {
        id: '手机',
        title: '手机t',
        children: [
          {
            id: '小米',
            title: '小米t',
            children: [
              {
                id: '小米3',
                title: '小米3t',
              },
              {
                id: '小米4',
                title: '小米4t',
              },
            ],
          },
          {
            id: '红米',
            title: '红米t',
            children: [
              {
                id: '红米3',
                title: '红米3t',
              },
              {
                id: '红米4',
                title: '红米4t',
              },
            ],
          },
        ],
      },
      {
        id: '电视',
        title: '电视t',
        children: [
          {
            id: '小米电视4A',
            title: '小米电视4At',
          },
          {
            id: '小米电视4C',
            title: '小米电视4Ct',
          },
        ],
      },
    ]

    const getDataOnlyLeafCheckable = (data: any) => {
      return data.map((item: any) => {
        if (item.children) {
          item.checkable = item.checkable ?? false
          item.children = getDataOnlyLeafCheckable(item.children)
        }

        return item
      })
    }

    const dataOnlyLeafCheckable = getDataOnlyLeafCheckable(data)

    return dataOnlyLeafCheckable
  })

  return (
    <>
      <h1>Addon</h1>
      <div className="cascader-basic__wrap">
        <CheckCascader
          style={{ width: 240 }}
          searchable={false}
          // clearable
          placeholder="请选择品类"
          defaultValue={[['手机', '红米', '红米4']]}
          tagInputProps={{ wrap: true }}
          prefix={<AppStoreOutlined style={{ color: '#333' }} />}
          suffix={<InfoCircleOutlined style={{ color: '#333' }} />}
          changeOnSelect
          data={dataOnlyLeafCheckable}
          onChange={console.log}
        ></CheckCascader>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'

/**
 * @title 基础用法
 * @desc 展示从多个收起的备选项中选出的多个选项
 */
export const Basic = () => {
  const [dataOnlyLeafCheckable] = React.useState(() => {
    const data = [
      {
        id: '手机',
        title: '手机t',
        children: [
          {
            id: '小米',
            title: '小米t',
            children: [
              {
                id: '小米3',
                title: '小米3t',
              },
              {
                id: '小米4',
                title: '小米4t',
              },
            ],
          },
          {
            id: '红米',
            title: '红米t',
            children: [
              {
                id: '红米3',
                title: '红米3t',
              },
              {
                id: '红米4',
                title: '红米4t',
              },
            ],
          },
        ],
      },
      {
        id: '电视',
        title: '电视t',
        children: [
          {
            id: '小米电视4A',
            title: '小米电视4At',
          },
          {
            id: '小米电视4C',
            title: '小米电视4Ct',
          },
        ],
      },
    ]

    const getDataOnlyLeafCheckable = (data: any) => {
      return data.map((item: any) => {
        if (item.children) {
          item.checkable = item.checkable ?? false
          item.children = getDataOnlyLeafCheckable(item.children)
        }

        return item
      })
    }

    const dataOnlyLeafCheckable = getDataOnlyLeafCheckable(data)

    return dataOnlyLeafCheckable
  })

  return (
    <>
      <h1>Basic</h1>
      <div className="cascader-basic__wrap">
        <CheckCascader
          style={{ width: 240 }}
          searchable={false}
          // clearable
          placeholder="请选择品类"
          defaultValue={[['手机', '红米', '红米4']]}
          changeOnSelect
          data={dataOnlyLeafCheckable}
          onChange={console.log}
        ></CheckCascader>
      </div>
    </>
  )
}

```

### custom-render.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'
import Input from '@hi-ui/input'

/**
 * @title 自定义触发器
 */
export const CusotmRender = () => {
  const [dataOnlyLeafCheckable] = React.useState(() => {
    const data = [
      {
        id: '手机',
        title: '手机t',
        children: [
          {
            id: '小米',
            title: '小米t',
            children: [
              {
                id: '小米3',
                title: '小米3t',
              },
              {
                id: '小米4',
                title: '小米4t',
              },
            ],
          },
          {
            id: '红米',
            title: '红米t',
            children: [
              {
                id: '红米3',
                title: '红米3t',
              },
              {
                id: '红米4',
                title: '红米4t',
              },
            ],
          },
        ],
      },
      {
        id: '电视',
        title: '电视t',
        children: [
          {
            id: '小米电视4A',
            title: '小米电视4At',
          },
          {
            id: '小米电视4C',
            title: '小米电视4Ct',
          },
        ],
      },
    ]

    const getDataOnlyLeafCheckable = (data: any) => {
      return data.map((item: any) => {
        if (item.children) {
          item.checkable = item.checkable ?? false
          item.children = getDataOnlyLeafCheckable(item.children)
        }

        return item
      })
    }

    const dataOnlyLeafCheckable = getDataOnlyLeafCheckable(data)

    return dataOnlyLeafCheckable
  })

  return (
    <>
      <h1>CusotmRender</h1>
      <div className="check-cascader-custom-render__wrap">
        <CheckCascader
          style={{ width: 240 }}
          searchable={false}
          placeholder="请选择品类"
          changeOnSelect
          data={dataOnlyLeafCheckable}
          onChange={console.log}
          customRender={(data) => {
            let value = ''
            if (data) {
              value = data?.map((item) => item?.title).join(',')
            }
            return <Input value={!value ? '' : value} placeholder="请选择" />
          }}
        ></CheckCascader>
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'

/**
 * @title 禁用状态
 */
export const Disabled = () => {
  const [data] = React.useState(() => {
    const data = [
      {
        id: '0',
        title: '0',
        children: [
          {
            id: '0-0',
            title: '0-0',
            children: [
              {
                id: '0-0-0',
                title: '0-0-0',
              },
              {
                id: '0-0-1',
                title: '0-0-1',
              },
              {
                id: '0-0-2',
                title: '0-0-2',
              },
            ],
          },
          {
            id: '0-1',
            title: '0-1',
            checkable: true,
            children: [
              {
                id: '0-1-0',
                title: '0-1-0',
              },
              {
                id: '0-1-1',
                title: '0-1-1',
              },
            ],
          },
          {
            id: '0-2',
            title: '0-2',
            checkable: true,
            disabled: true,
            children: [
              {
                id: '0-2-0',
                title: '0-2-0',
              },
              {
                id: '0-2-1',
                title: '0-2-1',
              },
            ],
          },
          {
            id: '0-3',
            title: '0-3',
            children: [
              {
                id: '0-3-0',
                title: '0-3-0',
              },
              {
                id: '0-3-1',
                title: '0-3-1',
              },
              {
                id: '0-3-2',
                title: '0-3-2',
              },
            ],
          },
          {
            id: '0-4',
            title: '0-4',
            checkable: true,
            disabledCheckbox: true,
            children: [
              {
                id: '0-4-0',
                title: '0-4-0',
              },
              {
                id: '0-4-1',
                title: '0-4-1',
              },
            ],
          },
          {
            id: '0-5',
            title: '0-5',
            checkable: true,
            children: [
              {
                id: '0-5-0',
                title: '0-5-0',
              },
              {
                id: '0-5-1',
                title: '0-5-1',
              },
            ],
          },
        ],
      },
      {
        id: '1',
        title: '1',
        children: [
          {
            id: '1-0',
            title: '1-0',
            disabledCheckbox: true,
            children: [
              {
                id: '1-0-0',
                title: '1-0-0',
                checkable: false,
              },
              {
                id: '1-0-1',
                title: '1-0-1',
                children: [
                  {
                    id: '1-0-1-0',
                    title: '1-0-1-0',
                  },
                  {
                    id: '1-0-1-1',
                    title: '1-0-1-1',
                  },
                ],
              },
              {
                id: '1-0-2',
                title: '1-0-2',
              },
            ],
          },
          {
            id: '1-1',
            title: '1-1',
            checkable: false,
          },
          {
            id: '1-2',
            title: '1-2',
          },
          {
            id: '1-3',
            title: '1-3',
          },
        ],
      },
    ]

    return data
  })

  return (
    <>
      <h2>整体禁用</h2>
      <div className="cascader-disabled__wrap">
        <CheckCascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          disabled
          searchPlaceholder="请输入搜索内容"
          data={data}
        />
      </div>

      <h2>禁用某个选项</h2>
      <div className="cascader-disabled__wrap">
        <CheckCascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          searchPlaceholder="请输入搜索内容"
          data={data}
          defaultValue={[['0', '0-2']]}
        />
      </div>
    </>
  )
}

```

### display-render.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'

/**
 * @title 自定义回显展示
 */
export const DisplayRender = () => {
  const [dataOnlyLeafCheckable] = React.useState(() => {
    const data = [
      {
        id: '手机',
        title: '手机t',
        children: [
          {
            id: '小米',
            title: '小米t',
            children: [
              {
                id: '小米3',
                title: '小米3t',
              },
              {
                id: '小米4',
                title: '小米4t',
              },
            ],
          },
          {
            id: '红米',
            title: '红米t',
            children: [
              {
                id: '红米3',
                title: '红米3t',
              },
              {
                id: '红米4',
                title: '红米4t',
              },
            ],
          },
        ],
      },
      {
        id: '电视',
        title: '电视t',
        children: [
          {
            id: '小米电视4A',
            title: '小米电视4At',
          },
          {
            id: '小米电视4C',
            title: '小米电视4Ct',
          },
        ],
      },
    ]

    const getDataOnlyLeafCheckable = (data: any) => {
      return data.map((item) => {
        if (item.children) {
          item.checkable = item.checkable ?? false
          item.children = getDataOnlyLeafCheckable(item.children)
        }

        return item
      })
    }

    const dataOnlyLeafCheckable = getDataOnlyLeafCheckable(data)

    return dataOnlyLeafCheckable
  })

  console.log(dataOnlyLeafCheckable)

  return (
    <>
      <h1>DisplayRender</h1>
      <div className="cascader-display-render__wrap">
        <CheckCascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          defaultValue={[['手机', '红米', '红米4']]}
          data={dataOnlyLeafCheckable}
          displayRender={(option) => {
            const titleArr = []
            while (option.parent) {
              titleArr.push(option.title)
              option = option.parent
            }
            return titleArr.reverse().join(' | ')
          }}
        ></CheckCascader>
      </div>
    </>
  )
}

```

### dropdown-column-render.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'

/**
 * @title 自定义下拉菜单内容
 */
export const DropdownColumnRender = () => {
  const [dataOnlyLeafCheckable] = React.useState(() => {
    const data = [
      {
        id: '手机',
        title: '手机t',
        children: [
          {
            id: '小米',
            title: '小米t',
            children: [
              {
                id: '小米3',
                title: '小米3t',
              },
              {
                id: '小米4',
                title: '小米4t',
              },
            ],
          },
          {
            id: '红米',
            title: '红米t',
            children: [
              {
                id: '红米3',
                title: '红米3t',
              },
              {
                id: '红米4',
                title: '红米4t',
              },
            ],
          },
        ],
      },
      {
        id: '电视',
        title: '电视t',
        children: [
          {
            id: '小米电视4A',
            title: '小米电视4At',
          },
          {
            id: '小米电视4C',
            title: '小米电视4Ct',
          },
        ],
      },
      {
        id: '1',
        title: '小米1',
      },
      {
        id: '2',
        title: '小米2',
      },
      {
        id: '3',
        title: '小米3',
      },
      {
        id: '4',
        title: '小米4',
      },
      {
        id: '5',
        title: '小米5',
      },
      {
        id: '6',
        title: '小米6',
      },
      {
        id: '7',
        title: '小米7',
      },
    ]

    const getDataOnlyLeafCheckable = (data: any) => {
      return data.map((item: any) => {
        if (item.children) {
          item.checkable = item.checkable ?? false
          item.children = getDataOnlyLeafCheckable(item.children)
        }

        return item
      })
    }

    const dataOnlyLeafCheckable = getDataOnlyLeafCheckable(data)

    return dataOnlyLeafCheckable
  })

  return (
    <>
      <h1>DropdownColumnRender</h1>
      <div className="cascader-dropdown-column-render__wrap">
        <CheckCascader
          style={{ width: 240 }}
          searchable={false}
          // clearable
          placeholder="请选择品类"
          defaultValue={[['手机', '红米', '红米4']]}
          changeOnSelect
          data={dataOnlyLeafCheckable}
          onChange={console.log}
          // 如果有样式不满足需求，可以给弹出层设置独有的 className 来进行样式覆写
          overlay={{ className: 'my-overlay' }}
          dropdownColumnRender={(menu, level) => {
            return level < 5 ? (
              <div
                className="custom-menu"
                style={{ overflow: 'hidden', borderRight: '1px solid #ebedf0' }}
              >
                <header
                  style={{
                    lineHeight: '20px',
                    padding: '0px 8px 8px',
                    borderBottom: '1px solid #ebedf0',
                  }}
                >
                  header
                </header>
                {React.cloneElement(menu, { style: { height: 186 } })}
                <footer
                  style={{
                    lineHeight: '20px',
                    padding: '8px 8px 0',
                    borderTop: '1px solid #ebedf0',
                  }}
                >
                  footer(level {level})
                </footer>
              </div>
            ) : (
              menu
            )
          }}
        ></CheckCascader>
      </div>
    </>
  )
}

```

### dynamic.stories.tsx

```typescript
import Alert from '@hi-ui/alert'
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'

/**
 * @title 异步加载数据
 */
export const Dynamic = () => {
  const [treeData] = React.useState([
    {
      id: 1,
      title: '小米',
      children: [
        {
          id: 2,
          title: '技术',
          children: [
            { id: 3, title: '后端' },
            { id: 4, title: '运维' },
            { id: 5, title: '前端' },
          ],
        },
        { id: 6, title: '产品' },
      ],
    },
    {
      id: 11,
      title: '小米',
      children: [
        { id: 22, title: '技术' },
        { id: 66, title: '产品' },
      ],
    },
  ])

  // 加载节点
  const loadChildren = async (node) => {
    return fetch(`https://my-json-server.typicode.com/hiui-group/db/conditiondata?id=${node.id}`)
      .then((res) => res.json())
      .then((data) => {
        if (data[0]) {
          data[0].id = Math.random()
        }

        // setTreeData((prev) => {
        //   const nextData = cloneTree(prev)
        //   const loadNode = findNode(node.id, nextData)
        //   loadNode.children = data
        //   console.log(loadNode, nextData)
        //   return nextData
        // })

        return data
      })
  }

  return (
    <>
      <h1>Dynamic for CheckCascader</h1>
      <div className="check-cascader-dynamic__wrap">
        <Alert
          type="danger"
          closeable={false}
          showIcon={false}
          title={
            '注意：对于异步加载子节点，可以配合 `node.isLeaf: true` 来表明是否为叶子结点。以此来告诉组件是否有下一级子面板'
          }
        ></Alert>
        <br />
        <CheckCascader
          style={{ width: 240 }}
          data={treeData}
          onLoadChildren={loadChildren}
          defaultValue={[[1]]}
          checkedMode="PARENT"
          onChange={console.log}
        ></CheckCascader>
      </div>
    </>
  )
}

```

### footer.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'

/**
 * @title 吸底内容条
 */
export const Footer = () => {
  const [dataOnlyLeafCheckable] = React.useState(() => {
    const data = [
      {
        id: '手机',
        title: '手机t',
        children: [
          {
            id: '小米',
            title: '小米t',
            children: [
              {
                id: '小米3',
                title: '小米3t',
              },
              {
                id: '小米4',
                title: '小米4t',
              },
            ],
          },
          {
            id: '红米',
            title: '红米t',
            children: [
              {
                id: '红米3',
                title: '红米3t',
              },
              {
                id: '红米4',
                title: '红米4t',
              },
            ],
          },
        ],
      },
      {
        id: '电视',
        title: '电视t',
        children: [
          {
            id: '小米电视4A',
            title: '小米电视4At',
          },
          {
            id: '小米电视4C',
            title: '小米电视4Ct',
          },
        ],
      },
    ]

    const getDataOnlyLeafCheckable = (data: any) => {
      return data.map((item: any) => {
        if (item.children) {
          item.checkable = item.checkable ?? false
          item.children = getDataOnlyLeafCheckable(item.children)
        }

        return item
      })
    }

    const dataOnlyLeafCheckable = getDataOnlyLeafCheckable(data)

    return dataOnlyLeafCheckable
  })

  return (
    <>
      <h1>Footer</h1>
      <div className="cascader-footer__wrap">
        <CheckCascader
          style={{ width: 240 }}
          searchable={false}
          // clearable
          placeholder="请选择品类"
          defaultValue={[['手机', '红米', '红米4']]}
          changeOnSelect
          data={dataOnlyLeafCheckable}
          onChange={console.log}
          renderExtraFooter={() => <div>custom footer</div>}
        ></CheckCascader>
      </div>
    </>
  )
}

```

### search.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'

/**
 * @title 带搜索
 * @desc 选项数量较大，不熟悉数据的结构关系情况下，用搜索关键词的方式快速定位
 */
export const Search = () => {
  const [dataOnlyLeafCheckable] = React.useState(() => {
    const data = [
      {
        id: 'up-1',
        title: 'up',
        children: [
          {
            id: 'up-1-0',
            title: '小米',
            children: [
              {
                id: 'up-1-0-0',
                title: 'leaf',
              },
            ],
          },
          {
            id: 'up-1-1',
            title: '1-1',
          },
        ],
      },
      {
        id: '0',
        title: '0',
        children: [
          {
            id: '0-0',
            title: '0-0',
            children: [
              {
                id: '0-0-0',
                title: '0-0-0',
              },
              {
                id: '0-0-1',
                title: '0-0-1',
              },
              {
                id: '0-0-2',
                title: '0-0-2',
              },
            ],
          },
          {
            id: '0-1',
            title: '0-1',
            checkable: true,
            children: [
              {
                id: '0-1-0',
                title: '0-1-0',
              },
              {
                id: '0-1-1',
                title: '0-1-1',
              },
            ],
          },
          {
            id: '0-2',
            title: '0-2',
            checkable: true,
            children: [
              {
                id: '0-2-0',
                title: '0-2-0',
              },
              {
                id: '0-2-1',
                title: '0-2-1',
              },
            ],
          },
          {
            id: '0-3',
            title: '0-3',
            children: [
              {
                id: '0-3-0',
                title: '0-3-0',
              },
              {
                id: '0-3-1',
                title: '0-3-1',
              },
              {
                id: '0-3-2',
                title: '0-3-2',
              },
            ],
          },
          {
            id: '0-4',
            title: '0-4',
            checkable: true,
            children: [
              {
                id: '0-4-0',
                title: '0-4-0',
              },
              {
                id: '0-4-1',
                title: '0-4-1',
              },
            ],
          },
          {
            id: '0-5',
            title: '0-5',
            checkable: true,
            children: [
              {
                id: '0-5-0',
                title: '0-5-0',
              },
              {
                id: '0-5-1',
                title: '0-5-1',
              },
            ],
          },
          {
            id: '0-6',
            title: '0-6',
            children: [
              {
                id: '0-6-0',
                title: '0-6-0',
              },
              {
                id: '0-6-1',
                title: '0-6-1',
              },
              {
                id: '0-6-2',
                title: '0-6-2',
              },
            ],
          },
          {
            id: '0-7',
            title: '0-7',
            checkable: true,
            children: [
              {
                id: '0-7-0',
                title: '0-7-0',
              },
              {
                id: '0-7-1',
                title: '0-7-1',
              },
            ],
          },
          {
            id: '0-8',
            title: '0-8',
            checkable: true,
            children: [
              {
                id: '0-8-0',
                title: '0-8-0',
              },
              {
                id: '0-8-1',
                title: '0-8-1',
              },
            ],
          },
        ],
      },
      {
        id: '1',
        title: '1',
        children: [
          {
            id: '1-0',
            title: '1-0',
          },
          {
            id: '1-1',
            title: '1-1',
          },
        ],
      },
      {
        id: '2',
        title: '2',
        children: [
          {
            id: '2-0',
            title: '2-0',
          },
          {
            id: '2-1',
            title: '2-1',
          },
        ],
      },
    ]

    const getDataOnlyLeafCheckable = (data: any) => {
      return data.map((item) => {
        if (item.children) {
          item.checkable = item.checkable ?? false
          item.children = getDataOnlyLeafCheckable(item.children)
        } else {
          item.checkable = true
        }

        return item
      })
    }

    const dataOnlyLeafCheckable = getDataOnlyLeafCheckable(data)

    return dataOnlyLeafCheckable
  })

  console.log(dataOnlyLeafCheckable)

  return (
    <>
      <h1>Search</h1>
      <div className="cascader-search__wrap">
        <CheckCascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          searchPlaceholder="请输入搜索内容"
          data={dataOnlyLeafCheckable}
          searchable
        />
      </div>
    </>
  )
}

```

### select-change.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'

/**
 * @title 选择即改变
 * @desc 选中选项即可完成勾选，配合 hover 展开使用
 */
export const SelectChange = () => {
  const [dataOnlyLeafCheckable] = React.useState(() => {
    const data = [
      {
        id: '0',
        title: '0',
        children: [
          {
            id: '0-0',
            title: '0-0',
            children: [
              {
                id: '0-0-0',
                title: '0-0-0',
              },
              {
                id: '0-0-1',
                title: '0-0-1',
              },
              {
                id: '0-0-2',
                title: '0-0-2',
              },
            ],
          },
          {
            id: '0-1',
            title: '0-1',
            checkable: true,
            children: [
              {
                id: '0-1-0',
                title: '0-1-0',
              },
              {
                id: '0-1-1',
                title: '0-1-1',
              },
            ],
          },
          {
            id: '0-2',
            title: '0-2',
            checkable: true,
            disabled: false,
            children: [
              {
                id: '0-2-0',
                title: '0-2-0',
              },
              {
                id: '0-2-1',
                title: '0-2-1',
              },
            ],
          },
          {
            id: '0-3',
            title: '0-3',
            children: [
              {
                id: '0-3-0',
                title: '0-3-0',
              },
              {
                id: '0-3-1',
                title: '0-3-1',
              },
              {
                id: '0-3-2',
                title: '0-3-2',
              },
            ],
          },
          {
            id: '0-4',
            title: '0-4',
            checkable: true,
            disabledCheckbox: true,
            children: [
              {
                id: '0-4-0',
                title: '0-4-0',
              },
              {
                id: '0-4-1',
                title: '0-4-1',
              },
            ],
          },
          {
            id: '0-5',
            title: '0-5',
            checkable: true,
            children: [
              {
                id: '0-5-0',
                title: '0-5-0',
              },
              {
                id: '0-5-1',
                title: '0-5-1',
              },
            ],
          },
        ],
      },
      {
        id: '1',
        title: '1',
        children: [
          {
            id: '1-0',
            title: '1-0',
            disabledCheckbox: true,
          },
          {
            id: '1-1',
            title: '1-1',
          },
        ],
      },
    ]

    const getDataOnlyLeafCheckable = (data: any) => {
      return data.map((item) => {
        if (item.children) {
          item.checkable = item.checkable ?? false
          item.children = getDataOnlyLeafCheckable(item.children)
        } else {
          item.checkable = true
        }

        return item
      })
    }

    const dataOnlyLeafCheckable = getDataOnlyLeafCheckable(data)

    return dataOnlyLeafCheckable
  })

  return (
    <>
      <h1>SelectChange</h1>
      <div className="cascader-select-change__wrap">
        <CheckCascader
          style={{ width: 240 }}
          placeholder="请选择品类"
          changeOnSelect
          expandTrigger="hover"
          searchPlaceholder="请输入搜索内容"
          data={dataOnlyLeafCheckable}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  const [dataOnlyLeafCheckable] = React.useState(() => {
    const data = [
      {
        id: '手机',
        title: '手机t',
        children: [
          {
            id: '小米',
            title: '小米t',
            children: [
              {
                id: '小米3',
                title: '小米3t',
              },
              {
                id: '小米4',
                title: '小米4t',
              },
            ],
          },
          {
            id: '红米',
            title: '红米t',
            children: [
              {
                id: '红米3',
                title: '红米3t',
              },
              {
                id: '红米4',
                title: '红米4t',
              },
            ],
          },
        ],
      },
      {
        id: '电视',
        title: '电视t',
        children: [
          {
            id: '小米电视4A',
            title: '小米电视4At',
          },
          {
            id: '小米电视4C',
            title: '小米电视4Ct',
          },
        ],
      },
    ]

    const getDataOnlyLeafCheckable = (data: any) => {
      return data.map((item: any) => {
        if (item.children) {
          item.checkable = item.checkable ?? false
          item.children = getDataOnlyLeafCheckable(item.children)
        }

        return item
      })
    }

    const dataOnlyLeafCheckable = getDataOnlyLeafCheckable(data)

    return dataOnlyLeafCheckable
  })

  return (
    <>
      <h1>Size</h1>
      <div className="cascader-size__wrap">
        <h2>sm</h2>
        <CheckCascader
          style={{ width: 240 }}
          size="sm"
          searchable={false}
          // clearable
          placeholder="请选择品类"
          defaultValue={[['手机', '红米', '红米4']]}
          changeOnSelect
          data={dataOnlyLeafCheckable}
          onChange={console.log}
        ></CheckCascader>
        <h2>md</h2>
        <CheckCascader
          style={{ width: 240 }}
          size="md"
          searchable={false}
          // clearable
          placeholder="请选择品类"
          defaultValue={[['手机', '红米', '红米4']]}
          changeOnSelect
          data={dataOnlyLeafCheckable}
          onChange={console.log}
        ></CheckCascader>
        <h2>lg</h2>
        <CheckCascader
          style={{ width: 240 }}
          size="lg"
          searchable={false}
          // clearable
          placeholder="请选择品类"
          defaultValue={[['手机', '红米', '红米4']]}
          changeOnSelect
          data={dataOnlyLeafCheckable}
          onChange={console.log}
        ></CheckCascader>
      </div>
    </>
  )
}

```

### tag-input-wrap.stories.tsx

```typescript
import React from 'react'
import CheckCascader from '@hi-ui/check-cascader'

/**
 * @title 展示全部已选项
 * @desc 设置后，选中内容超出宽度时会换行展示
 */
export const TagInputWrap = () => {
  const [dataOnlyLeafCheckable] = React.useState(() => {
    const data = [
      {
        id: '手机',
        title: '手机t',
        children: [
          {
            id: '小米',
            title: '小米t',
            children: [
              {
                id: '小米3',
                title: '小米3t',
              },
              {
                id: '小米4',
                title: '小米4t',
              },
            ],
          },
          {
            id: '红米',
            title: '红米t',
            children: [
              {
                id: '红米3',
                title: '红米3t',
              },
              {
                id: '红米4',
                title: '红米4t',
              },
            ],
          },
        ],
      },
      {
        id: '电视',
        title: '电视t',
        children: [
          {
            id: '小米电视4A',
            title: '小米电视4At',
          },
          {
            id: '小米电视4C',
            title: '小米电视4Ct',
          },
        ],
      },
    ]

    const getDataOnlyLeafCheckable = (data: any) => {
      return data.map((item: any) => {
        if (item.children) {
          item.checkable = item.checkable ?? false
          item.children = getDataOnlyLeafCheckable(item.children)
        }

        return item
      })
    }

    const dataOnlyLeafCheckable = getDataOnlyLeafCheckable(data)

    return dataOnlyLeafCheckable
  })

  return (
    <>
      <h1>展示全部已选项</h1>
      <div className="cascader-tag-input-wrap__wrap">
        <CheckCascader
          style={{ width: 240 }}
          searchable={false}
          // clearable
          placeholder="请选择品类"
          defaultValue={[['手机', '红米', '红米4']]}
          changeOnSelect
          data={dataOnlyLeafCheckable}
          onChange={console.log}
          tagInputProps={{
            wrap: true,
          }}
        ></CheckCascader>
      </div>
    </>
  )
}

```

## check-select 组件

### addon.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'
import { AppStoreOutlined, InfoCircleOutlined } from '@hi-ui/icons'

/**
 * @title 前后内置元素
 * @desc 将选择框与内置的其他元素组合使用
 */
export const Addon = () => {
  const [data] = React.useState([
    { title: '手机', id: '2' },
    { title: '小米2', id: '2-1' },
    { title: '小米3', id: '2-2' },
    { title: '小米4', id: '2-3' },
    { title: '小米5', id: '2-4' },
    { title: '电脑', id: '3' },
    { title: '笔记本', id: '4' },
    {
      title: '生活周边超长文案展示超长文案展示超长文案展示超长文案展示超长文案展示',
      id: '5',
    },
    { title: '其它', id: '6' },
  ])

  return (
    <>
      <h1>Addon</h1>
      <div className="check-select-addon__wrap">
        <CheckSelect
          style={{ width: 240 }}
          placeholder="请选择"
          searchable
          // clearable={false}
          data={data}
          tagInputProps={{ wrap: true }}
          prefix={<AppStoreOutlined />}
          suffix={<InfoCircleOutlined style={{ marginRight: 8 }} />}
        />
      </div>
    </>
  )
}

```

### appearance.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性、无UI三种
 */
export const Appearance = () => {
  const [value, setValue] = React.useState<React.ReactText[]>(['2'])
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Appearance</h1>
      <div className="tree-select-appearance__wrap">
        <div>
          <h4>filled</h4>
          <CheckSelect
            style={{ width: 240 }}
            data={data}
            value={value}
            clearable
            appearance="filled"
            onChange={(value, targetItem) => {
              console.log('CheckSelect onChange: ', value, targetItem)
              setValue(value)
            }}
          />
        </div>

        <div>
          <h4>outline</h4>
          <CheckSelect
            style={{ width: 240 }}
            data={data}
            value={value}
            clearable
            appearance="line"
            onChange={(value, targetItem) => {
              console.log('CheckSelect onChange: ', value, targetItem)
              setValue(value)
            }}
          />
        </div>

        <div>
          <h4>unset</h4>
          <CheckSelect
            data={data}
            value={value}
            clearable
            appearance="unset"
            optionWidth={260}
            onChange={(value, targetItem) => {
              console.log('CheckSelect onChange: ', value, targetItem)
              setValue(value)
            }}
          />
        </div>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 基础用法
 * @desc 展示从全部备选项选出的部分选项
 */
export const Basic = () => {
  const [data] = React.useState([
    { title: '手机', id: '2' },
    { title: '小米2', id: '2-1' },
    { title: '小米3', id: '2-2' },
    { title: '小米4', id: '2-3' },
    { title: '小米5', id: '2-4' },
    { title: '电脑', id: '3' },
    { title: '笔记本', id: '4' },
    {
      title: '生活周边超长文案展示超长文案展示超长文案展示超长文案展示超长文案展示',
      id: '5',
    },
    { title: '其它', id: '6' },
  ])

  return (
    <>
      <h1>Basic</h1>
      <div className="check-select-basic__wrap">
        <CheckSelect
          style={{ width: 240 }}
          placeholder="请选择"
          searchable
          clearable
          data={data}
          // render={(option) => {
          //   if (option.id === 'ABC1') {
          //     return '不限'
          //   }

          //   return true
          // }}
        />
      </div>
    </>
  )
}

```

### check-all.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 全选
 */
export const CheckAll = () => {
  const [value, setValue] = React.useState<React.ReactText[]>(['3'])

  const [data] = React.useState([
    { title: '红米 5A', id: '3' },
    { title: '红米 6A', id: '2' },
    { title: '红米 note8', id: '5' },
    { title: '小米电视E65A', id: '12' },
    { title: '小米电视4S', id: '13' },
    { title: '小米电视4C', id: '14' },
  ])

  return (
    <>
      <h1>CheckAll</h1>
      <div className="select-check-all__wrap">
        <CheckSelect
          style={{ width: 240 }}
          data={data}
          placeholder="请选择"
          showCheckAll
          showOnlyShowChecked
          value={value}
          onChange={(selectedId) => {
            setValue(selectedId)
          }}
        />
      </div>
    </>
  )
}

```

### clearable.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 清空选中项
 */
export const Clearable = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Clearable</h1>
      <div className="select-clearable__wrap">
        <CheckSelect style={{ width: 240 }} clearable data={data} onChange={console.log} />
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import Button from '@hi-ui/button'
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [value, setValue] = React.useState<React.ReactText[]>(['3'])
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Controlled</h1>
      <div className="select-controlled__wrap">
        <Button
          onClick={() => {
            setValue([])
          }}
        >
          清空
        </Button>
        <br />
        <br />
        <CheckSelect
          style={{ width: 240 }}
          clearable={false}
          data={data}
          value={value}
          onChange={(selectedId) => {
            setValue(selectedId)
          }}
        />
      </div>
    </>
  )
}

```

### custom-render.stories.tsx

```typescript
import React from 'react'
import { FilterOutlined } from '@hi-ui/icons'
import Button from '@hi-ui/button'
import Space from '@hi-ui/space'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 自定义触发器
 */
export const CustomRender = () => {
  const [data] = React.useState([
    { title: '手机', id: '2' },
    { title: '小米2', id: '2-1' },
    { title: '小米3', id: '2-2' },
    { title: '小米4', id: '2-3' },
    { title: '小米5', id: '2-4' },
    { title: '电脑', id: '3' },
    { title: '笔记本', id: '4' },
    {
      title: '生活周边超长文案展示超长文案展示超长文案展示超长文案展示超长文案展示',
      id: '5',
    },
    { title: '其它', id: '6' },
  ])

  return (
    <>
      <h1>CustomRender</h1>
      <div className="check-select-custom-render__wrap">
        <h2>只展示图标</h2>
        <CheckSelect
          style={{ width: 'auto' }}
          optionWidth={200}
          placeholder="请选择"
          searchable
          clearable
          data={data}
          onChange={console.log}
          customRender={<FilterOutlined />}
        />
        <h2>展示选中内容</h2>
        <CheckSelect
          style={{ width: 'auto' }}
          optionWidth={200}
          placeholder="请选择"
          searchable
          clearable
          data={data}
          onChange={console.log}
          customRender={(value) => {
            return (
              <Space>
                <Button>点击选择</Button>
                <Space onClick={(e) => e.stopPropagation()}>
                  {value.map((item, index) => (
                    <span key={index}>{item.title}</span>
                  ))}
                </Space>
              </Space>
            )
          }}
        />
      </div>
    </>
  )
}

```

### data-source.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 异步加载搜索
 * @desc 备选项数量较大时，通过搜索选项关键词调取存储于服务端数据备选项的一个或多个
 */
export const DataSource = () => {
  const [data] = React.useState([
    {
      id: 'up-1',
      title: 'up',
    },
    {
      id: '0',
      title: '0',
    },
    {
      id: '1',
      title: '1',
    },
    {
      id: '2',
      title: '2',
    },
  ])

  return (
    <>
      <h1>DataSource</h1>
      <div className="cascader-DataSource__wrap">
        <CheckSelect
          style={{ width: 240 }}
          // placeholder="请选择品类"
          // searchPlaceholder="请输入搜索内容"
          data={data}
          onChange={console.log}
          // searchOnInit
          dataSource={(keyword) => {
            console.log('DataSource', keyword)
            const url =
              'https://www.fastmock.site/mock/eef9b373d82560f30585521549c4b6cb/hiui/api/list?keyword=' +
              keyword
            return fetch(url)
              .then((response) => {
                return response.json()
              })
              .then(function (res) {
                return res.list
              })
          }}
        />
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 禁用状态
 * @desc 暂不可操作的状态
 */
export const Disabled = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: true },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: true },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])
  return (
    <>
      <h1>Disabled</h1>
      <div className="check-select-basic__wrap">
        <h2>整体禁用</h2>
        <CheckSelect
          style={{ width: 240 }}
          placeholder="请选择"
          searchable
          disabled
          data={data}
          defaultValue={['2']}
        />

        <h2>禁用某个选项</h2>
        <CheckSelect
          style={{ width: 240 }}
          placeholder="请选择"
          searchable
          data={data}
          defaultValue={['2']}
        />
      </div>
    </>
  )
}

```

### display-render.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 自定义回显展示
 */
export const DisplayRender = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>DisplayRender</h1>
      <div className="check-select-display-render__wrap">
        <CheckSelect
          style={{ width: 240 }}
          clearable={false}
          data={data}
          displayRender={(item) => {
            console.log(item)
            return (
              <React.Fragment>
                <span style={{ float: 'left' }}>{item.title}</span>
                <span style={{ float: 'right', color: '#999', fontSize: 14 }}>({item.id})</span>
              </React.Fragment>
            )
          }}
        />
      </div>
    </>
  )
}

```

### empty-content.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 自定义空内容
 */
export const EmptyContent = () => {
  const [data] = React.useState([])

  return (
    <>
      <h1>EmptyContent</h1>
      <div className="check-select-empty-content__wrap">
        <CheckSelect style={{ width: 240 }} data={data} emptyContent="暂无选项" />
      </div>
    </>
  )
}

```

### filter-options.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 自定义筛选
 * @desc 通过 filterOption 可自定义搜索条件的算法
 */
export const FilterOptions = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  // 注意 filterOption 是影响搜索渲染的，是完全受控的，useCallback 包裹可以减少无效的重渲染，提升性能
  const filterOptionMemo = React.useCallback((keyword: string, item: any) => {
    return item.id >= parseInt(keyword)
  }, [])

  return (
    <>
      <h1>FilterOptions</h1>
      <div className="select-filter-options__wrap">
        <CheckSelect
          style={{ width: 240 }}
          clearable={false}
          data={data}
          filterOption={filterOptionMemo}
        />
      </div>
    </>
  )
}

```

### footer.stories.tsx

```typescript
import Input from '@hi-ui/input'
import React from 'react'
import CheckSelect from '@hi-ui/check-select'
import { PlusOutlined } from '@hi-ui/icons'

/**
 * @title 吸底内容条
 */
export const Footer = () => {
  const [data, setData] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  const [inputValue, setInputValue] = React.useState('')

  return (
    <>
      <h1>Footer</h1>
      <div className="check-select-footer__wrap">
        <CheckSelect
          style={{ width: 240 }}
          clearable={false}
          data={data}
          renderExtraFooter={() => {
            return (
              <Input
                placeholder="添加选项"
                value={inputValue}
                onChange={(evt) => {
                  setInputValue(evt.target.value)
                }}
                suffix={
                  <PlusOutlined
                    style={{ cursor: 'pointer' }}
                    onClick={() => {
                      setData((prev) => {
                        return [...prev, { id: Math.random() + inputValue, title: inputValue }]
                      })
                      setInputValue('')
                    }}
                  />
                }
              />
            )
          }}
        />
      </div>
    </>
  )
}

```

### group.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 类型分组
 */
export const Group = () => {
  const [value, setValue] = React.useState<React.ReactText[]>(['3'])

  const [data] = React.useState([
    {
      groupId: 'redmi',
      groupTitle: '红米手机',
      children: [
        { title: '红米 5A', id: '3' },
        { title: '红米 6A', id: '2' },
        { title: '红米 note', id: '4' },
        { title: '红米 note8', id: '5' },
      ],
    },
    {
      groupId: 'mi',
      groupTitle: '小米电视',
      children: [
        { title: '小米电视4A 60寸', id: '10' },
        { title: '小米电视E55A', id: '11' },
        { title: '小米电视E65A', id: '12' },
        { title: '小米电视4S', id: '13' },
        { title: '小米电视4C', id: '14' },
      ],
    },
  ])

  return (
    <>
      <h1>Group</h1>
      <div className="select-Group__wrap">
        <CheckSelect
          style={{ width: 240 }}
          data={data}
          placeholder="请选择"
          value={value}
          onChange={(selectedId) => {
            setValue(selectedId)
          }}
        />
      </div>
    </>
  )
}

```

### only-checked.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 仅已选过滤
 */
export const OnlyChecked = () => {
  const [data] = React.useState([
    { title: '手机', id: '2' },
    { title: '小米2', id: '2-1' },
    { title: '小米3', id: '2-2' },
    { title: '小米4', id: '2-3' },
    { title: '小米5', id: '2-4' },
    { title: '电脑', id: '3' },
    { title: '笔记本', id: '4' },
    { title: '生活周边', id: '5' },
    { title: '其它', id: '6' },
  ])

  return (
    <>
      <h1>OnlyChecked</h1>
      <div className="check-select-only-checked__wrap">
        <CheckSelect
          style={{ width: 240 }}
          placeholder="请选择"
          searchable
          clearable
          data={data}
          showOnlyShowChecked
          // showCheckAll
        />
      </div>
    </>
  )
}

```

### pinyin.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

import { match } from 'pinyin-pro'

/**
 * @title 拼音搜索
 * @desc 通过输入拼音搜索关键字
 */
export const Pinyin = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  // 注意 filterOption 是影响搜索渲染的，是完全受控的，useCallback 包裹可以减少无效的重渲染，提升性能
  const filterOptionMemo = React.useCallback((keyword: string, item: any) => {
    return !!match(item.title as string, keyword)
  }, [])

  return (
    <>
      <h1>Pinyin</h1>
      <div className="select-pinyin__wrap">
        <CheckSelect
          style={{ width: 240 }}
          clearable={false}
          data={data}
          filterOption={filterOptionMemo}
        />
      </div>
    </>
  )
}

```

### search.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 带搜索
 */
export const Search = () => {
  const [data] = React.useState([
    {
      id: 'up-1',
      title: 'up',
    },
    {
      id: '0',
      title: '0',
    },
    {
      id: '1',
      title: '1',
    },
    {
      id: '2',
      title: '2',
    },
  ])

  return (
    <>
      <h1>Search</h1>
      <div className="check-select-search__wrap">
        <CheckSelect
          style={{ width: 240 }}
          searchable
          data={data}
          placeholder="请选择品类"
          searchPlaceholder="请输入搜索内容"
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  const [data] = React.useState([
    { title: '手机', id: '2' },
    { title: '小米2', id: '2-1' },
    { title: '小米3', id: '2-2' },
    { title: '小米4', id: '2-3' },
    { title: '小米5', id: '2-4' },
    { title: '电脑', id: '3' },
    { title: '笔记本', id: '4' },
    {
      title: '生活周边超长文案展示超长文案展示超长文案展示超长文案展示超长文案展示',
      id: '5',
    },
    { title: '其它', id: '6' },
  ])

  return (
    <>
      <h1>Size</h1>
      <div className="check-select-size__wrap">
        <h2>sm</h2>
        <CheckSelect
          style={{ width: 240 }}
          size="sm"
          placeholder="请选择"
          searchable
          clearable
          data={data}
        />
        <h2>md</h2>
        <CheckSelect
          style={{ width: 240 }}
          size="md"
          placeholder="请选择"
          searchable
          clearable
          data={data}
        />
        <h2>lg</h2>
        <CheckSelect
          style={{ width: 240 }}
          size="lg"
          placeholder="请选择"
          searchable
          clearable
          data={data}
        />
      </div>
    </>
  )
}

```

### tag-input-wrap.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 展示全部已选项
 * @desc 设置后，选中内容超出宽度时会换行展示
 */
export const TagInputWrap = () => {
  const [data] = React.useState([
    { title: '手机', id: '2' },
    { title: '小米2', id: '2-1' },
    { title: '小米3', id: '2-2' },
    { title: '小米4', id: '2-3' },
    { title: '小米5', id: '2-4' },
    { title: '电脑', id: '3' },
    { title: '笔记本', id: '4' },
    {
      title: '生活周边超长文案展示超长文案展示超长文案展示超长文案展示超长文案展示',
      id: '5',
    },
    { title: '其它', id: '6' },
  ])

  return (
    <>
      <h1>展示全部已选项</h1>
      <div className="check-select-tag-input-wrap__wrap">
        <CheckSelect
          style={{ width: 240 }}
          placeholder="请选择"
          searchable
          clearable
          data={data}
          tagInputProps={{
            wrap: true,
          }}
        />
      </div>
    </>
  )
}

```

### tip.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'
import Tooltip from '@hi-ui/tooltip'
import Checkbox from '@hi-ui/checkbox'

/**
 * @title 带Tooltip提示
 */
export const Tip = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边超级长文案展示生活周边超级长文案展示', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Tip</h1>
      <div className="check-select-tip__wrap">
        <CheckSelect
          style={{ width: 240 }}
          clearable={false}
          data={data}
          render={(item) => {
            console.log(item)
            return (
              <Tooltip title={item.title} placement="right">
                <Checkbox
                  checked={item.checked}
                  disabled={item.disabled}
                  style={{
                    width: '100%',
                    overflow: 'hidden',
                    textOverflow: 'ellipsis',
                    whiteSpace: 'nowrap',
                  }}
                >
                  {item.title}
                </Checkbox>
              </Tooltip>
            )
          }}
        />
      </div>
    </>
  )
}

```

### title-render.stories.tsx

```typescript
import { CheckOutlined } from '@hi-ui/icons'
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 自定义选项展示
 * @desc 可自定义选项的信息结构或样式
 */
export const TitleRender = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>TitleRender</h1>
      <div className="select-TitleRender__wrap">
        <CheckSelect
          style={{ width: 240 }}
          clearable={false}
          data={data}
          render={(item) => {
            return (
              <React.Fragment>
                <span style={{ float: 'left' }}>{item.title}</span>
                {item.checked ? (
                  <span style={{ float: 'right' }}>
                    <CheckOutlined />
                  </span>
                ) : null}
              </React.Fragment>
            )
          }}
        />
      </div>
    </>
  )
}

```

### uncontrolled.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 非受控
 */
export const Uncontrolled = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Uncontrolled</h1>
      <div className="select-uncontrolled__wrap">
        <CheckSelect
          style={{ width: 240 }}
          data={data}
          defaultValue={['3']}
          onChange={(selectedId) => {
            console.log('onChange', selectedId)
          }}
        />
      </div>
    </>
  )
}

```

### virtual-list.stories.tsx

```typescript
import React from 'react'
import CheckSelect from '@hi-ui/check-select'

/**
 * @title 大数据
 */
export const VirtualList = () => {
  const [data] = React.useState(() => {
    const data: any[] = []
    for (let i = 0; i < 5000; i++) {
      const value = `${i.toString(36)}-${i}`
      data.push({
        id: value,
        title: value,
        disabled: i === 10,
      })
    }

    return data
  })

  console.log('data', data)

  return (
    <>
      <h1>VirtualList</h1>
      <div className="check-select-search__wrap">
        <CheckSelect
          style={{ width: 240 }}
          data={data}
          searchable
          height={260}
          defaultValue={data.map((v) => v.id)}
          placeholder="请选择品类"
          searchPlaceholder="请输入搜索内容"
        ></CheckSelect>
      </div>
    </>
  )
}

```

## check-tree-select 组件

### addon.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'
import { AppStoreOutlined, InfoCircleOutlined } from '@hi-ui/icons'

/**
 * @title 前后内置元素
 */
export const Addon = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          disabled: true,
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Addon</h1>
      <div className="check-tree-select-addon__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          checkedMode="PARENT"
          onChange={console.log}
          tagInputProps={{ wrap: true }}
          prefix={<AppStoreOutlined />}
          suffix={<InfoCircleOutlined style={{ marginRight: 8 }} />}
        />
      </div>
    </>
  )
}

```

### appearance.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性、无UI三种
 */
export const Appearance = () => {
  const [value, setValue] = React.useState<React.ReactText[]>(['0-0'])
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Appearance</h1>
      <div className="tree-select-appearance__wrap">
        <div>
          <h2>filled</h2>
          <CheckTreeSelect
            style={{ width: 240 }}
            data={data}
            value={value}
            clearable
            appearance="filled"
            onChange={(value, options) => {
              console.log('CheckTreeSelect onChange: ', value, options)
              setValue(value)
            }}
          />
        </div>

        <div>
          <h2>outline</h2>
          <CheckTreeSelect
            style={{ width: 240 }}
            data={data}
            value={value}
            clearable
            appearance="line"
            onChange={(value, options) => {
              console.log('CheckTreeSelect onChange: ', value, options)
              setValue(value)
            }}
          />
        </div>

        <div>
          <h2>unset</h2>
          <CheckTreeSelect
            data={data}
            value={value}
            clearable
            appearance="unset"
            // 取消下拉框匹配 input 触发器的宽度
            overlay={{ matchWidth: false }}
            onChange={(value, options) => {
              console.log('CheckTreeSelect onChange: ', value, options)
              setValue(value)
            }}
          />
        </div>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 基础用法
 * @desc 展示从全部备选项选出的部分选项
 */
export const Basic = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          disabled: true,
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Basic</h1>
      <div className="check-tree-select-basic__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          checkedMode="PARENT"
          onChange={console.log}
        />
      </div>
    </>
  )
}

```

### check-all.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 全选
 */
export const CheckAll = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>CheckAll</h1>
      <div className="check-tree-select-check-all__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          showCheckAll
          checkedMode="PARENT"
          onChange={console.log}
        />
      </div>
    </>
  )
}

```

### clearable.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 清空选中项
 */
export const Clearable = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Clearable</h1>
      <div className="tree-select-clearable__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          clearable
          data={data}
          onChange={(checkedIds, options) => {
            console.log('CheckTreeSelect onChange: ', checkedIds, options)
          }}
        />
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [value, setValue] = React.useState<React.ReactText[]>(['0-0'])
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          disabled: true,
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Controlled</h1>
      <div className="check-tree-select-controlled__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          clearable
          checkedMode="PARENT"
          value={value}
          onChange={(checkedIds) => {
            setValue(checkedIds)
          }}
        ></CheckTreeSelect>
      </div>
    </>
  )
}

```

### custom-render.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 自定义触发器
 */
export const CustomRender = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          disabled: true,
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Basic</h1>
      <div className="check-tree-select-custom-render__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          checkedMode="PARENT"
          onChange={console.log}
          customRender={(value) => {
            return (
              <Input value={value.map((v) => v.title).join(',')} readOnly placeholder="请选择" />
            )
          }}
        />
      </div>
    </>
  )
}

```

### default-expand-all.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 默认展开全部
 */
export const DefaultExpandAll = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>DefaultExpandAll</h1>
      <div className="tree-select-default-expand-all__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          defaultExpandAll
          onChange={(checkedIds, options) => {
            console.log('CheckTreeSelect onChange: ', checkedIds, options)
          }}
        />
      </div>
    </>
  )
}

```

### only-checked.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 查看已选
 */
export const OnlyChecked = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          disabled: true,
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Only Checked</h1>
      <div className="check-tree-select-only-checked__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          checkedMode="PARENT"
          onChange={console.log}
          showOnlyShowChecked
        />
      </div>
    </>
  )
}

```

### searchable.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 带搜索
 * @desc 选项数量较大，不熟悉数据的结构关系情况下，用搜索关键词的方式快速定位
 */
export const Searchable = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  // 注意 filterOption 是影响搜索渲染的，是完全受控的，useCallback 包裹可以减少无效的重渲染，提升性能
  const filterOptionMemo = React.useCallback((keyword: string, item: any) => {
    console.log(keyword, item)

    const match = (node: any) =>
      typeof node.title === 'string' && node.title.indexOf(keyword) !== -1

    const matchUp = (node: any) => {
      let found = match(node)
      const { children } = node

      if (children && !found) {
        found = children.some((item: any) => matchUp(item))
      }

      return found
    }

    return matchUp(item)
  }, [])

  const [keyword, setKeyword] = React.useState('小米')

  return (
    <>
      <h1>Searchable</h1>
      <div className="tree-select-searchable__wrap">
        <div style={{ fontSize: 16, fontWeight: 500, margin: '20px 0 10px 0' }}>
          highlight 仅高亮
        </div>
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          searchable
          searchMode="highlight"
          onChange={(checkedIds, options) => {
            console.log('CheckTreeSelect onChange: ', checkedIds, options)
          }}
        />

        <div style={{ fontSize: 16, fontWeight: 500, margin: '20px 0 10px 0' }}>
          filter 高亮并且过滤无关节点
        </div>

        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          searchable
          keyword={keyword}
          onSearch={setKeyword}
          searchMode="filter"
          onChange={(checkedIds, options) => {
            console.log('CheckTreeSelect onChange: ', checkedIds, options)
          }}
        />

        <div style={{ fontSize: 16, fontWeight: 500, margin: '20px 0 10px 0' }}>
          filterOption 自定义搜索策略
        </div>
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          searchable
          filterOption={filterOptionMemo}
          onChange={(checkedIds, options) => {
            console.log('CheckTreeSelect onChange: ', checkedIds, options)
          }}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          disabled: true,
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Size</h1>
      <div className="check-tree-select-size__wrap">
        <h2>sm</h2>
        <CheckTreeSelect
          style={{ width: 240 }}
          size="sm"
          data={data}
          checkedMode="PARENT"
          onChange={console.log}
        />
        <h2>md</h2>
        <CheckTreeSelect
          style={{ width: 240 }}
          size="md"
          data={data}
          checkedMode="PARENT"
          onChange={console.log}
        />
        <h2>lg</h2>
        <CheckTreeSelect
          style={{ width: 240 }}
          size="lg"
          data={data}
          checkedMode="PARENT"
          onChange={console.log}
        />
      </div>
    </>
  )
}

```

### tag-input-wrap.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 展示全部已选项
 * @desc 设置后，选中内容超出宽度时会换行展示
 */
export const TagInputWrap = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          disabled: true,
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>展示全部已选项</h1>
      <div className="check-tree-select-tag-input-wrap__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          checkedMode="PARENT"
          onChange={console.log}
          tagInputProps={{
            wrap: true,
          }}
        />
      </div>
    </>
  )
}

```

### uncontrolled.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 非受控
 */
export const Uncontrolled = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          disabled: true,
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Uncontrolled</h1>
      <div className="check-tree-select-uncontrolled__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          clearable
          defaultValue={['1-0']}
          data={data}
        ></CheckTreeSelect>
      </div>
    </>
  )
}

```

### virtual-list.stories.tsx

```typescript
import React from 'react'
import CheckTreeSelect from '@hi-ui/check-tree-select'

/**
 * @title 大数据
 */
export const VirtualList = () => {
  const [data] = React.useState(() => {
    // 模拟 10^4 个数据量
    function dig(path = '0', level) {
      const list: any = []
      for (let i = 0; i < 5; i += 1) {
        const id = `${path}-${i}`
        const treeNode = {
          title: id,
          id,
          children: [] as any[],
        }

        if (level > 0) {
          treeNode.children = dig(id, level - 1)
        }

        list.push(treeNode)
      }
      return list
    }

    const treeData = dig('0', 4)
    return treeData
  })

  return (
    <>
      <h1>virtualList</h1>
      <div className="check-tree-select-virtual-list__wrap">
        <CheckTreeSelect
          style={{ width: 240 }}
          data={data}
          checkedMode="PARENT"
          onChange={console.log}
          virtual
          height={260}
        />
      </div>
    </>
  )
}

```

## checkbox 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Checkbox from '@hi-ui/checkbox'

/**
 * @title 基础用法
 * @desc 展示所有备选项，数量不宜超出10个
 */
export const Basic = () => {
  return (
    <>
      <h1>Checkbox</h1>
      <div className="checkbox-basic__wrap">
        <Checkbox>复选框</Checkbox>
      </div>
    </>
  )
}

```

### check-all.stories.tsx

```typescript
import React from 'react'
import Checkbox from '@hi-ui/checkbox'

/**
 * @title 全选
 * @desc 一次操作选中所有选项
 */
export const CheckAll = () => {
  const [data] = React.useState([
    {
      title: '手机',
      id: 'Phone',
    },
    {
      title: '电脑',
      id: 'Computer',
    },
    {
      title: '智能',
      id: 'Intelli',
    },
    {
      title: '出行',
      id: 'Transfer',
    },
  ])
  const [selectedList, setSelectedList] = React.useState<React.ReactText[]>(['Phone'])

  return (
    <>
      <h1>全选操作</h1>
      <div
        className="checkbox-check-all__wrap"
        style={{ display: 'flex', gap: 12, flexDirection: 'column' }}
      >
        <Checkbox
          indeterminate={selectedList.length > 0 && selectedList.length < 4}
          checked={selectedList.length === 4}
          onChange={() => {
            setSelectedList((prev) => {
              return prev.length < 4 ? data.map(({ id }) => id) : []
            })
          }}
        >
          全选
        </Checkbox>
        <Checkbox.Group
          data={data}
          value={selectedList}
          onChange={(value) => {
            console.log(value)
            setSelectedList(value)
          }}
        />
      </div>
    </>
  )
}

```

### children.stories.tsx

```typescript
import React from 'react'
import Checkbox from '@hi-ui/checkbox'
import Grid from '@hi-ui/grid'

/**
 * @title 灵活布局
 * @desc Checkbox 与 Grid 组件一起使用，可以实现灵活的布局
 */
export const Children = () => {
  const { Row, Col } = Grid
  const CheckboxGroup = Checkbox.Group

  const [selectedList, setSelectedList] = React.useState<React.ReactText[]>([
    'Phone',
    'Intelligent',
  ])

  return (
    <>
      <h1>Children</h1>
      <div className="checkbox-children__wrap">
        <CheckboxGroup
          value={selectedList}
          style={{ width: '100%' }}
          onChange={(value) => {
            console.log(value)
            setSelectedList(value)
          }}
        >
          <Row>
            <Col span={8}>
              <Checkbox value="Phone">手机</Checkbox>
            </Col>
            <Col span={8}>
              <Checkbox value="Computer">电脑</Checkbox>
            </Col>
            <Col span={8}>
              <Checkbox value="Intelligent">智能</Checkbox>
            </Col>
          </Row>
          <Row>
            <Col span={8}>
              <Checkbox value="Transfer" onChange={console.log}>
                出行
              </Checkbox>
            </Col>
            <Col span={8}>
              <Checkbox value="ecological" onChange={console.log}>
                生态
              </Checkbox>
            </Col>
          </Row>
        </CheckboxGroup>
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import Checkbox from '@hi-ui/checkbox'
import Button from '@hi-ui/button'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [checked, setChecked] = React.useState(false)

  return (
    <>
      <h1>Controlled</h1>
      <div className="checkbox-controlled__wrap">
        <Button onClick={() => setChecked((prev) => !prev)}>Toggle</Button>
        <br />
        <Checkbox
          checked={checked}
          onChange={(evt) => {
            console.log('onChange', evt.target.checked)
            setChecked(evt.target.checked)
          }}
        >
          Checkbox
        </Checkbox>
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import Checkbox from '@hi-ui/checkbox'

/**
 * @title 禁用状态
 */
export const Disabled = () => {
  return (
    <>
      <h1>禁用态</h1>
      <div className="checkbox-disabled__wrap">
        <Checkbox disabled checked>
          复选框
        </Checkbox>
        <br />
        <br />
        <Checkbox disabled>复选框</Checkbox>
        <br />
        <br />
        <Checkbox disabled indeterminate>
          复选框
        </Checkbox>
      </div>
    </>
  )
}

```

### group.stories.tsx

```typescript
import React from 'react'
import Checkbox from '@hi-ui/checkbox'

/**
 * @title 成组
 */
export const Group = () => {
  const CheckboxGroup = Checkbox.Group

  const [data] = React.useState([
    {
      title: '手机',
      id: 'Phone',
    },
    {
      title: '电脑',
      id: 'Computer',
    },
    {
      title: '智能',
      id: 'Intelli',
    },
    {
      title: '出行',
      id: 'Transfer',
      disabled: true,
    },
  ])
  const [selectedList, setSelectedList] = React.useState<React.ReactText[]>(['Phone'])

  return (
    <>
      <h1>CheckboxGroup</h1>
      <div className="checkbox-group__wrap">
        <CheckboxGroup
          data={data}
          value={selectedList}
          onChange={(value) => {
            console.log(value)
            setSelectedList(value)
          }}
        />
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import React from 'react'
import Checkbox from '@hi-ui/checkbox'

/**
 * @title 垂直样式
 * @desc 选项的另一种布局形式，视页面空间选用
 */
export const Placement = () => {
  const CheckboxGroup = Checkbox.Group

  const [data] = React.useState([
    {
      title: '手机',
      id: 'Phone',
    },
    {
      title: '电脑',
      id: 'Computer',
    },
    {
      title: '智能',
      id: 'Intelli',
    },
    {
      title: '出行',
      id: 'Transfer',
      disabled: true,
    },
  ])
  const [selectedList, setSelectedList] = React.useState<React.ReactText[]>(['Phone'])

  return (
    <>
      <h1>垂直样式</h1>
      <div className="checkbox-placement__wrap">
        <CheckboxGroup
          data={data}
          placement="vertical"
          value={selectedList}
          onChange={(value) => {
            console.log(value)
            setSelectedList(value)
          }}
        />
      </div>
    </>
  )
}

```

## collapse 组件

### accordion.stories.tsx

```typescript
import React from 'react'
import Collapse from '@hi-ui/collapse'

/**
 * @title 手风琴模式
 * @desc 一次仅展开一个面板，有效减少垂直空间的占用
 */
export const Accordion = () => {
  return (
    <>
      <h1>Accordion</h1>
      <div className="collapse-accordion__wrap">
        <Collapse defaultActiveId={['2']} arrowPlacement="left" accordion>
          <Collapse.Panel title="小米手机" id="1" disabled>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="红米手机" id="2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="小米笔记本" id="3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米笔记本的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="小米 AI" id="4">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米 AI 的内容
            </div>
          </Collapse.Panel>
        </Collapse>
      </div>
    </>
  )
}

```

### arrow-placement.stories.tsx

```typescript
import React from 'react'
import Collapse from '@hi-ui/collapse'
import { PlusOutlined } from '@hi-ui/icons'

/**
 * @title 箭头位置
 * @desc 指定箭头放置方式
 */
export const ArrowPlacement = () => {
  return (
    <>
      <h1>ArrowPlacement</h1>
      <div className="collapse-arrow-placement__wrap">
        <Collapse defaultActiveId={['2']} arrowPlacement="right">
          <Collapse.Panel title="小米手机" id="1" disabled>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="红米手机" id="2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="小米笔记本" id="3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米笔记本的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel
            title="小米 AI"
            id="4"
            extra={<PlusOutlined style={{ marginRight: 8 }} />}
          >
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米 AI 的内容
            </div>
          </Collapse.Panel>
        </Collapse>
      </div>
    </>
  )
}

```

### arrow-render.stories.tsx

```typescript
import React from 'react'
import Collapse from '@hi-ui/collapse'
import { FolderFilled, FolderOpenFilled } from '@hi-ui/icons'

/**
 * @title 自定义箭头
 */
export const ArrowRender = () => {
  const [activeId, setActiveId] = React.useState<React.ReactText[]>(['2'])

  return (
    <>
      <h1>ArrowRender</h1>
      <div className="collapse-arrow-render__wrap">
        <Collapse
          arrowPlacement="left"
          activeId={activeId}
          onChange={setActiveId}
          arrowRender={(expanded) => {
            return (
              <span style={{ marginRight: 8, color: '#fab007', fontSize: 16 }}>
                {expanded ? <FolderFilled /> : <FolderOpenFilled />}
              </span>
            )
          }}
        >
          <Collapse.Panel title="小米手机" id="1" disabled>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="红米手机" id="2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="小米笔记本" id="3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米笔记本的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="小米 AI" id="4">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米 AI 的内容
            </div>
          </Collapse.Panel>
        </Collapse>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Collapse from '@hi-ui/collapse'

/**
 * @title 基础用法
 * @desc 可以同时展开多个面板，对垂直空间没有特别限制
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="collapse-basic__wrap">
        <Collapse defaultActiveId={['2', '3']} arrowPlacement="left">
          <Collapse.Panel title="小米手机" id="1" disabled>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="红米手机" id="2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="小米笔记本" id="3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米笔记本的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="小米 AI" id="4">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米 AI 的内容
            </div>
          </Collapse.Panel>
        </Collapse>
      </div>
    </>
  )
}

```

### no-border.stories.tsx

```typescript
import React from 'react'
import Collapse from '@hi-ui/collapse'

/**
 * @title 带边框
 */
export const bordered = () => {
  return (
    <>
      <h1>Bordered</h1>
      <div
        className="collapse-bordered__wrap"
        style={{
          backgroundColor: '#F5F7FA',
          padding: 24,
        }}
      >
        <Collapse defaultActiveId={['2']} arrowPlacement="left" bordered={false}>
          <Collapse.Panel title="小米手机" id="1" disabled>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="红米手机" id="2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="小米笔记本" id="3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米笔记本的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="小米 AI" id="4">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是小米 AI 的内容
            </div>
          </Collapse.Panel>
        </Collapse>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Collapse from '@hi-ui/collapse'

/**
 * @title 设置头部大小
 */
export const Size = () => {
  return (
    <>
      <h1>Size</h1>
      <div className="collapse-size__wrap">
        <h2>小尺寸</h2>
        <Collapse size="sm">
          <Collapse.Panel title="小米手机" id="2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="红米手机" id="3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
        </Collapse>
        <h2>常规</h2>
        <Collapse size="md">
          <Collapse.Panel title="小米手机" id="1">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="红米手机" id="2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
        </Collapse>
        <h2>大尺寸</h2>
        <Collapse size="lg">
          <Collapse.Panel title="小米手机" id="2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
          <Collapse.Panel title="红米手机" id="3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是红米手机的内容
            </div>
          </Collapse.Panel>
        </Collapse>
      </div>
    </>
  )
}

```

### title.stories.tsx

```typescript
import React from 'react'
import Collapse from '@hi-ui/collapse'
import { TabList } from '@hi-ui/tabs'

/**
 * @title 设置标题内容
 */
export const Title = () => {
  const [xiaomiTabList] = React.useState([
    { tabId: '0', tabTitle: '小米10' },
    { tabId: '1', tabTitle: '小米11' },
    { tabId: '2', tabTitle: '小米12' },
  ])

  const [hongmiTabList] = React.useState([
    { tabId: '0', tabTitle: '红米2' },
    { tabId: '1', tabTitle: '红米note' },
    { tabId: '2', tabTitle: '红米note2' },
  ])

  const [xiaomiActiveId, setXiaomiActiveId] = React.useState<React.ReactText>('0')
  const [hongmiActiveId, setHongmiActiveId] = React.useState<React.ReactText>('0')

  return (
    <>
      <h1>Title</h1>
      <div className="collapse-title__wrap">
        <Collapse defaultActiveId={['1']}>
          <Collapse.Panel
            title={
              <TabList
                style={{ margin: '-14px 0 -14px -20px' }}
                data={xiaomiTabList}
                onClick={(evt) => {
                  evt.stopPropagation()
                }}
                activeId={xiaomiActiveId}
                onChange={setXiaomiActiveId}
              />
            }
            id="1"
          >
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是{xiaomiTabList.find((item) => item.tabId === xiaomiActiveId)?.tabTitle}
            </div>
          </Collapse.Panel>
          <Collapse.Panel
            title={
              <TabList
                style={{ margin: '-14px 0 -14px -20px' }}
                data={hongmiTabList}
                onClick={(evt) => {
                  evt.stopPropagation()
                }}
                activeId={hongmiActiveId}
                onChange={setHongmiActiveId}
              />
            }
            id="12"
          >
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              我是{hongmiTabList.find((item) => item.tabId === hongmiActiveId)?.tabTitle}
            </div>
          </Collapse.Panel>
        </Collapse>
      </div>
    </>
  )
}

```

## counter 组件

### Wheel.stories.tsx

```typescript
import React from 'react'
import Counter from '@hi-ui/counter'

/**
 * @title 滚轮滑动
 */
export const Wheel = () => {
  return (
    <>
      <h1>Wheel</h1>
      <div className="counter-wheel__wrap">
        <Counter
          step={10}
          changeOnWheel
          defaultValue={0}
          min={1}
          onChange={(v) => console.log('onChange', v)}
        />
      </div>
    </>
  )
}

```

### appearance.stories.tsx

```typescript
import React from 'react'
import Counter from '@hi-ui/counter'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性两种
 */
export const Appearance = () => {
  return (
    <>
      <h1>Appearance</h1>
      <div>
        <h2>Line 线性</h2>
        <div style={{ display: 'flex', gap: 12, flexDirection: 'column' }}>
          <Counter appearance={'line'} />
          <Counter appearance={'line'} max={2} min={0} defaultValue={5} />
        </div>

        <h2>Filled 面性</h2>
        <div style={{ display: 'flex', gap: 12, flexDirection: 'column' }}>
          <Counter appearance={'filled'} />
          <Counter appearance={'filled'} max={2} min={0} defaultValue={5} />
        </div>
      </div>
    </>
  )
}

```

### auto-focus.stories.tsx

```typescript
import React from 'react'
import Counter from '@hi-ui/counter'

/**
 * @title 自动聚焦
 */
export const AutoFocus = () => {
  return (
    <>
      <h1>AutoFocus</h1>
      <div className="counter-auto-focus__wrap">
        <Counter autoFocus defaultValue={1} min={1} onChange={(v) => console.log('onChange', v)} />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Counter from '@hi-ui/counter'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Counter</h1>
      <div className="counter-basic__wrap">
        <Counter defaultValue={0} onChange={(v) => console.log('onChange', v)} />
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import Counter from '@hi-ui/counter'
import Button from '@hi-ui/button'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [current, setCurrent] = React.useState<number | null>(1)
  return (
    <>
      <h1>Controlled</h1>
      <div className="counter-controlled__wrap">
        <Counter
          value={current}
          min={1}
          onChange={(v) => {
            console.log('onChange', v)
            setCurrent(v)
          }}
        />

        <br />
        <br />
        <Button onClick={() => setCurrent(5)}>更新为 5</Button>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Counter from '@hi-ui/counter'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>Counter size</h1>
      <div style={{ display: 'flex', gap: 160 }}>
        <div style={{ display: 'flex', gap: 12, flexDirection: 'column' }}>
          <Counter size={'sm'} />
          <Counter size="md" />
          <Counter size={'lg'} />
        </div>

        <div style={{ display: 'flex', gap: 12, flexDirection: 'column' }}>
          <Counter size={'sm'} appearance={'filled'} />
          <Counter size="md" appearance={'filled'} />
          <Counter size={'lg'} appearance={'filled'} />
        </div>
      </div>
    </>
  )
}

```

### step.stories.tsx

```typescript
import React from 'react'
import Counter from '@hi-ui/counter'

/**
 * @title 自定义步长
 */
export const Step = () => {
  return (
    <>
      <h1>Step</h1>
      <div className="counter-step__wrap">
        <Counter step={0.1} defaultValue={0} min={1} onChange={(v) => console.log('onChange', v)} />
      </div>
    </>
  )
}

```

## date-picker 组件

### addon.stories.tsx

```typescript
import React from 'react'
import DatePicker from '@hi-ui/date-picker'
import { AppStoreOutlined } from '@hi-ui/icons'

/**
 * @title 前内置元素
 */
export const Addon = () => {
  return (
    <div className="date-picker-addon__wrap">
      <h2>Addon</h2>
      <DatePicker
        style={{ width: 240 }}
        onChange={(date, dateStr) => {
          console.log('onChange', date, dateStr)
        }}
        onSelect={console.log}
        prefix={<AppStoreOutlined />}
      />
    </div>
  )
}

```

### appearance.stories.tsx

```typescript
import React from 'react'
import DatePicker from '@hi-ui/date-picker'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性两种
 */
export const Appearance = () => {
  return (
    <>
      <h1>Appearance</h1>
      <div className="date-picker-appearance__wrap">
        <h2>Line</h2>
        <DatePicker
          style={{ width: 240 }}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
        <h2>filled</h2>
        <DatePicker
          style={{ width: 240 }}
          appearance={'filled'}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
        <h2>unset</h2>
        <DatePicker
          appearance={'unset'}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React, { useState } from 'react'
import DatePicker from '@hi-ui/date-picker'

/**
 * @title 基础用法
 * @desc 以天为粒度，展示“YYYY-MM-DD”
 */
export const Basic = () => {
  const [controlledValue, setControlledValue] = useState(new Date())
  return (
    <>
      <h1>日期</h1>
      <div className="date-picker-basic__wrap">
        <h2>基础</h2>
        <DatePicker
          style={{ width: 240 }}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          onSelect={console.log}
        />

        <h2>带默认值</h2>
        <DatePicker
          style={{ width: 240 }}
          defaultValue={new Date()}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />

        <h2>受控</h2>
        <DatePicker
          style={{ width: 240 }}
          value={controlledValue}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
            setControlledValue(date as Date)
          }}
        />

        <h2>禁用</h2>
        <DatePicker
          style={{ width: 240 }}
          disabled
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />

        <h2>限制范围</h2>
        <DatePicker
          style={{ width: 240 }}
          minDate={new Date()}
          maxDate={new Date(new Date().getTime() + 30 * 24 * 60 * 60 * 1000)}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
      </div>
    </>
  )
}

```

### cell-render.stories.tsx

```typescript
import React from 'react'
import moment from 'moment'
import DatePicker from '@hi-ui/date-picker'

/**
 * @title 自定义单元格内容
 */
export const CellRender = () => {
  return (
    <>
      <h1>CellRender</h1>
      <div className="date-picker-ymw__wrap">
        <h2>年份</h2>
        <DatePicker
          style={{ width: 238 }}
          type="year"
          cellRender={(info) => {
            const { type, text } = info

            return type === 'today' ? <strong>{text}</strong> : text
          }}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
        <h2>月份</h2>
        <DatePicker
          style={{ width: 238 }}
          type="month"
          cellRender={(info) => {
            const { type, text } = info
            return type === 'today' ? <strong>{text}</strong> : text
          }}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />

        <h2>周</h2>
        <DatePicker
          style={{ width: 238 }}
          type="week"
          defaultValue={new Date()}
          cellRender={(info) => {
            const { value, weekNum } = info

            return weekNum ? weekNum + 'W' : value
          }}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
        <h2>周范围</h2>
        <DatePicker
          style={{ width: 560 }}
          type="weekrange"
          defaultValue={[new Date(), new Date()]}
          strideSelectMode="fixed"
          format={(value) => {
            // console.log('format', value)

            const lastDay = value.clone().endOf('month').date()
            const startOfWeek = value.clone().startOf('week')
            const endOfWeek = value.clone().endOf('week')
            const week = value.clone().week()
            const weekYear = value.clone().weekYear()

            // 如果当前日期是当月第一天或者或者小于周一，并且周一不是当月第一天，则该周视为 B 周
            if (
              (value.date() === 1 || startOfWeek.date() > value.date()) &&
              startOfWeek.date() !== 1
            ) {
              return `${weekYear}-${week}B`
            }

            // 如果当前日期是当月最后一天或者大于周日，并且周日不是最后一天，则该周视为 A 周
            if (
              (value.date() === lastDay || value.date() > endOfWeek.date()) &&
              endOfWeek.date() !== lastDay
            ) {
              return `${weekYear}-${week}A`
            }

            return `${weekYear}-${week}`
          }}
          // 自定义渲染出 AB 周，逻辑：
          // 在当前月周选择面板下，如果当月第一天位于第一行并且不是周一，则该周视为B周
          // 如果当前月最后一天位于最后一行并且不是周日，则该周视为A周
          cellRender={(cellInfo) => {
            // console.log('cellInfo', cellInfo)

            const { value, weekNum } = cellInfo

            if (weekNum) {
              // weekStartDate 周一日期
              // renderDate 当前月日期
              const { weekStartDate, renderDate } = cellInfo
              // 当前周最后一天
              const weekEndDate = weekStartDate?.clone().add(6, 'day')

              if (
                weekEndDate &&
                renderDate &&
                (weekEndDate?.month() > renderDate?.month() ||
                  weekEndDate?.year() > renderDate?.year()) &&
                weekStartDate?.month() === renderDate?.month()
              ) {
                return weekNum + 'A'
              }

              if (
                weekStartDate &&
                renderDate &&
                (weekStartDate?.month() < renderDate?.month() ||
                  weekStartDate?.year() < renderDate?.year()) &&
                weekEndDate?.month() === renderDate?.month()
              ) {
                return weekNum + 'B'
              }

              return weekNum
            } else {
              return value
            }
          }}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)

            const _date = date as Date[]
            const start = moment(_date?.[0])
            const end = moment(_date?.[1])
            const lastDay = end.clone().endOf('month').date()

            // 如果开始日期是当月第一天并且不是周一，则该周视为 B 周
            if (start.date() === 1 && start.clone().startOf('week').date() !== 1) {
              console.log('start week', dateStr?.[0] + 'B')
            }

            // 如果当前日期是当月最后一天并且不是周末，则该周视为 A 周
            if (end.date() === lastDay && end.clone().endOf('week').date() !== lastDay) {
              console.log('end week', dateStr?.[1] + 'A')
            }
          }}
        />
      </div>
    </>
  )
}

```

### custom-render.stories.tsx

```typescript
import React from 'react'
import DatePicker from '@hi-ui/date-picker'
import Input from '@hi-ui/input'

/**
 * @title 自定义触发器
 */
export const CustomRender = () => {
  return (
    <>
      <h1>自定义触发器</h1>
      <div className="date-picker-custom-render__wrap">
        <h2>日期</h2>
        <DatePicker
          style={{ width: 240 }}
          defaultValue={new Date()}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          onSelect={console.log}
          customRender={(data) => {
            const date = new Date(data[0] ?? new Date())
            const year = date.getFullYear()
            const month = (date.getMonth() + 1).toString().padStart(2, '0')
            const day = date.getDate().toString().padStart(2, '0')
            const formattedDate = `${year}-${month}-${day}`
            return <Input value={formattedDate} readOnly placeholder="请选择" />
          }}
        />
        <h2>日期范围</h2>
        <DatePicker
          style={{ width: 240 }}
          type="daterange"
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          defaultValue={[new Date(), new Date()]}
          customRender={(data) => {
            const date1 = new Date(data[0] ?? new Date())
            const date2 = new Date(data[1] ?? new Date())
            const year1 = date1.getFullYear()
            const year2 = date2.getFullYear()
            const month1 = (date1.getMonth() + 1).toString().padStart(2, '0')
            const month2 = (date2.getMonth() + 1).toString().padStart(2, '0')
            const day1 = date1.getDate().toString().padStart(2, '0')
            const day2 = date2.getDate().toString().padStart(2, '0')
            const formattedDateTime1 = `${year1}-${month1}-${day1}`
            const formattedDateTime2 = `${year2}-${month2}-${day2}`

            return (
              <Input
                value={`${formattedDateTime1} - ${formattedDateTime2}`}
                readOnly
                placeholder="请选择"
              />
            )
          }}
        />
      </div>
    </>
  )
}

```

### date-time.stories.tsx

```typescript
import React from 'react'
import DatePicker from '@hi-ui/date-picker'

/**
 * @title 日期时间
 * @desc 以时间点为粒度，展示“YYYY-MM-DD HH:mm:ss”
 */
export const DateTime = () => {
  return (
    <>
      <h1>日期时间</h1>
      <div className="date-time__wrap">
        <DatePicker
          defaultValue={new Date()}
          showTime={true}
          disabledHours={[2, 3, 4, 5, 6]}
          format="YYYY-MM-DD HH:mm:ss"
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
      </div>
    </>
  )
}

```

### footer-render.stories.tsx

```typescript
import React from 'react'
import DatePicker from '@hi-ui/date-picker'
import Button from '@hi-ui/button'

/**
 * @title 自定义渲染页脚
 */
export const FooterRender = () => {
  return (
    <>
      <h1>FooterRender</h1>
      <div className="date-picker-footer-render__wrap">
        <DatePicker
          style={{ width: 240 }}
          type="daterange"
          showTime
          footerRender={(sureActionContent) => (
            <div
              style={{
                display: 'flex',
                justifyContent: 'space-between',
                alignItems: 'center',
                width: '100%',
              }}
            >
              <Button type="secondary" appearance="link">
                自定义操作
              </Button>
              {sureActionContent}
            </div>
          )}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          onSelect={console.log}
        />
      </div>
    </>
  )
}

```

### lunar.stories.tsx

```typescript
import React, { useState } from 'react'
import DatePicker from '@hi-ui/date-picker'
import DayJs from 'dayjs'

/**
 * @title 日历面板
 */
export const Lunar = () => {
  const [customValue, setCustomValue] = useState(new Date('2020/4/8'))

  return (
    <>
      <h1>日历面板</h1>
      <div className="lunar__wrap">
        <h2>预置农历</h2>
        <DatePicker
          style={{ width: 338 }}
          altCalendarPreset="zh-CN"
          dateMarkPreset="zh-CN"
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
        <h2>自定义日期信息</h2>
        <DatePicker
          style={{ width: 338 }}
          value={customValue}
          altCalendar={[
            {
              date: '2020/4/8',
              content: '十周年',
              highlighted: true,
            },
          ]}
          dateMarkRender={(currentDate, today) => {
            // const date = DatePicker.format(currentDate, 'yyyy/M/D')
            // const yesterday = DatePicker.format(today - 86400000, 'yyyy/M/D')
            // const currentday = DatePicker.format(customValue, 'yyyy/M/D')

            const date = DayJs(currentDate).format('yyyy/M/D')
            const yesterday = DayJs(today - 86400000).format('yyyy/M/D')

            if (date === '2020/4/8') {
              return (
                <span style={{ color: '#ff6900', transform: 'scale(0.6)', fontWeight: 'bold' }}>
                  米
                </span>
              )
            } else if (date === yesterday) {
              return (
                <span style={{ color: '#63bbd0', transform: 'scale(0.6)', fontWeight: 'bold' }}>
                  昨
                </span>
              )
            } else {
              return ''
            }
          }}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
            setCustomValue(date as Date)
          }}
        />
      </div>
    </>
  )
}

```

### need-confirm.stories.tsx

```typescript
import React from 'react'
import DatePicker from '@hi-ui/date-picker'

/**
 * @title 选择确认
 * @desc 为 <code>true</code> 时，只有点击确认按钮才会触发值变化，暂不支持范围选择
 */
export const NeedConfirm = () => {
  return (
    <>
      <h1>使用确认按钮</h1>
      <div className="need-confirm__wrap">
        <h2>日期选择</h2>
        <DatePicker
          style={{ width: 240 }}
          needConfirm
          onChange={(date, dateStr) => console.log('onChange', date, dateStr)}
          onSelect={(date) => console.log('onSelect', date)}
          onConfirm={(date) => console.log('onConfirm', date)}
        />
        <h2>日期时间选择</h2>
        <DatePicker
          style={{ width: 240 }}
          defaultValue={new Date()}
          showTime
          needConfirm
          disabledHours={[2, 3, 4, 5, 6]}
          format="YYYY-MM-DD HH:mm:ss"
          onChange={(date, dateStr) => console.log('onChange', date, dateStr)}
          onSelect={(date) => console.log('onSelect', date)}
          onConfirm={(date) => console.log('onConfirm', date)}
        />
      </div>
    </>
  )
}

```

### range.stories.tsx

```typescript
import React, { useState } from 'react'
import DatePicker from '@hi-ui/date-picker'
import DayJs from 'dayjs'

/**
 * @title 范围
 * @desc 以天、周、月、季度、年等粒度展示一个时间的范围
 */
export const Range = () => {
  const [dynamicSelectedValue, setDynamicSelectedValue] = useState<any>('')
  return (
    <>
      <h1>范围</h1>
      <div className="range__wrap">
        <h2>日期</h2>
        <DatePicker
          type="daterange"
          style={{ width: 480 }}
          defaultValue={[new Date(), new Date()]}
          format="YYYY-MM-DD"
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          onSelect={console.log}
          disabledDate={(val) => {
            const tomorrow = DayJs(new Date()).isBefore(DayJs(val))
            if (tomorrow) return true

            if (dynamicSelectedValue) {
              const startTime = DayJs(dynamicSelectedValue).startOf('month').valueOf()
              const endTime = DayJs(dynamicSelectedValue).endOf('month').valueOf()

              if (DayJs(val).isBefore(startTime)) return true
              if (DayJs(val).isAfter(endTime)) return true
            }
            return false
          }}
        />

        <h2>年份</h2>
        <DatePicker
          style={{ width: 480 }}
          type="yearrange"
          defaultValue={[new Date(), new Date()]}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          onSelect={console.log}
        />

        <h2>季度</h2>
        <DatePicker
          style={{ width: 480 }}
          type="quarterrange"
          defaultValue={[new Date(), new Date()]}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          onSelect={console.log}
        />

        <h2>月份</h2>
        <DatePicker
          style={{ width: 480 }}
          type="monthrange"
          defaultValue={[new Date(), new Date()]}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          onSelect={console.log}
        />

        <h2>周</h2>
        {/* 如果遇到周范围选择选值问题，尝试手动引入 import 'moment/locale/zh-cn' */}
        <DatePicker
          style={{ width: 480 }}
          type="weekrange"
          defaultValue={[new Date(), new Date()]}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          onSelect={console.log}
        />

        <h2>日期时间范围</h2>
        <DatePicker
          style={{ width: 420 }}
          type="daterange"
          showTime
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          onSelect={console.log}
        />

        <h2>时间段快速选择</h2>
        <DatePicker
          style={{ width: 372 }}
          type="timeperiod"
          onSelect={console.log}
          timeInterval={30}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />

        <h2>动态限制日期范围</h2>
        <DatePicker
          style={{ width: 480 }}
          type="daterange"
          disabledDate={(val) => {
            if (dynamicSelectedValue) {
              const timestampCurrent = new Date(val).getTime()
              const timestampSelect = new Date(dynamicSelectedValue).getTime()
              const range = 7 * 24 * 60 * 60 * 1000
              return !(
                timestampSelect - range < timestampCurrent &&
                timestampCurrent < timestampSelect + range
              )
            }
            return false
          }}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
          onSelect={(val, isCompleted) => {
            console.log(val, isCompleted)
            setDynamicSelectedValue(isCompleted ? '' : val)
          }}
        />
      </div>
    </>
  )
}

```

### shortcut.stories.tsx

```typescript
import React from 'react'
import DatePicker from '@hi-ui/date-picker'

/**
 * @title 带快捷选项
 * @desc 将常用的日期或时间提炼成快捷项，节省操作成本
 */
export const Shortcut = () => {
  return (
    <>
      <h1>带快捷选项</h1>
      <div className="shortcut__wrap">
        <h2>内置</h2>
        <DatePicker
          style={{ width: 565 }}
          type="daterange"
          shortcuts={['近一周', '近一月', '近三月', '近一年']}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
        <h2>自定义选择范围</h2>
        <DatePicker
          style={{ width: 565 }}
          type="daterange"
          shortcuts={[
            {
              title: '近十天',
              range: [new Date().getTime() - 10 * 86400000, new Date()],
            },
            {
              title: '近二十天',
              range: [new Date().getTime() - 20 * 86400000, new Date()],
            },
            {
              title: '近三十天',
              range: [new Date().getTime() - 30 * 86400000, new Date()],
            },
          ]}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import DatePicker from '@hi-ui/date-picker'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>Size</h1>
      <div className="date-picker-size__wrap">
        <h2>sm</h2>
        <DatePicker
          style={{ width: 240 }}
          size={'sm'}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
        <h2>md</h2>
        <DatePicker
          style={{ width: 240 }}
          size={'md'}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
        <h2>lg</h2>
        <DatePicker
          style={{ width: 240 }}
          size={'lg'}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
      </div>
    </>
  )
}

```

### year-month-week.stories.tsx

```typescript
import React from 'react'
import DatePicker from '@hi-ui/date-picker'

/**
 * @title 年份 / 季度 / 月份 / 周
 * @desc 以年份 / 季度 / 月份 / 周为展示粒度
 */
export const YearMonthWeek = () => {
  return (
    <>
      <h1>年份 / 季度 / 月份 / 周</h1>
      <div className="date-picker-ymw__wrap">
        <h2>年份</h2>
        <DatePicker
          style={{ width: 238 }}
          type="year"
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />

        <h2>季度</h2>
        <DatePicker
          style={{ width: 238 }}
          type="quarter"
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />

        <h2>月份</h2>
        <DatePicker
          style={{ width: 238 }}
          type="month"
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />

        <h2>周</h2>
        {/* 如果遇到周选择选值问题，尝试手动引入 import 'moment/locale/zh-cn' */}
        <DatePicker
          style={{ width: 238 }}
          type="week"
          defaultValue={new Date()}
          weekOffset={0}
          onChange={(date, dateStr) => {
            console.log('onChange', date, dateStr)
          }}
        />
      </div>
    </>
  )
}

```

## descriptions 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'

/**
 * @title 基础用法
 * @desc Descriptions 结合 Descriptions.Item 完成描述列表的动态配置
 */
export const Basic = () => {
  return (
    <>
      <h1>基础用法</h1>
      <div className="descriptions-basic__wrap">
        <Descriptions>
          <Descriptions.Item label="名字">张三</Descriptions.Item>
          <Descriptions.Item label="Phone">15311969622</Descriptions.Item>
          <Descriptions.Item label="Address">北京天安门</Descriptions.Item>
          <Descriptions.Item label="Money1">100000000</Descriptions.Item>
          <Descriptions.Item label="Money2">100000022220</Descriptions.Item>
          <Descriptions.Item label="Money3">
            <div>test</div>
          </Descriptions.Item>
          <Descriptions.Item label="Money4">1000000222201133</Descriptions.Item>
        </Descriptions>
      </div>
    </>
  )
}

```

### bordered.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'

/**
 * @title 带边框的
 * @desc 设置 `appearance` 控制描述列表组件的展现形态
 */
export const Bordered = () => {
  return (
    <>
      <h1>带边框的</h1>
      <div className="descriptions-basic__wrap">
        <Descriptions appearance="table">
          <Descriptions.Item label="名字">张三</Descriptions.Item>
          <Descriptions.Item label="Phone">15311969622</Descriptions.Item>
          <Descriptions.Item label="Address">北京天安门</Descriptions.Item>
          <Descriptions.Item label="Money1">100000000</Descriptions.Item>
          <Descriptions.Item label="Money2" colSpan={2}>
            100000022220
          </Descriptions.Item>
          <Descriptions.Item label="Money3">
            <div>test</div>
          </Descriptions.Item>
          <Descriptions.Item label="Money4">1000000222201133</Descriptions.Item>
        </Descriptions>
      </div>
    </>
  )
}

```

### col.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'

/**
 * @title 自定义列数
 * @desc 支持一栏至四栏平均分布
 */
export const Col = () => {
  return (
    <>
      <h1>自定义列数</h1>
      <div className="descriptions-basic__wrap">
        <Descriptions column={2}>
          <Descriptions.Item label="名字">张三</Descriptions.Item>
          <Descriptions.Item label="Phone">15311969622</Descriptions.Item>
          <Descriptions.Item label="Address">北京天安门</Descriptions.Item>
          <Descriptions.Item label="Money1">100000000</Descriptions.Item>
          <Descriptions.Item label="Money2">100000022220</Descriptions.Item>
          <Descriptions.Item label="Money3">
            <div>test</div>
          </Descriptions.Item>
          <Descriptions.Item label="Money4">1000000222201133</Descriptions.Item>
        </Descriptions>
      </div>
    </>
  )
}

```

### config.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'

/**
 * @title 通过Data 数组配置
 * @desc Descriptions 通过 data api 描述 Item 信息
 */
export const Config = () => {
  const data = [
    {
      label: '满江红',
      value: '怒发冲冠',
    },
    {
      label: '靖康耻，犹未雪',
      value: '臣子恨，何时灭',
    },
    {
      label: '驾长车',
      value: '踏破贺兰山缺',
    },
    {
      label: '壮志饥餐胡虏肉',
      value: '笑谈渴饮匈奴血',
    },
    {
      label: '待从头',
      value: '收拾旧山河',
    },
    {
      label: '朝天阙',
      value: '结束',
    },
  ]

  return (
    <>
      <h1>使用JS配置</h1>
      <div className="descriptions-basic__wrap">
        <Descriptions data={data} />
      </div>
    </>
  )
}

```

### content-position.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'
import Preview from '@hi-ui/preview'
import { JpgColorful } from '@hi-ui/icons'

/**
 * @title 设置标签和内容对齐方式
 */
export const ContentPosition = () => {
  const [images] = React.useState([
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_1.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_2.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_3.png',
  ])
  const [visible, setVisible] = React.useState(false)
  const [current, setCurrent] = React.useState(0)

  return (
    <>
      <h1>ContentPosition</h1>
      <div className="descriptions-content-position__wrap">
        <h2>md</h2>
        <Descriptions contentPosition="center" columnGap={24}>
          <Descriptions.Item label="机构类型" labelWidth={84}>
            第三方网点
          </Descriptions.Item>
          <Descriptions.Item label="主子站类型" labelWidth={84}>
            主站
          </Descriptions.Item>
          <Descriptions.Item label="机构状态" labelWidth={84}>
            有效
          </Descriptions.Item>
          <Descriptions.Item label="机构名称" labelWidth={84}>
            某某有限公司
          </Descriptions.Item>
          <Descriptions.Item label="是否自营" labelWidth={84}>
            是
          </Descriptions.Item>
          <Descriptions.Item label="实体门店招牌" labelWidth={84}>
            <div style={{ display: 'flex', alignItems: 'center' }}>
              <JpgColorful style={{ fontSize: 16 }} />
              <a href="#" style={{ textDecoration: 'none', color: '#4a9eff' }}>
                主站.jpg
              </a>
            </div>
          </Descriptions.Item>
          <Descriptions.Item label="备注信息" labelWidth={84}>
            备注内容可能会非常长备注内容可能会非常长备注内容可能会非常长
          </Descriptions.Item>
          <Descriptions.Item label="维度名称常规" labelWidth={84}>
            <img
              src={images[0]}
              style={{ width: 40, height: 40, borderRadius: 2, cursor: 'pointer', marginRight: 6 }}
              onClick={() => {
                setCurrent(0)
                setVisible(true)
              }}
            />
            <img
              src={images[1]}
              style={{ width: 40, height: 40, borderRadius: 2, cursor: 'pointer', marginRight: 6 }}
              onClick={() => {
                setCurrent(1)
                setVisible(true)
              }}
            />
            <img
              src={images[2]}
              style={{ width: 40, height: 40, borderRadius: 2, cursor: 'pointer' }}
              onClick={() => {
                setCurrent(2)
                setVisible(true)
              }}
            />
          </Descriptions.Item>
        </Descriptions>

        <Preview
          title={`${current + 1}/${images.length}`}
          src={images}
          current={current}
          onPreviewChange={setCurrent}
          visible={visible}
          onClose={() => {
            setVisible(false)
          }}
        />
      </div>
    </>
  )
}

```

### ellipsis.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'
import EllipsisTooltip from '@hi-ui/ellipsis-tooltip'

/**
 * @title 超出展示省略号
 * @desc Descriptions 配合 EllipsisTooltip 组件，形成超出展示省略号功能
 */
export const Ellipsis = () => {
  const data = [
    {
      // 超出宽度限制才会展示，没有超出不展示
      label: <EllipsisTooltip>满江红</EllipsisTooltip>,
      value: '怒发冲冠',
    },
    {
      label: <EllipsisTooltip>靖康耻，犹未雪。</EllipsisTooltip>,
      labelWidth: 100,
      value: '臣子恨，何时灭。臣子恨，何时灭。',
    },
    {
      label: '驾长车',
      value: '踏破贺兰山缺',
    },
    {
      label: '壮志饥餐胡虏肉',
      value: '笑谈渴饮匈奴血',
    },
    {
      label: '待从头',
      labelWidth: 100,
      value: <EllipsisTooltip>收拾旧山河，收拾旧山河，收拾旧山河，收拾旧山河</EllipsisTooltip>,
    },
    {
      label: '朝天阙',
      value: '结束',
    },
  ]

  return (
    <>
      <h1>超出省略号</h1>
      <div className="descriptions-basic__wrap">
        <Descriptions data={data} />
      </div>
    </>
  )
}

```

### label-placement.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'

/**
 * @title label对齐方式
 * @desc 通过设置 `labelPlacement` 控制 label 的对齐方式
 */
export const LabelPlacement = () => {
  return (
    <>
      <h1>label对齐方式</h1>
      <div className="descriptions-basic__wrap">
        <h2>默认外形：右对齐</h2>
        <Descriptions labelPlacement="right">
          <Descriptions.Item label="名字">张三</Descriptions.Item>
          <Descriptions.Item label="Phone">15311969622</Descriptions.Item>
          <Descriptions.Item label="Address">北京天安门</Descriptions.Item>
          <Descriptions.Item label="Money1">100000000</Descriptions.Item>
          <Descriptions.Item label="Money2" colSpan={2}>
            100000022220
          </Descriptions.Item>
          <Descriptions.Item label="Money3">
            <div>test</div>
          </Descriptions.Item>
          <Descriptions.Item label="Money4">1000000222201133</Descriptions.Item>
        </Descriptions>

        <h2>表格外形：右对齐</h2>
        <Descriptions appearance="table" labelPlacement="right">
          <Descriptions.Item label="名字">张三</Descriptions.Item>
          <Descriptions.Item label="Phone">15311969622</Descriptions.Item>
          <Descriptions.Item label="Address">北京天安门</Descriptions.Item>
          <Descriptions.Item label="Money1">100000000</Descriptions.Item>
          <Descriptions.Item label="Money2">100000022220</Descriptions.Item>
          <Descriptions.Item label="Money3">
            <div>test</div>
          </Descriptions.Item>
          <Descriptions.Item label="Money4">1000000222201133</Descriptions.Item>
        </Descriptions>
      </div>
    </>
  )
}

```

### label-width.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'

/**
 * @title 固定label宽度
 * @desc 根据实际情况配置label宽度，一个页面中label宽度应该保持一致
 */
export const LabelWidth = () => {
  return (
    <>
      <h1>label设置固定宽度</h1>
      <div className="descriptions-basic__wrap">
        <Descriptions labelPlacement="right">
          <Descriptions.Item label="名字" labelWidth="100px">
            张三
          </Descriptions.Item>
          <Descriptions.Item label="Phone">15311969622</Descriptions.Item>
          <Descriptions.Item label="Address">北京天安门</Descriptions.Item>
          <Descriptions.Item label="Money1">100000000</Descriptions.Item>
          <Descriptions.Item label="Money2" colSpan={2}>
            100000022220
          </Descriptions.Item>
          <Descriptions.Item label="Money3">
            <div>test</div>
          </Descriptions.Item>
          <Descriptions.Item label="Money4">1000000222201133</Descriptions.Item>
        </Descriptions>
        <Descriptions labelPlacement="right">
          <Descriptions.Item label="label名称很长很长" labelWidth="100px" labelPlacement="left">
            张三
          </Descriptions.Item>
          <Descriptions.Item label="Phone">15311969622</Descriptions.Item>
          <Descriptions.Item label="Address">北京天安门</Descriptions.Item>
          <Descriptions.Item label="Money1">100000000</Descriptions.Item>
          <Descriptions.Item label="Money2" colSpan={2}>
            100000022220
          </Descriptions.Item>
          <Descriptions.Item label="Money3">
            <div>test</div>
          </Descriptions.Item>
          <Descriptions.Item label="Money4">1000000222201133</Descriptions.Item>
        </Descriptions>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'
import Preview from '@hi-ui/preview'
import { JpgColorful } from '@hi-ui/icons'

/**
 * @title 设置大小
 */
export const Size = () => {
  const [images] = React.useState([
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_1.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_2.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_3.png',
  ])
  const [visible, setVisible] = React.useState(false)
  const [current, setCurrent] = React.useState(0)

  return (
    <>
      <h1>Size</h1>
      <div className="descriptions-size__wrap">
        <h2>md</h2>
        <Descriptions size="md">
          <Descriptions.Item label="机构类型" labelWidth={84}>
            第三方网点
          </Descriptions.Item>
          <Descriptions.Item label="主子站类型" labelWidth={84}>
            主站
          </Descriptions.Item>
          <Descriptions.Item label="机构状态" labelWidth={84}>
            有效
          </Descriptions.Item>
          <Descriptions.Item label="机构名称" labelWidth={84}>
            某某有限公司
          </Descriptions.Item>
          <Descriptions.Item label="是否自营" labelWidth={84}>
            是
          </Descriptions.Item>
          <Descriptions.Item label="实体门店招牌" labelWidth={84}>
            <div style={{ display: 'flex', alignItems: 'center' }}>
              <JpgColorful style={{ fontSize: 16 }} />
              <a href="#" style={{ textDecoration: 'none', color: '#4a9eff' }}>
                主站.jpg
              </a>
            </div>
          </Descriptions.Item>
          <Descriptions.Item label="备注信息" labelWidth={84} colSpan={2}>
            备注内容可能会非常长备注内容可能会非常长备注内容可能会非常长
          </Descriptions.Item>
          <Descriptions.Item label="维度名称常规" labelWidth={84}>
            <img
              src={images[0]}
              style={{ width: 40, height: 40, borderRadius: 2, cursor: 'pointer', marginRight: 6 }}
              onClick={() => {
                setCurrent(0)
                setVisible(true)
              }}
            />
            <img
              src={images[1]}
              style={{ width: 40, height: 40, borderRadius: 2, cursor: 'pointer', marginRight: 6 }}
              onClick={() => {
                setCurrent(1)
                setVisible(true)
              }}
            />
            <img
              src={images[2]}
              style={{ width: 40, height: 40, borderRadius: 2, cursor: 'pointer' }}
              onClick={() => {
                setCurrent(2)
                setVisible(true)
              }}
            />
          </Descriptions.Item>
        </Descriptions>
        <h2>sm</h2>
        <Descriptions size="sm">
          <Descriptions.Item label="机构类型" labelWidth={84}>
            第三方网点
          </Descriptions.Item>
          <Descriptions.Item label="主子站类型" labelWidth={84}>
            主站
          </Descriptions.Item>
          <Descriptions.Item label="机构状态" labelWidth={84}>
            有效
          </Descriptions.Item>
          <Descriptions.Item label="机构名称" labelWidth={84}>
            某某有限公司
          </Descriptions.Item>
          <Descriptions.Item label="是否自营" labelWidth={84}>
            是
          </Descriptions.Item>
          <Descriptions.Item label="实体门店招牌" labelWidth={84}>
            <div style={{ display: 'flex', alignItems: 'center' }}>
              <JpgColorful style={{ fontSize: 16 }} />
              <a href="#" style={{ textDecoration: 'none', color: '#4a9eff' }}>
                主站.jpg
              </a>
            </div>
          </Descriptions.Item>
          <Descriptions.Item label="备注信息" labelWidth={84} colSpan={2}>
            备注内容可能会非常长备注内容可能会非常长备注内容可能会非常长
          </Descriptions.Item>
          <Descriptions.Item label="维度名称常规" labelWidth={84}>
            <img
              src={images[0]}
              style={{ width: 40, height: 40, borderRadius: 2, cursor: 'pointer', marginRight: 6 }}
              onClick={() => {
                setCurrent(0)
                setVisible(true)
              }}
            />
            <img
              src={images[1]}
              style={{ width: 40, height: 40, borderRadius: 2, cursor: 'pointer', marginRight: 6 }}
              onClick={() => {
                setCurrent(1)
                setVisible(true)
              }}
            />
            <img
              src={images[2]}
              style={{ width: 40, height: 40, borderRadius: 2, cursor: 'pointer' }}
              onClick={() => {
                setCurrent(2)
                setVisible(true)
              }}
            />
          </Descriptions.Item>
        </Descriptions>

        <Preview
          title={`${current + 1}/${images.length}`}
          src={images}
          current={current}
          onPreviewChange={setCurrent}
          visible={visible}
          onClose={() => {
            setVisible(false)
          }}
        />
      </div>
    </>
  )
}

```

### vertical-border.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'

/**
 * @title 垂直带边框
 */
export const VerticalBorder = () => {
  return (
    <>
      <h1>垂直带边框</h1>
      <div className="descriptions-basic__wrap">
        <Descriptions placement="vertical" appearance="table">
          <Descriptions.Item label="名字">张三</Descriptions.Item>
          <Descriptions.Item label="Phone">15311969622</Descriptions.Item>
          <Descriptions.Item label="Address">北京天安门</Descriptions.Item>
          <Descriptions.Item label="Money1">100000000</Descriptions.Item>
          <Descriptions.Item label="Money2">100000022220</Descriptions.Item>
          <Descriptions.Item label="Money3">
            <div>test</div>
          </Descriptions.Item>
          <Descriptions.Item label="Money4">1000000222201133</Descriptions.Item>
          <Descriptions.Item label="Money4">1000000222201133</Descriptions.Item>
        </Descriptions>
      </div>
    </>
  )
}

```

### vertical.stories.tsx

```typescript
import React from 'react'
import Descriptions from '@hi-ui/descriptions'

/**
 * @title 上下布局
 * @desc 支持 label 和 content 上下布局形式进行展示
 */
export const Vertical = () => {
  return (
    <>
      <h1>垂直列表</h1>
      <div className="descriptions-basic__wrap">
        <Descriptions placement="vertical">
          <Descriptions.Item label="名字">张三</Descriptions.Item>
          <Descriptions.Item label="Phone">15311969622</Descriptions.Item>
          <Descriptions.Item label="Address">北京天安门</Descriptions.Item>
          <Descriptions.Item label="Money1">100000000</Descriptions.Item>
          <Descriptions.Item label="Money2">100000022220</Descriptions.Item>
          <Descriptions.Item label="Money3">
            <div>test</div>
          </Descriptions.Item>
          <Descriptions.Item label="Money4">1000000222201133</Descriptions.Item>
        </Descriptions>
      </div>
    </>
  )
}

```

## drawer 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Drawer from '@hi-ui/drawer'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const [visible, setVisible] = React.useState(false)

  return (
    <>
      <h1>Basic</h1>
      <div className="drawer-basic__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Drawer
          title="抽屉标题"
          visible={visible}
          onClose={() => setVisible(false)}
          footer={
            <div style={{ textAlign: 'right' }}>
              <Button type="default" key={1} onClick={() => console.log(2)}>
                取消
              </Button>
              <Button type="primary" key={0} onClick={() => console.log(1)}>
                确认
              </Button>
            </div>
          }
        >
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
        </Drawer>
      </div>
    </>
  )
}

```

### container.stories.tsx

```typescript
import React from 'react'
import Drawer from '@hi-ui/drawer'
import Button from '@hi-ui/button'

/**
 * @title 局部容器抽屉
 * @desc `container` 自定义渲染抽屉的容器
 */
export const Container = () => {
  const [visible, setVisible] = React.useState(false)
  const [container, setContainer] = React.useState<any>(null)
  return (
    <>
      <h1>Container</h1>
      <div
        ref={setContainer}
        className="drawer-container__wrap"
        style={{
          width: '100%',
          minWidth: 660,
          height: 420,
          background: '#f5f7fa',
          boxShadow: '1px 2px 8px #ddd',
          display: 'flex',
          justifyContent: 'center',
          alignItems: 'center',

          // Need add for it
          position: 'relative',
          overflow: 'hidden',
          zIndex: 0,
        }}
      >
        <Button type="primary" onClick={() => setVisible(!visible)}>
          open
        </Button>
        <Drawer
          title="抽屉标题"
          style={{ position: 'absolute' }}
          container={container}
          visible={visible}
          closeable={false}
          onClose={() => setVisible(false)}
        >
          我是一段文字，也可以是表单、表格、步骤条等等
        </Drawer>
      </div>
    </>
  )
}

```

### extra.stories.tsx

```typescript
import React from 'react'
import Drawer from '@hi-ui/drawer'
import Button from '@hi-ui/button'
import { EditOutlined } from '@hi-ui/icons'

/**
 * @title 顶部额外操作
 */
export const Extra = () => {
  const [visible, setVisible] = React.useState(false)

  return (
    <>
      <h1>Extra</h1>
      <div className="drawer-extra">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Drawer
          title={
            <div style={{ display: 'flex', justifyContent: 'space-between', alignItems: 'center' }}>
              <div>我是大标题</div>
              <Button
                icon={<EditOutlined />}
                appearance="link"
                size="sm"
                style={{ marginRight: 8, flexShrink: 0 }}
              />
            </div>
          }
          visible={visible}
          onClose={() => setVisible(false)}
          footer={
            <div style={{ textAlign: 'right' }}>
              <Button type="default" key={1} onClick={() => console.log(2)}>
                取消
              </Button>
              <Button type="primary" key={0} onClick={() => console.log(1)}>
                确认
              </Button>
            </div>
          }
        >
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
        </Drawer>
      </div>
    </>
  )
}

```

### header.stories.tsx

```typescript
import React from 'react'
import Drawer from '@hi-ui/drawer'
import Button from '@hi-ui/button'

/**
 * @title 无头抽屉
 * @desc title 不设置任何内容开启无头模式
 */
export const Header = () => {
  const [visible, setVisible] = React.useState(false)

  return (
    <>
      <h1>Header</h1>
      <div className="drawer-header__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Drawer closeable={false} visible={visible} onClose={() => setVisible(false)}>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
        </Drawer>
      </div>
    </>
  )
}

```

### mask.stories.tsx

```typescript
import React from 'react'
import Drawer from '@hi-ui/drawer'
import Button from '@hi-ui/button'

/**
 * @title 无蒙层
 */
export const Mask = () => {
  const [visible, setVisible] = React.useState(false)

  return (
    <>
      <h1>Mask</h1>
      <div className="drawer-mask__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Drawer
          title="抽屉标题"
          visible={visible}
          showMask={false}
          onClose={() => setVisible(false)}
          footer={
            <div style={{ textAlign: 'right' }}>
              <Button type="default" key={1} onClick={() => console.log(2)}>
                取消
              </Button>
              <Button type="primary" key={0} onClick={() => console.log(1)}>
                确认
              </Button>
            </div>
          }
        >
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
        </Drawer>
      </div>
    </>
  )
}

```

### nested.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Drawer from '@hi-ui/drawer'

/**
 * @title 嵌套抽屉
 */
export const Nested = () => {
  const [visible, setVisible] = React.useState(false)
  const [nestVisible, setNestVisible] = React.useState(false)

  return (
    <>
      <h1>Nested</h1>
      <div className="Drawer-nested__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Drawer
          title="抽屉标题"
          width={754}
          visible={visible}
          closeable={false}
          onClose={() => setVisible(false)}
        >
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <Button style={{ marginTop: 20 }} onClick={() => setNestVisible(!nestVisible)}>
            Nested
          </Button>
          <Drawer
            title="抽屉标题"
            visible={nestVisible}
            closeable={false}
            onClose={() => setNestVisible(false)}
          >
            Nest我是一段文字，也可以是表单、表格、步骤条等等
          </Drawer>
        </Drawer>
      </div>
    </>
  )
}

```

### outside-click.stories.tsx

```typescript
import React from 'react'
import Drawer from '@hi-ui/drawer'
import Button from '@hi-ui/button'
import Tree, { TreeDataItem } from '@hi-ui/tree'

/**
 * @title 点击外部事件处理
 * @desc 常用于无蒙层模式下，切换列表项详情内容
 */
export const OutsideClick = () => {
  const [visible, setVisible] = React.useState(false)
  const [data] = React.useState([
    {
      id: 1,
      title: '小米',
      children: [
        {
          id: 2,
          title: '研发',
          disabled: true,
          children: [
            { id: 3, title: '后端', disabled: true },
            { id: 4, title: '运维' },
            { id: 5, title: '前端' },
          ],
        },
        { id: 6, title: '产品' },
      ],
    },
    {
      id: 11,
      title: '大米',
      children: [
        { id: 22, title: '可视化' },
        { id: 66, title: 'HiUI' },
      ],
    },
  ])
  const [currentData, setCurrentData] = React.useState<TreeDataItem>()
  const wrapperRef = React.useRef<HTMLDivElement | null>(null)

  return (
    <>
      <h1>OutsideClick</h1>
      <div className="drawer-outside-click__wrap">
        <div className="list-wrapper" ref={wrapperRef}>
          <Tree
            data={data}
            onSelect={(id, node) => {
              // console.log('node', node)

              if (id) {
                setVisible(true)
                setCurrentData(node?.raw)
              } else {
                setVisible(false)
              }
            }}
          />
        </div>
        <Drawer
          title={currentData?.title}
          visible={visible}
          showMask={false}
          onClose={() => setVisible(false)}
          // 点击列表外部内容时关闭抽屉
          onOutsideClick={(e) => {
            // console.log('target', e.target)

            if (!wrapperRef.current?.contains(e.target as Element)) {
              setVisible(false)
            }
          }}
          footer={
            <div style={{ textAlign: 'right' }}>
              <Button type="default" key={1} onClick={() => console.log(2)}>
                取消
              </Button>
              <Button type="primary" key={0} onClick={() => console.log(1)}>
                确认
              </Button>
            </div>
          }
        >
          {currentData?.title}
        </Drawer>
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import React from 'react'
import Drawer from '@hi-ui/drawer'
import Button from '@hi-ui/button'

/**
 * @title 出现方位
 * @desc 设置抽屉拉出的方向
 */
export const Placement = () => {
  const [visible, setVisible] = React.useState(false)
  const [placement, setPlacement] = React.useState<any>('tpp')

  return (
    <>
      <h1>Placement</h1>
      <div className="drawer-placement__wrap">
        <table className="placement-table" cellSpacing="5">
          <tbody>
            <tr>
              <td></td>
              <td></td>
              <td>
                <Button
                  style={{ width: 100 }}
                  onClick={() => {
                    setPlacement('top')
                    setVisible(true)
                  }}
                >
                  top
                </Button>
              </td>
              <td></td>
              <td></td>
            </tr>
            <tr>
              <td></td>
              <td></td>
              <td></td>
              <td></td>
              <td></td>
            </tr>
            <tr>
              <td>
                <Button
                  style={{ width: 100 }}
                  onClick={() => {
                    setPlacement('left')
                    setVisible(true)
                  }}
                >
                  left
                </Button>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Button
                  style={{ width: 100 }}
                  onClick={() => {
                    setPlacement('right')
                    setVisible(true)
                  }}
                >
                  right
                </Button>
              </td>
            </tr>
            <tr>
              <td></td>
              <td></td>
              <td></td>
              <td></td>
              <td></td>
            </tr>
            <tr>
              <td></td>
              <td></td>
              <td>
                <Button
                  style={{ width: 100 }}
                  onClick={() => {
                    setPlacement('bottom')
                    setVisible(true)
                  }}
                >
                  bottom
                </Button>
              </td>
              <td></td>
              <td></td>
            </tr>
          </tbody>
        </table>

        <Drawer
          title="抽屉标题"
          visible={visible}
          placement={placement}
          onClose={() => setVisible(false)}
          footer={
            <div style={{ textAlign: 'right' }}>
              <Button type="default" key={1} onClick={() => console.log(2)}>
                取消
              </Button>
              <Button type="primary" key={0} onClick={() => console.log(1)}>
                确认
              </Button>
            </div>
          }
        >
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
          <div>我是一段文字，也可以是表单、表格、步骤条等等</div>
        </Drawer>
      </div>
    </>
  )
}

```

## dropdown 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Dropdown from '@hi-ui/dropdown'

/**
 * @title 基础用法
 * @desc 将一组同类的动作收起成为菜单，由一个操作入口展示使用
 */
export const Basic = () => {
  const [list] = React.useState([
    {
      id: 0,
      title: '小米商城',
      href: 'https://www.mi.com',
    },
    {
      id: 1,
      title: '菜单二',
    },
    {
      id: 2,
      title: '菜单三',
    },
    {
      id: 3,
      title: '菜单四',
    },
    {
      id: 4,
      title: '菜单五',
    },
  ])

  return (
    <>
      <h1>Basic</h1>
      <div className="dropdown-basic__wrap">
        <Dropdown data={list} title="鼠标悬停" onClick={console.log} />
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import Dropdown from '@hi-ui/dropdown'

/**
 * @title 禁用状态
 */
export const Disabled = () => {
  const [list] = React.useState([
    {
      id: '1',
      title: '菜单一',
    },
    {
      id: '2',
      title: '菜单二',
    },
    {
      id: '3',
      title: '菜单三',
    },
    {
      id: '4',
      title: '链接一',
      href: 'https://www.mi.com',
    },
  ])

  return (
    <>
      <h1>Disabled</h1>
      <div className="dropdown-disabled__wrap">
        <Dropdown disabled data={list} title="鼠标悬停" onClick={console.log} />
      </div>
    </>
  )
}

```

### group.stories.tsx

```typescript
import React from 'react'
import Dropdown from '@hi-ui/dropdown'

/**
 * @title 分组
 * @desc 通过分隔线将选项进行分组划分
 */
export const Group = () => {
  const [list] = React.useState([
    {
      id: 0,
      title: '小米商城',
      href: 'https://www.mi.com',
    },
    {
      id: 1,
      title: '菜单二',
    },
    {
      id: 2,
      title: '菜单三',
    },
    {
      id: 3,
      title: '菜单四',
    },
    {
      id: 4,
      title: '菜单五',
    },
    {
      id: 5,
      title: '菜单六',
      split: true,
    },
    {
      id: 6,
      title: '小米商城',
      href: 'https://www.mi.com',
      disabled: true,
    },
  ])

  return (
    <>
      <h1>Group</h1>
      <div className="dropdown-group__wrap">
        <Dropdown data={list} title="鼠标悬停" onClick={console.log} />
      </div>
    </>
  )
}

```

### icon.stories.tsx

```typescript
import React from 'react'
import Dropdown from '@hi-ui/dropdown'
import { PlusOutlined, EditOutlined, DeleteOutlined } from '@hi-ui/icons'

/**
 * @title 带Icon
 */
export const Icon = () => {
  const [list] = React.useState([
    {
      id: 0,
      title: (
        <span style={{ display: 'flex', alignItems: 'center' }}>
          <PlusOutlined style={{ fontSize: 16, color: '#5f6a7a' }} />
          <span style={{ marginLeft: 8 }}>添加</span>
        </span>
      ),
    },
    {
      id: 1,
      title: (
        <span style={{ display: 'flex', alignItems: 'center' }}>
          <EditOutlined style={{ fontSize: 16, color: '#5f6a7a' }} />
          <span style={{ marginLeft: 8 }}>编辑</span>
        </span>
      ),
    },
    {
      id: 2,
      title: (
        <span style={{ display: 'flex', alignItems: 'center' }}>
          <DeleteOutlined style={{ fontSize: 16, color: '#5f6a7a' }} />
          <span style={{ marginLeft: 8 }}>删除</span>
        </span>
      ),
    },
  ])

  return (
    <>
      <h1>Icon</h1>
      <div className="dropdown-icon__wrap">
        <Dropdown data={list} width={120} title="鼠标悬停" onClick={console.log} />
      </div>
    </>
  )
}

```

### multi-menu.stories.tsx

```typescript
import React from 'react'
import Dropdown from '@hi-ui/dropdown'

/**
 * @title 多级菜单
 * @desc 菜单项不属于同一级别，可分层级展开使用
 */
export const MultiMenu = () => {
  const [list] = React.useState([
    {
      id: '移动至',
      title: '移动至',
      children: [
        {
          id: '2019',
          title: '2019',
          children: [
            {
              id: 'Q1',
              title: 'Q1',
              children: [
                {
                  id: '01',
                  title: '01',
                },
                {
                  id: '02',
                  title: '02',
                },
                {
                  id: '03',
                  title: '03',
                },
              ],
            },
            {
              id: 'Q2',
              title: 'Q2',
              disabled: true,
            },
            {
              id: 'Q3',
              title: 'Q3',
            },
          ],
        },
        {
          id: '2020',
          title: '2020',
          children: [
            {
              id: 'Q1',
              title: 'Q1',
              children: [
                {
                  id: '01',
                  title: '01',
                },
                {
                  id: '02',
                  title: '02',
                },
                {
                  id: '03',
                  title: '03',
                },
              ],
            },
            {
              id: 'Q2',
              title: 'Q2',
              disabled: true,
            },
            {
              id: 'Q3',
              title: 'Q3',
            },
          ],
        },
      ],
    },
    {
      id: '复制至',
      title: '复制至',
      children: [
        {
          id: '2019',
          title: '2019',
          children: [
            {
              id: 'Q1',
              title: 'Q1',
              disabled: true,
              children: [
                {
                  id: '01',
                  title: '01',
                },
                {
                  id: '02',
                  title: '02',
                  children: [
                    {
                      id: '02-01',
                      title: '02-01',
                    },
                    {
                      id: '02-02',
                      title: '02-02',
                    },
                  ],
                },
                {
                  id: '03',
                  title: '03',
                  children: [
                    {
                      id: '03-01',
                      title: '03-01',
                    },
                    {
                      id: '03-02',
                      title: '03-02',
                    },
                  ],
                },
              ],
            },
            {
              id: 'Q2',
              title: 'Q2',
            },
            {
              id: 'Q3',
              title: 'Q3',
            },
          ],
        },
        {
          id: '2020',
          title: '2020',
          children: [
            {
              id: 'Q1',
              title: 'Q1',
              disabled: true,
              children: [
                {
                  id: '01',
                  title: '01',
                },
                {
                  id: '02',
                  title: '02',
                  children: [
                    {
                      id: '02-01',
                      title: '02-01',
                    },
                    {
                      id: '02-02',
                      title: '02-02',
                    },
                  ],
                },
                {
                  id: '03',
                  title: '03',
                  children: [
                    {
                      id: '03-01',
                      title: '03-01',
                    },
                    {
                      id: '03-02',
                      title: '03-02',
                    },
                  ],
                },
              ],
            },
            {
              id: 'Q2',
              title: 'Q2',
            },
            {
              id: 'Q3',
              title: 'Q3',
            },
          ],
        },
      ],
    },
    {
      id: '删除',
      title: '删除',
    },
  ])

  return (
    <>
      <h1>MultiMenu</h1>
      <div className="dropdown-multi-menu__wrap">
        <Dropdown data={list} title="操作" width={120} trigger="click" />
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import React from 'react'
import Dropdown from '@hi-ui/dropdown'
import Button from '@hi-ui/button'

/**
 * @title 弹出方位
 * @desc 下拉菜单可打开不同的方向，以应对页面边缘的遮盖问题
 */
export const Placement = () => {
  const [list] = React.useState([
    {
      id: 0,
      title: '小米商城',
      href: 'https://www.mi.com',
    },
    {
      id: 1,
      title: '菜单二',
    },
    {
      id: 2,
      title: '菜单三',
    },
    {
      id: 3,
      title: '菜单四',
    },
    {
      id: 4,
      title: '菜单五',
    },
  ])

  return (
    <>
      <h1>Placement</h1>
      <div className="dropdown-placement__wrap">
        <table className="placement-table" cellSpacing="5">
          <tbody>
            <tr>
              <td></td>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'top-start' }}
                >
                  <Button>top-start</Button>
                </Dropdown>
              </td>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'top' }}
                >
                  <Button>top</Button>
                </Dropdown>
              </td>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'top-end' }}
                >
                  <Button>top-end</Button>
                </Dropdown>
              </td>
              <td></td>
            </tr>
            <tr>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'left-start' }}
                >
                  <Button>left-start</Button>
                </Dropdown>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'right-start' }}
                >
                  <Button>right-start</Button>
                </Dropdown>
              </td>
            </tr>
            <tr>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'left' }}
                >
                  <Button>left</Button>
                </Dropdown>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'right' }}
                >
                  <Button>right</Button>
                </Dropdown>
              </td>
            </tr>
            <tr>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'left-end' }}
                >
                  <Button>left-end</Button>
                </Dropdown>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'right-end' }}
                >
                  <Button>right-end</Button>
                </Dropdown>
              </td>
            </tr>
            <tr>
              <td></td>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'bottom-start' }}
                >
                  <Button>bottom-start</Button>
                </Dropdown>
              </td>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'bottom' }}
                >
                  <Button>bottom</Button>
                </Dropdown>
              </td>
              <td>
                <Dropdown
                  data={list}
                  title="鼠标悬停"
                  trigger="hover"
                  overlay={{ placement: 'bottom-end' }}
                >
                  <Button>bottom-end</Button>
                </Dropdown>
              </td>
              <td></td>
            </tr>
          </tbody>
        </table>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Dropdown from '@hi-ui/dropdown'
import { PlusOutlined, EditOutlined, DeleteOutlined } from '@hi-ui/icons'

/**
 * @title 设置选项大小
 */
export const Size = () => {
  const [list] = React.useState([
    {
      id: '添加',
      title: (
        <span style={{ display: 'flex', alignItems: 'center' }}>
          <PlusOutlined style={{ fontSize: 16, color: '#5f6a7a' }} />
          <span style={{ marginLeft: 6 }}>添加</span>
        </span>
      ),
      children: [
        {
          id: '2019',
          title: '2019',
          children: [
            {
              id: 'Q1',
              title: 'Q1',
              children: [
                {
                  id: '01',
                  title: '01',
                },
                {
                  id: '02',
                  title: '02',
                },
                {
                  id: '03',
                  title: '03',
                },
              ],
            },
            {
              id: 'Q2',
              title: 'Q2',
              disabled: true,
            },
            {
              id: 'Q3',
              title: 'Q3',
            },
          ],
        },
        {
          id: '2020',
          title: '2020',
          children: [
            {
              id: 'Q1',
              title: 'Q1',
              children: [
                {
                  id: '01',
                  title: '01',
                },
                {
                  id: '02',
                  title: '02',
                },
                {
                  id: '03',
                  title: '03',
                },
              ],
            },
            {
              id: 'Q2',
              title: 'Q2',
              disabled: true,
            },
            {
              id: 'Q3',
              title: 'Q3',
            },
          ],
        },
      ],
    },
    {
      id: '编辑',
      title: (
        <span style={{ display: 'flex', alignItems: 'center' }}>
          <EditOutlined style={{ fontSize: 16, color: '#5f6a7a' }} />
          <span style={{ marginLeft: 6 }}>编辑</span>
        </span>
      ),
      children: [
        {
          id: '2019',
          title: '2019',
          children: [
            {
              id: 'Q1',
              title: 'Q1',
              disabled: true,
              children: [
                {
                  id: '01',
                  title: '01',
                },
                {
                  id: '02',
                  title: '02',
                  children: [
                    {
                      id: '02-01',
                      title: '02-01',
                    },
                    {
                      id: '02-02',
                      title: '02-02',
                    },
                  ],
                },
                {
                  id: '03',
                  title: '03',
                  children: [
                    {
                      id: '03-01',
                      title: '03-01',
                    },
                    {
                      id: '03-02',
                      title: '03-02',
                    },
                  ],
                },
              ],
            },
            {
              id: 'Q2',
              title: 'Q2',
            },
            {
              id: 'Q3',
              title: 'Q3',
            },
          ],
        },
        {
          id: '2020',
          title: '2020',
          children: [
            {
              id: 'Q1',
              title: 'Q1',
              disabled: true,
              children: [
                {
                  id: '01',
                  title: '01',
                },
                {
                  id: '02',
                  title: '02',
                  children: [
                    {
                      id: '02-01',
                      title: '02-01',
                    },
                    {
                      id: '02-02',
                      title: '02-02',
                    },
                  ],
                },
                {
                  id: '03',
                  title: '03',
                  children: [
                    {
                      id: '03-01',
                      title: '03-01',
                    },
                    {
                      id: '03-02',
                      title: '03-02',
                    },
                  ],
                },
              ],
            },
            {
              id: 'Q2',
              title: 'Q2',
            },
            {
              id: 'Q3',
              title: 'Q3',
            },
          ],
        },
      ],
    },
    {
      id: '删除',
      title: (
        <span style={{ display: 'flex', alignItems: 'center' }}>
          <DeleteOutlined style={{ fontSize: 16, color: '#5f6a7a' }} />
          <span style={{ marginLeft: 6 }}>删除</span>
        </span>
      ),
    },
  ])

  return (
    <>
      <h1>Size</h1>
      <div className="dropdown-size__wrap">
        <h2>lg</h2>
        <Dropdown
          size="lg"
          data={list}
          title="左键单击"
          trigger={'click'}
          onClick={console.log}
        />
        <h2>md</h2>
        <Dropdown
          size="md"
          data={list}
          title="左键单击"
          trigger={'click'}
          onClick={console.log}
        />
        <h2>sm</h2>
        <Dropdown
          size="sm"
          data={list}
          title="左键单击"
          trigger={'click'}
          onClick={console.log}
        />
      </div>
    </>
  )
}

```

### trigger-button.stories.tsx

```typescript
import React from 'react'
import Dropdown from '@hi-ui/dropdown'
import { Tooltip } from '@hi-ui/tooltip'
import { Avatar } from '@hi-ui/avatar'

/**
 * @title 自定义触发按钮
 */
export const TriggerButton = () => {
  const [list] = React.useState([
    {
      id: 0,
      title: '小米商城',
      href: 'https://www.mi.com',
    },
    {
      id: 1,
      title: '菜单二',
    },
    {
      id: 2,
      title: '菜单三',
    },
    {
      id: 3,
      title: '菜单四',
    },
    {
      id: 4,
      title: '菜单五',
    },
    {
      id: 5,
      title: '菜单六',
    },
    {
      id: 6,
      title: '菜单七',
    },
  ])

  return (
    <>
      <h1>TriggerButton</h1>
      <div className="dropdown-trigger-button__wrap">
        <Dropdown data={list} title="鼠标悬停" onClick={console.log}>
          <div style={{ display: 'inline-block' }}>
            <Tooltip title="Dropdown 触发的事件传给 tooltip 不会影响 Avatar 哦">
              <Avatar initials="M" />
            </Tooltip>
          </div>
        </Dropdown>
      </div>
    </>
  )
}

```

### trigger.stories.tsx

```typescript
import React from 'react'
import Dropdown from '@hi-ui/dropdown'

/**
 * @title 触发方式
 * @desc 不同触发方式呼出菜单
 */
export const Trigger = () => {
  const [list] = React.useState([
    {
      id: 0,
      title: '小米商城',
      href: 'https://www.mi.com',
    },
    {
      id: 1,
      title: '菜单二',
    },
    {
      id: 2,
      title: '菜单三',
    },
    {
      id: 3,
      title: '菜单四',
    },
    {
      id: 4,
      title: '菜单五',
    },
    {
      id: 5,
      title: '菜单六',
    },
  ])

  return (
    <>
      <h1>Trigger</h1>
      <div className="dropdown-trigger__wrap">
        <Dropdown overlayClassName="xxx" data={list} trigger="click" title="左键单击" />
        <br />
        <br />
        <Dropdown overlayClassName="xxx" data={list} trigger="hover" title="鼠标悬停" />
        <br />
        <br />
        <Dropdown overlayClassName="xxx" data={list} trigger="contextmenu" title="右键单击" />
      </div>
    </>
  )
}

```

### type.stories.tsx

```typescript
import React from 'react'
import Dropdown from '@hi-ui/dropdown'
import message from '@hi-ui/message'

/**
 * @title 按钮用法
 * @desc 操作入口以 Button 样式展示，强调重要操作
 */
export const Type = () => {
  const [list] = React.useState([
    {
      id: 0,
      title: '小米商城',
      href: 'https://www.mi.com',
    },
    {
      id: 1,
      title: '菜单二',
    },
    {
      id: 2,
      title: '菜单三',
    },
    {
      id: 3,
      title: '菜单四',
    },
    {
      id: 4,
      title: '菜单五',
    },
    {
      id: 5,
      title: '菜单六',
    },
  ])

  return (
    <>
      <h1>Type</h1>
      <div className="dropdown-type__wrap">
        <Dropdown type="text" data={list} title="鼠标悬停" onClick={console.log} />
        <br />
        <br />
        <Dropdown type="button" data={list} title="鼠标悬停" onClick={console.log} />
        <br />
        <br />
        <Dropdown
          type="group"
          data={list}
          title="鼠标悬停"
          onClick={console.log}
          onButtonClick={() => {
            message.open({ title: '点击左侧按钮' })
          }}
        />
      </div>
    </>
  )
}

```

## ellipsis-tooltip 组件

### basic.stories.tsx

```typescript
import React from 'react'
import EllipsisTooltip from '@hi-ui/ellipsis-tooltip'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>基本使用 </h1>
      <div className="ellipsis-tooltip-basic__wrap" style={{ width: 400, margin: '0 auto' }}>
        <h4>没有超出</h4>
        <EllipsisTooltip>没有超出限制时，不会出现提示</EllipsisTooltip>
        <h4>超出宽度限制</h4>
        <EllipsisTooltip>
          学而时习之，不亦说乎？有朋自远方来，不亦乐乎？人不知而不愠，不亦君子乎？
        </EllipsisTooltip>
      </div>
    </>
  )
}

```

### max-text-count.stories.tsx

```typescript
import React from 'react'
import EllipsisTooltip from '@hi-ui/ellipsis-tooltip'

/**
 * @title 超出字数省略
 */
export const MaxTextCount = () => {
  return (
    <>
      <h1>超出字数省略</h1>
      <div className="ellipsis-tooltip-multiple__wrap" style={{ width: 400, margin: '0 auto' }}>
        <h4>没有超出</h4>
        <EllipsisTooltip maxTextCount={20}>学而时习之</EllipsisTooltip>
        <h4>文字超出 20 个字符时</h4>
        <EllipsisTooltip maxTextCount={20}>
          学而时习之，不亦说乎？有朋自远方来，不亦乐乎？人不知而不愠，不亦君子乎？
        </EllipsisTooltip>
        <h4>文字超出 40 个字符时</h4>
        <EllipsisTooltip maxTextCount={40}>
          【译】孔子说：“学习并且不断温习，不也很愉快吗？远方来了朋友，不也很快乐吗？人家不了解我，我也不怨恨，不也是君子吗？”
        </EllipsisTooltip>
      </div>
    </>
  )
}

```

### multiply-line.stories.tsx

```typescript
import React from 'react'
import EllipsisTooltip from '@hi-ui/ellipsis-tooltip'

/**
 * @title 多行省略
 */
export const MultiplyLine = () => {
  const textOverview =
    '【译】孔子说：“学习并且不断温习，不也很愉快吗？远方来了朋友，不也很快乐吗？人家不了解我，我也不怨恨，不也是君子吗？”，【译】孔子说：“学习并且不断温习，不也很愉快吗？远方来了朋友，不也很快乐吗？人家不了解我，我也不怨恨，不也是君子吗？”'

  return (
    <>
      <h1>多行省略</h1>
      <div className="ellipsis-tooltip-basic__wrap" style={{ width: 400, margin: '0 auto' }}>
        <h4>超出 3 行(tooltip 内容过多可设置样式换行)</h4>
        <EllipsisTooltip
          numberOfLines={3}
          tooltipProps={{
            title: <div style={{ width: 400 }}>{textOverview}</div>,
          }}
        >
          {textOverview}
        </EllipsisTooltip>
      </div>
    </>
  )
}

```

## empty-state 组件

### basic.stories.tsx

```typescript
import React from 'react'
import EmptyState from '@hi-ui/empty-state'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>EmptyState</h1>
      <div className="empty-state-basic__wrap">
        <EmptyState />
      </div>
    </>
  )
}

```

### colorful.stories.tsx

```typescript
import React from 'react'
import EmptyState, {
  EMPTY_STATE_IMAGE_NO_MESSAGE_COLOURFUL,
  EMPTY_STATE_IMAGE_NO_RESULT_COLOURFUL,
  EMPTY_STATE_IMAGE_NO_COLLECTION_COLOURFUL,
  EMPTY_STATE_IMAGE_NO_ACCESS_COLOURFUL,
  EMPTY_STATE_IMAGE_NO_NETWORK_COLOURFUL,
  EMPTY_STATE_IMAGE_NO_OPEN_COLOURFUL,
  EMPTY_STATE_IMAGE_404_COLOURFUL,
  EMPTY_STATE_IMAGE_SERVICE_ERROR_COLOURFUL,
  EMPTY_STATE_IMAGE_PAGE_ERROR_COLOURFUL,
  EMPTY_STATE_IMAGE_SUCCESS_COLOURFUL,
  EMPTY_STATE_IMAGE_ERROR_COLOURFUL,
  EMPTY_STATE_IMAGE_WARNING_COLOURFUL,
  EMPTY_STATE_IMAGE_NO_DATA_COLOURFUL,
  EMPTY_STATE_IMAGE_JUMP_COLOURFUL,
  EMPTY_STATE_IMAGE_CHART_NO_DATA_COLOURFUL,
} from '@hi-ui/empty-state'

/**
 * @title 彩色图标
 */
export const Colorful = () => {
  return (
    <>
      <h1>Colorful</h1>
      <div className="empty-state-colorful__wrap">
        <div style={{ display: 'grid', gridTemplateColumns: '1fr 1fr 1fr', rowGap: 32 }}>
          <EmptyState size="xxl" title="无权限" indicator={EMPTY_STATE_IMAGE_NO_ACCESS_COLOURFUL} />
          <EmptyState
            size="xxl"
            title="无网络"
            indicator={EMPTY_STATE_IMAGE_NO_NETWORK_COLOURFUL}
          />
          <EmptyState size="xxl" title="建设中" indicator={EMPTY_STATE_IMAGE_NO_OPEN_COLOURFUL} />
          <EmptyState size="xxl" title="404" indicator={EMPTY_STATE_IMAGE_404_COLOURFUL} />
          <EmptyState
            size="xxl"
            title="服务器失去链接"
            indicator={EMPTY_STATE_IMAGE_SERVICE_ERROR_COLOURFUL}
          />
          <EmptyState
            size="xxl"
            title="页面出错"
            indicator={EMPTY_STATE_IMAGE_PAGE_ERROR_COLOURFUL}
          />
          <EmptyState size="xxl" title="提交成功" indicator={EMPTY_STATE_IMAGE_SUCCESS_COLOURFUL} />
          <EmptyState size="xxl" title="错误提示" indicator={EMPTY_STATE_IMAGE_ERROR_COLOURFUL} />
          <EmptyState size="xxl" title="警告提示" indicator={EMPTY_STATE_IMAGE_WARNING_COLOURFUL} />
          <EmptyState size="xl" title="跳转" indicator={EMPTY_STATE_IMAGE_JUMP_COLOURFUL} />
          <EmptyState
            size="xl"
            title="无查询结果"
            indicator={EMPTY_STATE_IMAGE_NO_RESULT_COLOURFUL}
          />
          <EmptyState size="xl" title="暂无数据" indicator={EMPTY_STATE_IMAGE_NO_DATA_COLOURFUL} />
          <EmptyState
            size="xl"
            title="暂无收藏"
            indicator={EMPTY_STATE_IMAGE_NO_COLLECTION_COLOURFUL}
          />
          <EmptyState size="xl" title="无消息" indicator={EMPTY_STATE_IMAGE_NO_MESSAGE_COLOURFUL} />
          <EmptyState
            size="xl"
            title="无数据-图表类"
            indicator={EMPTY_STATE_IMAGE_CHART_NO_DATA_COLOURFUL}
          />
        </div>
      </div>
    </>
  )
}

```

### custom.stories.tsx

```typescript
import React from 'react'
import EmptyState, {
  EMPTY_STATE_IMAGE_NO_MESSAGE,
  EMPTY_STATE_IMAGE_NO_RESULT,
  EMPTY_STATE_IMAGE_NO_COLLECTION,
} from '@hi-ui/empty-state'

/**
 * @title 自定义
 */
export const Custom = () => {
  return (
    <>
      <h1>Custom</h1>
      <div className="empty-state-custom__wrap">
        <EmptyState
          style={{ marginTop: 32 }}
          title="暂无数据"
          indicator={
            <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAKAAAACgCAMAAAC8EZcfAAACFlBMVEUAAAD29/nw8vX19vjx8vX09Pf////////s7vLu8PP7+/v4+Prx8/Xs7vL4+fr9/v7p6+/u8fTr7fD////+///u7/Lm6O7v8fTo6u/5+fz29vvk5+z19vbp6/Di5ev5+fny8vj39/n09fjn6e3g5Onx8fTn6e/f4unl6O3j5uzx8vLg4+n39/nn6e3q7PHy9vfj5uvr7vLe4Ofc3+fr7fHz+fnd4Ob+/v7i5er////b3+bk5uzs7vLk6O34///39//k6u7a3uXg4+nd4ej09/fe4ebv8PX3///s7vDa3ePa3eLu7vPy9fXL0Nbu7vCco67s7fHZ3uPr7fCmrLavtb7r7fHT193r7vHs7vHr7fHq7vLS1923vMW+w8rc3+TP09rFyc/O0trV2d/P09jY2uDm5+vo6e3g4+nm6Ozh5OnS1tvf4uXh4+fk5ejQ1dzs7vHP1NzKztXX2+Hh5enj5+vCyNPU2uHf4ufX2t7e4OTW2eDg4+nN0trf4ubKz9fb3uPMz9jc4OTg4+nEydPLz9enrbfU19709Pjy8vfQ1t/r7fCyu8iSmqa+xdC9xM/Ax9LV2eC5wc20vMm4wMy1vcq2vsvP09rKz9e7ws7CyNPZ3OLX2+HR1tzQ1Nva3ePS1t3d4OXU2N/DytTT1963v8vN0tnM0djL0NjFy9be4ebg5Ojf4ufb3+Ta3uS7w87l6Ozi5erW3OTSupStAAAAiXRSTlMANFY/UEUCCHJmHiRLbC8Oglx3GRNhk2GIKTqeOn2pKjAYS420W426mKMUrw2IfDukZ8DLfSrFJK4U0Jl3mSQeHta/xUVAKh6/vp5sUMAH+dUZ8/Lq5q6mlI9ANeHXJvbNyr25pXx09efJspKLhoDt48avgWT38+SolWW6nJp8c2VVOujh2chENBVXMMkAAA1+SURBVHja7JnPaxpBGIa/0/aYa48t9FR6aqFnKSixEFHBGCNE9JJ4MSYNDSRt84NSGk+bEJKyrqubxYirov0P+87MZuvSi5vs4hTmOczN5dl3vm92+CSFQqFQKBT/F6lSNp/PllIkJ5mNlsdGhiQks9ryWZXRkOfnZ0jSkWoFkK8OS0HBEslGNiiYJdnIBwXzJBvSC0q/xdI3ifTHjPQHtfyfOukvC/JftxQKiSk3qs1K//5+cPt9r1Em2SjXzE6nc9PnhmBNMsWG3e1yw5ube0/xG0nER9uBIBRhyFIcMMUvJA0N3bahCEfTNxxIlGG5rQMHihCEIgz7PENZ6jBtcEMeoun1CkJEp9CCJIqFQjFBMVE2jHZbhAjDh17hhVhe0G+3BXbjMvxkWQ+KNlM0vUpEOzdoIYotTpHi4f3EMixhaAPnIURs8x4tREEIFigeDnsTZLi/8npf17GuO846Vh5iUwrB7V5vMrFyRLm2zlbbYSsPsSLFFh/2wCSBWjfabLVttvJCbErRJPUhE0xvbeG4wVrT9RpW3ivVSI8Z7ahaqVRPNQrJ19GwB8asEv1eEe0c6dcuh5fG2XC7lqNwbI5GwyEEx2MYBo/EJEWHltadLuqmP1gLmaF2OOKKvFcMwA1ZiM0MRccRnms7pon70imF48x1XWGIDEWIQvAs0uMWT8ZjWYhVCskrd+QiRGaISuQZshT3tWhPM7w8qx2zU6GQvKm7TNAz5ClC8N0bilRwiA8C3+ZuaEFKuIBXom9o1FYoUuruCFVusBB/UFh+ztzZXIgw/HyiUbQczFDoqHIU+NEjfgxcTxG8PVmhqNE+sAx6qMR0+Hd/Pp3OZjsvts6T4DyRoTh4CUMWYjpHoTmeTqc7KYoZ7aC+vV0/0Cg8O/CTed71THI/0o6zUvspFAqFQqGIiaSB+/Xc8NT0RpN8SC64m7aezOZTZrvC0BtlwM+f4ntc/n664OqjA7Qsz9AWE/LAEF8EeHWxxAjTEDT+2eP+/B5fXl8sK0IRIPDmGHMDcgj6AV5dLCtCEaDYY8/Q7Hb+7rEXIASXFWFywgd+MAz+CcIFheHdNQSXFmF6DMGAHwS5n98lv66wxcuKMPmHOTvIaRgGogCqqmLXE3TFGXoERA+HrKakiSVnwyKENkjIZ+RPxh3ZtCuQ8J8TPP0ZTywHrwz6UgWiClGSoJ3j0fcA1opw9wVharENIWqJUI9JgM+9VIpwn17SyggBtH/Cl9ErsE6EOzwC2SkR3+t70ePLGQH2vUOLq0S4t+fSNwHay33qsfwqnH2vCVaJ8OkTQvjyKZQWo3RVf5wb+JwC6+3CeZ5H1DAcUYfDoWliCG3bdt3klwAB/Hv9ApYDwTMfCkD4Oo+SDlcHZgGi1CdC8VEAQUSC5osxBmnwNImPAYj8xrzFOoE6gr1z9YE6gylAVAwCvAZYHygTWASohzi1mCHBRWi+2OiO6TxLgvOdJWNnmCDBrMPmUyB8DMClwwvPRhC8a4KuPlATTEBLcJIlc+odC7A8w5JgOsMcLTZgtgR1C3K0uPjONQIEUYA9DbDw6ZbWmwzHDA7ZmgYwdKnFLEDwhsyX31UdUYshFJ9uwQSkSdC2YCyvWifHACwmMAF1TZ/IgNmantJ3jgMI3s/LtPpYgMUWDLqlNUAWoC2ZBWg+mgSP2V0QQOswT4J2RKIGKN9hogSPt08eXAke8xG0q6D4SIDDnZsMKzCC19qWZgHaCMIXJEAIxcczg+BpgjEo0HO1+OZZEAF64f0j8HG12m636/XD82bzXWu59CYVBmEYatUKtLRcbKFFKAi2tJRSS6tSIWoTEy9xoXGlicbLwsvCGI0uXBnjxp26dKeJP9NnZj7Go9UYg77SU7+ey/fwvjMD4+PjY2MzM7P5Q4cOTU5OTOw8i07B98h7xPVpZL7njdbc9HSptJbZmZi4OMne+dmZmbGx8Uvj1dT+2FQ83m4vALi/aoD1+iyEHQHM3DYDf5yCiuf6OjLgmdpca3p6rZTJZCYmJicPddh/pg4gfABW4hDuS1XHxvKdzuT9e/ceP3708OWFC3fvXr/+4PIz+PyrFnyf4UMRwA8jG9hriYOba/AJIAbmZ+szAphSB6eGgPW8Aj4F8KEAvrj+4M7l18+UL/pl2vBcH7+OkvKXM73aHHzqIHwCCB8GAoiBAFYEkPozwPsK+PIVhAJ4587ly09u3bp1E924ceMauoquoHf/RBcatZYAloYJd+DLawlGABf2va2O0x2djgFCaIAPHBC+fw945c2FWgMDJeBN5aNHtEUAVD4Ay5IxbWxtcim0SX5W+5g+2SltEkBrjicdPrzUW5qfX19ePnJk5cTK0aNHjx3b2Dh7bmtr6/jx46dEZ6LSv3BmC53dOHvsGHecWFk5cmR5fXl+vtdbOny4UVM+DPQKpEXq2sOU4P79+2IFAPFQB83+VBVACGcAHBJmSms8Ya5Vq0F4egnC5eX1I44ojBuBUTFdrBCnznHFMceDD7z5pdPK16CDox1CwtLCbiCA5YpYaJMmpYQ2CzuBcCfDiBLCuUbjsJg4D+K6Iq4YIoxnNza2QAEGJlNYb4h3hreieOvr6zwBPOFrCR/P3zE+n4HWwvAB2J1SQjyMEv7g4eamEdZqIPYwcegijpw4GiBhROBsnUP8lqXDYd6JE4KHfYLXC/GS75rWn/F1bAQScDWlfMVYstydipahp2x1qPMaxJLETM6OGGyE0SCh3CvYDI56UDrMo/qWsK/WaMxZvJSfDxitP8sXPogWYv1kuaAeYuHPKRPz5LAQMTG4WJOgl04LImJfKAUTkr0SNNjQ8tC80xKupUu8Vn7OF/KFQvmKOJhMdstKaHW4CyIdhIces5i4k1mjndVFHm6IMGpPk7YKFmj0h+PQNnOOvkU96JDMFsNb29zx8XIIvOEArO4K30JxIR4bJJP9wtBD7RQh9ELMUxfBRBDVRUkaRsR+hB2slOkTkbsWcsU6Cs/oWvrhNs3zPF2pvqF9Ol8CXzyWSJwXD2UceiGmAuIMlRhcvGiMpSEjLU05Ihhp7CBoAhOWmWlmXO+0wjXMO5t8VnsTF3W46BcEs68ayk/w4lOxbCKR2E4WxESZh9bMDMRU6JU6Lv6IGOYijDVzUgMXUDXUpWsEmkgurrXAM+8wz2uP2UdzeHeYfW3lq8Sy2cVEop/c7pYramLbTNRKtJzNxY7WolZjCU0j8UKaxorSxceN+uXivExkBBx0bh54F7X2mH31SLoQtIuKN1WONRezWY25UO6CKJXYNkT7fmjdEmwMjKhkPWNW8qMMsCI1NrLW88ZGsNSd000a3SzhGp65h30L8FWmKuVCIZZr5kAUE5k3Zc/Zg4bRi1EZ3UiG4yZRTaMAygvRArawdTi/ucbV0rM7CkfldRSP0vPWiOLBB08/GUunT+ayi4uJ84kkLqqJjrjriDBSjQLZcUj5FETsiy0U5q9VCuczxoYuinVIYtFovTV2tTeG6RYKECViB1fTzVxOKnGAi4UhYjHiojFax1jWDHCnVDORGVrSl0Kx1jz1vF2qd+n9eZKtK52Z5+HSu4ZXZv4lBgBCmCZnXKQUtwmafiboH5OO+Mhw1LittR0zOMrLZY45mrIhvV8e5N6RbRgs7bjiUXyQwJPNxg4cOHgwncZFEGXk9GVuMxWFsQ2iMu6mLGuDrPPW2UO8NE6X0zoTskiNzVriu3WXUojn73M8vhiwP+HCAlEupoQgUopNQRxQi7jYBdGiXlBG5JAiNkFCiToSmkn/u2cNl/zDNWMDToNlqKAIHZ1b6BaS24JH7+ZOAqiIFnSOmbPIKRi3C11sBBEfHdLThlKlO5KWgkKgGBx/Wss1jgYbqkbhtG3NvLLSnce9bBae1TR8imiMq6EYsRFxdfCRrGF0SMeE06QEkZ/oGi4nQym93+DQAnjBO6HzbCGB5+BB5XPENIhMHcwVG7VjCpVgJCE4pQbumIb6O427qtwCmrO1eSRw0KFyV/piewAd+zdzTaoOogOG54gwrqZtdsPINx1ahnlZsaaBku9k7UDpnDjCkU9GxCEorP28JBrxra2xmnXY0IUuGejYX+gQTM4XtZGOEUbq0cLmg5q0RUbZLgYz0a5tu+uu6iH8shPIZrAVHHCBjbcd4Kg7tKje5QTgZzpH9Gqkq7Vnsto0iAysJqEMvSMRCajLjXWrXMVwfdx9oyOk6mweD7L40aS+Vn9PF2X0yZOD0SG3jRJMd9MGejFsXyxy+OU6HoRnvEUSAY7n6TQmV5QDz5P9PV40a4ykaeTGRZQYGKWOSYSd7KUt9EfpdRwq5FkQNNSHDbosDhAWwRLbr+ruz0aC2Wxab2OllmVf3zwuYAUHTd5fHH5aF7iqCxeB9uVG0GwQo5NadHut+ytIWlvnjyRunOfdTyS0XSzV+AWaX5G1nrerEqqBVI36JnCrsP09XBTSKUX60FwWyR4DSNVTpAR9XkbTD2s/r56BxkuqRkeJs0XhRqdEbNGEFVJk23JIRHSeF0TR83ILfUcraL2NzLaX0jEdlB4STo1feh6BIly+9vNpBYPM0X5k+5eYcLp0Uz3IEf1yDZaD/Se0vaDO+meBNTrY6LB7NTrUN/NI150FAaz3AAAAAElFTkSuQmCC"></img>
          }
        />
        <EmptyState
          style={{ marginTop: 32 }}
          title="暂无消息"
          indicator={EMPTY_STATE_IMAGE_NO_MESSAGE}
        />
        <EmptyState
          style={{ marginTop: 32 }}
          title="暂无搜索结果"
          indicator={EMPTY_STATE_IMAGE_NO_RESULT}
        />
        <EmptyState
          style={{ marginTop: 32 }}
          title="暂无收藏"
          indicator={EMPTY_STATE_IMAGE_NO_COLLECTION}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import EmptyState from '@hi-ui/empty-state'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>Size</h1>
      <div className="empty-state-size__wrap" style={{ display: 'flex', alignItems: 'center' }}>
        <EmptyState size={'sm'} />
        <EmptyState title="暂无数据" size={'md'} />
        <EmptyState title="暂无数据" size={'lg'} />
      </div>
    </>
  )
}

```

### with-content.stories.tsx

```typescript
import React from 'react'
import EmptyState from '@hi-ui/empty-state'
import { Button } from '@hi-ui/button'

/**
 * @title 带内容
 */
export const WithContent = () => {
  return (
    <>
      <h1>WithContent</h1>
      <div className="empty-state-with-content__wrap">
        <EmptyState title="当前页面暂无数据">
          <Button type="primary">刷新</Button>
        </EmptyState>
      </div>
    </>
  )
}

```

## file-select 组件

### basic.stories.tsx

```typescript
import React from 'react'
import FileSelect from '@hi-ui/file-select'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="file-select-basic__wrap">
        <FileSelect onSelect={console.log}>Upload</FileSelect>
      </div>
    </>
  )
}

```

## filter 组件

### appearance.stories.tsx

```typescript
import React from 'react'
import Filter from '@hi-ui/filter'

/**
 * @title 设置选中时的形状
 */
export const Appearance = () => {
  const [dataStore] = React.useState([
    {
      id: 1,
      title: '小米商城',
    },
    {
      id: 2,
      title: '米家有品',
    },
    {
      id: 3,
      title: '京东商城',
    },
    {
      id: 4,
      title: '天猫淘宝',
    },
    {
      id: 5,
      title: '创新渠道',
    },
    {
      id: 6,
      title: '线下KA',
    },
    {
      id: 7,
      title: '线下KA1',
    },
    {
      id: 8,
      title: '线下KA2',
    },
    {
      id: 9,
      title: '线下KA3',
    },
    {
      id: 10,
      title: '线下KA4',
    },
  ])

  const [dataColor] = React.useState([
    {
      id: 1,
      title: '深空',
    },
    {
      id: 2,
      title: '白色',
    },
    {
      id: 3,
      title: '亮黑色',
    },
    {
      id: 4,
      title: '金色',
    },
  ])

  return (
    <>
      <h1>Appearance</h1>
      <div className="filter-appearance__wrap">
        <h2>link</h2>
        <Filter
          label={['渠道']}
          appearance="link"
          defaultValue={[1]}
          data={dataStore}
          onChange={(value) => {
            console.log('value', value)
          }}
        />
        <Filter
          label={['颜色']}
          appearance="link"
          defaultValue={[1]}
          data={dataColor}
          onChange={(value) => {
            console.log('value', value)
          }}
        />
        <h2>filled</h2>
        <Filter
          label={['渠道']}
          appearance="filled"
          defaultValue={[1]}
          data={dataStore}
          onChange={(value) => {
            console.log('value', value)
          }}
        />
        <Filter
          label={['颜色']}
          appearance="filled"
          defaultValue={[1]}
          data={dataColor}
          onChange={(value) => {
            console.log('value', value)
          }}
        />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Filter from '@hi-ui/filter'

/**
 * @title 基础用法
 * @desc 一般作为筛选场景，作为筛选项
 */
export const Basic = () => {
  const [dataStore] = React.useState([
    {
      id: 1,
      title: '小米商城',
    },
    {
      id: 2,
      title: '米家有品',
    },
    {
      id: 3,
      title: '京东商城',
    },
    {
      id: 4,
      title: '天猫淘宝',
    },
    {
      id: 5,
      title: '创新渠道',
    },
    {
      id: 6,
      title: '线下KA',
    },
    {
      id: 7,
      title: '线下KA1',
    },
    {
      id: 8,
      title: '线下KA2',
    },
    {
      id: 9,
      title: '线下KA3',
    },
    {
      id: 10,
      title: '线下KA4',
    },
  ])

  const [dataColor] = React.useState([
    {
      id: 1,
      title: '深空',
    },
    {
      id: 2,
      title: '白色',
    },
    {
      id: 3,
      title: '亮黑色',
    },
    {
      id: 4,
      title: '金色',
    },
  ])

  return (
    <>
      <h1>Basic</h1>
      <div className="filter-basic__wrap">
        <Filter
          label={['渠道']}
          defaultValue={[1]}
          data={dataStore}
          onChange={(value) => {
            console.log('value', value)
          }}
        />
        <Filter
          label={['颜色']}
          defaultValue={[1]}
          data={dataColor}
          onChange={(value) => {
            console.log('value', value)
          }}
        />
      </div>
    </>
  )
}

```

### cascade.stories.tsx

```typescript
import React from 'react'
import Filter from '@hi-ui/filter'

/**
 * @title 级联选择
 * @desc 一般作为筛选场景，作为筛选项组合,每个级别之间有联动
 */
export const Cascade = () => {
  return (
    <>
      <h1>Cascade</h1>
      <div className="filter-cascade__wrap">
        <Filter
          label={['渠道', '分店', '机型']}
          defaultValue={[2, 21]}
          data={[
            {
              id: 1,
              title: '小米商城',
              children: [
                {
                  id: 11,
                  title: '小米商城',
                },
                {
                  id: 12,
                  title: '米家优品',
                  disabled: true,
                },
              ],
            },
            {
              id: 2,
              title: '米家有品',
              children: [
                {
                  id: 21,
                  title: '五彩城店',
                  children: [
                    {
                      id: '小米9',
                      title: '小米9',
                    },
                    {
                      id: '小米MIXS',
                      title: '小米MIXS',
                    },
                    {
                      id: '小米8',
                      title: '小米8',
                    },
                  ],
                },
                {
                  id: 22,
                  title: '清河店',
                },
                {
                  id: 23,
                  title: '西三旗店',
                },
              ],
            },

            {
              id: 3,
              title: '京东商城',
              children: [
                {
                  id: 31,
                  title: '小米直营',
                  children: [
                    {
                      id: '线下KA',
                      title: '线下KA',
                    },
                  ],
                },
              ],
            },
          ]}
        />
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import Filter from '@hi-ui/filter'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [value, setValue] = React.useState<React.ReactText[]>([2, 21])

  const data = [
    {
      id: 1,
      title: '小米商城',
      children: [
        {
          id: 11,
          title: '小米商城',
        },
        {
          id: 12,
          title: '米家优品',
          disabled: true,
        },
      ],
    },
    {
      id: 2,
      title: '米家有品',
      children: [
        {
          id: 21,
          title: '五彩城店',
          children: [
            {
              id: '小米9',
              title: '小米9',
            },
            {
              id: '小米MIXS',
              title: '小米MIXS',
            },
            {
              id: '小米8',
              title: '小米8',
            },
          ],
        },
        {
          id: 22,
          title: '清河店',
        },
        {
          id: 23,
          title: '西三旗店',
        },
      ],
    },

    {
      id: 3,
      title: '京东商城',
      children: [
        {
          id: 31,
          title: '小米直营',
          children: [
            {
              id: '线下KA',
              title: '线下KA',
            },
          ],
        },
      ],
    },
  ]

  return (
    <>
      <h1>Controlled</h1>
      <div className="filter-controlled__wrap">
        <Filter
          label={['渠道', '分店', '机型']}
          value={value}
          onChange={(ids, targetItem) => {
            console.log('onChange', ids, targetItem)
            setValue(ids)
          }}
          data={data}
        />
      </div>
    </>
  )
}

```

### underlined.stories.tsx

```typescript
import React from 'react'
import Filter from '@hi-ui/filter'

/**
 * @title 下划线
 */
export const Underlined = () => {
  return (
    <>
      <h1>Underlined</h1>
      <div className="filter-underline__wrap">
        <Filter
          showUnderline
          label={['渠道', '分店', '机型']}
          defaultValue={[2, 21]}
          data={[
            {
              id: 1,
              title: '小米商城',
              children: [
                {
                  id: 11,
                  title: '小米商城',
                },
                {
                  id: 12,
                  title: '米家优品',
                  disabled: true,
                },
              ],
            },
            {
              id: 2,
              title: '米家有品',
              children: [
                {
                  id: 21,
                  title: '五彩城店',
                  children: [
                    {
                      id: '小米9',
                      title: '小米9',
                    },
                    {
                      id: '小米MIXS',
                      title: '小米MIXS',
                    },
                    {
                      id: '小米8',
                      title: '小米8',
                    },
                  ],
                },
                {
                  id: 22,
                  title: '清河店',
                },
                {
                  id: 23,
                  title: '西三旗店',
                },
              ],
            },

            {
              id: 3,
              title: '京东商城',
              children: [
                {
                  id: 31,
                  title: '小米直营',
                  children: [
                    {
                      id: '线下KA',
                      title: '线下KA',
                    },
                  ],
                },
              ],
            },
          ]}
        />
      </div>
    </>
  )
}

```

## form 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Form from '@hi-ui/form'
import Input from '@hi-ui/input'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const FormItem = Form.Item

  return (
    <>
      <h1>Basic</h1>
      <div className="form-basic__wrap" style={{ width: 400 }}>
        <Form
          initialValues={{ testInput: 1, testInput2: 'testInput2' }}
          // validateTrigger={['onBlur']}
          labelWidth={80}
          rules={{
            testInput: [
              {
                // name: 'max',
                // strategy: 10,
                max: 100,
                type: 'number',
                message: 'max is 100',
              },
            ],
            testInput2: [
              {
                // name: 'required',
                // strategy: true,
                required: true,
                type: 'string',
                message: 'testInput2 is required',
              },
            ],
          }}
        >
          <FormItem field="testInput" valueType="number" label="用户名">
            <Input onChange={console.log} />
          </FormItem>
          <FormItem field="testInput2" valueType="string" label="密码">
            <Input />
          </FormItem>
        </Form>
      </div>
    </>
  )
}

```

### cascade.stories.tsx

```typescript
import React from 'react'
import Form, { FormHelpers } from '@hi-ui/form'
import Button from '@hi-ui/button'
import message from '@hi-ui/message'
import Select from '@hi-ui/select'
import { Counter } from '@hi-ui/counter'
import Checkbox from '@hi-ui/checkbox'
import { DatePicker } from '@hi-ui/date-picker'
import { Cascader } from '@hi-ui/cascader'
import Radio from '@hi-ui/radio'
import { Switch } from '@hi-ui/switch'
import { Rating } from '@hi-ui/rating'
import { Upload } from '@hi-ui/upload'

/**
 * @title 表单联动
 * @desc 根据数据控制某个表单的显示隐藏或校验规则
 */
export const Cascade = () => {
  const FormItem = Form.Item
  const FormReset = Form.Reset
  const FormSubmit = Form.Submit

  const CheckboxGroup = Checkbox.Group
  const RadioGroup = Radio.Group

  const formRef = React.useRef<FormHelpers>(null)
  const [formData, setFormData] = React.useState<any>({
    controlCounter: 'show',
    select: '3',
    counter: 3,
    radio: 0,
    rating: 3,
    checkbox: [],
    switch: false,
  })

  return (
    <>
      <h1>表单联动</h1>
      <div className="form-cascade__wrap">
        <Form
          labelWidth="140"
          labelPlacement="right"
          innerRef={formRef}
          initialValues={formData}
          onValuesChange={(changedValues, allValues) => {
            console.log('changedValues,allValues', changedValues, allValues)
            setFormData(allValues)
          }}
        >
          <FormItem label="表单名称" field={null} valueType={null}>
            <>动态表单</>
          </FormItem>
          <FormItem label="控制Counter" field="controlCounter" valueType="string">
            <Select
              clearable={false}
              style={{ width: 300 }}
              data={[
                {
                  id: 'hide',
                  title: '隐藏Counter',
                },
                {
                  id: 'show',
                  title: '显示Counter',
                },
              ]}
              placeholder="控制Counter的显示隐藏"
              onChange={(ids) => {
                console.log('select ids', ids)
              }}
            />
          </FormItem>

          {formData.controlCounter === 'show' ? (
            <FormItem label="Counter" field="counter" required valueType="number">
              <Counter step={1} min={-10} max={10} />
            </FormItem>
          ) : null}

          <FormItem
            label="Checkbox"
            field="checkbox"
            validateTrigger="onChange"
            rules={[
              {
                required: true,
              },
            ]}
            valueType="array"
          >
            <CheckboxGroup
              data={[
                { id: 'DatePicker', title: 'DatePicker' },
                { id: 'Cascader', title: 'Cascader' },
                { id: 'Radio', title: 'Radio' },
              ]}
              onChange={(data) => console.log('Checkbox data', data)}
            ></CheckboxGroup>
          </FormItem>

          {formData.checkbox.includes('DatePicker') && (
            <FormItem label="DatePicker" field="datePicker" required={true} valueType="array">
              <DatePicker
                type="daterange"
                onChange={(date, dateStr) => {
                  console.log('onChange DatePicker', date, dateStr)
                }}
              />
            </FormItem>
          )}
          {/* TODO: 动态切换时，是否移除脏数据，但是初始数据必然有额外数据，移除同名字段数据显然不合理 */}
          {formData.checkbox.includes('Cascader') && (
            <FormItem label="Cascader" field="Cascader" valueType="string">
              <Cascader
                onChange={(id) => {
                  console.log('Cascader change id', id)
                }}
                data={[
                  {
                    id: '手机',
                    title: '手机',
                    children: [
                      {
                        id: '小米',
                        title: '小米',
                        children: [
                          {
                            id: '小米3',
                            title: '小米3',
                          },
                          {
                            id: '小米4',
                            title: '小米4',
                          },
                        ],
                      },
                      {
                        id: '红米',
                        title: '红米',
                        children: [
                          {
                            id: '红米3',
                            title: '红米3',
                          },
                          {
                            id: '红米4',
                            title: '红米4',
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: '电视',
                    title: '电视',
                    children: [
                      {
                        id: '小米电视4A',
                        title: '小米电视4A',
                      },
                      {
                        id: '小米电视4C',
                        title: '小米电视4C',
                      },
                    ],
                  },
                ]}
                style={{ width: 300 }}
              />
            </FormItem>
          )}
          {formData.checkbox.includes('Radio') && (
            <FormItem label="Radio" field="radio" valueType="string">
              <RadioGroup
                data={[
                  { id: 0, title: '手机类' },
                  { id: 1, title: '电脑类' },
                  { id: 2, title: '生活类' },
                ]}
                onChange={(data) => console.log('radio data', data)}
              ></RadioGroup>
            </FormItem>
          )}

          <FormItem label="Switch" field="switch" valueType="boolean">
            <Switch content={['ON', 'OFF']} onChange={(val) => console.log('change Switch', val)} />
          </FormItem>

          <FormItem label="Rating" field="rating" valueType="number">
            <Rating />
          </FormItem>
          <FormItem label="Upload" field="upload" valueType="string" contentPosition="top">
            <Upload
              type="photo"
              uploadAction="http://www.mocky.io/v2/5dc3b4413000007600347501"
              onChange={(file, fileList, response) => {
                console.log('upload callback', file, fileList, response)
              }}
              onRemove={(file, fileList, index) => {
                console.log('remove callback', file, fileList, index)
                return new Promise((resolve) => resolve(true))
              }}
              name={'files[]'}
              defaultFileList={[
                {
                  name: 'b.png',
                  fileType: 'img',
                  uploadState: 'success',
                  url: 'https://i1.mifile.cn/f/i/2018/mix3/specs_black.png',
                },
              ]}
            />
          </FormItem>

          <FormItem field={null} valueType={null}>
            <>
              <FormSubmit
                type="primary"
                onClick={() => {
                  // console.log('Get form value:', values, errors)
                  const values = formRef.current.getFieldsValue()
                  message.open({
                    title: (
                      <div style={{ width: 400, wordBreak: 'break-all' }}>
                        {JSON.stringify(values)}
                      </div>
                    ),
                  })
                }}
              >
                提交
              </FormSubmit>

              <FormReset
                onClick={() => {
                  console.log('reset form')
                }}
              >
                重置
              </FormReset>

              <Button
                type="primary"
                appearance="link"
                onClick={() => {
                  console.log('填充表单')

                  formRef.current.setFieldsValue({
                    select: '2',
                    phone: '15666666666',
                    radio: 0,
                    rating: 4,
                    counter: 0,
                    switch: false,
                    datePicker: { start: new Date(), end: new Date() },
                    checkbox: ['Phone', 'Computer'],
                    cascader: ['电视', '小米电视4C'],
                  })
                }}
              >
                fill Form
              </Button>
            </>
          </FormItem>
        </Form>
      </div>
    </>
  )
}

```

### get-values.stories.tsx

```typescript
import React from 'react'
import Form, { FormHelpers } from '@hi-ui/form'
import Input from '@hi-ui/input'
import Button from '@hi-ui/button'
import message from '@hi-ui/message'

/**
 * @title 获取表单值
 * @desc 静默获取表单值：不触发校验
 */
export const GetValues = () => {
  const FormItem = Form.Item

  const formRef = React.useRef<FormHelpers>(null)

  return (
    <>
      <h1>获取表单值</h1>
      <div className="form-get-values__wrap" style={{ width: 400 }}>
        <Form
          initialValues={{
            phone: '',
            name: '',
          }}
          labelPlacement="left"
          labelWidth={80}
          innerRef={formRef}
        >
          <FormItem
            label="手机号"
            field="phone"
            valueType="string"
            validateTrigger="onChange"
            rules={[
              {
                validator: (rule, value, callback) => {
                  const telReg = /^[1][3|4|5|6|7|8|9][0-9]{9}$/
                  if (!value) {
                    callback(new Error('请输入手机号'))
                  } else if (!telReg.test(value)) {
                    callback(new Error('请输入正确的手机号'))
                  } else {
                    callback()
                  }
                },
              },
            ]}
          >
            <Input placeholder="请输入手机号" style={{ width: 200 }} />
          </FormItem>
          <FormItem required={true} label="姓名" field="name" valueType="string">
            <Input placeholder="请输入" style={{ width: 200 }} />
          </FormItem>
          <FormItem valueType={null} field={null} showValidateMessage={false}>
            <Button
              type="primary"
              onClick={() => {
                const values = formRef.current.getFieldsValue()
                console.log('获取表单值, 但是不触发校验方法', values)
                message.open({
                  title: JSON.stringify(values),
                })
              }}
            >
              获取表单值
            </Button>
          </FormItem>
        </Form>
      </div>
    </>
  )
}

```

### label-placement.stories.tsx

```typescript
import React from 'react'
import Form, { FormHelpers } from '@hi-ui/form'
import Input from '@hi-ui/input'

/**
 * @title 对齐方式
 * @desc 表单项较少，对应标题字数易对齐工整
 */
export const LabelPlacement = () => {
  const FormItem = Form.Item
  const FormSubmit = Form.Submit

  const formRef = React.useRef<FormHelpers>(null)

  return (
    <>
      <h1>LabelPlacement</h1>
      <div className="form-label-placement__wrap">
        <div>
          <h2>左对齐</h2>
          <div>
            <Form
              innerRef={formRef}
              initialValues={{ productCode: '', productName: '' }}
              labelWidth="100"
              labelPlacement="left"
            >
              <FormItem required={true} label="编码" field="productCode" valueType="string">
                <Input placeholder="请输入" />
              </FormItem>
              <FormItem required={true} label="产品名称" field="productName" valueType="string">
                <Input placeholder="请输入" />
              </FormItem>
              <FormItem label="" field="productName" valueType="string">
                <FormSubmit
                  type="primary"
                  onClick={() => {
                    console.log('Get form value:', formRef.current?.getFieldsValue())
                  }}
                >
                  提交
                </FormSubmit>
              </FormItem>
            </Form>
            <br />
          </div>
        </div>

        <div>
          <h2>右对齐</h2>
          <div>
            <Form
              innerRef={formRef}
              initialValues={{ productCode: '', productName: '' }}
              labelWidth="100"
              labelPlacement="right"
            >
              <FormItem required={true} label="编码" field="productCode" valueType="string">
                <Input placeholder="请输入" />
              </FormItem>
              <FormItem required={true} label="产品名称" field="productName" valueType="string">
                <Input placeholder="请输入" />
              </FormItem>
              <FormItem label="" field="productName" valueType="string">
                <FormSubmit
                  type="primary"
                  onClick={() => {
                    console.log('Get form value:', formRef.current?.getFieldsValue())
                  }}
                >
                  提交
                </FormSubmit>
              </FormItem>
            </Form>
            <br />
          </div>
        </div>

        <div>
          <h2>顶对齐</h2>
          <div>
            <Form
              innerRef={formRef}
              initialValues={{ productCode: '', productName: '' }}
              labelWidth="100"
              labelPlacement="top"
            >
              <FormItem required={true} label="编码" field="productCode" valueType="string">
                <Input placeholder="请输入" />
              </FormItem>
              <FormItem required={true} label="产品名称" field="productName" valueType="string">
                <Input placeholder="请输入" />
              </FormItem>
              <FormItem label="" field="productName" valueType="string">
                <FormSubmit
                  type="primary"
                  onClick={() => {
                    console.log('Get form value:', formRef.current?.getFieldsValue())
                  }}
                >
                  提交
                </FormSubmit>
              </FormItem>
            </Form>
            <br />
          </div>
        </div>
      </div>
    </>
  )
}

```

### list.stories.tsx

```typescript
import React from 'react'
import Form, { FormListHelper } from '@hi-ui/form'
import Input from '@hi-ui/input'
import Button from '@hi-ui/button'

/**
 * @title 动态表单组
 * @desc 动态 Form 删减表单组
 */
export const List = () => {
  const FormItem = Form.Item
  const FormList = Form.List

  const formListRef = React.useRef<FormListHelper>(null)

  return (
    <>
      <h1>List</h1>
      <div className="form-list__wrap">
        <div style={{ textAlign: 'right', marginBottom: '1em' }}>
          <Button onClick={() => formListRef.current?.add({ username: '', password: '' })}>
            动态添加成组表单
          </Button>
        </div>
        <Form
          initialValues={{ testInput: 'testInput', testInput2: 'testInput2' }}
          labelWidth={110}
          rules={{
            testInput: [
              {
                // name: 'max',
                // strategy: 10,
                max: 10,
                message: 'max is 10',
              },
            ],
            testInput2: [
              {
                // name: 'required',
                // strategy: true,
                required: true,
                message: 'testInput2 is required',
              },
            ],
          }}
        >
          <FormItem field="testInput" valueType="string" label="供应商">
            <Input />
          </FormItem>
          <FormItem field="testInput2" valueType="string" label="供应渠道">
            <Input />
          </FormItem>
          <FormList name="testList" innerRef={formListRef}>
            {(fields, { add, remove, insertBefore, swap, move }) => {
              return (
                <div>
                  {fields.map((field, index) => {
                    return (
                      <div key={index}>
                        <FormItem
                          field={['testList', index, 'username']}
                          valueType="string"
                          label={`材料名称${index + 1}`}
                          required
                          rules={[
                            {
                              required: true,
                              message: '请输入',
                            },
                          ]}
                        >
                          <Input />
                        </FormItem>
                        <FormItem
                          field={['testList', index, 'password']}
                          valueType="string"
                          label={`材料颜色${index + 1}`}
                        >
                          <Input />
                        </FormItem>
                        <FormItem field={null} valueType={null}>
                          <div>
                            <Button size="sm" type="danger" onClick={() => remove(index)}>
                              删除
                            </Button>
                            <Button
                              size="sm"
                              onClick={() => insertBefore(index, { username: '', password: '' })}
                            >
                              在该组之前插入
                            </Button>
                            <Button size="sm" onClick={() => move(index, 0)}>
                              移到数组索引 0 位置
                            </Button>
                            <Button size="sm" onClick={() => swap(index, 0)}>
                              和第一个置换值
                            </Button>
                          </div>
                        </FormItem>
                      </div>
                    )
                  })}
                  <Button onClick={() => add({ username: '', password: '' })}>
                    动态添加成组表单
                  </Button>
                </div>
              )
            }}
          </FormList>
        </Form>
      </div>
    </>
  )
}

```

### nested-field.stories.tsx

```typescript
import React from 'react'
import Form, { FormHelpers } from '@hi-ui/form'
import Input from '@hi-ui/input'
import Checkbox from '@hi-ui/checkbox'
import message from '@hi-ui/message'

/**
 * @title 字段嵌套
 */
export const NestedField = () => {
  const FormItem = Form.Item
  const FormReset = Form.Reset
  const FormSubmit = Form.Submit

  const formRef = React.useRef<FormHelpers>(null)

  return (
    <>
      <h1>字段嵌套</h1>
      <div className="form-nested-field__wrap" style={{ width: 400 }}>
        <Form
          innerRef={formRef}
          labelWidth="80"
          labelPlacement="left"
          initialValues={{
            login: {
              phone: '',
              password: '',
            },
            remember: true,
          }}
          onValuesChange={(changedValues, allValues) => {
            console.log('changedValues:', changedValues, 'allValues:', allValues)
          }}
        >
          <FormItem
            label="账号"
            field={['login', 'phone']}
            valueType="string"
            rules={[
              {
                required: true,
                validator: (rule, value, callback) => {
                  const telReg = /^[1][3|4|5|6|7|8|9][0-9]{9}$/
                  if (!value) {
                    callback(new Error('请输入手机号'))
                  } else if (!telReg.test(value)) {
                    callback(new Error('请输入正确的手机号'))
                  } else {
                    callback()
                  }
                },
              },
            ]}
          >
            <Input placeholder="请输入手机号" />
          </FormItem>
          <FormItem
            label="密码"
            valueType="string"
            field={['login', 'password']}
            rules={[
              {
                required: true,
              },
            ]}
          >
            <Input type="password" placeholder="请输入" />
          </FormItem>
          <FormItem
            field="remember"
            valuePropName="checked"
            valueType="boolean"
            valueChangeFuncPropName="onChange"
            // valueDispatchTransform={(evt) => {
            //   console.log('valueSync', evt)
            //   return evt.target.checked
            // }}
          >
            <Checkbox
            // onChange={() => {
            //   console.log('checkbox remember me')
            // }}
            >
              记住我
            </Checkbox>
          </FormItem>
          <FormItem valueType={null} field={null}>
            <>
              <FormSubmit
                type="primary"
                onClick={() => {
                  const values = formRef.current.getFieldsValue()
                  console.log('获取表单值, 但是不触发校验方法', values)

                  message.open({
                    title: JSON.stringify(values),
                  })
                }}
              >
                提交
              </FormSubmit>
              <FormReset
                onClick={() => {
                  console.log('reset form')
                }}
              >
                重置
              </FormReset>
            </>
          </FormItem>
        </Form>
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import React from 'react'
import Form from '@hi-ui/form'
import Input from '@hi-ui/input'
import Button from '@hi-ui/button'

/**
 * @title 横向表单
 * @desc 适用于筛选或查询数据的场景，和表格配合使用
 */
export const Placement = () => {
  const FormItem = Form.Item

  return (
    <>
      <h1>Placement</h1>
      <div className="form-label-placement__wrap" style={{ width: 900 }}>
        <Form
          initialValues={{
            account: '',
            password: '',
          }}
          placement="horizontal"
          labelPlacement="right"
        >
          <FormItem label="账号" labelWidth="58" field="account" valueType="string">
            <Input placeholder={'请输入'} />
          </FormItem>
          <FormItem label="密码" labelWidth="58" field="password" valueType="string">
            <Input type="password" placeholder={'请输入'} />
          </FormItem>
          <FormItem>
            <Button>提交</Button>
          </FormItem>
        </Form>
      </div>
    </>
  )
}

```

### render.stories.tsx

```typescript
import React from 'react'
import Form from '@hi-ui/form'
import Input from '@hi-ui/input'

/**
 * @title 自定义渲染表单控件
 */
export const Render = () => {
  const FormItem = Form.Item

  return (
    <>
      <h1>Render</h1>
      <div className="form-render__wrap" style={{ width: 400 }}>
        <Form
          initialValues={{ testInput: 'testInput', testInput2: 'testInput2' }}
          // validateTrigger={['onBlur']}
          labelWidth={80}
          rules={{
            testInput: [
              {
                max: 10,
                message: 'max is 10',
              },
            ],
            testInput2: [
              {
                required: true,
                message: 'testInput2 is required',
              },
            ],
          }}
        >
          <FormItem field="testInput" valueType="string" label="用户名">
            <Input />
          </FormItem>
          <FormItem
            field="testInput2"
            valueType="string"
            label="密码"
            contentPosition="bottom"
            render={(props) => {
              return (
                <div>
                  <span>我是示例提示，请注意大小写哦</span>
                  <Input {...props} />
                </div>
              )
            }}
          />
        </Form>
      </div>
    </>
  )
}

```

### scroll-to-error.stories.tsx

```typescript
import React from 'react'
import Form, { FormHelpers, FormRules } from '@hi-ui/form'
import Input from '@hi-ui/input'
import { Select } from '@hi-ui/select'
import { Cascader } from '@hi-ui/cascader'
import Radio from '@hi-ui/radio'
import Button from '@hi-ui/button'

/**
 * @title 滑动到错误字段
 * @desc 校验失败时，表单会自动滚动至第一个未通过的表单项
 */
export const ScrollToError = () => {
  const FormItem = Form.Item
  const RadioGroup = Radio.Group

  const formRef = React.useRef<FormHelpers>(null)

  const [cascaderOptions] = React.useState([
    {
      id: '手机',
      title: '手机',
      children: [
        {
          id: '小米',
          title: '小米',
          children: [
            {
              id: '小米3',
              title: '小米3',
            },
            {
              id: '小米4',
              title: '小米4',
            },
          ],
        },
        {
          id: '红米',
          title: '红米',
          children: [
            {
              id: '红米3',
              title: '红米3',
            },
            {
              id: '红米4',
              title: '红米4',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4A',
        },
        {
          id: '小米电视4C',
          title: '小米电视4C',
        },
      ],
    },
  ])

  const [rules] = React.useState<FormRules>({
    region: [
      {
        required: true,
        message: '请选择区域',
      },
    ],
    store: [
      {
        required: true,
        message: '请选择门店',
      },
    ],
    count: [
      {
        required: true,
        validator: (rule, value, cb) => {
          const count = +value
          if (isNaN(count)) {
            cb(new Error('请输入数字'))
          } else if (count <= 0) {
            cb(new Error('必须是正数'))
          } else {
            cb()
          }
        },
      },
    ],
  })

  return (
    <>
      <h1>ScrollToError</h1>
      <div
        className="form-scroll-to-error__wrap"
        style={{
          width: '100%',
          height: 240,
          padding: '20px 0',
          background: '#f5f7fa',
          boxShadow: '1px 2px 8px #ddd',
          overflow: 'auto',
        }}
      >
        <div
          style={{
            width: 400,
          }}
        >
          <Form
            innerRef={formRef}
            rules={rules}
            scrollToFirstError
            labelWidth="80"
            labelPlacement="right"
            initialValues={{
              user: { name: '' },
              name: '',
              region: '',
              count: '',
              store: '',
            }}
          >
            <FormItem
              label="名称"
              field={['user', 'name']}
              valueType="string"
              validateTrigger={['onBlur', 'onChange']}
              rules={[
                {
                  required: true,
                  message: '请输入名称',
                },
              ]}
            >
              <Input placeholder="请输入" />
            </FormItem>
            <FormItem label="数量" field="count" valueType="string">
              <Input placeholder="请输入" />
            </FormItem>
            <FormItem label="门店" field="store" valueType="string">
              <Select
                data={[
                  { title: '电视', id: '3' },
                  { title: '手机', id: '2' },
                  { title: '笔记本', id: '4' },
                  { title: '生活周边', id: '5' },
                  { title: '办公', id: '6' },
                ]}
                searchable
                placeholder="请选择"
                emptyContent="无匹配数据"
                onChange={(item) => {
                  console.log('多选结果', item)
                }}
              />
            </FormItem>
            <FormItem label="品类" field="category" valueType="string">
              <Cascader
                onChange={(id) => {
                  console.log('change', id)
                }}
                data={cascaderOptions}
                style={{ width: '100%' }}
              />
            </FormItem>
            <FormItem label="地区" field="region" valueType="string">
              <RadioGroup
                data={[
                  { id: 'beijing', title: '北京' },
                  { id: 'shanghai', title: '上海' },
                  { id: 'chongqing', title: '重庆' },
                ]}
              />
            </FormItem>

            <FormItem>
              <>
                <Button
                  type="primary"
                  onClick={() => {
                    console.log(formRef.current?.getFieldsValue())

                    formRef.current
                      ?.validate()
                      .then((values) => {
                        console.log('values', values)
                      })
                      .catch((errors) => {
                        console.log('error', errors)
                      })
                  }}
                >
                  提交
                </Button>
                <Button
                  type="default"
                  onClick={() => {
                    formRef.current?.reset()
                  }}
                >
                  重置
                </Button>
                <Button
                  type="danger"
                  onClick={() => {
                    formRef.current?.clearValidates()
                  }}
                >
                  清除校验信息
                </Button>
              </>
            </FormItem>
          </Form>
        </div>
      </div>
    </>
  )
}

```

### set-values.stories.tsx

```typescript
import React from 'react'
import Form, { FormHelpers } from '@hi-ui/form'
import Input from '@hi-ui/input'
import Button from '@hi-ui/button'
import { Select } from '@hi-ui/select'
import Grid from '@hi-ui/grid'

/**
 * @title 设置表单值
 * @desc 控制表单项的值
 */
export const SetValues = () => {
  const { Row, Col } = Grid
  const FormItem = Form.Item
  const FormSubmit = Form.Submit
  const FormReset = Form.Reset

  const formRef = React.useRef<FormHelpers>(null)

  const [singleList] = React.useState([
    { title: '电视', id: '3', disabled: true },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: true },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>填充表单</h1>
      <div className="form-set-values__wrap" style={{ width: 400 }}>
        <Form
          labelWidth="80"
          labelPlacement="right"
          innerRef={formRef}
          initialValues={{
            phone: '',
            select: '3',
          }}
        >
          <Row gutter>
            <Col>
              <FormItem
                label="Input"
                field="phone"
                valueType="string"
                validateTrigger="onChange"
                rules={[
                  {
                    validator: (rule, value, callback) => {
                      const telReg = /^[1][3|4|5|6|7|8|9][0-9]{9}$/
                      if (!value) {
                        callback(new Error('请输入手机号'))
                      } else if (!telReg.test(value)) {
                        callback(new Error('请输入正确的手机号'))
                      } else {
                        callback()
                      }
                    },
                  },
                ]}
              >
                <Input placeholder="请输入手机号" style={{ width: 200 }} />
              </FormItem>
            </Col>
            <Col>
              <Button appearance="link" style={{ lineHeight: '32px' }} type="secondary">
                Help?
              </Button>
            </Col>
          </Row>
          <FormItem label="Select" field="select" required={true} valueType="string">
            <Select
              clearable={false}
              style={{ width: 200 }}
              data={singleList}
              onChange={(ids) => {
                console.log('select ids', ids)
              }}
            />
          </FormItem>
          <FormItem field={null} valueType={null}>
            <>
              <FormSubmit
                type="primary"
                onClick={() => {
                  console.log('Get form value:', formRef.current.getFieldsValue())
                }}
              >
                提交
              </FormSubmit>
              <FormReset
                onClick={() => {
                  console.log('reset form')
                }}
              >
                重置
              </FormReset>
              <Button
                type="primary"
                appearance="link"
                onClick={() => {
                  console.log('填充表单')
                  formRef.current.setFieldsValue({
                    phone: '15688888888',
                    select: '2',
                  })
                }}
              >
                fill Form
              </Button>
            </>
          </FormItem>
        </Form>
      </div>
    </>
  )
}

```

### validate-field.stories.tsx

```typescript
import React from 'react'
import Form, { FormHelpers } from '@hi-ui/form'
import Input from '@hi-ui/input'
import Button from '@hi-ui/button'
import Grid from '@hi-ui/grid'

/**
 * @title 校验指定表单项
 * @desc 针对单个表单控件值进行校验
 */
export const ValidateField = () => {
  const { Row, Col } = Grid
  const FormItem = Form.Item
  const FormReset = Form.Reset
  const FormSubmit = Form.Submit

  const formRef = React.useRef<FormHelpers>(null)

  const [formData, setFormData] = React.useState<any>({
    phone: '',
    passwordConfirm: '',
    password: '',
    code: '',
  })

  const [countDown, setCountDown] = React.useState(60)
  const [codeDisabled, setCodeDisabled] = React.useState(false)

  const getCode = () => {
    const countDownTimer = setInterval(() => {
      if (countDown - 1 <= 0) {
        clearInterval(countDownTimer)
        setCountDown(60)
        setCodeDisabled(false)
        return
      }

      setCountDown((prev) => prev - 1)
    }, 1000)
  }

  return (
    <>
      <h1>ValidateField</h1>
      <div className="form-validate-field__wrap" style={{ width: 400 }}>
        <Form
          labelWidth="100"
          labelPlacement="right"
          innerRef={formRef}
          initialValues={{
            phone: '',
            passwordConfirm: '',
            password: '',
            code: '',
          }}
          onValuesChange={(changedValues, allValues) => {
            console.log('onValuesChange', changedValues, allValues)
            setFormData(allValues)
          }}
        >
          <FormItem
            label="手机号"
            field="phone"
            valueType="number"
            validateTrigger="onChange"
            rules={[
              {
                validator: (rule, value, callback) => {
                  const telReg = /^[1][3|4|5|6|7|8|9][0-9]{9}$/

                  if (!value) {
                    callback(new Error('请输入手机号'))
                  } else if (!telReg.test(value)) {
                    callback(new Error('请输入正确的手机号'))
                  } else {
                    callback()
                  }
                },
              },
            ]}
          >
            <Input placeholder="请输入手机号" style={{ width: 240 }} />
          </FormItem>
          <Row gutter={20}>
            <Col span={14}>
              <FormItem
                label="验证码"
                field="code"
                valueType="string"
                validateTrigger="onChange"
                rules={[
                  {
                    validator: (rule, value, callback) => {
                      const telReg = /^[0-9]{6}$/
                      if (!value) {
                        callback(new Error('请输入手机号'))
                      } else if (!telReg.test(value)) {
                        callback(new Error('请输入正确的验证码'))
                      } else {
                        callback()
                      }
                    },
                  },
                ]}
              >
                <Input placeholder="请输入验证码" style={{ width: 130 }} />
              </FormItem>
            </Col>
            <Col span={10}>
              <Button
                type="primary"
                disabled={codeDisabled && countDown <= 60 && countDown >= 0}
                onClick={() => {
                  console.log(1113)

                  formRef.current.validateField('phone').then((values) => {
                    console.log('values', values)
                    setCodeDisabled(true)
                    getCode()
                  })
                }}
              >
                {countDown < 60 && countDown >= 0 ? `获取中(${countDown})` : '获取验证码'}
              </Button>
            </Col>
          </Row>
          <FormItem
            label="密码"
            field="password"
            valueType="string"
            validateTrigger="onChange"
            rules={[
              {
                validator: (rule, value, callback) => {
                  const telReg = /^(?![^a-zA-Z]+$)(?!\D+$).{8,16}$/
                  if (!value) {
                    callback(new Error('请输入密码'))
                  } else if (!telReg.test(value)) {
                    callback(new Error('请输入包括数字和字母、长度8到16位的密码组合'))
                  } else {
                    callback()
                  }
                },
              },
            ]}
          >
            <Input type="password" placeholder="请输入" style={{ width: 240 }} />
          </FormItem>

          <FormItem
            label="确认密码"
            field="passwordConfirm"
            valueType="string"
            validateTrigger="onChange"
            rules={[
              {
                validator: (rule, value, callback) => {
                  console.log(value, formData.password)

                  if (value !== formData.password) {
                    callback(new Error('两次密码不同'))
                  } else {
                    callback()
                  }
                },
              },
            ]}
          >
            <Input type="password" placeholder="请再次输入密码" style={{ width: 240 }} />
          </FormItem>

          <FormItem valueType={null} field={null}>
            <>
              <FormSubmit
                type="primary"
                onClick={() => {
                  console.log('Get form value:', formRef.current.getFieldsValue())
                }}
              >
                提交
              </FormSubmit>
              <FormReset
                type="default"
                onClick={() => {
                  console.log('reset form')
                }}
              >
                重置
              </FormReset>
            </>
          </FormItem>
        </Form>
      </div>
    </>
  )
}

```

### validate-message.stories.tsx

```typescript
import React from 'react'
import Form from '@hi-ui/form'
import Input from '@hi-ui/input'
import Button from '@hi-ui/button'
import Card from '@hi-ui/card'

/**
 * @title 是否显示校验提示
 * @desc 适用于无需展示校验提示的场景
 */
export const ValidateMessage = () => {
  const FormItem = Form.Item

  return (
    <>
      <h1>ValidateMessage</h1>
      <div className="form-validate-message__wrap" style={{ width: 900 }}>
        <Card>
          <Form
            initialValues={{}}
            placement="horizontal"
            labelPlacement="right"
            showValidateMessage={false}
          >
            <FormItem label="商品ID" labelWidth="100" valueType="string">
              <Input placeholder={'请输入'} />
            </FormItem>
            <FormItem label="商品分类" labelWidth="100" valueType="string">
              <Input placeholder={'请输入'} />
            </FormItem>
            <FormItem showValidateMessage={false}>
              <Button>查询</Button>
            </FormItem>
          </Form>
        </Card>
      </div>
    </>
  )
}

```

### validate.stories.tsx

```typescript
import React from 'react'
import Form, { FormHelpers, FormRules } from '@hi-ui/form'
import Input from '@hi-ui/input'
import { Select } from '@hi-ui/select'
import { Cascader } from '@hi-ui/cascader'
import Radio from '@hi-ui/radio'
import Button from '@hi-ui/button'

/**
 * @title 表单校验
 * @desc 可在Form中配置全部Item的rules,也可在Form.Item中使用rules校验单个表单项
 */
export const Validate = () => {
  const FormItem = Form.Item
  const RadioGroup = Radio.Group

  const formRef = React.useRef<FormHelpers>(null)

  const [cascaderOptions] = React.useState([
    {
      id: '手机',
      title: '手机',
      children: [
        {
          id: '小米',
          title: '小米',
          children: [
            {
              id: '小米3',
              title: '小米3',
            },
            {
              id: '小米4',
              title: '小米4',
            },
          ],
        },
        {
          id: '红米',
          title: '红米',
          children: [
            {
              id: '红米3',
              title: '红米3',
            },
            {
              id: '红米4',
              title: '红米4',
            },
          ],
        },
      ],
    },
    {
      id: '电视',
      title: '电视',
      children: [
        {
          id: '小米电视4A',
          title: '小米电视4A',
        },
        {
          id: '小米电视4C',
          title: '小米电视4C',
        },
      ],
    },
  ])

  const [rules] = React.useState<FormRules>({
    region: [
      {
        required: true,
        message: '请选择区域',
      },
    ],
    store: [
      {
        required: true,
        message: '请选择门店',
      },
    ],
    count: [
      {
        required: true,
        validator: (rule, value, cb) => {
          const count = +value
          if (isNaN(count)) {
            cb(new Error('请输入数字'))
          } else if (count <= 0) {
            cb(new Error('必须是正数'))
          } else {
            cb()
          }
        },
      },
    ],
  })

  return (
    <>
      <h1>Validate</h1>
      <div className="form-validate__wrap" style={{ width: 400 }}>
        <Form
          innerRef={formRef}
          rules={rules}
          // lazyValidate
          labelWidth="80"
          labelPlacement="right"
          initialValues={{
            user: { name: '' },
            name: '',
            region: '',
            count: '',
            store: '',
          }}
        >
          <FormItem
            label="名称"
            field={['user', 'name']}
            valueType="string"
            validateTrigger={['onBlur', 'onChange']}
            rules={[
              {
                required: true,
                message: '请输入名称',
              },
            ]}
          >
            <Input placeholder="请输入" />
          </FormItem>
          <FormItem label="数量" field="count" valueType="string">
            <Input placeholder="请输入" />
          </FormItem>
          <FormItem label="门店" field="store" valueType="string">
            <Select
              data={[
                { title: '电视', id: '3' },
                { title: '手机', id: '2' },
                { title: '笔记本', id: '4' },
                { title: '生活周边', id: '5' },
                { title: '办公', id: '6' },
              ]}
              searchable
              placeholder="请选择"
              emptyContent="无匹配数据"
              onChange={(item) => {
                console.log('多选结果', item)
              }}
            />
          </FormItem>
          <FormItem label="品类" field="category" valueType="string">
            <Cascader
              onChange={(id) => {
                console.log('change', id)
              }}
              data={cascaderOptions}
              style={{ width: '100%' }}
            />
          </FormItem>
          <FormItem label="地区" field="region" valueType="string">
            <RadioGroup
              data={[
                { id: 'beijing', title: '北京' },
                { id: 'shanghai', title: '上海' },
                { id: 'chongqing', title: '重庆' },
              ]}
            />
          </FormItem>

          <FormItem>
            <>
              <Button
                type="primary"
                onClick={() => {
                  console.log(formRef.current?.getFieldsValue())

                  formRef.current
                    ?.validate()
                    .then((values) => {
                      console.log('values', values)
                    })
                    .catch((errors) => {
                      console.log('error', errors)
                    })
                }}
              >
                提交
              </Button>
              <Button
                type="default"
                onClick={() => {
                  formRef.current?.reset()
                }}
              >
                重置
              </Button>
              <Button
                type="danger"
                onClick={() => {
                  formRef.current?.clearValidates()
                }}
              >
                清除校验信息
              </Button>
            </>
          </FormItem>
        </Form>
      </div>
    </>
  )
}

```

## grid 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Grid from '@hi-ui/grid'

/**
 * @title 基础用法
 * @desc 无间隔水平排列
 */
export const Basic = () => {
  const { Row, Col } = Grid

  const blockStyle: React.CSSProperties = {
    width: '100%',
    padding: '16px 0',
    textAlign: 'center',
    opacity: '1',
    color: '#fff',
  }

  return (
    <>
      <h1>Basic</h1>
      <div className="grid-basic__wrap">
        <Row>
          <Col span={24}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-24</div>
          </Col>
        </Row>
        <Row>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>
              col-6
              <br />
              25%
            </div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>
              col-6
              <br />
              25%
            </div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>
              col-6
              <br />
              25%
            </div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>
              col-6
              <br />
              25%
            </div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>
              col-6
              <br />
              25%
            </div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>
              col-6
              <br />
              25%
            </div>
          </Col>
        </Row>
      </div>
    </>
  )
}

```

### gutter.stories.tsx

```typescript
import React from 'react'
import Grid from '@hi-ui/grid'

/**
 * @title 区块间隔
 * @desc 在 Row 设置 gutter = true 来使水平排列有间隔
 */
export const Gutter = () => {
  const { Row, Col } = Grid

  const blockStyle: React.CSSProperties = {
    width: '100%',
    padding: '16px 0',
    textAlign: 'center',
    opacity: '1',
    color: '#fff',
  }

  return (
    <>
      <h1>Gutter</h1>
      <div className="grid-gutter__wrap">
        <Row gutter={true}>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>
              col-6
              <br />
              25%
            </div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>
              col-6
              <br />
              25%
            </div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>
              col-6
              <br />
              25%
            </div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>
              col-6
              <br />
              25%
            </div>
          </Col>
        </Row>
      </div>
    </>
  )
}

```

### justify.stories.tsx

```typescript
import React from 'react'
import Grid from '@hi-ui/grid'

/**
 * @title 对齐排列
 * @desc 设置 justify 来指定对齐方式
 */
export const Justify = () => {
  const { Row, Col } = Grid

  const blockStyle: React.CSSProperties = {
    width: '100%',
    padding: '16px 0',
    textAlign: 'center',
    opacity: '1',
    color: '#fff',
  }

  return (
    <>
      <h1>Justify</h1>
      <div className="grid-justify">
        <Row justify="center" gutter={true}>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-6</div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-6</div>
          </Col>
        </Row>
        <Row justify="space-between" gutter={true}>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-6</div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-6</div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-6</div>
          </Col>
        </Row>
      </div>
    </>
  )
}

```

### nested.stories.tsx

```typescript
import React from 'react'
import Grid from '@hi-ui/grid'

/**
 * @title 嵌套
 * @desc 嵌套栅格来完成布局
 */
export const Nested = () => {
  const { Row, Col } = Grid

  const blockStyle: React.CSSProperties = {
    width: '100%',
    padding: '16px 0',
    textAlign: 'center',
    opacity: '1',
    color: '#fff',
  }

  return (
    <>
      <h1>Nested</h1>
      <div className="grid-nested__wrap">
        <Row gutter={true}>
          <Col span={16}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>
              col-16
              <Row gutter={8}>
                <Col span={12}>
                  <div style={{ ...blockStyle, backgroundColor: '#237ffa', opacity: 1 }}>
                    col-12
                  </div>
                </Col>
                <Col span={12}>
                  <div style={{ ...blockStyle, backgroundColor: '#237ffa', opacity: 1 }}>
                    col-12
                  </div>
                </Col>
              </Row>
            </div>
          </Col>
          <Col span={8}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-4</div>
          </Col>
        </Row>
      </div>
    </>
  )
}

```

### offset.stories.tsx

```typescript
import React from 'react'
import Grid from '@hi-ui/grid'

/**
 * @title 左右偏移
 * @desc 设置 offset 来指定左右的偏移量
 */
export const Offset = () => {
  const { Row, Col } = Grid

  const blockStyle: React.CSSProperties = {
    width: '100%',
    padding: '16px 0',
    textAlign: 'center',
    opacity: '1',
    color: '#fff',
  }

  return (
    <>
      <h1>Offset</h1>
      <div className="grid-offset__wrap">
        <Row gutter={true}>
          <Col span={8}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-8</div>
          </Col>
          <Col span={6} offset={6}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>col-6-offset-6</div>
          </Col>
          <Col span={4}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-4</div>
          </Col>
        </Row>
        <Row gutter={true}>
          <Col span={4}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-4</div>
          </Col>
          <Col span={6} offset={4}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>col-6-offset-4</div>
          </Col>
          <Col span={4}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-4</div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>col-6</div>
          </Col>
        </Row>
      </div>
    </>
  )
}

```

### order.stories.tsx

```typescript
import React from 'react'
import Grid from '@hi-ui/grid'

/**
 * @title 重排序
 * @desc 通过配置 order 优化 Grid 项的展示空间的排序位置
 */
export const Order = () => {
  const { Row, Col } = Grid

  const blockStyle: React.CSSProperties = {
    width: '100%',
    padding: '16px 0',
    textAlign: 'center',
    opacity: '1',
    color: '#fff',
  }

  return (
    <>
      <h1>Order</h1>
      <div className="grid-order__wrap">
        <Row>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>
              <div>1号空间</div>
              <div>序号：未定义</div>
            </div>
          </Col>
          <Col span={6} order={-1}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>
              <div>2号空间</div>
              <div>序号：-1</div>
            </div>
          </Col>
          <Col span={6} order={24}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>
              <div>3号空间</div>
              <div>序号：24</div>
            </div>
          </Col>
          <Col span={6}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>
              <div>4号空间</div>
              <div>序号：未定义</div>
            </div>
          </Col>
        </Row>
      </div>
    </>
  )
}

```

### responsive.stories.tsx

```typescript
import React from 'react'
import Grid from '@hi-ui/grid'

/**
 * @title 响应式
 * @desc 配置 span 在不同屏幕宽度下所包含的栅格数，支持 { xs, sm, md, lg, xl } 设置。请通过改变窗口宽度查看示例效果
 */
export const Responsive = () => {
  const { Row, Col } = Grid

  const blockStyle: React.CSSProperties = {
    width: '100%',
    padding: '16px 0',
    textAlign: 'center',
    opacity: '1',
    color: '#fff',
  }

  return (
    <>
      <h1>Responsive</h1>
      <div className="grid-responsive__wrap">
        <h2>span</h2>
        <Row>
          <Col span={{ xs: 24, md: 12, lg: 6 }}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>.xs-24 .md-12 .lg-6</div>
          </Col>
          <Col span={{ xs: 24, md: 12, lg: 6 }}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>.xs-24 .md-12 .lg-6</div>
          </Col>
          <Col span={{ xs: 24, md: 12, lg: 6 }}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>.xs-24 .md-12 .lg-6</div>
          </Col>
          <Col span={{ xs: 24, md: 12, lg: 6 }}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>.xs-24 .md-12 .lg-6</div>
          </Col>
        </Row>

        <h2>offset</h2>
        <Row>
          <Col span={{ xs: 12, md: 8 }}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>.xs-12 .md-8</div>
          </Col>
          <Col span={{ xs: 12, md: 8 }} offset={{ xs: 6, md: 0 }}>
            <div style={{ ...blockStyle, backgroundColor: '#fab007' }}>xs-12 .md-8</div>
          </Col>
          <Col span={{ xs: 12, md: 8 }} offset={{ xs: 12, md: 0 }}>
            <div style={{ ...blockStyle, backgroundColor: '#237ffa' }}>xs-12 .md-8</div>
          </Col>
        </Row>
      </div>
    </>
  )
}

```

## highlighter 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Highlighter from '@hi-ui/highlighter'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="highlighter-basic__wrap">
        <Highlighter keyword="高亮">我想要高亮的文案是：高亮</Highlighter>
      </div>
    </>
  )
}

```

## icon-button 组件

### basic.stories.tsx

```typescript
import React from 'react'
import IconButton from '@hi-ui/icon-button'
import { CloseOutlined } from '@hi-ui/icons'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="icon-button-basic__wrap">
        <IconButton icon={<CloseOutlined />} />
        <br />
        <br />
        <IconButton icon={<CloseOutlined />} active />
        <br />
        <br />
        <IconButton icon={<CloseOutlined />} effect />
        <br />
        <br />
        <IconButton icon={<CloseOutlined />} effect active />
        <br />
        <br />
        测试
        <IconButton icon={<CloseOutlined />} effect />
        文档流空间是否占用
      </div>
    </>
  )
}

```

## icons 组件

### basic.stories.tsx

```typescript
import React from 'react'
import * as Icons from '@hi-ui/icons'

/**
 * @title 基础用法
 */
export const Basic = () => {
  // import * as Icons from '@hi-ui/icons'
  const iconGroups = React.useMemo(() => {
    return [
      {
        id: 'alert',
        title: '提示',
        children: [
          {
            id: 'filled',
            title: '面型',
            children: [
              { component: Icons.CheckCircleFilled, tagName: 'CheckCircleFilled' },

              { component: Icons.CheckSquareFilled, tagName: 'CheckSquareFilled' },

              { component: Icons.CloseCircleFilled, tagName: 'CloseCircleFilled' },

              { component: Icons.MinusSquareFilled, tagName: 'MinusSquareFilled' },

              { component: Icons.ExclamationCircleFilled, tagName: 'ExclamationCircleFilled' },

              { component: Icons.InfoCircleFilled, tagName: 'InfoCircleFilled' },

              { component: Icons.QuestionCircleFilled, tagName: 'QuestionCircleFilled' },

              { component: Icons.StopFilled, tagName: 'StopFilled' },

              { component: Icons.WarningFilled, tagName: 'WarningFilled' },
            ],
          },
          {
            id: 'outlined',
            title: '线型',
            children: [
              { component: Icons.CheckOutlined, tagName: 'CheckOutlined' },

              { component: Icons.CheckCircleOutlined, tagName: 'CheckCircleOutlined' },

              { component: Icons.CheckSquareOutlined, tagName: 'CheckSquareOutlined' },

              { component: Icons.CloseOutlined, tagName: 'CloseOutlined' },

              { component: Icons.CloseCircleOutlined, tagName: 'CloseCircleOutlined' },

              { component: Icons.CloseSquareOutlined, tagName: 'CloseSquareOutlined' },

              { component: Icons.ExclamationOutlined, tagName: 'ExclamationOutlined' },

              { component: Icons.ExclamationCircleOutlined, tagName: 'ExclamationCircleOutlined' },

              { component: Icons.InfoOutlined, tagName: 'InfoOutlined' },

              { component: Icons.InfoCircleOutlined, tagName: 'InfoCircleOutlined' },

              { component: Icons.MinusOutlined, tagName: 'MinusOutlined' },

              { component: Icons.MinusSquareOutlined, tagName: 'MinusSquareOutlined' },

              { component: Icons.PlusOutlined, tagName: 'PlusOutlined' },

              { component: Icons.PlusSquareOutlined, tagName: 'PlusSquareOutlined' },

              { component: Icons.QuestionOutlined, tagName: 'QuestionOutlined' },

              { component: Icons.QuestionCircleOutlined, tagName: 'QuestionCircleOutlined' },

              { component: Icons.StopOutlined, tagName: 'StopOutlined' },

              { component: Icons.WarningOutlined, tagName: 'WarningOutlined' },
            ],
          },
        ],
      },
      {
        id: 'common',
        title: '通用',
        children: [
          {
            id: 'filled',
            title: '面型',
            children: [
              { component: Icons.AlarmFilled, tagName: 'AlarmFilled' },

              { component: Icons.AlarmClockFilled, tagName: 'AlarmClockFilled' },

              { component: Icons.AppStoreFilled, tagName: 'AppStoreFilled' },

              { component: Icons.ApproveFilled, tagName: 'ApproveFilled' },

              { component: Icons.ArchiveFilled, tagName: 'ArchiveFilled' },

              { component: Icons.AssetMonitorFilled, tagName: 'AssetMonitorFilled' },

              { component: Icons.AudioFilled, tagName: 'AudioFilled' },

              { component: Icons.BankCardFilled, tagName: 'BankCardFilled' },

              { component: Icons.BellFilled, tagName: 'BellFilled' },

              { component: Icons.BlockFilled, tagName: 'BlockFilled' },

              { component: Icons.BookmarkFilled, tagName: 'BookmarkFilled' },

              { component: Icons.BuildingFilled, tagName: 'BuildingFilled' },

              { component: Icons.BulbFilled, tagName: 'BulbFilled' },

              { component: Icons.CalculatorFilled, tagName: 'CalculatorFilled' },

              { component: Icons.CalendarFilled, tagName: 'CalendarFilled' },

              { component: Icons.CameraFilled, tagName: 'CameraFilled' },

              { component: Icons.CarFilled, tagName: 'CarFilled' },

              { component: Icons.CertificateFilled, tagName: 'CertificateFilled' },

              { component: Icons.ChatFilled, tagName: 'ChatFilled' },

              { component: Icons.CloudFilled, tagName: 'CloudFilled' },

              { component: Icons.CloudDownloadFilled, tagName: 'CloudDownloadFilled' },

              { component: Icons.CloudUploadFilled, tagName: 'CloudUploadFilled' },

              { component: Icons.CollectionFilled, tagName: 'CollectionFilled' },

              { component: Icons.DataMonitorFilled, tagName: 'DataMonitorFilled' },

              { component: Icons.DislikeFilled, tagName: 'DislikeFilled' },

              { component: Icons.DocumentFilled, tagName: 'DocumentFilled' },

              { component: Icons.DocumentExclamationFilled, tagName: 'DocumentExclamationFilled' },

              { component: Icons.EndDateFilled, tagName: 'EndDateFilled' },

              { component: Icons.ExpressionFilled, tagName: 'ExpressionFilled' },

              { component: Icons.FileFilled, tagName: 'FileFilled' },

              { component: Icons.FireFilled, tagName: 'FireFilled' },

              { component: Icons.FlagFilled, tagName: 'FlagFilled' },

              { component: Icons.FolderFilled, tagName: 'FolderFilled' },

              { component: Icons.FolderOpenFilled, tagName: 'FolderOpenFilled' },

              { component: Icons.HeartFilled, tagName: 'HeartFilled' },

              { component: Icons.HomeFilled, tagName: 'HomeFilled' },

              { component: Icons.KeyFilled, tagName: 'KeyFilled' },

              { component: Icons.LightningFilled, tagName: 'LightningFilled' },

              { component: Icons.LikeFilled, tagName: 'LikeFilled' },

              { component: Icons.LocationFilled, tagName: 'LocationFilled' },

              { component: Icons.LockFilled, tagName: 'LockFilled' },

              { component: Icons.MailFilled, tagName: 'MailFilled' },

              { component: Icons.MailOpenFilled, tagName: 'MailOpenFilled' },

              { component: Icons.MailSendFilled, tagName: 'MailSendFilled' },

              { component: Icons.ManFilled, tagName: 'ManFilled' },

              { component: Icons.MessageFilled, tagName: 'MessageFilled' },

              { component: Icons.MobileFilled, tagName: 'MobileFilled' },

              { component: Icons.MonitorFilled, tagName: 'MonitorFilled' },

              { component: Icons.MoonFilled, tagName: 'MoonFilled' },

              { component: Icons.PadFilled, tagName: 'PadFilled' },

              { component: Icons.PauseFilled, tagName: 'PauseFilled' },

              { component: Icons.PhoneFilled, tagName: 'PhoneFilled' },

              { component: Icons.PictureFilled, tagName: 'PictureFilled' },

              { component: Icons.PinFilled, tagName: 'PinFilled' },

              { component: Icons.PlayFilled, tagName: 'PlayFilled' },

              { component: Icons.PrinterFilled, tagName: 'PrinterFilled' },

              { component: Icons.QrCodeFilled, tagName: 'QrCodeFilled' },

              { component: Icons.RelationFilled, tagName: 'RelationFilled' },

              { component: Icons.RmbFilled, tagName: 'RmbFilled' },

              { component: Icons.SadFilled, tagName: 'SadFilled' },

              { component: Icons.SendOutFilled, tagName: 'SendOutFilled' },

              { component: Icons.SettingFilled, tagName: 'SettingFilled' },

              { component: Icons.ShieldFilled, tagName: 'ShieldFilled' },

              { component: Icons.ShoppingFilled, tagName: 'ShoppingFilled' },

              { component: Icons.ShoppingCartFilled, tagName: 'ShoppingCartFilled' },

              { component: Icons.SkinFilled, tagName: 'SkinFilled' },

              { component: Icons.SoundFilled, tagName: 'SoundFilled' },

              { component: Icons.StarFilled, tagName: 'StarFilled' },

              { component: Icons.StartDateFilled, tagName: 'StartDateFilled' },

              { component: Icons.StudentFilled, tagName: 'StudentFilled' },

              { component: Icons.SunFilled, tagName: 'SunFilled' },

              { component: Icons.TagFilled, tagName: 'TagFilled' },

              { component: Icons.TalkFilled, tagName: 'TalkFilled' },

              { component: Icons.TaskFilled, tagName: 'TaskFilled' },

              { component: Icons.TemplateFilled, tagName: 'TemplateFilled' },

              { component: Icons.TimeFilled, tagName: 'TimeFilled' },

              { component: Icons.ToolFilled, tagName: 'ToolFilled' },

              { component: Icons.TravelFilled, tagName: 'TravelFilled' },

              { component: Icons.TruckFilled, tagName: 'TruckFilled' },

              { component: Icons.UmbrellaFilled, tagName: 'UmbrellaFilled' },

              { component: Icons.UnlockFilled, tagName: 'UnlockFilled' },

              { component: Icons.UpdateFilled, tagName: 'UpdateFilled' },

              { component: Icons.UserFilled, tagName: 'UserFilled' },

              { component: Icons.VideoCameraFilled, tagName: 'VideoCameraFilled' },

              { component: Icons.VoiceFilled, tagName: 'VoiceFilled' },

              { component: Icons.WebpageFilled, tagName: 'WebpageFilled' },
            ],
          },
          {
            id: 'outlined',
            title: '线型',
            children: [
              { component: Icons.AlarmOutlined, tagName: 'AlarmOutlined' },

              { component: Icons.AlarmClockOutlined, tagName: 'AlarmClockOutlined' },

              { component: Icons.AppStoreOutlined, tagName: 'AppStoreOutlined' },

              { component: Icons.ApproveOutlined, tagName: 'ApproveOutlined' },

              { component: Icons.ArchiveOutlined, tagName: 'ArchiveOutlined' },

              { component: Icons.AssetMonitorOutlined, tagName: 'AssetMonitorOutlined' },

              { component: Icons.AssociateOutlined, tagName: 'AssociateOutlined' },

              { component: Icons.AudioOutlined, tagName: 'AudioOutlined' },

              { component: Icons.BankCardOutlined, tagName: 'BankCardOutlined' },

              { component: Icons.BarsOutlined, tagName: 'BarsOutlined' },

              { component: Icons.BellOutlined, tagName: 'BellOutlined' },

              { component: Icons.BlockOutlined, tagName: 'BlockOutlined' },

              { component: Icons.BookmarkOutlined, tagName: 'BookmarkOutlined' },

              { component: Icons.BuildingOutlined, tagName: 'BuildingOutlined' },

              { component: Icons.BulbOutlined, tagName: 'BulbOutlined' },

              {
                component: Icons.BusinessCardTransverseOutlined,
                tagName: 'BusinessCardTransverseOutlined',
              },

              { component: Icons.BusinessCardOutlined, tagName: 'BusinessCardOutlined' },

              { component: Icons.CalculatorOutlined, tagName: 'CalculatorOutlined' },

              { component: Icons.CalendarOutlined, tagName: 'CalendarOutlined' },

              { component: Icons.CameraOutlined, tagName: 'CameraOutlined' },

              { component: Icons.ChatOutlined, tagName: 'ChatOutlined' },

              { component: Icons.ChatForwardingOutlined, tagName: 'ChatForwardingOutlined' },

              { component: Icons.ClockOutlined, tagName: 'ClockOutlined' },

              { component: Icons.CloseCodeOutlined, tagName: 'CloseCodeOutlined' },

              { component: Icons.CloudOutlined, tagName: 'CloudOutlined' },

              { component: Icons.CloudDownloadOutlined, tagName: 'CloudDownloadOutlined' },

              { component: Icons.CloudUploadOutlined, tagName: 'CloudUploadOutlined' },

              { component: Icons.CompassOutlined, tagName: 'CompassOutlined' },

              { component: Icons.CustomerServiceOutlined, tagName: 'CustomerServiceOutlined' },

              { component: Icons.CollectionOutlined, tagName: 'CollectionOutlined' },

              { component: Icons.DataExportOutlined, tagName: 'DataExportOutlined' },

              { component: Icons.DataMonitorOutlined, tagName: 'DataMonitorOutlined' },

              { component: Icons.DiagramOutlined, tagName: 'DiagramOutlined' },

              { component: Icons.DislikeOutlined, tagName: 'DislikeOutlined' },

              { component: Icons.DocumentOutlined, tagName: 'DocumentOutlined' },

              {
                component: Icons.DocumentExclamationOutlined,
                tagName: 'DocumentExclamationOutlined',
              },

              { component: Icons.DownloadOutlined, tagName: 'DownloadOutlined' },

              { component: Icons.DragDotOutlined, tagName: 'DragDotOutlined' },

              { component: Icons.EndDateOutlined, tagName: 'EndDateOutlined' },

              { component: Icons.ExportOutlined, tagName: 'ExportOutlined' },

              { component: Icons.ExpressionOutlined, tagName: 'ExpressionOutlined' },

              { component: Icons.EyeOutlined, tagName: 'EyeOutlined' },

              { component: Icons.EyeInvisibleOutlined, tagName: 'EyeInvisibleOutlined' },

              { component: Icons.FileOutlined, tagName: 'FileOutlined' },

              { component: Icons.FileExcelOutlined, tagName: 'FileExcelOutlined' },

              { component: Icons.FileExeOutlined, tagName: 'FileExeOutlined' },

              { component: Icons.FileJpgOutlined, tagName: 'FileJpgOutlined' },

              { component: Icons.FileKeynoteOutlined, tagName: 'FileKeynoteOutlined' },

              { component: Icons.FileMusicOutlined, tagName: 'FileMusicOutlined' },

              { component: Icons.FilePdfOutlined, tagName: 'FilePdfOutlined' },

              { component: Icons.FilePptOutlined, tagName: 'FilePptOutlined' },

              { component: Icons.FileQuestionOutlined, tagName: 'FileQuestionOutlined' },

              { component: Icons.FileTxtOutlined, tagName: 'FileTxtOutlined' },

              { component: Icons.FileVideoOutlined, tagName: 'FileVideoOutlined' },

              { component: Icons.FileWordOutlined, tagName: 'FileWordOutlined' },

              { component: Icons.FileZipOutlined, tagName: 'FileZipOutlined' },

              { component: Icons.FireOutlined, tagName: 'FireOutlined' },

              { component: Icons.FlagOutlined, tagName: 'FlagOutlined' },

              { component: Icons.FolderOutlined, tagName: 'FolderOutlined' },

              { component: Icons.FolderOpenOutlined, tagName: 'FolderOpenOutlined' },

              { component: Icons.FreezeOutlined, tagName: 'FreezeOutlined' },

              { component: Icons.GlobalOutlined, tagName: 'GlobalOutlined' },

              { component: Icons.HangUpOutlined, tagName: 'HangUpOutlined' },

              { component: Icons.HeartOutlined, tagName: 'HeartOutlined' },

              { component: Icons.HeartSimpleOutlined, tagName: 'HeartSimpleOutlined' },

              { component: Icons.HomeOutlined, tagName: 'HomeOutlined' },

              { component: Icons.ImportOutlined, tagName: 'ImportOutlined' },

              { component: Icons.KeyOutlined, tagName: 'KeyOutlined' },

              { component: Icons.LightningOutlined, tagName: 'LightningOutlined' },

              { component: Icons.LikeOutlined, tagName: 'LikeOutlined' },

              { component: Icons.LinkOutlined, tagName: 'LinkOutlined' },

              { component: Icons.LocationOutlined, tagName: 'LocationOutlined' },

              { component: Icons.LockOutlined, tagName: 'LockOutlined' },

              { component: Icons.MailOutlined, tagName: 'MailOutlined' },

              { component: Icons.MailOpenOutlined, tagName: 'MailOpenOutlined' },

              { component: Icons.MailSendOutlined, tagName: 'MailSendOutlined' },

              { component: Icons.ManOutlined, tagName: 'ManOutlined' },

              { component: Icons.MenuOutlined, tagName: 'MenuOutlined' },

              { component: Icons.MessageOutlined, tagName: 'MessageOutlined' },

              { component: Icons.MobileOutlined, tagName: 'MobileOutlined' },

              { component: Icons.MonitorOutlined, tagName: 'MonitorOutlined' },

              { component: Icons.MoonOutlined, tagName: 'MoonOutlined' },

              { component: Icons.MoveOutlined, tagName: 'MoveOutlined' },

              { component: Icons.PadOutlined, tagName: 'PadOutlined' },

              { component: Icons.PauseOutlined, tagName: 'PauseOutlined' },

              { component: Icons.PhoneOutlined, tagName: 'PhoneOutlined' },

              { component: Icons.PictureOutlined, tagName: 'PictureOutlined' },

              { component: Icons.PinOutlined, tagName: 'PinOutlined' },

              { component: Icons.PlayOutlined, tagName: 'PlayOutlined' },

              { component: Icons.PowerOffOutlined, tagName: 'PowerOffOutlined' },

              { component: Icons.PrinterOutlined, tagName: 'PrinterOutlined' },

              { component: Icons.QrCodeOutlined, tagName: 'QrCodeOutlined' },

              { component: Icons.RelationOutlined, tagName: 'RelationOutlined' },

              { component: Icons.ResetOutlined, tagName: 'ResetOutlined' },

              { component: Icons.SealOutlined, tagName: 'SealOutlined' },

              { component: Icons.RmbOutlined, tagName: 'RmbOutlined' },

              { component: Icons.RobotOutlined, tagName: 'RobotOutlined' },

              { component: Icons.SadOutlined, tagName: 'SadOutlined' },

              { component: Icons.ScanOutlined, tagName: 'ScanOutlined' },

              { component: Icons.SearchOutlined, tagName: 'SearchOutlined' },

              { component: Icons.SendOutOutlined, tagName: 'SendOutOutlined' },

              { component: Icons.SettingOutlined, tagName: 'SettingOutlined' },

              { component: Icons.ShareOutlined, tagName: 'ShareOutlined' },

              { component: Icons.ShieldOutlined, tagName: 'ShieldOutlined' },

              { component: Icons.ShopOutlined, tagName: 'ShopOutlined' },

              { component: Icons.ShoppingOutlined, tagName: 'ShoppingOutlined' },

              { component: Icons.ShoppingCartOutlined, tagName: 'ShoppingCartOutlined' },

              { component: Icons.ShowCodeOutlined, tagName: 'ShowCodeOutlined' },

              { component: Icons.SkinOutlined, tagName: 'SkinOutlined' },

              { component: Icons.SoundOutlined, tagName: 'SoundOutlined' },

              { component: Icons.StarOutlined, tagName: 'StarOutlined' },

              { component: Icons.StartDateOutlined, tagName: 'StartDateOutlined' },

              { component: Icons.StudentOutlined, tagName: 'StudentOutlined' },

              { component: Icons.SunOutlined, tagName: 'SunOutlined' },

              { component: Icons.SwitchOutlined, tagName: 'SwitchOutlined' },

              { component: Icons.SynchronizeOutlined, tagName: 'SynchronizeOutlined' },

              { component: Icons.TagOutlined, tagName: 'TagOutlined' },

              { component: Icons.TalkOutlined, tagName: 'TalkOutlined' },

              { component: Icons.TaskOutlined, tagName: 'TaskOutlined' },

              { component: Icons.TemplateOutlined, tagName: 'TemplateOutlined' },

              { component: Icons.TextExtractionOutlined, tagName: 'TextExtractionOutlined' },

              { component: Icons.TimeOutlined, tagName: 'TimeOutlined' },

              { component: Icons.TimeRewindOutlined, tagName: 'TimeRewindOutlined' },

              { component: Icons.ToolOutlined, tagName: 'ToolOutlined' },

              { component: Icons.TravelOutlined, tagName: 'TravelOutlined' },

              { component: Icons.TruckOutlined, tagName: 'TruckOutlined' },

              { component: Icons.UmberOutlined, tagName: 'UmberOutlined' },

              { component: Icons.UmbrellaOutlined, tagName: 'UmbrellaOutlined' },

              { component: Icons.UnlockOutlined, tagName: 'UnlockOutlined' },

              { component: Icons.UpdateOutlined, tagName: 'UpdateOutlined' },

              { component: Icons.UploadOutlined, tagName: 'UploadOutlined' },

              { component: Icons.UserOutlined, tagName: 'UserOutlined' },

              { component: Icons.UserAddOutlined, tagName: 'UserAddOutlined' },

              { component: Icons.UsersOutlined, tagName: 'UsersOutlined' },

              { component: Icons.VideoCameraOutlined, tagName: 'VideoCameraOutlined' },

              { component: Icons.VipOutlined, tagName: 'VipOutlined' },

              { component: Icons.VoiceOutlined, tagName: 'VoiceOutlined' },

              { component: Icons.WebpageOutlined, tagName: 'WebpageOutlined' },

              { component: Icons.WomanOutlined, tagName: 'WomanOutlined' },
            ],
          },
        ],
      },
      {
        id: 'direction',
        title: '方向',
        children: [
          {
            id: 'filled',
            title: '面型',
            children: [
              { component: Icons.CaretDownFilled, tagName: 'CaretDownFilled' },

              { component: Icons.CaretLeftFilled, tagName: 'CaretLeftFilled' },

              { component: Icons.CaretRightFilled, tagName: 'CaretRightFilled' },

              { component: Icons.CaretUpFilled, tagName: 'CaretUpFilled' },
            ],
          },
          {
            id: 'outlined',
            title: '线型',
            children: [
              { component: Icons.ArrowDownOutlined, tagName: 'ArrowDownOutlined' },

              { component: Icons.ArrowLeftOutlined, tagName: 'ArrowLeftOutlined' },

              { component: Icons.ArrowRightOutlined, tagName: 'ArrowRightOutlined' },

              { component: Icons.ArrowUpOutlined, tagName: 'ArrowUpOutlined' },

              { component: Icons.DirectionDownOutlined, tagName: 'DirectionDownOutlined' },

              { component: Icons.DirectionLeftOutlined, tagName: 'DirectionLeftOutlined' },

              { component: Icons.DirectionRightOutlined, tagName: 'DirectionRightOutlined' },

              { component: Icons.DirectionUpOutlined, tagName: 'DirectionUpOutlined' },

              { component: Icons.DownOutlined, tagName: 'DownOutlined' },

              { component: Icons.ExpandOutlined, tagName: 'ExpandOutlined' },

              { component: Icons.FullscreenOutlined, tagName: 'FullscreenOutlined' },

              { component: Icons.FullscreenExitOutlined, tagName: 'FullscreenExitOutlined' },

              { component: Icons.LeftOutlined, tagName: 'LeftOutlined' },

              { component: Icons.LeftRightOutlined, tagName: 'LeftRightOutlined' },

              { component: Icons.MenuFoldOutlined, tagName: 'MenuFoldOutlined' },

              { component: Icons.MenuUnfoldOutlined, tagName: 'MenuUnfoldOutlined' },

              { component: Icons.RightOutlined, tagName: 'RightOutlined' },

              { component: Icons.ShrinkOutlined, tagName: 'ShrinkOutlined' },

              { component: Icons.ToBottomOutlined, tagName: 'ToBottomOutlined' },

              { component: Icons.ToTopOutlined, tagName: 'ToTopOutlined' },

              { component: Icons.UpOutlined, tagName: 'UpOutlined' },
            ],
          },
        ],
      },
      {
        id: 'edit',
        title: '编辑',
        children: [
          {
            id: 'filled',
            title: '面型',
            children: [
              { component: Icons.CopyFilled, tagName: 'CopyFilled' },
              { component: Icons.DeleteFilled, tagName: 'DeleteFilled' },
              { component: Icons.DetailsFilled, tagName: 'DetailsFilled' },
              { component: Icons.DuplicateFilled, tagName: 'DuplicateFilled' },
              { component: Icons.EditFilled, tagName: 'EditFilled' },
              { component: Icons.EllipsisCircleFilled, tagName: 'EllipsisCircleFilled' },
              { component: Icons.EmptyFilled, tagName: 'EmptyFilled' },
              { component: Icons.FilterFilled, tagName: 'FilterFilled' },
              { component: Icons.FolderAddFilled, tagName: 'FolderAddFilled' },
              { component: Icons.FolderMoveFilled, tagName: 'FolderMoveFilled' },
              { component: Icons.PasteFilled, tagName: 'PasteFilled' },
            ],
          },
          {
            id: 'outlined',
            title: '线型',
            children: [
              { component: Icons.AverageOutlined, tagName: 'AverageOutlined' },
              { component: Icons.ColumnHeightOutlined, tagName: 'ColumnHeightOutlined' },
              { component: Icons.ColumnsOutlined, tagName: 'ColumnsOutlined' },
              { component: Icons.CopyOutlined, tagName: 'CopyOutlined' },
              { component: Icons.DeleteOutlined, tagName: 'DeleteOutlined' },
              { component: Icons.DetailsOutlined, tagName: 'DetailsOutlined' },
              { component: Icons.DocumentSearchOutlined, tagName: 'DocumentSearchOutlined' },
              { component: Icons.DragOutlined, tagName: 'DragOutlined' },
              { component: Icons.DuplicateOutlined, tagName: 'DuplicateOutlined' },
              { component: Icons.EditOutlined, tagName: 'EditOutlined' },
              { component: Icons.EllipsisCircleOutlined, tagName: 'EllipsisCircleOutlined' },
              { component: Icons.EllipsisOutlined, tagName: 'EllipsisOutlined' },
              { component: Icons.EllipsisVerticalOutlined, tagName: 'EllipsisVerticalOutlined' },
              { component: Icons.EmptyOutlined, tagName: 'EmptyOutlined' },
              { component: Icons.EqualProportionOutlined, tagName: 'EqualProportionOutlined' },
              { component: Icons.FilterOutlined, tagName: 'FilterOutlined' },
              { component: Icons.FolderAddOutlined, tagName: 'FolderAddOutlined' },
              { component: Icons.FolderMoveOutlined, tagName: 'FolderMoveOutlined' },
              { component: Icons.FreezeColumnOutlined, tagName: 'FreezeColumnOutlined' },
              { component: Icons.FrozenLineOutlined, tagName: 'FrozenLineOutlined' },
              { component: Icons.PasteOutlined, tagName: 'PasteOutlined' },
              { component: Icons.RotateLeftOutlined, tagName: 'RotateLeftOutlined' },
              { component: Icons.RotateRightOutlined, tagName: 'RotateRightOutlined' },
              { component: Icons.SaveOutlined, tagName: 'SaveOutlined' },
              { component: Icons.ScissorOutlined, tagName: 'ScissorOutlined' },
              { component: Icons.SortAscendingOutlined, tagName: 'SortAscendingOutlined' },
              { component: Icons.SortDescendingOutlined, tagName: 'SortDescendingOutlined' },
              { component: Icons.SummationOutlined, tagName: 'SummationOutlined' },
              { component: Icons.TableOutlined, tagName: 'TableOutlined' },
              { component: Icons.ZoomInOutlined, tagName: 'ZoomInOutlined' },
              { component: Icons.ZoomOutOutlined, tagName: 'ZoomOutOutlined' },
            ],
          },
        ],
      },
      {
        id: 'data',
        title: '数据',
        children: [
          {
            id: 'outlined',
            title: '',
            children: [
              { component: Icons.BarChartOutlined, tagName: 'BarChartOutlined' },
              { component: Icons.LineChartOutlined, tagName: 'LineChartOutlined' },
              { component: Icons.PieChartOutlined, tagName: 'PieChartOutlined' },
              { component: Icons.StockChartOutlined, tagName: 'StockChartOutlined' },
            ],
          },
        ],
      },
      {
        id: 'file',
        title: '文件',
        children: [
          {
            id: 'colorful',
            title: '多色型',
            children: [
              { component: Icons.ExcelColorful, tagName: 'ExcelColorful' },

              { component: Icons.ExeColorful, tagName: 'ExeColorful' },

              { component: Icons.JpgColorful, tagName: 'JpgColorful' },

              { component: Icons.MusicColorful, tagName: 'MusicColorful' },

              { component: Icons.PdfColorful, tagName: 'PdfColorful' },

              { component: Icons.PptColorful, tagName: 'PptColorful' },

              { component: Icons.QuestionColorful, tagName: 'QuestionColorful' },

              { component: Icons.WordColorful, tagName: 'WordColorful' },

              { component: Icons.ZipColorful, tagName: 'ZipColorful' },
            ],
          },
        ],
      },
    ]
  }, [])

  const renderIcon = React.useCallback(({ component: Component, tagName }) => {
    return (
      <div
        style={{
          display: 'flex',
          flexDirection: 'column',
          alignItems: 'center',
          justifyContent: 'center',
          width: '200px',
          padding: '24px 0',
          margin: '12px',
          marginLeft: '0px',
          background: '#f2f4f7',
          borderRadius: '8px',
        }}
      >
        <Component style={{ fontSize: '32px' }} />
        <div style={{ marginTop: '24px', fontSize: '14px' }}>{tagName}</div>
      </div>
    )
  }, [])

  return (
    <>
      <h1>Icons</h1>
      <div className="icons-basic__wrap" style={{ marginTop: -24 }}>
        {iconGroups.map((groupItem) => {
          return (
            <React.Fragment key={groupItem.id}>
              <div style={{ lineHeight: '24px', fontSize: '20px', margin: '24px 0 16px' }}>
                {groupItem.title}
              </div>
              {groupItem.children.map((typeItem) => (
                <React.Fragment key={typeItem.id}>
                  <div style={{ lineHeight: '22px', fontSize: '16px', marginBottom: 8 }}>
                    {typeItem.title}
                  </div>
                  <div style={{ display: 'flex', flexWrap: 'wrap' }}>
                    {typeItem.children.map(renderIcon)}
                  </div>
                </React.Fragment>
              ))}
            </React.Fragment>
          )
        })}
      </div>
    </>
  )
}

```

## input 组件

### addon.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'
import { ExpressionOutlined, AudioOutlined, SearchOutlined, MessageOutlined } from '@hi-ui/icons'

/**
 * @title 前后外置元素
 * @desc 将输入框与外置的其他元素组合使用
 */
export const Addon = () => {
  return (
    <>
      <h1>Addon for Input</h1>
      <div className="input-addon__wrap">
        <h2>prefix or suffix</h2>
        <Input placeholder="请输入" prefix="http://" suffix=".com"></Input>
        <br />
        <br />
        <Input
          clearable
          clearableTrigger="always"
          placeholder="请输入"
          suffix={<SearchOutlined />}
        ></Input>
        <br />
        <br />
        <Input placeholder="请输入" prefix={<ExpressionOutlined />}></Input>
        <br />
        <br />
        <Input
          placeholder="请输入"
          prefix={<MessageOutlined />}
          suffix={
            <>
              <AudioOutlined style={{ marginRight: 4 }} />
              <ExpressionOutlined />
            </>
          }
        ></Input>
      </div>
      <br />
      <div className="input-addon__wrap">
        <h2>prepend or append</h2>
        <Input placeholder="请输入" prepend="http://" append=".com"></Input>
        <br />
        <br />
        <Input
          clearable
          clearableTrigger="always"
          placeholder="请输入"
          append={<SearchOutlined />}
        ></Input>
        <br />
        <br />
        <Input placeholder="请输入" prepend={<ExpressionOutlined />}></Input>
        <br />
        <br />
        <Input
          placeholder="请输入"
          prepend={<MessageOutlined />}
          append={
            <>
              <AudioOutlined style={{ marginRight: 4 }} />
              <ExpressionOutlined />
            </>
          }
        ></Input>
      </div>
      <div className="input-addon__wrap">
        <h2>mixin addon</h2>
        <Input
          size="md"
          clearable
          placeholder="请输入"
          prepend={<ExpressionOutlined />}
          suffix={<AudioOutlined />}
          append={<div>Send</div>}
        ></Input>
      </div>
    </>
  )
}

```

### appearance.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'
import { ExpressionOutlined, AudioOutlined, MessageOutlined } from '@hi-ui/icons'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性、无UI三种
 */
export const Appearance = () => {
  return (
    <>
      <h1>Appearance for Input</h1>
      <div className="input-appearance__wrap">
        <h2>outline</h2>
        <Input size="md" appearance="line" placeholder="请输入内容"></Input>
        <br />
        <br />
        <Input
          size="md"
          clearable
          placeholder="请输入"
          prepend={<ExpressionOutlined />}
          prefix={<MessageOutlined />}
          suffix={<AudioOutlined />}
          append={<div>Send</div>}
        ></Input>
        <br />
        <br />
        <h2>unset</h2>
        <Input size="md" appearance="unset" placeholder="请输入内容"></Input>
        <br />
        <br />
        <Input
          appearance="unset"
          size="md"
          clearable
          placeholder="请输入"
          prepend={<ExpressionOutlined />}
          prefix={<MessageOutlined />}
          suffix={<AudioOutlined />}
          append={<div>Send</div>}
        ></Input>
        <br />
        <br />
        <h2>filled</h2>
        <Input size="md" appearance="filled" placeholder="请输入内容"></Input>
        <br />
        <br />
        <Input
          appearance="filled"
          size="md"
          clearable
          placeholder="请输入"
          prepend={<ExpressionOutlined />}
          prefix={<MessageOutlined />}
          suffix={<AudioOutlined />}
          append={<div>Send</div>}
        ></Input>
        <br />
        <br />
        <h2>underline</h2>
        <Input size="md" appearance="underline" placeholder="请输入内容"></Input>
        <br />
        <br />
        <Input
          appearance="underline"
          size="md"
          clearable
          placeholder="请输入"
          prepend={<ExpressionOutlined />}
          prefix={<MessageOutlined />}
          suffix={<AudioOutlined />}
          append={<div>Send</div>}
        ></Input>
        <br />
        <br />
      </div>
    </>
  )
}

```

### auto-focus.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'

/**
 * @title 自动聚焦
 */
export const AutoFocus = () => {
  return (
    <>
      <h1>AutoFocus for Input</h1>
      <div className="input-auto-focus__wrap">
        <Input autoFocus placeholder="请输入"></Input>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'

/**
 * @title 基础用法
 * @desc 可获取有限长度的字符串，不折行显示
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic for Input</h1>
      <div className="input-basic__wrap">
        <Input placeholder="请输入" onChange={(e, t) => console.log(e.target.value, t)} />
      </div>
    </>
  )
}

```

### clearable.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'

/**
 * @title 可清除
 */
export const Clearable = () => {
  return (
    <>
      <h1>Clearable for Input</h1>
      <div className="input-clearable__wrap">
        <Input
          clearable
          placeholder="内容输入后只在 hover 时可清除"
          onChange={(e) => console.log('change', e.target.value)}
          onBlur={(e) => console.log('onBlur', e.target.value)}
        ></Input>
        <br />
        <br />
        <Input clearable clearableTrigger="always" placeholder="内容输入后就可清除"></Input>
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [value, setValue] = React.useState('我是输入文本')

  return (
    <>
      <h1>Controlled for Input</h1>
      <div className="input-controlled__wrap">
        <div style={{ fontSize: 14 }}>输入值：{value}</div>
        <Input
          style={{ marginTop: 8 }}
          placeholder="请输入"
          value={value}
          onChange={(e) => setValue(e.target.value)}
        />
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'

/**
 * @title 禁用状态
 */
export const Disabled = () => {
  return (
    <>
      <h1>Disabled for Input</h1>
      <div className="input-disabled__wrap">
        <h2>普通</h2>
        <div>
          <Input appearance="line" disabled placeholder="请输入"></Input>
          <br />
          <br />
          <Input appearance="unset" disabled placeholder="请输入"></Input>
          <br />
          <br />
          <Input appearance="filled" disabled placeholder="请输入"></Input>
        </div>
        <br />
        <h2>Invalid</h2>
        <div>
          <Input invalid appearance="line" disabled placeholder="请输入"></Input>
          <br />
          <br />
          <Input invalid appearance="unset" disabled placeholder="请输入"></Input>
          <br />
          <br />
          <Input invalid appearance="filled" disabled placeholder="请输入"></Input>
        </div>
        <br />
        <h2>有值</h2>
        <div>
          <Input clearable value="输入值" appearance="line" disabled placeholder="请输入"></Input>
          <br />
          <br />
          <Input clearable value="输入值" appearance="unset" disabled placeholder="请输入"></Input>
          <br />
          <br />
          <Input clearable value="输入值" appearance="filled" disabled placeholder="请输入"></Input>
        </div>
      </div>
    </>
  )
}

```

### focus.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'
import Button from '@hi-ui/button'

/**
 * @title 手动聚焦
 * @desc 通过 ref 获取 input 引用手动调用 focus 方法
 */
export const Focus = () => {
  const inputRef = React.useRef<any>(null)

  return (
    <>
      <h1>Focus for Input</h1>
      <div className="input-focus__wrap">
        <Button
          onClick={() => {
            inputRef.current?.focus()
          }}
        >
          手动聚焦
        </Button>
        <Input style={{ marginTop: 10 }} ref={inputRef} placeholder="请输入"></Input>
      </div>
    </>
  )
}

```

### group.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'
import { SearchOutlined } from '@hi-ui/icons'
import { Select } from '@hi-ui/select'
import { message } from '@hi-ui/message'
import Button from '@hi-ui/button'

/**
 * @title 组合
 */
export const Group = () => {
  return (
    <>
      <h1>Group for Input</h1>
      <div className="input-Group__wrap">
        <Input
          placeholder="请输入"
          prepend={
            <Select
              clearable={false}
              style={{ width: 80 }}
              data={[
                { title: '+86', id: '86' },
                { title: '+1', id: '1' },
                { title: '+33', id: '33' },
                { title: '+91', id: '91' },
              ]}
              defaultValue="86"
            />
          }
        />
        <br />
        <br />
        <Input
          clearable
          clearableTrigger="always"
          placeholder="请输入"
          append={
            <Button
              appearance="filled"
              type="primary"
              icon={<SearchOutlined />}
              onClick={() => {
                message.open({ type: 'success', title: '查询成功', duration: 2000 })
              }}
            />
          }
        />
      </div>
    </>
  )
}

```

### invalid.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'

/**
 * @title 无效状态
 */
export const Invalid = () => {
  return (
    <>
      <h1>Invalid for Input</h1>
      <div className="input-invalid__wrap">
        <div>
          <Input appearance="line" invalid placeholder="请输入"></Input>
          <br />
          <br />
          <Input appearance="unset" invalid placeholder="请输入"></Input>
          <br />
          <br />
          <Input appearance="filled" invalid placeholder="请输入"></Input>
          <br />
          <br />
          <Input appearance="underline" invalid placeholder="请输入"></Input>
        </div>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'
import { ExpressionOutlined, AudioOutlined } from '@hi-ui/icons'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>Size for Input</h1>
      <div className="input-size__wrap">
        <Input
          size="sm"
          placeholder="sm"
          prefix={<ExpressionOutlined />}
          suffix={<AudioOutlined style={{ marginRight: 4 }} />}
        ></Input>
        <br />
        <br />
        <Input
          size="md"
          placeholder="md"
          prefix={<ExpressionOutlined />}
          suffix={<AudioOutlined style={{ marginRight: 4 }} />}
        ></Input>
        <br />
        <br />
        <Input
          size="lg"
          placeholder="lg"
          prefix={<ExpressionOutlined />}
          suffix={<AudioOutlined style={{ marginRight: 4 }} />}
        ></Input>
      </div>
    </>
  )
}

```

### trim.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'

/**
 * @title 自动 Trim
 */
export const Trim = () => {
  return (
    <>
      <h1>Trim</h1>
      <div className="input-trim__wrap">
        <Input
          placeholder="请输入"
          onChange={(e) => console.log('change', e.target.value)}
          trimValueOnBlur
        ></Input>
        <br />
        <br />
        <Input disabled placeholder="请输入"></Input>
      </div>
    </>
  )
}

```

### type.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'

/**
 * @title 特殊格式
 * @desc 满足不同业务场景的特殊格式
 */
export const Type = () => {
  return (
    <>
      <h1>特殊格式</h1>
      <div className="input-type__wrap">
        <h2>身份证</h2>
        <Input
          type="id"
          style={{ width: 250 }}
          placeholder="请输入"
          clearable
          trimValueOnBlur
          onChange={(event, value) => {
            console.log(event.target.value, value)
          }}
        />
        <h2>手机号</h2>
        <Input
          type="tel"
          style={{ width: 250 }}
          placeholder="请输入"
          clearable
          trimValueOnBlur
          onChange={(event, value) => {
            console.log(event.target.value, value)
          }}
        />
        <h2>金额</h2>
        <Input
          type="amount"
          style={{ width: 250 }}
          placeholder="请输入"
          clearable
          trimValueOnBlur
          onChange={(event, value) => {
            console.log(event.target.value, value)
          }}
        />
        <h2>银行卡</h2>
        <Input
          type="card"
          style={{ width: 250 }}
          placeholder="请输入"
          clearable
          trimValueOnBlur
          onChange={(event, value) => {
            console.log(event.target.value, value)
          }}
        />
      </div>
    </>
  )
}

```

### with-tooltip.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'
import Tooltip from '@hi-ui/tooltip'

/**
 * @title 带Tooltip
 */
export const WithTooltip = () => {
  const [value, setValue] = React.useState('Tooltip')

  return (
    <>
      <h1>带Tooltip</h1>
      <div className="input-Tooltip__wrap">
        <Tooltip trigger="focus" title={value || '请输入'}>
          <Input
            placeholder="请输入"
            value={value}
            onChange={(e) => setValue(e.target.value)}
          ></Input>
        </Tooltip>
      </div>
    </>
  )
}

```

## input-group 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'
import Select from '@hi-ui/select'

import InputGroup from '@hi-ui/input-group'

/**
 * @title 基础用法
 * @desc 通过包裹多个表单控件，将它们进行组合展示
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="input-group-basic__wrap">
        <InputGroup>
          <Select
            style={{ width: '36%' }}
            data={[
              { id: 1, title: 'Option 1' },
              { id: 2, title: 'Option 2' },
            ]}
          />
          <Input />
        </InputGroup>
      </div>
    </>
  )
}

```

### group.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'
import Select from '@hi-ui/select'
import CheckSelect from '@hi-ui/check-select'
import Cascader from '@hi-ui/cascader'
import DatePicker from '@hi-ui/date-picker'
import Button from '@hi-ui/button'

import InputGroup from '@hi-ui/input-group'

/**
 * @title 不同组合形式
 * @desc 根据不同场景组合不同类型的表单控件
 */
export const Group = () => {
  return (
    <>
      <h1>Group</h1>
      <div
        className="input-group-group__wrap"
        style={{ display: 'flex', flexDirection: 'column', gap: 16 }}
      >
        {/* Input + button */}
        <InputGroup>
          <Input placeholder="请输入" />
          <Button type="primary">检索</Button>
        </InputGroup>

        <InputGroup>
          <Select
            style={{ width: '36%' }}
            data={[
              { id: 1, title: 'Option 1' },
              { id: 2, title: 'Option 2' },
            ]}
          />
          <Input placeholder="请输入" />
        </InputGroup>

        <InputGroup>
          <Input placeholder="请输入" />
          <Input placeholder="请输入" />
        </InputGroup>

        <InputGroup>
          <Select
            style={{ width: '36%' }}
            data={[
              { id: 1, title: 'Option 1' },
              { id: 2, title: 'Option 2' },
            ]}
          />
          <Input placeholder="请输入" />
          <Button type="primary">确定</Button>
        </InputGroup>

        <InputGroup>
          <CheckSelect
            style={{ width: '36%' }}
            data={[
              { id: 1, title: 'Option 1' },
              { id: 2, title: 'Option 2' },
            ]}
          />
          <CheckSelect
            style={{ width: '36%' }}
            data={[
              { id: 1, title: 'Option 1' },
              { id: 2, title: 'Option 2' },
            ]}
          />
          <Input placeholder="请输入" />
        </InputGroup>

        <InputGroup>
          <Cascader
            style={{ width: '36%' }}
            data={[
              { id: 1, title: 'Option 1' },
              { id: 2, title: 'Option 2' },
            ]}
          />
          <DatePicker placeholder="请输入" />
        </InputGroup>

        <InputGroup>
          <Select
            style={{ width: '36%' }}
            data={[
              { id: 1, title: 'Option 1' },
              { id: 2, title: 'Option 2' },
            ]}
          />
          <Cascader
            style={{ width: '36%' }}
            data={[
              {
                id: '1',
                title: 'Option 1',
                children: [
                  { id: '1-1', title: 'Option 1-1' },
                  { id: '1-2', title: 'Option 1-2' },
                ],
              },
              {
                id: 2,
                title: 'Option 2',
                children: [
                  { id: '2-1', title: 'Option 1-1' },
                  { id: '2-2', title: 'Option 1-2' },
                ],
              },
            ]}
          />
          <Input placeholder="请输入" />
        </InputGroup>

        <InputGroup>
          <Select
            style={{ width: '36%' }}
            data={[
              { id: 1, title: 'Option 1' },
              { id: 2, title: 'Option 2' },
            ]}
          />
          <DatePicker type="daterange" />
        </InputGroup>

        <InputGroup>
          <DatePicker type="daterange" placeholder={['开始时间', '结束时间']} />
          <Input style={{ width: '36%' }} placeholder="请输入" />
        </InputGroup>
      </div>
    </>
  )
}

```

## list 组件

### action.stories.tsx

```typescript
import React from 'react'
import List from '@hi-ui/list'

/**
 * @title 带操作
 */
export const Action = () => {
  return (
    <>
      <h1>带操作</h1>
      <div className="list-basic__wrap">
        <List
          style={{ marginBottom: 20 }}
          data={[
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
          ]}
          render={(dataItem) => {
            return <List.Item {...dataItem} />
          }}
        />
        <List
          style={{ marginBottom: 20 }}
          data={[
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
          ]}
          render={(dataItem) => {
            return <List.Item {...dataItem} actionPlacement={'top'} />
          }}
        />
        <List
          data={[
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
          ]}
          render={(dataItem) => {
            return <List.Item {...dataItem} actionPlacement={'bottom'} />
          }}
        />
      </div>
    </>
  )
}

```

### avatar.stories.tsx

```typescript
import React from 'react'
import List from '@hi-ui/list'
import Avatar from '@hi-ui/avatar'

/**
 * @title 自定义头像
 */
export const CustomAvatar = () => {
  return (
    <>
      <h1>CustomAvatar</h1>
      <div className="list-custom-avatar__wrap">
        <List
          data={[
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
          ]}
          render={(dataItem) => {
            console.log('dataItem', dataItem)

            return (
              <List.Item
                {...dataItem}
                avatar={<Avatar size={'lg'} shape={'square'} src={dataItem.avatar as string} />}
              />
            )
          }}
        />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import List from '@hi-ui/list'

/**
 * @title 基础用法
 * @desc 常用在数据管理、信息展示等领域
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="list-basic__wrap">
        <List
          data={[
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
          ]}
          render={(dataItem) => {
            return <List.Item {...dataItem} />
          }}
        />
      </div>
    </>
  )
}

```

### empty.stories.tsx

```typescript
import React from 'react'
import List from '@hi-ui/list'
import EmptyState, { EMPTY_STATE_IMAGE_NO_DATA_COLOURFUL } from '@hi-ui/empty-state'

/**
 * @title 数据为空
 */
export const Empty = () => {
  return (
    <>
      <h1>数据为空</h1>
      <div className="list-basic__wrap">
        <List
          data={[]}
          render={(dataItem) => {
            return <List.Item {...dataItem} />
          }}
          emptyContent={() => (
            <EmptyState
              indicator={EMPTY_STATE_IMAGE_NO_DATA_COLOURFUL}
              style={{ paddingBottom: 16 }}
            />
          )}
        />
      </div>
    </>
  )
}

```

### no-border.stories.tsx

```typescript
import React from 'react'
import List from '@hi-ui/list'

/**
 * @title 无边框
 * @desc 常用在搜索、动态发布信息流、附件等场景
 */
export const NoBordered = () => {
  return (
    <>
      <h1>NoBordered</h1>
      <div className="list-no-bordered__wrap">
        <List
          bordered={false}
          data={[
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
          ]}
          render={(dataItem) => {
            return <List.Item {...dataItem} />
          }}
        />
      </div>
    </>
  )
}

```

### no-split.stories.tsx

```typescript
import React from 'react'
import List from '@hi-ui/list'

/**
 * @title 不带分割线
 */
export const NoSplit = () => {
  return (
    <>
      <h1>不带分割线</h1>
      <div className="list-basic__wrap">
        <List
          split={false}
          data={[
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
          ]}
          render={(dataItem) => {
            return <List.Item {...dataItem} />
          }}
        />
      </div>
    </>
  )
}

```

### pagination.stories.tsx

```typescript
import React from 'react'
import List from '@hi-ui/list'

/**
 * @title 带分页
 */
export const Pagination = () => {
  return (
    <>
      <h1>带分页</h1>
      <div className="list-basic__wrap">
        <List
          data={[
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
          ]}
          pagination={{
            total: 200,
            pageSize: 10,
            placement: 'right',
          }}
          render={(dataItem) => {
            return <List.Item {...dataItem} />
          }}
        />
        <List
          style={{ marginBottom: 20 }}
          data={[
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
          ]}
          pagination={{
            total: 200,
            pageSize: 10,
            placement: 'left',
          }}
          render={(dataItem) => {
            return <List.Item {...dataItem} />
          }}
        />
        <List
          style={{ marginBottom: 20 }}
          data={[
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
            {
              title: '下单量-指标',
              description: '下单量在交易环节中整体用户下单的数量',
              extra: '最新使用：2019.12.23 下午07:07',
              avatar:
                'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png',
              action: '编辑',
            },
          ]}
          pagination={{
            total: 200,
            pageSize: 10,
            placement: 'middle',
          }}
          render={(dataItem) => {
            return <List.Item {...dataItem} />
          }}
        />
      </div>
    </>
  )
}

```

## loading 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Loading from '@hi-ui/loading'

/**
 * @title 基础用法
 * @desc 耐心等待，正拼力加载…
 */
export const Basic = () => {
  const loadingIdRef = React.useRef<any>(null)

  React.useEffect(() => {
    return () => {
      Loading.close(loadingIdRef.current)
    }
  }, [])

  return (
    <>
      <h1>Loading</h1>
      <div
        className="loading-basic__wrap"
        style={{ position: 'relative', width: 500, height: 300 }}
      >
        <Loading content="Loading..." delay={500}>
          <div
            style={{
              width: 500,
              height: 300,
              boxSizing: 'border-box',
              background: '#f5f7fa',
              padding: 20,
              border: '20px solid #5f6a7a',
            }}
          />
        </Loading>
      </div>
    </>
  )
}

```

### duration.stories.tsx

```typescript
import React from 'react'
import Loading from '@hi-ui/loading'
import Button from '@hi-ui/button'

/**
 * @title API调用
 */
export const Duration = () => {
  const loadingIdRef = React.useRef<any>(null)

  React.useEffect(() => {
    return () => {
      Loading.close(loadingIdRef.current)
    }
  }, [])

  return (
    <>
      <h1>Loading</h1>
      <div className="loading-duration__wrap">
        <Button
          onClick={() => {
            loadingIdRef.current = Loading.open(undefined, { duration: 3000 })
          }}
        >
          Awake by API
        </Button>
      </div>
    </>
  )
}

```

### type.stories.tsx

```typescript
import React from 'react'
import Loading from '@hi-ui/loading'

/**
 * @title 设置加载指示符类型
 */
export const Type = () => {
  return (
    <>
      <h1>Type</h1>
      <div
        className="loading-basic__wrap"
        style={{ position: 'relative', width: 500, height: 300 }}
      >
        <Loading type="spin">
          <div
            style={{
              width: 500,
              height: 300,
              boxSizing: 'border-box',
              background: '#f5f7fa',
              padding: 20,
              border: '20px solid #5f6a7a',
            }}
          />
        </Loading>
      </div>
    </>
  )
}

```

### visible.stories.tsx

```typescript
import React from 'react'
import Loading from '@hi-ui/loading'

/**
 * @title 局部容器加载
 */
export const Visible = () => {
  const [visible, setVisible] = React.useState(false)

  return (
    <>
      <h1>Visible</h1>
      <div
        className="loading-visible__wrap"
        style={{ position: 'relative', width: 500, height: 300 }}
      >
        <Loading visible={visible} content="Loading..." delay={500}>
          <div
            onClick={() => {
              setVisible((prev) => !prev)
            }}
            style={{
              width: 500,
              height: 300,
              boxSizing: 'border-box',
              background: '#f5f7fa',
              padding: 20,
              border: '20px solid #5f6a7a',
            }}
          />
        </Loading>
      </div>
    </>
  )
}

```

## locale-context 组件

### basic.stories.tsx

```typescript
import React, { useContext } from 'react'
import { LocaleContext } from '@hi-ui/locale-context'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const i18n = useContext(LocaleContext)

  return (
    <>
      <h1>Basic</h1>
      <div className="locale-context-basic__wrap">{i18n.get('datePicker.ok')}</div>
    </>
  )
}

```

## menu 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Menu from '@hi-ui/menu'
import { AppStoreOutlined, UserOutlined, SunOutlined, PadOutlined } from '@hi-ui/icons'

/**
 * @title 基础用法
 * @desc 当导航的菜单项和层级较多时适用，可收起
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div
        className="menu-basic__wrap"
        style={{ background: '#f5f7fa', padding: 20, minWidth: 600 }}
      >
        <Menu
          showCollapse
          defaultExpandedIds={[3]}
          data={[
            {
              title: '首页',
              id: 1,
              icon: <AppStoreOutlined />,
            },
            {
              title: '小米MIX',
              id: 2,
              icon: <UserOutlined />,
            },
            {
              title: '手机',
              id: 3,
              icon: <SunOutlined />,
              children: [
                {
                  title: '小米',
                  id: 666,
                  children: [
                    {
                      title: '小米9',
                      id: 'xiaomi9',
                    },
                    {
                      title: '小米8',
                      id: 'xiaomi8',
                      disabled: true,
                    },
                    {
                      title: '小米7',
                      id: 'xiaomi7',
                    },
                    {
                      title: '小米6',
                      id: 'xiaomi6',
                    },
                    {
                      title: '小米5',
                      id: 'xiaomi5',
                    },
                    {
                      title: '小米4',
                      id: 'xiaomi4',
                    },
                    {
                      title: '小米3',
                      id: 'xiaomi3',
                    },
                  ],
                },
                {
                  title: '红米',
                  id: 'hongmi',
                },
                {
                  title: '小米note',
                  disabled: true,
                  id: 'xiaominote',

                  children: [
                    {
                      title: '小米 note7',
                      id: 'xiaomi note7',
                    },
                    {
                      title: '小米 note6',
                      id: 'xiaomi note6',
                    },
                    {
                      title: '小米 note5',
                      id: 'xiaomi note5',
                    },
                    {
                      title: '小米 note4',
                      id: 'xiaomi note4',
                    },
                    {
                      title: '小米 note3',
                      id: 'xiaomi note3',
                    },
                  ],
                },
              ],
            },
            {
              title: '超长超长超长字符超长超长超长字符',
              id: 4,
              icon: <PadOutlined />,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### expand-all.stories.tsx

```typescript
import React from 'react'
import Menu from '@hi-ui/menu'
import { AppStoreOutlined, SunOutlined } from '@hi-ui/icons'

/**
 * @title 默认展开所有
 * @desc 在初次渲染时，展开所有节点
 */
export const DefaultExpandAll = () => {
  return (
    <>
      <h1>DefaultExpandAll</h1>
      <div
        className="menu-expand-all__wrap"
        style={{ background: '#f5f7fa', padding: 20, minWidth: 600 }}
      >
        <Menu
          showCollapse
          defaultExpandAll
          data={[
            {
              title: '首页',
              id: 1,
              icon: <AppStoreOutlined />,
            },
            {
              title: '小米手机',
              id: 3,
              icon: <SunOutlined />,
              children: [
                {
                  title: '小米',
                  id: 666,
                  children: [
                    {
                      title: '小米9',
                      id: 'xiaomi9',
                    },
                    {
                      title: '小米8',
                      id: 'xiaomi8',
                    },
                    {
                      title: '小米7',
                      id: 'xiaomi7',
                    },
                    {
                      title: '小米6',
                      id: 'xiaomi6',
                    },
                  ],
                },
                {
                  title: '小米note',
                  id: 'xiaominote',

                  children: [
                    {
                      title: '小米 note7',
                      id: 'xiaomi note7',
                    },
                  ],
                },
              ],
            },
          ]}
        />
      </div>
    </>
  )
}

```

### fat.stories.tsx

```typescript
import React from 'react'
import Menu from '@hi-ui/menu'

/**
 * @title 水平胖菜单
 * @desc 二级菜单项，以分组的形式展示，分组数不宜过多
 */
export const HorizontalFat = () => {
  return (
    <>
      <h1>水平胖菜单</h1>
      <div
        className="menu-horizontal-fat__wrap"
        style={{ background: '#f5f7fa', padding: 20, minWidth: 600 }}
      >
        <Menu
          placement="horizontal"
          showAllSubMenus
          data={[
            {
              title: '电视',
              id: 1,
            },
            {
              title: '小米MIX',
              id: 2,
            },
            {
              title: '手机',
              id: 3,
              children: [
                {
                  title: '小米',
                  id: 666,

                  children: [
                    {
                      title: '小米9',
                      id: 'xiaomi9',
                    },
                    {
                      title: '小米8',
                      id: 'xiaomi8',
                    },
                    {
                      title: '小米7',
                      id: 'xiaomi7',
                    },
                    {
                      title: '小米6',
                      id: 'xiaomi6',
                    },
                    {
                      title: '小米5',
                      id: 'xiaomi5',
                    },
                    {
                      title: '小米4',
                      id: 'xiaomi4',
                    },
                    {
                      title: '小米3',
                      id: 'xiaomi3',
                    },
                  ],
                },
                {
                  title: '红米',
                  id: 'hongmi',
                },
                {
                  title: '小米note',
                  id: 'xiaominote',
                  children: [
                    {
                      title: '小米 note7',
                      id: 'xiaomi note7',
                    },
                    {
                      title: '小米 note6',
                      id: 'xiaomi note6',
                    },
                    {
                      title: '小米 note5',
                      id: 'xiaomi note5',
                    },
                    {
                      title: '小米 note4',
                      id: 'xiaomi note4',
                    },
                    {
                      title: '小米 note3',
                      id: 'xiaomi note3',
                    },
                  ],
                },
              ],
            },
            {
              title: '数码产品',
              id: 4,
            },
            {
              title: '笔记本',
              id: 5,
            },
            {
              title: '智能生活',
              id: 6,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### footer-render.stories.tsx

```typescript
import React from 'react'
import Menu from '@hi-ui/menu'
import { AppStoreOutlined, SunOutlined } from '@hi-ui/icons'

/**
 * @title 自定义 Footer 渲染
 * @desc 自行控制底部内容展示，支持插入额外的元素等场景
 */
export const FooterRender = () => {
  return (
    <>
      <h1>FooterRender</h1>
      <div
        className="menu-footer-render__wrap"
        style={{ background: '#f5f7fa', padding: 20, minWidth: 600 }}
      >
        <Menu
          showCollapse
          footerRender={({ collapsed, collapseNode }) => {
            return (
              <div
                style={{
                  display: 'flex',
                  alignItems: 'center',
                  justifyContent: 'space-between',
                }}
              >
                {collapseNode}
                {collapsed ? null : <div style={{ margin: '8px 8px 0 0' }}>我是谁</div>}
              </div>
            )
          }}
          data={[
            {
              title: '首页',
              id: 1,
              icon: <AppStoreOutlined />,
            },
            {
              title: '小米手机',
              id: 3,
              icon: <SunOutlined />,
              children: [
                {
                  title: '小米',
                  id: 666,
                  children: [
                    {
                      title: '小米9',
                      id: 'xiaomi9',
                    },
                    {
                      title: '小米8',
                      id: 'xiaomi8',
                    },
                    {
                      title: '小米7',
                      id: 'xiaomi7',
                    },
                    {
                      title: '小米6',
                      id: 'xiaomi6',
                    },
                  ],
                },
                {
                  title: '小米note',
                  id: 'xiaominote',
                  children: [
                    {
                      title: '小米 note7',
                      id: 'xiaomi note7',
                    },
                  ],
                },
              ],
            },
          ]}
        />
      </div>
    </>
  )
}

```

### horizontal.stories.tsx

```typescript
import React from 'react'
import {
  HomeOutlined,
  UserOutlined,
  SunOutlined,
  PadOutlined,
  ManOutlined,
  LockOutlined,
} from '@hi-ui/icons'
import Menu from '@hi-ui/menu'

/**
 * @title 水平布局
 * @desc 水平方向的导航菜单，菜单项在4-7个为适
 */
export const Horizontal = () => {
  return (
    <>
      <h1>水平菜单</h1>
      <div
        className="menu-horizontal__wrap"
        style={{ background: '#f5f7fa', padding: 20, minWidth: 600 }}
      >
        <Menu
          placement="horizontal"
          onClick={console.log}
          data={[
            {
              title: '电视',
              id: 1,
              icon: <HomeOutlined />,
            },
            {
              title: '小米MIX',
              id: 2,
              icon: <UserOutlined />,
            },
            {
              title: '手机',
              id: 3,
              icon: <SunOutlined />,
              children: [
                {
                  title: '小米',
                  id: 666,
                  icon: <LockOutlined />,

                  children: [
                    {
                      title: '小米9',
                      id: 'xiaomi9',
                    },
                    {
                      title: '小米8',
                      id: 'xiaomi8',
                    },
                    {
                      title: '小米7',
                      id: 'xiaomi7',
                    },
                    {
                      title: '小米6',
                      id: 'xiaomi6',
                      icon: <ManOutlined />,
                    },
                    {
                      title: '小米5',
                      id: 'xiaomi5',
                    },
                    {
                      title: '小米4',
                      id: 'xiaomi4',
                    },
                    {
                      title: '小米3',
                      id: 'xiaomi3',
                    },
                  ],
                },
                {
                  title: '红米',
                  id: 'hongmi',
                },
                {
                  title: '小米note',
                  id: 'xiaominote',

                  children: [
                    {
                      title: '小米 note7',
                      id: 'xiaomi note7',
                    },
                    {
                      title: '小米 note6',
                      id: 'xiaomi note6',
                    },
                    {
                      title: '小米 note5',
                      id: 'xiaomi note5',
                    },
                    {
                      title: '小米 note4',
                      id: 'xiaomi note4',
                    },
                    {
                      title: '小米 note3',
                      id: 'xiaomi note3',
                    },
                  ],
                },
              ],
            },
            {
              title: '数码产品',
              id: 4,
              icon: <PadOutlined />,
            },
            {
              title: '一级导航1',
              id: 5,
              icon: <PadOutlined />,
            },
            {
              title: '一级导航2',
              id: 6,
              icon: <PadOutlined />,
            },
            {
              title: '一级导航3',
              id: 7,
              icon: <PadOutlined />,
            },
            {
              title: '一级导航4',
              id: 8,
              icon: <PadOutlined />,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### mini.stories.tsx

```typescript
import React from 'react'
import Menu from '@hi-ui/menu'
import { AppStoreOutlined, UserOutlined, SunOutlined, PadOutlined } from '@hi-ui/icons'

/**
 * @title 收缩态受控
 * @desc 根据页面内容宽度，自行调整 Menu 收缩或者展开以适应空间
 */
export const Mini = () => {
  const [mini, setMini] = React.useState(true)
  const [menuData] = React.useState([
    {
      title: '首页',
      id: 1,
      icon: <AppStoreOutlined />,
    },
    {
      title: '小米MIX',
      id: 2,
      icon: <UserOutlined />,
    },
    {
      title: '手机',
      id: 3,
      icon: <SunOutlined />,
      children: [
        {
          title: '小米',
          id: 666,
          children: [
            {
              title: '小米9',
              id: 'xiaomi9',
            },
            {
              title: '小米8',
              id: 'xiaomi8',
            },
            {
              title: '小米7',
              id: 'xiaomi7',
            },
            {
              title: '小米6',
              id: 'xiaomi6',
            },
            {
              title: '小米5',
              id: 'xiaomi5',
            },
            {
              title: '小米4',
              id: 'xiaomi4',
            },
            {
              title: '小米3',
              id: 'xiaomi3',
            },
          ],
        },
        {
          title: '红米',
          id: 'hongmi',
        },
        {
          title: '小米note',
          id: 'xiaominote',

          children: [
            {
              title: '小米 note7',
              id: 'xiaomi note7',
            },
            {
              title: '小米 note6',
              id: 'xiaomi note6',
            },
            {
              title: '小米 note5',
              id: 'xiaomi note5',
            },
            {
              title: '小米 note4',
              id: 'xiaomi note4',
            },
            {
              title: '小米 note3',
              id: 'xiaomi note3',
            },
          ],
        },
      ],
    },
    {
      title: '超长超长超长字符超长超长超长字符',
      id: 4,
      icon: <PadOutlined />,
    },
  ])

  return (
    <>
      <h1>Mini</h1>
      <div
        className="menu-mini__wrap"
        style={{ background: '#f5f7fa', padding: 20, minWidth: 600 }}
      >
        <Menu showCollapse collapsed={mini} onCollapse={setMini} data={menuData} />
      </div>
    </>
  )
}

```

### pop.stories.tsx

```typescript
import React from 'react'
import Menu from '@hi-ui/menu'

/**
 * @title 弹出式展开
 * @desc 二级菜单项，以弹层的形式展示，弹层嵌套不宜过多
 */
export const Pop = () => {
  return (
    <>
      <h1>Pop</h1>
      <div className="menu-pop__wrap" style={{ background: '#f5f7fa', padding: 20, minWidth: 600 }}>
        <Menu
          expandedType="pop"
          data={[
            {
              title: '电视',
              id: 1,
            },
            {
              title: '小米MIX',
              id: 2,
            },
            {
              title: '手机',
              id: 3,
              children: [
                {
                  title: '小米',
                  id: 666,

                  children: [
                    {
                      title: '小米9',
                      id: 'xiaomi9',
                    },
                    {
                      title: '小米8',
                      id: 'xiaomi8',
                    },
                    {
                      title: '小米7',
                      id: 'xiaomi7',
                    },
                    {
                      title: '小米6',
                      id: 'xiaomi6',
                    },
                    {
                      title: '小米5',
                      id: 'xiaomi5',
                    },
                    {
                      title: '小米4',
                      id: 'xiaomi4',
                    },
                    {
                      title: '小米3',
                      id: 'xiaomi3',
                    },
                  ],
                },
                {
                  title: '红米',
                  id: 'hongmi',
                },
                {
                  title: '小米note',
                  id: 'xiaominote',
                  children: [
                    {
                      title: '小米 note7',
                      id: 'xiaomi note7',
                    },
                    {
                      title: '小米 note6',
                      id: 'xiaomi note6',
                    },
                    {
                      title: '小米 note5',
                      id: 'xiaomi note5',
                    },
                    {
                      title: '小米 note4',
                      id: 'xiaomi note4',
                    },
                    {
                      title: '小米 note3',
                      id: 'xiaomi note3',
                    },
                  ],
                },
              ],
            },
            {
              title: '超长超长超长字符超长超长超长字符',
              id: 4,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### render.stories.tsx

```typescript
import React from 'react'
import Menu, { MenuDataItem } from '@hi-ui/menu'
import {
  RightOutlined,
  AppStoreOutlined,
  UserOutlined,
  SunOutlined,
  PadOutlined,
  SearchOutlined,
} from '@hi-ui/icons'
import Popper from '@hi-ui/popper'
import Search from '@hi-ui/search'

/**
 * @title 自定义渲染
 */
export const Render = () => {
  const menuData = [
    {
      title: '首页',
      id: 1,
      icon: <AppStoreOutlined />,
    },
    {
      title: '小米MIX',
      id: 2,
      icon: <UserOutlined />,
    },
    {
      title: '手机',
      id: 3,
      icon: <SunOutlined />,
    },
    {
      title: '电脑',
      id: 4,
      icon: <PadOutlined />,
    },
  ]

  const menuRef = React.useRef<HTMLDivElement | null>(null)
  const [currentMenu, setCurrentMenu] = React.useState<MenuDataItem>(menuData[0])
  const [visible, setVisible] = React.useState(false)

  return (
    <>
      <h1>Render</h1>
      <div
        className="menu-render__wrap"
        style={{ background: '#f5f7fa', padding: 20, minWidth: 600 }}
      >
        <Menu
          ref={menuRef}
          showCollapse
          extraHeader={
            <div style={{ padding: '10px 0' }}>
              <Search prefix={<SearchOutlined />} append={null} />
            </div>
          }
          defaultExpandedIds={[3]}
          render={(item) => {
            return (
              <div
                style={{ display: 'flex', justifyContent: 'space-between', alignItems: 'center' }}
              >
                {item.title}
                <RightOutlined style={{ marginLeft: 4 }} />
              </div>
            )
          }}
          onClick={(id, data) => {
            console.log('click', id, data)

            setCurrentMenu(data)
            setVisible(true)
          }}
          data={menuData}
        />
        {/* 如果不需要阴影，可以设置 className 去覆盖样式 */}
        <Popper
          className="menu-render__popper"
          visible={visible}
          attachEl={menuRef.current}
          placement="right"
          gutterGap={0}
          flip={false}
          animationType="scaleX"
          onClose={() => {
            setVisible(false)
          }}
          onOutsideClick={() => console.log('onOutsideClick')}
        >
          <div
            style={{
              width: 200,
              height: menuRef.current?.getBoundingClientRect().height,
              padding: 10,
              boxSizing: 'border-box',
            }}
          >
            菜单：{currentMenu.title}
          </div>
        </Popper>
      </div>
    </>
  )
}

```

### sidebar.stories.tsx

```typescript
import React from 'react'
import { Sidebar, MenuDataItem, filterTreeData } from '@hi-ui/menu'
import Search, { SearchDataItem } from '@hi-ui/search'
import Tooltip from '@hi-ui/tooltip'
import {
  AppStoreOutlined,
  UserOutlined,
  SunOutlined,
  PadOutlined,
  SearchOutlined,
} from '@hi-ui/icons'

/**
 * @title 侧边栏风格菜单
 */
export const SidebarMenu = () => {
  const [activeId, setActiveId] = React.useState<React.ReactText>('xiaomi1')
  const [searchKey, setSearchKey] = React.useState<string>('')
  const [data] = React.useState<MenuDataItem[]>([
    {
      title: '首页',
      id: '1',
      icon: <AppStoreOutlined />,
      children: [
        {
          title: '新品发布',
          id: '1-1',
          children: [
            {
              title: '新品发布',
              id: '1-1-1',
            },
          ],
        },
        {
          title: '在线反馈',
          id: '1-2',
          children: [
            {
              title: '在线反馈',
              id: '1-2-1',
            },
            {
              title: '在线人员处理',
              id: '1-2-2',
            },
          ],
        },
      ],
    },
    {
      title: '小米MIX',
      id: '2',
      icon: <UserOutlined />,
      children: [
        {
          title: '小米Mix',
          id: '2-1',
          icon: <AppStoreOutlined />,
          children: [
            {
              title: '小米Mix1',
              id: '2-1-1',
            },
            {
              title: '小米Mix2',
              id: '2-1-2',
            },
            {
              title: '小米Mix3',
              id: '2-1-3',
            },
          ],
        },
      ],
    },
    {
      title: '手机',
      id: 'shouji',
      icon: <SunOutlined />,
      children: [
        {
          title: '小米',
          id: 'xiaomi',
          icon: <SunOutlined />,
          children: [
            {
              title: '小米1',
              id: 'xiaomi1',
            },
            {
              title: '小米2',
              id: 'xiaomi2',
              disabled: true,
            },
            {
              title: '小米3',
              id: 'xiaomi3',
            },
          ],
        },
        {
          title: '红米',
          id: 'hongmi',
          icon: <SunOutlined />,
          children: [
            {
              title: '红米1',
              id: 'redmi1',
            },
            {
              title: '红米2',
              id: 'redmi2',
            },
            {
              title: '红米3',
              id: 'redmi3',
            },
          ],
        },
        {
          title: '小米note',
          id: 'xiaominote',
          icon: <SunOutlined />,
          children: [
            {
              title: '小米 note7',
              id: 'xiaomi note7',
            },
            {
              title: '小米 note6',
              id: 'xiaomi note6',
            },
            {
              title: '小米 note5',
              id: 'xiaomi note5',
            },
          ],
        },
      ],
    },
    {
      title: (
        <Tooltip title={'超长超长超长字符超长超长超长字符'} placement="right">
          <div style={{ overflow: 'hidden', textOverflow: 'ellipsis', whiteSpace: 'nowrap' }}>
            超长超长超长字符超长超长超长字符
          </div>
        </Tooltip>
      ),
      id: '4',
      icon: <PadOutlined />,
    },
  ])

  const showData = React.useMemo(() => {
    return (filterTreeData(data, searchKey, activeId) ?? []) as SearchDataItem[]
  }, [activeId, data, searchKey])

  return (
    <>
      <h1>SidebarMenu</h1>
      <div
        className="menu-basic__wrap"
        style={{ background: '#f5f7fa', padding: 20, minWidth: 600, height: 400 }}
      >
        <div style={{ background: '#fff', height: '100%' }}>
          <Sidebar
            activeId={activeId}
            onClick={setActiveId}
            collapsible={false}
            data={data}
            render={(data, level) => {
              return data.title
            }}
            extraHeader={
              <div style={{ marginBottom: 8 }}>
                <Search
                  prefix={<SearchOutlined />}
                  append={null}
                  placeholder="搜素"
                  value={searchKey}
                  data={showData}
                  onInput={(e) => {
                    setSearchKey((e.target as HTMLInputElement).value)
                  }}
                  onSearch={(key, item) => console.log({ key, item })}
                />
              </div>
            }
          />
        </div>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Menu from '@hi-ui/menu'
import { AppStoreOutlined, UserOutlined, SunOutlined, PadOutlined } from '@hi-ui/icons'

/**
 * @title 设置尺寸
 * @desc 默认是 lg 尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>Size</h1>
      <div
        className="menu-size__wrap"
        style={{ background: '#f5f7fa', padding: 20, minWidth: 600 }}
      >
        <h2>lg</h2>
        <Menu
          showCollapse
          size="lg"
          data={[
            {
              title: '首页',
              id: 1,
              icon: <AppStoreOutlined />,
            },
            {
              title: '小米MIX',
              id: 2,
              icon: <UserOutlined />,
            },
            {
              title: '手机',
              id: 3,
              icon: <SunOutlined />,
              children: [
                {
                  title: '小米',
                  id: 666,
                },
                {
                  title: '红米',
                  id: 'hongmi',
                },
                {
                  title: '小米note',
                  id: 'xiaominote',
                  children: [
                    {
                      title: '小米 note7',
                      id: 'xiaomi note7',
                    },
                    {
                      title: '小米 note6',
                      id: 'xiaomi note6',
                    },
                    {
                      title: '小米 note5',
                      id: 'xiaomi note5',
                    },
                    {
                      title: '小米 note4',
                      id: 'xiaomi note4',
                    },
                    {
                      title: '小米 note3',
                      id: 'xiaomi note3',
                    },
                  ],
                },
              ],
            },
            {
              title: '超长超长超长字符超长超长超长字符',
              id: 4,
              icon: <PadOutlined />,
            },
          ]}
        />
        <h2>md</h2>
        <Menu
          showCollapse
          size="md"
          data={[
            {
              title: '首页',
              id: 1,
              icon: <AppStoreOutlined />,
            },
            {
              title: '小米MIX',
              id: 2,
              icon: <UserOutlined />,
            },
            {
              title: '手机',
              id: 3,
              icon: <SunOutlined />,
              children: [
                {
                  title: '小米',
                  id: 666,
                },
                {
                  title: '红米',
                  id: 'hongmi',
                },
                {
                  title: '小米note',
                  id: 'xiaominote',
                  children: [
                    {
                      title: '小米 note7',
                      id: 'xiaomi note7',
                    },
                    {
                      title: '小米 note6',
                      id: 'xiaomi note6',
                    },
                    {
                      title: '小米 note5',
                      id: 'xiaomi note5',
                    },
                    {
                      title: '小米 note4',
                      id: 'xiaomi note4',
                    },
                    {
                      title: '小米 note3',
                      id: 'xiaomi note3',
                    },
                  ],
                },
              ],
            },
            {
              title: '超长超长超长字符超长超长超长字符',
              id: 4,
              icon: <PadOutlined />,
            },
          ]}
        />
        <h2>sm</h2>
        <Menu
          showCollapse
          size="sm"
          data={[
            {
              title: '首页',
              id: 1,
              icon: <AppStoreOutlined />,
            },
            {
              title: '小米MIX',
              id: 2,
              icon: <UserOutlined />,
            },
            {
              title: '手机',
              id: 3,
              icon: <SunOutlined />,
              children: [
                {
                  title: '小米',
                  id: 666,
                },
                {
                  title: '红米',
                  id: 'hongmi',
                },
                {
                  title: '小米note',
                  id: 'xiaominote',
                  children: [
                    {
                      title: '小米 note7',
                      id: 'xiaomi note7',
                    },
                    {
                      title: '小米 note6',
                      id: 'xiaomi note6',
                    },
                    {
                      title: '小米 note5',
                      id: 'xiaomi note5',
                    },
                    {
                      title: '小米 note4',
                      id: 'xiaomi note4',
                    },
                    {
                      title: '小米 note3',
                      id: 'xiaomi note3',
                    },
                  ],
                },
              ],
            },
            {
              title: '超长超长超长字符超长超长超长字符',
              id: 4,
              icon: <PadOutlined />,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### vertical-fat.stories.tsx

```typescript
import React from 'react'
import Menu from '@hi-ui/menu'

/**
 * @title 垂直胖菜单
 * @desc 二级菜单项，以分组的形式展示，分组数不宜过多
 */
export const VerticalFat = () => {
  return (
    <>
      <h1>垂直胖菜单</h1>
      <div
        className="menu-vertical-fat__wrap"
        style={{ background: '#f5f7fa', padding: 20, minWidth: 600 }}
      >
        <Menu
          placement="vertical"
          showAllSubMenus
          data={[
            {
              title: '电视',
              id: 1,
            },
            {
              title: '小米MIX',
              id: 2,
            },
            {
              title: '手机',
              id: 3,
              children: [
                {
                  title: '小米',
                  id: 666,

                  children: [
                    {
                      title: '小米9',
                      id: 'xiaomi9',
                    },
                    {
                      title: '小米8',
                      id: 'xiaomi8',
                    },
                    {
                      title: '小米7',
                      id: 'xiaomi7',
                    },
                    {
                      title: '小米6',
                      id: 'xiaomi6',
                    },
                    {
                      title: '小米5',
                      id: 'xiaomi5',
                    },
                    {
                      title: '小米4',
                      id: 'xiaomi4',
                    },
                    {
                      title: '小米3',
                      id: 'xiaomi3',
                    },
                  ],
                },
                {
                  title: '红米',
                  id: 'hongmi',
                },
                {
                  title: '小米note',
                  id: 'xiaominote',
                  children: [
                    {
                      title: '小米 note7',
                      id: 'xiaomi note7',
                    },
                    {
                      title: '小米 note6',
                      id: 'xiaomi note6',
                    },
                    {
                      title: '小米 note5',
                      id: 'xiaomi note5',
                    },
                    {
                      title: '小米 note4',
                      id: 'xiaomi note4',
                    },
                    {
                      title: '小米 note3',
                      id: 'xiaomi note3',
                    },
                  ],
                },
              ],
            },
            {
              title: '超长超长超长字符超长超长超长字符',
              id: 4,
            },
          ]}
        />
      </div>
    </>
  )
}

```

## message 组件

### auto-close.stories.tsx

```typescript
import React from 'react'
import message from '@hi-ui/message'
import Button from '@hi-ui/button'

/**
 * @title 取消自动关闭
 */
export const AutoClose = () => {
  return (
    <>
      <h1>AutoClose</h1>
      <div className="message-auto-close">
        <Button
          onClick={() => {
            const toastId = message.open({
              autoClose: false,
              title: (
                <div style={{ display: 'flex', alignItems: 'center' }}>
                  <span>这个 Toast 将不会自动被关闭哦 </span>
                  <Button
                    style={{ marginLeft: 24 }}
                    type="primary"
                    appearance="link"
                    onClick={() => {
                      message.close(toastId)
                    }}
                  >
                    撤销
                  </Button>
                </div>
              ),
              type: 'success',
            })
          }}
        >
          Toast
        </Button>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import message from '@hi-ui/message'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 * @desc 一般提醒，不具有明确的引导倾向，自动关闭
 *
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="message-basic__wrap">
        <Button
          onClick={() => {
            message.open({
              title: '欢迎使用 HiUI 组件库',
              type: 'success',
            })
          }}
        >
          Toast
        </Button>
      </div>
    </>
  )
}

```

### close.stories.tsx

```typescript
import React from 'react'
import message from '@hi-ui/message'
import Button from '@hi-ui/button'

/**
 * @title 手动关闭
 */
export const Close = () => {
  const toastIdsRef = React.useRef([])

  function close() {
    const popId = toastIdsRef.current.pop()
    message.close(popId)
  }

  function closeAll() {
    message.closeAll()
  }

  function addToast() {
    const id = message.open({
      title: '问君能有几多愁，恰似一江春水向东流',
      type: ['error', 'warning', 'success', 'info'][Math.floor(Math.random() * 4)] as any,
    })
    toastIdsRef.current.push(id)
  }

  return (
    <>
      <h1>Close</h1>
      <div className="message-close__wrap">
        <Button onClick={addToast}>Toast</Button>

        <Button onClick={close}>Close latest toast</Button>

        <Button onClick={closeAll}>Close all toasts</Button>
      </div>
    </>
  )
}

```

### custom.stories.tsx

```typescript
import React, { useMemo, useState } from 'react'
import { createMessage } from '@hi-ui/message'
import Button from '@hi-ui/button'

/**
 * @title message 属性自定义
 * @desc 支持配置 container 和 zIndex
 */

export const Custom = () => {
  const [container, setContainer] = useState<HTMLElement>()
  const message = useMemo(
    () =>
      createMessage({
        container,
        zIndex: 1000,
      }),
    [container]
  )
  return (
    <>
      <h1>Custom</h1>
      <div className="message-custom__wrap">
        <div
          ref={(e) => {
            setContainer(e as HTMLDivElement)
          }}
          style={{
            width: '100%',
            minWidth: 660,
            height: 420,
            marginBottom: 20,
            background: '#f5f7fa',
            boxShadow: '1px 2px 8px #ddd',
            display: 'flex',
            justifyContent: 'center',
            alignItems: 'center',

            // Need add for it
            position: 'relative',
            overflow: 'hidden',
            zIndex: 0,
          }}
        >
          <Button
            type="primary"
            onClick={() => {
              message.open({
                title: '欢迎使用 HiUI 组件库',
                type: 'success',
              })
            }}
          >
            Toast
          </Button>
        </div>
      </div>
    </>
  )
}

```

### type.stories.tsx

```typescript
import React from 'react'
import message from '@hi-ui/message'
import Button from '@hi-ui/button'

/**
 * @title 不同类型
 * @desc 通过 type 指定不同类型场景的消息提醒
 */
export const Type = () => {
  function addToast(type) {
    return () => {
      message.open({
        title: '问君能有几多愁，恰似一江春水向东流',
        type,
      })
    }
  }

  return (
    <>
      <h1>Close</h1>
      <div className="message-close__wrap">
        <Button type="secondary" onClick={addToast('info')}>
          Info
        </Button>
        <Button type="success" onClick={addToast('success')}>
          Success
        </Button>
        <Button type="danger" onClick={addToast('error')}>
          Error
        </Button>
        <Button type="default" onClick={addToast('warning')}>
          Warning
        </Button>
      </div>
    </>
  )
}

```

## modal 组件

### async-confirm.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Modal from '@hi-ui/modal'

/**
 * @title 异步确认关闭
 * @desc 通过 confirmLoading 控制确定按钮的 loading 状态，实现异步关闭
 */
export const AsyncConfirm = () => {
  const [visible, setVisible] = React.useState(false)
  const [confirmLoading, setConfirmLoading] = React.useState(false)
  console.log('visible', visible)

  return (
    <>
      <h1>AsyncConfirm</h1>
      <div className="modal-async-confirm__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Modal
          title="提示"
          visible={visible}
          closeable={false}
          onCancel={() => setVisible(false)}
          onConfirm={() => {
            console.log('自定义确认事件')

            setConfirmLoading(true)
            setTimeout(() => {
              setVisible(false)
              setConfirmLoading(false)
            }, 1000)
          }}
          confirmLoading={confirmLoading}
        >
          代码如写诗
          <br />
          <br />
          写诗如代码
          <br />
          <br />
          这是一门艺术
        </Modal>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Modal from '@hi-ui/modal'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const [visible, setVisible] = React.useState(false)
  console.log('visible', visible)

  return (
    <>
      <h1>Basic</h1>
      <div className="modal-basic__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Modal title="提示" visible={visible} closeable={false} onCancel={() => setVisible(false)}>
          代码如写诗
          <br />
          <br />
          写诗如代码
          <br />
          <br />
          这是一门艺术
        </Modal>
      </div>
    </>
  )
}

```

### closeable.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Modal from '@hi-ui/modal'

/**
 * @title 带关闭按钮
 */
export const Closeable = () => {
  const [visible, setVisible] = React.useState(false)
  console.log(visible)

  return (
    <>
      <h1>Closeable</h1>
      <div className="modal-closeable__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Modal title="提示消息" visible={visible} closeable onCancel={() => setVisible(false)}>
          <span>哈哈哈哈哈....</span>
          <br />
          <span>哈哈哈哈哈...</span>
          <br />
          <span>哈哈哈哈哈...</span>
        </Modal>
      </div>
    </>
  )
}

```

### container.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Modal from '@hi-ui/modal'

/**
 * @title 局部容器弹窗
 */
export const Container = () => {
  const [visible, setVisible] = React.useState(false)
  const [container, setContainer] = React.useState(undefined)

  console.log('visible', visible)

  return (
    <>
      <h1>Container</h1>

      <div
        ref={setContainer}
        className="modal-container__wrap"
        style={{
          width: '100%',
          minWidth: 660,
          height: 420,
          background: '#f5f7fa',
          boxShadow: '1px 2px 8px #ddd',
          display: 'flex',
          justifyContent: 'center',
          alignItems: 'center',

          // Need add for it
          position: 'relative',
          overflow: 'hidden',
          zIndex: 0,
        }}
      >
        <Button type="primary" onClick={() => setVisible(!visible)}>
          open
        </Button>
        <Modal
          title="提示"
          style={{ position: 'absolute' }}
          visible={visible}
          closeable={false}
          onCancel={() => setVisible(false)}
          container={container}
        >
          我是挂载指定容器的模态框内容
        </Modal>
      </div>
    </>
  )
}

```

### footer.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Modal from '@hi-ui/modal'

/**
 * @title 自定义按钮
 * @desc 通过 footer 自定义底部的按钮，并自定义事件
 */
export const Footer = () => {
  const [visible, setVisible] = React.useState(false)
  console.log('visible', visible)

  return (
    <>
      <h1>Footer</h1>
      <div className="modal-footer__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Modal
          title="提示"
          visible={visible}
          closeable={false}
          onCancel={() => setVisible(false)}
          footer={[
            <Button type="primary" key={0} onClick={() => console.log(1)}>
              自定义按钮1
            </Button>,
            <Button type="success" key={1} onClick={() => console.log(2)}>
              自定义按钮2
            </Button>,
            <Button type="danger" key={2} onClick={() => console.log(3)}>
              自定义按钮3
            </Button>,
            <Button type="default" key={3} onClick={() => setVisible(false)}>
              关闭
            </Button>,
          ]}
        >
          代码如写诗
          <br />
          <br />
          写诗如代码
          <br />
          <br />
          这是一门艺术
        </Modal>
      </div>
    </>
  )
}

```

### nested.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Modal from '@hi-ui/modal'

/**
 * @title 嵌套弹窗
 * @desc 反复操作确认弹窗场景
 */
export const Nested = () => {
  const [visible, setVisible] = React.useState(false)
  const [nestVisible, setNestVisible] = React.useState(false)

  return (
    <>
      <h1>Nested</h1>
      <div className="modal-nested__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Modal title="提示" visible={visible} closeable={false} onCancel={() => setVisible(false)}>
          <div>这里是弹窗内容</div>
          <Button style={{ marginTop: 20 }} onClick={() => setNestVisible(!nestVisible)}>
            Nested
          </Button>
          <Modal
            title="提示"
            visible={nestVisible}
            closeable={false}
            onCancel={() => setNestVisible(false)}
          >
            Nest这里是弹窗内容
          </Modal>
        </Modal>
      </div>
    </>
  )
}

```

### popup.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Modal from '@hi-ui/modal'

/**
 * @title 提示弹窗
 * @desc 未传入 title 及 closeable 为 false，可取消 title 部分；footer 为 null，可取消底部按钮
 */
export const Popup = () => {
  const [visible, setVisible] = React.useState(false)
  console.log('visible', visible)

  return (
    <>
      <h1>提示弹窗</h1>
      <div className="modal-popup__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Modal visible={visible} closeable={false} onCancel={() => setVisible(false)} footer={null}>
          代码如写诗
          <br />
          <br />
          写诗如代码
          <br />
          <br />
          这是一门艺术
        </Modal>
      </div>
    </>
  )
}

```

### scroll.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Modal from '@hi-ui/modal'

/**
 * @title 内容溢出滚动
 */
export const Scroll = () => {
  const [visible, setVisible] = React.useState(false)
  console.log('visible', visible)

  return (
    <>
      <h1>Scroll</h1>
      <div className="modal-scroll__wrap">
        <Button onClick={() => setVisible(!visible)}>open</Button>
        <Modal title="弹窗标题" visible={visible} onCancel={() => setVisible(false)}>
          <div>
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区 模拟超长的内容区 模拟超长的内容区 模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
            <br />
            模拟超长的内容区
          </div>
        </Modal>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Modal, { ModalSizeEnum } from '@hi-ui/modal'

/**
 * @title 不同尺寸
 * @desc 通过 size 自定义尺寸
 */
export const Size = () => {
  const [visibleModalSize, setVisibleModalSize] = React.useState<ModalSizeEnum>()

  return (
    <>
      <h1>Size</h1>
      <div className="modal-size__wrap">
        <Button onClick={() => setVisibleModalSize('sm')}>sm</Button>

        <Button onClick={() => setVisibleModalSize('md')}>md</Button>

        <Button onClick={() => setVisibleModalSize('lg')}>lg</Button>
        <Modal
          title="提示"
          visible={!!visibleModalSize}
          closeable={false}
          size={visibleModalSize}
          onCancel={() => setVisibleModalSize(undefined)}
        >
          这是一个标题描述…
          <br />
          这是一个标题描述…
          <br />
          这是一个标题描述…
        </Modal>
      </div>
    </>
  )
}

```

### with-api.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Modal from '@hi-ui/modal'

/**
 * @title 询问式弹窗
 * @desc 用户在界面交互过程中的行为确认，适合轻量简单的场景
 */
export const WithAPI = () => {
  return (
    <>
      <h1>WithAPI</h1>
      <div className="modal-with-api__wrap">
        <Button
          type="danger"
          onClick={() =>
            Modal.confirm({
              type: 'error',
              title: '错误',
              content: '操作失败，请联系管理员！',
              cancelText: null,
              confirmText: '我知道了',
            })
          }
        >
          打开错误提示
        </Button>
        <Button
          type="default"
          onClick={() =>
            Modal.confirm({
              type: 'warning',
              title: '警告',
              content: '执行该操作后将无法撤销，是否确定继续？',
              cancelText: null,
              confirmText: '确定',
              closeOnEsc: false,
              maskClosable: false,
            })
          }
        >
          打开警告提示
        </Button>

        <Button
          type="success"
          onClick={() =>
            Modal.confirm({
              type: 'success',
              title: '成功',
              content:
                '这是信息提示对话框的描述，这是信息提示对话框的描述，这是信息提示对话框的描述',
              cancelText: null,
              confirmText: '确定',
            })
          }
        >
          打开成功提示
        </Button>

        <Button
          type="secondary"
          onClick={() =>
            Modal.confirm({
              type: 'info',
              title: '普通',
              content:
                '这是信息提示对话框的描述，这是信息提示对话框的描述，这是信息提示对话框的描述',
              cancelText: null,
              confirmText: '确定',
            })
          }
        >
          打开普通提示
        </Button>
      </div>
    </>
  )
}

```

## notification 组件

### action.stories.tsx

```typescript
import React from 'react'
import notification from '@hi-ui/notification'
import Button from '@hi-ui/button'

/**
 * @title 带操作
 */
export const Action = () => {
  const notificationIdRef = React.useRef<React.ReactText>('')

  return (
    <>
      <h1>Action</h1>
      <div className="notification-action__wrap">
        <Button
          onClick={() => {
            notificationIdRef.current = notification.open({
              autoClose: false,
              title: '数据备份通知',
              content:
                '各位同学请注意，将于2019.08.10 00:00:00 -08:00：00 期间进行系统服务器升级维护，请做好数据备份工作，以防丢失。带来不便，敬请谅解！',
              action: (
                <>
                  <Button
                    type="default"
                    onClick={() => {
                      if (notificationIdRef.current) {
                        notification.close(notificationIdRef.current)
                      }
                    }}
                  >
                    取消
                  </Button>
                  <Button
                    type="primary"
                    onClick={() => {
                      if (notificationIdRef.current) {
                        notification.close(notificationIdRef.current)
                      }
                    }}
                  >
                    确认
                  </Button>
                </>
              ),
            })
          }}
        >
          Notice
        </Button>
      </div>
    </>
  )
}

```

### auto-close.stories.tsx

```typescript
import React from 'react'
import notification from '@hi-ui/notification'
import Button from '@hi-ui/button'

/**
 * @title 取消自动关闭
 */
export const AutoClose = () => {
  return (
    <>
      <h1>AutoClose</h1>
      <div className="notification-auto-close">
        {/* <Message></Message> */}
        <Button
          onClick={() => {
            notification.open({
              autoClose: false,
              title: '数据备份通知',
              content:
                '各位同学请注意，将于2019.08.10 00:00:00 -08:00：00 期间进行系统服务器升级维护，请做好数据备份工作，以防丢失。带来不便，敬请谅解！',
            })
          }}
        >
          Toast
        </Button>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import notification from '@hi-ui/notification'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="notification-basic__wrap">
        <Button
          onClick={() => {
            notification.open({
              title: '数据备份通知',
              content:
                '各位同学请注意，将于2019.08.10 00:00:00 -08:00：00 期间进行系统服务器升级维护，请做好数据备份工作，以防丢失。带来不便，敬请谅解！',
            })
          }}
        >
          Notice
        </Button>
      </div>
    </>
  )
}

```

### close.stories.tsx

```typescript
import React from 'react'
import notification from '@hi-ui/notification'
import Button from '@hi-ui/button'

/**
 * @title 手动关闭
 */
export const Close = () => {
  const toastIdsRef = React.useRef([])

  function close() {
    const popId = toastIdsRef.current.pop()
    notification.close(popId)
  }

  function closeAll() {
    notification.closeAll()
  }

  function addToast() {
    const id = notification.open({
      title: 'some text',
      type: ['error', 'warning', 'success', 'info'][Math.floor(Math.random() * 4)] as any,
      content: 'some content',
    })
    toastIdsRef.current.push(id)
  }

  return (
    <>
      <h1>Close</h1>
      <div className="notification-close__wrap">
        <Button onClick={addToast}>Notice</Button>

        <Button onClick={close}>Close latest Notice</Button>

        <Button onClick={closeAll}>Close all Notices</Button>
      </div>
    </>
  )
}

```

### custom.stories.tsx

```typescript
import React, { useState, useMemo } from 'react'
import { createNotification } from '@hi-ui/notification'
import Button from '@hi-ui/button'

/**
 * @title notification 属性配置
 * @desc 支持配置 container 和 zIndex
 */
export const Custom = () => {
  const [container, setContainer] = useState<HTMLElement>()

  const notification = useMemo(
    () =>
      createNotification({
        container,
        zIndex: 2000,
      }),
    [container]
  )

  return (
    <>
      <h1>Custom</h1>

      <div
        ref={(e) => {
          e && setContainer(e)
        }}
        className="notification-custom__wrap"
        style={{
          width: '100%',
          minWidth: 660,
          height: 420,
          marginBottom: 20,
          background: '#f5f7fa',
          boxShadow: '1px 2px 8px #ddd',
          display: 'flex',
          justifyContent: 'center',
          alignItems: 'center',

          // Need add for it
          position: 'relative',
          overflow: 'hidden',
          zIndex: 0,
        }}
      >
        <Button
          type="primary"
          onClick={() => {
            notification.open({
              size: 'sm',
              title: '数据备份通知',
              content:
                '各位同学请注意，将于2019.08.10 00:00:00 -08:00：00 期间进行系统服务器升级维护！',
            })
          }}
        >
          Open
        </Button>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import notification from '@hi-ui/notification'
import Button from '@hi-ui/button'

/**
 * @title 设置尺寸
 */
export const Size = () => {
  const notificationIdRef = React.useRef<React.ReactText>()

  const openNotification = (size) => {
    notificationIdRef.current = notification.open({
      size,
      autoClose: false,
      title: '数据备份通知',
      content: '将于 2035.08.10 00:00:00-08:00：00 期间进行系统服务器升级维护！',
    })
  }
  return (
    <>
      <h1>Size</h1>
      <div className="notification-size__wrap">
        <Button onClick={() => openNotification('lg')}>Notice lg</Button>
        <Button onClick={() => openNotification('md')}>Notice md</Button>
        <Button onClick={() => openNotification('sm')}>Notice sm</Button>
      </div>
    </>
  )
}

```

### title.stories.tsx

```typescript
import React from 'react'
import notification from '@hi-ui/notification'
import Button from '@hi-ui/button'

/**
 * @title 通知内容
 */
export const Title = () => {
  return (
    <>
      <h1>Title</h1>
      <div className="notification-title__wrap">
        <Button
          onClick={() => {
            notification.open({
              title: '重要通知：重复三遍',
            })
            notification.open({
              title: '重要通知：重复三遍',
            })
            notification.open({
              title: '重要通知：重复三遍',
            })
          }}
        >
          Notice
        </Button>
      </div>
    </>
  )
}

```

## number-input 组件

### Wheel.stories.tsx

```typescript
import React from 'react'
import NumberInput from '@hi-ui/number-input'

/**
 * @title 滚轮滑动
 */
export const Wheel = () => {
  return (
    <>
      <h1>Wheel</h1>
      <div className="NumberInput-wheel__wrap">
        <NumberInput
          step={10}
          changeOnWheel
          defaultValue={0}
          min={1}
          onChange={(v) => console.log('onChange', v)}
        />
      </div>
    </>
  )
}

```

### addon.stories.tsx

```typescript
import React from 'react'
import NumberInput from '@hi-ui/number-input'
import { AppStoreOutlined } from '@hi-ui/icons'

/**
 * @title 前内置元素
 */
export const Addon = () => {
  return (
    <>
      <h1>NumberInput</h1>
      <div className="NumberInput-addon__wrap">
        <NumberInput
          defaultValue={5}
          min={1}
          placeholder="请输入数字"
          onChange={(v) => console.log('onChange', v)}
          prefix={<AppStoreOutlined />}
        />
      </div>
    </>
  )
}

```

### appearance.stories.tsx

```typescript
import React from 'react'
import NumberInput from '@hi-ui/number-input'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性两种
 */
export const Appearance = () => {
  return (
    <>
      <h1>Appearance</h1>
      <div>
        <h2>outline</h2>
        <NumberInput appearance={'line'} />
        <br />
        <br />
        <NumberInput appearance={'line'} max={2} min={0} defaultValue={5} />
      </div>
      <div>
        <h2>filled</h2>
        <NumberInput appearance={'filled'} />
        <br />
        <br />
        <NumberInput appearance={'filled'} max={2} min={0} defaultValue={5} />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import NumberInput from '@hi-ui/number-input'

/**
 * @title 基础用法
 * @desc 用于输入数字的输入框
 */
export const Basic = () => {
  return (
    <>
      <h1>NumberInput</h1>
      <div className="NumberInput-basic__wrap">
        <NumberInput
          autoFocus
          defaultValue={5}
          min={1}
          placeholder="请输入数字"
          onChange={(v) => console.log('onChange', v)}
        />
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import NumberInput from '@hi-ui/number-input'
import Button from '@hi-ui/button'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [current, setCurrent] = React.useState<number | null>(1)
  return (
    <>
      <h1>Controlled</h1>
      <div className="NumberInput-controlled__wrap">
        <NumberInput
          value={current}
          min={1}
          onChange={(v) => {
            console.log('onChange', v)
            setCurrent(v)
          }}
        />

        <br />
        <br />
        <Button onClick={() => setCurrent(5)}>更新为 5</Button>
      </div>
    </>
  )
}

```

### formatter.stories.tsx

```typescript
import React from 'react'
import NumberInput from '@hi-ui/number-input'

/**
 * @title 格式化展示
 * @desc 自定义格式化展示
 */
export const Formatter = () => {
  const currency = {
    format(value: string) {
      return value.replace(/\d+/, (ret) => {
        return ret.replace(/(\d)(?=(\d{3})+$)/g, ($1) => $1 + ',')
      })
    },
    pure(valueString: string) {
      return valueString.replace(/[^\d|.]/g, '')
    },
  }

  function formatNumberPrecision(
    num: number,
    precision = 2,
    precisionMode: 'cut' | 'round' = 'round'
  ) {
    if (isNaN(num) || isNaN(precision)) {
      return num
    }

    let result: string | number = num

    if (precisionMode === 'round') {
      result = Math.round(num * Math.pow(10, precision)) / Math.pow(10, precision)
      if (
        String(result).split('.').length === 1 ||
        String(result).split('.')[1].length < precision
      ) {
        return parseFloat(String(result)).toFixed(precision)
      }
    }

    if (precisionMode === 'cut') {
      if (String(result).split('.')[1]?.length > precision) {
        result = String(result).substring(0, String(result).indexOf('.') + precision + 1)
      }
      return parseFloat(String(result)).toFixed(precision)
    }

    return result
  }

  const [value, setValue] = React.useState<number | null>(1234)

  return (
    <>
      <h1>NumberInput formatter</h1>
      <div className="NumberInput-formatter__wrap">
        <h2>千分位展示</h2>
        <NumberInput
          defaultValue={1234}
          min={1}
          formatter={(value) => currency.format(value + '')}
          parser={(value) => Number(currency.pure(value + ''))}
          onChange={(v) => console.log('onChange', v)}
        />
        <h2>千分位展示 受控</h2>
        <NumberInput
          value={value}
          min={0}
          formatter={(value) => currency.format(value + '')}
          parser={(value) => Number(currency.pure(value + ''))}
          onChange={(v) => {
            console.log('onChange', v)
            setValue(v)
          }}
        />
        <h2>小数点精度展示</h2>
        <NumberInput
          defaultValue={null}
          formatter={(value) => formatNumberPrecision(Number(value), 2, 'cut')}
          onChange={(v) => console.log('onChange', v)}
        />
        <h2>小数点精度展示 受控</h2>
        <NumberInput
          value={value}
          min={0}
          formatter={(value) => formatNumberPrecision(Number(value), 2, 'round')}
          onChange={(v) => {
            console.log('onChange', v)
            setValue(v)
          }}
        />
      </div>
    </>
  )
}

```

### invalid.stories.tsx

```typescript
import React from 'react'
import { NumberInput } from '@hi-ui/number-input'

/**
 * @title 无效态
 * @desc 输入无效或异常时可激活此态
 */
export const Invalid = () => {
  return (
    <>
      <h1>NumberInput</h1>
      <div className="NumberInput-invalid__wrap">
        <NumberInput invalid appearance={'line'} defaultValue={5} />
        <br />
        <br />
        <NumberInput invalid appearance={'filled'} defaultValue={5} />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import NumberInput from '@hi-ui/number-input'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>NumberInput size</h1>
      <div>
        <h2>outline</h2>
        <br />
        <br />
        <NumberInput size={'sm'} />
        <br />
        <br />
        <NumberInput size="md" />
        <br />
        <br />
        <NumberInput size={'lg'} />
      </div>
      <div>
        <h2>filled</h2>
        <br />
        <br />
        <NumberInput size={'sm'} appearance={'filled'} />
        <br />
        <br />
        <NumberInput size="md" appearance={'filled'} />
        <br />
        <br />
        <NumberInput size={'lg'} appearance={'filled'} />
      </div>
    </>
  )
}

```

### step.stories.tsx

```typescript
import React from 'react'
import NumberInput from '@hi-ui/number-input'

/**
 * @title 自定义步长
 */
export const Step = () => {
  return (
    <>
      <h1>Step</h1>
      <div className="NumberInput-step__wrap">
        <NumberInput
          step={0.1}
          defaultValue={0}
          min={1}
          onChange={(v) => console.log('onChange', v)}
        />
      </div>
    </>
  )
}

```

## pagination 组件

### basic.stories.tsx

```typescript
import React, { useState } from 'react'
import Pagination from '@hi-ui/pagination'

/**
 * @title 基础用法
 * @desc 常见的分页用法，用于数据量或分页数适中的场景，进行基础翻页操作
 */
export const Basic = () => {
  const [current, updateCurrent] = useState(1)
  return (
    <>
      <h1>Basic for Pagination</h1>
      <div className="pagination-basic__wrap">
        <Pagination
          total={200}
          pageSize={10}
          current={current}
          onChange={(cur, prev, pageSize) => {
            updateCurrent(cur)
            console.log('onChange', cur, prev, pageSize)
          }}
        />
      </div>
    </>
  )
}

```

### custom.stories.tsx

```typescript
import React from 'react'
import Pagination from '@hi-ui/pagination'
import Form from '@hi-ui/form'
import Switch from '@hi-ui/switch'
import Select from '@hi-ui/select'
import NumberInput from '@hi-ui/number-input'

/**
 * @title 自定义组合
 * @desc 灵活搭配，适配不同的场景
 */
export const Custom = () => {
  const [paginationProps, setPaginationProps] = React.useState<any>({
    total: 200,
    showTotal: true,
    showJumper: true,
    showPagers: true,
    pageSize: 10,
    pageSizeOptions: [10, 20, 50, 100],
    current: 1,
  })

  return (
    <>
      <h1>自定义组合</h1>
      <div className="pagination-basic__wrap">
        <div>
          <Form
            initialValues={paginationProps}
            onValuesChange={(_, allValues) => {
              setPaginationProps(allValues)
            }}
            style={{ display: 'flex', columnGap: 36, flexWrap: 'wrap' }}
          >
            <Form.Item label="ShowTotal" field="showTotal" valuePropName="checked">
              <Switch />
            </Form.Item>
            <Form.Item label="ShowJumper" field="showJumper" valuePropName="checked">
              <Switch />
            </Form.Item>
            <Form.Item label="ShowPagers" field="showPagers" valuePropName="checked">
              <Switch />
            </Form.Item>
            <Form.Item label="PageSize" field="pageSize">
              <Select
                clearable={false}
                data={[
                  { id: 10, title: '10' },
                  { id: 20, title: '20' },
                  { id: 50, title: '50' },
                  { id: 100, title: '100' },
                ]}
              />
            </Form.Item>
            <Form.Item label="Total" field="total">
              <NumberInput />
            </Form.Item>
          </Form>
        </div>
        <Pagination
          {...paginationProps}
          onChange={(cur) => {
            // updateCurrent(cur)
          }}
        />
      </div>
    </>
  )
}

```

### mini-input.stories.tsx

```typescript
import React, { useState } from 'react'
import { Pagination } from '@hi-ui/pagination'

/**
 * @title 文本框用法
 * @desc 节省页码的占用空间
 */
export const MiniInput = () => {
  const [current, setCurrent] = useState(1)
  return (
    <>
      <h1>MiniInput</h1>
      <div className="pagination-mini-input__wrap">
        <Pagination
          type="shrink"
          total={200}
          pageSize={10}
          current={current}
          onChange={(cur) => {
            console.log('onChange', cur)
            setCurrent(cur)
          }}
        />
      </div>
    </>
  )
}

```

### page-size-options.stories.tsx

```typescript
import React, { useState } from 'react'
import Pagination from '@hi-ui/pagination'

/**
 * @title 每页最大条数
 * @desc 数据量庞大，分页数较多时使用
 */
export const PageSizeOptions = () => {
  const [current, updateCurrent] = useState(1)
  const [pageSize, updatePageSize] = useState(10)

  return (
    <>
      <h1>Different page size options</h1>
      <div className="pagination-basic__wrap">
        <Pagination
          total={200}
          pageSize={pageSize}
          showTotal
          showJumper
          pageSizeOptions={[10, 20, 50, 100]}
          onPageSizeChange={(pageSize, current) => {
            console.log('onPageSizeChange', pageSize, current)
            updatePageSize(pageSize)
          }}
          current={current}
          onChange={(cur, prev, pageSize) => {
            console.log('onChange', cur, prev, pageSize)
            updateCurrent(cur)
          }}
        />
      </div>
    </>
  )
}

```

### simple.stories.tsx

```typescript
import React, { useState } from 'react'
import { Pagination } from '@hi-ui/pagination'

/**
 * @title 简洁用法
 * @desc 数据分批展示的形式，弱化页码
 */
export const Simple = () => {
  const [current, setCurrent] = useState(1)
  return (
    <>
      <h1>Simple</h1>
      <div className="pagination-simple__wrap">
        <Pagination
          type="shrink"
          total={200}
          pageSize={10}
          showJumper={false}
          current={current}
          onChange={(cur) => {
            console.log('onChange', cur)
            setCurrent(cur)
          }}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Pagination from '@hi-ui/pagination'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>不同尺寸</h1>
      <div className="button-basic__wrap">
        <div style={{ marginBottom: 20 }}>
          <Pagination
            total={200}
            pageSize={10}
            showTotal
            showJumper
            showPagers
            size="sm"
            onChange={(cur, prev, pageSize) => {
              console.log('onChange', cur, prev, pageSize)
            }}
          />
        </div>
        <div style={{ marginBottom: 20 }}>
          <Pagination
            type="shrink"
            total={200}
            pageSize={10}
            size={'sm'}
            onChange={(cur) => {
              console.log('onChange', cur)
            }}
          />
        </div>
        <div style={{ marginBottom: 20 }}>
          <Pagination
            total={200}
            pageSize={10}
            showTotal
            showJumper
            showPagers
            size="md"
            onChange={(cur, prev, pageSize) => {
              console.log('onChange', cur, prev, pageSize)
            }}
          />
        </div>
        <div style={{ marginBottom: 20 }}>
          <Pagination
            type="shrink"
            total={200}
            pageSize={10}
            size="md"
            onChange={(cur) => {
              console.log('onChange', cur)
            }}
          />
        </div>
        <div style={{ marginBottom: 24 }}></div>
      </div>
    </>
  )
}

```

## picker 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Picker from '@hi-ui/picker'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="picker-basic__wrap">
        <Picker searchable trigger={<Button>Trigger</Button>} footer="1">
          <div>content</div>
        </Picker>
      </div>
    </>
  )
}

```

## pop-confirm 组件

### async.stories.tsx

```typescript
import Button from '@hi-ui/button'
import React from 'react'
import PopConfirm from '@hi-ui/pop-confirm'

/**
 * @title 异步确认关闭
 * @desc 自定义 `footer` 实现自定义确认按钮以及点击事件
 */
export const Async = () => {
  const [visible, setVisible] = React.useState(false)
  const [loading, setLoading] = React.useState(false)
  return (
    <>
      <h1>Async</h1>
      <div className="pop-confirm-async__wrap">
        <PopConfirm
          title="Are you OK ?"
          visible={visible}
          footer={[
            <Button key="1" type="default" size="md" onClick={() => setVisible(false)}>
              取消
            </Button>,
            <Button
              key="2"
              type="primary"
              size="md"
              loading={loading}
              onClick={() => {
                setLoading(true)
                setTimeout(() => {
                  setLoading(false)
                  setVisible(false)
                }, 2000)
              }}
            >
              确认
            </Button>,
          ]}
        >
          <Button onClick={() => setVisible(true)}>Trigger</Button>
        </PopConfirm>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import Button from '@hi-ui/button'
import React from 'react'
import PopConfirm from '@hi-ui/pop-confirm'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="pop-confirm-basic__wrap">
        <PopConfirm title="Delete this item along with the entered content?">
          <Button>Trigger</Button>
        </PopConfirm>
      </div>
    </>
  )
}

```

### custom-content.stories.tsx

```typescript
import Button from '@hi-ui/button'
import React from 'react'
import PopConfirm from '@hi-ui/pop-confirm'

/**
 * @title 自定义内容
 */
export const CustomContent = () => {
  return (
    <>
      <h1>CustomContent</h1>
      <div className="pop-confirm-basic__wrap">
        <PopConfirm
          title={
            <div style={{ whiteSpace: 'normal' }}>很长的通知标题很长的通知标题很长的通知标题</div>
          }
          content={<div>这是一段很长的内容这是一段很长的内容这是一段很长的内容</div>}
          style={{ maxWidth: 300 }}
        >
          <Button>Trigger</Button>
        </PopConfirm>
      </div>
    </>
  )
}

```

### custom-icon.stories.tsx

```typescript
import Button from '@hi-ui/button'
import { AssetMonitorFilled } from '@hi-ui/icons'
import React from 'react'
import PopConfirm from '@hi-ui/pop-confirm'

/**
 * @title 自定义图标
 */
export const customIcon = () => {
  return (
    <>
      <h1>customIcon</h1>
      <div className="pop-confirm-custom-icon__wrap">
        <PopConfirm title="Are you OK ?" icon={<AssetMonitorFilled />}>
          <Button>Trigger</Button>
        </PopConfirm>
      </div>
    </>
  )
}

```

### gutter-gap.stories.tsx

```typescript
import React from 'react'
import PopConfirm from '@hi-ui/pop-confirm'
import Button from '@hi-ui/button'

/**
 * @title 设置间隙偏移量
 * @desc 设置基于依附元素的间隙偏移量
 */
export const GutterGap = () => {
  return (
    <>
      <h1>Gutter Gap</h1>
      <div className="pop-confirm-basic__wrap">
        <PopConfirm title="Delete this item along with the entered content?" gutterGap={30}>
          <Button>Trigger</Button>
        </PopConfirm>
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import Button from '@hi-ui/button'
import React from 'react'
import PopConfirm from '@hi-ui/pop-confirm'
import { PopperJS } from '@hi-ui/popper'

/**
 * @title 不同方位
 */
export const Placement = () => {
  const [placement, setPlacement] = React.useState<undefined | PopperJS.Placement>()

  const handleClick = (newPlacement) => () => {
    setPlacement(newPlacement)
  }

  const title = <span>文字提示</span>

  return (
    <>
      <h1>Placement</h1>
      <div className="pop-confirm-placement__wrap">
        <table className="placement-table" cellSpacing="5">
          <tbody>
            <tr>
              <td></td>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('top-start')}>
                    topStart
                  </Button>
                </PopConfirm>
              </td>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('top')}>
                    top
                  </Button>
                </PopConfirm>
              </td>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('top-end')}>
                    topEnd
                  </Button>
                </PopConfirm>
              </td>
              <td></td>
            </tr>
            <tr>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('left-start')}>
                    leftStart
                  </Button>
                </PopConfirm>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('right-start')}>
                    rightStart
                  </Button>
                </PopConfirm>
              </td>
            </tr>
            <tr>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('left')}>
                    left
                  </Button>
                </PopConfirm>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('right')}>
                    right
                  </Button>
                </PopConfirm>
              </td>
            </tr>
            <tr>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('left-end')}>
                    leftEnd
                  </Button>
                </PopConfirm>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('right-end')}>
                    rightEnd
                  </Button>
                </PopConfirm>
              </td>
            </tr>
            <tr>
              <td></td>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('bottom-start')}>
                    bottomStart
                  </Button>
                </PopConfirm>
              </td>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('bottom')}>
                    bottom
                  </Button>
                </PopConfirm>
              </td>
              <td>
                <PopConfirm placement={placement} title={title}>
                  <Button style={{ width: 100 }} onClick={handleClick('bottom-end')}>
                    bottomEnd
                  </Button>
                </PopConfirm>
              </td>
              <td></td>
            </tr>
          </tbody>
        </table>
      </div>
    </>
  )
}

```

## popover 组件

### arrow.stories.tsx

```typescript
import React from 'react'
import Popover from '@hi-ui/popover'
import Button from '@hi-ui/button'

/**
 * @title 不带箭头
 */
export const Arrow = () => {
  return (
    <>
      <h1>Arrow</h1>
      <div className="popper-arrow__wrap">
        <Popover arrow={false} content="Popover 文字内容">
          <Button>trigger</Button>
        </Popover>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Popover from '@hi-ui/popover'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 * @desc 用于信息描述、辅助信息等
 */
export const Basic = () => {
  const title = <span>文字提示</span>
  const content = (
    <div>
      <div>此处展示 Popover 具体内容</div>
      <div>具体内容可以自行渲染</div>
    </div>
  )

  return (
    <>
      <h1>Basic</h1>
      <div className="popover-basic__wrap">
        <Popover title={title} content={content} trigger="click" onExited={() => console.log(33)}>
          <Button>trigger</Button>
        </Popover>
      </div>
    </>
  )
}

```

### content.stories.tsx

```typescript
import React from 'react'
import Popover from '@hi-ui/popover'
import Button from '@hi-ui/button'
import Form from '@hi-ui/form'
import Input from '@hi-ui/input'
import { CloseOutlined } from '@hi-ui/icons'
import { IconButton } from '@hi-ui/icon-button'

/**
 * @title 自定义内容
 */
export const Content = () => {
  const FormItem = Form.Item

  const [visible, setVisible] = React.useState<boolean>(false)
  const [loading, setLoading] = React.useState<boolean>(false)
  const popoverVisibleRef = React.useRef<boolean>(false)

  const title = (
    <div
      style={{
        display: 'flex',
        alignItems: 'center',
        justifyContent: 'space-between',
        height: 20,
      }}
    >
      <span>文字标题</span>
      <IconButton
        effect
        icon={<CloseOutlined />}
        onClick={() => {
          setVisible(false)
          popoverVisibleRef.current = false
        }}
      />
    </div>
  )

  const content = (
    <div style={{ width: 344 }}>
      <div style={{}}>
        <Form
          initialValues={{ testInput: 1, testInput2: 'testInput2' }}
          labelWidth={80}
          labelPlacement="top"
          rules={{
            testInput: [
              {
                required: true,
                message: 'testInput1 is required',
              },
            ],
            testInput2: [
              {
                required: true,
                type: 'string',
                message: 'testInput2 is required',
              },
            ],
          }}
        >
          <FormItem field="testInput" valueType="number" label="用户名" required>
            <Input onChange={console.log} />
          </FormItem>
          <FormItem field="testInput2" valueType="string" label="密码" required>
            <Input />
          </FormItem>
        </Form>
      </div>
      <div style={{ textAlign: 'right' }}>
        <Button
          onClick={() => {
            setVisible(false)
            popoverVisibleRef.current = false
          }}
        >
          取消
        </Button>
        <Button
          type="primary"
          loading={loading}
          onClick={() => {
            setLoading(true)
            setTimeout(() => {
              setLoading(false)
              setVisible(false)
              popoverVisibleRef.current = false
            }, 1000)
          }}
        >
          保存
        </Button>
      </div>
    </div>
  )

  return (
    <>
      <h1>Content</h1>
      <div className="popover-basic__wrap">
        <Popover
          title={title}
          content={content}
          trigger="click"
          visible={visible}
          arrow={false}
          crossGap={0}
          placement={'bottom-start'}
          showTitleDivider
          disabledPortal
        >
          <Button
            onClick={() => {
              if (!popoverVisibleRef.current) {
                setVisible(true)
                popoverVisibleRef.current = true
              } else {
                setVisible(false)
                popoverVisibleRef.current = false
              }
            }}
          >
            trigger
          </Button>
        </Popover>
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import Popover from '@hi-ui/popover'
import Button from '@hi-ui/button'

/**
 * @title 受控显隐
 * @desc 如何自定义控制创建可悬停和单击的弹出窗口
 */
export const Controlled = () => {
  const [clickVisible, setClickVisible] = React.useState(false)
  const [hoverVisible, setHoverVisible] = React.useState(false)

  const contentClick = (
    <div>
      <div>此处展示 Popover click 触发后的内容</div>
      <div
        style={{
          color: '#4285f4',
          fontSize: '14px',
          cursor: 'pointer',
          marginTop: '10px',
        }}
        onClick={() => {
          setClickVisible(false)
        }}
      >
        点击关闭
      </div>
    </div>
  )

  return (
    <>
      <h1>Controlled</h1>
      <div className="popover-controlled__wrap">
        <Popover
          title={<span>文字提示</span>}
          content={
            <div>
              <div>此处展示 Popover hover 触发后的内容</div>
            </div>
          }
          visible={hoverVisible}
        >
          <span>
            <Popover visible={clickVisible} title={<span>文字提示</span>} content={contentClick}>
              <Button
                onMouseEnter={() => {
                  setHoverVisible(true)
                  setClickVisible(false)
                }}
                onMouseLeave={() => {
                  setHoverVisible(false)
                }}
                onClick={() => {
                  setHoverVisible(false)
                  setClickVisible((prev) => !prev)
                }}
              >
                Hover and click / 悬停并单击
              </Button>
            </Popover>
          </span>
        </Popover>
      </div>
    </>
  )
}

```

### gutter-gap.stories.tsx

```typescript
import React from 'react'
import Popover from '@hi-ui/popover'
import Button from '@hi-ui/button'

/**
 * @title 设置间隙偏移量
 * @desc 设置基于依附元素的间隙偏移量
 */
export const GutterGap = () => {
  const title = <span>文字提示</span>
  const content = (
    <div>
      <div>此处展示 Popover 具体内容</div>
      <div>具体内容可以自行渲染</div>
    </div>
  )

  return (
    <>
      <h1>Gutter Gap</h1>
      <div className="popover-basic__wrap">
        <Popover title={title} content={content} gutterGap={30} trigger="click">
          <Button>trigger</Button>
        </Popover>
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import React from 'react'
import Popover from '@hi-ui/popover'
import Button from '@hi-ui/button'
import { PopperJS } from '@hi-ui/popper'

/**
 * @title 不同方位
 */
export const Placement = () => {
  const [placement, setPlacement] = React.useState<undefined | PopperJS.Placement>()

  const handleClick = (newPlacement) => () => {
    setPlacement(newPlacement)
  }

  const title = <span>文字提示</span>
  const content = (
    <div>
      <div>当前展示方位：{placement}</div>
    </div>
  )

  return (
    <>
      <h1>Placement</h1>
      <div className="popper-placement__wrap">
        <table className="placement-table" cellSpacing="5">
          <tbody>
            <tr>
              <td></td>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('top-start')}>
                    topStart
                  </Button>
                </Popover>
              </td>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('top')}>
                    top
                  </Button>
                </Popover>
              </td>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('top-end')}>
                    topEnd
                  </Button>
                </Popover>
              </td>
              <td></td>
            </tr>
            <tr>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('left-start')}>
                    leftStart
                  </Button>
                </Popover>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('right-start')}>
                    rightStart
                  </Button>
                </Popover>
              </td>
            </tr>
            <tr>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('left')}>
                    left
                  </Button>
                </Popover>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('right')}>
                    right
                  </Button>
                </Popover>
              </td>
            </tr>
            <tr>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('left-end')}>
                    leftEnd
                  </Button>
                </Popover>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('right-end')}>
                    rightEnd
                  </Button>
                </Popover>
              </td>
            </tr>
            <tr>
              <td></td>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('bottom-start')}>
                    bottomStart
                  </Button>
                </Popover>
              </td>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('bottom')}>
                    bottom
                  </Button>
                </Popover>
              </td>
              <td>
                <Popover placement={placement} title={title} content={content} trigger="click">
                  <Button style={{ width: 100 }} onClick={handleClick('bottom-end')}>
                    bottomEnd
                  </Button>
                </Popover>
              </td>
              <td></td>
            </tr>
          </tbody>
        </table>
      </div>
    </>
  )
}

```

### trigger.stories.tsx

```typescript
import React from 'react'
import Popover from '@hi-ui/popover'
import Button from '@hi-ui/button'

/**
 * @title 自定义触发器
 * @desc 请确保子元素能接受对应的 onMouseEnter、onMouseLeave、onFocus、onClick 事件
 */
export const Trigger = () => {
  const title = <span>文字提示</span>
  const content = (
    <div>
      <div>此处展示 Popover 具体内容</div>
      <div>具体内容可以自行渲染</div>
    </div>
  )

  return (
    <>
      <h1>Trigger</h1>
      <div className="Popover-trigger__wrap">
        <Popover title={title} content={content}>
          <Button>default click</Button>
        </Popover>
        <br />
        <br />
        <Popover title={title} content={content} trigger="hover">
          <Button>hover</Button>
        </Popover>
        <br />
        <br />
        <Popover title={title} content={content} trigger="contextmenu">
          <Button>contextmenu</Button>
        </Popover>
      </div>
    </>
  )
}

```

### with-api.stories.tsx

```typescript
import React from 'react'
import Popover from '@hi-ui/popover'
import Button from '@hi-ui/button'
import Form from '@hi-ui/form'
import Input from '@hi-ui/input'
import { CloseOutlined } from '@hi-ui/icons'
import { IconButton } from '@hi-ui/icon-button'

/**
 * @title API 方式调用
 */
export const WithApi = () => {
  const FormItem = Form.Item
  const key = 'my_key'

  const Title = ({ title }: { title: string }) => {
    return (
      <div
        style={{
          display: 'flex',
          alignItems: 'center',
          justifyContent: 'space-between',
          height: 20,
        }}
      >
        <span>{title}</span>
        <IconButton effect icon={<CloseOutlined />} onClick={() => Popover.close(key)} />
      </div>
    )
  }

  const Content = () => {
    const [loading, setLoading] = React.useState<boolean>(false)

    return (
      <div style={{ width: 344 }}>
        <div style={{}}>
          <Form
            initialValues={{ testInput: 1, testInput2: 'testInput2' }}
            labelWidth={80}
            labelPlacement="top"
            rules={{
              testInput: [
                {
                  required: true,
                  message: 'testInput1 is required',
                },
              ],
              testInput2: [
                {
                  required: true,
                  type: 'string',
                  message: 'testInput2 is required',
                },
              ],
            }}
          >
            <FormItem field="testInput" valueType="number" label="用户名" required>
              <Input onChange={console.log} />
            </FormItem>
            <FormItem field="testInput2" valueType="string" label="密码" required>
              <Input />
            </FormItem>
          </Form>
        </div>
        <div style={{ display: 'flex' }}>
          <Button style={{ flex: 1 }} onClick={() => Popover.close(key)}>
            取消
          </Button>
          <Button
            style={{ flex: 1 }}
            type="primary"
            loading={loading}
            onClick={() => {
              setLoading(true)
              setTimeout(() => {
                setLoading(false)
                Popover.close(key)
              }, 1000)
            }}
          >
            保存
          </Button>
        </div>
      </div>
    )
  }

  return (
    <>
      <h1>WithApi</h1>
      <div className="popover-basic__wrap">
        <h4>此处展示多个操作使用同一个容器，即 API 调用时，将 key 设置为同一个</h4>
        <Button
          onClick={(e) => {
            Popover.open(e.target as HTMLElement, {
              key: key,
              title: <Title title="文字标题" />,
              content: <Content />,
              arrow: false,
              crossGap: 0,
              placement: 'bottom-start',
              showTitleDivider: true,
              disabledPortal: true,
              zIndex: 99,
            })
          }}
        >
          trigger 1
        </Button>
        <Button
          onClick={(e) => {
            Popover.open(e.target as HTMLElement, {
              key: key,
              title: <Title title="文字标题 2" />,
              content: <Content />,
              arrow: false,
              crossGap: 0,
              placement: 'bottom-start',
              showTitleDivider: true,
              disabledPortal: true,
              zIndex: 99,
            })
          }}
        >
          trigger 2
        </Button>
      </div>
    </>
  )
}

```

## popper 组件

### arrow.stories.tsx

```typescript
import React from 'react'
import Popper, { PopperJS } from '@hi-ui/popper'
import Button from '@hi-ui/button'

/**
 * @title 不带箭头
 */
export const Arrow = () => {
  const [btnEl, setBtnEl] = React.useState(null)
  const [visible, setVisible] = React.useState(false)
  const [placement, setPlacement] = React.useState<undefined | PopperJS.Placement>()

  const handleClick = (newPlacement) => (event) => {
    setBtnEl(event.currentTarget)
    setPlacement(newPlacement)
    setVisible(true)
  }

  return (
    <>
      <h1>Arrow</h1>
      <div className="popper-arrow__wrap">
        <Popper
          visible={visible}
          attachEl={btnEl}
          placement={placement}
          onClose={() => setVisible(false)}
          arrow
        >
          <div style={{ width: 200, height: 80 }}>Here is HiUI Popper.</div>
        </Popper>

        <table className="placement-table" cellSpacing="5">
          <tbody>
            <tr>
              <td></td>
              <td>
                <Button onClick={handleClick('top-start')}>topStart</Button>
              </td>
              <td>
                <Button onClick={handleClick('top')}>top</Button>
              </td>
              <td>
                <Button onClick={handleClick('top-end')}>topEnd</Button>
              </td>
              <td></td>
            </tr>
            <tr>
              <td>
                <Button onClick={handleClick('left-start')}>leftStart</Button>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Button onClick={handleClick('right-start')}>rightStart</Button>
              </td>
            </tr>
            <tr>
              <td>
                <Button onClick={handleClick('left')}>left</Button>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Button onClick={handleClick('right')}>right</Button>
              </td>
            </tr>
            <tr>
              <td>
                <Button onClick={handleClick('left-end')}>leftEnd</Button>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Button onClick={handleClick('right-end')}>rightEnd</Button>
              </td>
            </tr>
            <tr>
              <td></td>
              <td>
                <Button onClick={handleClick('bottom-start')}>bottomStart</Button>
              </td>
              <td>
                <Button onClick={handleClick('bottom')}>bottom</Button>
              </td>
              <td>
                <Button onClick={handleClick('bottom-end')}>bottomEnd</Button>
              </td>
              <td></td>
            </tr>
          </tbody>
        </table>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Popper from '@hi-ui/popper'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const [btnRef, setBtnRef] = React.useState(null)
  const [visible, setVisible] = React.useState(false)

  return (
    <>
      <h1>Basic</h1>
      <div className="popper-basic__wrap">
        <Button ref={setBtnRef} onClick={() => setVisible(true)}>
          Open
        </Button>
        <Popper
          visible={visible}
          attachEl={btnRef}
          onClose={() => {
            console.log('onClose')
            setVisible(false)
          }}
        >
          The content of the Popper.
        </Popper>
      </div>
    </>
  )
}

```

### container.stories.tsx

```typescript
import React from 'react'
import Popper from '@hi-ui/popper'
import Button from '@hi-ui/button'

/**
 * @title 指定挂载容器
 * @desc 默认挂载到 body 下
 */
export const Container = () => {
  const [btnRef, setBtnRef] = React.useState(null)
  const [visible, setVisible] = React.useState(false)
  const containerRef = React.useRef(null)

  return (
    <div
      style={{
        width: '60vw',
        height: '200px',
        overflow: 'auto',
        border: '1px solid #eee',
        position: 'relative',
      }}
    >
      <h1>Container</h1>
      <div
        ref={containerRef}
        className="popper-container__wrap"
        style={{ zoom: 2, height: '200vh' }}
      >
        <Button ref={setBtnRef} onClick={() => setVisible(true)}>
          Open
        </Button>
        <Popper
          visible={visible}
          attachEl={btnRef}
          onClose={() => setVisible(false)}
          container={btnRef}
        >
          The content of the Popper.
        </Popper>
      </div>
    </div>
  )
}

```

### hook.stories.tsx

```typescript
import React from 'react'
import { usePopper } from '@hi-ui/popper'
import Button from '@hi-ui/button'

/**
 * @title usePopper
 */
export const Hook = () => {
  const [btnEl, setBtnEl] = React.useState(null)
  const [visible, setVisible] = React.useState(false)
  const { shouldRenderPopper, getPopperProps } = usePopper({
    attachEl: btnEl,
    visible,
    placement: 'bottom-end',
    onClose: () => setVisible(false),
    unmountOnClose: false,
    // preload: true,
  })

  return (
    <>
      <h1>Hook</h1>
      <div className="popper-hook__wrap">
        <Button ref={setBtnEl} onClick={() => setVisible((prev) => !prev)}>
          Open
        </Button>
        {shouldRenderPopper ? (
          <div {...getPopperProps()}>The content of the Popper.The content of the Popper.</div>
        ) : null}
      </div>
    </>
  )
}

```

### lazy.stories.tsx

```typescript
import React from 'react'
import Popper from '@hi-ui/popper'
import Button from '@hi-ui/button'

/**
 * @title 性能优化
 */
export const Lazy = () => {
  const [btnRef, setBtnRef] = React.useState(null)
  const [visible, setVisible] = React.useState(false)

  return (
    <>
      <h1>Lazy</h1>
      <div className="popper-lazy__wrap">
        <Button ref={setBtnRef} onClick={() => setVisible(true)}>
          Open
        </Button>
        <div>
          <h1>unmountOnClose</h1>
          <Popper visible={visible} attachEl={btnRef} onClose={() => setVisible(false)}>
            The content of the Popper1.
          </Popper>
        </div>
        <div>
          <h1>lazyLoad</h1>
          <Popper
            visible={visible}
            preload={false}
            unmountOnClose={false}
            placement="top"
            attachEl={btnRef}
            onClose={() => setVisible(false)}
          >
            The content of the Popper2.
          </Popper>
        </div>
        <div>
          <h1>keep</h1>
          <Popper
            visible={visible}
            preload={true}
            unmountOnClose={false}
            placement="right"
            attachEl={btnRef}
            onClose={() => setVisible(false)}
          >
            The content of the Popper3.
          </Popper>
        </div>
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import React from 'react'
import Popper, { PopperPlacementEnum } from '@hi-ui/popper'
import Button from '@hi-ui/button'

/**
 * @title 不同方位
 */
export const Placement = () => {
  const [btnEl, setBtnEl] = React.useState(null)
  const [visible, setVisible] = React.useState(false)
  const [placement, setPlacement] = React.useState<undefined | PopperPlacementEnum>()

  const handleClick = (newPlacement) => (event) => {
    setBtnEl(event.currentTarget)
    setPlacement(newPlacement)
    setVisible(true)
  }

  return (
    <>
      <h1>Placement</h1>
      <div className="popper-placement__wrap">
        <Popper
          visible={visible}
          attachEl={btnEl}
          placement={placement}
          onClose={() => setVisible(false)}
        >
          {/* <div style={{ width: 200 }}>HiUI</div> */}
          {/* <div style={{ height: 200 }}>HiUI</div> */}
          {/* <div style={{ width: 200, height: 200 }}>HiUI</div> */}
        </Popper>

        <table className="placement-table" cellSpacing="5">
          <tbody>
            <tr>
              <td></td>
              <td>
                <Button onClick={handleClick('top-start')}>topStart</Button>
              </td>
              <td>
                <Button onClick={handleClick('top')}>top</Button>
              </td>
              <td>
                <Button onClick={handleClick('top-end')}>topEnd</Button>
              </td>
              <td></td>
            </tr>
            <tr>
              <td>
                <Button onClick={handleClick('left-start')}>leftStart</Button>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Button onClick={handleClick('right-start')}>rightStart</Button>
              </td>
            </tr>
            <tr>
              <td>
                <Button onClick={handleClick('left')}>left</Button>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Button onClick={handleClick('right')}>right</Button>
              </td>
            </tr>
            <tr>
              <td>
                <Button onClick={handleClick('left-end')}>leftEnd</Button>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Button onClick={handleClick('right-end')}>rightEnd</Button>
              </td>
            </tr>
            <tr>
              <td></td>
              <td>
                <Button onClick={handleClick('bottom-start')}>bottomStart</Button>
              </td>
              <td>
                <Button onClick={handleClick('bottom')}>bottom</Button>
              </td>
              <td>
                <Button onClick={handleClick('bottom-end')}>bottomEnd</Button>
              </td>
              <td></td>
            </tr>
          </tbody>
        </table>
      </div>
    </>
  )
}

```

### portal.stories.tsx

```typescript
import React from 'react'
import Popper from '@hi-ui/popper'
import Button from '@hi-ui/button'

/**
 * @title 跟随当前文档流
 */
export const Portal = () => {
  const [btnRef, setBtnRef] = React.useState(null)
  const [visible, setVisible] = React.useState(false)

  return (
    <>
      <h1>Portal</h1>
      <div className="popper-portal__wrap">
        <Button ref={setBtnRef} onClick={() => setVisible(true)}>
          Open
        </Button>
        <Popper
          visible={visible}
          disabledPortal
          attachEl={btnRef}
          onClose={() => setVisible(false)}
        >
          The content of the Popper.
        </Popper>
      </div>
    </>
  )
}

```

### toggle.stories.tsx

```typescript
import React from 'react'
import Popper from '@hi-ui/popper'
import Button from '@hi-ui/button'
import { useToggle } from '@hi-ui/hooks'

/**
 * @title 受控显隐
 */
export const Toggle = () => {
  const [btnRef, setBtnRef] = React.useState(null)
  const [visible, visibleAction] = useToggle(true)

  return (
    <>
      <h1>Toggle</h1>
      <div className="popper-toggle__wrap">
        <Button ref={setBtnRef} onClick={() => visibleAction.not()}>
          Toggle
        </Button>
        <Popper visible={visible} attachEl={btnRef} onClose={() => visibleAction.off()}>
          The content of the Popper.
        </Popper>
      </div>
    </>
  )
}

```

## portal 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Portal from '@hi-ui/portal'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="portal-basic__wrap">
        <Portal>
          <div
            style={{
              position: 'fixed',
              top: '50%',
              left: '50%',
              padding: 20,
              background: 'rgb(160, 182, 249)',
            }}
          >
            Portal
          </div>
        </Portal>
      </div>
    </>
  )
}

```

## portal-context 组件

### basic.stories.tsx

```typescript
import React, { useContext } from 'react'
import { PortalContext } from '@hi-ui/portal-context'

/**
 * @title 基础用法
 */
export const Basic = () => {
  useContext(PortalContext)

  return (
    <>
      <h1>Basic</h1>
      <div className="portal-context-basic__wrap"></div>
    </>
  )
}

```

## preview 组件

### banned.stories.tsx

```typescript
import React from 'react'
import Preview from '@hi-ui/preview'
import Grid from '@hi-ui/grid'

/**
 * @title 禁止右键下载
 */
export const Banned = () => {
  const [showIndex, setShowIndex] = React.useState(-1)
  const [images] = React.useState([
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_1.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_2.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_3.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_4.png',
  ])

  return (
    <>
      <h1>Banned</h1>
      <div className="preview-banned__wrap">
        <Preview
          title={`pic_${showIndex}.png`}
          src={images[showIndex]}
          visible={showIndex !== -1}
          disabledDownload={true}
          onClose={() => {
            setShowIndex(-1)
          }}
        />

        <Grid.Row gutter={true}>
          {images.map((url, index) => {
            return (
              <Grid.Col span={4} key={index}>
                <div>
                  <img
                    src={url}
                    style={{ width: '100%', cursor: 'pointer' }}
                    onClick={() => {
                      setShowIndex(index)
                    }}
                  />
                </div>
              </Grid.Col>
            )
          })}
        </Grid.Row>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Preview from '@hi-ui/preview'
import Grid from '@hi-ui/grid'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const [showIndex, setShowIndex] = React.useState(-1)
  const [images] = React.useState([
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_1.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_2.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_3.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_4.png',
  ])

  return (
    <>
      <h1>Basic</h1>
      <div className="preview-basic__wrap">
        <Preview
          title={`pic_${showIndex}.png`}
          src={images[showIndex]}
          visible={showIndex !== -1}
          onClose={() => {
            setShowIndex(-1)
          }}
        />

        <Grid.Row gutter={true}>
          {images.map((url, index) => {
            return (
              <Grid.Col span={4} key={index}>
                <div>
                  <img
                    src={url}
                    style={{ width: '100%', cursor: 'pointer' }}
                    onClick={() => {
                      setShowIndex(index)
                    }}
                  />
                </div>
              </Grid.Col>
            )
          })}
        </Grid.Row>
      </div>
    </>
  )
}

```

### multiple.stories.tsx

```typescript
import React from 'react'
import Preview from '@hi-ui/preview'
import Grid from '@hi-ui/grid'

/**
 * @title 多图预览
 */
export const Multiple = () => {
  const [images] = React.useState([
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_1.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_2.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_3.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_4.png',
  ])
  const [visible, setVisible] = React.useState(false)
  const [current, setCurrent] = React.useState(0)

  return (
    <>
      <h1>Multiple</h1>
      <div className="preview-multiple__wrap">
        <Preview
          title={`${current + 1}/${images.length}`}
          src={images}
          current={current}
          onPreviewChange={setCurrent}
          visible={visible}
          onClose={() => {
            setVisible(false)
          }}
        />

        <Grid.Row gutter={true}>
          {images.map((url, index) => {
            return (
              <Grid.Col span={4} key={index}>
                <div>
                  <img
                    src={url}
                    style={{ width: '100%', cursor: 'pointer' }}
                    onClick={() => {
                      setCurrent(index)
                      setVisible(true)
                    }}
                  />
                </div>
              </Grid.Col>
            )
          })}
        </Grid.Row>
      </div>
    </>
  )
}

```

### watermark.stories.tsx

```typescript
import React from 'react'
import Preview from '@hi-ui/preview'
import Grid from '@hi-ui/grid'

/**
 * @title 添加水印
 */
export const Watermark = () => {
  const [showIndex, setShowIndex] = React.useState(-1)
  const [images] = React.useState([
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_1.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_2.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_3.png',
    'http://i1.mifile.cn/f/i/hiui/docs/card/pic_4.png',
  ])

  return (
    <>
      <h1>Watermark</h1>
      <div className="preview-watermark__wrap">
        <Preview
          title={`pic_${showIndex}.png`}
          src={images[showIndex]}
          visible={showIndex !== -1}
          onClose={() => {
            setShowIndex(-1)
          }}
          watermarkProps={{
            content: ['HiUI', '做中台，就用 HiUI'],
            style: {
              pointerEvents: 'none',
              position: 'fixed',
              top: 0,
              right: 0,
              bottom: 0,
              left: 0,
              zIndex: 2048,
            },
          }}
        />

        <Grid.Row gutter={true}>
          {images.map((url, index) => {
            return (
              <Grid.Col span={4} key={index}>
                <div>
                  <img
                    src={url}
                    style={{ width: '100%', cursor: 'pointer' }}
                    onClick={() => {
                      setShowIndex(index)
                    }}
                  />
                </div>
              </Grid.Col>
            )
          })}
        </Grid.Row>
      </div>
    </>
  )
}

```

## progress 组件

### bar-size.stories.tsx

```typescript
import React from 'react'
import Progress from '@hi-ui/progress'

/**
 * @title 条形进度条不同尺寸
 */
export const BarSize = () => {
  return (
    <>
      <h1>条形进度条尺寸</h1>
      <div className="progress-basic__wrap">
        <Progress percent={75} size="sm" />
        <br />
        <Progress percent={75} />
        <br />
        <Progress percent={75} size="lg" active />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Progress from '@hi-ui/progress'

/**
 * @title 基础用法
 * @desc 有足够的空间，突出展示进度状态
 */
export const Basic = () => {
  return (
    <>
      <h1>条形进度条</h1>
      <div className="progress-basic__wrap">
        <Progress type="success" content="成功" percent={100} />
        <br />
        <Progress type="warning" content="警示" percent={50} />
        <br />
        <Progress type="error" content="错误" percent={20} />
        <br />
        <Progress type="primary" percent={75} />
        <br />
      </div>
    </>
  )
}

```

### circle-size.stories.tsx

```typescript
import React from 'react'
import { CircleProgress } from '@hi-ui/progress'

/**
 * @title 环形进度条尺寸
 */
export const CircleSize = () => {
  return (
    <>
      <h1>环形进度条尺寸</h1>
      <div
        className="progress-circle-size__wrap"
        style={{ display: 'flex', flexWrap: 'wrap', alignItems: 'center', gap: 48 }}
      >
        <CircleProgress percent={75} size="sm" />
        <CircleProgress percent={75} />
        <CircleProgress percent={75} size="lg" />
      </div>
    </>
  )
}

```

### circle.stories.tsx

```typescript
import React from 'react'
import { CircleProgress } from '@hi-ui/progress'
import { CheckOutlined, CloseOutlined, ExclamationOutlined } from '@hi-ui/icons'

/**
 * @title 环形用法
 * @desc 在局限空间里展示加载进度，如图片上传、附件上传
 */
export const Circle = () => {
  return (
    <>
      <h1>环形用法</h1>
      <div className="progress-circle__wrap" style={{ display: 'flex', flexWrap: 'wrap', gap: 48 }}>
        <CircleProgress percent={75} />

        <CircleProgress
          type="success"
          content={<CheckOutlined style={{ fontSize: '20px' }} />}
          percent={100}
        />

        <CircleProgress
          type="warning"
          content={<CloseOutlined style={{ fontSize: '20px' }} />}
          percent={50}
        />

        <CircleProgress
          type="error"
          content={<ExclamationOutlined style={{ fontSize: '20px' }} />}
          percent={20}
        />
      </div>
    </>
  )
}

```

### custom-percent.stories.tsx

```typescript
import React from 'react'
import Progress from '@hi-ui/progress'
import Counter from '@hi-ui/counter'

/**
 * @title 自定义进度
 * @desc 设置组件和进度条的配合使用
 */
export const CustomPercent = () => {
  const [percent, setPercent] = React.useState(0)

  return (
    <>
      <h1>条形进度条</h1>
      <div
        className="progress-custom-percent__wrap"
        style={{ display: 'flex', flexWrap: 'wrap', alignItems: 'center', gap: 48 }}
      >
        <Progress percent={percent} size="lg" />
        <div>
          <Counter
            value={percent}
            step={10}
            min={0}
            max={100}
            onChange={(percent) => {
              setPercent(percent)
            }}
          />
        </div>
      </div>
    </>
  )
}

```

### dashboard-size.stories.tsx

```typescript
import React from 'react'
import { DashboardProgress } from '@hi-ui/progress'

/**
 * @title 仪表盘不同尺寸
 */
export const DashboardSize = () => {
  return (
    <>
      <h1>仪表盘不同尺寸</h1>
      <div
        className="progress-dashboard-size__wrap"
        style={{ display: 'flex', flexWrap: 'wrap', alignItems: 'center', gap: 48 }}
      >
        <DashboardProgress percent={75} size="sm" />
        <DashboardProgress percent={75} />
        <DashboardProgress percent={75} size="lg" />
      </div>
    </>
  )
}

```

### dashboard.stories.tsx

```typescript
import React from 'react'
import { DashboardProgress } from '@hi-ui/progress'
import { CheckOutlined, CloseOutlined, ExclamationOutlined } from '@hi-ui/icons'

/**
 * @title 仪表盘用法
 * @desc 设置组件和进度条的配合使用
 */
export const Dashboard = () => {
  return (
    <>
      <h1>Dashboard</h1>
      <div
        className="progress-dashboard__wrap"
        style={{ display: 'flex', flexWrap: 'wrap', alignItems: 'center', gap: 48 }}
      >
        <DashboardProgress content="成功" percent={80} />

        <DashboardProgress
          type="success"
          content={<CheckOutlined style={{ fontSize: '20px' }} />}
          percent={100}
        />

        <DashboardProgress
          type="warning"
          content={<CloseOutlined style={{ fontSize: '20px' }} />}
          percent={50}
        />

        <DashboardProgress
          type="error"
          content={<ExclamationOutlined style={{ fontSize: '20px' }} />}
          percent={20}
        />
        <DashboardProgress percent={75} />
      </div>
    </>
  )
}

```

### indeterminate.stories.tsx

```typescript
import React from 'react'
import Progress from '@hi-ui/progress'

/**
 * @title 等待中进度
 */
export const Indeterminate = () => {
  return (
    <>
      <h1>Indeterminate</h1>
      <div className="progress-indeterminate__wrap">
        <Progress indeterminate />
      </div>
    </>
  )
}

```

### inside.stories.tsx

```typescript
import React from 'react'
import Progress from '@hi-ui/progress'

/**
 * @title 文字内显
 * @desc 设置组件和进度条的配合使用
 */
export const Inside = () => {
  return (
    <>
      <h1>文字内显</h1>
      <div className="progress-basic__wrap">
        <Progress percent={0} placement="inside" strokeWidth={20} />
        <Progress percent={2} placement="inside" strokeWidth={20} />
        <Progress content="成功" percent={80} placement="inside" strokeWidth={20} />
        <br />
        <Progress type="success" content="成功" percent={100} placement="inside" strokeWidth={20} />
        <br />
        <Progress type="warning" content="警示" percent={50} placement="inside" strokeWidth={20} />
        <br />
        <Progress type="error" content="错误" percent={20} placement="inside" strokeWidth={20} />
        <Progress percent={75} strokeWidth={20} />
        <br />
      </div>
    </>
  )
}

```

## provider 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Provider, { DesignSystemAccentColorEnum } from '@hi-ui/provider'
import { LocaleEnum } from '@hi-ui/locale-context'
import Pagination from '@hi-ui/pagination'
import Select from '@hi-ui/select'
import { Row, Col } from '@hi-ui/grid'
import Alert from '@hi-ui/alert'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const [locale, setLocale] = React.useState<LocaleEnum>()
  const [accentColor, setAccentColor] = React.useState<DesignSystemAccentColorEnum>()

  return (
    <>
      <h1>基础用法</h1>
      <div className="provider-basic__wrap">
        <Alert title="在 APP 最外层包裹使用，用于主色、国际化、圆角、边框、特效等主题设置"></Alert>
        <Provider locale={locale} accentColor={accentColor} theme={{}}>
          <Row gutter style={{ marginTop: 20, marginBottom: 20 }}>
            <Col span={6}>
              <Select
                placeholder="语言"
                data={[
                  {
                    id: 'zh-CN',
                    title: '中文',
                  },
                  {
                    id: 'zh-TW',
                    title: '繁体',
                  },
                  {
                    id: 'en-US',
                    title: 'English',
                  },
                ]}
                value={locale}
                onChange={(val) => setLocale(val as LocaleEnum)}
              />
            </Col>
            <Col span={6}>
              <Select
                placeholder="配色"
                data={[
                  {
                    id: 'brandblue',
                    title: '品牌蓝',
                  },
                  {
                    id: 'ultramarine',
                    title: '深蓝',
                  },
                  {
                    id: 'pastelblue',
                    title: '浅蓝',
                  },
                  {
                    id: 'skyblue',
                    title: '天空蓝',
                  },
                  {
                    id: 'orange',
                    title: '活力橙',
                  },
                  {
                    id: 'amber',
                    title: '琥珀',
                  },
                  {
                    id: 'purple',
                    title: '紫罗兰',
                  },
                  {
                    id: 'cyan',
                    title: '橘青',
                  },
                ]}
                value={accentColor}
                onChange={(val) => setAccentColor(val as DesignSystemAccentColorEnum)}
              />
            </Col>
          </Row>
          <Pagination
            total={200}
            pageSize={10}
            showTotal
            showJumper
            pageSizeOptions={[10, 20, 50, 100]}
          />
        </Provider>
      </div>
    </>
  )
}

```

### portal.stories.tsx

```typescript
import React from 'react'
import Provider from '@hi-ui/provider'
import Button from '@hi-ui/button'
import Drawer from '@hi-ui/drawer'
import Modal from '@hi-ui/modal'
import Space from '@hi-ui/space'
import { createMessage } from '@hi-ui/message'
import { createNotification } from '@hi-ui/notification'

/**
 * @title 设置 portal
 * @desc 通过 Provider 设置 portal，可以将 Drawer、Modal 等组件的弹出层渲染在特定的 DOM 节点下
 */
export const Portal = () => {
  const [drawerVisible, setDrawerVisible] = React.useState(false)
  const [modalVisible, setModalVisible] = React.useState(false)
  const [container, setContainer] = React.useState<HTMLElement | null>(null)

  const message = React.useMemo(() => {
    if (!container) return createMessage()
    return createMessage({ container })
  }, [container])

  const notification = React.useMemo(() => {
    if (!container) return createNotification()
    return createNotification({ container })
  }, [container])

  return (
    <>
      <h1>设置 Portal</h1>
      <div className="provider-portal__wrap">
        <Provider portal={{ container }}>
          <Space style={{ marginBottom: 12 }}>
            <Button type="secondary" onClick={() => setDrawerVisible(!drawerVisible)}>
              Drawer
            </Button>
            <Button type="secondary" onClick={() => setModalVisible(!modalVisible)}>
              Modal
            </Button>
            <Button
              type="secondary"
              onClick={() => {
                message.open({
                  title: '欢迎使用 HiUI 组件库',
                  type: 'success',
                })
              }}
            >
              Message
            </Button>
            <Button
              type="secondary"
              onClick={() => {
                notification.open({
                  size: 'sm',
                  title: '数据备份通知',
                  content:
                    '各位同学请注意，将于2019.08.10 00:00:00 -08:00：00 期间进行系统服务器升级维护！',
                })
              }}
            >
              Notification
            </Button>
          </Space>
          {/* 必须设置一个拥有定位的父元素，组件显示在该元素内 */}
          <div
            ref={setContainer}
            className="drawer-container__wrap"
            style={{
              width: '100%',
              minWidth: 660,
              height: 420,
              background: '#f5f7fa',
              boxShadow: '1px 2px 8px #ddd',
              display: 'flex',
              justifyContent: 'center',
              alignItems: 'center',

              // Need add for it
              position: 'relative',
              overflow: 'hidden',
              zIndex: 0,
            }}
          >
            <Drawer
              title="抽屉标题"
              style={{ position: 'absolute' }}
              visible={drawerVisible}
              closeable={false}
              onClose={() => setDrawerVisible(false)}
            >
              我是一段文字，也可以是表单、表格、步骤条等等
            </Drawer>
            <Modal
              title="提示"
              style={{ position: 'absolute' }}
              visible={modalVisible}
              closeable={false}
              onCancel={() => setModalVisible(false)}
            >
              我是挂载指定容器的模态框内容
            </Modal>
          </div>
        </Provider>
      </div>
    </>
  )
}

```

## radio 组件

### auto-width.stories.tsx

```typescript
import React from 'react'
import Radio from '@hi-ui/radio'

/**
 * @title 宽度自适应
 * @desc 仅支持横向按钮组
 */
export const AutoWidth = () => {
  const RadioGroup = Radio.Group

  const [data] = React.useState([
    {
      id: 0,
      title: '手机类',
    },
    {
      id: 1,
      title: '电脑类',
    },
    {
      id: 2,
      title: '生活类',
    },
    {
      id: 3,
      title: '其它',
    },
    {
      id: 4,
      title: '禁用未选',
      disabled: true,
    },
  ])

  return (
    <>
      <h1>AutoWidth</h1>
      <div className="radio-auto-width__wrap">
        <div>
          <RadioGroup
            defaultValue={0}
            type={'button'}
            data={data}
            autoWidth={true}
            onChange={(value) => {
              console.log('onChange', value)
            }}
          />
        </div>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import { Radio } from '@hi-ui/radio'

/**
 * @title 基础用法
 * @desc 展示所有备选项，数量不宜超出10个
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="radio-basic__wrap">
        <Radio onChange={console.log}>Radio</Radio>
      </div>
    </>
  )
}

```

### button.stories.tsx

```typescript
import React from 'react'
import Radio from '@hi-ui/radio'

/**
 * @title 按钮组用法
 * @desc 样式突出，突显在页面的重要级别，选项数5个左右为宜
 */
export const Button = () => {
  const RadioGroup = Radio.Group

  const [data] = React.useState([
    {
      id: 0,
      title: '手机类',
    },
    {
      id: 1,
      title: '电脑类',
    },
    {
      id: 2,
      title: '生活类',
    },
    {
      id: 3,
      title: '其它',
    },
    {
      id: 4,
      title: '禁用未选',
      disabled: true,
    },
  ])

  return (
    <>
      <h1>Button</h1>
      <div className="radio-button__wrap">
        <div>
          <RadioGroup
            defaultValue={0}
            type={'button'}
            data={data}
            onChange={(value) => {
              console.log('onChange', value)
            }}
          />
        </div>
        <h2>vertical</h2>
        <div>
          <RadioGroup
            defaultValue={0}
            placement={'vertical'}
            type={'button'}
            data={data}
            onChange={(value) => {
              console.log('onChange', value)
            }}
          />
        </div>
      </div>
    </>
  )
}

```

### children.stories.tsx

```typescript
import React from 'react'
import Radio from '@hi-ui/radio'
import Grid from '@hi-ui/grid'

/**
 * @title 灵活布局
 * @desc Radio 与 Grid 组件一起使用，可以实现灵活的布局
 */
export const Children = () => {
  const { Row, Col } = Grid
  const RadioGroup = Radio.Group

  const [selectedId, setSelectedId] = React.useState<React.ReactText>('Phone')

  return (
    <>
      <h1>Children</h1>
      <div className="radio-children__wrap">
        <RadioGroup
          value={selectedId}
          style={{ width: '100%' }}
          onChange={(value) => {
            console.log(value)
            setSelectedId(value)
          }}
        >
          <Row>
            <Col span={8}>
              <Radio value="Phone">手机</Radio>
            </Col>
            <Col span={8}>
              <Radio value="Computer">电脑</Radio>
            </Col>
            <Col span={8}>
              <Radio value="Intelligent">智能</Radio>
            </Col>
          </Row>
          <Row>
            <Col span={8}>
              <Radio value="Transfer" onChange={console.log}>
                出行
              </Radio>
            </Col>
            <Col span={8}>
              <Radio value="ecological" onChange={console.log}>
                生态
              </Radio>
            </Col>
          </Row>
        </RadioGroup>
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import Radio from '@hi-ui/radio'
import Button from '@hi-ui/button'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [checked, setChecked] = React.useState(false)

  return (
    <>
      <h1>Controlled</h1>
      <div className="radio-controlled__wrap">
        <Button onClick={() => setChecked((prev) => !prev)}>Toggle</Button>
        <div style={{ marginTop: 10 }}>
          <Radio
            checked={checked}
            onChange={(evt) => {
              console.log('onChange', evt)
              setChecked(evt.target.checked)
            }}
          >
            Radio
          </Radio>
        </div>
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import Radio from '@hi-ui/radio'

/**
 * @title 禁用状态
 */
export const Disabled = () => {
  return (
    <>
      <h1>disabled</h1>
      <div
        className="radio-disabled__wrap"
        style={{ display: 'flex', flexDirection: 'column', gap: 10 }}
      >
        <Radio disabled checked>
          disabled Checked Radio
        </Radio>
        <Radio disabled>Disabled No-Checked Radio</Radio>
      </div>
    </>
  )
}

```

### group.stories.tsx

```typescript
import React from 'react'
import Radio from '@hi-ui/radio'

/**
 * @title 成组
 */
export const Group = () => {
  const RadioGroup = Radio.Group

  const [data] = React.useState([
    {
      id: 0,
      title: '手机类',
    },
    {
      id: 1,
      title: '电脑类',
    },
    {
      id: 2,
      title: '生活类',
    },
    {
      id: 3,
      title: '其它',
    },
    {
      id: 4,
      title: '禁用未选',
      disabled: true,
    },
  ])

  return (
    <>
      <h1>Group</h1>
      <div className="radio-group__wrap">
        <RadioGroup
          defaultValue={0}
          data={data}
          onChange={(value) => {
            console.log('onChange', value)
          }}
        />
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import React from 'react'
import Radio from '@hi-ui/radio'

/**
 * @title 垂直样式
 * @desc 选项的另一种布局形式，视页面空间选用
 */
export const Placement = () => {
  const RadioGroup = Radio.Group

  const [data] = React.useState([
    {
      title: '手机',
      id: 'Phone',
    },
    {
      title: '电脑',
      id: 'Computer',
    },
    {
      title: '智能',
      id: 'Intelli',
    },
    {
      title: '出行',
      id: 'Transfer',
      disabled: true,
    },
  ])
  const [selectedId, setSelectedId] = React.useState<React.ReactText>('Phone')

  return (
    <>
      <h1>垂直样式</h1>
      <div className="checkbox-placement__wrap">
        <RadioGroup
          data={data}
          placement="vertical"
          value={selectedId}
          onChange={(value) => {
            console.log(value)
            setSelectedId(value)
          }}
        />
      </div>
    </>
  )
}

```

## rating 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 基础用法
 * @desc 评定业务指标、信用等级、满意度等
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="rating-basic__wrap">
        <Rating defaultValue={3} />
      </div>
    </>
  )
}

```

### character.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 基础用法
 * @desc 评定业务指标、信用等级、满意度等
 */
export const Character = () => {
  return (
    <>
      <h1>Character</h1>
      <div className="rating-character__wrap">
        <h2>文字字符</h2>
        <Rating defaultValue={3} character="HiUI" />

        <br />
        <h2>图片字符</h2>
        <Rating
          defaultValue={3.5}
          character={
            <img
              src="https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/logo.png"
              style={{ width: 24, height: 24 }}
            />
          }
        />
      </div>
    </>
  )
}

```

### clearable.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 禁止清除
 */
export const Clearable = () => {
  return (
    <>
      <h1>Clearable</h1>
      <div className="rating-clearable__wrap">
        <Rating defaultValue={3} clearable={false} />
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [value, setValue] = React.useState(1)
  return (
    <>
      <h1>Controlled</h1>
      <div className="rating-controlled__wrap">
        <div>当前打分：{value} 分</div>
        <Rating style={{ marginTop: 8 }} value={value} onChange={setValue} />
      </div>
    </>
  )
}

```

### count.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 任意数量
 */
export const Count = () => {
  return (
    <>
      <h1>任意数量</h1>
      <div className="rating-count__wrap">
        <Rating count={10} allowHalf defaultValue={9.5} />
      </div>
    </>
  )
}

```

### custom.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 自定义渲染
 * @desc 使用 renderCharacter()=>ReactNode 自定义渲染
 */
export const Custom = () => {
  const smile1Png =
    'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/rating-emoji-1%402x.png'

  const smile2Png =
    'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/rating-emoji-2%402x.png'

  const smile3Png =
    'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/rating-emoji-3%402x.png'

  const smile4Png =
    'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/rating-emoji-4%402x.png'

  const smile5Png =
    'https://cdn.cnbj1.fds.api.mi-img.com/hiui-template/resources/images/HiUI/rating-emoji-5%402x.png'

  return (
    <>
      <h1>Custom</h1>
      <div className="rating-custom__wrap">
        <Rating
          defaultValue={1}
          characterRender={(value) => {
            const Emojis = [smile1Png, smile2Png, smile3Png, smile4Png, smile5Png]

            return <img src={Emojis[Math.ceil(value) - 1]} style={{ width: 24, height: 24 }} />
          }}
        ></Rating>
      </div>
    </>
  )
}

```

### desc.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 辅助文字
 */
export const Desc = () => {
  return (
    <>
      <h1>Desc</h1>
      <div className="rating-desc__wrap">
        <Rating
          defaultValue={1}
          descRender={(value) => {
            const arr = ['极差', '失望', '一般', '满意', '很满意']
            return <span style={{ color: '#ff5959' }}>{arr[Math.ceil(value) - 1]}</span>
          }}
        ></Rating>
      </div>
    </>
  )
}

```

### emoji.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 使用表情
 * @desc 运用图标直观表达评级结果的优劣
 */
export const Emoji = () => {
  return (
    <>
      <h1>Emoji</h1>
      <div className="rating-emoji__wrap">
        <p>使用表情后将不可自定义数量，不可定义半星</p>
        <Rating defaultValue={5} useEmoji halfPlacement="horizontal"></Rating>
      </div>
    </>
  )
}

```

### half.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 半星
 */
export const Half = () => {
  return (
    <>
      <h1>半星</h1>
      <div className="rating-half__wrap">
        <Rating
          allowHalf
          defaultValue={3.5}
          halfPlacement="horizontal"
          onHover={console.log}
        ></Rating>
        <br />
        <br />
        <Rating allowHalf defaultValue={3.5} halfPlacement="vertical" />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 设置尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>Size</h1>
      <div className="rating-size__wrap">
        <div>
          <Rating defaultValue={3} style={{ fontSize: 14 }} />
        </div>
        <div style={{ marginTop: 10 }}>
          <Rating defaultValue={3} style={{ fontSize: 20 }} />
        </div>
      </div>
    </>
  )
}

```

### status.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 不同状态
 * @desc 展示所有备选项，数量不宜超出10个
 */
export const Status = () => {
  return (
    <>
      <h1>不同状态</h1>
      <div className="rating-status__wrap">
        <h2>禁用</h2>
        <Rating disabled defaultValue={3.5} halfPlacement="vertical" onHover={console.log}></Rating>
        <h2>只读</h2>
        <Rating readOnly defaultValue={4} allowHalf={false} halfPlacement="horizontal"></Rating>
        <br />
        <h2>自动聚焦</h2>
        <Rating
          autoFocus
          defaultValue={3.5}
          halfPlacement="vertical"
          onHover={console.log}
        ></Rating>
      </div>
    </>
  )
}

```

### tooltip.stories.tsx

```typescript
import React from 'react'
import Rating from '@hi-ui/rating'

/**
 * @title 带Tooltip
 */
export const Tooltip = () => {
  return (
    <>
      <h1>带Tooltip</h1>
      <div className="rating-tooltip__wrap">
        <Rating
          defaultValue={3.5}
          tooltips={['极差', '失望', '一般', '满意', '很满意']}
          allowHalf
          halfPlacement="horizontal"
        ></Rating>
      </div>
    </>
  )
}

```

## resize-box 组件

### basic.stories.tsx

```typescript
import React from 'react'
import ResizeBox, { ResizeBoxPane } from '@hi-ui/resize-box'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="resize-box-basic__wrap">
        <ResizeBox style={{ width: 600, height: 400, border: '1px solid #ddd' }}>
          <ResizeBoxPane defaultWidth={300} onResize={console.log}>
            <div
              style={{
                width: '100%',
                overflow: 'auto',
                display: 'flex',
                justifyContent: 'center',
                alignItems: 'center',
              }}
            >
              left content
            </div>
          </ResizeBoxPane>
          <ResizeBoxPane>
            <div
              style={{
                width: '100%',
                overflow: 'auto',
                display: 'flex',
                justifyContent: 'center',
                alignItems: 'center',
              }}
            >
              right content
            </div>
          </ResizeBoxPane>
        </ResizeBox>
      </div>
    </>
  )
}

```

### collapsible.stories.tsx

```typescript
import React from 'react'
import ResizeBox, { ResizeBoxPane } from '@hi-ui/resize-box'

/**
 * @title 设置是否可折叠
 */
export const Collapsible = () => {
  const [collapsed, setCollapsed] = React.useState<boolean>(false)

  return (
    <>
      <h1>Collapsible</h1>
      <div className="resize-box-collapsible__wrap">
        <ResizeBox style={{ width: 600, height: 400, border: '1px solid #ddd' }}>
          <ResizeBoxPane
            collapsible
            collapsed={collapsed}
            onCollapse={setCollapsed}
            defaultWidth={200}
            onResize={console.log}
          >
            <div
              style={{
                width: '100%',
                overflow: 'auto',
                display: 'flex',
                justifyContent: 'center',
                alignItems: 'center',
              }}
            >
              left content
            </div>
          </ResizeBoxPane>
          <ResizeBoxPane>
            <div
              style={{
                width: '100%',
                overflow: 'auto',
                display: 'flex',
                justifyContent: 'center',
                alignItems: 'center',
              }}
            >
              right content
            </div>
          </ResizeBoxPane>
        </ResizeBox>
      </div>
    </>
  )
}

```

### min-width.stories.tsx

```typescript
import React from 'react'
import ResizeBox, { ResizeBoxPane } from '@hi-ui/resize-box'

/**
 * @title 设置 pane 最小宽度
 */
export const MinWidth = () => {
  return (
    <>
      <h1>MinWidth</h1>
      <div className="resize-box-min-width__wrap">
        <ResizeBox style={{ width: 600, height: 400, border: '1px solid #ddd' }}>
          <ResizeBoxPane defaultWidth={300} minWidth={100}>
            <div
              style={{
                width: '100%',
                overflow: 'auto',
                display: 'flex',
                justifyContent: 'center',
                alignItems: 'center',
              }}
            >
              left content
            </div>
          </ResizeBoxPane>
          <ResizeBoxPane>
            <div
              style={{
                width: '100%',
                overflow: 'auto',
                display: 'flex',
                justifyContent: 'center',
                alignItems: 'center',
              }}
            >
              right content
            </div>
          </ResizeBoxPane>
        </ResizeBox>
      </div>
    </>
  )
}

```

## result 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Result from '@hi-ui/result'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>基础功能</h1>
      <div className="result-basic__wrap">
        <Result title="我是标题" content="我是结果信息的说明文案"></Result>
      </div>
    </>
  )
}

```

### complete.stories.tsx

```typescript
import React from 'react'
import Result, { RESULT_IMAGE_NET_ERROR } from '@hi-ui/result'
import Button from '@hi-ui/button'

/**
 * @title 带按钮
 * @desc 通过 `children` 配置补充的操作或建议提示
 */
export const Complete = () => {
  return (
    <>
      <h1>完整功能</h1>
      <div className="result-basic__wrap">
        <Result
          image={RESULT_IMAGE_NET_ERROR}
          title="网络连接失败"
          content="这是对网络连接失败的说明文案"
        >
          <div>
            {[
              <Button key="refresh">刷新</Button>,
              <Button type="primary" key="back">
                返回
              </Button>,
            ]}
            <div
              style={{
                whiteSpace: 'pre-wrap',
                marginTop: '30px',
                padding: '30px',
                background: '#f2f4f7',
                boxSizing: 'border-box',
                fontSize: '14px',
                color: '#1F2733',
                textAlign: 'left',
              }}
            >
              <div>请尝试：</div>
              <div>1. 检查您的电脑网络是否正常</div>
              <div>2. 关闭 Wi-Fi 重新链接</div>
            </div>
          </div>
        </Result>
      </div>
    </>
  )
}

```

### custom.stories.tsx

```typescript
import React from 'react'
import Result, {
  ResultImageClientError,
  ResultImageNetError,
  ResultImageForbidden,
  ResultImageNotFound,
  ResultImageServerError,
} from '@hi-ui/result'
import Button from '@hi-ui/button'

/**
 * @title 自定义指示器
 * @desc 通过 `image` 完全自定义指示器，可以是 img 标签
 */
export const Custom = () => {
  return (
    <>
      <h1>自定义指示器</h1>
      <div className="result-basic__wrap">
        <Result
          image={<ResultImageClientError />}
          title="页面发送错误"
          content="这是对页面错误的说明文案"
          children={[
            <Button key="refresh">刷新</Button>,
            <Button type="primary" key="back">
              返回
            </Button>,
          ]}
        />
        <Result
          image={<ResultImageNetError />}
          title="网络连接失败"
          content="这是对网络连接失败的说明文案"
          children={[
            <Button key="refresh">刷新</Button>,
            <Button type="primary" key="back">
              返回
            </Button>,
          ]}
        />
        <Result
          image={<ResultImageForbidden />}
          title="暂无权限"
          content="这是对暂无权限的说明文案"
          children={[
            <Button key="refresh">立即申请</Button>,
            <Button type="primary" key="back">
              返回
            </Button>,
          ]}
        />
        <Result
          image={<ResultImageNotFound />}
          title="404"
          content="抱歉，请求资源不存在！"
          children={<Button type="primary">返回首页</Button>}
        />
        <Result
          image={<ResultImageServerError />}
          title="500"
          content="抱歉，服务器开小差了！"
          children={<Button type="primary">刷新</Button>}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Result from '@hi-ui/result'

/**
 * @title 不同尺寸
 * @desc 设置指示器的尺寸大小
 */
export const Size = () => {
  return (
    <>
      <h1>不同尺寸</h1>
      <div className="result-Size__wrap">
        <Result
          imageSize="sm"
          type="success"
          title="这是一条成功信息"
          content="这是对成功信息的说明文案"
        />
        <Result
          imageSize="md"
          type="success"
          title="这是一条成功信息"
          content="这是对成功信息的说明文案"
        />
        <Result
          imageSize="lg"
          type="success"
          title="这是一条成功信息"
          content="这是对成功信息的说明文案"
        />
      </div>
    </>
  )
}

```

### type.stories.tsx

```typescript
import React from 'react'
import Result from '@hi-ui/result'

/**
 * @title 不同类型
 * @desc 默认有通知、成功、错误、警告四种类型
 */
export const Type = () => {
  return (
    <>
      <h1>不同类型</h1>
      <div className="result-type__wrap">
        <Result type="info" title="这是一条常规信息" content="这是对常规信息的说明文案" />
        <Result type="success" title="这是一条成功信息" content="这是对成功信息的说明文案" />
        <Result type="warning" title="这是一条警示信息" content="这是对警示信息的说明文案" />
        <Result type="error" title="这是一条错误信息" content="这是对错误信息的说明文案" />
      </div>
    </>
  )
}

```

## scrollbar 组件

### axes.stories.tsx

```typescript
import React, { useMemo } from 'react'
import Scrollbar from '@hi-ui/scrollbar'

/**
 * @title 使用坐标轴
 * @desc 默认 `x`、`y` 都可滚动
 */
export const Axes = () => {
  const scrollContent = useMemo(() => {
    return (
      <div style={{ height: 640, width: '200%' }}>
        <div style={{ height: 160, background: 'linear-gradient(90deg,#03A9F433,#03A9F4cc)' }} />
        <div style={{ height: 160, background: 'linear-gradient(90deg,#00968833,#009688cc)' }} />
        <div style={{ height: 160, background: 'linear-gradient(90deg,#FF572233,#FF5722cc)' }} />
        <div style={{ height: 160, background: 'linear-gradient(90deg,#E91E6333,#E91E63cc)' }} />
      </div>
    )
  }, [])

  return (
    <>
      <h1>使用坐标轴</h1>
      <h2>both(default)</h2>
      <div className="scrollbar-axes__wrap" style={{ height: 320, marginBottom: 64 }}>
        <Scrollbar>{scrollContent}</Scrollbar>
      </div>
      <h2>x</h2>
      <div className="scrollbar-axes__wrap" style={{ height: 320, marginBottom: 64 }}>
        <Scrollbar axes={'x'}>{scrollContent}</Scrollbar>
      </div>
      <h2>y</h2>
      <div className="scrollbar-axes__wrap" style={{ height: 320, marginBottom: 64 }}>
        <Scrollbar axes={'y'}>{scrollContent}</Scrollbar>
      </div>
      <h2>none</h2>
      <div className="scrollbar-axes__wrap" style={{ height: 320, marginBottom: 64 }}>
        <Scrollbar axes={'none'}>{scrollContent}</Scrollbar>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Scrollbar from '@hi-ui/scrollbar'

/**
 * @title 基础用法
 * @desc 默认鼠标不再容器内隐藏，x、y轴都展示
 */
export const Basic = () => {
  return (
    <>
      <h1>默认</h1>
      <div className="scrollbar-basic__wrap" style={{ height: 320 }}>
        <Scrollbar>
          <div style={{ height: 640, width: '100%' }}>
            <div style={{ height: 160, background: '#03A9F433' }} />
            <div style={{ height: 160, background: '#00968833' }} />
            <div style={{ height: 160, background: '#FF572233' }} />
            <div style={{ height: 160, background: '#E91E6333' }} />
          </div>
        </Scrollbar>
      </div>
    </>
  )
}

```

### config.stories.tsx

```typescript
import React, { useMemo } from 'react'
import Scrollbar from '@hi-ui/scrollbar'

/**
 * @title 展示配置
 * @desc 可配置轴展示行为
 */
export const Config = () => {
  const scrollContent = useMemo(() => {
    return (
      <div style={{ height: 640, width: '100%' }}>
        <div style={{ height: 160, background: '#03A9F433' }} />
        <div style={{ height: 160, background: '#00968833' }} />
        <div style={{ height: 160, background: '#FF572233' }} />
        <div style={{ height: 160, background: '#E91E6333' }} />
      </div>
    )
  }, [])

  return (
    <>
      <h1>展示配置</h1>
      <h2>keepVisible</h2>
      <div className="scrollbar-config__wrap" style={{ height: 320, marginBottom: 64 }}>
        <Scrollbar keepVisible>{scrollContent}</Scrollbar>
      </div>
      <h2>onlyScrollVisible</h2>
      <div className="scrollbar-config__wrap" style={{ height: 320, marginBottom: 64 }}>
        <Scrollbar onlyScrollVisible>{scrollContent}</Scrollbar>
      </div>
    </>
  )
}

```

### event.stories.tsx

```typescript
import React, { useMemo } from 'react'
import Scrollbar from '@hi-ui/scrollbar'

/**
 * @title 滚动事件
 * @desc 可以使用内置提供的一系列自定义滚动事件
 */
export const Event = () => {
  const scrollContent = useMemo(() => {
    return (
      <div style={{ height: 640, width: '200%' }}>
        <div style={{ height: 160, background: 'linear-gradient(90deg,#03A9F433,#03A9F4cc)' }} />
        <div style={{ height: 160, background: 'linear-gradient(90deg,#00968833,#009688cc)' }} />
        <div style={{ height: 160, background: 'linear-gradient(90deg,#FF572233,#FF5722cc)' }} />
        <div style={{ height: 160, background: 'linear-gradient(90deg,#E91E6333,#E91E63cc)' }} />
      </div>
    )
  }, [])

  return (
    <>
      <h1>滚动事件</h1>
      <h2>x、y滚动事件</h2>
      <div className="scrollbar-basic__wrap" style={{ height: 320, marginBottom: 64 }}>
        <Scrollbar
          onScrollX={() => console.log('scroll x')}
          onScrollY={() => console.log('scroll y')}
        >
          {scrollContent}
        </Scrollbar>
      </div>
      <h2>特定滚动方向事件</h2>
      <div className="scrollbar-basic__wrap" style={{ height: 320, marginBottom: 64 }}>
        <Scrollbar
          onScrollUp={() => console.log('scroll up')}
          onScrollDown={() => console.log('scroll down')}
          onScrollLeft={() => console.log('scroll left')}
          onScrollRight={() => console.log('scroll right')}
        >
          {scrollContent}
        </Scrollbar>
      </div>
      <h2>滚动到边界事件</h2>
      <div className="scrollbar-basic__wrap" style={{ height: 320, marginBottom: 64 }}>
        <Scrollbar
          onXReachStart={() => console.log('reach x start')}
          onXReachEnd={() => console.log('reach x end')}
          onYReachStart={() => console.log('reach y start')}
          onYReachEnd={() => console.log('reach y end')}
        >
          {scrollContent}
        </Scrollbar>
      </div>
    </>
  )
}

```

### fixed.stories.tsx

```typescript
import React, { useRef, useEffect } from 'react'
import Scrollbar from '@hi-ui/scrollbar'

/**
 * @title 滚动条固定到屏幕底部
 * @desc 默认不开启
 */
export const Fixed = () => {
  const innerRef = useRef<any>()
  useEffect(() => {
    document.addEventListener('scroll', () => {
      innerRef.current?.updata()
    })
  }, [])
  return (
    <div
      id="outer"
      style={{
        height: '150vh',
        display: 'flex',
        flexDirection: 'column',
        justifyContent: 'flex-end',
      }}
    >
      <Scrollbar
        innerRef={innerRef}
        keepVisible
        style={{
          height: 400,
          width: 600,
        }}
        settings={{ isBottomToScreenBottom: true, heightFromBottom: 20 }}
      >
        <div style={{ height: 640, width: '200%' }}>
          <div
            style={{
              height: 160,
              background: 'linear-gradient(90deg,#03A9F433,#03A9F4cc)',
            }}
          />
          <div
            style={{
              height: 160,
              background: 'linear-gradient(90deg,#00968833,#009688cc)',
            }}
          />
          <div
            style={{
              height: 160,
              background: 'linear-gradient(90deg,#FF572233,#FF5722cc)',
            }}
          />
          <div
            style={{
              height: 160,
              background: 'linear-gradient(90deg,#E91E6333,#E91E63cc)',
            }}
          />
        </div>
      </Scrollbar>
    </div>
  )
}

```

### sticky.stories.tsx

```typescript
import React, { useRef, useEffect } from 'react'
import Scrollbar, { ScrollbarHelpers } from '@hi-ui/scrollbar'

/**
 * @title 滚动条吸底
 * @desc 默认不开启，开启后默认在 Scrollbar 组件内部滚动有效，如需外部使用，需要手动调用 update 方法
 */
export const Fixed = () => {
  const innerRef = useRef<ScrollbarHelpers>(null)
  const update = () => innerRef.current?.update?.()

  // 此处演示在外部使用该效果
  useEffect(() => {
    document.addEventListener('scroll', update)

    return () => {
      document.removeEventListener('scroll', update)
    }
  }, [])

  return (
    <>
      <h1>滚动条吸底</h1>
      <div className="scrollbar-sticky__wrap">
        <Scrollbar
          innerRef={innerRef}
          keepVisible
          style={{
            height: 400,
          }}
          settings={{ scrollbarXStickToBottom: true, scrollbarXStickToBottomGap: 20 }}
        >
          <div style={{ height: 640, width: '200%' }}>
            <div
              style={{
                height: 160,
                background: 'linear-gradient(90deg,#03A9F433,#03A9F4cc)',
              }}
            />
            <div
              style={{
                height: 160,
                background: 'linear-gradient(90deg,#00968833,#009688cc)',
              }}
            />
            <div
              style={{
                height: 160,
                background: 'linear-gradient(90deg,#FF572233,#FF5722cc)',
              }}
            />
            <div
              style={{
                height: 160,
                background: 'linear-gradient(90deg,#E91E6333,#E91E63cc)',
              }}
            />
          </div>
        </Scrollbar>
      </div>
    </>
  )
}

```

## search 组件

### addon.stories.tsx

```typescript
import React from 'react'
import Search from '@hi-ui/search'
import { SearchOutlined } from '@hi-ui/icons'

/**
 * @title 自定义按钮
 */
export const Addon = () => {
  const [data] = React.useState([
    {
      id: 'miphone',
      title: '手机',
      children: [
        {
          id: 1,
          title: '小米9 Pro',
        },
        {
          id: 2,
          title: '小米9 探索版',
        },
        {
          id: 3,
          title: '小米9 CC 美图定制版',
        },
      ],
    },
    {
      id: 'live',
      title: '智能生活',
      children: [
        {
          id: 4,
          title: '小米 手环',
        },
        {
          id: 5,
          title: '小米 净水器',
        },
        {
          id: 6,
          title: '小米 小爱音响',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Addon</h1>
      <div className="search-addon__wrap">
        <Search
          style={{ width: 260 }}
          placeholder="搜索关键字"
          prefix={<SearchOutlined />}
          append={null}
          data={data}
        />
      </div>
    </>
  )
}

```

### appearance.stories.tsx

```typescript
import React from 'react'
import Search from '@hi-ui/search'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性两种
 */
export const Appearance = () => {
  const [data] = React.useState([
    {
      id: 'miphone',
      title: '手机',
      children: [
        {
          id: 1,
          title: '小米9 Pro',
        },
        {
          id: 2,
          title: '小米9 探索版',
        },
        {
          id: 3,
          title: '小米9 CC 美图定制版',
        },
      ],
    },
    {
      id: 'live',
      title: '智能生活',
      children: [
        {
          id: 4,
          title: '小米 手环',
        },
        {
          id: 5,
          title: '小米 净水器',
        },
        {
          id: 6,
          title: '小米 小爱音响',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Appearance</h1>
      <div className="search-appearance__wrap">
        <div>
          <h2>线性</h2>
          <Search style={{ width: 260 }} placeholder="搜索关键字" data={data} appearance="line" />
        </div>
        <div>
          <h2>面性</h2>
          <Search style={{ width: 260 }} placeholder="搜索关键字" data={data} appearance="filled" />
        </div>
      </div>
    </>
  )
}

```

### async.stories.tsx

```typescript
import React from 'react'
import Search from '@hi-ui/search'

/**
 * @title 异步搜索
 */
export const Async = () => {
  const [loading, setLoading] = React.useState(false)
  const [data, setData] = React.useState([])

  return (
    <>
      <h1>Async</h1>
      <div className="search-async__wrap">
        <Search
          style={{ width: 260 }}
          placeholder="搜索关键字"
          loading={loading}
          data={data}
          onSearch={(keyword) => {
            console.log('onSearch', keyword)
          }}
          onChange={(value) => {
            if (!value) {
              // 清空操作
              setData([])
              return
            }

            // 模拟异步请求数据
            setLoading(true)
            setTimeout(() => {
              const mockDataItem = (str: string, value: number) => ({
                id: str.repeat(value),
                title: str.repeat(value),
              })

              setData([mockDataItem(value, 1), mockDataItem(value, 2), mockDataItem(value, 3)])
              setLoading(false)
            }, 1000)
          }}
        />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Search from '@hi-ui/search'

/**
 * @title 基础用法
 * @desc 按搜索关键字直接请求结果
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="search-basic__wrap">
        <Search
          style={{ width: 260 }}
          placeholder="搜索关键字"
          onSearch={(keyword) => {
            console.log('onSearch', keyword)
          }}
        />
      </div>
    </>
  )
}

```

### classify.stories.tsx

```typescript
import React from 'react'
import Search from '@hi-ui/search'
import Select from '@hi-ui/select'

/**
 * @title 分类检索
 * @desc 按不同的类别划分搜索范围；可减少搜索成本
 */
export const Classify = () => {
  return (
    <>
      <h1>分类检索</h1>
      <div className="search-classify__wrap">
        <Search
          style={{ width: 360 }}
          placeholder="搜索关键字"
          prepend={
            <Select
              clearable={false}
              style={{ width: 90 }}
              onChange={(selectedIds, changedItem) => {
                console.log(selectedIds, changedItem)
              }}
              data={[
                { title: '订单号', id: '1' },
                { title: '用户名', id: '2' },
              ]}
              defaultValue="1"
            />
          }
          onSearch={(title) => {
            console.log('Input Value', title)
          }}
        />
      </div>
    </>
  )
}

```

### data.stories.tsx

```typescript
import React from 'react'
import Search from '@hi-ui/search'

/**
 * @title 关键词联想数据
 * @desc 输入搜索关键词时，可以自动联想匹配的关键字，提高检索效率
 */
export const Data = () => {
  return (
    <>
      <h1>带关联数据</h1>
      <div className="search-basic__wrap">
        <div>
          <h2>普通数据</h2>
          <Search
            style={{ width: 260 }}
            placeholder="搜索关键字"
            data={[
              {
                id: 'miphone',
                title: '手机',
              },
              {
                id: 'live',
                title: '智能生活',
              },
            ]}
            onSearch={(keyword, item) => {
              console.log('Input Value', keyword, item)
            }}
          />
        </div>
        <div>
          <h2>分组</h2>
          <Search
            style={{ width: 260 }}
            placeholder="搜索关键字"
            data={[
              {
                id: 'miphone',
                title: '手机',
                children: [
                  {
                    id: 1,
                    title: '小米9 Pro',
                  },
                  {
                    id: 2,
                    title: '小米9 探索版',
                  },
                  {
                    id: 3,
                    title: '小米9 CC 美图定制版',
                  },
                ],
              },
              {
                id: 'live',
                title: '智能生活',
                children: [
                  {
                    id: 4,
                    title: '小米 手环',
                  },
                  {
                    id: 5,
                    title: '小米 净水器',
                  },
                  {
                    id: 6,
                    title: '小米 小爱音响',
                  },
                ],
              },
            ]}
            // onSearch={(keyword) => {
            //   console.log('Input Value', keyword)
            //   keyword && alert('Input Value: ' + keyword)
            // }}
          />
        </div>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Search from '@hi-ui/search'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>Size</h1>
      <div className="search-size__wrap">
        <Search style={{ width: 260 }} placeholder="搜索关键字" size="sm" />
        <br />
        <br />
        <Search style={{ width: 260 }} placeholder="搜索关键字" size="md" />
        <br />
        <br />
        <Search style={{ width: 260 }} placeholder="搜索关键字" size="lg" />
      </div>
    </>
  )
}

```

## select 组件

### addon.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'
import { AppStoreOutlined, InfoCircleOutlined } from '@hi-ui/icons'

/**
 * @title 前后内置元素
 * @desc 将选择框与内置的其他元素组合使用
 */
export const Addon = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    {
      title: '生活周边超长文案展示超长文案展示',
      id: '5',
    },
    { title: '办公', id: '6' },
    { title: '生活周边7', id: '7' },
    { title: '办公8', id: '8' },
  ])

  return (
    <>
      <h1>Addon</h1>
      <div className="select-addon__wrap">
        <Select
          style={{ width: 240 }}
          // clearable={false}
          data={data}
          prefix={<AppStoreOutlined style={{ color: '#333' }} />}
          suffix={<InfoCircleOutlined style={{ color: '#333' }} />}
        />
      </div>
    </>
  )
}

```

### appearance.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性、无UI三种
 */
export const Appearance = () => {
  const [value, setValue] = React.useState<React.ReactText>('0')
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Appearance</h1>
      <div className="tree-select-appearance__wrap">
        <div>
          <h2>filled</h2>
          <Select
            style={{ width: 240 }}
            data={data}
            value={value}
            clearable
            appearance="filled"
            onChange={(value, targetItem) => {
              console.log('Select onChange: ', value, targetItem)
              setValue(value)
            }}
          />
        </div>

        <div>
          <h2>outline</h2>
          <Select
            style={{ width: 240 }}
            data={data}
            value={value}
            clearable
            appearance="line"
            onChange={(value, targetItem) => {
              console.log('Select onChange: ', value, targetItem)
              setValue(value)
            }}
          />
        </div>

        <div>
          <h2>unset</h2>
          <Select
            data={data}
            value={value}
            clearable
            appearance="unset"
            optionWidth={260}
            onChange={(value, targetItem) => {
              console.log('Select onChange: ', value, targetItem)
              setValue(value)
            }}
          />
        </div>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 基础用法
 * @desc 展示从多个收起的备选项中选出的一个选项
 */
export const Basic = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    {
      title: '生活周边超长文案展示超长文案展示',
      id: '5',
    },
    { title: '办公', id: '6' },
    { title: '生活周边7', id: '7' },
    { title: '办公8', id: '8' },
  ])

  return (
    <>
      <h1>Basic</h1>
      <div className="select-basic__wrap">
        <Select style={{ width: 240 }} clearable={false} data={data} />
      </div>
    </>
  )
}

```

### clearable.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 清空选中项
 */
export const Clearable = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Clearable</h1>
      <div className="select-clearable__wrap">
        <Select style={{ width: 240 }} clearable data={data} onChange={console.log} />
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [value, setValue] = React.useState<React.ReactText>('3')
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Controlled</h1>
      <div className="select-controlled__wrap">
        <Select
          style={{ width: 240 }}
          clearable={false}
          data={data}
          value={value}
          onChange={(selectedId) => {
            setValue(selectedId)
          }}
        />
      </div>
    </>
  )
}

```

### custom-render.stories.tsx

```typescript
import React from 'react'
import Input from '@hi-ui/input'
import Select from '@hi-ui/select'

/**
 * @title 自定义触发器
 */
export const CustomRender = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    {
      title: '生活周边超长文案展示超长文案展示',
      id: '5',
    },
    { title: '办公', id: '6' },
    { title: '生活周边7', id: '7' },
    { title: '办公8', id: '8' },
  ])

  return (
    <>
      <h1>CustomRender</h1>
      <div className="select-custom-render__wrap">
        <Select
          style={{ width: 240 }}
          clearable={false}
          data={data}
          customRender={(data) => {
            return <Input value={!data ? '' : data.title + ''} readOnly placeholder="请选择" />
          }}
        />
      </div>
    </>
  )
}

```

### data-source.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 异步加载数据
 * @desc 备选项数量较大时，通过搜索选项关键词调取存储于服务端数据备选项
 */
export const DataSource = () => {
  const [data] = React.useState([
    {
      id: 'up-1',
      title: 'up',
    },
    {
      id: '0',
      title: '0',
    },
    {
      id: '1',
      title: '1',
    },
    {
      id: '2',
      title: '2',
    },
  ])

  return (
    <>
      <h1>DataSource</h1>
      <div className="cascader-DataSource__wrap">
        <Select
          style={{ width: 240 }}
          // placeholder="请选择品类"
          // searchPlaceholder="请输入搜索内容"
          data={data}
          onChange={console.log}
          // searchOnInit
          dataSource={(keyword) => {
            console.log('DataSource', keyword)
            const url =
              'https://www.fastmock.site/mock/eef9b373d82560f30585521549c4b6cb/hiui/api/list?keyword=' +
              keyword
            return fetch(url)
              .then((response) => {
                return response.json()
              })
              .then(function (res) {
                return res.list
              })
          }}
        />
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 禁用状态
 * @desc 暂不可操作的状态
 */
export const Disabled = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: true },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: true },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Disabled</h1>
      <div className="select-disabled__wrap">
        <h2>整体禁用</h2>
        <Select style={{ width: 240 }} disabled data={data} defaultValue="2" />

        <h2>整体禁用</h2>
        <Select style={{ width: 240 }} data={data} defaultValue="2" />
      </div>
    </>
  )
}

```

### display-render.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 自定义回显展示
 */
export const DisplayRender = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>DisplayRender</h1>
      <div className="select-display-render__wrap">
        <Select
          style={{ width: 240 }}
          clearable={false}
          data={data}
          displayRender={(item) => {
            console.log(item)
            return (
              <span style={{ float: 'left' }}>
                {item.title}
                <span style={{ float: 'right', color: '#999', fontSize: 14 }}>({item.id})</span>
              </span>
            )
          }}
        />
      </div>
    </>
  )
}

```

### empty-content.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 自定义空内容
 */
export const EmptyContent = () => {
  const [data] = React.useState([])

  return (
    <>
      <h1>EmptyContent</h1>
      <div className="select-empty-content__wrap">
        <Select style={{ width: 240 }} data={data} emptyContent="暂无选项" />
      </div>
    </>
  )
}

```

### filter-options.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 自定义筛选
 * @desc 通过 filterOption 可自定义搜索条件的算法
 */
export const FilterOptions = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  // 注意 filterOption 是影响搜索渲染的，是完全受控的，useCallback 包裹可以减少无效的重渲染，提升性能
  const filterOptionMemo = React.useCallback((keyword: string, item: any) => {
    return item.id >= parseInt(keyword)
  }, [])

  return (
    <>
      <h1>FilterOptions</h1>
      <div className="select-filter-options__wrap">
        <Select
          style={{ width: 240 }}
          clearable={false}
          data={data}
          searchPlaceholder="搜索：id >= keyword"
          filterOption={filterOptionMemo}
        />
      </div>
    </>
  )
}

```

### footer.stories.tsx

```typescript
import Input from '@hi-ui/input'
import React from 'react'
import Select from '@hi-ui/select'
import { PlusOutlined } from '@hi-ui/icons'

/**
 * @title 吸底内容条
 */
export const Footer = () => {
  const [data, setData] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  const [inputValue, setInputValue] = React.useState('')

  return (
    <>
      <h1>Footer</h1>
      <div className="select-footer__wrap">
        <Select
          style={{ width: 240 }}
          clearable={false}
          data={data}
          renderExtraFooter={() => {
            return (
              <Input
                placeholder="添加选项"
                value={inputValue}
                onChange={(evt) => {
                  setInputValue(evt.target.value)
                }}
                suffix={
                  <PlusOutlined
                    style={{ cursor: 'pointer' }}
                    onClick={() => {
                      setData((prev) => {
                        return [...prev, { id: Math.random() + inputValue, title: inputValue }]
                      })
                      setInputValue('')
                    }}
                  />
                }
              />
            )
          }}
        />
      </div>
    </>
  )
}

```

### group.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 类型分组
 */
export const Group = () => {
  const [value, setValue] = React.useState<React.ReactText>('3')

  const [data] = React.useState([
    {
      groupId: 'redmi',
      groupTitle: '红米手机',
      children: [
        { title: '红米 5A', id: '3' },
        { title: '红米 6A', id: '2' },
        { title: '红米 note', id: '4' },
        { title: '红米 note8', id: '5' },
      ],
    },
    {
      groupId: 'mi',
      groupTitle: '小米电视',
      children: [
        { title: '小米电视4A 60寸', id: '10' },
        { title: '小米电视E55A', id: '11' },
        { title: '小米电视E65A', id: '12' },
        { title: '小米电视4S', id: '13' },
        { title: '小米电视4C', id: '14' },
      ],
    },
  ])

  return (
    <>
      <h1>Group</h1>
      <div className="select-Group__wrap">
        <Select
          style={{ width: 240 }}
          data={data}
          placeholder="请选择"
          searchable
          value={value}
          onChange={(selectedId) => {
            setValue(selectedId)
          }}
        />
      </div>
    </>
  )
}

```

### pinyin.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

import { match } from 'pinyin-pro'

/**
 * @title 拼音搜索
 * @desc 通过输入拼音搜索关键字
 */
export const Pinyin = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  // 注意 filterOption 是影响搜索渲染的，是完全受控的，useCallback 包裹可以减少无效的重渲染，提升性能
  const filterOptionMemo = React.useCallback((keyword: string, item: any) => {
    return !!match(item.title as string, keyword)
  }, [])

  return (
    <>
      <h1>Pinyin</h1>
      <div className="select-pinyin__wrap">
        <Select
          style={{ width: 240 }}
          clearable={false}
          data={data}
          filterOption={filterOptionMemo}
        />
      </div>
    </>
  )
}

```

### search-controlled.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 搜索关键字受控
 * @desc searchable 为 true 时生效
 */
export const SearchControlled = () => {
  const [keyword, setKeyword] = React.useState('1')

  const [data] = React.useState([
    {
      id: 'up-1',
      title: 'up',
    },
    {
      id: '0',
      title: '0',
    },
    {
      id: '1',
      title: '1',
    },
    {
      id: '2',
      title: '2',
    },
    {
      id: '11',
      title: '11',
    },
    {
      id: '12',
      title: '12',
    },
  ])

  return (
    <>
      <h1>Search Controlled</h1>
      <div className="select-search-controlled__wrap">
        <Select
          style={{ width: 240 }}
          searchable
          keyword={keyword}
          onSearch={(value) => {
            setKeyword(value)
            console.log('onSearch', value)
          }}
          onClear={() => {
            setKeyword('')
          }}
          placeholder="请选择品类"
          searchPlaceholder="请输入搜索内容"
          data={data}
        />
      </div>
    </>
  )
}

```

### search.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 带搜索
 */
export const Search = () => {
  const [data] = React.useState([
    {
      id: 'up-1',
      title: 'up',
    },
    {
      id: '0',
      title: '0',
    },
    {
      id: '1',
      title: '1',
    },
    {
      id: '2',
      title: '2',
    },
  ])
  return (
    <>
      <h1>Search</h1>
      <div className="select-search__wrap">
        <Select
          style={{ width: 240 }}
          searchable
          placeholder="请选择品类"
          searchPlaceholder="请输入搜索内容"
          data={data}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    {
      title: '生活周边超长文案展示超长文案展示',
      id: '5',
    },
    { title: '办公', id: '6' },
    { title: '生活周边7', id: '7' },
    { title: '办公8', id: '8' },
  ])

  return (
    <>
      <h1>Size</h1>
      <div className="select-size__wrap">
        <h2>sm</h2>
        <Select style={{ width: 240 }} size="sm" clearable={false} data={data} />
        <h2>md</h2>
        <Select style={{ width: 240 }} size="md" clearable={false} data={data} />
        <h2>lg</h2>
        <Select style={{ width: 240 }} size="lg" clearable={false} data={data} />
      </div>
    </>
  )
}

```

### tip.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'
import Tooltip from '@hi-ui/tooltip'

/**
 * @title 带Tooltip提示
 */
export const Tip = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边超级长文案展示生活周边超级长文案展示', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Tip</h1>
      <div className="select-Tip__wrap">
        <Select
          style={{ width: 240 }}
          clearable={false}
          data={data}
          render={(item) => {
            console.log(item)
            return (
              <Tooltip title={item.title} placement="right">
                <span
                  style={{
                    width: '100%',
                    display: 'inline-block',
                    overflow: 'hidden',
                    textOverflow: 'ellipsis',
                    whiteSpace: 'nowrap',
                    verticalAlign: 'middle',
                  }}
                >
                  {item.title}
                </span>
              </Tooltip>
            )
          }}
        />
      </div>
    </>
  )
}

```

### title-render.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 自定义选项展示
 * @desc 可自定义选项的信息结构或样式
 */
export const TitleRender = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>TitleRender</h1>
      <div className="select-TitleRender__wrap">
        <Select
          style={{ width: 240 }}
          clearable={false}
          data={data}
          render={(item) => {
            console.log(item)
            return (
              <React.Fragment>
                <span style={{ float: 'left' }}>{item.title}</span>
                <span style={{ float: 'right', color: '#999', fontSize: 14 }}>{item.id}</span>
              </React.Fragment>
            )
          }}
        />
      </div>
    </>
  )
}

```

### uncontrolled.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 非受控
 */
export const Uncontrolled = () => {
  const [data] = React.useState([
    { title: '电视', id: '3', disabled: false },
    { title: '手机', id: '2' },
    { title: '笔记本', id: '4', disabled: false },
    { title: '生活周边', id: '5' },
    { title: '办公', id: '6' },
  ])

  return (
    <>
      <h1>Uncontrolled</h1>
      <div className="select-uncontrolled__wrap">
        <Select
          style={{ width: 240 }}
          data={data}
          defaultValue={'3'}
          onChange={(selectedId) => {
            console.log('onChange', selectedId)
          }}
        />
      </div>
    </>
  )
}

```

### virtual-list.stories.tsx

```typescript
import React from 'react'
import Select from '@hi-ui/select'

/**
 * @title 大数据
 */
export const VirtualList = () => {
  const [data] = React.useState(() => {
    const defaultData = []
    for (let i = 0; i < 5000; i++) {
      defaultData.push({
        id: `id${i}`,
        title: `title${i}`,
        disabled: i === 8,
      })
    }
    return defaultData
  })

  return (
    <>
      <h1>VirtualList</h1>
      <div className="select-display-render__wrap">
        <Select style={{ width: 240 }} clearable={false} data={data} height={260} />
      </div>
    </>
  )
}

```

## slider 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Slider from '@hi-ui/slider'

/**
 * @title 基础用法
 * @desc 滑动输入连续或离散数据的单点值或范围值
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="slider-basic__wrap">
        <Slider
          style={{ width: 300 }}
          onChange={(value) => {
            console.log(value)
          }}
        ></Slider>
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import Slider from '@hi-ui/slider'
import { Counter } from '@hi-ui/counter'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [value, setValue] = React.useState(0)
  return (
    <>
      <h1>Controlled</h1>
      <div className="slider-controlled__wrap">
        <Slider value={value} onChange={setValue} style={{ width: 300 }} />
        <Counter
          style={{ marginTop: 16 }}
          value={value}
          onChange={setValue}
          step={10}
          min={0}
          max={100}
        />
      </div>
    </>
  )
}

```

### custom-color.stories.tsx

```typescript
import React from 'react'
import Slider from '@hi-ui/slider'

/**
 * @title 自定义颜色
 * @desc 自定义滑块条的颜色
 */
export const CustomColor = () => {
  const colorMap = [
    {
      color: '#237ffa',
      type: 'primary',
    },
    {
      color: '#ff5959',
      type: 'danger',
    },
    {
      color: '#14ca64',
      type: 'success',
    },
    {
      color: '#fab007',
      type: 'warning',
    },
  ]

  const [type, setType] = React.useState('primary')
  return (
    <>
      <h1>CustomColor</h1>
      <div className="slider-custom-color__wrap">
        <div style={{ display: 'flex', justifyContent: 'flex-end' }}>
          {colorMap.map((item) => (
            <span
              style={{
                width: 25,
                height: 22,
                marginRight: 12,
                background: item.color,
                display: 'inline-block',
                cursor: 'pointer',
                boxShadow: type === item.type ? '0px 2px 4px 0px rgba(0,0,0,0.5)' : 'none',
              }}
              onClick={() => {
                setType(item.type)
              }}
              key={item.color}
            ></span>
          ))}
        </div>
        <Slider color={colorMap.find((item) => item.type === type).color} />
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import Slider from '@hi-ui/slider'

/**
 * @title 禁用状态
 */
export const Disabled = () => {
  return (
    <>
      <h1>Disabled</h1>
      <div className="slider-disabled__wrap">
        <Slider
          style={{ width: 300 }}
          onChange={(value) => {
            console.log(value)
          }}
          defaultValue={80}
          disabled
        ></Slider>
      </div>
    </>
  )
}

```

### mark.stories.tsx

```typescript
import React from 'react'
import Slider from '@hi-ui/slider'

/**
 * @title 自定义步长
 * @desc 按定义步长输入离散型数值，可加入特殊位置
 */
export const Mark = () => {
  const [marks] = React.useState({
    0: '0°C',
    27: '27°C',
    45: '45°C',
    100: '100°C',
  })
  return (
    <>
      <h1>Mark</h1>
      <div className="slider-mark__wrap">
        <Slider
          style={{ width: 300 }}
          marks={marks}
          step={9}
          onChange={(value) => {
            console.log(value)
          }}
        />
      </div>
    </>
  )
}

```

### range.stories.tsx

```typescript
import React from 'react'
import Slider from '@hi-ui/slider'

/**
 * @title 可控范围
 */
export const Range = () => {
  const [value, setValue] = React.useState(0)
  return (
    <>
      <h1>Range</h1>
      <div className="slider-range__wrap">
        <Slider
          style={{ width: 300 }}
          defaultValue={value}
          min={1}
          max={90}
          onChange={setValue}
          showRangeLabel
        />
      </div>
    </>
  )
}

```

### reversed.stories.tsx

```typescript
import React from 'react'
import Slider from '@hi-ui/slider'

/**
 * @title 方向反转
 */
export const Reversed = () => {
  return (
    <>
      <h1>Reversed</h1>
      <div className="slider-reversed__wrap">
        <Slider
          reversed
          style={{ width: 300 }}
          onChange={(value) => {
            console.log(value)
          }}
        ></Slider>
      </div>
    </>
  )
}

```

### tip.stories.tsx

```typescript
import React from 'react'
import Slider from '@hi-ui/slider'

/**
 * @title 自定义提示
 * @desc 可自定义提示内容的格式
 */
export const TipFormatter = () => {
  return (
    <>
      <h1>TipFormatter</h1>
      <div className="slider-tip-formatter__wrap">
        <Slider
          style={{ width: 300 }}
          onChange={(value) => {
            console.log(value)
          }}
          tipFormatter={(value) => {
            console.log(value)
            return value + '英寸'
          }}
        ></Slider>
      </div>
    </>
  )
}

```

### vertical.stories.tsx

```typescript
import React from 'react'
import Slider from '@hi-ui/slider'
import { Counter } from '@hi-ui/counter'

/**
 * @title 垂直用法
 */
export const Vertical = () => {
  const [value, setValue] = React.useState(0)
  return (
    <>
      <h1>Vertical</h1>
      <div className="slider-Vertical__wrap">
        <Slider vertical value={value} onChange={setValue} style={{ height: 300 }} />
        <br />
        <Counter value={value} onChange={setValue} step={10} min={0} max={100} />
      </div>
    </>
  )
}

```

## space 组件

### align.stories.tsx

```typescript
import React from 'react'
import Space from '@hi-ui/space'
import Avatar from '@hi-ui/avatar'
import Button from '@hi-ui/button'

/**
 * @title 对齐方式
 * @desc 自定义元素之间的对齐方式，默认是居中
 */
export const Align = () => {
  return (
    <>
      <h1>对齐方式</h1>
      <div className="space-basic__wrap">
        <Space size={10}>
          <Space align="flex-start" size="md" style={{ border: '1px solid #f1f1f1', padding: 10 }}>
            <Avatar
              src="https://avatars.githubusercontent.com/u/810438?v=4"
              initials="P"
              size="lg"
            />
            <span>start</span>
            <Button type="primary">button</Button>
          </Space>
          <Space align="center" size="md" style={{ border: '1px solid #f1f1f1', padding: 10 }}>
            <Avatar
              src="https://avatars.githubusercontent.com/u/810438?v=4"
              initials="P"
              size="lg"
            />
            <span>center</span>
            <Button type="primary">button</Button>
          </Space>
          <Space align="flex-end" size="md" style={{ border: '1px solid #f1f1f1', padding: 10 }}>
            <Avatar
              src="https://avatars.githubusercontent.com/u/810438?v=4"
              initials="P"
              size="lg"
            />
            <span>end</span>
            <Button type="primary">button</Button>
          </Space>
        </Space>
      </div>
    </>
  )
}

```

### auto-size.stories.tsx

```typescript
import React, { useState } from 'react'
import Space from '@hi-ui/space'
import Button from '@hi-ui/button'
import Counter from '@hi-ui/counter'
import Switch from '@hi-ui/switch'

/**
 * @title 自定义间距大小
 * @desc 通过 size 设置数字开启自定义间距的大小，也支持数组分别设置纵横向间距
 */
export const AutoSize = () => {
  const [size, setSize] = useState(8)
  const [checked, setChecked] = useState(false)
  const nextSize = checked ? [size * 2, size] : size

  return (
    <>
      <h1>自定义间距大小</h1>
      <div className="space-basic__wrap">
        <Space direction="column" align="flex-start" size={12}>
          <div>是否同时设置2倍于横向间距的纵向间距</div>
          <Switch checked={checked} onChange={(checked) => setChecked(checked)} />

          <div>间距调整</div>
          <Counter value={size} min={0} onChange={(v) => setSize(v)} />

          <Space size={nextSize}>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
            <Button>HiUI Button</Button>
          </Space>
        </Space>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Space from '@hi-ui/space'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 * @desc 包裹目标元素们并使它们产生间距
 */
export const Basic = () => {
  return (
    <>
      <h1>基本使用</h1>
      <div className="space-basic__wrap">
        <Space>
          <Button type="primary">Button1</Button>
          <Button>Button2</Button>
          <Button>Button3</Button>
          <Button>Button4</Button>
        </Space>
      </div>
    </>
  )
}

```

### direction.stories.tsx

```typescript
import React from 'react'
import Space from '@hi-ui/space'
import Button from '@hi-ui/button'

/**
 * @title 垂直排列
 * @desc 通过 direction 设置元素排版方向，支持垂直间距
 */
export const Direction = () => {
  return (
    <>
      <h1>垂直排列</h1>
      <div className="space-basic__wrap">
        <Space direction="column" size="lg">
          <Button type="primary">Button1</Button>
          <Button>Button2</Button>
          <Button>Button3</Button>
        </Space>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Space from '@hi-ui/space'
import Button from '@hi-ui/button'

/**
 * @title 不同大小
 * @desc 通过 size 设置标椎的间距大小，默认为小号
 */
export const Size = () => {
  return (
    <>
      <h1>不同大小</h1>
      <div className="space-size__wrap">
        <h2>sm</h2>
        <Space size="sm">
          <Button type="primary">Button1</Button>
          <Button>Button2</Button>
          <Button>Button3</Button>
          <Button>Button4</Button>
        </Space>
        <h2>md</h2>
        <Space size="md">
          <Button type="primary">Button1</Button>
          <Button>Button2</Button>
          <Button>Button3</Button>
          <Button>Button4</Button>
        </Space>
        <h2>lg</h2>
        <Space size="lg">
          <Button type="primary">Button1</Button>
          <Button>Button2</Button>
          <Button>Button3</Button>
          <Button>Button4</Button>
        </Space>
      </div>
    </>
  )
}

```

### split.stories.tsx

```typescript
import React from 'react'
import Space from '@hi-ui/space'
import Button from '@hi-ui/button'
import { RightOutlined } from '@hi-ui/icons'

/**
 * @title 分隔符
 * @desc 通过 separator 自定义分隔符
 */
export const Split = () => {
  return (
    <>
      <h1>分隔符</h1>
      <div className="space-basic__wrap">
        <Space separator={<RightOutlined />} align="center">
          <Button type="primary" appearance="link">
            button
          </Button>
          <Button type="primary" appearance="link">
            button
          </Button>
          <Button type="primary" appearance="link">
            button
          </Button>
          <Button type="primary" appearance="link">
            button
          </Button>
        </Space>
      </div>
    </>
  )
}

```

## spinner 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Spinner from '@hi-ui/spinner'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="spinner-basic__wrap">
        <Spinner />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Space from '@hi-ui/space'
import Spinner from '@hi-ui/spinner'

/**
 * @title 设置大小
 */
export const Size = () => {
  return (
    <>
      <h1>Size</h1>
      <div className="spinner-size__wrap">
        <Space size={20}>
          <Spinner size={12} />
          <Spinner size={24} />
          <Spinner size="lg" />
        </Space>
      </div>
    </>
  )
}

```

## stepper 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Stepper from '@hi-ui/stepper'

/**
 * @title 基础用法
 * @desc 一个复杂任务需要拆分多个步骤完成，步骤数量不宜过多，4-7个为宜
 */
export const Basic = () => {
  const [data] = React.useState([
    {
      title: '账号信息',
    },
    {
      title: '邮箱激活',
    },
    {
      title: '信息登记',
    },
  ])

  return (
    <>
      <h1>Stepper</h1>
      <div className="stepper-basic__wrap">
        <Stepper data={data} current={2} />
      </div>
    </>
  )
}

```

### content.stories.tsx

```typescript
import React from 'react'
import Stepper from '@hi-ui/stepper'

/**
 * @title 辅助信息
 * @desc 步骤名称不足以表达明确用意，用辅助信息进一步说明
 */
export const Content = () => {
  const [data] = React.useState([
    {
      title: '账号信息',
      content: '请输入账号信息',
    },
    {
      title: '邮箱激活',
      content: '请输入邮箱',
    },
    {
      title: '信息登记',
      content:
        '请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息请输入个人信息',
    },
  ])

  return (
    <>
      <h1>Content</h1>
      <div className="stepper-content__wrap">
        <Stepper data={data} current={2} onChange={console.log} />
      </div>
    </>
  )
}

```

### custom-icon.stories.tsx

```typescript
import React from 'react'
import Stepper from '@hi-ui/stepper'
import { TimeOutlined, UserOutlined } from '@hi-ui/icons'

/**
 * @title 图标用法
 * @desc 每个步骤可用图标明确表示含义，带来丰富生动的效果
 */
export const CustomIcon = () => {
  const [data] = React.useState([
    {
      title: '账号信息',
      icon: <UserOutlined />,
    },
    {
      title: '邮箱激活',
      icon: <TimeOutlined />,
    },
    {
      title: '信息登记',
      icon: <UserOutlined />,
    },
  ])

  return (
    <>
      <h1>CustomIcon</h1>
      <div className="stepper-custom-icon__wrap">
        <Stepper
          data={data}
          current={2}
          itemLayout="vertical"
          // type="dot"
          onChange={console.log}
        />
      </div>
    </>
  )
}

```

### dot.stories.tsx

```typescript
import React from 'react'
import Stepper from '@hi-ui/stepper'

/**
 * @title 小圆点
 */
export const Dot = () => {
  const [data] = React.useState([
    {
      title: '账号信息',
      content: '请输入账号信息',
    },
    {
      title: '邮箱激活',
      content: '请输入邮箱',
    },
    {
      title: '信息登记',
      content: '请输入个人信息',
    },
  ])

  return (
    <>
      <h1>Dot</h1>
      <div className="stepper-dot__wrap">
        <Stepper data={data} current={2} type="dot" />
      </div>
    </>
  )
}

```

### item-layout.stories.tsx

```typescript
import React from 'react'
import Stepper from '@hi-ui/stepper'

/**
 * @title 标题结构
 * @desc 步骤与内容通过上下结构可以有效利用页面空间
 */
export const ItemLayout = () => {
  const [data] = React.useState([
    {
      title: '账号信息',
      content: '请输入账号信息',
    },
    {
      title: '邮箱激活',
      content: '请输入邮箱',
    },
    {
      title: '信息登记',
      content: '请输入个人信息',
    },
  ])

  return (
    <>
      <h1>ItemLayout</h1>
      <div className="stepper-item-vertical__wrap">
        <Stepper data={data} current={2} itemLayout="vertical" />
        <br />
        <br />
        <Stepper data={data} current={3} itemLayout="vertical" type="dot" />
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import React from 'react'
import Stepper from '@hi-ui/stepper'

/**
 * @title 垂直用法
 */
export const Placement = () => {
  const [data] = React.useState([
    {
      title: '账号信息',
      content: '请输入账号信息',
    },
    {
      title: '邮箱激活',
      content: '请输入邮箱',
    },
    {
      title: '信息登记信息登记信息登记信息登记信息登记',
      content: '请输入个人信息',
    },
  ])

  return (
    <>
      <h1>Placement</h1>
      <div className="stepper-placement__wrap">
        <Stepper data={data} current={2} placement="vertical" />
      </div>
    </>
  )
}

```

## svg-icon 组件

### basic.stories.tsx

```typescript
import React from 'react'
import SvgIcon from '@hi-ui/svg-icon'

/**
 * @title 基础用法
 * @desc 作为 svg 容器快速绘制生成简单的 SvgIcon
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="svg-icon-basic__wrap">
        <SvgIcon aria-label="home">
          <path d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z" />
        </SvgIcon>
      </div>
    </>
  )
}

```

### viewbox.stories.tsx

```typescript
import React from 'react'
import SvgIcon from '@hi-ui/svg-icon'

/**
 * @title Viewbox
 * @desc 自定义 viewBox 设置 svg 显示区域
 */
export const Viewbox = () => {
  return (
    <>
      <h1>Viewbox</h1>
      <div className="svg-icon-viewbox__wrap">
        <SvgIcon aria-label="action" viewBox="0 0 16 16">
          <path d="M4.5,6.5 L4.5,9.5 L1.5,9.5 L1.5,6.5 L4.5,6.5 Z M9.5,6.5 L9.5,9.5 L6.5,9.5 L6.5,6.5 L9.5,6.5 Z M14.5,6.5 L14.5,9.5 L11.5,9.5 L11.5,6.5 L14.5,6.5 Z"></path>
        </SvgIcon>
      </div>
    </>
  )
}

```

## switch 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Switch from '@hi-ui/switch'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>状态</h1>
      <div className="switch-basic__wrap">
        <Switch defaultChecked />
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import Switch from '@hi-ui/switch'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [checked, setChecked] = React.useState(false)

  return (
    <>
      <h1>Controlled</h1>
      <div
        className="switch-controlled__wrap"
        style={{ display: 'flex', flexDirection: 'column', gap: 10 }}
      >
        <Switch checked={checked} onChange={setChecked} />
        <Switch checked={checked} onChange={setChecked} />
      </div>
    </>
  )
}

```

### custom.stories.tsx

```typescript
import React from 'react'
import Switch from '@hi-ui/switch'
import { CloseOutlined, CheckOutlined } from '@hi-ui/icons'

/**
 * @title 自定义内容
 */
export const Custom = () => {
  return (
    <>
      <h1>自定义内容</h1>
      <div className="switch-basic__wrap">
        <h2>自定义文字 </h2>
        <div style={{ display: 'flex', flexDirection: 'column', gap: 10 }}>
          <Switch
            defaultChecked
            content={['开', '关']}
            onChange={(checked) => console.log('change', checked)}
          />
          <Switch
            defaultChecked
            content={['ON', 'OFF']}
            onChange={(checked) => console.log('change', checked)}
          />
        </div>

        <h2>自定义图标 </h2>
        <div>
          <Switch
            defaultChecked
            content={[<CheckOutlined key={1} />, <CloseOutlined key={2} />]}
            onChange={(checked) => console.log('change', checked)}
          />
        </div>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Switch from '@hi-ui/switch'

/**
 * @title 不同大小
 */
export const Size = () => {
  return (
    <>
      <h1>Size</h1>
      <div className="switch-basic__wrap">
        <h2>sm</h2>
        <div>
          <Switch size="sm" defaultChecked />
        </div>

        <h2>md</h2>
        <div>
          <Switch size="md" defaultChecked />
        </div>

        <h2>lg</h2>
        <Switch size="lg" defaultChecked />
      </div>
    </>
  )
}

```

### status.stories.tsx

```typescript
import React from 'react'
import Switch from '@hi-ui/switch'

/**
 * @title 不同状态
 */
export const Status = () => {
  return (
    <>
      <h1>状态</h1>
      <div className="switch-basic__wrap">
        <h2>默认</h2>
        <div>
          <Switch defaultChecked />
        </div>

        <h2>受控开启</h2>
        <div>
          <Switch checked />
        </div>

        <h2>受控关闭</h2>
        <Switch checked={false} />

        <h2>禁用</h2>
        <div style={{ display: 'flex', flexDirection: 'column', gap: 10 }}>
          <Switch disabled checked />
          <Switch disabled checked={false} />
        </div>
      </div>
    </>
  )
}

```

## table 组件

### async-expanded-render.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 异步展开渲染
 */
export const AsyncExpandedRender = () => {
  const [columns] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 150,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 240,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])

  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])

  return (
    <>
      <h1>AsyncExpandedRender for Table</h1>
      <div className="table-async-expanded-render__wrap" style={{ minWidth: 660 }}>
        <Table
          defaultExpandedEmbedRowKeys={[1]}
          expandedRender={(rowData, index) => {
            console.log('expandedRender', rowData, index)

            return new Promise((resolve) => {
              // 模拟异步
              setTimeout(() => {
                const embedTable = (
                  <Table
                    striped
                    columns={columns}
                    data={[
                      {
                        name: '小米9',
                        type: '手机',
                        size: '6G+64G',
                        price: '3299.00',
                        address: '华润五彩城店',
                        stock: '29,000',
                        key: 1,
                      },
                      {
                        name: '小米9 SE',
                        type: '手机',
                        size: '6G+64G 幻彩蓝',
                        price: '1999.00',
                        address: '清河店',
                        stock: '10,000',
                        key: 2,
                      },
                      {
                        name: '小米8',
                        type: '手机',
                        size: '6G+64G 幻彩蓝',
                        price: '2599.00',
                        address: '双安店',
                        stock: '12,000',
                        key: 3,
                      },
                    ]}
                  ></Table>
                )

                resolve(embedTable)
              }, 3000)
            })
          }}
          columns={columns}
          data={data}
        />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic for Table</h1>
      <div className="table-basic__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
              render: (text, row) => {
                console.log(text, row)
                return text + '*'
              },
            },
            {
              title: '品类',
              dataKey: 'type',
            },
            {
              title: '规格',
              dataKey: 'size',
            },
            {
              title: '单价',
              dataKey: 'price',
            },
            {
              title: '门店',
              dataKey: 'address',
            },
            {
              title: '库存',
              dataKey: 'stock',
            },
          ]}
          // rowSelection={{ selectedRowKeys: [] }}
          data={[
            {
              name: '小米9',
              type: '手机',
              size: '6G+64G',
              price: '3299.00',
              address: '华润五彩城店',
              stock: '29,000',
              key: 1,
            },
            {
              name: '小米9 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '1999.00',
              address: '清河店',
              stock: '10,000',
              key: 2,
            },
            {
              name: '小米8',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '2599.00',
              address: '双安店',
              stock: '12,000',
              key: 3,
            },
            {
              name: 'Redmi Note7',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '999.00',
              address: '华润五彩城店',
              stock: '140,000',
              key: 4,
            },
            {
              name: '小米8 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '699.00',
              address: '双安店',
              stock: '12,000',
              key: 5,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### bordered.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 带边框
 */
export const Bordered = () => {
  const [column] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size1',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price1',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size2',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price2',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size3',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price3',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size4',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price4',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size5',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price5',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size6',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price6',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size7',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price7',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 150,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])
  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      price1: '3299.00',
      price2: '3299.00',
      price3: '3299.00',
      price4: '3299.00',
      price5: '3299.00',
      price6: '3299.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      price1: '1999.00',
      price2: '1999.00',
      price3: '1999.00',
      price4: '1999.00',
      price5: '1999.00',
      price6: '1999.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      price1: '2599.00',
      price2: '2599.00',
      price3: '2599.00',
      price4: '2599.00',
      price5: '2599.00',
      price6: '2599.00',
      price7: '2599.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      price1: '999.00',
      price2: '999.00',
      price3: '999.00',
      price4: '999.00',
      price5: '999.00',
      price6: '999.00',
      price7: '999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])

  return (
    <>
      <h1>Bordered for Table</h1>
      <div className="table-bordered__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table bordered columns={column} data={data} />
      </div>
    </>
  )
}

```

### calc.stories.tsx

```typescript
import React from 'react'
import Table, { TableColumnItem } from '@hi-ui/table'

/**
 * @title 统计行
 */
export const Calc = () => {
  const [columns] = React.useState<TableColumnItem[]>([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 180,
    },
    {
      title: '单价',
      dataKey: 'price',
      align: 'right',
      total: true,
      avg: true,
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 180,
    },
    {
      title: '库存',
      dataKey: 'stock',
      align: 'right',
      width: 100,
    },
  ])
  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 全息幻彩蓝',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 全息幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 全息幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 全息幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 全息幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])

  return (
    <>
      <h1>Calc for Table</h1>
      <div className="table-calc__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table columns={columns} data={data} fixedToColumn={{ right: 'stock' }} />
      </div>
    </>
  )
}

```

### col-menu.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 列筛选
 */
export const ColMenu = () => {
  const [columns] = React.useState([
    {
      title: 'Name',
      dataKey: 'name',
      width: 120,
      key: 1,
    },
    {
      title: 'Age',
      dataKey: 'age',
      key: 2,
      width: 80,
      sorter(pre: any, next: any) {
        return pre.raw.age - next.raw.age
      },
    },
    {
      title: 'Home phone',
      width: 180,
      dataKey: 'tel',
      key: 3,
    },
    {
      title: 'Home phone1',
      dataKey: 'tel1',
      width: 180,
      key: 4,
    },
    {
      title: 'Home phone2',
      width: 180,
      dataKey: 'tel2',
      key: 5,
    },
    {
      title: 'Home phone3',
      width: 180,
      dataKey: 'tel3',
      key: 6,
    },
    {
      title: 'Home phone4',
      width: 180,
      dataKey: 'tel4',
      key: 7,
    },
    {
      title: 'Home phone5',
      width: 180,
      dataKey: 'tel5',
      key: 8,
    },
    {
      title: 'Home phone6',
      width: 180,
      dataKey: 'tel6',
      key: 9,
    },
    {
      title: 'Home phone7',
      width: 180,
      dataKey: 'tel7',
      key: 10,
    },
    {
      title: 'Home phone8',
      width: 180,
      dataKey: 'tel8',
      key: 11,
    },
    {
      title: 'Home phone9',
      width: 180,
      dataKey: 'tel9',
      key: 12,
    },
    {
      title: 'Home phone10',
      width: 180,
      dataKey: 'tel10',
      key: 13,
    },
    {
      title: 'Home phone11',
      width: 180,
      dataKey: 'tel11',
      key: 14,
    },

    {
      title: 'Home phone12',
      width: 180,
      dataKey: 'tel12',
      key: 15,
    },

    {
      title: 'Phone',
      dataKey: 'phone',
      width: 180,
      key: 16,
      sorter(pre: any, next: any) {
        return pre.phone - next.phone
      },
    },
    {
      title: 'Address',
      width: 240,
      dataKey: 'address',
      key: 17,
    },
  ])
  const [data] = React.useState([
    {
      key: '1',
      name: 'John Brown',
      age: 32,
      tel: '0571-22098909',
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18889898989,
      address: 'New York No. 1 Lake Park',
    },
    {
      key: '2',
      name: 'Jim Green',
      phone: 18889898888,
      tel: '0571-22098909',
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      age: 42,
      address: 'London No. 1 Lake Park',
    },
    {
      key: '3',
      name: 'Joe Black',
      age: 32,
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel: '0575-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18900010002,
      address: 'Sidney No. 1 Lake Park',
    },
    {
      key: '4',
      name: 'Jim Red',
      age: 18,
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel: '0575-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18900010002,
      address: 'London No. 2 Lake Park',
    },
    {
      key: '5',
      name: 'Jake White',
      age: 18,
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel: '0575-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18900010002,
      address: 'Dublin No. 2 Lake Park',
    },
  ])

  return (
    <>
      <h1>ColMenu for Table</h1>
      <div className="table-col-menu__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table
          columns={columns}
          data={data}
          showColMenu
          onHighlightedCol={(changedColInfo, highlightedColKeys) => {
            console.log(changedColInfo, highlightedColKeys)
          }}
          onChange={(sorter, extra) => {
            console.log(sorter, extra)
          }}
        />
      </div>
    </>
  )
}

```

### custom-filter.stories.tsx

```typescript
import { SearchOutlined, FilterOutlined } from '@hi-ui/icons'
import React from 'react'
import Table from '@hi-ui/table'
import Input from '@hi-ui/input'
import Button from '@hi-ui/button'
import CheckSelect from '@hi-ui/check-select'
import EllipsisTooltip from '@hi-ui/ellipsis-tooltip'

/**
 * @title 自定义过滤
 */
export const CustomFilter = () => {
  const initialData = React.useRef([
    {
      key: '1',
      name: 'John Brown',
      age: 32,
      tel: '0571-22098909',
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18889898989,
      address: 'New York No. 1 Lake Park',
    },
    {
      key: '2',
      name: 'Jim Green',
      phone: 18889898888,
      tel: '0571-22098909',
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      age: 42,
      address: 'London No. 1 Lake Park',
    },
    {
      key: '3',
      name: 'Joe Black',
      age: 32,
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel: '0575-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18900010002,
      address: 'Sidney No. 1 Lake Park',
    },
    {
      key: '4',
      name: 'Jim Red',
      age: 18,
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel: '0575-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18900010002,
      address: 'London No. 2 Lake Park',
    },
    {
      key: '5',
      name: 'Jake White',
      age: 18,
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel: '0575-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18900010002,
      address: 'Dublin No. 2 Lake Park',
    },
  ])
  const [data, setData] = React.useState(initialData.current)
  const customFilterData = (keyword, label) => {
    if (keyword.length > 0) {
      setData(
        initialData.current.filter((item) => {
          return typeof keyword === 'string'
            ? item[label].includes(keyword)
            : keyword.includes(item[label])
        })
      )
    } else {
      setData(initialData.current)
    }
  }

  const [columns] = React.useState([
    {
      title: 'Name',
      dataKey: 'name',
      width: 120,
      key: 1,
      filterDropdownClassName: 'table-customefilter',
      filterIcon: <SearchOutlined />,
      filterDropdown({ setFilterDropdownVisible }) {
        let keyword = ''
        return (
          <div>
            <Input
              placeholder="请输入关键字"
              onChange={(e) => {
                keyword = e.target.value
              }}
            />
            <div style={{ marginTop: '8px' }}>
              <Button
                onClick={() => {
                  customFilterData(keyword, 'name')
                  setFilterDropdownVisible(false)
                }}
                type="primary"
                size="sm"
              >
                确定
              </Button>
              <Button onClick={() => setFilterDropdownVisible(false)} size="sm">
                取消
              </Button>
            </div>
          </div>
        )
      },
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
    },
    {
      title: 'Age',
      dataKey: 'age',
      key: 2,
      width: 80,
      sorter(pre, next) {
        return pre.raw.age - next.raw.age
      },
    },
    {
      title: (
        <div style={{ display: 'inline-flex', alignItems: 'center' }}>
          Home phone
          <CheckSelect
            style={{ width: 'auto', marginLeft: 2 }}
            optionWidth={200}
            customRender={<FilterOutlined />}
            searchable
            data={[
              { id: '0571-22098909', title: '0571-22098909' },
              { id: '0575-22098909', title: '0575-22098909' },
            ]}
            onChange={(value) => {
              console.log('value', value)
              customFilterData(value, 'tel')
            }}
          />
        </div>
      ),
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel',
      key: 3,
    },
    {
      title: 'Home phone1',
      dataKey: 'tel1',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      key: 4,
    },
    {
      title: 'Home phone2',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel2',
      key: 5,
    },
    {
      title: 'Home phone3',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel3',
      key: 6,
    },
    {
      title: 'Home phone4',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel4',
      key: 7,
    },
    {
      title: 'Home phone5',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel5',
      key: 8,
    },
    {
      title: 'Home phone6',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel6',
      key: 9,
    },
    {
      title: 'Home phone7',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel7',
      key: 10,
    },
    {
      title: 'Home phone8',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel8',
      key: 11,
    },
    {
      title: 'Home phone9',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel9',
      key: 12,
    },
    {
      title: 'Home phone10',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel10',
      key: 13,
    },
    {
      title: 'Home phone11',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel11',
      key: 14,
    },

    {
      title: 'Home phone12',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'tel12',
      key: 15,
    },
    {
      title: 'Phone',
      dataKey: 'phone',
      width: 180,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      key: 16,
      sorter(pre, next) {
        return pre.phone - next.phone
      },
    },
    {
      title: 'Address',
      width: 240,
      render(text) {
        return <EllipsisTooltip>{text}</EllipsisTooltip>
      },
      dataKey: 'address',
      key: 17,
    },
  ])

  return (
    <>
      <h1>CustomFilter for Table</h1>
      <div className="table-custom-filter__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table columns={columns} data={data} />
      </div>
    </>
  )
}

```

### data-sorter.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 数据排序
 */
export const DataSorter = () => {
  const [columns] = React.useState([
    {
      title: 'Name',
      dataKey: 'name',
      width: 120,
      key: 1,
    },
    {
      title: 'Age',
      dataKey: 'age',
      key: 2,
      width: 80,
      sorter(pre, next) {
        return pre.raw.age - next.raw.age
      },
    },
    {
      title: 'Home phone',
      width: 180,
      dataKey: 'tel',
      key: 3,
    },
    {
      title: 'Home phone1',
      dataKey: 'tel1',
      width: 180,
      key: 4,
    },
    {
      title: 'Home phone2',
      width: 180,
      dataKey: 'tel2',
      key: 5,
    },
    {
      title: 'Home phone3',
      width: 180,
      dataKey: 'tel3',
      key: 6,
    },
    {
      title: 'Home phone4',
      width: 180,
      dataKey: 'tel4',
      key: 7,
    },
    {
      title: 'Home phone5',
      width: 180,
      dataKey: 'tel5',
      key: 8,
    },
    {
      title: 'Home phone6',
      width: 180,
      dataKey: 'tel6',
      key: 9,
    },
    {
      title: 'Home phone7',
      width: 180,
      dataKey: 'tel7',
      key: 10,
    },
    {
      title: 'Home phone8',
      width: 180,
      dataKey: 'tel8',
      key: 11,
    },
    {
      title: 'Home phone9',
      width: 180,
      dataKey: 'tel9',
      key: 12,
    },
    {
      title: 'Home phone10',
      width: 180,
      dataKey: 'tel10',
      key: 13,
    },
    {
      title: 'Home phone11',
      width: 180,
      dataKey: 'tel11',
      key: 14,
    },

    {
      title: 'Home phone12',
      width: 180,
      dataKey: 'tel12',
      key: 15,
    },

    {
      title: 'Phone',
      dataKey: 'phone',
      width: 180,
      key: 16,
      sorter(pre, next) {
        return pre.phone - next.phone
      },
    },
    {
      title: 'Address',
      width: 240,
      dataKey: 'address',
      key: 17,
    },
  ])
  const [data] = React.useState([
    {
      key: '1',
      name: 'John Brown',
      age: 32,
      tel: '0571-22098909',
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18889898989,
      address: 'New York No. 1 Lake Park',
    },
    {
      key: '3',
      name: 'Joe Black',
      age: 32,
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel: '0575-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18900010002,
      address: 'Sidney No. 1 Lake Park',
    },
    {
      key: '4',
      name: 'Jim Red',
      age: 18,
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel: '0575-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18900010002,
      address: 'London No. 2 Lake Park',
    },
    {
      key: '5',
      name: 'Jake White',
      age: 18,
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel: '0575-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      phone: 18900010002,
      address: 'Dublin No. 2 Lake Park',
    },
    {
      key: '2',
      name: 'Jim Green',
      phone: 18889898888,
      tel: '0571-22098909',
      tel1: '0571-22098909',
      tel2: '0571-22098909',
      tel3: '0571-22098909',
      tel4: '0571-22098909',
      tel5: '0571-22098909',
      tel6: '0571-22098909',
      tel7: '0571-22098909',
      tel8: '0571-22098909',
      tel9: '0571-22098909',
      tel10: '0571-22098909',
      tel11: '0571-22098909',
      tel12: '0571-22098909',
      age: 42,
      address: 'London No. 1 Lake Park',
    },
  ])

  return (
    <>
      <h1>DataSorter for Table</h1>
      <div className="table-data-sorter__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table columns={columns} data={data} onChange={console.log} />
      </div>
    </>
  )
}

```

### data-source.stories.tsx

```typescript
import React from 'react'
import Space from '@hi-ui/space'
import Button from '@hi-ui/button'
import Table from '@hi-ui/table'

/**
 * @title 异步加载数据
 * @desc 封装了分页加载数据的逻辑
 */
export const DataSource = () => {
  const [columns] = React.useState([
    { title: 'ID', dataKey: 'id' },
    { title: 'Title', dataKey: 'title' },
  ])

  const [searchVal, setSearchVal] = React.useState(0)

  const handleDataSource = React.useCallback(
    (current, pageSize) => {
      return {
        url: 'https://mife-gallery.test.mi.com/hiui/stores',
        params: {
          page: current,
          pageSize,
          // searchParams: searchVal,
        },
        transformResponse: (res) => {
          const data = JSON.parse(res).data

          return {
            list: data.map((item, i) => {
              return {
                key: i,
                title: item.title + current,
                id: item.id,
              }
            }),
            total: 28,
          }
        },
      }
    },
    // 当查询参数变化后会更新 dataSource，此时会自动刷新数据
    // 如果不希望查询参数变化后马上更新数据，例如点击查询按钮后再去刷新数据，可以将该依赖值设置一个其他自定义的状态值
    [searchVal]
  )

  return (
    <>
      <h1>DataSource for Table</h1>
      <div className="table-data-source__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Space align="center" style={{ marginBottom: '1em' }}>
          <Button onClick={() => setSearchVal(searchVal + 1)}>模拟更新查询参数</Button>
          <small>更新后表格会从第一页开始重新加载数据</small>
        </Space>
        <Table
          columns={columns}
          dataSource={handleDataSource}
          // @ts-ignore
          // pagination={{
          //   showTotal: true,
          //   pageSizeOptions: [5, 10, 20],
          // }}
        />
      </div>
    </>
  )
}

```

### draggable.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 行拖拽
 */
export const Draggable = () => {
  return (
    <>
      <h1>Draggable for Table</h1>
      <div className="table-draggable__wrap" style={{ minWidth: 660 }}>
        <Table
          draggable
          onDragStart={(e) => console.log('onDragStart', e)}
          onDrop={(e) => {
            console.log('onDrop', e)
            return true
          }}
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
            },
            {
              title: '品类',
              dataKey: 'type',
            },
            {
              title: '规格',
              dataKey: 'size',
            },
            {
              title: '单价',
              dataKey: 'price',
            },
            {
              title: '门店',
              dataKey: 'address',
            },
            {
              title: '库存',
              dataKey: 'stock',
            },
          ]}
          // rowSelection={{ selectedRowKeys: [] }}
          data={[
            {
              name: '小米9',
              type: '手机',
              size: '6G+64G',
              price: '3299.00',
              address: '华润五彩城店',
              stock: '29,000',
              key: 1,
            },
            {
              name: '小米9 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '1999.00',
              address: '清河店',
              stock: '10,000',
              key: 2,
            },
            {
              name: '小米8',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '2599.00',
              address: '双安店',
              stock: '12,000',
              key: 3,
            },
            {
              name: 'Redmi Note7',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '999.00',
              address: '华润五彩城店',
              stock: '140,000',
              key: 4,
            },
            {
              name: '小米8 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '699.00',
              address: '双安店',
              stock: '12,000',
              key: 5,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### empty.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'
import EmptyState from '@hi-ui/empty-state'

/**
 * @title 空状态
 */
export const Empty = () => {
  return (
    <>
      <h1>Empty for Table</h1>
      <div className="table-empty__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
            },
            {
              title: '品类',
              dataKey: 'type',
            },
            {
              title: '规格',
              dataKey: 'size',
            },
            {
              title: '单价',
              dataKey: 'price',
            },
            {
              title: '门店',
              dataKey: 'address',
            },
            {
              title: '库存',
              dataKey: 'stock',
            },
          ]}
          data={[]}
          emptyContent={<EmptyState title={'暂时没有数据，请联系管理员'} />}
        />
      </div>
    </>
  )
}

```

### expanded-render.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 内嵌面板
 */
export const ExpandedRender = () => {
  const [columns] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 240,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])

  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])

  return (
    <>
      <h1>ExpandedRender for Table</h1>
      <div className="table-expanded-render__wrap" style={{ minWidth: 660 }}>
        <Table
          fixedToColumn={{ left: 'type' }}
          columns={columns}
          expandedRender={() => {
            return (
              <div style={{ backgroundColor: '#fff', padding: 24, textAlign: 'center' }}>
                此处是自定义展开渲染内容
              </div>
            )
          }}
          data={data}
        />
      </div>
    </>
  )
}

```

### field-key.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 字段别名
 */
export const FieldKey = () => {
  const [selectedRowKeys, setSelectedRowKeys] = React.useState<any>([])
  console.log('selectedRowKeys', selectedRowKeys)

  return (
    <>
      <h1>FieldKey for Table</h1>
      <div className="table-field-key__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table
          fixedToColumn={{ left: 'type' }}
          fieldKey="name"
          rowSelection={{
            selectedRowKeys,
            onChange: setSelectedRowKeys,
          }}
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
            },
            {
              title: '品类',
              dataKey: 'type',
              width: 80,
            },
            {
              title: '规格',
              dataKey: 'size',
            },
            {
              title: '单价',
              dataKey: 'price',
            },
            {
              title: '门店',
              dataKey: 'address',
            },
            {
              title: '库存',
              dataKey: 'stock',
            },
          ]}
          data={[
            {
              name: '小米9',
              type: '手机',
              size: '6G+64G',
              price: '3299.00',
              address: '华润五彩城店',
              stock: '29,000',
            },
            {
              name: '小米9 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '1999.00',
              address: '清河店',
              stock: '10,000',
            },
            {
              name: '小米8',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '2599.00',
              address: '双安店',
              stock: '12,000',
            },
            {
              name: 'Redmi Note7',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '999.00',
              address: '华润五彩城店',
              stock: '140,000',
            },
            {
              name: '小米8 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '699.00',
              address: '双安店',
              stock: '12,000',
            },
          ]}
        />
      </div>
    </>
  )
}

```

### fixed-header.stories.tsx

```typescript
import React from 'react'
import Table, { TableColumnItem } from '@hi-ui/table'

/**
 * @title 固定表头
 */
export const FixedHeader = () => {
  const [columns] = React.useState<TableColumnItem[]>([
    {
      title: 'Name',
      dataKey: 'name',
      width: 100,
    },
    {
      title: 'Other',
      dataKey: 'other',
      children: [
        {
          title: 'Age',
          dataKey: 'age',
          width: 100,
        },
        {
          title: 'Address',
          dataKey: 'address',
          children: [
            {
              title: 'Street',
              dataKey: 'street',
              width: 100,
            },
            {
              title: 'Block',
              dataKey: 'block',
              children: [
                {
                  title: 'Building',
                  dataKey: 'building',
                  width: 100,
                },
                {
                  title: 'Door No.',
                  dataKey: 'number',
                  width: 100,
                },
              ],
            },
          ],
        },
      ],
    },
    {
      title: 'Name2',
      dataKey: 'name2',
      width: 100,
    },
    {
      title: 'Name3',
      dataKey: 'name3',
      width: 100,
    },
    {
      title: 'Name4',
      dataKey: 'name4',
      width: 100,
    },
    {
      title: 'Name5',
      dataKey: 'name5',
      width: 100,
    },
    {
      title: 'Name6',
      dataKey: 'name6',
      width: 100,
    },
    {
      title: 'Name7',
      dataKey: 'name7',
      width: 100,
    },
    {
      title: 'Name8',
      dataKey: 'name8',
      width: 100,
    },
    {
      title: 'Name9',
      dataKey: 'name9',
      width: 100,
    },
    {
      title: 'Name10',
      dataKey: 'name10',
      width: 100,
    },
    {
      title: 'Company',
      dataKey: 'company',
      children: [
        {
          title: 'Address',
          dataKey: 'companyAddress',
          width: 200,
        },
        {
          title: 'Name',
          dataKey: 'companyName',
          width: 150,
        },
      ],
    },
    {
      title: 'Name11',
      dataKey: 'name11',
      width: 100,
    },
    {
      title: 'Name12',
      dataKey: 'name12',
      width: 100,
    },
    {
      title: 'Name13',
      dataKey: 'name13',
      width: 100,
    },
    {
      title: 'Name14',
      dataKey: 'name14',
      width: 100,
    },
    {
      title: 'Gender',
      dataKey: 'gender',
      width: 100,
    },
  ])

  const [data] = React.useState(() => {
    const data: any[] = []
    for (let i = 0; i < 6; i++) {
      const item = {
        key: i + 1,
        age: i + 1,
        street: 'Lake Park',
        building: 'C',
        number: 2035,
        name: 'Flcwl',
        companyAddress: 'Lake Street 42',
        companyName: 'SoftLake Co',
        gender: 'M',
      }

      for (let j = 2; j <= 14; j++) {
        item[`name${j}`] = `name${j}`
      }

      data.push(item)
    }

    return data
  })

  return (
    <>
      <h1>FixedHeader for Table</h1>
      <div className="table-fixed-header__wrap" style={{ minWidth: 660 }}>
        <Table
          rowSelection={{}}
          maxHeight={400}
          fixedToColumn={{
            // left: 'building',
            // left: 'address',
            left: 'number',
            right: 'gender',
            // right: 'companyName',
            // right: 'companyAddress',
          }}
          columns={columns}
          data={data}
        />
      </div>
    </>
  )
}

```

### footer-render.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 自定义页脚
 */
export const FooterRender = () => {
  const [columns] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
    },
    {
      title: '品类',
      dataKey: 'type',
    },
    {
      title: '规格',
      dataKey: 'size',
    },
    {
      title: '单价',
      dataKey: 'price',
    },
    {
      title: '门店',
      dataKey: 'address',
    },
    {
      title: '库存',
      dataKey: 'stock',
    },
  ])

  const [dataSource] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
    {
      name: '小米10',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 6,
    },
    {
      name: '小米10 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 7,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 8,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 9,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 10,
    },
  ])

  const [paginationState, setPaginationState] = React.useState({
    current: 1,
    data: dataSource.slice(0, 5),
  })

  const [selectedRowKeys, setSelectedRowKeys] = React.useState<any>([])

  return (
    <>
      <h1>FooterRender for Table</h1>
      <div className="table-footer-render__wrap" style={{ minWidth: 660 }}>
        <Table
          pagination={{
            showTotal: true,
            showJumper: true,
            pageSize: 5,
            total: dataSource.length,
            current: paginationState.current,
            onChange: (page, pre, size = 5) => {
              console.log('onPaginationChange', page, pre, size)

              setPaginationState({
                current: page,
                data: dataSource.slice(size * (page - 1), size * page),
              })
            },
          }}
          columns={columns}
          data={paginationState.data}
          rowSelection={{
            selectedRowKeys,
            onChange: (keys, target, shouldChecked, rows) => {
              console.log(keys, target, shouldChecked, rows)

              setSelectedRowKeys(keys)
            },
          }}
          footerRender={(pagination) => {
            return (
              <div
                style={{ display: 'flex', alignItems: 'center', justifyContent: 'space-between' }}
              >
                <div>
                  已选 <span style={{ color: '#237ffa' }}>{selectedRowKeys.length}</span> 项
                </div>
                {pagination}
              </div>
            )
          }}
        />
      </div>
    </>
  )
}

```

### frozen.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 列冻结
 */
export const Frozen = () => {
  return (
    <>
      <h1>Frozen for Table</h1>
      <div className="table-frozen__wrap" style={{ minWidth: 660 }}>
        <p>使用列冻结必须指定 column 每项 width</p>
        <Table
          fixedToColumn={{ left: 'type', right: 'address' }}
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
              width: 150,
            },
            {
              title: '品类',
              dataKey: 'type',
              width: 150,
              fixed: true,
            },
            {
              title: '规格',
              dataKey: 'size',
              width: 150,
            },
            {
              title: '单价',
              dataKey: 'price',
              width: 150,
            },
            {
              title: '规格1',
              dataKey: 'size1',
              width: 150,
            },
            {
              title: '单价1',
              dataKey: 'price1',
              width: 150,
            },
            {
              title: '规格2',
              dataKey: 'size2',
              width: 150,
            },
            {
              title: '单价2',
              dataKey: 'price2',
              width: 150,
            },
            {
              title: '规格3',
              dataKey: 'size3',
              width: 150,
            },
            {
              title: '单价3',
              dataKey: 'price3',
              width: 150,
            },
            {
              title: '规格4',
              dataKey: 'size4',
              width: 150,
            },
            {
              title: '单价4',
              dataKey: 'price4',
              width: 150,
            },
            {
              title: '规格5',
              dataKey: 'size5',
              width: 150,
            },
            {
              title: '单价5',
              dataKey: 'price5',
              width: 150,
            },
            {
              title: '规格6',
              dataKey: 'size6',
              width: 150,
            },
            {
              title: '单价6',
              dataKey: 'price6',
              width: 150,
            },

            {
              title: '规格7',
              dataKey: 'size7',
              width: 150,
            },
            {
              title: '单价7',
              dataKey: 'price7',
              width: 150,
            },
            {
              title: '门店',
              dataKey: 'address',
              width: 150,
              fixed: true,
            },
            {
              title: '库存',
              dataKey: 'stock',
              width: 150,
            },
          ]}
          data={[
            {
              name: '小米9',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '3299.00',
              size1: '6G+64G 幻彩蓝',
              price1: '3299.00',
              size2: '6G+64G 幻彩蓝',
              price2: '3299.00',
              size3: '6G+64G 幻彩蓝',
              price3: '3299.00',
              size4: '6G+64G 幻彩蓝',
              price4: '3299.00',
              size5: '6G+64G 幻彩蓝',
              price5: '3299.00',
              size6: '6G+64G 幻彩蓝',
              price6: '3299.00',
              size7: '6G+64G 幻彩蓝',
              price7: '3299.00',

              address: '华润五彩城店',
              stock: '29,000',
              key: 1,
            },
            {
              name: '小米9 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '1999.00',
              size1: '6G+64G 幻彩蓝',
              price1: '3299.00',
              size2: '6G+64G 幻彩蓝',
              price2: '3299.00',
              size3: '6G+64G 幻彩蓝',
              price3: '3299.00',
              size4: '6G+64G 幻彩蓝',
              price4: '3299.00',
              size5: '6G+64G 幻彩蓝',
              price5: '3299.00',
              size6: '6G+64G 幻彩蓝',
              price6: '3299.00',
              size7: '6G+64G 幻彩蓝',
              price7: '3299.00',
              address: '清河店',
              stock: '10,000',
              key: 2,
            },
            {
              name: '小米8',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '2599.00',
              size1: '6G+64G 幻彩蓝',
              price1: '3299.00',
              size2: '6G+64G 幻彩蓝',
              price2: '3299.00',
              size3: '6G+64G 幻彩蓝',
              price3: '3299.00',
              size4: '6G+64G 幻彩蓝',
              price4: '3299.00',
              size5: '6G+64G 幻彩蓝',
              price5: '3299.00',
              size6: '6G+64G 幻彩蓝',
              price6: '3299.00',
              size7: '6G+64G 幻彩蓝',
              price7: '3299.00',
              address: '双安店',
              stock: '12,000',
              key: 3,
            },
            {
              name: 'Redmi Note7',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '999.00',
              size1: '6G+64G 幻彩蓝',
              price1: '3299.00',
              size2: '6G+64G 幻彩蓝',
              price2: '3299.00',
              size3: '6G+64G 幻彩蓝',
              price3: '3299.00',
              size4: '6G+64G 幻彩蓝',
              price4: '3299.00',
              size5: '6G+64G 幻彩蓝',
              price5: '3299.00',
              size6: '6G+64G 幻彩蓝',
              price6: '3299.00',
              size7: '6G+64G 幻彩蓝',
              price7: '3299.00',
              address: '华润五彩城店',
              stock: '140,000',
              key: 4,
            },
            {
              name: '小米8 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '699.00',
              size1: '6G+64G 幻彩蓝',
              price1: '3299.00',
              size2: '6G+64G 幻彩蓝',
              price2: '3299.00',
              size3: '6G+64G 幻彩蓝',
              price3: '3299.00',
              size4: '6G+64G 幻彩蓝',
              price4: '3299.00',
              size5: '6G+64G 幻彩蓝',
              price5: '3299.00',
              size6: '6G+64G 幻彩蓝',
              price6: '3299.00',
              size7: '6G+64G 幻彩蓝',
              price7: '3299.00',
              address: '双安店',
              stock: '12,000',
              key: 5,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### group-header.stories.tsx

```typescript
import React from 'react'
import Table, { TableColumnItem } from '@hi-ui/table'

/**
 * @title 表头分组
 */
export const GroupHeader = () => {
  const [columns] = React.useState<TableColumnItem[]>([
    {
      title: 'Name',
      dataKey: 'name',
      width: 100,
    },
    {
      title: 'Other',
      dataKey: 'other',
      children: [
        {
          title: 'Age',
          dataKey: 'age',
          width: 80,
        },
        {
          title: 'Address',
          dataKey: 'address',
          children: [
            {
              title: 'Street',
              dataKey: 'street',
              width: 100,
            },
            {
              title: 'Block',
              dataKey: 'block',
              children: [
                {
                  title: 'Building',
                  dataKey: 'building',
                  width: 90,
                },
                {
                  title: 'Door No.',
                  dataKey: 'number',
                  width: 90,
                },
              ],
            },
          ],
        },
      ],
    },
    {
      title: 'Name2',
      dataKey: 'name2',
      width: 100,
    },
    {
      title: 'Name3',
      dataKey: 'name3',
      width: 100,
    },
    {
      title: 'Name4',
      dataKey: 'name4',
      width: 100,
    },
    {
      title: 'Name5',
      dataKey: 'name5',
      width: 100,
    },
    {
      title: 'Name6',
      dataKey: 'name6',
      width: 100,
    },
    {
      title: 'Name7',
      dataKey: 'name7',
      width: 100,
    },
    {
      title: 'Name8',
      dataKey: 'name8',
      width: 100,
    },
    {
      title: 'Name9',
      dataKey: 'name9',
      width: 100,
    },
    {
      title: 'Name10',
      dataKey: 'name10',
      width: 100,
    },
    {
      title: 'Company',
      dataKey: 'company',
      children: [
        {
          title: 'Address',
          dataKey: 'companyAddress',
          width: 200,
        },
        {
          title: 'Name',
          dataKey: 'companyName',
          width: 150,
        },
      ],
    },
    {
      title: 'Name11',
      dataKey: 'name11',
      width: 100,
    },
    {
      title: 'Name12',
      dataKey: 'name12',
      width: 100,
    },
    {
      title: 'Name13',
      dataKey: 'name13',
      width: 100,
    },
    {
      title: 'Name14',
      dataKey: 'name14',
      children: [
        {
          title: 'Address14',
          dataKey: 'address14',
          width: 100,
        },
        {
          title: 'Company14',
          dataKey: 'company14',
          width: 100,
        },
      ],
    },
    {
      title: 'Gender',
      dataKey: 'gender',
      width: 100,
    },
  ])

  const [data] = React.useState(() => {
    const data: any[] = []
    for (let i = 0; i < 6; i++) {
      const item = {
        key: i + 1,
        age: i + 1,
        street: 'Lake Park',
        building: 'C',
        number: 2035,
        name: 'Flcwl',
        companyAddress: 'Lake Street 42',
        companyName: 'SoftLake Co',
        gender: 'M',
      }

      for (let j = 2; j <= 14; j++) {
        item[`name${j}`] = `name${j}`
      }

      data.push(item)
    }

    return data
  })

  return (
    <>
      <h1>GroupHeader for Table</h1>
      <div className="table-group-header__wrap" style={{ minWidth: 660 }}>
        <Table
          rowSelection={{}}
          fixedToColumn={{
            // left: 'building',
            // left: 'address',
            left: 'number',
            right: 'gender',
            // right: 'address14',
            // right: 'companyName',
            // right: 'companyAddress',
          }}
          columns={columns}
          data={data}
        />
      </div>
    </>
  )
}

```

### header-colspan.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 表头列合并
 * @desc 只支持表头列合并，被合并的表头需要设置 colSpan 为 0，则该表头不显示
 */
export const HeaderColSpan = () => {
  return (
    <>
      <h1>Header ColSpan</h1>
      <div className="table-header-colspan__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table
          bordered
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
              width: 100,
              align: 'center',
              render: (text, row) => {
                console.log(text, row)
                return text + '*'
              },
            },
            {
              title: '品类 + 型号',
              dataKey: 'type',
              align: 'center',
              width: 100,
              colSpan: 2,
            },
            {
              title: '规格',
              dataKey: 'size',
              width: 100,
              colSpan: 0,
            },
            {
              title: '单价',
              dataKey: 'price',
              width: 100,
            },
            {
              title: '门店 + 库存',
              dataKey: 'address',
              align: 'center',
              width: 100,
              colSpan: 2,
            },
            {
              title: '库存',
              dataKey: 'stock',
              width: 100,
              colSpan: 0,
            },
          ]}
          data={[
            {
              name: '小米9',
              type: '手机',
              size: '6G+64G',
              price: '3299.00',
              address: '华润五彩城店',
              stock: '29,000',
              key: 1,
            },
            {
              name: '小米9 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '1999.00',
              address: '清河店',
              stock: '10,000',
              key: 2,
            },
            {
              name: '小米8',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '2599.00',
              address: '双安店',
              stock: '12,000',
              key: 3,
            },
            {
              name: 'Redmi Note7',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '999.00',
              address: '华润五彩城店',
              stock: '140,000',
              key: 4,
            },
            {
              name: '小米8 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '699.00',
              address: '双安店',
              stock: '12,000',
              key: 5,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### highlight-cols.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 列高亮
 */
export const HighlightCols = () => {
  const [column] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size1',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price1',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size2',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price2',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size3',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price3',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size4',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price4',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size5',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price5',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size6',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price6',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size7',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price7',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 150,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])
  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      price1: '3299.00',
      price2: '3299.00',
      price3: '3299.00',
      price4: '3299.00',
      price5: '3299.00',
      price6: '3299.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      price1: '1999.00',
      price2: '1999.00',
      price3: '1999.00',
      price4: '1999.00',
      price5: '1999.00',
      price6: '1999.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      price1: '2599.00',
      price2: '2599.00',
      price3: '2599.00',
      price4: '2599.00',
      price5: '2599.00',
      price6: '2599.00',
      price7: '2599.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      price1: '999.00',
      price2: '999.00',
      price3: '999.00',
      price4: '999.00',
      price5: '999.00',
      price6: '999.00',
      price7: '999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])

  return (
    <>
      <h1>HighlightCols for Table</h1>
      <div className="table-highlight-cols__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table columns={column} data={data} highlightedColKeys={['name']} striped />
      </div>
    </>
  )
}

```

### highlight-rows.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 行高亮
 */
export const HighlightRows = () => {
  const [column] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size1',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price1',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size2',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price2',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size3',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price3',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size4',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price4',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size5',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price5',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size6',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price6',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size7',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price7',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 150,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])
  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      price1: '3299.00',
      price2: '3299.00',
      price3: '3299.00',
      price4: '3299.00',
      price5: '3299.00',
      price6: '3299.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      price1: '1999.00',
      price2: '1999.00',
      price3: '1999.00',
      price4: '1999.00',
      price5: '1999.00',
      price6: '1999.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      price1: '2599.00',
      price2: '2599.00',
      price3: '2599.00',
      price4: '2599.00',
      price5: '2599.00',
      price6: '2599.00',
      price7: '2599.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      price1: '999.00',
      price2: '999.00',
      price3: '999.00',
      price4: '999.00',
      price5: '999.00',
      price6: '999.00',
      price7: '999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])

  return (
    <>
      <h1>HighlightRows for Table</h1>
      <div className="table-highlight-rows__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table columns={column} data={data} highlightedRowKeys={[1, 4]} striped />
      </div>
    </>
  )
}

```

### highlight.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title hover 列高亮
 */
export const Highlight = () => {
  return (
    <>
      <h1>Highlight for Table</h1>
      <div className="table-highlight__wrap" style={{ minWidth: 660 }}>
        <Table
          showColHighlight
          showRowHighlight={false}
          striped
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
            },
            {
              title: '品类',
              dataKey: 'type',
            },
            {
              title: '规格',
              dataKey: 'size',
            },
            {
              title: '单价',
              dataKey: 'price',
            },
            {
              title: '门店',
              dataKey: 'address',
            },
            {
              title: '库存',
              dataKey: 'stock',
            },
          ]}
          // rowSelection={{ selectedRowKeys: [] }}
          data={[
            {
              name: '小米9',
              type: '手机',
              size: '6G+64G',
              price: '3299.00',
              address: '华润五彩城店',
              stock: '29,000',
              key: 1,
            },
            {
              name: '小米9 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '1999.00',
              address: '清河店',
              stock: '10,000',
              key: 2,
            },
            {
              name: '小米8',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '2599.00',
              address: '双安店',
              stock: '12,000',
              key: 3,
            },
            {
              name: 'Redmi Note7',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '999.00',
              address: '华润五彩城店',
              stock: '140,000',
              key: 4,
            },
            {
              name: '小米8 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '699.00',
              address: '双安店',
              stock: '12,000',
              key: 5,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### loading.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 加载态
 */
export const Loading = () => {
  return (
    <>
      <h1>Loading for Table</h1>
      <div className="table-loading__wrap" style={{ minWidth: 660 }}>
        <Table
          loading
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
            },
            {
              title: '品类',
              dataKey: 'type',
            },
            {
              title: '规格',
              dataKey: 'size',
            },
            {
              title: '单价',
              dataKey: 'price',
            },
            {
              title: '门店',
              dataKey: 'address',
            },
            {
              title: '库存',
              dataKey: 'stock',
            },
          ]}
          pagination={{ pageSize: 5, total: 5 }}
          data={[
            {
              name: '小米9',
              type: '手机',
              size: '6G+64G',
              price: '3299.00',
              address: '华润五彩城店',
              stock: '29,000',
              key: 1,
            },
            {
              name: '小米9 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '1999.00',
              address: '清河店',
              stock: '10,000',
              key: 2,
            },
            {
              name: '小米8',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '2599.00',
              address: '双安店',
              stock: '12,000',
              key: 3,
            },
            {
              name: 'Redmi Note7',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '999.00',
              address: '华润五彩城店',
              stock: '140,000',
              key: 4,
            },
            {
              name: '小米8 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '699.00',
              address: '双安店',
              stock: '12,000',
              key: 5,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### max-height.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 设置最大高度
 */
export const MaxHeight = () => {
  const [columns] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      render: (text, row) => {
        console.log(text, row)
        return text + '*'
      },
    },
    {
      title: '品类',
      dataKey: 'type',
    },
    {
      title: '规格',
      dataKey: 'size',
    },
    {
      title: '单价',
      dataKey: 'price',
    },
    {
      title: '门店',
      dataKey: 'address',
    },
    {
      title: '库存',
      dataKey: 'stock',
    },
  ])

  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 6,
    },
    {
      name: 'Redmi Note10',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 7,
    },
    {
      name: '小米11',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 8,
    },
  ])

  return (
    <>
      <h1>MaxHeight for Table</h1>
      <div className="table-max-height__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table
          columns={columns}
          data={data}
          // maxHeight={300}
          maxHeight={'calc(100vh - 80vh)'}
        />
      </div>
    </>
  )
}

```

### merged-cell.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 合并单元格
 */
export const MergedCell = () => {
  return (
    <>
      <h1>MergedCell for Table</h1>
      <div className="table-merged-cell__wrap" style={{ minWidth: 660 }}>
        <Table
          striped
          columns={[
            {
              title: 'Name',
              dataKey: 'name',
              width: 150,
              render: (text, row, index) => {
                return {
                  children: <span>{text}</span>,
                  props: {
                    // 自定义单元格列合并
                    colSpan: index === 4 ? 4 : undefined,
                  },
                }
              },
            },
            {
              title: 'Age',
              dataKey: 'age',
              width: 150,
              render: (value, row, index) => {
                return {
                  children: value,
                  props: {
                    // 自定义单元格行合并（第 2 ~ 3 行）
                    rowSpan: index === 1 ? 2 : index === 2 ? 0 : undefined,
                    // 自定义单元格列合并（第 4 行）
                    colSpan: index === 4 ? 0 : undefined,
                  },
                }
              },
            },
            {
              title: 'Home phone',
              dataKey: 'tel',
              render: (value, row, index) => {
                return {
                  children: value,
                  props: {
                    colSpan: index === 4 ? 0 : undefined,
                  },
                }
              },
            },
            {
              title: 'Address',
              dataKey: 'address',
              render: (value, row, index) => {
                return {
                  children: value,
                  props: {
                    colSpan: index === 4 ? 0 : undefined,
                  },
                }
              },
            },
          ]}
          data={[
            {
              key: '1',
              name: 'John Brown',
              age: 32,
              tel: '0571-22098909',
              address: 'New York No. 1 Lake Park',
            },
            {
              key: '2',
              name: 'Jim Green',
              tel: '0571-22098333',
              age: 42,
              address: 'London No. 1 Lake Park',
            },
            {
              key: '3',
              name: 'Joe Black',
              age: 32,
              tel: '0575-22098909',
              address: 'Sidney No. 1 Lake Park',
            },
            {
              key: '4',
              name: 'Jim Red',
              age: 18,
              tel: '0575-22098909',
              address: 'London No. 2 Lake Park',
            },
            {
              key: '5',
              name: 'Jake White',
              age: 18,
              tel: '0575-22098909',
              address: 'Dublin No. 2 Lake Park',
            },
          ]}
        />
      </div>
    </>
  )
}

```

### on-load-children.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 异步加载 children
 */
export const OnLoadChildren = () => {
  const [columns] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 240,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])

  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '13,000',
      key: 5,
    },
  ])

  return (
    <>
      <h1>OnLoadChildren for Table</h1>
      <div className="table-basic__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table
          columns={columns}
          data={data}
          fieldKey="stock"
          onLoadChildren={(item) => {
            const { depth } = item
            console.log('item', item)
            return new Promise((resolve) => {
              setTimeout(() => {
                // 模拟无子节点情况处理
                if (depth > 0) {
                  resolve([])
                } else {
                  const children = [
                    {
                      name: '小米10',
                      type: '手机',
                      size: '6G+64G',
                      price: '3299.00',
                      address: '华润五彩城店',
                      stock: '100',
                      key: new Date().getTime(),
                    },
                    {
                      name: '小米11',
                      type: '手机',
                      size: '6G+64G',
                      price: '3299.00',
                      address: '华润五彩城店',
                      stock: '200',
                      key: new Date().getTime() + 1,
                    },
                  ]
                  resolve(children)
                }
              }, 1000)
            })
          }}
        />
      </div>
    </>
  )
}

```

### pagination.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 表格分页
 */
export const Pagination = () => {
  const [columns] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
    },
    {
      title: '规格',
      dataKey: 'size',
    },
    {
      title: '单价',
      dataKey: 'price',
    },
    {
      title: '门店',
      dataKey: 'address',
    },
    {
      title: '库存',
      dataKey: 'stock',
    },
  ])

  const [dataSource] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
    {
      name: '小米10',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 6,
    },
    {
      name: '小米10 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 7,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 8,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 9,
    },
    // {
    //   name: '小米8 SE',
    //   type: '手机',
    //   size: '6G+64G 幻彩蓝',
    //   price: '699.00',
    //   address: '双安店',
    //   stock: '12,000',
    //   key: 10,
    // },
  ])

  const [paginationState, setPaginationState] = React.useState({
    current: 1,
    data: dataSource.slice(0, 5),
    pageSize: 5,
  })

  console.log('paginationState', paginationState)

  return (
    <>
      <h1>Pagination for Table</h1>
      <div className="table-pagination__wrap" style={{ minWidth: 660 }}>
        <Table
          pagination={{
            showTotal: true,
            showJumper: true,
            pageSize: paginationState.pageSize,
            pageSizeOptions: [5, 10, 20],
            pageSizeOptionsOverlay: {
              // 该参数用来配置分页器下拉框的挂载容器，默认是 body，设置为 true 时，会自动寻找最近的元素作为父节点
              // 在浏览器原生的全屏模式中，需要将此值设成 true，否则无法正常显示，若无需在全屏状态下使用，则不需要做任何处理
              disabledPortal: true,
            },
            onPageSizeChange: (pageSize) => {
              setPaginationState((prev) => ({
                ...prev,
                pageSize,
              }))
            },
            total: dataSource.length,
            current: paginationState.current,
            onChange: (page, pre, size = 5) => {
              console.log('onPaginationChange', page, pre, size)

              setPaginationState((prev) => ({
                ...prev,
                current: page,
                data: dataSource.slice(size * (page - 1), size * page),
              }))
            },
          }}
          columns={columns}
          data={paginationState.data}
        />
      </div>
    </>
  )
}

```

### resizable.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'
import EllipsisTooltip from '@hi-ui/ellipsis-tooltip'

/**
 * @title 可调节列宽
 */
export const Resizable = () => {
  return (
    <>
      <h1>Resizable for Table</h1>
      <div className="table-resizable__wrap" style={{ minWidth: 660 }}>
        <Table
          fixedToColumn={{ left: 'type', right: 'address' }}
          resizable
          onResizeStop={(e, data, index, columnsWidth) => {
            console.log('onResizeStop', e, data, index, columnsWidth)
          }}
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
              width: 120,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '品类',
              dataKey: 'type',
              width: 80,
            },
            {
              title: '规格',
              dataKey: 'size',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '单价',
              dataKey: 'price',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '规格',
              dataKey: 'size',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '单价',
              dataKey: 'price',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '规格',
              dataKey: 'size',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '单价',
              dataKey: 'price',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '规格',
              dataKey: 'size',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '单价',
              dataKey: 'price',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '规格',
              dataKey: 'size',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '单价',
              dataKey: 'price',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },

            {
              title: '规格',
              dataKey: 'size',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '单价',
              dataKey: 'price',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '规格',
              dataKey: 'size',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '单价',
              dataKey: 'price',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },

            {
              title: '规格',
              dataKey: 'size',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '单价',
              dataKey: 'price',
              width: 150,
              render(text) {
                return <EllipsisTooltip>{text}</EllipsisTooltip>
              },
            },
            {
              title: '门店',
              dataKey: 'address',
              width: 150,
            },
            {
              title: '库存',
              dataKey: 'stock',
              width: 150,
            },
          ]}
          data={[
            {
              name: '小米9',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '3299.00',
              address: '华润五彩城店',
              stock: '29,000',
              key: 1,
            },
            {
              name: '小米9 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '1999.00',
              address: '清河店',
              stock: '10,000',
              key: 2,
            },
            {
              name: '小米8',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '2599.00',
              address: '双安店',
              stock: '12,000',
              key: 3,
            },
            {
              name: 'Redmi Note7',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '999.00',
              address: '华润五彩城店',
              stock: '140,000',
              key: 4,
            },
            {
              name: '小米8 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '699.00',
              address: '双安店',
              stock: '12,000',
              key: 5,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### row-class-name.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 设置表格行和单元格类名
 * @desc 用于自定义行和单元格的个性化样式
 */
export const RowClassName = () => {
  // 实际使用中可以直接将样式写在样式文件中，不必这样动态创建style标签，此处只是做示例展示
  React.useLayoutEffect(() => {
    const head = document.getElementsByTagName('head')[0]
    const style = document.createElement('style')
    style.appendChild(
      document.createTextNode(`
        .table-row--price-normal .hi-v4-table-cell {
          background: #e5feeb;
        }
        .table-row--price-warning .hi-v4-table-cell {
          background: #fefae0;
        }
        .hi-v4-table-row .table-cell--stock-danger {
          background: #fee9e5;
        }
      `)
    )
    head.appendChild(style)
  }, [])

  return (
    <>
      <h1>RowClassName for Table</h1>
      <div className="table-row-class-name__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table
          rowClassName={(record, index) => {
            const { price } = record.raw
            if (price > 2000) {
              return 'table-row--price-warning'
            }
            return 'table-row--price-normal'
          }}
          cellClassName={(record, column, index) => {
            if (column.raw.dataKey === 'stock' && record.raw.stock <= 10000) {
              return 'table-cell--stock-danger'
            }
            return ''
          }}
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
              render: (text, row) => {
                console.log(text, row)
                return text + '*'
              },
            },
            {
              title: '品类',
              dataKey: 'type',
            },
            {
              title: '规格',
              dataKey: 'size',
            },
            {
              title: '单价',
              dataKey: 'price',
            },
            {
              title: '门店',
              dataKey: 'address',
            },
            {
              title: '库存',
              dataKey: 'stock',
            },
          ]}
          data={[
            {
              name: '小米9',
              type: '手机',
              size: '6G+64G',
              price: '3299.00',
              address: '华润五彩城店',
              stock: '29000',
              key: 1,
            },
            {
              name: '小米9 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '1999.00',
              address: '清河店',
              stock: '10000',
              key: 2,
            },
            {
              name: '小米8',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '2599.00',
              address: '双安店',
              stock: '12000',
              key: 3,
            },
            {
              name: 'Redmi Note7',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '999.00',
              address: '华润五彩城店',
              stock: '140000',
              key: 4,
            },
            {
              name: '小米8 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '699.00',
              address: '双安店',
              stock: '12000',
              key: 5,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### row-selection.stories.tsx

```typescript
import React from 'react'
import { RadioGroup } from '@hi-ui/radio'
import Table from '@hi-ui/table'

/**
 * @title 行选中
 * @desc 通过 rowSelection.type 属性来设置单选或多选，默认为 <code>checkbox</code>
 */
export const RowSelection = () => {
  const [columns] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 240,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])
  const [dataSource] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
    {
      name: '小米10',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 6,
    },
    {
      name: '小米10 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 7,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 8,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 9,
    },
    // {
    //   name: '小米8 SE',
    //   type: '手机',
    //   size: '6G+64G 幻彩蓝',
    //   price: '699.00',
    //   address: '双安店',
    //   stock: '12,000',
    //   key: 10,
    // },
  ])

  const [paginationState, setPaginationState] = React.useState({
    current: 1,
    data: dataSource.slice(0, 5),
    pageSize: 5,
  })

  const [selectedRowKeys, setSelectedRowKeys] = React.useState<any>([])
  const [type, setType] = React.useState<'checkbox' | 'radio'>('checkbox')

  React.useEffect(() => {
    if (type === 'radio' && selectedRowKeys.length > 1) {
      setSelectedRowKeys([selectedRowKeys[0]])
    }
  }, [selectedRowKeys, type])

  return (
    <>
      <h1>RowSelection for Table</h1>
      <div className="table-row-selection__wrap" style={{ minWidth: 660 }}>
        <RadioGroup
          defaultValue={'checkbox'}
          type={'button'}
          data={[
            { title: '多选', id: 'checkbox' },
            { title: '单选', id: 'radio' },
          ]}
          onChange={(value) => {
            console.log('onChange', value)
            setType(value as 'checkbox' | 'radio')
          }}
          style={{ marginBottom: 16 }}
        />
        <Table
          fixedToColumn={{ left: 'type' }}
          rowSelection={{
            type,
            selectedRowKeys,
            onChange: (keys, target, shouldChecked, rows) => {
              console.log(keys, target, shouldChecked, rows)

              setSelectedRowKeys(keys)
            },
          }}
          pagination={{
            showTotal: true,
            showJumper: true,
            pageSize: paginationState.pageSize,
            pageSizeOptions: [5, 10, 20],
            onPageSizeChange: (pageSize) => {
              setPaginationState((prev) => ({
                ...prev,
                pageSize,
              }))
            },
            total: dataSource.length,
            current: paginationState.current,
            onChange: (page, pre, size = 5) => {
              console.log('onPaginationChange', page, pre, size)

              setPaginationState((prev) => ({
                ...prev,
                current: page,
                data: dataSource.slice(size * (page - 1), size * page),
              }))
            },
          }}
          columns={columns}
          data={paginationState.data}
        />
      </div>
    </>
  )
}

```

### scrollbar.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 设置滚动条
 * @desc 解决Windows环境下滚动条样式不美观问题
 */
export const Scrollbar = () => {
  const [column] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
      fixed: true,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size1',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price1',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size2',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price2',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size3',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price3',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size4',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price4',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size5',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price5',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size6',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price6',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size7',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price7',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 150,
      fixed: true,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])
  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      price1: '3299.00',
      price2: '3299.00',
      price3: '3299.00',
      price4: '3299.00',
      price5: '3299.00',
      price6: '3299.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      price1: '1999.00',
      price2: '1999.00',
      price3: '1999.00',
      price4: '1999.00',
      price5: '1999.00',
      price6: '1999.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      price1: '2599.00',
      price2: '2599.00',
      price3: '2599.00',
      price4: '2599.00',
      price5: '2599.00',
      price6: '2599.00',
      price7: '2599.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      price1: '999.00',
      price2: '999.00',
      price3: '999.00',
      price4: '999.00',
      price5: '999.00',
      price6: '999.00',
      price7: '999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 6,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 7,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 8,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 9,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 10,
    },
  ])

  const scrollbarInnerRef = React.useRef<any>(null)
  const update = () => scrollbarInnerRef.current?.update?.()

  // 在外部滚动时更新 Scrollbar 滚动条的位置
  // 该处理是针对 scrollbarXStickToBottom 参数为 true 的情况，让滚动条始终保持在底部，详见 Scrollbar 组件文档
  React.useEffect(() => {
    document.addEventListener('scroll', update)

    return () => {
      document.removeEventListener('scroll', update)
    }
  }, [])

  return (
    <>
      <h1>Scrollbar for Table</h1>
      <div className="table-scrollbar__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table
          fixedToColumn={{ left: 'type', right: 'address' }}
          columns={column}
          data={data}
          maxHeight={300}
          scrollbar={
            // 根据需要进行以下配置
            {
              // 保持滚动条始终可见
              keepVisible: true,
              innerRef: scrollbarInnerRef,
              // 设置滚动条的 z-index 值
              zIndex: 9,
              settings: {
                // 垂直滑动时，让横向滚动条一直显示在容器底部
                scrollbarXStickToBottom: true,
                // 横向滚动条距离底部的距离
                scrollbarXStickToBottomGap: 20,
              },
            }
          }
        />
      </div>
    </>
  )
}

```

### setting-drawer-check-all.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Table, { SettingDrawer } from '@hi-ui/table'

/**
 * @title 设置抽屉-全选
 */
export const SettingDrawerCheckAll = () => {
  const [dataSource] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])

  const columnsMemo = React.useMemo(() => {
    return [
      {
        title: '商品名',
        dataKey: 'name',
        width: 150,
      },
      {
        title: '品类',
        dataKey: 'type',
        width: 150,
      },
      {
        title: '规格',
        dataKey: 'size',
        width: 150,
      },
      {
        title: '单价',
        dataKey: 'price',
        width: 150,
      },
      {
        title: '门店',
        dataKey: 'address',
        width: 150,
      },
      {
        title: '库存',
        dataKey: 'stock',
        width: 150,
      },
    ]
  }, [])

  const [columns, setColumns] = React.useState(columnsMemo)
  const [hiddenColKeys, setHiddenColKeys] = React.useState<string[]>(['price'])
  const [sortedColKeys, setSortColKeys] = React.useState<string[]>()

  const onSetColKeysChange = (
    sortedColKeys: string[],
    hiddenColKeys: string[],
    newColumns: any[]
  ) => {
    console.log('onColKeysChange', { sortedColKeys, hiddenColKeys, newColumns })

    setSortColKeys(sortedColKeys)
    setHiddenColKeys(hiddenColKeys)
    setColumns(newColumns)
  }

  const [visible, setVisible] = React.useState<boolean>(false)

  return (
    <>
      <h1>Check All for Table Setting Drawer</h1>
      <div className="table-setting-drawer-check-all__wrap" style={{ minWidth: 660 }}>
        <div style={{ marginBottom: '1em' }}>
          <Button onClick={() => setVisible(true)}>列设置抽屉</Button>
        </div>
        <Table columns={columns} data={dataSource} />
        <SettingDrawer
          visible={visible}
          showCheckAll
          onClose={() => setVisible(false)}
          drawerProps={{ width: 400, title: '表格字段设置' }}
          columns={columnsMemo}
          checkDisabledColKeys={['name', 'type']}
          // 禁用拖拽的列
          dragDisabledColKeys={['name', 'type']}
          hiddenColKeys={hiddenColKeys}
          sortedColKeys={sortedColKeys}
          onSetColKeysChange={onSetColKeysChange}
        />
      </div>
    </>
  )
}

```

### setting-drawer-extra-header.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Search from '@hi-ui/search'
import { SearchOutlined } from '@hi-ui/icons'
import Highlighter from '@hi-ui/highlighter'
import Table, { SettingDrawer, TableColumnItem } from '@hi-ui/table'

/**
 * @title 设置抽屉-扩展头部内容
 */
export const SettingDrawerExtraHeader = () => {
  const [dataSource] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',

      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])
  const [originColumns] = React.useState<TableColumnItem[]>([
    {
      title: '商品名',
      dataKey: 'name',
      width: 150,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 150,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])
  const [columns, setColumns] = React.useState<TableColumnItem[]>(originColumns)
  const [disabledColumns] = React.useState<string[]>(['name', 'type'])
  const [searchKey, setSearchKey] = React.useState<string>('')
  const [hiddenColKeys, setHiddenColKeys] = React.useState<string[]>(['price'])
  const [sortedColKeys, setSortColKeys] = React.useState<string[]>()
  const [visible, setVisible] = React.useState<boolean>(false)

  const settingColumnsMemo = React.useMemo(() => {
    return [...originColumns]
    // searchKey 作为依赖项，目的是搜索结果改变时重新渲染设置项，让关键字高亮
  }, [originColumns, searchKey])

  const onSetColKeysChange = (
    sortedColKeys: string[],
    hiddenColKeys: string[],
    newColumns: TableColumnItem[]
  ) => {
    console.log('onColKeysChange', { sortedColKeys, hiddenColKeys, newColumns })

    setSortColKeys(sortedColKeys)
    setHiddenColKeys(hiddenColKeys)
    setColumns(newColumns)
  }

  return (
    <>
      <h1>Extra Header for Table Setting Drawer</h1>
      <div className="table-setting-drawer-extra-header__wrap" style={{ minWidth: 660 }}>
        <div style={{ marginBottom: '1em' }}>
          <Button onClick={() => setVisible(true)}>列设置抽屉</Button>
        </div>
        <Table columns={columns} data={dataSource} />
        <SettingDrawer
          visible={visible}
          onClose={() => setVisible(false)}
          drawerProps={{ width: 400, title: '表格字段设置' }}
          columns={settingColumnsMemo}
          // 禁用拖拽的列
          dragDisabledColKeys={settingColumnsMemo.map((d) => d.dataKey!)}
          checkDisabledColKeys={disabledColumns}
          hiddenColKeys={hiddenColKeys}
          sortedColKeys={sortedColKeys}
          onSetColKeysChange={onSetColKeysChange}
          itemRender={(item) => {
            return <Highlighter keyword={searchKey}>{item.title}</Highlighter>
          }}
          extraHeader={
            <div style={{ marginBottom: 16 }}>
              <Search
                prefix={<SearchOutlined />}
                append={null}
                placeholder="搜素"
                onInput={(e) => {
                  const searchKey = (e.target as HTMLInputElement).value
                  setSearchKey(searchKey)
                }}
                onSearch={(key, item) => console.log({ key, item })}
              />
            </div>
          }
        />
      </div>
    </>
  )
}

```

### setting-drawer.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Table, { SettingDrawer } from '@hi-ui/table'

/**
 * @title 设置抽屉
 */
export const TableSettingDrawer = () => {
  const [dataSource] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])

  const columnsMemo = React.useMemo(() => {
    return [
      {
        title: '商品名',
        dataKey: 'name',
        width: 150,
      },
      {
        title: '品类',
        dataKey: 'type',
        width: 150,
      },
      {
        title: '规格',
        dataKey: 'size',
        width: 150,
      },
      {
        title: '单价',
        dataKey: 'price',
        width: 150,
      },
      {
        title: '门店',
        dataKey: 'address',
        width: 150,
      },
      {
        title: '库存',
        dataKey: 'stock',
        width: 150,
      },
    ]
  }, [])

  const [columns, setColumns] = React.useState(columnsMemo)
  const [hiddenColKeys, setHiddenColKeys] = React.useState<string[]>(['price'])
  const [sortedColKeys, setSortColKeys] = React.useState<string[]>()

  const onSetColKeysChange = (
    sortedColKeys: string[],
    hiddenColKeys: string[],
    newColumns: any[]
  ) => {
    console.log('onColKeysChange', { sortedColKeys, hiddenColKeys, newColumns })

    setSortColKeys(sortedColKeys)
    setHiddenColKeys(hiddenColKeys)
    setColumns(newColumns)
  }

  const [visible, setVisible] = React.useState<boolean>(false)

  return (
    <>
      <h1>Setting Drawer for Table</h1>
      <div className="table-setting-drawer__wrap" style={{ minWidth: 660 }}>
        <div style={{ marginBottom: '1em' }}>
          <Button onClick={() => setVisible(true)}>列设置抽屉</Button>
        </div>
        <Table columns={columns} data={dataSource} />
        <SettingDrawer
          visible={visible}
          onClose={() => setVisible(false)}
          drawerProps={{ width: 400, title: '表格字段设置' }}
          columns={columnsMemo}
          checkDisabledColKeys={['name', 'type']}
          // 禁用拖拽的列
          dragDisabledColKeys={['name', 'type']}
          hiddenColKeys={hiddenColKeys}
          sortedColKeys={sortedColKeys}
          onSetColKeysChange={onSetColKeysChange}
        />
      </div>
    </>
  )
}

```

### setting.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 自定义列控制
 */
export const Setting = () => {
  const [dataSource] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',

      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      size1: '6G+64G 幻彩蓝',
      price1: '3299.00',
      size2: '6G+64G 幻彩蓝',
      price2: '3299.00',
      size3: '6G+64G 幻彩蓝',
      price3: '3299.00',
      size4: '6G+64G 幻彩蓝',
      price4: '3299.00',
      size5: '6G+64G 幻彩蓝',
      price5: '3299.00',
      size6: '6G+64G 幻彩蓝',
      price6: '3299.00',
      size7: '6G+64G 幻彩蓝',
      price7: '3299.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])
  const cacheKey = '_hiuiTableSetStoreKey_'
  const initStoreInfo: any = localStorage.getItem(cacheKey)
    ? JSON.parse(localStorage.getItem(cacheKey))
    : {}
  const [hiddenColKeys, setHiddenColKeys] = React.useState(initStoreInfo.hiddenColKeys)
  const [sortedColKeys, setSortedColKeys] = React.useState(initStoreInfo.sortedColKeys)
  const onSetColKeysChange = (sortedColKeys: string[], hiddenColKeys: string[]) => {
    console.log('onColKeysChange', { sortedColKeys, hiddenColKeys })
    setHiddenColKeys(hiddenColKeys)
    setSortedColKeys(sortedColKeys)
    localStorage.setItem(cacheKey, JSON.stringify({ hiddenColKeys, sortedColKeys }))
  }
  const columnsMemo = React.useMemo(() => {
    return [
      {
        title: '商品名',
        dataKey: 'name',
        width: 150,
      },
      {
        title: '品类',
        dataKey: 'type',
        width: 150,
      },
      {
        title: '规格',
        dataKey: 'size',
        width: 150,
      },
      {
        title: '单价',
        dataKey: 'price',
        width: 150,
      },
      {
        title: '规格1',
        dataKey: 'size1',
        width: 150,
      },
      {
        title: '单价1',
        dataKey: 'price1',
        width: 150,
      },
      {
        title: '规格2',
        dataKey: 'size2',
        width: 150,
      },
      {
        title: '单价2',
        dataKey: 'price2',
        width: 150,
      },
      {
        title: '规格3',
        dataKey: 'size3',
        width: 150,
      },
      {
        title: '单价3',
        dataKey: 'price3',
        width: 150,
      },
      {
        title: '规格4',
        dataKey: 'size4',
        width: 150,
      },
      {
        title: '单价4',
        dataKey: 'price4',
        width: 150,
      },
      {
        title: '规格5',
        dataKey: 'size5',
        width: 150,
      },
      {
        title: '单价5',
        dataKey: 'price5',
        width: 150,
      },
      {
        title: '规格6',
        dataKey: 'size6',
        width: 150,
      },
      {
        title: '单价6',
        dataKey: 'price6',
        width: 150,
      },

      {
        title: '规格7',
        dataKey: 'size7',
        width: 150,
      },
      {
        title: '单价7',
        dataKey: 'price7',
        width: 150,
      },
      {
        title: '门店',
        dataKey: 'address',
        width: 150,
      },
      {
        title: '库存',
        dataKey: 'stock',
        width: 150,
      },
    ]
  }, [])

  return (
    <>
      <h1>Setting for Table</h1>
      <div className="table-setting__wrap" style={{ minWidth: 660 }}>
        <Table
          hiddenColKeys={hiddenColKeys}
          sortedColKeys={sortedColKeys}
          onSetColKeysChange={onSetColKeysChange}
          checkDisabledColKeys={['name', 'type']}
          columns={columnsMemo}
          data={dataSource}
          setting
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  const [column] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size1',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price1',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size2',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price2',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size3',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price3',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size4',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price4',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size5',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price5',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size6',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price6',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size7',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price7',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 150,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])
  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      price1: '3299.00',
      price2: '3299.00',
      price3: '3299.00',
      price4: '3299.00',
      price5: '3299.00',
      price6: '3299.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      price1: '1999.00',
      price2: '1999.00',
      price3: '1999.00',
      price4: '1999.00',
      price5: '1999.00',
      price6: '1999.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      price1: '2599.00',
      price2: '2599.00',
      price3: '2599.00',
      price4: '2599.00',
      price5: '2599.00',
      price6: '2599.00',
      price7: '2599.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      price1: '999.00',
      price2: '999.00',
      price3: '999.00',
      price4: '999.00',
      price5: '999.00',
      price6: '999.00',
      price7: '999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])

  return (
    <>
      <h1>Size for Table</h1>
      <div className="table-size__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table bordered columns={column} data={data} size="sm" rowSelection={{}} />
        <br />
        <br />
        <Table bordered columns={column} data={data} size="md" rowSelection={{}} />
        <br />
        <br />
        <Table bordered columns={column} data={data} size="lg" rowSelection={{}} />
      </div>
    </>
  )
}

```

### sticky-footer.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 表脚底部
 */
export const StickyFooter = () => {
  const [columns] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
    },
    {
      title: '品类',
      dataKey: 'type',
    },
    {
      title: '规格',
      dataKey: 'size',
    },
    {
      title: '单价',
      dataKey: 'price',
    },
    {
      title: '门店',
      dataKey: 'address',
    },
    {
      title: '库存',
      dataKey: 'stock',
    },
  ])
  const [dataSource] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
    {
      name: '小米10',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      address: '华润五彩城店',
      stock: '29,000',
      key: 6,
    },
    {
      name: '小米10 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      address: '清河店',
      stock: '10,000',
      key: 7,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      address: '双安店',
      stock: '12,000',
      key: 8,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      address: '华润五彩城店',
      stock: '140,000',
      key: 9,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      address: '双安店',
      stock: '12,000',
      key: 10,
    },
  ])

  const [paginationState, setPaginationState] = React.useState({
    current: 0,
    data: dataSource.slice(0, 5),
  })

  console.log('paginationState', paginationState)

  return (
    <>
      <h1>StickyFooter for Table</h1>
      <div className="table-sticky-footer__wrap" style={{ minWidth: 660 }}>
        <Table
          stickyFooter
          maxHeight={200}
          pagination={{
            showTotal: true,
            showJumper: true,
            pageSize: 5,
            total: dataSource.length,
            current: paginationState.current,
            onChange: (page, pre, size = 5) => {
              console.log('onPaginationChange', page, pre, size)

              setPaginationState({
                current: page,
                data: dataSource.slice(size * (page - 1), size * page),
              })
            },
          }}
          columns={columns}
          data={paginationState.data}
        />
      </div>
    </>
  )
}

```

### sticky-header.stories.tsx

```typescript
import React from 'react'
import Table, { TableColumnItem } from '@hi-ui/table'

/**
 * @title 表头吸顶
 */
export const StickyHeader = () => {
  const [columns] = React.useState<TableColumnItem[]>([
    {
      title: 'Name',
      dataKey: 'name',
      width: 100,
    },
    {
      title: 'Other',
      dataKey: 'other',
      children: [
        {
          title: 'Age',
          dataKey: 'age',
          width: 100,
        },
        {
          title: 'Address',
          dataKey: 'address',
          children: [
            {
              title: 'Street',
              dataKey: 'street',
              width: 100,
            },
            {
              title: 'Block',
              dataKey: 'block',
              children: [
                {
                  title: 'Building',
                  dataKey: 'building',
                  width: 100,
                },
                {
                  title: 'Door No.',
                  dataKey: 'number',
                  width: 100,
                },
              ],
            },
          ],
        },
      ],
    },
    {
      title: 'Name2',
      dataKey: 'name2',
      width: 100,
    },
    {
      title: 'Name3',
      dataKey: 'name3',
      width: 100,
    },
    {
      title: 'Name4',
      dataKey: 'name4',
      width: 100,
    },
    {
      title: 'Name5',
      dataKey: 'name5',
      width: 100,
    },
    {
      title: 'Name6',
      dataKey: 'name6',
      width: 100,
    },
    {
      title: 'Name7',
      dataKey: 'name7',
      width: 100,
    },
    {
      title: 'Name8',
      dataKey: 'name8',
      width: 100,
    },
    {
      title: 'Name9',
      dataKey: 'name9',
      width: 100,
    },
    {
      title: 'Name10',
      dataKey: 'name10',
      width: 100,
    },
    {
      title: 'Company',
      dataKey: 'company',
      children: [
        {
          title: 'Address',
          dataKey: 'companyAddress',
          width: 200,
        },
        {
          title: 'Name',
          dataKey: 'companyName',
          width: 150,
        },
      ],
    },
    {
      title: 'Name11',
      dataKey: 'name11',
      width: 100,
    },
    {
      title: 'Name12',
      dataKey: 'name12',
      width: 100,
    },
    {
      title: 'Name13',
      dataKey: 'name13',
      width: 100,
    },
    {
      title: 'Name14',
      dataKey: 'name14',
      width: 100,
    },
    {
      title: 'Gender',
      dataKey: 'gender',
      width: 100,
    },
  ])

  const [data] = React.useState(() => {
    const data: any[] = []
    for (let i = 0; i < 6; i++) {
      const item = {
        key: i + 1,
        age: i + 1,
        street: 'Lake Park',
        building: 'C',
        number: 2035,
        name: 'Flcwl',
        companyAddress: 'Lake Street 42',
        companyName: 'SoftLake Co',
        gender: 'M',
      }

      for (let j = 2; j <= 14; j++) {
        item[`name${j}`] = `name${j}`
      }

      data.push(item)
    }

    return data
  })

  return (
    <>
      <h1>StickyHeader for Table</h1>
      <div
        className="table-sticky-header__wrap"
        style={{ minWidth: 660, maxHeight: 800, overflow: 'scroll' }}
      >
        <Table
          sticky
          stickyTop={0}
          fixedToColumn={{
            // left: 'building',
            // left: 'address',
            left: 'number',
            right: 'gender',
            // right: 'companyName',
            // right: 'companyAddress',
          }}
          columns={columns}
          data={data}
        />
        <div style={{ height: 600, paddingTop: 48, textAlign: 'center' }}>模拟外层滚动</div>
      </div>
    </>
  )
}

```

### striped.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 斑马纹
 */
export const Striped = () => {
  return (
    <>
      <h1>Striped for Table</h1>
      <div className="table-striped__wrap" style={{ minWidth: 660 }}>
        <Table
          striped
          columns={[
            {
              title: '商品名',
              dataKey: 'name',
            },
            {
              title: '品类',
              dataKey: 'type',
            },
            {
              title: '规格',
              dataKey: 'size',
            },
            {
              title: '单价',
              dataKey: 'price',
            },
            {
              title: '门店',
              dataKey: 'address',
            },
            {
              title: '库存',
              dataKey: 'stock',
            },
          ]}
          // rowSelection={{ selectedRowKeys: [] }}
          data={[
            {
              name: '小米9',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '3299.00',
              address: '华润五彩城店',
              stock: '29,000',
              key: 1,
            },
            {
              name: '小米9 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '1999.00',
              address: '清河店',
              stock: '10,000',
              key: 2,
            },
            {
              name: '小米8',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '2599.00',
              address: '双安店',
              stock: '12,000',
              key: 3,
            },
            {
              name: 'Redmi Note7',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '999.00',
              address: '华润五彩城店',
              stock: '140,000',
              key: 4,
            },
            {
              name: '小米8 SE',
              type: '手机',
              size: '6G+64G 幻彩蓝',
              price: '699.00',
              address: '双安店',
              stock: '12,000',
              key: 5,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### table-tree.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 树形表格
 */
export const TableTree = () => {
  return (
    <>
      <h1>TableTree for Table</h1>
      <div className="table-TableTree__wrap" style={{ minWidth: 660 }}>
        <Table
          // striped
          // fixedToColumn={'a'}
          // expandedRowKeys={[1]}
          // rowSelection={{}}
          // expandedRender={(row, index) => {
          //   return <div>12313</div>
          // }}
          // maxHeight={'calc(100vh - 900px)'}
          columns={[
            {
              title: 'A',
              dataKey: 'a',
              sorter(pre, next) {
                return pre.raw.b - next.raw.b
              },
            },
            { title: 'B', dataKey: 'b' },
            { title: 'C', dataKey: 'c' },
            { title: 'D', dataKey: 'd' },
          ]}
          data={[
            { a: 'a-4', b: '4', c: 'c-4', d: 'd-4', key: 4 },
            {
              a: 'a-3',
              b: '3',
              c: 'c-3',
              d: 'd-3',
              key: 3,
              children: [
                {
                  a: 'a-3-2',
                  b: '32',
                  c: 'c-3-2',
                  d: 'd-3-2',
                  key: 32,
                },
                {
                  a: 'a-3-1',
                  b: '31',
                  c: 'c-3-1',
                  d: 'd-3-1',
                  key: 31,
                },
              ],
            },
            {
              a: 'a-1',
              b: '1',
              c: 'c-1',
              d: 'd-1',
              key: 1,
              children: [
                { a: 'a-1-3', b: '13', c: 'c-1-3', d: 'd-1-3', key: 13 },
                {
                  a: 'a-1-1',
                  b: '11',
                  c: 'c-1-1',
                  d: 'd-1-1',
                  key: 11,
                  children: [
                    {
                      a: 'a-1-1-1',
                      b: '111',
                      c: 'c-1-1-1',
                      d: 'd-1-1-1d-1-1-1d-1-1-1d-1-1-1',
                      key: 111,
                    },
                    {
                      a: 'a-1-1-3',
                      b: '113',
                      c: 'c-1-1-3',
                      d: 'd-1-1-1d-1-1-1d-1-1-1d-1-1-3',
                      key: 113,
                    },
                    {
                      a: 'a-1-1-2',
                      b: '112',
                      c: 'c-1-1-2',
                      d: 'd-1-1-1d-1-1-1d-1-1-1d-1-1-2',
                      key: 112,
                    },
                  ],
                },
                { a: 'a-1-2', b: '12', c: 'c-1-2', d: 'd-1-2', key: 12 },
              ],
            },

            { a: 'a-2', b: '2', c: 'c-2', d: 'd-2', key: 2 },
          ]}
        />
      </div>
    </>
  )
}

```

### virtual.stories.tsx

```typescript
import React from 'react'
import Table, { TableHelper } from '@hi-ui/table'
import Button from '@hi-ui/button'
/**
 * @title 虚拟列表
 */
export const Virtual = () => {
  const MockData: any = []
  for (let index = 0; index < 10000; index++) {
    MockData.push({
      name: '小米-' + index,
      type: '手机',
      size:
        '6G+64G 幻彩蓝' +
        (index % 10 === 0 ? 'f地方对了时间放的书法大师到了撒娇发了多少解封了的' : ''),
      price: '3299.00',
      operation: '查看',
    })
  }
  const [column] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 300,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 200,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '操作',
      dataKey: 'operation',
      width: 150,
    },
  ])
  const [data] = React.useState(MockData)
  const tableRef = React.useRef<TableHelper>(null)

  return (
    <>
      <h1>Virtual for Table</h1>
      <div className="table-virtual__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <div style={{ marginBottom: '1em' }}>
          <Button
            onClick={() => {
              // key 为节点 id
              tableRef.current?.scrollTo?.({ key: '小米-1000', align: 'top' })
            }}
          >
            scroll to key: 小米-1000
          </Button>
        </div>
        <Table
          fieldKey="name"
          columns={column}
          data={data}
          virtual={true}
          innerRef={tableRef}
          // virtual={{
          //   onVisibleChange(...args) {
          //     console.log('onVisibleChange', ...args)
          //   },
          // }}
          fixedToColumn={{ right: 'operation' }}
        />
      </div>
    </>
  )
}

```

### width.stories.tsx

```typescript
import React from 'react'
import Table from '@hi-ui/table'

/**
 * @title 自定义列宽
 */
export const Width = () => {
  const [column] = React.useState([
    {
      title: '商品名',
      dataKey: 'name',
      width: 120,
    },
    {
      title: '品类',
      dataKey: 'type',
      width: 80,
    },
    {
      title: '规格',
      dataKey: 'size',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size1',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price1',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size2',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price2',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size3',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price3',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size4',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price4',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size5',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price5',
      width: 150,
    },
    {
      title: '规格',
      dataKey: 'size6',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price6',
      width: 150,
    },

    {
      title: '规格',
      dataKey: 'size7',
      width: 150,
    },
    {
      title: '单价',
      dataKey: 'price7',
      width: 150,
    },
    {
      title: '门店',
      dataKey: 'address',
      width: 150,
    },
    {
      title: '库存',
      dataKey: 'stock',
      width: 150,
    },
  ])
  const [data] = React.useState([
    {
      name: '小米9',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '3299.00',
      price1: '3299.00',
      price2: '3299.00',
      price3: '3299.00',
      price4: '3299.00',
      price5: '3299.00',
      price6: '3299.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '29,000',
      key: 1,
    },
    {
      name: '小米9 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '1999.00',
      price1: '1999.00',
      price2: '1999.00',
      price3: '1999.00',
      price4: '1999.00',
      price5: '1999.00',
      price6: '1999.00',
      price7: '1999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '清河店',
      stock: '10,000',
      key: 2,
    },
    {
      name: '小米8',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '2599.00',
      price1: '2599.00',
      price2: '2599.00',
      price3: '2599.00',
      price4: '2599.00',
      price5: '2599.00',
      price6: '2599.00',
      price7: '2599.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 3,
    },
    {
      name: 'Redmi Note7',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '999.00',
      price1: '999.00',
      price2: '999.00',
      price3: '999.00',
      price4: '999.00',
      price5: '999.00',
      price6: '999.00',
      price7: '999.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '华润五彩城店',
      stock: '140,000',
      key: 4,
    },
    {
      name: '小米8 SE',
      type: '手机',
      size: '6G+64G 幻彩蓝',
      price: '699.00',
      price1: '699.00',
      price2: '699.00',
      price3: '699.00',
      price4: '699.00',
      price5: '699.00',
      price6: '699.00',
      price7: '699.00',
      size1: '6G+64G 幻彩蓝',
      size2: '6G+64G 幻彩蓝',
      size3: '6G+64G 幻彩蓝',
      size4: '6G+64G 幻彩蓝',
      size5: '6G+64G 幻彩蓝',
      size6: '6G+64G 幻彩蓝',
      size7: '6G+64G 幻彩蓝',
      address: '双安店',
      stock: '12,000',
      key: 5,
    },
  ])

  return (
    <>
      <h1>Width for Table</h1>
      <div className="table-width__wrap" style={{ minWidth: 660, background: '#fff' }}>
        <Table columns={column} data={data} />
      </div>
    </>
  )
}

```

## tabs 组件

### basic.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 * @desc 基础标签页
 */
export const Basic = () => {
  const [activeTab, setActiveTab] = React.useState<React.ReactText>('1')

  return (
    <>
      <h1>Basic</h1>
      <div className="tabs-basic__wrap">
        <Button onClick={() => setActiveTab('2')}>更新面板</Button>
        <Tabs style={{ marginTop: 16 }} activeId={activeTab} onChange={setActiveTab}>
          <TabPane tabId="1" tabTitle="Tab 1">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
      </div>
    </>
  )
}

```

### button.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'

/**
 * @title 胶囊样式
 * @desc 可用于页面的按钮式布局样式
 */
export const Button = () => {
  return (
    <>
      <h1>胶囊式</h1>
      <div className="tabs-basic__wrap">
        <Tabs type="button" placement="vertical" style={{ marginBottom: 40 }} draggable>
          <TabPane tabId="1" tabTitle={<div style={{ padding: '0 10px' }}>Tab1</div>}>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle={<div style={{ padding: '0 10px' }}>Tab2</div>}>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle={<div style={{ padding: '0 10px' }}>Tab3</div>}>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
        <Tabs type="button" placement="horizontal" draggable>
          <TabPane tabId="1" tabTitle={<div style={{ padding: '0 10px' }}>Tab1</div>}>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle={<div style={{ padding: '0 10px' }}>Tab2</div>}>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle={<div style={{ padding: '0 10px' }}>Tab3</div>}>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
          <TabPane tabId="4" tabTitle={<div style={{ padding: '0 10px' }}>Tab4</div>}>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 4
            </div>
          </TabPane>
          <TabPane tabId="5" tabTitle={<div style={{ padding: '0 10px' }}>Tab5</div>}>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 5
            </div>
          </TabPane>
        </Tabs>
      </div>
    </>
  )
}

```

### card.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'

/**
 * @title 卡片样式
 * @desc 常用于面板、卡片等局部空间
 */
export const Card = () => {
  return (
    <>
      <h1>Card</h1>
      <div className="tabs-card__wrap" style={{ padding: 20, background: '#f5f7fa' }}>
        <Tabs type="card" placement="vertical" style={{ marginBottom: 40 }}>
          <TabPane tabId="1" tabTitle="Tab 1">
            <div
              style={{
                backgroundColor: '#fff',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2">
            <div
              style={{
                backgroundColor: '#fff',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3">
            <div
              style={{
                backgroundColor: '#fff',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
        <Tabs type="card" placement="horizontal">
          <TabPane tabId="1" tabTitle="Tab 1">
            <div
              style={{
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2">
            <div
              style={{
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3">
            <div
              style={{
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
      </div>
    </>
  )
}

```

### desc.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'

/**
 * @title 带描述
 */
export const Desc = () => {
  return (
    <>
      <h1>带描述</h1>
      <div className="tabs-basic__wrap">
        <Tabs type="desc" placement="vertical" style={{ marginBottom: 40 }}>
          <TabPane tabId="1" tabTitle="Tab 1" tabDesc="关于标签的描述信息">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2" tabDesc="关于标签的描述信息">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3" tabDesc="关于标签的描述信息">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
        <Tabs type="desc" placement="horizontal">
          <TabPane tabId="1" tabTitle="Tab 1" tabDesc="关于标签的描述信息">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2" tabDesc="关于标签的描述信息">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3" tabDesc="关于标签的描述信息">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'
import Button from '@hi-ui/button'

/**
 * @title 禁用状态
 */
export const Disabled = () => {
  const [activeTab, setActiveTab] = React.useState<React.ReactText>('1')

  return (
    <>
      <h1>Disabled</h1>
      <div className="tabs-disabled__wrap">
        <Button onClick={() => setActiveTab('2')}>更新面板</Button>
        <Tabs style={{ marginTop: 16 }} activeId={activeTab} onChange={setActiveTab}>
          <TabPane tabId="1" tabTitle="Tab 1">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2" disabled>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
      </div>
    </>
  )
}

```

### editable.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'

/**
 * @title 可编辑
 * @desc 可以自定义标签的增加和关闭
 */
export const Editable = () => {
  return (
    <>
      <h1>Editable</h1>
      <div className="tabs-editable__wrap">
        <Tabs
          editable
          onAdd={() => {
            console.log('ADD')
          }}
          onDelete={(a, b) => {
            console.log('DEL', a, b)
          }}
        >
          <TabPane tabId="1" tabTitle="Tab 1">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
      </div>
    </>
  )
}

```

### extra.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'
import Button from '@hi-ui/button'

/**
 * @title 额外元素
 */
export const Extra = () => {
  return (
    <>
      <h1>Extra</h1>
      <div className="tabs-extra__wrap">
        <Tabs extra={<Button>申请</Button>}>
          <TabPane tabId="1" tabTitle="Tab 1">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
      </div>
    </>
  )
}

```

### nested.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'

/**
 * @title 嵌套 Tabs
 */
export const Nested = () => {
  return (
    <>
      <h1>Nested</h1>
      <div className="tabs-nested__wrap">
        <Tabs type="button" defaultActiveId={'3'} placement="vertical">
          <TabPane tabId="1" tabTitle="Tab 1">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3">
            <Tabs>
              <TabPane tabId="1" tabTitle="Sub Tab 1">
                <div
                  style={{
                    backgroundColor: '#f5f7fa',
                    textAlign: 'center',
                    padding: 32,
                    color: '#1f2733',
                  }}
                >
                  Content of Tab Panel 1
                </div>
              </TabPane>
              <TabPane tabId="2" tabTitle="Sub Tab 2">
                <div
                  style={{
                    backgroundColor: '#f5f7fa',
                    textAlign: 'center',
                    padding: 32,
                    color: '#1f2733',
                  }}
                >
                  Content of Tab Panel 2
                </div>
              </TabPane>
              <TabPane tabId="3" tabTitle="Sub Tab 3">
                <div
                  style={{
                    backgroundColor: '#f5f7fa',
                    textAlign: 'center',
                    padding: 32,
                    color: '#1f2733',
                  }}
                >
                  Content of Tab Panel 3
                </div>
              </TabPane>
            </Tabs>
          </TabPane>
        </Tabs>
        <br />
        <br />
        <Tabs type="button" defaultActiveId={'3'}>
          <TabPane tabId="1" tabTitle="Tab 1">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3">
            <Tabs placement="vertical">
              <TabPane tabId="1" tabTitle="Sub Tab 1">
                <div
                  style={{
                    backgroundColor: '#f5f7fa',
                    textAlign: 'center',
                    padding: 32,
                    color: '#1f2733',
                  }}
                >
                  Content of Tab Panel 1
                </div>
              </TabPane>
              <TabPane tabId="2" tabTitle="Sub Tab 2">
                <div
                  style={{
                    backgroundColor: '#f5f7fa',
                    textAlign: 'center',
                    padding: 32,
                    color: '#1f2733',
                  }}
                >
                  Content of Tab Panel 2
                </div>
              </TabPane>
              <TabPane tabId="3" tabTitle="Sub Tab 3">
                <div
                  style={{
                    backgroundColor: '#f5f7fa',
                    textAlign: 'center',
                    padding: 32,
                    color: '#1f2733',
                  }}
                >
                  Content of Tab Panel 3
                </div>
              </TabPane>
            </Tabs>
          </TabPane>
        </Tabs>
      </div>
    </>
  )
}

```

### scroll.stories.tsx

```typescript
import React from 'react'
import Tabs from '@hi-ui/tabs'

/**
 * @title 超出滚动
 * @desc 标签数量增多展示滚动条
 */
export const Scroll = () => {
  const [data] = React.useState(() => {
    return Array(48)
      .fill(null)
      .map((_, index) => {
        const num = index + 1
        return {
          id: num,
          title: `Tab ${num}`,
          content: (
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              {`Content of Tab Panel ${num}`}
            </div>
          ),
        }
      })
  })

  return (
    <>
      <h1>Scroll</h1>
      <div className="tabs-scroll__wrap" style={{ maxWidth: 1000 }}>
        <Tabs>
          {data.map((v) => {
            return (
              <Tabs.Pane key={v.id} tabId={v.id} tabTitle={v.title}>
                {v.content}
              </Tabs.Pane>
            )
          })}
        </Tabs>
      </div>
    </>
  )
}

```

### tab-list.stories.tsx

```typescript
import React from 'react'
import { TabList } from '@hi-ui/tabs'

/**
 * @title 单独使用 TabList
 */
export const TabsList = () => {
  return (
    <>
      <h1>单独使用 TabList</h1>
      <div className="tabs-basic__wrap">
        <TabList
          data={[
            { tabId: '0', tabTitle: '角色' },
            { tabId: '1', tabTitle: '数据' },
          ]}
        />
      </div>
    </>
  )
}

```

### unmount-on-inactive.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'

/**
 * @title 不活跃时卸载
 * @desc 标签内容不活跃时默认会卸载，可以通过 `unmountOnInactive` 属性来控制是否卸载
 */
export const UnmountOnInactive = () => {
  const [activeTab, setActiveTab] = React.useState<React.ReactText>('1')

  return (
    <>
      <h1>UnmountOnInactive</h1>
      <div className="tabs-unmount-on-inactive__wrap">
        <Tabs style={{ marginTop: 16 }} activeId={activeTab} onChange={setActiveTab}>
          <TabPane tabId="1" tabTitle="Tab 1" unmountOnInactive={false}>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane tabId="2" tabTitle="Tab 2" unmountOnInactive={false}>
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane tabId="3" tabTitle="Tab 3">
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
      </div>
    </>
  )
}

```

### vertical.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'

/**
 * @title 垂直布局
 */
export const Vertical = () => {
  return (
    <>
      <h1>Vertical</h1>
      <div className="tabs-vertical__wrap" style={{ marginBottom: 16 }}>
        <Tabs placement="vertical" style={{ height: 400 }}>
          {Array(48)
            .fill(undefined)
            .map((_, index) => {
              return (
                <TabPane key={index} tabId={index} tabTitle={`Tab ${index}`}>
                  <div
                    style={{
                      backgroundColor: '#f5f7fa',
                      textAlign: 'center',
                      padding: 32,
                      color: '#1f2733',
                    }}
                  >
                    {`Content of Tab Panel ${index}`}
                  </div>
                </TabPane>
              )
            })}
        </Tabs>
      </div>
    </>
  )
}

```

### with-icon.stories.tsx

```typescript
import React from 'react'
import { Tabs, TabPane } from '@hi-ui/tabs'
import { MailSendOutlined, FireOutlined, StarOutlined } from '@hi-ui/icons'

/**
 * @title 带图标
 */
export const WithIcon = () => {
  return (
    <>
      <h1>带图标</h1>
      <div className="tabs-basic__wrap">
        <Tabs>
          <TabPane
            tabId="1"
            tabTitle={
              <span>
                <MailSendOutlined style={{ marginRight: 4 }} />
                目标
              </span>
            }
          >
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 1
            </div>
          </TabPane>
          <TabPane
            tabId="2"
            tabTitle={
              <span>
                <FireOutlined style={{ marginRight: 4 }} />
                结果
              </span>
            }
          >
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 2
            </div>
          </TabPane>
          <TabPane
            tabId="3"
            tabTitle={
              <span>
                <StarOutlined style={{ marginRight: 4 }} />
                复盘
              </span>
            }
          >
            <div
              style={{
                backgroundColor: '#f5f7fa',
                textAlign: 'center',
                padding: 32,
                color: '#1f2733',
              }}
            >
              Content of Tab Panel 3
            </div>
          </TabPane>
        </Tabs>
      </div>
    </>
  )
}

```

## tag 组件

### appearance.stories.tsx

```typescript
import React from 'react'
import Tag from '@hi-ui/tag'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性、实心三种
 */
export const Appearance = () => {
  return (
    <>
      <h1>Tag Appearance</h1>
      <h2>Filled 面性</h2>
      <div style={{ display: 'flex', gap: 8 }}>
        <Tag type="warning" appearance="filled">
          待审批
        </Tag>
        <Tag type="primary" appearance="filled">
          审批中
        </Tag>
        <Tag type="success" appearance="filled">
          已通过
        </Tag>
        <Tag type="danger" appearance="filled">
          已驳回
        </Tag>
        <Tag type="default" appearance="filled">
          待审批
        </Tag>
      </div>
      <h2>line 线性</h2>
      <div style={{ display: 'flex', gap: '8px' }}>
        <Tag type="warning" appearance={'line'}>
          待审批
        </Tag>
        <Tag type="primary" appearance={'line'}>
          审批中
        </Tag>
        <Tag type="success" appearance={'line'}>
          已通过
        </Tag>
        <Tag type="danger" appearance={'line'}>
          已驳回
        </Tag>
        <Tag type="default" appearance={'line'}>
          待审批
        </Tag>
      </div>
      <h2>solid 实心</h2>
      <div style={{ display: 'flex', gap: 8 }}>
        <Tag type="warning" appearance="solid">
          待审批
        </Tag>
        <Tag type="primary" appearance="solid">
          审批中
        </Tag>
        <Tag type="success" appearance="solid">
          已通过
        </Tag>
        <Tag type="danger" appearance="solid">
          已驳回
        </Tag>
        <Tag type="default" appearance="solid">
          待审批
        </Tag>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Tag from '@hi-ui/tag'

/**
 * @title 基础用法
 * @desc 标签的信息重要级别高，识别度较高
 */
export const Basic = () => {
  return (
    <>
      <h1>Tag Basic</h1>
      <div style={{ display: 'flex', gap: 8 }}>
        <Tag type="warning">待审批</Tag>
        <Tag type="primary">审批中</Tag>
        <Tag type="success">已通过</Tag>
        <Tag type="danger">已驳回</Tag>
        <Tag type="default">待审批</Tag>
      </div>
    </>
  )
}

```

### closeable.stories.tsx

```typescript
import React from 'react'
import Tag from '@hi-ui/tag'

/**
 * @title 可关闭的
 */
export const Closeable = () => {
  return (
    <>
      <h1>Tag Closeable</h1>
      <div style={{ display: 'flex', gap: 8, flexWrap: 'wrap' }}>
        <Tag appearance="filled" type="primary" closeable onDelete={() => console.log('click')}>
          Closeable default
        </Tag>
        <Tag appearance="filled" closeable>
          Closeable default
        </Tag>
        <Tag appearance="solid" type="primary" closeable>
          Closeable solid
        </Tag>
        <Tag appearance="solid" closeable>
          Closeable solid
        </Tag>
      </div>
    </>
  )
}

```

### colors.stories.tsx

```typescript
import React from 'react'
import Tag from '@hi-ui/tag'

/**
 * @title 不同颜色
 */
export const Colors = () => {
  return (
    <>
      <h1>Tag colors</h1>
      <div style={{ display: 'flex', gap: 8 }}>
        <Tag type="warning">待审批</Tag>
        <Tag type="primary">审批中</Tag>
        <Tag type="success">已通过</Tag>
        <Tag type="danger">已驳回</Tag>
        <Tag type="default">待审批</Tag>
      </div>
    </>
  )
}

```

### custom-color.stories.tsx

```typescript
import React from 'react'
import Tag from '@hi-ui/tag'

/**
 * @title 自定义颜色
 * @desc 标签的信息重要级别高，识别度较高
 */
export const CustomColor = () => {
  return (
    <>
      <h1>Tag Custom Color</h1>
      <div style={{ display: 'flex', gap: 8 }}>
        <Tag color="#48D4CF">color #48D4CF</Tag>
        <Tag background="#48D4CF" appearance="solid">
          background #48D4CF
        </Tag>
      </div>
    </>
  )
}

```

### editable.stories.tsx

```typescript
import { SunFilled } from '@hi-ui/icons'
import React from 'react'
import Tag from '@hi-ui/tag'

/**
 * @title 可编辑的
 */
export const Editable = () => {
  const [testValue1, setTestValue1] = React.useState('test-value')
  const [testValue2, setTestValue2] = React.useState('test-value')

  return (
    <>
      <h1>Tag Editable</h1>
      <div style={{ display: 'flex', gap: 8, flexWrap: 'wrap' }}>
        <Tag editable onEdit={setTestValue1} type={'primary'}>
          {testValue1}
        </Tag>
        <Tag appearance={'solid'} editable onEdit={setTestValue2} type={'primary'}>
          {testValue2}
        </Tag>

        <Tag
          type={'primary'}
          render={(children) => (
            <span>
              <SunFilled style={{ marginRight: '2px' }} />
              {children}
            </span>
          )}
          maxWidth={240}
          editable
        >
          Test Content Max Length Placeholder Max Length Placeholder
        </Tag>
      </div>
    </>
  )
}

```

### editor-render.stories.tsx

```typescript
import React, { useState } from 'react'
import Tag, { TagGroupDataItem } from '@hi-ui/tag'
import Select from '@hi-ui/select'

/**
 * @title 自定义编辑器渲染
 */
export const EditorRender = () => {
  const [baseData, setBaseData] = useState<TagGroupDataItem[]>([
    {
      children: 'Test',
      id: 1,
    },
  ])
  const [tagsData] = useState([
    { id: 1, title: 'Test' },
    { id: 2, title: 'Test2' },
    { id: 3, title: 'Test3' },
    { id: 4, title: 'Test4' },
    { id: 5, title: 'Test5' },
  ])

  const selectData = React.useMemo(() => {
    return tagsData.filter((item) => !baseData.find((d) => d.id === item.id))
  }, [baseData, tagsData])

  return (
    <>
      <h1>EditorRender</h1>
      <Tag.Group
        data={baseData}
        // editable={false}
        editorRender={(updated) => {
          return (
            <Select
              style={{ display: 'inline-flex', width: 120, margin: '8px 0 0 0' }}
              size={'sm'}
              data={selectData}
              onClose={() => updated()}
              onChange={(id, item) => {
                if (id !== undefined) {
                  setBaseData((pre) => {
                    const result = [...pre]
                    result.push({
                      children: item.title,
                      id,
                    })
                    return result
                  })

                  updated()
                }
              }}
            />
          )
        }}
        onDelete={(e, index) => {
          setBaseData((pre) => {
            const result = [...pre]
            result.splice(index, 1)
            return result
          })
        }}
      />
    </>
  )
}

```

### max-width.stories.tsx

```typescript
import React from 'react'
import Tag from '@hi-ui/tag'

/**
 * @title 文本溢出隐藏
 */
export const MaxWidth = () => {
  const [maxEditableValue, setMaxEditableValue] = React.useState(
    'max 180px editable (placeholder1 placeholder2 placeholder3 placeholder4)'
  )

  return (
    <>
      <h1>Tag MaxWidth</h1>
      <div style={{ display: 'flex', gap: 8, flexWrap: 'wrap' }}>
        <Tag maxWidth={240}>max 240px (placeholder1 placeholder2 placeholder3 placeholder4)</Tag>
        {/* Tooltip 禁用 portal */}
        <Tag maxWidth={240} closeable tooltipProps={{ disabledPortal: true }}>
          max 240px (placeholder1 placeholder2 placeholder3 placeholder4)
        </Tag>
        <Tag maxWidth={180} editable onEdit={setMaxEditableValue}>
          {maxEditableValue}
        </Tag>
      </div>
    </>
  )
}

```

### shape.stories.tsx

```typescript
import React from 'react'
import Tag from '@hi-ui/tag'

/**
 * @title 不同形状
 */
export const Shape = () => {
  return (
    <>
      <h1>Tag Shape</h1>
      <div>
        <h2>square 方型</h2>

        <div style={{ display: 'flex', gap: 8 }}>
          <Tag shape="square" type="warning" appearance="filled">
            待审批
          </Tag>
          <Tag shape="square" type="primary" appearance="filled">
            审批中
          </Tag>
          <Tag shape="square" type="success" appearance="filled">
            已通过
          </Tag>
          <Tag shape="square" type="danger" appearance="filled">
            已驳回
          </Tag>
          <Tag shape="square" type="default" appearance="filled">
            待审批
          </Tag>
        </div>
        <br />
        <div style={{ display: 'flex', gap: 8 }}>
          <Tag shape="square" type="warning" appearance={'line'}>
            待审批
          </Tag>
          <Tag shape="square" type="primary" appearance={'line'}>
            审批中
          </Tag>
          <Tag shape="square" type="success" appearance={'line'}>
            已通过
          </Tag>
          <Tag shape="square" type="danger" appearance={'line'}>
            已驳回
          </Tag>
          <Tag shape="square" type="default" appearance={'line'}>
            待审批
          </Tag>
        </div>
        <br />
        <div style={{ display: 'flex', gap: 8 }}>
          <Tag shape="square" type="warning" appearance="solid">
            待审批
          </Tag>
          <Tag shape="square" type="primary" appearance="solid">
            审批中
          </Tag>
          <Tag shape="square" type="success" appearance="solid">
            已通过
          </Tag>
          <Tag shape="square" type="danger" appearance="solid">
            已驳回
          </Tag>
          <Tag shape="square" type="default" appearance="solid">
            待审批
          </Tag>
        </div>
        <h2>round 圆润型</h2>
        <div style={{ display: 'flex', gap: 8 }}>
          <Tag shape="round" type="warning" appearance="filled">
            待审批
          </Tag>
          <Tag shape="round" type="primary" appearance="filled">
            审批中
          </Tag>
          <Tag shape="round" type="success" appearance="filled">
            已通过
          </Tag>
          <Tag shape="round" type="danger" appearance="filled">
            已驳回
          </Tag>
          <Tag shape="round" type="default" appearance="filled">
            待审批
          </Tag>
        </div>
        <br />
        <div style={{ display: 'flex', gap: 8 }}>
          <Tag shape="round" type="warning" appearance={'line'}>
            待审批
          </Tag>
          <Tag shape="round" type="primary" appearance={'line'}>
            审批中
          </Tag>
          <Tag shape="round" type="success" appearance={'line'}>
            已通过
          </Tag>
          <Tag shape="round" type="danger" appearance={'line'}>
            已驳回
          </Tag>
          <Tag shape="round" type="default" appearance={'line'}>
            待审批
          </Tag>
        </div>
        <br />
        <div style={{ display: 'flex', gap: 8 }}>
          <Tag shape="round" type="warning" appearance="solid">
            待审批
          </Tag>
          <Tag shape="round" type="primary" appearance="solid">
            审批中
          </Tag>
          <Tag shape="round" type="success" appearance="solid">
            已通过
          </Tag>
          <Tag shape="round" type="danger" appearance="solid">
            已驳回
          </Tag>
          <Tag shape="round" type="default" appearance="solid">
            待审批
          </Tag>
        </div>
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Tag from '@hi-ui/tag'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>Tag Size</h1>
      <div>
        <h2>sm</h2>
        <div style={{ display: 'flex', gap: 8 }}>
          <Tag size="sm" type="warning" appearance="filled">
            待审批
          </Tag>
          <Tag size="sm" type="primary" appearance="filled">
            审批中
          </Tag>
          <Tag size="sm" type="success" appearance="filled">
            已通过
          </Tag>
          <Tag size="sm" type="danger" appearance="filled">
            已驳回
          </Tag>
          <Tag size="sm" type="default" appearance="filled">
            待审批
          </Tag>
        </div>
        <h2>md</h2>
        <div style={{ display: 'flex', gap: 8 }}>
          <Tag size="md" type="warning" appearance="filled">
            待审批
          </Tag>
          <Tag size="md" type="primary" appearance="filled">
            审批中
          </Tag>
          <Tag size="md" type="success" appearance="filled">
            已通过
          </Tag>
          <Tag size="md" type="danger" appearance="filled">
            已驳回
          </Tag>
          <Tag size="md" type="default" appearance="filled">
            待审批
          </Tag>
        </div>
        <h2>lg</h2>
        <div style={{ display: 'flex', gap: 8 }}>
          <Tag size="lg" type="warning" appearance="filled">
            待审批
          </Tag>
          <Tag size="lg" type="primary" appearance="filled">
            审批中
          </Tag>
          <Tag size="lg" type="success" appearance="filled">
            已通过
          </Tag>
          <Tag size="lg" type="danger" appearance="filled">
            已驳回
          </Tag>
          <Tag size="lg" type="default" appearance="filled">
            待审批
          </Tag>
        </div>
      </div>
    </>
  )
}

```

### tag-group.stories.tsx

```typescript
import React, { useState } from 'react'
import Tag, { TagGroupDataItem } from '@hi-ui/tag'

/**
 * @title 标签组用法
 * @desc 以标签为信息实体进行编辑操作，如品类、频道等管理
 */
export const TagGroup = () => {
  const [baseData, setBaseData] = useState<TagGroupDataItem[]>([
    {
      children: 'Test',
      id: '0',
    },
  ])

  return (
    <>
      <h1>Tag group</h1>
      <Tag.Group
        data={baseData}
        onEdit={(newString, node, index) => {
          setBaseData((pre) => {
            const result = [...pre]
            result[index].children = newString
            return result
          })
        }}
        onDelete={(e, index) => {
          setBaseData((pre) => {
            const result = [...pre]
            result.splice(index, 1)
            return result
          })
        }}
        onAdd={(e) => {
          if (e) {
            setBaseData((pre) => {
              const result = [...pre]
              result.push({
                children: e,
                id: Math.random(),
              })
              return result
            })
          }
        }}
      />
    </>
  )
}

```

## tag-input 组件

### basic.stories.tsx

```typescript
import { DownOutlined } from '@hi-ui/icons'
import React from 'react'
import TagInput from '@hi-ui/tag-input'

export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="tag-input-basic__wrap">
        <TagInput
          clearable
          // wrap={false}
          defaultValue={['1', '2', '不存在的测试']}
          suffix={<DownOutlined />}
          data={[
            {
              id: '1',
              title: '1',
            },
            {
              id: '2',
              title: '2',
            },
            {
              id: '3',
              title: '3',
            },
            {
              id: '4',
              title: '4',
            },
          ]}
        />
      </div>
    </>
  )
}

```

### mock.stories.tsx

```typescript
import { DownOutlined } from '@hi-ui/icons'
import React from 'react'
import { TagInputMock } from '@hi-ui/tag-input'

export const Mock = () => {
  const [value] = React.useState(['1', '2', '不存在的测试', '11', '12', '13', '14'])
  const [data] = React.useState([
    {
      id: '1',
      title: 'title1',
    },
    {
      id: '2',
      title: '二锅头',
    },
    {
      id: '3',
      title: '梦幻3',
    },
    {
      id: '4',
      title: '老四',
    },
    {
      id: '11',
      title: '1title1',
    },
    {
      id: '12',
      title: '1二锅头',
    },
    {
      id: '13',
      title: '1梦幻3',
    },
    {
      id: '14',
      title: '1老四',
    },
  ])

  return (
    <>
      <h1>Mock</h1>
      <div className="tag-input-basic__wrap">
        <TagInputMock
          clearable
          suffix={<DownOutlined />}
          // style={{ width: 380 }}
          // wrap={false}
          // disabled
          value={value}
          data={data}
        />

        <div>
          <h2>Outline</h2>
          <TagInputMock
            appearance="line"
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="sm"
            appearance="line"
            clearable
            placeholder="请输入"
            value={value}
            data={data}
            suffix={<DownOutlined />}
          />
          <br />
          <br />
          <TagInputMock
            size="sm"
            focused
            appearance="line"
            clearable
            placeholder="请输入"
            value={value}
            data={data}
            suffix={<DownOutlined />}
          />
          <br />
          <br />
          <TagInputMock
            size="md"
            appearance="line"
            focused
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="lg"
            invalid
            appearance="line"
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="lg"
            invalid
            focused
            appearance="line"
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="lg"
            appearance="line"
            disabled
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
        </div>

        <div>
          <h2>Filled</h2>
          <TagInputMock
            appearance="filled"
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="sm"
            appearance="filled"
            clearable
            placeholder="请输入"
            value={value}
            data={data}
            suffix={<DownOutlined />}
          />
          <br />
          <br />
          <TagInputMock
            size="sm"
            focused
            appearance="filled"
            clearable
            placeholder="请输入"
            value={value}
            data={data}
            suffix={<DownOutlined />}
          />
          <br />
          <br />
          <TagInputMock
            size="md"
            appearance="filled"
            focused
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="lg"
            invalid
            appearance="filled"
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="lg"
            invalid
            focused
            appearance="filled"
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="lg"
            appearance="filled"
            disabled
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
        </div>

        <div>
          <h2>Unset</h2>
          <TagInputMock
            appearance="unset"
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="sm"
            appearance="unset"
            clearable
            placeholder="请输入"
            value={value}
            data={data}
            suffix={<DownOutlined />}
          />
          <br />
          <br />
          <TagInputMock
            size="sm"
            appearance="unset"
            focused
            clearable
            placeholder="请输入"
            value={value}
            data={data}
            suffix={<DownOutlined />}
          />
          <br />
          <br />
          <TagInputMock
            size="md"
            appearance="unset"
            focused
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="lg"
            invalid
            appearance="unset"
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="lg"
            invalid
            focused
            appearance="unset"
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
          <TagInputMock
            size="lg"
            appearance="unset"
            disabled
            placeholder="请输入"
            suffix={<DownOutlined />}
          ></TagInputMock>
          <br />
          <br />
        </div>
      </div>
    </>
  )
}

```

### wrap.stories.tsx

```typescript
import { DownOutlined } from '@hi-ui/icons'
import React from 'react'
import { TagInputMock } from '@hi-ui/tag-input'

export const Wrap = () => {
  return (
    <>
      <h1>Wrap</h1>
      <div className="tag-input-wrap__wrap">
        <TagInputMock
          wrap
          clearable
          // style={{ width: 380 }}
          // wrap={false}
          // disabled
          defaultValue={['1', '2', '不存在的测试', '11', '12', '13', '14']}
          suffix={<DownOutlined />}
          data={[
            {
              id: '1',
              title: 'title1',
            },
            {
              id: '2',
              title: '二锅头',
            },
            {
              id: '3',
              title: '梦幻3',
            },
            {
              id: '4',
              title: '老四',
            },
            {
              id: '11',
              title: '1title1',
            },
            {
              id: '12',
              title: '1二锅头',
            },
            {
              id: '13',
              title: '1梦幻3',
            },
            {
              id: '14',
              title: '1老四',
            },
          ]}
        />
      </div>
    </>
  )
}

```

## textarea 组件

### auto-size.stories.tsx

```typescript
import React from 'react'
import TextArea from '@hi-ui/textarea'

/**
 * @title 自动适应高度
 */
export const AutoSize = () => {
  const [value, setValue] = React.useState('')

  return (
    <>
      <h1>AutoSize</h1>
      <div className="textarea-auto-size__wrap">
        <TextArea
          value={value}
          onChange={(evt) => setValue(evt.target.value)}
          placeholder="请输入"
          minRows={2}
          appearance="line"
        />
        <br />
        <TextArea
          value={value}
          onChange={(evt) => setValue(evt.target.value)}
          placeholder="请输入"
          maxRows={3}
          appearance="line"
        />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import TextArea from '@hi-ui/textarea'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const [value, setValue] = React.useState('')
  return (
    <>
      <h1>Basic</h1>
      <div className="textarea-basic__wrap">
        <TextArea
          value={value}
          onChange={(evt) => setValue(evt.target.value)}
          placeholder="请输入"
          appearance="line"
        />
        <br />
        <br />
        <TextArea
          value={value}
          onChange={(evt) => setValue(evt.target.value)}
          placeholder="请输入"
          maxRows={3}
          appearance="filled"
        />
        <br />
        <br />
        <TextArea
          value={value}
          onChange={(evt) => setValue(evt.target.value)}
          placeholder="请输入"
          rows={3}
          appearance="unset"
        />
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import TextArea from '@hi-ui/textarea'

/**
 * @title 禁用状态
 */
export const Disabled = () => {
  return (
    <>
      <h1>Disabled</h1>
      <div className="textarea-disabled__wrap">
        <h2>普通</h2>
        <div>
          <TextArea appearance="line" disabled placeholder="请输入"></TextArea>
          <br />
          <br />
          <TextArea appearance="unset" disabled placeholder="请输入"></TextArea>
          <br />
          <br />
          <TextArea appearance="filled" disabled placeholder="请输入"></TextArea>
        </div>
        <br />
        <h2>Invalid</h2>
        <div>
          <TextArea invalid appearance="line" disabled placeholder="请输入"></TextArea>
          <br />
          <br />
          <TextArea invalid appearance="unset" disabled placeholder="请输入"></TextArea>
          <br />
          <br />
          <TextArea invalid appearance="filled" disabled placeholder="请输入"></TextArea>
        </div>
        <br />
        <h2>有值</h2>
        <div>
          <TextArea value="输入值" appearance="line" disabled placeholder="请输入"></TextArea>
          <br />
          <br />
          <TextArea value="输入值" appearance="unset" disabled placeholder="请输入"></TextArea>
          <br />
          <br />
          <TextArea value="输入值" appearance="filled" disabled placeholder="请输入"></TextArea>
        </div>
      </div>
    </>
  )
}

```

### header.stories.tsx

```typescript
import React from 'react'
import TextArea from '@hi-ui/textarea'
import { CopyFilled, ExpressionOutlined } from '@hi-ui/icons'

/**
 * @title 输入框内置内容
 * @desc header默认在顶部展示，可根据需求自行定义样式
 */
export const Header = () => {
  return (
    <>
      <h1>Header</h1>
      <div className="text-header__wrap">
        <TextArea
          placeholder="请输入"
          header={
            <>
              <CopyFilled style={{ marginRight: 5, fontSize: 16, color: '#5f6a7a' }} />
              <ExpressionOutlined style={{ fontSize: 16, color: '#5f6a7a' }} />
            </>
          }
        ></TextArea>
      </div>
    </>
  )
}

```

### show-count.stories.tsx

```typescript
import React from 'react'
import TextArea from '@hi-ui/textarea'

/**
 * @title 展示输入字数
 */
export const ShowCount = () => {
  const [value, setValue] = React.useState('')
  return (
    <>
      <h1>ShowCount</h1>
      <div className="textarea-show-count__wrap">
        <TextArea
          value={value}
          onChange={(evt) => setValue(evt.target.value)}
          placeholder="请输入"
          appearance="line"
          showCount
          maxLength={80}
        />
      </div>
    </>
  )
}

```

## time-picker 组件

### addon.stories.tsx

```typescript
import React, { useState } from 'react'
import TimePicker from '@hi-ui/time-picker'
import { AppStoreOutlined } from '@hi-ui/icons'

/**
 * @title 前内置元素
 */
export const Addon = () => {
  const [addonValue, setAddonValue] = useState<string | string[]>(['12:00:00'])

  return (
    <>
      <h1>Addon</h1>
      <div className="time-picker-addon__wrap">
        <TimePicker
          placeholder={['请选择时间']}
          value={addonValue}
          onChange={(e) => {
            console.log('basic-default', e)
            setAddonValue(e)
          }}
          prefix={<AppStoreOutlined />}
        />
      </div>
    </>
  )
}

```

### appearance.stories.tsx

```typescript
import React from 'react'
import TimePicker from '@hi-ui/time-picker'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性、无UI三种
 */
export const Appearance = () => {
  return (
    <>
      <h1>Appearance</h1>
      <div className="time-picker-appearance__wrap">
        <h2>line</h2>
        <TimePicker placeholder={['请选择时间']} appearance={'line'} />
        <h2>solid</h2>
        <TimePicker placeholder={['请选择时间']} appearance={'filled'} />
        <h2>unset</h2>
        <TimePicker placeholder={['请选择时间']} appearance={'unset'} />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React, { useState } from 'react'
import TimePicker from '@hi-ui/time-picker'

/**
 * @title 基础用法
 * @desc 选择时间点，可与日期搭配使用，也可用于展示当天时间
 */
export const Basic = () => {
  const [basicValue, setBasicValue] = useState<string | string[]>(['12:00:00'])

  return (
    <>
      <h1>Basic</h1>
      <div className="time-picker-basic__wrap">
        <TimePicker
          placeholder={['请选择时间']}
          value={basicValue}
          onChange={(e) => {
            console.log('basic-default', e)
            setBasicValue(e)
          }}
        />
      </div>
    </>
  )
}

```

### custom-disabled.stories.tsx

```typescript
import React, { useState } from 'react'
import TimePicker from '@hi-ui/time-picker'

/**
 * @title 自定义禁选值
 * @desc 自定义禁选的时、分、秒数据
 */
export const CustomDisabled = () => {
  const [hourValue, setHourValue] = useState(['11:11:11', '13:13:13'])
  const [minuteValue, setMinuteValue] = useState(['11:11:11', '13:13:13'])
  const [secondValue, setSecondValue] = useState(['11:11:11', '13:13:13'])

  return (
    <>
      <h1>Custom Disabled</h1>
      <div className="time-picker-custom-disabled__wrap" style={{ height: 400 }}>
        <h2>hour</h2>
        <TimePicker
          value={hourValue}
          placeholder={['请选择开始时间', '请选择结束时间']}
          onChange={(value: any) => {
            console.log('custom-hour-value', value)
            setHourValue(value)
          }}
          disabledHours={() => [5]}
          type="range"
        />
        <h2>minute</h2>
        <TimePicker
          value={minuteValue}
          placeholder={['请选择开始时间', '请选择结束时间']}
          onChange={(value: any) => {
            console.log('custom-minute-value', value)
            setMinuteValue(value)
          }}
          disabledMinutes={(hour) => {
            if (hour === 5) {
              return [2]
            }
            return []
          }}
          type="range"
        />
        <h2>second</h2>
        <TimePicker
          value={secondValue}
          placeholder={['请选择开始时间', '请选择结束时间']}
          onChange={(value: any) => {
            console.log('custom-second-value', value)
            setSecondValue(value)
          }}
          disabledSeconds={(hour, minute) => {
            if (hour === 5 && minute === 2) {
              return [0]
            }
            return []
          }}
          type="range"
        />
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import TimePicker from '@hi-ui/time-picker'

/**
 * @title 禁用状态
 */
export const Disabled = () => {
  return (
    <>
      <h1>Disabled</h1>
      <div className="time-picker-disabled__wrap">
        <TimePicker disabled placeholder={['请选择时间']} />
      </div>
    </>
  )
}

```

### format.stories.tsx

```typescript
import React, { useCallback, useState } from 'react'
import TimePicker, { TimePickerFormat } from '@hi-ui/time-picker'

/**
 * @title 不同粒度
 * @desc 可自定义不同的时间粒度
 */
export const Format = () => {
  const [values, setValues] = useState([['11:11:11'], ['11:11'], ['11:11'], ['11'], ['11'], ['11']])

  const setMatchIndexValue = useCallback((newValue: string[], index: number) => {
    setValues((pre) => {
      const result = [...pre]
      result[index] = newValue
      return result
    })
  }, [])

  return (
    <>
      <h1>Basic use</h1>
      <div className="time-picker-format__wrap">
        {['HH:mm:ss', 'HH:mm', 'mm:ss', 'HH', 'mm', 'ss'].map((item, index) => (
          <React.Fragment key={index}>
            <h2>{item}</h2>
            <TimePicker
              format={item as TimePickerFormat}
              placeholder={['请选择时间']}
              value={values[index]}
              onChange={(value: any) => {
                console.log(item, value)
                setMatchIndexValue(value, index)
              }}
            />
          </React.Fragment>
        ))}
      </div>
    </>
  )
}

```

### input-readonly.stories.tsx

```typescript
import React, { useState } from 'react'
import TimePicker from '@hi-ui/time-picker'

/**
 * @title 输入框只读
 */
export const InputReadonly = () => {
  const [inputReadonlyValue, setInputReadonlyValue] = useState<string | string[]>(['11:11:11'])

  return (
    <>
      <h1>Input Readonly</h1>
      <div className="time-picker-input-readonly__wrap">
        <TimePicker
          placeholder={['请选择时间']}
          value={inputReadonlyValue}
          onChange={(e) => {
            console.log('input-readonly', e)
            setInputReadonlyValue(e)
          }}
          inputReadonly
        />
      </div>
    </>
  )
}

```

### range.stories.tsx

```typescript
import React, { useState } from 'react'
import TimePicker from '@hi-ui/time-picker'

/**
 * @title 时间范围
 * @desc 选择时间范围，可与日期搭配使用，也可用于展示当天时间范围
 */
export const Range = () => {
  const [rangeValue, setRangeValue] = useState<string | string[]>(['11:11:11', '12:00:00'])

  return (
    <>
      <h1>Range</h1>
      <div className="time-picker-range__wrap">
        <TimePicker
          value={rangeValue}
          placeholder={['请选择开始时间', '请选择结束时间']}
          onChange={(value) => {
            console.log('range-value', value)
            setRangeValue(value)
          }}
          type="range"
        />
      </div>
    </>
  )
}

```

## timeline 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Timeline from '@hi-ui/timeline'

/**
 * @title 基础用法
 * @desc 以时间为第一维度，展示该时间点的事务、日程、任务或记录
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="timeline-basic__wrap">
        <Timeline
          style={{ width: 440 }}
          data={[
            {
              title: '管理层例会',
              content: '毕加索会议室 B2层 可提前预定预…',
              timestamp: '10:00',
              extraTime: '02-23',
            },
            {
              title: '社招面试-设计师',
              content: '总参',
              timestamp: '10:00',
              extraTime: '02-27',
              children: [
                {
                  title: 'Sub 1',
                  content: 'Here are some descriptions',
                  timestamp: '10:00',
                  extraTime: '02-23',
                },
                {
                  title: 'Sub 2',
                  content: 'Here are some descriptions',
                },
              ],
            },
            {
              title: '管理层例会',
              content: '毕加索会议室 B2层 可提前预定预…',
              timestamp: '12:00',
              extraTime: '03-02',
            },
            {
              title: '社招面试-设计师',
              content: '总参',
              timestamp: '11:00',
              extraTime: '03-10',
              children: [
                {
                  title: 'Sub 1',
                  content: 'Here are some descriptions',
                  timestamp: '10:00',
                  extraTime: '02-23',
                },
                {
                  title: 'Sub 2',
                  content: 'Here are some descriptions',
                },
              ],
            },
          ]}
        />
      </div>
    </>
  )
}

```

### card-content.stories.tsx

```typescript
import React from 'react'
import Timeline from '@hi-ui/timeline'
import Card from '@hi-ui/card'

/**
 * @title 卡片内容
 */
export const CardContent = () => {
  return (
    <>
      <h1>卡片内容</h1>
      <div className="timeline-card__wrap" style={{ backgroundColor: '#F2F4F7', padding: 24 }}>
        <Timeline
          data={[
            {
              title: (
                <Card bordered={false}>
                  <div>毕加索会议室 B2层 可提前预定预…</div>
                  <div>毕加索会议室 B2层 可提前预定预…</div>
                  <div>毕加索会议室 B2层 可提前预定预…</div>
                  <div>毕加索会议室 B2层 可提前预定预…</div>
                </Card>
              ),
              timestamp: '10:00',
              extraTime: '02-23',
            },
            {
              title: <Card bordered={false}>社招面试-设计师</Card>,
              timestamp: '10:00',
              extraTime: '02-27',
              children: [
                {
                  title: <Card bordered={false}>Here are some descriptions 1</Card>,
                  timestamp: '10:00',
                  extraTime: '02-23',
                },
                {
                  title: <Card bordered={false}>Here are some descriptions 2</Card>,
                },
              ],
            },
            {
              title: <Card bordered={false}>毕加索会议室 B2层 可提前预定预…</Card>,
              timestamp: '12:00',
              extraTime: '03-02',
            },
            {
              title: (
                <Card bordered={false}>
                  <div>社招面试-设计师</div>
                  <div>社招面试-设计师</div>
                  <div>社招面试-设计师</div>
                  <div>社招面试-设计师</div>
                  <div>社招面试-设计师</div>
                </Card>
              ),
              timestamp: '11:00',
              extraTime: '03-10',
              children: [
                {
                  title: <Card bordered={false}>Here are some descriptions 1</Card>,
                  timestamp: '10:00',
                  extraTime: '02-23',
                },
                {
                  title: <Card bordered={false}>Here are some descriptions 2</Card>,
                },
              ],
            },
          ]}
        />
      </div>
    </>
  )
}

```

### cross.stories.tsx

```typescript
import React from 'react'
import Timeline from '@hi-ui/timeline'

/**
 * @title 左右结构样式
 * @desc 不同样式的时间轴，突出时间走向
 */
export const Cross = () => {
  return (
    <>
      <h1>Cross</h1>
      <div className="timeline-cross__wrap">
        <Timeline
          type="cross"
          data={[
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '10:00',
              extraTime: '02-23',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '10:00',
              extraTime: '02-27',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '12:00',
              extraTime: '03-02',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '11:00',
              extraTime: '03-10',
            },
          ]}
        />
      </div>
    </>
  )
}

```

### custom-icon.stories.tsx

```typescript
import React from 'react'
import Timeline from '@hi-ui/timeline'
import { EmptyFilled, SunFilled, CheckCircleFilled } from '@hi-ui/icons'

/**
 * @title 自定义图标
 * @desc 可运用图标加强对时间节点上的信息状态表示
 */
export const CustomIcon = () => {
  return (
    <>
      <h1>CustomIcon</h1>
      <div className="timeline-custom-icon__wrap">
        <Timeline
          style={{ width: 440 }}
          data={[
            {
              title: '管理层例会',
              content: '毕加索会议室 B2层 可提前预定预…',
              timestamp: '10:00',
              extraTime: '02-23',

              icon: <SunFilled style={{ color: '#fab007' }} />,
            },
            {
              title: '社招面试-设计师',
              content: '总参',
              timestamp: '10:00',
              extraTime: '02-27',
              icon: <EmptyFilled style={{ color: '#237ffa' }} />,
            },
            {
              title: '管理层例会',
              content: '毕加索会议室 B2层 可提前预定预…',
              timestamp: '12:00',
              extraTime: '03-02',
              icon: <CheckCircleFilled style={{ color: '#14ca64' }} />,
            },
          ]}
        />
      </div>
    </>
  )
}

```

### group.stories.tsx

```typescript
import React from 'react'
import Timeline from '@hi-ui/timeline'

/**
 * @title 内容分组
 */
export const Group = () => {
  return (
    <>
      <h1>Group</h1>
      <div className="timeline-group__wrap">
        <Timeline
          style={{ width: 440 }}
          data={[
            {
              groupTitle: '上午',
              children: [
                {
                  title: '管理层例会',
                  content: '毕加索会议室 B2层 可提前预定预…',
                  timestamp: '10:00',
                },
                {
                  title: '社招面试-设计师',
                  content: '总参',
                  timestamp: '10:00',
                },
              ],
            },
            {
              groupTitle: '下午',
              children: [
                {
                  title: '管理层例会',
                  content: '毕加索会议室 B2层 可提前预定预…',
                  timestamp: '12:00',
                },
                {
                  title: '社招面试-设计师',
                  content: '总参',
                  timestamp: '11:00',
                },
              ],
            },
          ]}
        />
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import React from 'react'
import Timeline from '@hi-ui/timeline'

/**
 * @title 左右结构样式
 * @desc 不同样式的时间轴，突出时间走向
 */
export const Placement = () => {
  return (
    <>
      <h1>Placement</h1>
      <div className="timeline-placement__wrap">
        <Timeline
          placement="horizontal"
          data={[
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '10:00',
              extraTime: '02-23',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '10:00',
              extraTime: '02-27',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '12:00',
              extraTime: '03-02',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '11:00',
              extraTime: '03-10',
            },
          ]}
        />
        <br />
        <br />
        <Timeline
          placement="horizontal"
          itemPlacement="center"
          data={[
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '10:00',
              extraTime: '02-23',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '10:00',
              extraTime: '02-27',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '12:00',
              extraTime: '03-02',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '11:00',
              extraTime: '03-10',
            },
          ]}
        />
      </div>
    </>
  )
}

```

### right.stories.tsx

```typescript
import React from 'react'
import Timeline from '@hi-ui/timeline'

/**
 * @title 信息流样式
 * @desc 在一段时间范围里，信息流向增长，数量庞大，必要时可收起部分
 */
export const Right = () => {
  return (
    <>
      <h1>Right</h1>
      <div className="timeline-right__wrap">
        <Timeline
          type="right"
          data={[
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '10:00',
              extraTime: '02-23',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '10:00',
              extraTime: '02-27',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '12:00',
              extraTime: '03-02',
            },
            {
              title: '信息部全员财务培训需求收集',
              content:
                '为使信息部同事更好的研发、运维和服务财务部的需求和工作，财务部计划给信息部同事提供财务相关的培训',
              timestamp: '11:00',
              extraTime: '03-10',
            },
          ]}
        />
      </div>
    </>
  )
}

```

## toast 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Toast from '@hi-ui/toast'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const ToastAPI = React.useMemo(() => Toast.create({ prefixCls: 'basic' }), [])

  return (
    <>
      <h1>Basic</h1>
      <div className="toast-basic__wrap">
        <Button
          onClick={() => {
            ToastAPI.open({
              title: 'xxxx',
            })
          }}
        >
          Toast
        </Button>

        <Button
          onClick={() => {
            ToastAPI.destroy()
          }}
        >
          Destroy Toast
        </Button>
      </div>
    </>
  )
}

```

## tooltip 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Tooltip from '@hi-ui/tooltip'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 * @desc 用于解释、描述、引导
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="Tooltip-basic__wrap">
        <Tooltip title="Tooltip Title" trigger="hover">
          <Button>trigger</Button>
        </Tooltip>
      </div>
    </>
  )
}

```

### break-word.stories.tsx

```typescript
import React from 'react'
import Tooltip from '@hi-ui/tooltip'
import Button from '@hi-ui/button'

/**
 * @title 文本换行
 */
export const BreakWord = () => {
  return (
    <>
      <h1>BreakWord</h1>
      <div className="Tooltip-break-word__wrap">
        <Tooltip
          title={<div style={{ width: 200 }}>这是两行提示文字这是两行提示文字这是两行提示文字</div>}
          trigger="click"
        >
          <Button>trigger</Button>
        </Tooltip>
      </div>
    </>
  )
}

```

### gutter-gap.stories.tsx

```typescript
import React from 'react'
import Tooltip from '@hi-ui/tooltip'
import Button from '@hi-ui/button'

/**
 * @title 设置间隙偏移量
 * @desc 设置基于依附元素的间隙偏移量
 */
export const GutterGap = () => {
  return (
    <>
      <h1>Gutter Gap</h1>
      <div className="Tooltip-basic__wrap">
        <Tooltip title="Tooltip Title" gutterGap={30} trigger="hover">
          <Button>trigger</Button>
        </Tooltip>
      </div>
    </>
  )
}

```

### placement.stories.tsx

```typescript
import React from 'react'
import Tooltip from '@hi-ui/tooltip'
import Button from '@hi-ui/button'

/**
 * @title 不同方位
 */
export const Placement = () => {
  return (
    <>
      <h1>Placement</h1>
      <div className="popper-placement__wrap">
        <table className="placement-table" cellSpacing="5">
          <tbody>
            <tr>
              <td></td>
              <td>
                <Tooltip
                  title="我是内容我是内容我是内容我是内容"
                  trigger="hover"
                  placement="top-start"
                >
                  <Button style={{ width: 100 }}>top-start</Button>
                </Tooltip>
              </td>
              <td>
                <Tooltip title="我是内容我是内容我是内容我是内容" trigger="hover" placement="top">
                  <Button style={{ width: 100 }}>top</Button>
                </Tooltip>
              </td>
              <td>
                <Tooltip
                  title="我是内容我是内容我是内容我是内容"
                  trigger="hover"
                  placement="top-end"
                >
                  <Button style={{ width: 100 }}>top-end</Button>
                </Tooltip>
              </td>
              <td></td>
            </tr>
            <tr>
              <td>
                <Tooltip
                  title="我是内容我是内容我是内容我是内容"
                  trigger="hover"
                  placement="left-start"
                >
                  <Button style={{ width: 100 }}>left-start</Button>
                </Tooltip>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Tooltip
                  title="我是内容我是内容我是内容我是内容"
                  trigger="hover"
                  placement="right-start"
                >
                  <Button style={{ width: 100 }}>right-start</Button>
                </Tooltip>
              </td>
            </tr>
            <tr>
              <td>
                <Tooltip title="我是内容我是内容我是内容我是内容" trigger="hover" placement="left">
                  <Button style={{ width: 100 }}>left</Button>
                </Tooltip>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Tooltip title="我是内容我是内容我是内容我是内容" trigger="hover" placement="right">
                  <Button style={{ width: 100 }}>right</Button>
                </Tooltip>
              </td>
            </tr>
            <tr>
              <td>
                <Tooltip
                  title="我是内容我是内容我是内容我是内容"
                  trigger="hover"
                  placement="left-end"
                >
                  <Button style={{ width: 100 }}>left-end</Button>
                </Tooltip>
              </td>
              <td></td>
              <td></td>
              <td></td>
              <td>
                <Tooltip
                  title="我是内容我是内容我是内容我是内容"
                  trigger="hover"
                  placement="right-end"
                >
                  <Button style={{ width: 100 }}>right-end</Button>
                </Tooltip>
              </td>
            </tr>
            <tr>
              <td></td>
              <td>
                <Tooltip
                  title="我是内容我是内容我是内容我是内容"
                  trigger="hover"
                  placement="bottom-start"
                >
                  <Button style={{ width: 100 }}>bottom-start</Button>
                </Tooltip>
              </td>
              <td>
                <Tooltip
                  title="我是内容我是内容我是内容我是内容"
                  trigger="hover"
                  placement="bottom"
                >
                  <Button style={{ width: 100 }}>bottom</Button>
                </Tooltip>
              </td>
              <td>
                <Tooltip
                  title="我是内容我是内容我是内容我是内容"
                  trigger="hover"
                  placement="bottom-end"
                >
                  <Button style={{ width: 100 }}>bottom-end</Button>
                </Tooltip>
              </td>
              <td></td>
            </tr>
          </tbody>
        </table>
      </div>
    </>
  )
}

```

### trigger.stories.tsx

```typescript
import React from 'react'
import Tooltip from '@hi-ui/tooltip'
import Button from '@hi-ui/button'

/**
 * @title 自定义触发器
 * @desc 请确保子元素能接受对应的 onMouseEnter、onMouseLeave、onFocus、onClick 事件
 */
export const Trigger = () => {
  return (
    <>
      <h1>Trigger</h1>
      <div className="Tooltip-trigger__wrap">
        <Tooltip title="Tooltip Title">
          <Button>default</Button>
        </Tooltip>
        <br />
        <br />
        <Tooltip title="Tooltip Title" trigger="click">
          <Button>click</Button>
        </Tooltip>
        <br />
        <br />
        <Tooltip title="Tooltip Title" trigger="contextmenu">
          <Button>contextmenu</Button>
        </Tooltip>
        <br />
        <br />
        <Tooltip title="Tooltip Title" trigger="focus">
          <Button>focus</Button>
        </Tooltip>
      </div>
    </>
  )
}

```

### with-api.stories.tsx

```typescript
import React from 'react'
import Button from '@hi-ui/button'
import Tooltip from '@hi-ui/tooltip'

/**
 * @title API 调用
 */
export const WithAPI = () => {
  const [showTooltip, setShowTooltip] = React.useState(false)
  const triggerElementRef = React.useRef<HTMLSpanElement | null>(null)

  const toggleTooltip = () => {
    if (showTooltip) {
      Tooltip.close('123')
      setShowTooltip(false)
    } else {
      Tooltip.open(triggerElementRef.current, {
        key: '123',
        title: 'Click again to hide me.',
        placement: 'right',
      })
      setShowTooltip(true)
    }
  }

  return (
    <>
      <h1>WithAPI</h1>
      <div className="modal-with-api__wrap">
        <Button type="primary" onClick={toggleTooltip}>
          {showTooltip ? 'Hide' : 'Show'} tooltip
        </Button>
        <br />
        <span ref={triggerElementRef} style={{ marginTop: '10px', display: 'inline-block' }}>
          <Button disabled>Show tooltip on me</Button>
        </span>
      </div>
    </>
  )
}

```

## transfer 组件

### all-check.stories.tsx

```typescript
import React from 'react'
import Transfer from '@hi-ui/transfer'

/**
 * @title 可全选
 * @desc 快速完成源集合的全部选择，避开冗余操作
 */
export const AllCheck = () => {
  const [data] = React.useState(() => {
    const generateData = () => {
      const arr = []
      for (let i = 1; i < 100; i++) {
        arr.push({
          id: i,
          title: '选项' + i,
          disabled: i % 6 === 0,
        })
      }
      return arr
    }

    const data = generateData()
    return data
  })

  const [targetIds, setTargetIds] = React.useState<React.ReactText[]>([2, 3])

  return (
    <>
      <h1>AllCheck</h1>
      <div className="transfer-all-check__wrap">
        <Transfer
          type="multiple"
          data={data}
          targetIds={targetIds}
          onChange={(ids) => setTargetIds(ids)}
          emptyContent={['暂无数据']}
          showCheckAll
          title={['源数据', '目标数据']}
        />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Transfer from '@hi-ui/transfer'

/**
 * @title 基础用法
 * @desc 源集合中的数据可全部展示
 */
export const Basic = () => {
  const [data] = React.useState(() => {
    const generateData = () => {
      const arr = []
      for (let i = 1; i < 100; i++) {
        arr.push({
          id: i,
          title: '选项' + i,
          disabled: i % 6 === 0,
        })
      }
      return arr
    }

    const data = generateData()
    return data
  })

  const [targetIds, setTargetIds] = React.useState<React.ReactText[]>([2, 3])

  return (
    <>
      <h1>Basic</h1>
      <div className="transfer-basic__wrap">
        <Transfer
          data={data}
          targetLimit={6}
          targetIds={targetIds}
          onChange={(ids) => setTargetIds(ids)}
          emptyContent={['暂无数据']}
        />
      </div>
    </>
  )
}

```

### disabled.stories.tsx

```typescript
import React from 'react'
import Transfer from '@hi-ui/transfer'

/**
 * @title 禁用状态
 */
export const Disabled = () => {
  const [data] = React.useState(() => {
    const generateData = () => {
      const arr = []
      for (let i = 1; i < 100; i++) {
        arr.push({
          id: i,
          title: '选项' + i,
          disabled: i % 6 === 0,
        })
      }
      return arr
    }

    const data = generateData()
    return data
  })

  const [targetIds, setTargetIds] = React.useState<React.ReactText[]>([2, 3])

  return (
    <>
      <h1>Disabled</h1>
      <div className="transfer-disabled__wrap">
        <Transfer
          data={data}
          targetIds={targetIds}
          onChange={(ids) => setTargetIds(ids)}
          emptyContent={['暂无数据']}
          title={['title']}
          disabled
          type="multiple"
        />
      </div>
    </>
  )
}

```

### draggable.stories.tsx

```typescript
import React from 'react'
import Transfer from '@hi-ui/transfer'

/**
 * @title 拖拽排序
 * @desc 可通过拖拽的形式对目标区域内进行排序
 */
export const Draggable = () => {
  const [data] = React.useState(() => {
    const generateData = () => {
      const arr = []
      for (let i = 1; i < 100; i++) {
        arr.push({
          id: i,
          title: '选项' + i,
          disabled: i % 6 === 0,
        })
      }
      return arr
    }

    const data = generateData()
    return data
  })

  const [targetIds, setTargetIds] = React.useState<React.ReactText[]>([2, 3])

  return (
    <>
      <h1>可排序</h1>
      <div className="transfer-all-check__wrap">
        <Transfer
          type="multiple"
          data={data}
          targetIds={targetIds}
          onChange={(ids) => setTargetIds(ids)}
          emptyContent={['暂无数据']}
          showCheckAll
          draggable
          title={['源数据', '目标数据']}
        />
      </div>
    </>
  )
}

```

### limit.stories.tsx

```typescript
import React from 'react'
import Transfer from '@hi-ui/transfer'

/**
 * @title 数量上限
 */
export const Limit = () => {
  const [data] = React.useState(() => {
    const generateData = () => {
      const arr = []
      for (let i = 1; i < 100; i++) {
        arr.push({
          id: i,
          title: '选项' + i,
          disabled: i % 6 === 0,
        })
      }
      return arr
    }

    const data = generateData()
    return data
  })

  const [targetIds, setTargetIds] = React.useState<React.ReactText[]>([2, 3])

  return (
    <>
      <h1>Limit</h1>
      <div className="transfer-limit__wrap">
        <Transfer
          data={data}
          targetLimit={6}
          targetIds={targetIds}
          onChange={(ids) => setTargetIds(ids)}
          emptyContent={['暂无数据']}
        />
      </div>
    </>
  )
}

```

### multiple.stories.tsx

```typescript
import React from 'react'
import Transfer from '@hi-ui/transfer'

/**
 * @title 批量选中
 */
export const Multiple = () => {
  const [data] = React.useState(() => {
    const generateData = () => {
      const arr = []
      for (let i = 1; i < 100; i++) {
        arr.push({
          id: i,
          title: '选项' + i,
          disabled: i % 6 === 0,
        })
      }
      return arr
    }

    const data = generateData()
    return data
  })

  const [targetIds, setTargetIds] = React.useState<React.ReactText[]>([2, 3])

  return (
    <>
      <h1>Multiple</h1>
      <div className="transfer-multiple__wrap">
        <Transfer
          data={data}
          type="multiple"
          targetLimit={8}
          targetIds={targetIds}
          onChange={(ids) => setTargetIds(ids)}
          emptyContent={['暂无数据']}
        />
      </div>
    </>
  )
}

```

### pagination.stories.tsx

```typescript
import React from 'react'
import Transfer from '@hi-ui/transfer'

/**
 * @title 分页
 */
export const Pagination = () => {
  const [data] = React.useState(() => {
    const generateData = () => {
      const arr = []
      for (let i = 1; i < 100; i++) {
        arr.push({
          id: i,
          title: '选项' + i,
          // disabled: i % 6 === 0,
        })
      }
      return arr
    }

    const data = generateData()
    return data
  })

  const [targetIds, setTargetIds] = React.useState<React.ReactText[]>([2, 3])

  return (
    <>
      <h1>Pagination</h1>
      <div className="transfer-pagination__wrap">
        <Transfer
          type="multiple"
          data={data}
          // targetLimit={8}
          targetIds={targetIds}
          onChange={(ids) => setTargetIds(ids)}
          emptyContent={['暂无数据']}
          searchable
          pagination={{ pageSize: 10 }}
          draggable
          showCheckAll
        />
      </div>
    </>
  )
}

```

### render.stories.tsx

```typescript
import React from 'react'
import Transfer from '@hi-ui/transfer'
import { Avatar } from '@hi-ui/avatar'

/**
 * @title 自定义渲染
 */
export const Render = () => {
  const [data] = React.useState([
    { avatarColor: '#237ffa', initials: 'R', id: '荣莎', title: '荣莎', dept: '信息技术部' },
    { avatarColor: '#9772fb', initials: 'N', id: '尼坚', title: '尼坚', dept: '手机部' },
    { avatarColor: '#0daeff', initials: 'L', id: '伦颖璧', title: '伦颖璧', dept: '信息技术部' },
    { avatarColor: '#38d677', initials: 'X', id: '幸婉娥', title: '幸婉娥', dept: '汽车部' },
    { avatarColor: '#fab007', initials: 'B', id: '柏胜', title: '柏胜', dept: '信息技术部' },
    { avatarColor: '#fe7940', initials: 'Q', id: '曲强', title: '曲强', dept: '信息技术部' },
    { avatarColor: '#237ffa', initials: 'P', id: '皮莎仪', title: '皮莎仪', dept: '信息技术部' },
    { avatarColor: '#9772fb', initials: 'Z', id: '仲希', title: '仲希', dept: '信息技术部' },
  ])
  const [targetIds, setTargetIds] = React.useState<React.ReactText[]>([2, 3])

  return (
    <>
      <h1>Render</h1>
      <div className="transfer-render__wrap">
        <Transfer
          type="multiple"
          data={data}
          targetLimit={6}
          targetIds={targetIds}
          onChange={(ids) => setTargetIds(ids)}
          emptyContent={['暂无数据']}
          render={(item: any) => {
            return (
              <div style={{ lineHeight: '20px', display: 'inline-flex', alignItems: 'center' }}>
                <Avatar
                  shape="square"
                  initials={item.initials}
                  size="sm"
                  style={{ backgroundColor: item.avatarColor }}
                />
                <div style={{ marginLeft: 8 }}>
                  <div style={{ marginTop: 4 }}>{item.title}</div>
                  <div style={{ color: '#929AA6', marginBottom: 4 }}>{item.dept}</div>
                </div>
              </div>
            )
          }}
        />
      </div>
    </>
  )
}

```

### searchable.stories.tsx

```typescript
import React from 'react'
import Transfer from '@hi-ui/transfer'

/**
 * @title 可搜索
 * @desc 源集合庞大，需借助搜索工具完成
 */
export const Searchable = () => {
  const [data] = React.useState(() => {
    const generateData = () => {
      const arr = []
      for (let i = 1; i < 100; i++) {
        arr.push({
          id: i,
          title: '选项' + i,
          disabled: i % 6 === 0,
        })
      }
      return arr
    }

    const data = generateData()
    return data
  })

  const [targetIds, setTargetIds] = React.useState<React.ReactText[]>([2, 3])

  return (
    <>
      <h1>Searchable</h1>
      <div className="transfer-searchable__wrap">
        <Transfer
          data={data}
          targetLimit={6}
          targetIds={targetIds}
          onChange={(ids) => setTargetIds(ids)}
          emptyContent={['暂无数据']}
          searchable
        />
      </div>
    </>
  )
}

```

### title.stories.tsx

```typescript
import React from 'react'
import Transfer from '@hi-ui/transfer'

/**
 * @title 带标题
 */
export const Title = () => {
  const [data] = React.useState(() => {
    const generateData = () => {
      const arr = []
      for (let i = 1; i < 100; i++) {
        arr.push({
          id: i,
          title: '选项' + i,
          disabled: i % 6 === 0,
        })
      }
      return arr
    }

    const data = generateData()
    return data
  })

  const [targetIds, setTargetIds] = React.useState<React.ReactText[]>([2, 3])

  return (
    <>
      <h1>Title</h1>
      <div className="transfer-title__wrap">
        <Transfer
          data={data}
          targetLimit={6}
          targetIds={targetIds}
          onChange={(ids) => setTargetIds(ids)}
          emptyContent={['暂无数据']}
          title={['源数据', '目标数据']}
        />
      </div>
    </>
  )
}

```

## tree 组件

### action-render.stories.tsx

```typescript
import React from 'react'
import Tree, { useTreeAction } from '@hi-ui/tree'
import Space from '@hi-ui/space'
import PopConfirm from '@hi-ui/pop-confirm'
import { PlusOutlined, DuplicateOutlined, EditOutlined, DeleteOutlined } from '@hi-ui/icons'

/**
 * @title 自定义编辑项
 * @desc 用于编辑树操作菜单显示在外面的场景
 */
export const ActionRender = () => {
  const ActionTree = useTreeAction(Tree)

  return (
    <>
      <h1>ActionRender for Tree</h1>
      <div className="tree-action-render__wrap">
        <ActionTree
          expandOnSelect
          editPlaceholder="请填写菜单"
          actionRender={(node, editActions) => {
            console.log('node', node)

            const { id } = node

            return id === 11 ? (
              <Space>
                <PlusOutlined onClick={() => editActions.addChildNode(1)} />
                <DuplicateOutlined onClick={() => editActions.addSiblingNode()} />
                <EditOutlined onClick={() => editActions.editNode()} />
                <PopConfirm
                  title={'确认删除该节点？'}
                  onConfirm={editActions.deleteNode}
                  onClose={editActions.closeMenu}
                >
                  <DeleteOutlined onClick={() => editActions.openMenu()} />
                </PopConfirm>
              </Space>
            ) : null
          }}
          data={[
            {
              id: 1,
              title: '小米',
              children: [
                {
                  id: 2,
                  title: '研发',
                  children: [
                    { id: 3, title: '后端' },
                    { id: 4, title: '运维' },
                    { id: 5, title: '前端' },
                  ],
                },
                { id: 6, title: '产品' },
              ],
            },
            {
              id: 11,
              title: '大米',
              children: [
                { id: 22, title: '可视化' },
                { id: 66, title: 'HiUI' },
              ],
            },
          ]}
        />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Tree from '@hi-ui/tree'
import Button from '@hi-ui/button'

/**
 * @title 基础用法
 * @desc 二叉树或多叉树的展现形式，常见于组织架构、文件管理、索引目录等应用场景
 */
export const Basic = () => {
  const [expandedIds, setExpandedIds] = React.useState<React.ReactText[]>([])

  return (
    <>
      <h1>Basic for Tree</h1>
      <div className="tree-basic__wrap">
        <Button
          onClick={() => {
            setExpandedIds([1])
          }}
        >
          setExpanded
        </Button>
        <Tree
          expandedIds={expandedIds}
          onExpand={setExpandedIds}
          data={[
            {
              id: 1,
              title: '小米',
              children: [
                {
                  id: 2,
                  title: '研发',
                  disabled: true,
                  children: [
                    { id: 3, title: '后端', disabled: true },
                    { id: 4, title: '运维' },
                    { id: 5, title: '前端' },
                  ],
                },
                { id: 6, title: '产品' },
              ],
            },
            {
              id: 11,
              title: '大米',
              children: [
                { id: 22, title: '可视化' },
                { id: 66, title: 'HiUI' },
              ],
            },
          ]}
        ></Tree>
      </div>
    </>
  )
}

```

### checkable.stories.tsx

```typescript
import React from 'react'
import Tree from '@hi-ui/tree'

/**
 * @title 基础多选
 * @desc 用于一次性选中同级多个节点或全选同级节点，可与其它组件搭配使用
 */
export const Checkable = () => {
  const [checkedIds, setCheckedIds] = React.useState([])
  const [treeData] = React.useState([
    {
      id: 1,
      title: '小米',
      children: [
        {
          id: 2,
          title: '技术',
          children: [
            { id: 3, title: '后端' },
            { id: 4, title: '运维' },
            { id: 5, title: '前端' },
          ],
        },
        {
          id: 6,
          title: '产品',
          disabled: true,
          children: [
            { id: 61, title: '后端' },
            { id: 62, title: '运维' },
            { id: 63, title: '前端' },
          ],
        },
        {
          id: 8,
          title: '发发发',

          children: [],
        },
      ],
    },
    {
      id: 11,
      title: '大米',
      children: [
        { id: 22, title: '技术' },
        { id: 66, title: '产品' },
      ],
    },
  ])

  return (
    <>
      <h1>Checkable for Tree</h1>
      <div className="tree-checkable__wrap">
        <Tree
          checkable
          data={treeData}
          checkedIds={checkedIds}
          onCheck={(...args) => {
            console.log(...args)
            setCheckedIds(args[0])
          }}
          render={(node) => `${node.title}(${node.id})`}
        ></Tree>
      </div>
    </>
  )
}

```

### custom-icon.stories.tsx

```typescript
import { FileOutlined, FolderOpenOutlined, FolderOutlined } from '@hi-ui/icons'
import React from 'react'
import Tree from '@hi-ui/tree'

/**
 * @title 自定义 Icon
 */
export const CustomIcon = () => {
  const [treeData] = React.useState([
    {
      id: 1,
      title: '小米',
      children: [
        {
          id: 2,
          title: '技术',
          children: [
            { id: 3, title: '后端' },
            { id: 4, title: '运维' },
            { id: 5, title: '前端' },
          ],
        },
        {
          id: 6,
          title: '产品',

          children: [
            { id: 61, title: '后端' },
            { id: 62, title: '运维' },
            { id: 63, title: '前端' },
          ],
        },
        {
          id: 8,
          title: '发发发',

          children: [],
        },
      ],
    },
    {
      id: 11,
      title: '大米',
      children: [
        { id: 22, title: '技术' },
        { id: 66, title: '产品' },
      ],
    },
  ])

  return (
    <>
      <h1>CustomIcon for Tree</h1>
      <div className="tree-custom-icon__wrap">
        <Tree
          data={treeData}
          collapsedIcon={<FolderOutlined />}
          expandedIcon={<FolderOpenOutlined />}
          leafIcon={<FileOutlined />}
        />
      </div>
    </>
  )
}

```

### custom-search.stories.tsx

```typescript
import React from 'react'
import Tree, { useTreeSearchProps } from '@hi-ui/tree'
import Input from '@hi-ui/input'
import Button from '@hi-ui/button'

/**
 * @title 自定义搜索 UI
 * @desc 通过 useTreeSearchProps 复用搜索逻辑，搜索 UI 交互展示完全自定义
 */
export const CustomSearch = () => {
  const [data] = React.useState([
    {
      id: '1',
      title: '小米',
      children: [
        {
          id: '2',
          title: '研发',
          children: [
            { id: '3', title: '后端' },
            { id: '4', title: '运维' },
            { id: '5', title: '前端' },
          ],
        },
        { id: '6', title: '产品' },
      ],
    },
    {
      id: '11',
      title: '大米',
      children: [
        { id: '22', title: '可视化' },
        { id: '66', title: 'HiUI' },
      ],
    },
  ])

  const [searchValue, setSearchValue] = React.useState('')
  const { filterTree, customFilterTree, isEmpty, treeProps } = useTreeSearchProps({
    searchable: true,
    searchPlaceholder: '搜索',
    data,
    // checkable: true,
  })

  return (
    <>
      <h1>CustomSearch for Tree</h1>
      <div className="tree-custom-search__wrap">
        <Input
          value={searchValue}
          onChange={(evt) => setSearchValue(evt.target.value)}
          placeholder="请输入要查询的岗位"
        />
        <Button
          style={{ margin: '12px 12px 12px 0' }}
          onClick={() => {
            filterTree(searchValue)
          }}
        >
          点击搜索岗位
        </Button>
        <Button
          style={{ margin: '12px 0' }}
          onClick={() => {
            customFilterTree(searchValue, (node) =>
              !searchValue ? false : (node.raw.title as string).indexOf(searchValue) > -1
            )
          }}
        >
          点击搜索岗位（自定义匹配逻辑）
        </Button>
        <div style={{ fontSize: 14, color: '#5f6a7a' }}>
          我是提示：{isEmpty ? '暂时匹配不到相关岗位信息' : '无'}
        </div>
        <Tree {...treeProps} onCheck={console.log} />
      </div>
    </>
  )
}

```

### custom-title.stories.tsx

```typescript
import React from 'react'
import { ExcelColorful } from '@hi-ui/icons'
import Tree, { TreeDataItem } from '@hi-ui/tree'

/**
 * @title 自定义渲染
 * @desc 自定义渲染树节点标题
 */
export const CustomTitle = () => {
  const [treeData] = React.useState([
    {
      id: 1,
      title: '小米',
      children: [
        {
          id: 2,
          title: '技术',
          children: [
            { id: 3, title: '后端' },
            { id: 4, title: '运维' },
            { id: 5, title: '前端' },
          ],
        },
        {
          id: 6,
          title: '产品',

          children: [
            { id: 61, title: '后端' },
            { id: 62, title: '运维' },
            { id: 63, title: '前端' },
          ],
        },
        {
          id: 8,
          title: '发发发',

          children: [],
        },
      ],
    },
    {
      id: 11,
      title: '大米',
      children: [
        { id: 22, title: '技术' },
        { id: 66, title: '产品' },
      ],
    },
  ])

  const renderTreeNodeTitle = (node: TreeDataItem) => {
    return (
      <div
        style={{
          width: '100%',
          display: 'flex',
          justifyContent: 'space-between',
          alignItems: 'center',
        }}
      >
        <div>
          {/* 自定义 title 的前缀 icon */}
          {/* <span className="custom-left-icon" style={{ marginRight: 12 }}>
            😄
          </span> */}
          <ExcelColorful style={{ marginRight: 2 }} />
          <span>{node.title}</span>
          <span>{`（${node.id}）`}</span>
        </div>
        {/* 自定义 title 的后缀 icon */}
        {/* <div>
          {Array.isArray(node.children) && node.children.length > 0 ? null : (
            <span className="custom-right-icon">❤</span>
          )}
        </div> */}
      </div>
    )
  }

  return (
    <>
      <h1>CustomTitle for Tree</h1>
      <div className="tree-custom-title__wrap">
        <Tree data={treeData} render={renderTreeNodeTitle}></Tree>
      </div>
    </>
  )
}

```

### draggable.stories.tsx

```typescript
import React from 'react'
import Tree from '@hi-ui/tree'

/**
 * @title 拖拽排序
 * @desc 通过鼠标拖拽行为，改变树的层级结构
 */
export const Draggable = () => {
  const [treeData] = React.useState([
    {
      id: 1,
      title: '小米',
      children: [
        {
          id: 2,
          title: '技术',
          children: [
            { id: 3, title: '后端' },
            { id: 4, title: '运维' },
            { id: 5, title: '前端' },
          ],
        },
        { id: 6, title: '产品' },
      ],
    },
    {
      id: 11,
      title: '大米',
      children: [
        { id: 22, title: '技术' },
        { id: 66, title: '产品' },
      ],
    },
  ])

  return (
    <>
      <h1>draggable for Tree</h1>
      <div className="tree-draggable__wrap">
        <Tree
          showLine
          draggable
          onDrop={(...args) => {
            console.log('onDrop', ...args)
            // setTreeData(data.after)
            return true
          }}
          data={treeData}
          onDragStart={console.log}
          onDragEnd={console.log}
          onDragOver={console.log}
          onDragLeave={console.log}
        />
      </div>
    </>
  )
}

```

### dynamic.stories.tsx

```typescript
import React from 'react'
import Tree from '@hi-ui/tree'
import { cloneTree, findNodeById } from '@hi-ui/utils'
import Alert from '@hi-ui/alert'

/**
 * @title 异步加载
 * @desc 打开下一级时从服务端调取节点数据
 */
export const Dynamic = () => {
  const [treeData, setTreeData] = React.useState([
    {
      id: 1,
      title: '小米',
      children: [
        {
          id: 2,
          title: '技术',
          children: [
            { id: 3, title: '后端' },
            { id: 4, title: '运维' },
            { id: 5, title: '前端' },
          ],
        },
        { id: 6, title: '产品' },
      ],
    },
    {
      id: 11,
      title: '小米',
      children: [
        { id: 22, title: '技术' },
        { id: 66, title: '产品' },
      ],
    },
  ])

  // 加载节点
  const loadChildren = async (node) => {
    return fetch(`https://my-json-server.typicode.com/hiui-group/db/conditiondata?id=${node.id}`)
      .then((res) => res.json())
      .then((data) => {
        if (data[0]) {
          data[0].id = Math.random()
          data[0].parent = treeData
        }

        // Utils Helper: import { cloneTree, findNodeById } from '@hi-ui/utils'
        setTreeData((prev) => {
          const nextData = cloneTree(prev)
          const loadNode = findNodeById(nextData, node.id)
          loadNode.children = data
          console.log(loadNode, nextData)
          return nextData
        })

        // return data
      })
  }

  return (
    <>
      <h1>Dynamic for Tree</h1>
      <div className="tree-dynamic__wrap">
        <Alert
          type="danger"
          closeable={false}
          showIcon={false}
          title={
            '注意：对于异步加载子节点，可以配合 `node.isLeaf: true` 来表明是否为叶子结点。以此来告诉组件该节点是否有下一级子树'
          }
        ></Alert>
        <br />
        <Tree data={treeData} onLoadChildren={loadChildren}></Tree>
      </div>
    </>
  )
}

```

### editable.stories.tsx

```typescript
import React from 'react'
import Tree, { useTreeAction } from '@hi-ui/tree'
import { Modal } from '@hi-ui/modal'

/**
 * @title 编辑用法
 * @desc 通过树的节点进行新增、删除、编辑等操作
 */
export const Editable = () => {
  const ActionTree = useTreeAction(Tree)

  return (
    <>
      <h1>Editable for Tree</h1>
      <div className="tree-editable__wrap">
        <ActionTree
          expandOnSelect
          editPlaceholder="请填写菜单"
          menuOptions={[
            {
              type: 'addChildNode',
              title: '新建子节点',
            },
            {
              type: 'addSiblingNode',
              title: '新建兄弟节点',
            },
            {
              // type: 'deleteNode',
              title: '删除当前菜单',
              onClick(node, action) {
                action.closeMenu()

                Modal.confirm({
                  title: '提示',
                  content: '确定删除吗？',
                  onConfirm: () => {
                    action.deleteNode()
                  },
                })
              },
            },
            {
              type: 'editNode',
              title: '编辑当前菜单',
            },
            {
              title: 'Hello，自定义的菜单',
              onClick(node, action) {
                console.log(node)
                action.closeMenu()
              },
            },
          ]}
          data={[
            {
              id: 1,
              title: '小米',
              children: [
                {
                  id: 2,
                  title: '研发',
                  children: [
                    { id: 3, title: '后端' },
                    { id: 4, title: '运维' },
                    { id: 5, title: '前端' },
                  ],
                },
                { id: 6, title: '产品' },
              ],
            },
            {
              id: 11,
              title: '大米',
              children: [
                { id: 22, title: '可视化' },
                { id: 66, title: 'HiUI' },
              ],
            },
          ]}
        />
      </div>
    </>
  )
}

```

### expand-on-click.stories.tsx

```typescript
import React from 'react'
import Tree from '@hi-ui/tree'

/**
 * @title 选中时展开子节点
 */
export const ExpandOnSelect = () => {
  return (
    <>
      <h1>ExpandOnSelect for Tree</h1>
      <div className="tree-expand-on-click__wrap">
        <Tree
          expandOnSelect
          onSelect={console.log}
          data={[
            {
              id: 1,
              title: '小米',
              children: [
                {
                  id: 2,
                  title: '研发',
                  disabled: true,
                  children: [
                    { id: 3, title: '后端', disabled: true },
                    { id: 4, title: '运维' },
                    { id: 5, title: '前端' },
                  ],
                },
                { id: 6, title: '产品' },
              ],
            },
            {
              id: 11,
              title: '大米',
              children: [
                { id: 22, title: '可视化' },
                { id: 66, title: 'HiUI' },
              ],
            },
          ]}
        ></Tree>
      </div>
    </>
  )
}

```

### expand.stories.tsx

```typescript
import React from 'react'
import Tree from '@hi-ui/tree'

/**
 * @title 默认展开所有
 */
export const Expand = () => {
  return (
    <>
      <h1>Expand for Tree</h1>
      <div className="tree-expand__wrap">
        <Tree
          defaultExpandAll
          data={[
            {
              id: 1,
              title: '小米',
              children: [
                {
                  id: 2,
                  title: '研发',
                  children: [
                    { id: 3, title: '后端' },
                    { id: 4, title: '运维' },
                    { id: 5, title: '前端' },
                  ],
                },
                { id: 6, title: '产品' },
              ],
            },
            {
              id: 11,
              title: '大米',
              children: [
                { id: 22, title: '可视化' },
                { id: 66, title: 'HiUI' },
              ],
            },
          ]}
        ></Tree>
      </div>
    </>
  )
}

```

### icon-render.stories.tsx

```typescript
import React from 'react'
import Tree, { useTreeAction } from '@hi-ui/tree'
import { Modal } from '@hi-ui/modal'
import { FileOutlined, FolderOpenOutlined, FolderOutlined } from '@hi-ui/icons'

/**
 * @title 自定义 icon 渲染函数
 */
export const IconRender = () => {
  const ActionTree = useTreeAction(Tree)

  return (
    <>
      <h1>IconRender for Tree</h1>
      <div className="tree-icon-render__wrap">
        <ActionTree
          expandOnSelect
          editPlaceholder="请填写菜单"
          menuOptions={[
            {
              type: 'addChildNode',
              title: '新建子节点',
            },
            {
              type: 'addSiblingNode',
              title: '新建兄弟节点',
            },
            {
              // type: 'deleteNode',
              title: '删除当前菜单',
              onClick(node, action) {
                action.closeMenu()

                Modal.confirm({
                  title: '提示',
                  content: '确定删除吗？',
                  onConfirm: () => {
                    action.deleteNode()
                  },
                })
              },
            },
            {
              type: 'editNode',
              title: '编辑当前菜单',
            },
            {
              title: 'Hello，自定义的菜单',
              onClick(node, action) {
                console.log(node)
                action.closeMenu()
              },
            },
          ]}
          data={[
            {
              id: 1,
              title: '小米',
              children: [
                {
                  id: 2,
                  title: '研发',
                  children: [
                    { id: 3, title: '后端' },
                    { id: 4, title: '运维' },
                    { id: 5, title: '前端' },
                  ],
                },
                { id: 6, title: '产品' },
              ],
            },
            {
              id: 11,
              title: '大米',
              children: [
                { id: 22, title: '可视化' },
                { id: 66, title: 'HiUI' },
              ],
            },
          ]}
          iconRender={(node) => {
            if (!node.children?.length) {
              return <FileOutlined />
            }

            if (node.expanded) {
              return <FolderOpenOutlined />
            } else return <FolderOutlined />
          }}
        />
      </div>
    </>
  )
}

```

### scroll-to.stories.tsx

```typescript
import React from 'react'
import Tree, { TreeHelper } from '@hi-ui/tree'
import Button from '@hi-ui/button'

/**
 * @title 设置滚动位置
 * @desc 仅在设置 height 属性即虚拟列表下有效
 */
export const ScrollTo = () => {
  const treeRef = React.useRef<TreeHelper>(null)

  const [treeData] = React.useState(() => {
    function dig(path = '0', level) {
      const list: { title: string; id: string; children: any[] }[] = []

      for (let i = 0; i < 5; i += 1) {
        const id = `${path}-${i}`
        const treeNode = {
          title: id,
          id,
          children: [] as any[],
        }

        if (level > 0) {
          treeNode.children = dig(id, level - 1)
        }

        list.push(treeNode)
      }
      return list
    }

    const treeData = dig('0', 4)
    return treeData
  })

  return (
    <>
      <h1>ScrollTo for Tree</h1>
      <div className="tree-scroll-to__wrap">
        <Button
          onClick={() => {
            // key 为节点 id
            treeRef.current?.scrollTo?.({ key: '0-2-2-0-0', align: 'top' })
          }}
        >
          scroll to key: 0-2-2-0-0
        </Button>
        <Tree
          innerRef={treeRef}
          height={300}
          defaultExpandAll
          data={treeData}
          expandOnSelect
        ></Tree>
      </div>
    </>
  )
}

```

### search.stories.tsx

```typescript
import React from 'react'
import Tree, { useTreeSearch } from '@hi-ui/tree'

/**
 * @title 搜索用法
 * @desc 树的层级多、节点数量庞大，借助搜索工具快速找到结点
 */
export const Search = () => {
  const [data] = React.useState([
    {
      id: 1,
      title: '小米',
      children: [
        {
          id: 2,
          title: '研发',
          children: [
            { id: 3, title: '后端' },
            { id: 4, title: '运维' },
            { id: 5, title: '前端' },
          ],
        },
        { id: 6, title: '产品' },
      ],
    },
    {
      id: 11,
      title: '大米',
      children: [
        { id: 22, title: '可视化' },
        { id: 66, title: 'HiUI' },
      ],
    },
  ])

  const SearchTree = useTreeSearch(Tree)

  return (
    <>
      <h1>Search for Tree</h1>
      <div className="tree-search__wrap">
        <SearchTree searchable={true} searchPlaceholder={'搜索'} data={data} />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import Tree from '@hi-ui/tree'

/**
 * @title 设置尺寸
 */
export const Size = () => {
  return (
    <>
      <h1>Size for Tree</h1>
      <div className="tree-size__wrap">
        <div>
          <div>
            <h3>
              lg <small>默认</small>
            </h3>
            <Tree
              expandOnSelect
              data={[
                {
                  id: 1,
                  title: '小米',
                  children: [
                    {
                      id: 2,
                      title: '研发',
                      disabled: true,
                      children: [
                        { id: 3, title: '后端', disabled: true },
                        { id: 4, title: '运维' },
                        { id: 5, title: '前端' },
                      ],
                    },
                    { id: 6, title: '产品' },
                  ],
                },
                {
                  id: 11,
                  title: '大米',
                  children: [
                    { id: 22, title: '可视化' },
                    { id: 66, title: 'HiUI' },
                  ],
                },
              ]}
            />
          </div>
          <div>
            <h3>md</h3>
            <Tree
              expandOnSelect
              size="md"
              data={[
                {
                  id: 1,
                  title: '小米',
                  children: [
                    {
                      id: 2,
                      title: '研发',
                      disabled: true,
                      children: [
                        { id: 3, title: '后端', disabled: true },
                        { id: 4, title: '运维' },
                        { id: 5, title: '前端' },
                      ],
                    },
                    { id: 6, title: '产品' },
                  ],
                },
                {
                  id: 11,
                  title: '大米',
                  children: [
                    { id: 22, title: '可视化' },
                    { id: 66, title: 'HiUI' },
                  ],
                },
              ]}
            />
          </div>
          <div>
            <h3>sm</h3>
            <Tree
              expandOnSelect
              size="sm"
              data={[
                {
                  id: 1,
                  title: '小米',
                  children: [
                    {
                      id: 2,
                      title: '研发',
                      disabled: true,
                      children: [
                        { id: 3, title: '后端', disabled: true },
                        { id: 4, title: '运维' },
                        { id: 5, title: '前端' },
                      ],
                    },
                    { id: 6, title: '产品' },
                  ],
                },
                {
                  id: 11,
                  title: '大米',
                  children: [
                    { id: 22, title: '可视化' },
                    { id: 66, title: 'HiUI' },
                  ],
                },
              ]}
            />
          </div>
        </div>
      </div>
    </>
  )
}

```

### virtual-list.stories.tsx

```typescript
import React from 'react'
import Tree from '@hi-ui/tree'

/**
 * @title 大数据
 */
export const VirtualList = () => {
  // 模拟 10^4 个数据量
  const [treeData] = React.useState(() => {
    function dig(path = '0', level) {
      const list = []
      for (let i = 0; i < 10; i += 1) {
        const id = `${path}-${i}`
        const treeNode = {
          title: id,
          id,
          children: [] as any[],
        }

        if (level > 0) {
          treeNode.children = dig(id, level - 1)
        }

        list.push(treeNode)
      }
      return list
    }

    const treeData = dig('0', 4)
    return treeData
  })

  return (
    <>
      <h1>VirtualList for Tree</h1>
      <div className="tree-virtual-list__wrap">
        <Tree height={300} data={treeData}></Tree>
      </div>
    </>
  )
}

```

## tree-select 组件

### appearance.stories.tsx

```typescript
import React from 'react'
import TreeSelect from '@hi-ui/tree-select'

/**
 * @title 不同UI风格
 * @desc UI风格包括线性、面性、无UI三种
 */
export const Appearance = () => {
  const [value, setValue] = React.useState<React.ReactText>('0')
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Appearance</h1>
      <div className="tree-select-appearance__wrap">
        <div>
          <h2>filled</h2>
          <TreeSelect
            data={data}
            value={value}
            clearable
            appearance="filled"
            onChange={(value, selectItems) => {
              console.log('TreeSelect onChange: ', value, selectItems)
              setValue(value)
            }}
          />
        </div>

        <div>
          <h2>outline</h2>
          <TreeSelect
            data={data}
            value={value}
            clearable
            appearance="line"
            onChange={(value, selectItems) => {
              console.log('TreeSelect onChange: ', value, selectItems)
              setValue(value)
            }}
          />
        </div>

        <div>
          <h2>unset</h2>
          <TreeSelect
            data={data}
            value={value}
            clearable
            appearance="unset"
            // 取消下拉框匹配 input 触发器的宽度
            overlay={{ matchWidth: false }}
            onChange={(value, selectItems) => {
              console.log('TreeSelect onChange: ', value, selectItems)
              setValue(value)
            }}
          />
        </div>
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import TreeSelect from '@hi-ui/tree-select'

/**
 * @title 基础用法
 * @desc 展示从多个收起的备选项中选出的一个选项
 */
export const Basic = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Basic</h1>
      <div className="tree-select-basic__wrap">
        <TreeSelect
          data={data}
          onChange={(checkedIds, selectItem) => {
            console.log('TreeSelect onChange: ', checkedIds, selectItem)
          }}
        />
      </div>
    </>
  )
}

```

### clearable.stories.tsx

```typescript
import React from 'react'
import TreeSelect from '@hi-ui/tree-select'

/**
 * @title 清空选中项
 */
export const Clearable = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Clearable</h1>
      <div className="tree-select-clearable__wrap">
        <TreeSelect
          clearable
          data={data}
          onChange={(checkedIds, selectItem) => {
            console.log('TreeSelect onChange: ', checkedIds, selectItem)
          }}
        />
      </div>
    </>
  )
}

```

### controlled.stories.tsx

```typescript
import React from 'react'
import TreeSelect from '@hi-ui/tree-select'

/**
 * @title 受控
 */
export const Controlled = () => {
  const [value, setValue] = React.useState<React.ReactText>('0')
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      disabled: true,
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Controlled</h1>
      <div className="tree-select-controlled__wrap">
        <TreeSelect
          data={data}
          value={value}
          onChange={(value, selectItems) => {
            console.log('TreeSelect onChange: ', value, selectItems)
            setValue(value)
          }}
        />
      </div>
    </>
  )
}

```

### custom-render.stories.tsx

```typescript
import React from 'react'
import TreeSelect from '@hi-ui/tree-select'
import Input from '@hi-ui/input'

/**
 * @title 自定义触发器
 */
export const CustomRender = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>CustomRender</h1>
      <div className="tree-select-custom-render__wrap">
        <TreeSelect
          data={data}
          onChange={(checkedIds, selectItem) => {
            console.log('TreeSelect onChange: ', checkedIds, selectItem)
          }}
          customRender={(data) => {
            return <Input value={!data ? '' : data.title + ''} placeholder="请选择" />
          }}
        />
      </div>
    </>
  )
}

```

### default-expand-all.stories.tsx

```typescript
import React from 'react'
import TreeSelect from '@hi-ui/tree-select'

/**
 * @title 默认展开全部
 */
export const DefaultExpandAll = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>DefaultExpandAll</h1>
      <div className="tree-select-default-expand-all__wrap">
        <TreeSelect
          data={data}
          defaultExpandAll
          onChange={(checkedIds, checkedNode) => {
            console.log('TreeSelect onChange: ', checkedIds, checkedNode)
          }}
        />
      </div>
    </>
  )
}

```

### searchable.stories.tsx

```typescript
import React from 'react'
import TreeSelect from '@hi-ui/tree-select'

/**
 * @title 带搜索
 */
export const Searchable = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  // 注意 filterOption 是影响搜索渲染的，是完全受控的，useCallback 包裹可以减少无效的重渲染，提升性能
  const filterOptionMemo = React.useCallback((keyword: string, item: any) => {
    console.log(keyword, item)

    const match = (node: any) =>
      typeof node.title === 'string' && node.title.indexOf(keyword) !== -1

    const matchUp = (node: any) => {
      let found = match(node)
      const { children } = node

      if (children && !found) {
        found = children.some((item: any) => matchUp(item))
      }

      return found
    }

    return matchUp(item)
  }, [])

  return (
    <>
      <h1>Searchable</h1>
      <div className="tree-select-searchable__wrap">
        <h2>highlight</h2>
        <TreeSelect
          data={data}
          searchable
          searchMode="highlight"
          onChange={(checkedIds, checkedNode) => {
            console.log('TreeSelect onChange: ', checkedIds, checkedNode)
          }}
        />

        <h2>filter</h2>
        <TreeSelect
          data={data}
          searchable
          searchMode="filter"
          onChange={(checkedIds, checkedNode) => {
            console.log('TreeSelect onChange: ', checkedIds, checkedNode)
          }}
        />

        <h2>custom filter</h2>
        <TreeSelect
          data={data}
          searchable
          filterOption={filterOptionMemo}
          onChange={(checkedIds, checkedNode) => {
            console.log('TreeSelect onChange: ', checkedIds, checkedNode)
          }}
        />
      </div>
    </>
  )
}

```

### size.stories.tsx

```typescript
import React from 'react'
import TreeSelect from '@hi-ui/tree-select'

/**
 * @title 不同尺寸
 */
export const Size = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Size</h1>
      <div className="tree-select-size__wrap">
        <h2>sm</h2>
        <TreeSelect
          size="sm"
          data={data}
          onChange={(checkedIds, selectItem) => {
            console.log('TreeSelect onChange: ', checkedIds, selectItem)
          }}
        />
        <h2>md</h2>
        <TreeSelect
          size="md"
          data={data}
          onChange={(checkedIds, selectItem) => {
            console.log('TreeSelect onChange: ', checkedIds, selectItem)
          }}
        />
        <h2>lg</h2>
        <TreeSelect
          size="lg"
          data={data}
          onChange={(checkedIds, selectItem) => {
            console.log('TreeSelect onChange: ', checkedIds, selectItem)
          }}
        />
      </div>
    </>
  )
}

```

### uncontrolled.stories.tsx

```typescript
import React from 'react'
import TreeSelect from '@hi-ui/tree-select'

/**
 * @title 非受控
 */
export const Uncontrolled = () => {
  const [data] = React.useState([
    {
      title: '手机类',
      id: '0',
      disabled: true,
      children: [
        {
          title: 'Redmi系列',
          id: '0-0',
          children: [
            {
              id: '0-0-1',
              title: 'Redmi K30',
            },
            {
              id: '0-0-2',
              title: 'Redmi K30 Pro',
            },
            {
              id: '0-0-3',
              title: 'Redmi 10X 5G',
            },
            {
              id: '0-0-4',
              title: 'Redmi Note 8',
            },
            {
              id: '0-0-5',
              title: 'Redmi 9',
            },
            {
              id: '0-0-6',
              title: 'Redmi 9A',
            },
          ],
        },
        {
          title: '小米手机',
          id: '0-1',
          children: [
            {
              id: '0-1-1',
              title: '小米10 Pro',
            },
            {
              id: '0-1-2',
              title: '小米10',
            },
            {
              id: '0-1-3',
              title: '小米10 青春版 5G',
            },
            {
              id: '0-1-4',
              title: '小米MIX Alpha',
            },
          ],
        },
      ],
    },
    {
      title: '电视',
      id: '1',
      children: [
        {
          title: '小米电视 大师 65英寸OLED',
          id: '1-0',
        },
        {
          title: 'Redmi 智能电视 MAX 98',
          id: '1-1',
        },
        {
          title: '小米电视4A 60英寸',
          id: '1-2',
        },
      ],
    },
  ])

  return (
    <>
      <h1>Uncontrolled</h1>
      <div className="tree-select-uncontrolled__wrap">
        <TreeSelect
          data={data}
          defaultValue={'1-2'}
          // defaultValue={defaultValue}
          onChange={(selectedId, selectedItem) => {
            console.log('TreeSelect onChange: ', selectedId, selectedItem)
          }}
        />
      </div>
    </>
  )
}

```

### virtual-list.stories.tsx

```typescript
import React from 'react'
import TreeSelect from '@hi-ui/tree-select'

/**
 * @title 大数据
 */
export const VirtualList = () => {
  const [data] = React.useState(() => {
    // 模拟 10^4 个数据量
    function dig(path = '0', level) {
      const list = []
      for (let i = 0; i < 10; i += 1) {
        const id = `${path}-${i}`
        const treeNode = {
          title: id,
          id,
          children: [] as any[],
        }

        if (level > 0) {
          treeNode.children = dig(id, level - 1)
        }

        list.push(treeNode)
      }
      return list
    }

    const treeData = dig('0', 4)
    return treeData
  })

  return (
    <>
      <h1>virtualList</h1>
      <div className="check-tree-select-virtual-list__wrap">
        <TreeSelect data={data} onChange={console.log} virtual height={260} />
      </div>
    </>
  )
}

```

## upload 组件

### action-render.stories.tsx

```typescript
import React from 'react'
import Upload from '@hi-ui/upload'

/**
 * @title 自定义渲染操作区
 */
export const ActionRender = () => {
  return (
    <>
      <h1>ActionRender</h1>
      <div className="upload-action-render__wrap">
        <Upload
          type="default"
          uploadAction="https://jsonplaceholder.typicode.com/posts/"
          tips="仅支持 jpg/png 文件，且不超过 500kb"
          accept="image/png,image/jpg"
          headers={{ name: 'mi' }}
          defaultFileList={[
            {
              name: 'a.png',
              fileType: 'img', // 文件类型，可取值img, zip, word, pdf, ppt, excel, other
              uploadState: 'success', // 上传状态，可取值success, error
              url: 'https://i8.mifile.cn/a1/pms_1531116957.78852376.jpg',
            },
            {
              name: 'b.png',
              fileType: 'img',
              uploadState: 'error',
              url: 'https://i1.mifile.cn/f/i/2018/mix3/specs_black.png',
            },
          ]}
          name={'files[]'}
          onChange={(file, fileList, response) => {
            console.log('upload callback', file, fileList, response)
            // if(response&&response.status !== 200) return false // 返回 false 则该文件会从列表里删除
          }}
          actionRender={({ file }) => {
            return <span>{file.uploadState === 'loading' ? '加载中' : '删除'}</span>
          }}
        />
      </div>
    </>
  )
}

```

### async-upload-action.stories.tsx

```typescript
import React from 'react'
import Upload from '@hi-ui/upload'

/**
 * @title 上传前的处理
 * @desc uploadAction 接收一个函数，返回一个 Promise
 */
export const AsyncUploadAction = () => {
  return (
    <>
      <h1>AsyncUploadAction</h1>
      <div className="upload-before-uplod__wrap">
        <h2>异步的 UploadAction</h2>
        <Upload
          type="default"
          uploadAction={() => {
            console.log('上传前的处理')
            return new Promise((resolve) => {
              setTimeout(() => resolve('https://jsonplaceholder.typicode.com/posts/'), 1000)
            })
          }}
          tips="仅支持 jpg/png 文件，且不超过 500kb"
          accept="image/png,image/jpg"
          headers={{ name: 'mi' }}
          multiple
          data={[]}
          name={'files[]'}
          onChange={(file, fileList, response) => {
            console.log('upload callback', file, fileList, response)
            // if(response&&response.status !== 200) return false // 返回 false 则该文件会从列表里删除
          }}
          disabled={false}
        />
      </div>
    </>
  )
}

```

### avatar.stories.tsx

```typescript
import React from 'react'
import Upload from '@hi-ui/upload'

/**
 * @title 头像上传
 * @desc 与其它组件配合使用，常见于名片、通讯录、账号管理等
 */
export const Avatar = () => {
  return (
    <>
      <h1>Avatar</h1>
      <div className="upload-avatar__wrap">
        <Upload
          type="avatar"
          uploadAction="http://www.mocky.io/v2/5dc3b4413000007600347501"
          headers={{ name: 'mi' }}
          data={{ id: 'uid', channel: 'youpin' }}
          onChange={(file, fileList, response) => {
            console.log('upload callback', file, fileList, response)
          }}
          onRemove={(file, fileList, index) => {
            console.log('remove callback', file, fileList, index)
            return new Promise((resolve) => resolve(true))
          }}
          name="uploadAvatar"
        />
      </div>
    </>
  )
}

```

### basic.stories.tsx

```typescript
import React from 'react'
import Upload from '@hi-ui/upload'

/**
 * @title 基础用法
 * @desc 突出上传附件的操作入口，节省页面空间
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div className="upload-basic__wrap">
        <Upload
          type="default"
          uploadAction="https://jsonplaceholder.typicode.com/posts/"
          tips="仅支持 jpg/png 文件，且不超过 500kb"
          accept="image/png,image/jpg"
          headers={{ name: 'mi' }}
          data={[]}
          defaultFileList={[
            {
              name: 'a.png',
              fileType: 'img', // 文件类型，可取值img, zip, word, pdf, ppt, excel, other
              uploadState: 'success', // 上传状态，可取值success, error
              url: 'https://i8.mifile.cn/a1/pms_1531116957.78852376.jpg',
            },
            {
              name: 'b.png',
              fileType: 'img',
              uploadState: 'error',
              url: 'https://i1.mifile.cn/f/i/2018/mix3/specs_black.png',
            },
          ]}
          name={'files[]'}
          onChange={(file, fileList, response) => {
            console.log('upload callback', file, fileList, response)
            // if(response&&response.status !== 200) return false // 返回 false 则该文件会从列表里删除
          }}
          disabled={false}
        />
      </div>
    </>
  )
}

```

### custom-upload.stories.tsx

```typescript
import React from 'react'
import Upload, { UploadFileItem } from '@hi-ui/upload'

/**
 * @title 自定义上传
 * @desc 完全自定义上传逻辑，适合复杂上传逻辑场景
 */
export const CustomUpload = () => {
  const [fileList, setFileList] = React.useState<UploadFileItem[]>([
    {
      name: 'a.png',
      fileType: 'img', // 文件类型，可取值img, zip, word, pdf, ppt, excel, other
      uploadState: 'success', // 上传状态，可取值success, error
    },
    {
      name: 'b.png',
      fileType: 'img',
      uploadState: 'error',
    },
  ])

  return (
    <>
      <h1>CustomUpload</h1>
      <div className="upload-custom-upload__wrap">
        <Upload
          type="default"
          customUpload={(files) => {
            const nextFileList = fileList.concat({
              name: files[0].name,
              fileType: files[0].name.slice(files[0].name.lastIndexOf('.') + 1).toLowerCase(),
              uploadState: 'success',
            })

            setFileList(nextFileList)
          }}
          content="上传文件"
          fileList={fileList}
        />
      </div>
    </>
  )
}

```

### draggable.stories.tsx

```typescript
import React from 'react'
import Upload from '@hi-ui/upload'

/**
 * @title 拖拽上传
 * @desc 附件上传的区域固定且宽敞，上传附件数量较多，拖拽可有效提高效率
 */
export const Draggable = () => {
  return (
    <>
      <h1>Draggable</h1>
      <div className="upload-draggable__wrap">
        <Upload
          type="drag"
          uploadAction="http://www.mocky.io/v2/5dc3b4413000007600347501"
          headers={{ name: 'mi' }}
          accept=".png,.jpg,.jpeg"
          onChange={(file, fileList, response) => {
            console.log('upload callback', file, fileList, response)
          }}
          tips="仅支持 jpg/png 文件，且不超过 500kb"
          data={{ id: 'uid', channel: 'youpin' }}
          name={'files[]'}
          multiple={true}
        />
      </div>
    </>
  )
}

```

### photo.stories.tsx

```typescript
import React from 'react'
import Upload from '@hi-ui/upload'

/**
 * @title 照片墙上传
 * @desc 展示一组照片内容
 */
export const Photo = () => {
  return (
    <>
      <h1>Photo</h1>
      <div className="upload-photo__wrap">
        <Upload
          type="photo"
          uploadAction="http://www.mocky.io/v2/5dc3b4413000007600347501"
          onChange={(file, fileList, response) => {
            console.log('upload callback', file, fileList, response)
          }}
          onRemove={(file, fileList, index) => {
            console.log('remove callback', file, fileList, index)
            return new Promise((resolve) => resolve(true))
          }}
          defaultFileList={[
            {
              name: 'a.png',
              fileType: 'img', // 文件类型，可取值img, zip, word, pdf, ppt, excel, other
              uploadState: 'success', // 上传状态，可取值success, error
              url: 'https://i8.mifile.cn/a1/pms_1531116957.78852376.jpg',
            },
            {
              name: 'b.png',
              fileType: 'img',
              uploadState: 'error',
              url: 'https://i1.mifile.cn/f/i/2018/mix3/specs_black.png',
            },
          ]}
          data={{ id: 'uid', channel: 'youpin' }}
          name={'files[]'}
        />
      </div>
    </>
  )
}

```

### picture-card.stories.tsx

```typescript
import React from 'react'
import Upload from '@hi-ui/upload'

/**
 * @title 卡片图片
 */
export const PictureCard = () => {
  return (
    <>
      <h1>PictureCard</h1>
      <div className="upload-picture-list__wrap">
        <Upload
          type="pictureCard"
          uploadAction="http://www.mocky.io/v2/5dc3b4413000007600347501"
          headers={{ name: 'mi' }}
          onChange={(file, fileList, response) => {
            console.log('upload callback', file, fileList, response)
          }}
          content="上传文件"
          data={{ id: 'uid', channel: 'youpin' }}
          name="pictureCard"
        />
      </div>
    </>
  )
}

```

### single-import.stories.tsx

```typescript
import React from 'react'
import { NormalUpload, DragUpload, PictureUpload, PictureListUpload, AvatarUpload } from '@hi-ui/upload'

/**
 * @title 单个导入，按需引用
 * @desc 建议采用该方式引用，有利用打包时做 Tree Shaking
 */
export const SingleImport = () => {
  return (
    <>
      <h1>SingleImport</h1>
      <div className="upload-single-import__wrap">
        <NormalUpload
          uploadAction="https://jsonplaceholder.typicode.com/posts/"
          tips="仅支持 jpg/png 文件，且不超过 500kb"
          accept="image/png,image/jpg"
          headers={{ name: 'mi' }}
          name={'files[]'}
          onChange={(file, fileList, response) => {
            console.log('upload callback', file, fileList, response)
          }}
        />
      </div>
    </>
  )
}

```

## watermark 组件

### basic.stories.tsx

```typescript
import React from 'react'
import Watermark from '@hi-ui/watermark'

/**
 * @title 基础用法
 */
export const Basic = () => {
  return (
    <>
      <h1>Basic</h1>
      <div
        className="watermark-basic__wrap"
        style={{ height: 402, minWidth: 660, position: 'relative', zIndex: 0 }}
      >
        <Watermark content={['HiUI', '做中台，就用 HiUI']}></Watermark>
      </div>
    </>
  )
}

```

### container.stories.tsx

```typescript
import React, { useState } from 'react'
import Watermark from '@hi-ui/watermark'
import { Button } from '@hi-ui/button'

/**
 * @title 指定容器
 * @desc 指定要挂载水印的容器位置
 */
export const Container = () => {
  const [mounted, setMounted] = useState<any>(false)

  return (
    <>
      <h1>Container</h1>
      <div className="watermark-container__wrap" style={{ height: 402, minWidth: 660 }}>
        <Button
          type="primary"
          onClick={() => {
            setMounted(!mounted)
          }}
        >
          {mounted ? '取消挂载水印到全局' : '挂载水印到全局'}
        </Button>
      </div>
      {mounted ? (
        <Watermark
          style={{
            pointerEvents: 'none',
            position: 'fixed',
            top: 0,
            right: 0,
            bottom: 0,
            left: 0,
            zIndex: 2048,
          }}
          content={['HiUI', '做中台，就用 HiUI']}
          container={document.body}
          allowCopy={true}
        />
      ) : null}
    </>
  )
}

```

### density.stories.tsx

```typescript
import React from 'react'
import Watermark from '@hi-ui/watermark'

/**
 * @title 自定义疏密度
 * @desc 通过 density 设置水印的疏密度
 */
export const Density = () => {
  return (
    <>
      <h1>Density</h1>
      <div
        className="watermark-density__wrap"
        style={{ height: 402, minWidth: 660, position: 'relative', zIndex: 0 }}
      >
        <Watermark density="low" content={['HiUI', '做中台，就用 HiUI']}></Watermark>
      </div>
    </>
  )
}

```

## zen-mode 组件

### basic.stories.tsx

```typescript
import React, { useState } from 'react'
import ZenMode from '@hi-ui/zen-mode'
import { Button } from '@hi-ui/button'

/**
 * @title 基础用法
 */
export const Basic = () => {
  const [visible, setVisible] = useState(false)
  return (
    <>
      <h1>Basic for ZenMode</h1>
      <div className="zen-mode-basic__wrap">
        <Button
          style={{ marginBottom: 10 }}
          onClick={() => {
            setVisible(true)
          }}
        >
          开启禅模式
        </Button>

        <ZenMode
          visible={visible}
          onBack={() => {
            setVisible(false)
          }}
          toolbar={[
            <Button
              key="btn"
              onClick={() => {
                setVisible(false)
              }}
            >
              退出演示
            </Button>,
          ]}
        >
          <div
            style={{ fontSize: 14, textAlign: 'center', backgroundColor: '#F5F7FA', padding: 16 }}
          >
            <div style={{ fontWeight: 600, lineHeight: '32px' }}>我是大标题</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
            <div>我是禅模式测试的文本内容</div>
          </div>
        </ZenMode>
      </div>
    </>
  )
}

```



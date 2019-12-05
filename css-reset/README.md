# [minireset.css](https://github.com/jgthms/minireset.css/blob/master/minireset.css)

关于CSSReset，确实令人纠结。其实都大同小异，之前也分析过好几个不同的reset.css。最后还是选择了这个，主要是轻量。

针对个人使用，我还会基于这个进行补充：

```css
a {
  color: #333;
  text-decoration: none;
}

a:hover {
  opacity: 0.9;
}

.clearfix::after {
  display: block;
  clear: both;
  content: '';
}

.float-left {
  float: left;
}

.float-right {
  float: right;
}

.huge-txt {
  font-size: 40px;
}

.big-txt {
  font-size: 30px;
}
```

以及部分规范：

```scss
/* normal font size */
$size: (
  sm: 12px, nm: 14px, md: 16px, lg: 20px, xl: 24px
);
@each $key, $val in $size {
  .fs-#{$key} {
    font-size: $val;
    line-height: $val + 8px;
  }
};

/* font color */
$cf-light: #B6B6B6;
$cf-gray: rgba(47, 56, 67, 0.6);
$cf-med: rgba(47, 56, 67, 1);
$cf-dark: #333333;
$cf-highlight: #1775F0;
$cf-highlight-hover: #57A0FF;

/* border color */
$cb-light: #E3E6E9;

/* charts color for notes */
$color-chart: #3AA0FF, #36CBCB, #4DCB73, #FAD337, #F2637B, #975FE4, #3FC3FF, #2EE7B0, #6DDE79, #FF9652, #F04BB1, #6966E8;
```

> Inspired from [bootstrap](https://getbootstrap.com/docs/4.4/getting-started/introduction/)

## Other

* [modern-css-reset](https://github.com/hankchizljaw/modern-css-reset/blob/master/src/reset.css)：除了上面的minireset.css，这个备选可能会更好（个人感觉倾向移动端），作者还有篇配文[A Modern CSS Reset](https://hankchizljaw.com/wrote/a-modern-css-reset/)(1st October 2019)
* [marx.css](https://github.com/mblode/marx/blob/master/css/marx.css)：过于复杂
* [ress](https://github.com/filipelinhares/ress/blob/master/ress.css)：过于复杂
* [normalize.css](https://github.com/necolas/normalize.css/blob/master/normalize.css)：用于标准化，其实不属于reset

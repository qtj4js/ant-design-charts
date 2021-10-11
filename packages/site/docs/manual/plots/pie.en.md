

## title: Pie&#xA;order: 6

<div class="manual-docs">
  <div data-card-type="block" data-lake-card="table" id="pLwYV" class="">
    <table
      class="lake-table"
      style="width: 100%; outline: none; border-collapse: collapse"
    >
      <colgroup>
        <col width="425" span="1" />
        <col width="340" span="1" />
      </colgroup>
      <tbody>
        <tr style="height: 33px">
          <td colspan="1" rowspan="5" style="background: #fff">
            <playground path="pie/basic/demo/basic.ts"></playground>
          </td>
          <td class="style1">
            <p><strong>定义</strong></p>
            <p>
              <span class="lake-fontsize-12"
                >通过扇形区块的颜色和弧长（角度、面积）来展现数据的分类和占比情况。</span
              >
            </p>
          </td>
        </tr>
        <tr style="height: 33px">
          <td class="style1">
            <p><strong>何时使用</strong></p>
            <p><span class="lake-fontsize-12">饼图通过扇形区块的面积，弧度和颜色等视觉标记，展现数据的分类和占比情况。它的特点是展现部分与部分之间，以及部分与整体的关系。部分相加之和等于整体的 100%，用整圆表示。</span></p>
          </td>
        </tr>
        <tr style="height: 33px">
          <td class="style1">
            <p><strong>视觉通道</strong></p>
            <p><span class="lake-fontsize-12">弧长</span></p>
          </td>
        </tr>
        <tr style="height: 33px">
          <td colspan="1">
            <p><strong>分析目的</strong></p>
            <p><span class="lake-fontsize-12">比较、组成、占比</span></p>
          </td>
        </tr>
        <tr style="height: 33px">
          <td colspan="1">
            <p><strong>数据准备</strong></p>
            <p>
              <span class="lake-fontsize-12">1 个「无序名词」字段</span>
            </p>
            <p><span class="lake-fontsize-12">1 个「数值」字段</span></p>
          </td>
        </tr>
      </tbody>
    </table>
  </div>

## Design Guide

### 用法建议

<p style="margin: 24px 0 8px;"><strong>💡 分类数不超过 9 个</strong></p>

<img alt="design" src='https://gw.alipayobjects.com/mdn/rms_d314dd/afts/img/A*JRd_TLOoVhgAAAAAAAAAAABkARQnAQ' width='600'>

<p style="margin: 24px 0 8px;"><strong>💡 将多个极小值合并展示</strong></p>

<img alt="design" src='https://gw.alipayobjects.com/mdn/rms_d314dd/afts/img/A*-0l7QLDcs2QAAAAAAAAAAABkARQnAQ' width='600'>

<p style="margin: 24px 0 8px;"><strong>💡 排列顺序</strong></p>

<img alt="design" src='https://gw.alipayobjects.com/mdn/rms_d314dd/afts/img/A*RQ4ARoHq2VoAAAAAAAAAAABkARQnAQ' width='600'>

<p style="margin: 24px 0 8px;"><strong>💡 如果每个数值的差异不大，那么不建议使用饼图</strong></p>

<img alt="design" src='https://gw.alipayobjects.com/mdn/rms_d314dd/afts/img/A*C0prR7ZpOdcAAAAAAAAAAABkARQnAQ' width='600'>

<p style="margin: 24px 0 8px;"><strong>💡 何时将标签放在内部/外部</strong></p>

<img alt="design" src='https://gw.alipayobjects.com/mdn/rms_d314dd/afts/img/A*elfETrq8NDcAAAAAAAAAAABkARQnAQ' width='600'>

<p style="margin: 24px 0 8px;"><strong>💡 所有的项目相加之和为 100%</strong></p>

<img alt="design" src='https://gw.alipayobjects.com/mdn/rms_d314dd/afts/img/A*tk2zTqTyMvEAAAAAAAAAAABkARQnAQ' width='600'>

### 元素

<img alt="design" src='https://gw.alipayobjects.com/mdn/rms_d314dd/afts/img/A*rUSJQJmhtQ8AAAAAAAAAAABkARQnAQ' width='800'>

<div class="design-guide-list">

*   图形(Element)：饼图由扇形组成，环图由滑块组成。
*   图形标签(Label)：显示各个区块的占比（%），名称（华东、华南、华北）和实际数值（123.45）。
*   复合指标：在环图中心位置处显示，或以指标卡形式显示在图表上部分，。
*   图形辅助组件(Info Component)：图例，tooltip 或者指标卡等的组件支持。

</div>

## Quick start

<div class='sign'>

```ts
import React, { useState, useEffect } from 'react';
import {  } from '@ant-design/charts';

const Demo: React.FC = () => {
  
  return < {...config} />;
};

export default Demo;


```

</div>

📊 See more <a href="/en/examples/pie/basic" target='blank'>examples</a>.

🎨 For an overview of the pie plot options see the [API reference](/en/docs/api/plots/pie).

## Pie plot features

### Donut (Ring) pie

With G2Plot, you can set the `innerRadius` to create concentric ring.

<playground path='pie/donut/demo/basic.ts' rid='rect2'></playground>

### Fan chart

By setting startAngle and endAngle, we can turn a pie plot into a fan chart.

<playground path='pie/basic/demo/quarter-circle.ts' rid='rect3'></playground>

</div>
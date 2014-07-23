---
layout: page
title: "九型人格测试"
date: 2014-07-23 00:47
comments: false
sharing: false
footer: false
---

<script type="text/javascript" src="/javascripts/libs/jquery-1.8.3.min.js"></script>
<script type="text/javascript" src="/javascripts/libs/jquery.jqplot.min.js"></script>


<script type="text/javascript" src="/javascripts/libs/jqplot.donutRenderer.min.js"></script>
<script type="text/javascript" src="/javascripts/libs/jqplot.pieRenderer.min.js"></script>

<script type="text/javascript" src="/javascripts/sunny/personalityTestData.js"></script>
<script type="text/javascript" src="/javascripts/sunny/personalityTest.js"></script>

<link rel="stylesheet" type="text/css" href="/stylesheets/libs/jquery.jqplot.min.css" />
<link rel="stylesheet" type="text/css" href="/stylesheets/sunny/personalityTest.css" />

<!--Page Content-->
<div id = "question-notice" class="fixed-width">
    <ul>
        <li>答题填写方法:
            <ol>
                <li>两者择一，如果两个答案都不是很确定，就选较为接近的一个答案。</li>
                <li>在选定答案的代码上，打“√”,比如第一题,如果选择“我需要向人表示关怀……A”则在“A”上打“√”。</li>
            </ol>
        </li>
        <li>请按自己的现况，诚实，坦白完成问卷，不用分析问题。</li>
        <li>建议用45分钟完成问卷</li>
    </ul>
</div>
<div id = "result-notice" class="fixed-width">
    <h1>诺亚财富管理中心-性格测试结果</h1>
</div>
<div id="results-chart"></div>
<div id="questions" class="fixed-width"></div>
<div id="results" class="fixed-width"></div>
<div id="action-form" class="fixed-width">
    <div id="result-buttons">
        <input id="restart" type="button" value="重新测试"></input>
    </div>
    <div id="question-buttons">
        <input id="reset" type="button" value="清空结果"></input>
        <input id="random-input" type="button" value="随机填写"></input>
        <input id="submit-result" type="button" value="提交测试"></input>
    </div>
</div>
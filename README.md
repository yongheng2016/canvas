[https://yuque.com/airing/canvas/readme](https://yuque.com/airing/canvas/readme)

        <li class="title">canvas是行内元素</li>
        <li>
            <span class="title">设置画布大小只有两种方法</span>
            <ul>
                <li>在canvas标签中设置</li>
                <li>在JS代码中更改canvas属性值</li>
            </ul>
        </li>
        <li>
            <span class="title">canvas使用：</span>
            <ul>
                <li>布置画布：添加
                    <code>canvas</code>标签元素</li>
                <li>获取画布：通过
                    <code>canvas</code>标签id，获取canvas对象</li>
                <li>获取画笔：通过canvas对象的
                    <code>getContext("2d")</code>方法，获取2D环境</li>
            </ul>
        </li>
        <li class="title">canvas绘制都数值都基于px值</li>
        <li>
            <span class="title">路径（线、弧形、等）闭合：</span>
            <br>
            <span>当你调用
                <code>fill()</code>函数时，所有没有闭合的形状都会自动闭合，所以你不需要调用
                <code>closePath()</code>函数。但是调用
                <code>stroke()</code>时不会自动闭合。</span>
        </li>
        <li>
            <span class="title">绘制图形：(canvas是基于状态的绘制，即向做好绘制计划，最后染色绘制)</span>
            <ul>
                <li>移动画笔
                    <code>moveTo</code>
                </li>
                <li>
                    <span>绘制计划</span>
                    <ul>
                        <li>线段：
                            <code>lineTo(x,y)</code>
                        </li>
                        <li>矩形：
                            <code>fillRect(x, y, width, height)</code>
                            <code>strokeRect(x, y, width, height)</code>
                        </li>
                        <li>
                            圆弧：
                            <code>arc(x, y, radius, startAngle, endAngle, anticlockwise)</code>
                        </li>
                        <ul>
                            <li>
                                <code>（x,y）</code>为圆心</li>
                            <li>
                                <code>radius</code>为半径</li>
                            <li>从startAngle开始到endAngle结束</li>
                            <li>anticlockwise(逆时针))给定方向（默认false，即顺时针）</li>
                        </ul>
                        <li>
                            二次贝塞尔曲线及三次贝塞尔曲线
                            <ul>
                                <li>二次：<code>quadraticCurveTo(cp1x, cp1y, x, y)</code></li>
                                <li>三次：<code>bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)</code></li>
                            </ul>
                        </li>
                        <li>
                            <span>Path2D对象</span><br>
                            <code>new Path2D();     // 空的Path对象</code><br>
                            <code>new Path2D(path); // 克隆Path对象</code><br>
                            <code>new Path2D(d);    // 从SVG建立Path对象</code>
                        </li>
                        <li>SVG paths</li>
                    </ul>

                </li>
                <li>设置画笔样式</li>
                <li>
                    <span>确定绘制：</span>
                    <ul>
                        <li>
                            <code>fill()</code> 填充</li>
                        <li>
                            <code>stroke()</code> 描边</li>
                    </ul>
                </li>
            </ul>
        </li>
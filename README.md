# F013  vue+flask租房可视化大数据可视化系统
完整项目收费，可联系微信: mmdsj186011 注明从git来的，谢谢！
也可以关注我的B站： 麦麦大数据 https://space.bilibili.com/1583208775

## 视频网址

[video(video-AS5Lfze4-1756351684230)(type-bilibili)(url-https://player.bilibili.com/player.html?aid=470408527)(image-https://i-blog.csdnimg.cn/img_convert/edc79311fe4e9376b7da30bde23e531d.png)(title-【vue+flask】 python 租房大数据可视化技术 echarts  mysql)]
### **1 技术架构**

- **前端技术栈：** Vue.js 与 Echarts
- **后端框架：** Flask
- **开发语言：** Python3
- **数据库：** MySQL
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/bcb236a2653b43ccbe8594dac316e194.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/afbc4fe233494ae8aa8764830c5ba2b6.png)

### **2 项目功能概述**
本项目旨在对从链家平台爬取到的数万**条区域的租房数据**进行可视化展示与深度分析。核心功能基于Echarts图表库，并融合了多种交互式展示与数据分析手段。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cda9fde5a24f4a5ab213abb020b270be.png)

**具体功能点包括：**

1. **用户登录管理：**
    - 提供完善的**登录与注册**功能，确保用户身份认证。
2. **数据统计与可视化：**
    - **核心功能**，涵盖**11种不同类型**的Echarts可视化图表，旨在全面呈现租房数据的各项统计信息。
    - 数据统计结果将以**动画形式**动态呈现，增强用户体验和数据可读性。
3. **多维度数据分析图表：**
    - 项目利用Echarts库的丰富图表类型，对租房数据进行**多角度、深层次的分析**。支持的图表类型包括：
        - **柱状图：** 展示数据的分布和对比。
        - **折线图：** 追踪数据的时间趋势。
        - **饼图：** 展现各类别数据的占比情况。
        - **花瓣图：** 提供独特的数据展示方式。
        - **环图：** 类似饼图，但更具视觉冲击力。
        - **仪表盘：** 直观显示关键指标的当前状态。
        - **漏斗图：** 分析数据在各阶段的转化率。
        - **词云：** 突出显示数据中的高频关键词。
4. **动态交互效果：**
    - 为提升用户体验，图表展示中融入了多种动态效果，例如：
        - **动态饼图：** 饼图的切片可随数据变化或交互进行动画展示。
        - **动态滚动的柱状图：** 柱状图可实现平滑滚动效果，方便浏览大量数据。

通过上述技术栈和功能实现，本项目致力于为用户提供一个直观、交互友好且分析深入的苏州租房数据可视化平台。
## 3 项目功能

系统是vue+flask架构，有2个前端，一个是数据大屏，另一个是数据可视化分析系统。
### 3.1 数据大屏
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1d2fb21d755440998a8024511c19d5ba.png)
### 3.2 登录
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c1f3afdb2a46495eb0c9dda577499056.png)
### 3.3 主页（数据统计）
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/becad4a1dbf44fbeb1936b25504af0d3.png)
### 3.4 可视化分析
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/747e962bdb384aa98a97988dfe02ca72.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4ee7e01d427b4bdb934a7f5be3615450.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4ce1681563b5414ea27ec0045356c642.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/01be455c640046f6b17013f40c3cea56.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fd52ab60099c4b6a84565f1c078b228b.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cbd23b5a2cee42f7a5598a361bdce3df.png)
### 3.5 词云分析
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6cfb51e3e492482cbf83a6073c901ea7.png)
## 4 程序代码

该租房数据可视化系统基于Vue.js 2.0框架开发，整合了Chart.js数据可视化库，提供直观的租房市场分析界面。系统动态展示不同区域租金波动、房源分布、户型比例及用户搜索趋势等关键指标。顶部筛选器支持城市、区域的互动查询，星级评分功能可收集用户价格满意度反馈。中部核心区域以四种图表呈现多维数据分布，底部统计卡片展示核心市场指标与同比变化。界面采用响应式设计，适配多种设备尺寸，为租房市场参与者提供决策支持与趋势洞察。

```python
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>城市租房市场数据分析平台</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4edf5 100%);
            color: #333;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            background: linear-gradient(90deg, #3498db, #2c3e50);
            color: white;
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, #e74c3c, #f39c12, #2ecc71, #3498db);
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        h1 i {
            margin: 0 15px;
            font-size: 2.5rem;
        }
        
        .subtitle {
            text-align: center;
            font-size: 1.2rem;
            margin-bottom: 20px;
            opacity: 0.9;
        }
        
        .toolbar {
            display: flex;
            justify-content: space-between;
            background: rgba(255, 255, 255, 0.15);
            padding: 15px;
            border-radius: 10px;
            margin-top: 20px;
        }
        
        .toolbar-item {
            flex: 1;
            margin: 0 10px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        select, .rating-box {
            width: 100%;
            padding: 12px;
            border-radius: 8px;
            border: none;
            background: rgba(255, 255, 255, 0.9);
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
            font-size: 16px;
            outline: none;
        }
        
        .dashboard {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .card {
            background: white;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
            padding: 25px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.15);
        }
        
        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #f0f4f8;
        }
        
        .card-title {
            font-size: 1.5rem;
            color: #2c3e50;
            font-weight: 600;
            display: flex;
            align-items: center;
        }
        
        .card-title i {
            margin-right: 12px;
            color: #3498db;
        }
        
        .chart-container {
            height: 320px;
            width: 100%;
            position: relative;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
            gap: 20px;
            margin-top: 25px;
        }
        
        .stat-card {
            background: linear-gradient(120deg, #f0f8ff, #fdfdfd);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
            border-left: 5px solid #3498db;
        }
        
        .stat-card:nth-child(2) {
            border-color: #2ecc71;
        }
        
        .stat-card:nth-child(3) {
            border-color: #e74c3c;
        }
        
        .stat-card:nth-child(4) {
            border-color: #f39c12;
        }
        
        .stat-value {
            font-size: 2.2rem;
            font-weight: 700;
            color: #2c3e50;
            margin: 10px 0;
        }
        
        .stat-label {
            color: #7f8c8d;
            font-weight: 500;
        }
        
        .footer {
            text-align: center;
            padding: 20px;
            color: #7f8c8d;
            font-size: 0.9rem;
            background: white;
            border-radius: 15px;
            box-shadow: 0 3px 15px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
        }
        
        .highlight {
            color: #e74c3c;
            font-weight: 600;
        }
        
        .trend-up {
            color: #2ecc71;
        }
        
        .trend-down {
            color: #e74c3c;
        }
        
        @media (max-width: 768px) {
            .dashboard {
                grid-template-columns: 1fr;
            }
            
            .toolbar {
                flex-direction: column;
            }
            
            .toolbar-item {
                margin: 10px 0;
            }
        }
        
        .rating-box {
            display: flex;
            justify-content: space-around;
            align-items: center;
            padding: 10px;
        }
        
        .rating-star {
            color: #ccc;
            cursor: pointer;
            font-size: 22px;
            transition: color 0.2s;
        }
        
        .rating-star:hover, .rating-star.active {
            color: #f39c12;
        }
    </style>
</head>
<body>
    <div id="app">
        <div class="container">
            <header>
                <h1>
                    <i class="fas fa-city"></i>
                    城市租房市场数据分析平台
                    <i class="fas fa-home"></i>
                </h1>
                <p class="subtitle">基于市场数据的实时可视化分析与租房趋势预测</p>
                
                <div class="toolbar">
                    <div class="toolbar-item">
                        <label for="city-select"><i class="fas fa-map-marker-alt"></i> 选择城市</label>
                        <select id="city-select" v-model="selectedCity">
                            <option v-for="city in cities" :value="city">{{ city }}</option>
                        </select>
                    </div>
                    
                    <div class="toolbar-item">
                        <label for="district-select"><i class="fas fa-location-dot"></i> 选择区域</label>
                        <select id="district-select" v-model="selectedDistrict">
                            <option v-for="district in districts" :value="district">{{ district }}</option>
                        </select>
                    </div>
                    
                    <div class="toolbar-item">
                        <label for="price-range"><i class="fas fa-tag"></i> 价格满意度评级</label>
                        <div class="rating-box">
                            <span v-for="n in 5" 
                                  :key="n" 
                                  class="rating-star"
                                  :class="{ 'active': n <= rating }"
                                  @click="rating = n"
                                  @mouseover="hoverRating(n)"
                                  @mouseleave="hoverRating(0)">
                                <i class="fas fa-star"></i>
                            </span>
                        </div>
                    </div>
                </div>
            </header>
            
            <div class="dashboard">
                <div class="card">
                    <div class="card-header">
                        <h2 class="card-title"><i class="fas fa-chart-line"></i> 区域平均租金 (元/月)</h2>
                    </div>
                    <div class="chart-container">
                        <canvas id="priceChart"></canvas>
                    </div>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <h2 class="card-title"><i class="fas fa-chart-pie"></i> 户型分布比例</h2>
                    </div>
                    <div class="chart-container">
                        <canvas id="typeChart"></canvas>
                    </div>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <h2 class="card-title"><i class="fas fa-chart-bar"></i> 区域房源数量对比</h2>
                    </div>
                    <div class="chart-container">
                        <canvas id="inventoryChart"></canvas>
                    </div>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <h2 class="card-title"><i class="fas fa-search"></i> 搜索热度趋势</h2>
                    </div>
                    <div class="chart-container">
                        <canvas id="trendChart"></canvas>
                    </div>
                </div>
            </div>
            
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-label">平均租金</div>
                    <div class="stat-value">¥{{ avgRentPrice }}</div>
                    <div><span class="trend-up">↑12%</span> 环比上月</div>
                </div>
                
                <div class="stat-card">
                    <div class="stat-label">在租房源</div>
                    <div class="stat-value">{{ totalListings }}</div>
                    <div><span class="trend-down">↓5%</span> 环比上月</div>
                </div>
                
                <div class="stat-card">
                    <div class="stat-label">满意度平均</div>
                    <div class="stat-value">{{ avgRating.toFixed(1) }}<span style="font-size: 1rem">/5</span></div>
                    <div><span class="trend-up">↑0.3</span> 环比上月</div>
                </div>
                
                <div class="stat-card">
                    <div class="stat-label">平均成交周期</div>
                    <div class="stat-value">{{ avgDays }}天</div>
                    <div><span class="trend-down">↓8%</span> 环比上月</div>
                </div>
            </div>
            
            <div class="footer">
                <p>数据更新时间: {{ currentDate }} | 数据来源: 城市房地产数据中心</p>
                <p>统计涵盖全市 <span class="highlight">{{ totalCoverageCount }}</span> 个小区/<span class="highlight">{{ totalListings }}</span> 套在租房源</p>
            </div>
        </div>
    </div>

    <script>
        new Vue({
            el: '#app',
            data: {
                selectedCity: '上海',
                selectedDistrict: '浦东新区',
                cities: ['上海', '北京', '广州', '深圳', '杭州', '成都'],
                districts: ['浦东新区', '黄浦区', '徐汇区', '长宁区', '静安区', '普陀区', '虹口区', '杨浦区'],
                rating: 4, // 默认评分
                charts: {},
                avgRentPrice: 6580,
                totalListings: 53462,
                avgRating: 4.2,
                avgDays: 21.5,
                totalCoverageCount: 1834
            },
            computed: {
                currentDate() {
                    return new Date().toLocaleDateString('zh-CN', {
                        year: 'numeric',
                        month: 'long',
                        day: 'numeric'
                    });
                }
            },
            mounted() {
                this.initCharts();
            },
            methods: {
                initCharts() {
                    // 创建图表实例
                    const priceCtx = document.getElementById('priceChart').getContext('2d');
                    const typeCtx = document.getElementById('typeChart').getContext('2d');
                    const inventoryCtx = document.getElementById('inventoryChart').getContext('2d');
                    const trendCtx = document.getElementById('trendChart').getContext('2d');
                    
                    // 租金趋势图表
                    this.charts.priceChart = new Chart(priceCtx, {
                        type: 'line',
                        data: {
                            labels: ['1月', '2月', '3月', '4月', '5月', '6月', '7月'],
                            datasets: [{
                                label: '平均租金（元/月）',
                                data: [6200, 6300, 6400, 6500, 6580, 6690, 6800],
                                backgroundColor: 'rgba(52, 152, 219, 0.1)',
                                borderColor: '#3498db',
                                borderWidth: 3,
                                pointBackgroundColor: '#fff',
                                pointBorderWidth: 2,
                                pointRadius: 5,
                                tension: 0.3,
                                fill: true
                            }]
                        },
                        options: {
                            responsive: true,
                            maintainAspectRatio: false,
                            scales: {
                                y: {
                                    beginAtZero: false,
                                    ticks: {
                                        callback: function(value) {
                                            return '¥' + value.toLocaleString();
                                        }
                                    }
                                }
                            }
                        }
                    });
                    
                    // 户型分布图表
                    this.charts.typeChart = new Chart(typeCtx, {
                        type: 'doughnut',
                        data: {
                            labels: ['一居室', '二居室', '三居室', '四居室及以上', '整租'],
                            datasets: [{
                                data: [25, 38, 20, 10, 7],
                                backgroundColor: [
                                    '#3498db',
                                    '#2ecc71',
                                    '#f39c12',
                                    '#e74c3c',
                                    '#9b59b6'
                                ],
                                borderWidth: 0
                            }]
                        },
                        options: {
                            responsive: true,
                            maintainAspectRatio: false,
                            plugins: {
                                legend: {
                                    position: 'right',
                                }
                            }
                        }
                    });
                    
                    // 房源数量对比
                    this.charts.inventoryChart = new Chart(inventoryCtx, {
                        type: 'bar',
                        data: {
                            labels: ['浦东新区', '闵行区', '徐汇区', '静安区', '黄浦区', '长宁区', '虹口区'],
                            datasets: [{
                                label: '在租房源数量',
                                data: [7850, 6250, 4820, 4310, 3520, 2980, 2650],
                                backgroundColor: '#2ecc71',
                                borderRadius: 8
                            }]
                        },
                        options: {
                            responsive: true,
                            maintainAspectRatio: false,
                            indexAxis: 'y',
                            scales: {
                                x: {
                                    beginAtZero: true
                                }
                            }
                        }
                    });
                    
                    // 搜索热度趋势图
                    this.charts.trendChart = new Chart(trendCtx, {
                        type: 'line',
                        data: {
                            labels: ['周一', '周二', '周三', '周四', '周五', '周六', '周日'],
                            datasets: [{
                                label: '用户搜索热度指数',
                                data: [1250, 1320, 1180, 1450, 1680, 1920, 1580],
                                backgroundColor: 'rgba(231, 76, 60, 0.1)',
                                borderColor: '#e74c3c',
                                borderWidth: 3,
                                pointBackgroundColor: '#fff',
                                pointBorderWidth: 2,
                                pointRadius: 5,
                                tension: 0.3,
                                fill: true
                            }]
                        },
                        options: {
                            responsive: true,
                            maintainAspectRatio: false,
                        }
                    });
                },
                hoverRating(n) {
                    // 这里可以添加鼠标悬停时的效果处理
                }
            }
        });
    </script>
</body>
</html>
```

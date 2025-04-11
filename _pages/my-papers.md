---
layout: subpage
permalink: /my-papers/
title: "我的论文集"
---

<style>
  /* 基本样式 */
  .papers-container {
    padding: 20px 0;
  }
  
  /* 布局容器 */
  .two-column-layout {
    display: flex;
    gap: 30px;
    margin-top: 20px;
  }
  
  /* 左侧导航区域 */
  .sidebar {
    width: 250px;
    flex-shrink: 0;
  }
  
  /* 右侧内容区域 */
  .main-content {
    flex: 1;
  }
  
  /* 导航和目录样式 */
  .papers-nav {
    background-color: #f5f5f5;
    padding: 15px;
    border-radius: 8px;
    position: sticky;
    top: 20px;
  }
  
  .papers-nav ul {
    list-style-type: none;
    padding-left: 0;
  }
  
  .papers-nav li {
    margin-bottom: 8px;
  }
  
  .papers-nav a {
    text-decoration: none;
    color: #333;
    transition: color 0.3s;
  }
  
  .papers-nav a:hover {
    color: #0074D9;
  }
  
  /* 响应式布局 */
  @media (max-width: 992px) {
    .two-column-layout {
      flex-direction: column;
    }
    
    .sidebar {
      width: 100%;
      margin-bottom: 20px;
    }
    
    .papers-nav {
      position: relative;
      top: 0;
    }
  }
  
  /* 论文卡片样式 */
  .paper-card {
    background-color: white;
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 20px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    transition: transform 0.3s, box-shadow 0.3s;
  }
  
  .paper-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  }
  
  .paper-title {
    font-size: 1.2em;
    font-weight: bold;
    margin-bottom: 10px;
  }
  
  .paper-authors {
    font-style: italic;
    margin-bottom: 10px;
  }
  
  .paper-journal {
    font-weight: bold;
    color: #0074D9;
    margin-bottom: 10px;
  }
  
  .paper-abstract {
    margin-bottom: 15px;
  }
  
  .paper-links {
    display: flex;
    gap: 10px;
  }
  
  .paper-links a {
    display: inline-block;
    padding: 5px 10px;
    background-color: #f0f0f0;
    border-radius: 4px;
    text-decoration: none;
    color: #333;
    transition: background-color 0.3s;
  }
  
  .paper-links a:hover {
    background-color: #e0e0e0;
  }
  
  /* 过滤和搜索栏 */
  .filter-container {
    margin-bottom: 20px;
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }
  
  .search-box {
    padding: 8px 15px;
    border: 1px solid #ddd;
    border-radius: 4px;
    flex-grow: 1;
  }
  
  .filter-button {
    padding: 8px 15px;
    background-color: #f0f0f0;
    border: 1px solid #ddd;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .filter-button:hover, .filter-button.active {
    background-color: #0074D9;
    color: white;
  }
  
  /* 响应式布局 */
  @media (max-width: 768px) {
    .filter-container {
      flex-direction: column;
    }
  }

  /* 显示摘要切换按钮 */
  .toggle-abstract {
    background: none;
    border: none;
    color: #0074D9;
    cursor: pointer;
    padding: 5px 0;
    font-size: 0.9em;
    display: block;
    margin-top: 10px;
  }
</style>

<div class="papers-container">
  <h1>我的论文集</h1>
  
  <!-- 两列布局开始 -->
  <div class="two-column-layout">
    
    <!-- 左侧导航栏 -->
    <div class="sidebar">
      <div class="papers-nav">
        <h3>目录</h3>
        <ul>
          <li><a href="#published-papers">已发表论文</a></li>
          <li><a href="#preprints">预印本和在投论文</a></li>
          <li><a href="#patents">专利与软件著作权</a></li>
        </ul>
      </div>
    </div>
    
    <!-- 右侧内容区域 -->
    <div class="main-content">
      
      <!-- 过滤和搜索栏 -->
      <div class="filter-container">
        <input type="text" class="search-box" id="paperSearch" placeholder="搜索论文标题或关键词...">
        <button class="filter-button active" data-category="all">全部</button>
        <button class="filter-button" data-category="published">已发表</button>
        <button class="filter-button" data-category="preprint">预印本</button>
        <button class="filter-button" data-category="har">人体活动识别</button>
        <button class="filter-button" data-category="medical">医学影像</button>
        <button class="filter-button" data-category="neuroscience">神经科学</button>
      </div>
  
  <!-- 已发表论文 -->
  <section id="published-papers">
    <h2>已发表论文</h2>
    
    <div class="paper-card" data-categories="published medical">
      <div class="paper-title">Joint Modelling Histology and Molecular Markers for Cancer Classification</div>
      <div class="paper-authors">Wang, X., <strong>Liu, H.</strong>, Zhang, Y., Zhao, B., Duan, H., Hu, W., ... & Li, C.</div>
      <div class="paper-journal">Medical Image Analysis, 102(4): 103505 (2025)</div>
      <div class="paper-abstract" style="display: none;">
        这篇论文探讨了如何将组织学和分子标记物联合建模用于癌症分类。我们提出了一种新的方法，通过整合两种不同类型的生物医学数据来提高癌症分类的准确性。本研究的创新点在于...
      </div>
      <button class="toggle-abstract">显示摘要</button>
      <div class="paper-links">
        <a href="https://www.sciencedirect.com/science/article/pii/S1361841525000532" target="_blank">网页</a>
        <a href="https://arxiv.org/pdf/2502.07979" target="_blank">预览</a>
        <a href="/paper/MedIA.pdf" target="_blank">下载</a>
      </div>
    </div>
    
    <div class="paper-card" data-categories="published har">
      <div class="paper-title">Multi-scale context-aware networks based on fragment association for human activity recognition</div>
      <div class="paper-authors"><strong>Liu, H.</strong>, Wang, Z., Zhao, B., Shen, Q., Li, M., Que, N., ... & Xin, J.</div>
      <div class="paper-journal">Proceedings of the Thirty-Third International Joint Conference on Artificial Intelligence (2024)</div>
      <div class="paper-abstract" style="display: none;">
        本研究提出了一种基于片段关联的多尺度上下文感知网络，用于人体活动识别。通过捕捉不同时间尺度的动作特征，我们的方法显著提高了识别准确率。该网络能够自适应地处理不同持续时间的活动，解决了传统方法在处理复杂活动时的局限性。
      </div>
      <button class="toggle-abstract">显示摘要</button>
      <div class="paper-links">
        <a href="https://www.ijcai.org/proceedings/2024/351" target="_blank">网页</a>
        <a href="https://www.ijcai.org/proceedings/2024/0351.pdf" target="_blank">预览</a>
        <a href="/paper/IJCAI2024.pdf" target="_blank">下载</a>
      </div>
    </div>
    
    <div class="paper-card" data-categories="published har">
      <div class="paper-title">MAG-Res2Net: A novel deep learning network for human activity recognition</div>
      <div class="paper-authors"><strong>Liu, H.</strong>, Zhao, B., Dai, C., Sun, B., Li, A., & Wang, Z.</div>
      <div class="paper-journal">Physiological Measurement, 44(11), 115007 (2023)</div>
      <div class="paper-abstract" style="display: none;">
        本文提出了MAG-Res2Net，这是一种用于人体活动识别的新型深度学习网络。该网络结合了多尺度注意力机制和改进的残差连接，能够有效提取可穿戴传感器数据中的时间依赖特征。实验表明，我们的方法在多个公开数据集上达到了最先进的性能。
      </div>
      <button class="toggle-abstract">显示摘要</button>
      <div class="paper-links">
        <a href="https://iopscience.iop.org/article/10.1088/1361-6579/ad0ab8/meta" target="_blank">网页</a>
        <a href="https://iopscience.iop.org/article/10.1088/1361-6579/ad0ab8/pdf" target="_blank">预览</a>
        <a href="/paper/PMEA2023.pdf" target="_blank">下载</a>
      </div>
    </div>
  </section>
  
  <!-- 预印本和在投论文 -->
  <section id="preprints">
    <h2>预印本和在投论文</h2>
    
    <div class="paper-card" data-categories="preprint neuroscience">
      <div class="paper-title">FOD-Diff: 3D Multi-Channel Patch Diffusion Model for Fiber Orientation Distribution</div>
      <div class="paper-authors">Tang H, <strong>Liu, H.</strong>, Li C.</div>
      <div class="paper-journal">MICCAI2025 (在投)</div>
      <div class="paper-abstract" style="display: none;">
        本文提出了FOD-Diff，这是一种用于纤维方向分布的3D多通道补丁扩散模型。该模型能够更准确地模拟大脑白质纤维束的方向分布，为神经连接组学研究提供了新的工具。
      </div>
      <button class="toggle-abstract">显示摘要</button>
      <div class="paper-links">
        <a href="#" target="_blank">即将发布</a>
      </div>
    </div>
    
    <div class="paper-card" data-categories="preprint har">
      <div class="paper-title">Redundant feature screening method for human activity recognition based on attention purification mechanism</div>
      <div class="paper-authors"><strong>Liu, H.</strong>, Li, X., Jiang, Y., Tang, H., Wu, D., & Guo, Y.</div>
      <div class="paper-journal">arXiv preprint (2025)</div>
      <div class="paper-abstract" style="display: none;">
        本研究提出了一种基于注意力纯化机制的人体活动识别冗余特征筛选方法。通过自适应地识别和过滤无关特征，我们的方法显著提高了活动识别的效率和准确性。实验结果表明，该方法在计算资源有限的场景中尤其有效。
      </div>
      <button class="toggle-abstract">显示摘要</button>
      <div class="paper-links">
        <a href="https://arxiv.org/abs/2503.23537" target="_blank">网页</a>
        <a href="https://arxiv.org/pdf/2503.23537" target="_blank">预览</a>
        <a href="/paper/submit1.pdf" target="_blank">下载</a>
      </div>
    </div>
    
    <div class="paper-card" data-categories="preprint har">
      <div class="paper-title">CMD-HAR: Cross-Modal Disentanglement for Wearable Human Activity Recognition</div>
      <div class="paper-authors"><strong>Liu, H.</strong>, Li, S., Yu, Y., Jiang, Y., Xiao, H., Long, J., & Tang, H.</div>
      <div class="paper-journal">arXiv preprint (2025)</div>
      <div class="paper-abstract" style="display: none;">
        本文提出了CMD-HAR，这是一种用于可穿戴人体活动识别的跨模态解耦方法。该方法能够有效分离不同传感器模态中的共享和唯一信息，提高了模型在多传感器环境中的鲁棒性和泛化能力。
      </div>
      <button class="toggle-abstract">显示摘要</button>
      <div class="paper-links">
        <a href="https://arxiv.org/abs/2503.21843" target="_blank">网页</a>
        <a href="https://arxiv.org/pdf/2503.21843" target="_blank">预览</a>
        <a href="/paper/submit2.pdf" target="_blank">下载</a>
      </div>
    </div>
    
    <div class="paper-card" data-categories="preprint har">
      <div class="paper-title">Optimizing End-to-End Sensor-Based Human Activity Recognition Through Multi-Attention Interaction</div>
      <div class="paper-authors">Yu Y., Wang H., Wang J., Yan M., Han X., Wu D., Zhao X., <strong>Liu, H.</strong></div>
      <div class="paper-journal">SSRN (2024)</div>
      <div class="paper-abstract" style="display: none;">
        本研究通过多注意力交互机制优化了端到端的基于传感器的人体活动识别。该方法在不同传感器模态间建立了动态的注意力机制，显著提高了识别性能，特别是在处理复杂环境下的活动时。
      </div>
      <button class="toggle-abstract">显示摘要</button>
      <div class="paper-links">
        <a href="http://dx.doi.org/10.2139/ssrn.4777248" target="_blank">网页</a>
        <a href="/paper/submit3.pdf" target="_blank">下载</a>
      </div>
    </div>
  </section>
  
  <!-- 专利与软件著作权 -->
  <section id="patents">
    <h2>专利与软件著作权</h2>
    
    <div class="paper-card" data-categories="published har">
      <div class="paper-title">基于多尺度度量学习的人类活动识别综合优化方法</div>
      <div class="paper-authors"><strong>刘涵瑜</strong>, 赵伯阳, 王之琼</div>
      <div class="paper-journal">专利（已受理）</div>
      <div class="paper-abstract" style="display: none;">
        本专利提出了一种基于多尺度度量学习的人类活动识别综合优化方法，该方法能够有效处理不同频率特征，提高识别准确率。
      </div>
      <button class="toggle-abstract">显示摘要</button>
    </div>
    
    <div class="paper-card" data-categories="published har">
      <div class="paper-title">基于多尺度神经网络的动作识别系统V1.0</div>
      <div class="paper-authors">赵伯阳, <strong>刘涵瑜</strong>, 王之琼</div>
      <div class="paper-journal">软件著作权（已受理）</div>
      <div class="paper-abstract" style="display: none;">
        该软件系统实现了基于多尺度神经网络的动作识别功能，支持多种传感器数据输入，可实时识别用户的日常活动。
      </div>
      <button class="toggle-abstract">显示摘要</button>
    </div>
  </section>
    
    </div> <!-- 结束右侧内容区域 -->
  </div> <!-- 结束两列布局 -->
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  // 摘要显示/隐藏功能
  document.querySelectorAll('.toggle-abstract').forEach(button => {
    button.addEventListener('click', function() {
      const abstract = this.previousElementSibling;
      if (abstract.style.display === 'none') {
        abstract.style.display = 'block';
        this.textContent = '隐藏摘要';
      } else {
        abstract.style.display = 'none';
        this.textContent = '显示摘要';
      }
    });
  });
  
  // 目录平滑滚动功能
  document.querySelectorAll('.papers-nav a').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      e.preventDefault();
      
      const targetId = this.getAttribute('href').substring(1);
      const targetElement = document.getElementById(targetId);
      
      if (targetElement) {
        window.scrollTo({
          top: targetElement.offsetTop - 20,
          behavior: 'smooth'
        });
      }
    });
  });
  
  // 过滤功能
  const filterButtons = document.querySelectorAll('.filter-button');
  const paperCards = document.querySelectorAll('.paper-card');
  
  filterButtons.forEach(button => {
    button.addEventListener('click', function() {
      // 移除所有按钮的active类
      filterButtons.forEach(btn => btn.classList.remove('active'));
      // 为当前按钮添加active类
      this.classList.add('active');
      
      const category = this.getAttribute('data-category');
      
      paperCards.forEach(card => {
        if (category === 'all') {
          card.style.display = 'block';
        } else {
          const cardCategories = card.getAttribute('data-categories').split(' ');
          if (cardCategories.includes(category)) {
            card.style.display = 'block';
          } else {
            card.style.display = 'none';
          }
        }
      });
    });
  });
  
  // 搜索功能
  const searchBox = document.getElementById('paperSearch');
  searchBox.addEventListener('input', function() {
    const searchTerm = this.value.toLowerCase();
    
    paperCards.forEach(card => {
      const title = card.querySelector('.paper-title').textContent.toLowerCase();
      const abstract = card.querySelector('.paper-abstract').textContent.toLowerCase();
      
      if (title.includes(searchTerm) || abstract.includes(searchTerm)) {
        card.style.display = 'block';
      } else {
        card.style.display = 'none';
      }
    });
  });
});
</script>

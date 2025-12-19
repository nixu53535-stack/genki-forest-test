// 9种人格数据 - 根据您的文档调整
const results = {
    "开拓者": {
        flavor: "卡曼橘味气泡水",
        tags: ["活力满格", "敢闯敢爆", "先锋开拓"],
        slogan: "去挑战｜先一步爆裂｜元气出发",
        desc: "你是团队中的『破局先锋』，不惧规则束缚，善于在未知中炸出新路。行动力是你的超能力，你相信『先做再说』，用果敢的尝试带动团队向前。在快速变化的职场中，你是那股最先涌动、最具爆发力的元气能量。",
        scene: "适配场景：新项目启动、市场开拓、危机应变、创新试错",
        color: "#FF6B35",
        bottle: "assets/bottles/orange.png"
    },
    "调和者": {
        flavor: "荔枝味气泡水",
        tags: ["灵动悦人", "亲和包容", "自然融合"],
        slogan: "愉悦连接｜甜感调节｜元气在场",
        desc: "你是团队中的『氛围调节师』，善于在紧张或尴尬中注入轻松与甜感。你不强势，却能用亲和力让不同性格的人自然融合、愉快协作。你的存在让职场不仅是『做事的地方』，也是『相处愉快的地方』。",
        scene: "适配场景：团队融合、冲突调解、客户关系、活动主持",
        color: "#FF9BD2",
        bottle: "assets/bottles/lychee.png"
    },
    "从容派": {
        flavor: "夏黑葡萄味气泡水",
        tags: ["优雅从容", "稳定输出", "内心自洽"],
        slogan: "保持平衡｜稳定输出｜元气自洽",
        desc: "你是团队中的『定海神针』，无论外界如何波动，你总能保持自己的节奏与判断。不随波逐流，也不急于表态，你的存在本身就让团队多了一份安定感。在焦虑弥漫的职场中，你是一种温和而坚定的力量。",
        scene: "适配场景：项目管理、风险控制、决策支持、团队维稳",
        color: "#8B5FBF",
        bottle: "assets/bottles/purple.png"
    },
    "思想者": {
        flavor: "柠檬味苏打气泡水",
        tags: ["思维敏捷", "脑洞活跃", "灵感涌现"],
        slogan: "思维跃动｜灵感成真｜元气无限",
        desc: "你是团队中的『思维引擎』，善于在复杂信息中梳理脉络、捕捉灵感。你的思考如绵密气泡般不断涌现，总能提出让人眼前一亮的视角或方案。不急于行动，但一旦想透，便是最有方向感的执行者。",
        scene: "适配场景：策略规划、创意发想、数据分析、方案优化",
        color: "#FFD93D",
        bottle: "assets/bottles/lemon.png"
    },
    "串联者": {
        flavor: "海盐椰子味气泡水",
        tags: ["协作达人", "情绪共振", "自然连接"],
        slogan: "协作链接｜情绪共振｜元气相连",
        desc: "你是团队中的『人际黏合剂』，善于让不同的人、不同的想法和谐共振。你像跃动的气泡，轻盈穿梭在团队之间，促进沟通、化解隔阂。不追求个人锋芒，却能让整体协作更流畅、更有温度。",
        scene: "适配场景：团队协作、跨部门沟通、客户关系、文化建设",
        color: "#6BC5D2",
        bottle: "assets/bottles/blue.png"
    },
    "洞察者": {
        flavor: "青瓜味气泡水",
        tags: ["清醒通透", "理性分析", "冷静输出"],
        slogan: "清醒判断｜稳定输出｜元气洞察",
        desc: "你是团队中的『清流视角』，善于在情绪化或混乱的情境中保持冷静与清晰。你的思考如青瓜般通透，不带偏见，直指核心。不急于表态，但每句话都带着理性分量，让人信服。",
        scene: "适配场景：数据分析、风险评估、策略评估、争议调解",
        color: "#C1E1C1",
        bottle: "assets/bottles/lightgreen.png"
    },
    "造梦家": {
        flavor: "白桃味气泡水",
        tags: ["奇思妙想", "灵感成真", "梦幻创造"],
        slogan: "奇思无限｜灵感成真｜元气造梦",
        desc: "你是团队中的『想象引擎』，总能看见别人看不见的可能性。你的思维如奇幻气泡，包裹着一个个色彩斑斓的『小世界』，充满超现实的创意。不被现实束缚，你用想象力为团队打开新的视野与赛道。",
        scene: "适配场景：产品创新、内容创作、品牌营销、用户体验设计",
        color: "#FF9BD2",
        bottle: "assets/bottles/pink.png"
    },
    "破壁者": {
        flavor: "山楂味气泡水",
        tags: ["果敢破局", "敏锐觉察", "清醒冲击"],
        slogan: "敏锐觉察｜破局前行｜元气醒神",
        desc: "你是团队中的『清醒剂』，善于在惯性思维中看见破绽、提出挑战。你不满足于表面和谐，敢于追问本质、打破僵局。你的存在让团队保持清醒，避免陷入『温水煮青蛙』的舒适区。",
        scene: "适配场景：问题诊断、流程再造、变革推动、决策挑战",
        color: "#D32F2F",
        bottle: "assets/bottles/red.png"
    },
    "鼓舞者": {
        flavor: "草莓味气泡水",
        tags: ["热情鼓舞", "感染他人", "情绪带动"],
        slogan: "热情鼓舞｜感染他人｜元气甜漾",
        desc: "你是团队中的『情绪引擎』，善于用热情与甜漾的能量带动整体氛围。你的存在就像草莓气泡般明快动人，让人不自觉被感染、被激励。你相信『情绪也是生产力』，主动为团队注入正向能量。",
        scene: "适配场景：团队激励、活动策划、客户互动、品牌传播",
        color: "#FF4081",
        bottle: "assets/bottles/strawberry.png"
    }
};

// 9人格测试题库（12题）
const questions = [
    {
        id: 1,
        text: "面对一个全新的项目方向，你的第一反应是？",
        options: [
            { text: "立刻行动，边做边学，用实践开路", type: "开拓者" },
            { text: "先搜集资料，分析可行性，制定计划", type: "思想者" },
            { text: "主动联系相关同事，组建小组一起探讨", type: "串联者" },
            { text: "构思一些别人没想到的创新点", type: "造梦家" }
        ]
    },
    {
        id: 2,
        text: "团队会议上，大家的意见陷入僵局，你会？",
        options: [
            { text: "提出一个大胆的新方案，打破僵局", type: "开拓者" },
            { text: "冷静分析各方观点，寻找共识点", type: "洞察者" },
            { text: "主动调解气氛，让大家放松下来再讨论", type: "调和者" },
            { text: "默默观察，最后给出一个综合建议", type: "从容派" }
        ]
    },
    {
        id: 3,
        text: "工作中遇到情绪低落的时候，你通常会？",
        options: [
            { text: "运动、听音乐，快速调节状态", type: "鼓舞者" },
            { text: "写日记、思考，梳理情绪来源", type: "思想者" },
            { text: "找朋友或同事聊一聊", type: "串联者" },
            { text: "独自静一静，慢慢恢复", type: "从容派" }
        ]
    },
    {
        id: 4,
        text: "你更擅长哪种工作节奏？",
        options: [
            { text: "快节奏，多任务同时推进", type: "开拓者" },
            { text: "有节奏，按计划一步步完成", type: "思想者" },
            { text: "协作型，喜欢团队同步进行", type: "串联者" },
            { text: "灵感型，有状态时高效输出", type: "造梦家" }
        ]
    },
    {
        id: 5,
        text: "面对一个复杂问题，你更倾向于？",
        options: [
            { text: "快速试错，用行动验证", type: "开拓者" },
            { text: "逻辑分析，拆解结构", type: "洞察者" },
            { text: "集思广益，听取多方意见", type: "串联者" },
            { text: "跳出框架，寻找创新解法", type: "造梦家" }
        ]
    },
    {
        id: 6,
        text: "你希望自己在团队中扮演什么角色？",
        options: [
            { text: "推动者，带领大家向前冲", type: "开拓者" },
            { text: "思考者，提供方向与策略", type: "思想者" },
            { text: "连接者，促进沟通与协作", type: "串联者" },
            { text: "稳定者，保持团队平衡", type: "从容派" }
        ]
    },
    {
        id: 7,
        text: "你如何处理工作中的压力？",
        options: [
            { text: "转化为动力，更加投入工作", type: "鼓舞者" },
            { text: "理性分解，逐步解决", type: "洞察者" },
            { text: "找人倾诉，分担情绪", type: "调和者" },
            { text: "自我调节，保持内心平稳", type: "从容派" }
        ]
    },
    {
        id: 8,
        text: "你更喜欢的反馈方式是？",
        options: [
            { text: "直接、即时，对事不对人", type: "破壁者" },
            { text: "有建设性，带分析建议", type: "思想者" },
            { text: "温和鼓励，带情感支持", type: "鼓舞者" },
            { text: "书面或冷静沟通", type: "洞察者" }
        ]
    },
    {
        id: 9,
        text: "你如何看待职场中的规则？",
        options: [
            { text: "可以打破，创新更重要", type: "开拓者" },
            { text: "理解规则，再优化规则", type: "思想者" },
            { text: "在规则中灵活协作", type: "调和者" },
            { text: "尊重规则，保持稳定", type: "从容派" }
        ]
    },
    {
        id: 10,
        text: "面对团队中的不合理现象，你会？",
        options: [
            { text: "直接指出问题，推动改变", type: "破壁者" },
            { text: "分析原因，提出改进方案", type: "洞察者" },
            { text: "先安抚情绪，再慢慢沟通", type: "调和者" },
            { text: "观察后再决定是否介入", type: "从容派" }
        ]
    },
    {
        id: 11,
        text: "你更认同以下哪句话？",
        options: [
            { text: "先做再说，行动胜于一切", type: "开拓者" },
            { text: "想清楚再走，方向大于速度", type: "思想者" },
            { text: "一个人走得快，一群人走得远", type: "串联者" },
            { text: "内心稳定，才能走得更远", type: "从容派" }
        ]
    },
    {
        id: 12,
        text: "你希望别人如何形容你？",
        options: [
            { text: "有冲劲，敢闯敢拼", type: "开拓者" },
            { text: "有头脑，思维清晰", type: "思想者" },
            { text: "好相处，温暖可信", type: "鼓舞者" },
            { text: "有定力，从容不迫", type: "从容派" }
        ]
    }
];

// 状态管理
let currentQuestion = 0;
let answers = {};

// DOM元素
const startPage = document.getElementById('start-page');
const testPage = document.getElementById('test-page');
const resultPage = document.getElementById('result-page');
const startBtn = document.getElementById('start-btn');
const nextBtn = document.getElementById('next-btn');
const questionText = document.getElementById('question-text');
const optionsContainer = document.getElementById('options-container');
const progressFill = document.querySelector('.progress-fill');
const currentQ = document.getElementById('current-q');

// 初始化
function init() {
    startBtn.addEventListener('click', startTest);
    nextBtn.addEventListener('click', nextQuestion);
    document.getElementById('retry-btn').addEventListener('click', restartTest);
    document.getElementById('share-btn').addEventListener('click', showShareModal);
    document.querySelector('.close-modal').addEventListener('click', hideShareModal);
    document.getElementById('copy-btn').addEventListener('click', copyLink);
}

// 开始测试
function startTest() {
    startPage.classList.remove('active');
    testPage.classList.add('active');
    loadQuestion(0);
}

// 加载题目
function loadQuestion(index) {
    const q = questions[index];
    questionText.textContent = q.text;
    optionsContainer.innerHTML = '';
    
    q.options.forEach((option, i) => {
        const optionEl = document.createElement('div');
        optionEl.className = 'option';
        optionEl.textContent = option.text;
        optionEl.dataset.type = option.type;
        optionEl.addEventListener('click', () => selectOption(optionEl, option.type));
        optionsContainer.appendChild(optionEl);
    });
    
    currentQ.textContent = index + 1;
    progressFill.style.width = `${((index + 1) / questions.length) * 100}%`;
    nextBtn.disabled = true;
}

// 选择选项
function selectOption(optionEl, type) {
    // 移除其他选项的选中状态
    document.querySelectorAll('.option').forEach(opt => {
        opt.classList.remove('selected');
    });
    
    // 选中当前选项
    optionEl.classList.add('selected');
    answers[currentQuestion] = type;
    nextBtn.disabled = false;
}

// 下一题
function nextQuestion() {
    currentQuestion++;
    
    if (currentQuestion < questions.length) {
        loadQuestion(currentQuestion);
    } else {
        showResult();
    }
}

// 显示结果
function showResult() {
    testPage.classList.remove('active');
    resultPage.classList.add('active');
    
    const resultType = calculateResult();
    const result = results[resultType];
    
    if (!result) {
        console.error('未找到结果:', resultType);
        return;
    }
    
    // 更新结果页内容
    document.getElementById('result-title').textContent = resultType;
    document.getElementById('result-flavor').textContent = result.flavor;
    document.getElementById('result-bottle').src = result.bottle;
    document.getElementById('result-bottle').alt = result.flavor;
    
    // 标签
    const tagsHtml = result.tags.map(tag => `<span class="tag">${tag}</span>`).join('');
    document.getElementById('result-tags').innerHTML = tagsHtml;
    
    // 其他信息
    document.getElementById('result-slogan').textContent = result.slogan;
    document.getElementById('result-desc').textContent = result.desc;
    document.getElementById('result-scene').innerHTML = `<h4>${result.scene}</h4>`;
    
    // 更新分享卡片
    updateShareCard(resultType, result);
}

// 计算结果
function calculateResult() {
    // 统计各人格得分
    const scores = {};
    
    // 初始化分数
    Object.keys(results).forEach(personality => {
        scores[personality] = 0;
    });
    
    // 计算分数
    Object.values(answers).forEach(personality => {
        if (scores[personality] !== undefined) {
            scores[personality]++;
        }
    });
    
    // 找出最高分
    let maxScore = 0;
    let resultPersonality = "开拓者"; // 默认
    
    Object.entries(scores).forEach(([personality, score]) => {
        if (score > maxScore) {
            maxScore = score;
            resultPersonality = personality;
        }
    });
    
    // 处理平局
    const tiedPersonalities = Object.keys(scores).filter(p => scores[p] === maxScore);
    if (tiedPersonalities.length > 1) {
        // 如果有平局，根据最后几题决定
        if (answers[11] && tiedPersonalities.includes(answers[11])) {
            return answers[11];
        } else if (answers[10] && tiedPersonalities.includes(answers[10])) {
            return answers[10];
        } else {
            return tiedPersonalities[0];
        }
    }
    
    return resultPersonality;
}

// 更新分享卡片
function updateShareCard(personality, result) {
    const shareCard = document.getElementById('share-card');
    shareCard.innerHTML = `
        <div style="text-align:center; padding:20px; background:white; border-radius:20px; border:2px solid ${result.color}">
            <h3 style="color:${result.color}; margin-bottom:10px;">${personality}</h3>
            <p style="color:#666; margin:10px 0;">${result.flavor}</p>
            <p style="font-size:18px; font-weight:bold; color:#333;">${result.slogan}</p>
            <p style="margin-top:15px; color:#888;">元气森林 · 职场元气诊断书</p>
        </div>
    `;
}

// 分享功能
function showShareModal() {
    document.getElementById('share-modal').classList.add('active');
}

function hideShareModal() {
    document.getElementById('share-modal').classList.remove('active');
}

function copyLink() {
    const url = window.location.href;
    navigator.clipboard.writeText(url).then(() => {
        alert('链接已复制到剪贴板！');
    });
}

// 重新测试
function restartTest() {
    currentQuestion = 0;
    answers = {};
    resultPage.classList.remove('active');
    startPage.classList.add('active');
}

// 初始化
window.addEventListener('DOMContentLoaded', init);
<script setup>
import { computed, ref } from 'vue'

let list1 = ref([{
  name: "数分1",
  point: 6,
  checked: true
}, {
  name: "线代",
  point: 6,
  checked: true
}, {
  name: "数分2",
  point: 6,
  checked: true
}, {
  name: "大物1",
  point: 4,
  checked: true
}, {
  name: "大物2",
  point: 4,
  checked: true
}, {
  name: "概统",
  point: 3,
  checked: true
}, {
  name: "基物实验1",
  point: 1,
  checked: true
}, {
  name: "基物实验2",
  point: 1,
  checked: true
}])
let tot1 = computed(() => tot(list1))

let list2 = ref([{
  name: "电设",
  point: 2,
  checked: true
}, {
  name: "程设",
  point: 2, 
  checked: true
}, {
  name: "离散1",
  point: 2, 
  checked: true
}, {
  name: "数据结构",
  point: 3, 
  checked: true
}])
let tot2 = computed(() => tot(list2))

let list3 = ref([{
  name: "大英A1/B1",
  point: 4,
  checked: true
}, {
  name: "大英A2/B2",
  point: 4, 
  checked: true
}])
let tot3 = computed(() => tot(list3))

let TOT1 = computed(() => tot1.value + tot2.value + tot3.value)

let list4 = ref([{
  name: "思想道德修养与法律基础",
  point: 2,
  checked: true
}, {
  name: "中国近现代史纲要",
  point: 2, 
  checked: true
}, {
  name: "习近平中国特色社会主义思想概论",
  point: 2, 
  checked: true
}, {
  name: "毛泽东思想和中国特色社会主义理论体系概论",
  point: 3, 
  checked: true
}, {
  name: "马克思理论基本原理概论",
  point: 3, 
  checked: true
}])
let tot4 = computed(() => tot(list4))

let list5 = ref([{
  name: "军事理论",
  point: 2,
  checked: true
}])
let tot5 = computed(() => tot(list5))

let list6 = ref([{
  name: "体育1",
  point: 0.5,
  checked: true
}, {
  name: "体育2",
  point: 0.5, 
  checked: true
}, {
  name: "体育3",
  point: 0.5, 
  checked: true
}, {
  name: "体育4",
  point: 0.5, 
  checked: true
}, {
  name: "体育5",
  point: 0.5,
  checked: true
}, {
  name: "体育6",
  point: 0.5, 
  checked: true
}, {
  name: "体育7",
  point: 1, 
  checked: true
}])
let tot6 = computed(() => tot(list6))

let list7 = ref([{
  name: "一年级导论课",
  point: 1.5,
  checked: true
}, {
  name: "航概A",
  point: 2, 
  checked: true
}, {
  name: "经济管理",
  point: 2, 
  checked: true
}, {
  name: "法律科技与社会",
  point: 2, 
  checked: true
}, {
  need: "人文、经典、社科和科技文明类",
  point: 1,
  checked: false
}, {
  need: "其它校级核通",
  point: 2,
  checked: false
}])
let tot7 = computed(() => tot(list7))

let list8 = ref([{
  name: "博雅1",
  point: 0.5,
  checked: true
}, {
  name: "博雅2",
  point: 0.5, 
  checked: true
}, {
  name: "博雅3",
  point: 0.5, 
  checked: true
}, {
  name: "博雅4",
  point: 0.5, 
  checked: true
}, {
  name: "博雅5",
  point: 0.5,
  checked: true
}, {
  name: "博雅6",
  point: 0.5, 
  checked: true
}, {
  name: "博雅7",
  point: 0.5, 
  checked: true
}, {
  name: "博雅8",
  point: 0.5, 
  checked: false
}])
let tot8 = computed(() => tot(list8))

let TOT2 = computed(() => tot4.value + tot5.value + tot6.value + tot7.value + tot8.value)

let list9 = ref([{
  name: "数学建模",
  point: 2,
  checked: true
}])
let tot9 = computed(() => tot(list9))

let list10 = ref([{
  name: "计组",
  point: 5.5,
  checked: true
}, {
  name: "离散2",
  point: 3,
  checked: true
}, {
  name: "OO",
  point: 3,
  checked: true
}, {
  name: "OS",
  point: 4.5,
  checked: true
}, {
  name: "编译",
  point: 4.5,
  checked: true
}, {
  name: "数据库",
  point: 4,
  checked: true
}, {
  name: "算法",
  point: 2,
  checked: true
}, {
  name: "软工",
  point: 2,
  checked: true
}, {
  name: "计网",
  point: 2,
  checked: true
}, {
  name: "计网实验",
  point: 1,
  checked: true
}, {
  name: "生产实习？",
  point: 3,
  checked: true
}, {
  name: "毕业设计",
  point: 8,
  checked: false
}])
let tot10 = computed(() => tot(list10))

let list11 = ref([{
  name: "职业规划与选择讲座",
  point: 0.5,
  checked: true
}, {
  name: "学科技术前沿讲座",
  point: 1,
  checked: true
}, {
  name: "求职辅导系列讲座",
  point: 0.5,
  checked: true
}, {
  name: "实践与展示1",
  point: 1,
  checked: true
}, {
  name: "实践与展示2",
  point: 1,
  checked: true
}, {
  name: "计算机研究方法论",
  point: 2,
  checked: true
}, {
  need: "全英文课程",
  point: 2,
  checked: false
}, {
  need: "跨专业课程",
  point: 2,
  checked: false
}])
let tot11 = computed(() => tot(list11))

let customValue = ref([
  {
    num: 1,
    string: '一般专业课程'
  }
])
let onCreate = () => {
  return  {
          num: 1,
          string: '新的一般专业课程'
        }
}

let list12 = ref([{
    name: "Java程序设计", point:1.5, checked: false
}, {
    name: "Swift程序设计实践", point:1.5, checked: false
}, {
    name: "智能计算概论", point:2, checked: false
}, {
    name: "Unix系统", point:1.5, checked: false
}, {
    name: "社会计算", point:2, checked: false
}, {
    name: "计算引论", point:1, checked: false
}, {
    name: "离散数学（3）", point:3, checked: false
}, {
    name: "C++与C#程序设计", point:1.5, checked: false
}, {
    name: "Python程序设计（全英文）", point:2, checked: false
}, {
    name: "计算机视觉计算", point:2, checked: false
}, {
    name: "移动应用创新实践", point:3, checked: false
}, {
    name: "并行计算程序设计", point:2, checked: false
}, {
    name: "多媒体技术", point:2, checked: false
}, {
    name: "分布式系统原理", point:2, checked: false
}, {
    name: "高级语言程序设计方法学", point:2, checked: false
}, {
    name: "互联网软件新技术（XML和Web)", point:2, checked: false
}, {
    name: "MATLAB基础及其应用", point:2, checked: false
}, {
    name: "机器学习导论", point:2.5, checked: false
}, {
    name: "计算机工程中最优化的方法", point:2, checked: false
}, {
    name: "计算机控制", point:2, checked: false
}, {
    name: "计算机图形学", point:2, checked: false
}, {
    name: "具体数学", point:1.5, checked: false
}, {
    name: "领导力培养与提升", point:2, checked: false
}, {
    name: "区块链与数字经济", point:1, checked: false
}, {
    name: "Android平台开发技术", point:2, checked: false
}, {
    name: "嵌入式系统设计实训", point:2, checked: false
}, {
    name: "软件测试技术", point:2, checked: false
}, {
    name: "数据挖掘导论", point:2.5, checked: false
}, {
    name: "数学建模入门", point:1.5, checked: false
}, {
    name: "物联网引论", point:2, checked: false
}, {
    name: "无线网络系统", point:2, checked: false
}, {
    name: "信号与系统", point:2, checked: false
}, {
    name: "虚拟现实技术", point:2, checked: false
}, {
    name: "形式语言与自动机", point:2, checked: false
}, {
    name: "移动计算导论", point:2, checked: false
}, {
    name: "RUBY语言程序设计", point:1, checked: false
}, {
    name: "智能计算体系结构", point:2, checked: false
}, {
    name: "并行计算程序设计", point:2, checked: false
}, {
    name: "FPGA多核并行计算", point:2, checked: false
}, {
    name: "大数据分析", point:2, checked: false
}, {
    name: "机器学习工程基础", point:2, checked: false
}, {
    name: "电子商务", point:1, checked: false
}, {
    name: "高级算法设计与分析", point:2, checked: false
}, {
    name: "X86汇编程序设计", point:2, checked: false
}, {
    name: "计算机图形学", point:2, checked: false
}, {
    name: "计算机网络安全技术", point:2, checked: false
}, {
    name: "人工智能", point:2, checked: false
}, {
    name: "人工智能安全导论", point:2, checked: false
}, {
    name: "人工智能的计算与信息理论", point:3, checked: false
}, {
    name: "人机交互 ", point:2, checked: false
}, {
    name: "软件项目管理", point:1.5, checked: false
}, {
    name: "深度学习", point:2.5, checked: false
}, {
    name: "数据可视化分析技术", point:2, checked: false
}, {
    name: "图象处理与模式识别", point:2, checked: false
}, {
    name: "网络攻防技术", point:2, checked: false
}, {
    name: "物联网与大数据系统设计", point:2, checked: false
}, {
    name: "物联网引论", point:2, checked: false
}, {
    name: "信号处理与信息推断", point:2, checked: false
}, {
    name: "信息系统分析与设计", point:1.5, checked: false
}, ])

let tot12 = computed(() => {
  let t = 0
  for (let i = 0; i < customValue.value.length; i++) {
    t += customValue.value[i].num
  }
  return t + tot(list12)
})

let TOT3 = computed(() => tot9.value + tot10.value + tot11.value + tot12.value)

function tot(l) {
  let t = 0
  for (let i = 0; i < l.value.length; i++) {
    if (l.value[i].checked) {
      t += l.value[i].point
    }
  }
  return t
}

</script>

<template>
  <div style="padding-left: 12px; padding-right: 12px; padding-top: 20px;">
    <n-h1><strong>我能毕业不能？</strong></n-h1>


    <n-collapse>
    <n-collapse-item title="关于2020级毕业学分说明" name="1">
      <div>
        2020级至少获得150学分才可授予计算机科学与技术学士学位。包括：<br>
        基础课程48学分（数学与自然科学类31学分，工程基础类9学分，外语类8学分）<br>
        通识课程32.5学分（思政类12学分，军理类2学分，体育类4学分，核心通识类10.5学分，一般通识类0学分，博雅类4学分）<br>
        专业课程69.5学分（含数学建模课2学分，核心专业类42.5学分，一般专业类25学分）。
        <br><br>
        A）全英文课程是不限课程性质，全校任何专业开设的一门2学分的核心专业课，一般专业课及一般通识课且授课方式为全英文的（除语言、写作、听说、翻译和语法词语类课程）的课程；国外交换期间一门2学分全英文授课的（不含实践和实习课程）的课程也算全英文课程；
        <br><br>
        B）跨专业课程是指全校理工科学院（除经济管理学院外）开设的1门2学分（含以上）核心专业课和一般专业课程（所选课程要与计算机学院所开课程的名称有巨大区分度）；
        <br><br>
        C）核心通识课程必须是人文社会科学学院、马克思主义学院、人文与社会科学高等研究院、法学院和新媒体艺术与设计学院五个学院开设的一门2学分非技术类不含一年级导论类，经济管理课程的核心通识课。
      </div>
    </n-collapse-item>
    <n-collapse-item :title="`基础课程48学分 / ${TOT1} 已取得`" name="2">
      <div style="padding-left: 20px;">
        <div><strong>数学与自然科学类31学分，已取得{{ tot1 }}分</strong></div>
        <div><n-checkbox v-for="c in list1" v-model:checked="c.checked">{{ c.name }}, {{ c.point }}分</n-checkbox></div>
        <n-divider></n-divider>
        <div><strong>工程基础类9学分，已取得{{ tot2 }}分</strong></div>
        <div><n-checkbox v-for="c in list2" v-model:checked="c.checked">{{ c.name }}, {{ c.point }}分</n-checkbox></div>
        <n-divider></n-divider>
        <div><strong>外语类8学分，已取得{{ tot3 }}分</strong></div>
        <div><n-checkbox v-for="c in list3" v-model:checked="c.checked">{{ c.name }}, {{ c.point }}分</n-checkbox></div>
        <n-divider></n-divider>
        <strong>这一部分共取得{{ TOT1 }}分</strong>
      </div>
    </n-collapse-item>
    <n-collapse-item :title="`通识课程32.5学分 / ${TOT2} 已取得`" name="3">
      <div style="padding-left: 20px;">
        <div><strong>思政类12学分，已取得{{ tot4 }}分</strong></div>
        <div><n-checkbox v-for="c in list4" v-model:checked="c.checked">{{ c.name }}, {{ c.point }}分</n-checkbox></div>
        <n-divider></n-divider>
        <div><strong>军理类2学分，已取得{{ tot5 }}分</strong></div>
        <div><n-checkbox v-for="c in list5" v-model:checked="c.checked">{{ c.name }}, {{ c.point }}分</n-checkbox></div>
        <n-divider></n-divider>
        <div><strong>体育类4学分，已取得{{ tot6 }}分</strong></div>
        <div><n-checkbox v-for="c in list6" v-model:checked="c.checked">{{ c.name }}, {{ c.point }}分</n-checkbox></div>
        <n-divider></n-divider>
        <div><strong>核心通识类10.5学分，已取得{{ tot7 }}分</strong></div>
        核心通识类10.5学分包括：<br>
        <div><n-checkbox v-for="c in list7" v-model:checked="c.checked">
          <template v-if="c.name">{{ c.name }}, {{ c.point }}分</template>
          <template v-else><n-input size="tiny" :placeholder="`${c.point}分 ${c.need}`"></n-input>
          </template>
        </n-checkbox></div>

        <n-divider></n-divider>
        <div><strong>一般通识类0学分</strong></div>
        <n-divider></n-divider>
        <div><strong>博雅类4学分，已取得{{ tot8 }}分</strong></div>
        <div><n-checkbox v-for="c in list8" v-model:checked="c.checked">{{ c.name }}, {{ c.point }}分</n-checkbox></div>
        <n-divider></n-divider>
        
        <strong>这一部分共取得{{ TOT2 }}分</strong>
      </div>
    </n-collapse-item>
    <n-collapse-item :title="`专业课程69.5学分 / ${TOT3} 已取得`" name="4">
      <div style="padding-left: 20px;">
        <div><strong>数学建模类2学分，已取得{{ tot9 }}分</strong></div>
        <div><n-checkbox v-for="c in list9" v-model:checked="c.checked">{{ c.name }}, {{ c.point }}分</n-checkbox></div>
        <div><strong>核心专业类42.5学分，已取得{{ tot10 }}分</strong></div>
        <div><n-checkbox v-for="c in list10" v-model:checked="c.checked">
          <template v-if="c.name">{{ c.name }}, {{ c.point }}分</template>
          <template v-else><n-input size="tiny" :placeholder="`${c.point}分 ${c.need}`"></n-input>
          </template>
        </n-checkbox></div>
        <div><strong>一般专业类25学分，其中下列课程占10分，已取得{{ tot11 }}分</strong></div>
        <div><n-checkbox v-for="c in list11" v-model:checked="c.checked">
          <template v-if="c.name">{{ c.name }}, {{ c.point }}分</template>
          <template v-else><n-input size="tiny" :placeholder="`${c.point}分 ${c.need}`"></n-input>
          </template>
        </n-checkbox></div>
        <br>
        <div><strong>此外，还有15分一般专业课，已取得{{ tot12 }}分</strong></div>
        <div>先看看下面你上过哪些：</div>
        <div><n-checkbox v-for="c in list12" v-model:checked="c.checked">{{ c.name }}, {{ c.point }}分</n-checkbox></div>
        <br>
        <div>没找到的话：</div>
        <n-dynamic-input v-model:value="customValue" :on-create="onCreate">
        <template #default="{ value }">
          <div style="display: flex; align-items: center; width: 100%">
            <n-input-number
              v-model:value="value.num"
              style="margin-right: 12px; width: 160px"
              size="tiny"
            />
            <n-input size="tiny" v-model:value="value.string" type="text" />
          </div>

        </template>
      </n-dynamic-input>
      <br>
      <strong>这一部分共取得{{ TOT3 }}分</strong>
      </div>
    </n-collapse-item>
  </n-collapse>
    

  </div>

  <n-h1 style="padding-left: 12px"><strong>祝您毕设顺利！</strong></n-h1>
  <n-h5 style="padding-left: 12px">在此鸣谢qs哥哥的xmind图，yjk哥哥和pzy姐姐的表</n-h5>
</template>

<style scoped>
</style>

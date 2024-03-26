<template>
  <table>
    <thead>
      <td v-for="info in infos">{{ info }}</td>
    </thead>
    <tbody>
      <tr v-for="sector in industrySectors">{{ sector }}</tr>
    </tbody>
  </table>
</template>

<script>
export default {
  data(){
    return{
      /*
      没找到，一个网页就能爬所有板块的，因此先一个板块对应一个网页，这样爬取
      找到乌龟量化网站，可以简单爬取 https://wglh.com/indicestop/ - 指数分类
      腾讯证券 
      
      证券 x
      纳斯达克100 代码和同花顺不一样，数一样 http://wglh.com/chinaindicespe/ndx
      标普500  代码乌龟和同花顺不一样，数一样， http://wglh.com/chinaindicespe/sp500
      恒生科技指数 x
      恒生国企指数 hscei (乌龟和同花顺数一不样?) http://wglh
      传媒 https://q.10jqka.com.cn/thshy/detail/code/881164/
      中证传媒 (乌龟和同花顺数一样) 399971 http://wglh.com/chinaindicese/sz399971
      有色金属 代码和同花顺不一样，数一样 http://wglh.com/chinaindicespe/sh000819
      房地产 931775 (乌龟和同花顺数一样) http://wglh.com/chinaindicespe/csi931775
      房地产开发 x
      燃气 x
      国证钢铁 399440 (乌龟和同花顺数一样) http://wglh.com/chinaindicespe/sz399440
      中证1000 代码和同花顺不一样，数一样 http://wglh.com/chinaindicespe/sh000852
      中证军工 399967(乌龟和同花顺数一样) https://wglh.com/chinaindicespe/sz399967
      基建工程 (乌龟和同花顺数一样) 399995 https://wglh.com/chinaindicespe/sz399995
      通信服务 https://q.10jqka.com.cn/thshy/detail/code/881162/
      国证军工 399368 (乌龟和同花顺数一样) http://wglh.com/chinaindicespe/sz399368
      稀土 x
      中证医疗 (乌龟和同花顺数一样) 399989 http://wglh.com/chinaindicespe/sz399989
      上证指数 (代码乌龟和同花顺不一样。数一样) http://wglh.com/chinaindicespe/sh000001

      */
      // 行业板块
      industrySectors: ["标普500", "纳斯达克100"],
      // 行业信息
      infos: ["板块名称", "同花顺代码", "乌龟量化代码", "类型", "最高","最低", "35%", "30%", "当前", "最早年份", "今年", "参考时间", 
      "备注", "是否可下单35%", "是否可下单30%", "当前位置占比", "历史最低占比", "历史最低与当前位置相差5-10", "是否有周期", "历史最低位是否失效过"]
    }
  }
}
</script>
<template>
    <div>
        <h1>豆瓣电影排行榜</h1>
        <el-row style="text-align: left;font-size: 5px" >
            <el-col :span="16" :offset="4">
                <hr style="color:lightgray;border-style: dashed;width: 100%"/>
            </el-col>
        </el-row>
        <el-row  type="flex" justify="center" :gutter="20">
            <el-col :span="5">
                <img src="../assets/1.jpg" style="width: 150px;height:200px">
            </el-col>
            <el-col :span="8" style="text-align: left">
                <div class="a">
                    <h5>{{movie.alias}}</h5>
                    <p style="text-indent: 20px">{{movie.describe}}</p>
                    <div style="display: inline-block">
                        <el-rate disabled v-model="movie.scoring.star"></el-rate>
                        <div style="font-size:12px;color:#37a;padding-left: 3px">
                            <p style="margin: 3px">{{movie.scoring.score}}
                                ({{movie.scoring.amount}}人评价)</p>
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>
        <!--<el-row v-for="subList in movieList"type="flex" justify="center"
                style="margin-top: 20px">
            <el-col :span="4">
                <img v-bind:src="subList[0].imgUrl"/>
                <div>
                    <span class="title-span"v-on:click="detailPage(subList[0].title)">{{subList[0].title}}</span>
                    &nbsp;&nbsp;
                    <span class="describe-span">{{subList[0].describe}}</span>
                </div>
            </el-col>
        </el-row>
-->

        <el-row style="text-align: left;font-size: 5px" >
            <el-col :span="16" :offset="4">
                <hr style="color:lightgray;border-style: dashed;width: 100%"/>
            </el-col>
        </el-row>
        <el-row type="flex" justify="center" :gutter="20">
            <el-col :span="5">
                <img src="../assets/2.jpg" style="width: 150px;height:200px">
            </el-col>
            <el-col :span="8" style="text-align: left">
                <div class="a">
                    <h5>{{movie.alias1}}</h5>
                    <p style="text-indent: 20px">{{movie.describe1}}</p>
                    <div style="display: inline-block">
                        <el-rate disabled v-model="movie.scoring.star1"></el-rate>
                        <div style="font-size:12px;color:#37a;padding-left: 3px">
                            <p style="margin: 3px">{{movie.scoring.score1}}
                                ({{movie.scoring.amount1}}人评价)</p>
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>


        <el-row style="text-align: left;font-size: 5px" >
            <el-col :span="16" :offset="4">
                <hr style="color:lightgray;border-style: dashed;width: 100%"/>
            </el-col>
        </el-row>
        <el-row type="flex" justify="center" :gutter="20">
            <el-col :span="5">
                <img src="../assets/3.jpg" style="width: 150px;height:200px">
            </el-col>
            <el-col :span="8" style="text-align: left">
                <div class="a">
                    <h5>{{movie.alias2}}</h5>
                    <p style="text-indent: 20px">{{movie.describe2}}</p>
                    <div style="display: inline-block">
                        <el-rate disabled v-model="movie.scoring.star2"></el-rate>
                        <div style="font-size:12px;color:#37a;padding-left: 3px">
                            <p style="margin: 3px">{{movie.scoring.score2}}
                                ({{movie.scoring.amount2}}人评价)</p>
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>


        <el-row style="text-align: left;font-size: 5px" >
            <el-col :span="16" :offset="4">
                <hr style="color:lightgray;border-style: dashed;width: 100%"/>
            </el-col>
        </el-row>
        <el-row type="flex" justify="center" :gutter="20">
            <el-col :span="5">
                <img src="../assets/4.jpg" style="width: 150px;height:200px">
            </el-col>
            <el-col :span="8" style="text-align: left">
                <div class="a">
                    <h5>{{movie.alias3}}</h5>
                    <p style="text-indent: 20px">{{movie.describe3}}</p>
                    <div style="display: inline-block">
                        <el-rate disabled v-model="movie.scoring.star3"></el-rate>
                        <div style="font-size:12px;color:#37a;padding-left: 3px">
                            <p style="margin: 3px">{{movie.scoring.score3}}
                                ({{movie.scoring.amount3}}人评价)</p>
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>


        <el-row style="text-align: left;font-size: 5px" >
            <el-col :span="16" :offset="4">
                <hr style="color:lightgray;border-style: dashed;width: 100%"/>
            </el-col>
        </el-row>
        <el-row type="flex" justify="center" :gutter="20">
            <el-col :span="5">
                <img src="../assets/5.jpg" style="width: 150px;height:200px">
            </el-col>
            <el-col :span="8" style="text-align: left">
                <div class="a">
                    <h5>{{movie.alias4}}</h5>
                    <p style="text-indent: 20px">{{movie.describe4}}</p>
                    <div style="display: inline-block">
                        <el-rate disabled v-model="movie.scoring.star4"></el-rate>
                        <div style="font-size:12px;color:#37a;padding-left: 3px">
                            <p style="margin: 3px">{{movie.scoring.score4}}
                                ({{movie.scoring.amount4}}人评价)</p>
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>


        <el-row style="text-align: left;font-size: 5px" >
            <el-col :span="16" :offset="4">
                <hr style="color:lightgray;border-style: dashed;width: 100%"/>
            </el-col>
        </el-row>
        <el-row type="flex" justify="center" :gutter="20">
            <el-col :span="5">
                <img src="../assets/6.jpg" style="width: 150px;height:200px">
            </el-col>
            <el-col :span="8" style="text-align: left">
                <div class="a">
                    <h5>{{movie.alias5}}</h5>
                    <p style="text-indent: 20px">{{movie.describe5}}</p>
                    <div style="display: inline-block">
                        <el-rate disabled v-model="movie.scoring.star5"></el-rate>
                        <div style="font-size:12px;color:#37a;padding-left: 3px">
                            <p style="margin: 3px">{{movie.scoring.score5}}
                                ({{movie.scoring.amount5}}人评价)</p>
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>


        <el-row style="text-align: left;font-size: 5px" >
            <el-col :span="16" :offset="4">
                <hr style="color:lightgray;border-style: dashed;width: 100%"/>
            </el-col>
        </el-row>
        <el-row type="flex" justify="center" :gutter="20">
            <el-col :span="5">
                <img src="../assets/7.jpg" style="width: 150px;height:200px">
            </el-col>
            <el-col :span="8" style="text-align: left">
                <div class="a">
                    <h5>{{movie.alias6}}</h5>
                    <p style="text-indent: 20px">{{movie.describe6}}</p>
                    <div style="display: inline-block">
                        <el-rate disabled v-model="movie.scoring.star6"></el-rate>
                        <div style="font-size:12px;color:#37a;padding-left: 3px">
                            <p style="margin: 3px">{{movie.scoring.score6}}
                                ({{movie.scoring.amount6}}人评价)</p>
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>


        <el-row style="text-align: left;font-size: 5px" >
            <el-col :span="16" :offset="4">
                <hr style="color:lightgray;border-style: dashed;width: 100%"/>
            </el-col>
        </el-row>
        <el-row type="flex" justify="center" :gutter="20">
            <el-col :span="5">
                <img src="../assets/8.jpg" style="width: 150px;height:200px">
            </el-col>
            <el-col :span="8" style="text-align: left">
                <div class="a">
                    <h5>{{movie.alias7}}</h5>
                    <p style="text-indent: 20px">{{movie.describe7}}</p>
                    <div style="display: inline-block">
                        <el-rate disabled v-model="movie.scoring.star7"></el-rate>
                        <div style="font-size:12px;color:#37a;padding-left: 3px">
                            <p style="margin: 3px">{{movie.scoring.score7}}
                                ({{movie.scoring.amount7}}人评价)</p>
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>


        <el-row style="text-align: left;font-size: 5px" >
            <el-col :span="16" :offset="4">
                <hr style="color:lightgray;border-style: dashed;width: 100%"/>
            </el-col>
        </el-row>
        <el-row type="flex" justify="center" :gutter="20">
            <el-col :span="5">
                <img src="../assets/9.jpg" style="width: 150px;height:200px">
            </el-col>
            <el-col :span="8" style="text-align: left">
                <div class="a">
                    <h5>{{movie.alias8}}</h5>
                    <p style="text-indent: 20px">{{movie.describe8}}</p>
                    <div style="display: inline-block">
                        <el-rate disabled v-model="movie.scoring.star8"></el-rate>
                        <div style="font-size:12px;color:#37a;padding-left: 3px">
                            <p style="margin: 3px">{{movie.scoring.score8}}
                                ({{movie.scoring.amount8}}人评价)</p>
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>


        <el-row style="text-align: left;font-size: 5px" >
            <el-col :span="16" :offset="4">
                <hr style="color:lightgray;border-style: dashed;width: 100%"/>
            </el-col>
        </el-row>
        <el-row type="flex" justify="center" :gutter="20">
            <el-col :span="5">
                <img src="../assets/10.jpg" style="width: 150px;height:200px">
            </el-col>
            <el-col :span="8" style="text-align: left">
                <div class="a">
                    <h5>{{movie.alias9}}</h5>
                    <p style="text-indent: 20px">{{movie.describe9}}</p>
                    <div style="display: inline-block">
                        <el-rate disabled v-model="movie.scoring.star9"></el-rate>
                        <div style="font-size:12px;color:#37a;padding-left: 3px">
                            <p style="margin: 3px">{{movie.scoring.score9}}
                                ({{movie.scoring.amount9}}人评价)</p>
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>
    </div>
</template>
<script>
   /* export default{
        data: function () {
            return {
                movieList: [
                    [
                        {title:'小丑 / 小丑起源电影：罗密欧 / Romeo ',score:8.8, amount: 474206,star: 4.5,
                            describe:"2019-08-31(威尼斯电影节) / 2019-10-04(美国) / 杰昆·菲尼克斯 / 罗伯特·德尼罗 / 马克·马龙 / 莎姬·贝兹 /谢伊·惠格姆 / 弗兰西丝·康罗伊 / 布莱恩·考伦 / 布莱恩·泰里·亨利 / 布莱特·卡伦 / 道格拉斯·霍奇斯 / 格伦·弗莱施勒 / 比尔·坎普...",
                            imgUrl:require('../assets/1.jpg')},
                        {title:'好莱坞往事 / 从前，有个荷里活(港) / 从前，有个好莱坞...(台) ',score:7.4,amount: 74166, star: 3.5,
                            describe:"2019-05-21(戛纳电影节) / 2019-07-26(美国) / 2019(中国大陆) / 莱昂纳多·迪卡普里奥 / 布拉德·皮特 / 玛格特·罗比 / 埃米尔·赫斯基 / 玛格丽特·库里 / 蒂莫西·奥利芬特 / 茱莉亚·巴特斯 / 奥斯汀·巴特勒 / 达科塔·范宁 / 布鲁斯·邓恩 /...",
                            imgUrl:require('../assets/2.jpg')},
                        {title:'爱尔兰人 / 爱尔兰杀手(港) / 听说你刷房子了',score: 9.1,amount2: 47209,star: 4.5,
                            describe:"2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 /乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 /阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                         imgUrl:require('../assets/3.jpg')},
                        {title:'我在你床下',score:6.7,  amount: 26531, star: 3.5,
                            describe:"2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 /乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 /阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                            imgUrl:require('../assets/5.jpg')},
                        {title:'酷刑报告',score:7.0,amount: 47209, star: 4.5,
                            describe:"2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 /乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 /阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                            imgUrl:require('../assets/6.jpg')}
                    ],
                    [
                        {title:'爱尔兰人',score:9.1,amount: 14902, star: 4.0,
                            describe:"2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 /乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 /阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                            imgUrl:require('../assets/6.jpg')},
                        {title:'攀登者',score:6.2,amount: 193463, star: 3.0,
                            describe:"2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 /乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 /阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                            imgUrl:require('../assets/7.jpg')},
                        {title:'准备好了没',score:6.8,amount: 26531,star: 3.5,
                            describe:"2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 /乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 /阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                            imgUrl:require('../assets/8.jpg')},
                        {title:'双子杀手',score:7.1,amount: 174335, star: 3.5,
                            describe:"2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 /乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 /阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                            imgUrl:require('../assets/9.jpg')},
                        {title:'地久天长',score:8.0, amount: 180267, star: 4.0,
                            describe:"2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 /乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 /阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                            imgUrl:require('../assets/10.jpg')}
                    ]

                ]
            }
        },
        methods:{
            /!**
             * 出发页面跳转，跳转到电影的详情页
             * @param title
             *!/
            detailPage:function(title){
                //获取router对象,调用router对象的push方法
                this.$router.push({ name:"movie",params:{title:title}});
            }
        }
    }*/
    import ElProgress from "../../node_modules/element-ui/packages/progress/src/progress";
    export default {
        components: {ElProgress},
        /**
         * 当detail.vue被加载时，首先执行created函数，实际上指的是页面未加载完成前，先执行的函数
         * 生命周期钩子函数
         */
        created: function () {
            //先给movie对象附上title的值
            //console.log(this.$route)
            //alert(this.$route.params.title)
            this.movie.title = this.$route.params.title;
        },
        data () {
            return {
                movie: {
                    alias:"小丑 / 小丑起源电影：罗密欧 / Romeo ",
                    describe:"2019-08-31(威尼斯电影节) / 2019-10-04(美国) / 杰昆·菲尼克斯 / 罗伯特·德尼罗 / 马克·马龙 / 莎姬·贝兹 /谢伊·惠格姆 / 弗兰西丝·康罗伊 / 布莱恩·考伦 / 布莱恩·泰里·亨利 / 布莱特·卡伦 / 道格拉斯·霍奇斯 / 格伦·弗莱施勒 / 比尔·坎普...",
                    alias1:"好莱坞往事 / 从前，有个荷里活(港) / 从前，有个好莱坞...(台) ",
                    describe1:"2019-05-21(戛纳电影节) / 2019-07-26(美国) / 2019(中国大陆) / 莱昂纳多·迪卡普里奥 / 布拉德·皮特 / 玛格特·罗比 / 埃米尔·赫斯基 / 玛格丽特·库里 / 蒂莫西·奥利芬特 / 茱莉亚·巴特斯 / 奥斯汀·巴特勒 / 达科塔·范宁 / 布鲁斯·邓恩 /...",
                    alias2:"爱尔兰人 / 爱尔兰杀手(港) / 听说你刷房子了",
                    describe2:"2019-09-27(纽约电影节) / 2019-11-01(美国点映) / 2019-11-27(美国网络) / 罗伯特·德尼罗 / 阿尔·帕西诺 /乔·佩西 / 安娜·帕奎因 / 杰西·普莱蒙 / 哈威·凯特尔 / 斯蒂芬·格拉汉姆 / 鲍比·坎纳瓦尔 / 杰克·休斯顿 /阿莱卡萨·帕拉迪诺 / 凯瑟琳·纳杜奇...",
                    alias3:"婚姻故事",
                    describe3:"2019-08-29(威尼斯电影节) / 2019-12-06(美国) / 斯嘉丽·约翰逊 / 亚当·德赖弗 / 梅里特·韦弗 / 劳拉·邓恩 / 雷·利奥塔 / 朱丽·哈基提 / 马克·奥布莱恩 / 华莱士·肖恩 / 阿伦·阿尔达 / 凯尔·柏海莫 / 米奇·萨姆纳 /艾奇·罗伯逊 / 马修·马希尔...",
                    alias4:"准备好了没 / 弑婚游戏(台) / 爆血新婚夜(港)",
                    describe4:"2019-08-21(美国) / 萨玛拉·维文 / 安迪·麦克道威尔 / 马克·奥布莱恩 / 亚当·布罗迪 /亨利·科泽尼 / 妮基·瓜达尼 / 梅兰妮·斯科洛凡诺 / 克里斯蒂安·布鲁恩 / 伊利斯 莱韦斯克 / 约翰·拉尔斯顿 / 达妮埃拉·巴博萨 / 伊拉娜·盖尔 /...",
                    alias5:"第一滴血5：最后的血 / 第一滴血：终极血战(港) / 蓝波：最后一滴血(台)",
                    describe5:"2019-09-18(印度尼西亚) / 2019-09-20(美国) / 2019-09-27(西班牙) / 西尔维斯特·史泰龙 / 帕斯·贝加 /塞尔吉奥·佩里斯-门切塔 / 艾德里安娜·巴拉扎 / 维特·蒙雷尔 / 吉妮·金 / 华金·科西奥 / 帕斯卡西奥·洛佩斯 /奥斯卡·贾恩那达 / 亚历山大·迪米特罗夫...",
                    alias6:"攀登者‎ (2019)",
                    describe6:"中国大陆 / 剧情 / 爱情 / 冒险 / The Climbers / 125分钟李仁港 / 吴京 / 章子怡 / 井柏然 / 张译 / 胡歌 / 成龙 / 陈龙 / 多布杰",
                    alias7:"准备好了没 / 弑婚游戏(台) / 爆血新婚夜(港)",
                    describe7:"019-08-21(美国) / 萨玛拉·维文 / 安迪·麦克道威尔 / 马克·奥布莱恩 / 亚当·布罗迪 /亨利·科泽尼 / 妮基·瓜达尼 / 梅兰妮·斯科洛凡诺 / 克里斯蒂安·布鲁恩 / 伊利斯 莱韦斯克 /约翰·拉尔斯顿 / 达妮埃拉·巴博萨 / 伊拉娜·盖尔 /...",
                    alias8:"双子杀手 Gemini Man‎ (2019)",
                    describe8:"美国 / 中国大陆 / 剧情 / 动作 / 科幻 / 双子任务：叠影危机(港) / 双子煞星 / 117分钟李安 / 威尔·史密斯 / 玛丽·伊丽莎白·温斯特德 / 克里夫·欧文 / 本尼迪克特·王 /道格拉斯·霍奇斯 / 拉尔夫·布朗 / 琳达·...",
                    alias9:"地久天长‎ (2019)",
                    describe9:"中国大陆 / 剧情 / 家庭 / So Long, My Son / 175分钟王小帅 / 王景春 / 咏梅 / 齐溪 / 王源 / 杜江 / 艾丽娅 / 徐程 / 李菁菁...",

                    scoring: {
                        score: 8.8,
                        amount: 474206,
                        star: 4.5,

                        score1: 7.3,
                        amount1: 74166,
                        star1: 3.5,

                        score2: 9.1,
                        amount2: 47209,
                        star2: 4.5,

                        score3: 8.8,
                        amount3: 19915,
                        star3: 4.5,

                        score4: 6.7,
                        amount4: 26531,
                        star4: 3.5,

                        score5: 7.5,
                        amount5: 14902,
                        star5: 4.0,

                        score6: 6.2,
                        amount6: 193463,
                        star6: 3.0,

                        score7: 6.7,
                        amount7: 26531,
                        star7: 3.5,

                        score8: 7.1,
                        amount8: 174335,
                        star8: 3.5,

                        score9: 8.0,
                        amount9: 180267,
                        star9: 4.0,
                    }
                }
            }

        }
    }
</script>
<style>
    img {
        margin-top: 25px;
    }
    .a{
        text-align: left;
    }
</style>

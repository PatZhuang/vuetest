<template>
    <el-row type="flex" justify="space-between">
        <el-col :span="1"></el-col>
        <el-col :span="22">
            <el-card>
                <p slot="header" id="ebook-card-title" style="margin: 0; margin-left: 20px; font-weight: 600;">
                    电子图书
                    <span>
                        <a href="#/" class="link small-text" style="margin-left: 0px; display: inline">查看更多>></a>
                    </span>
                </p>
                <el-row type="flex" justify="space-between">
                    <el-col :span="4" v-for="ebook in ebooks.slice(0, 5)" :key="ebook.title">
                        <el-card :body-style="cardBodyStyle">
                            <div style="text-align: left;">
                                <a href="#/"><img :src='ebook.cover' alt="" class="book-cover" style="width: 100%"></a>
                                <a href="#/" class="link small-text">{{ebook.title}}</a>
                                <p class="small-text">￥{{ebook.price}}</p>
                            </div>
                        </el-card>
                    </el-col>
                </el-row>
                <el-row type="flex" justify="space-between">
                    <el-col :span="4" v-for="ebook in ebooks.slice(5)" :key="ebook.title">
                        <el-card :body-style="cardBodyStyle">
                            <div style="text-align: left">
                                <a href="#/"><img :src='ebook.cover' alt="" class="book-cover" style="width: 100%"></a>
                                <a href="#/" class="link small-text">{{ebook.title}}</a>
                                <p class="small-text">￥{{ebook.price}}</p>
                            </div>
                        </el-card>
                    </el-col>
                </el-row>
            </el-card>
        </el-col>
        <el-col :span="1"></el-col>
    </el-row>
</template>

<script>
    export default {
        data() {
            return {
                name: 'ebookPage',
                ebooks: [
                    {
                        title: '未来简史',
                        price: '40.80',
                        cover: require('../assets/ebook/ebook1.jpeg')
                    },
                    {
                        title: '恋情的终结',
                        price: '9.99',
                        cover: require('../assets/ebook/ebook2.jpeg')
                    },
                    {
                        title: '七堂极简物理课',
                        price: '14.99',
                        cover: require('../assets/ebook/ebook3.jpeg')
                    },
                    {
                        title: '故事：材质、结构、风格和银幕剧作的原理',
                        price: '21.99',
                        cover: require('../assets/ebook/ebook4.jpeg')
                    },
                    {
                        title: '当呼吸化为空气',
                        price: '14.40',
                        cover: require('../assets/ebook/ebook5.jpeg')
                    },
                    {
                        title: '新名字的故事',
                        price: '35.00',
                        cover: require('../assets/ebook/ebook6.jpeg')
                    },
                    {
                        title: '杀死一只知更鸟',
                        price: '20.00',
                        cover: require('../assets/ebook/ebook7.jpeg')
                    },
                    {
                        title: '十一种孤独',
                        price: '9.99',
                        cover: require('../assets/ebook/ebook8.jpeg')
                    },
                    {
                        title: '精进：如何成为一个很厉害的人',
                        price: '12.00',
                        cover: require('../assets/ebook/ebook9.jpeg')
                    },
                    {
                        title: '追风筝的人',
                        price: '12.99',
                        cover: require('../assets/ebook/ebook10.jpeg')
                    },
                ],
                cardBodyStyle: {
                    padding: '15px'
                }
            }
        }
    }
</script>

<style scoped>
    #ebook-card-title {
      text-align: left;
      font-size: 20px;
      margin-left: 30px;
    }

    .link {
        display: inline-block;
        width: 100%;
      color: #27ae60;
      text-overflow: ellipsis;
      /*超出部分...*/
      white-space: nowrap;
      /*禁止换行*/
      overflow: hidden;
      /*超出部分隐藏*/
    }

    .link:hover {
      color: #2ecc71;
    }

    .small-text {
      font-size: 13px;
      font-weight: normal;
      margin: 0;
    }

    .book-cover {
        width: 100%;
    }

    .book-cover:hover {
        box-shadow: 4px 4px 4px lightgray;
    }

    .book-cover {
        -webkit-transition: box-shadow .2s;
        -moz-transition: box-shadow .2s;
        transition: box-shadow .2s;
    }
    .el-card {
        border: none;
        box-shadow: none;
    }
</style>
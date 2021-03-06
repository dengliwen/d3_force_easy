## d3ForceEasy
**v1.0.2**

 一个封装D3js force力导向图 简单使用的轮子

>依赖d3.js >v4.0.0

### 示例
> 代码在test文件中

![test1](./img/test1.png)
### 使用方法

    1.npm install d3_force_easy --save
    
    2.引入配置和数据
    
    import  d3ForceEasy from 'd3_force_easy'
    import 'd3ForceEasy.css'
    
    ...
    //基础配置
    const option = {
        dom:document.getElementById('app'),
        nodes:this.nodes,
        links:this.links,
        ...
    }
 
    d3ForceEasy.drawForce(option)

>其他引用方式请引用d3ForceEasy.js文件

### 测试数据
```
const nodes = [
    {name:'2.2.2.2',id:12,type:'ip'},
    {name:'3.4.25.22',id:13,type:'ip'},
    {name:'13020002299',id:14,type:'phone'},
    {name:'asdmklasdlnlwee.pdf',id:15,type:'file'},
    {name:'sdf78f6s87d5fsud7fts87d6587r23grbusd7f78',id:16,type:'md5'},
    {name:'15838837736',id:17,type:'phone'},
]

const links = [
    {source:0,target:1},
    {source:0,target:2},
    {source:0,target:3},
    {source:3,target:4},
    {source:3,target:5},
]

```

### 详细配置
> *为必填项
```
 const option = {
        *dom: document.getElementsByTagName('app'),
        color: '#00a8ff',//单色或['#fff',#'ccc'...]，无color默认随机色
        *nodes:this.nodes,//参考上面的实例数据
        *links:this.links,
        icons:[{type:'ip',icon:'(svg <path>的d路径属性)'},...],
        //icon默认为圆形
        zoom:true,//开启缩放
        zoomRange:[1,8],//缩放范围
        text:{
            show:true, //初始显示文字与否
        },
}
```

### 功能

**新增节点**

    d3ForceEasy.addNodes(newNodesSourceId = 0,newNodes = [])
    //newNodesSourceId->源节点id，newNodes->新增节点数组 
  
**删除选中节点**

    d3ForceEasy.removeNode()
    
**显示/隐藏名称**

    d3ForceEasy.toggleName()    
    
**返回当前选中节点数据**

    d3ForceEasy.currentNode()


### 样式
**可使用css覆盖相应节点和连线的颜色**



升级改造中。。。
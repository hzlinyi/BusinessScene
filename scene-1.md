### case-1:
离线场景下，在流量日志力找出商品流量凸增的时间区间，拿时间区间去商品变更的binlog中匹配该区间内商品做的变更操作，寻找变更内容和流量变化的关系

### scene:
搜索场景、商品关键字优化、商品标题优化等

### 凸增时间区间算法：
流量按照商品分组，取访问时间倒排，计算每次访问和上一次访问的时间差，取时间差值在经验区间范围内，筛选出这部分，取首尾两端的时间，及时凸增时间区间。
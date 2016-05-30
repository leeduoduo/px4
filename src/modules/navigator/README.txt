进入RTL_MODE会首先进行判断
1，如果此时是landed，会直接进入RTL_STATE_LANDED;
2，如果此时是takeoff，但离home position的距离小于5m，不会爬升，而会直接进入RTL_STATE_RETURN;
3，如果此时是takeoff，离home position 的距离大于5m，会进入RTL_STATE_CLIMB;

RTL_MODE的流程一般是：
CLIMB——RETURN——DESCED——LAND——LANDED
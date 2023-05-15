# test_5_15
#include <stdio.h>
//图的存储
//邻接矩阵存储无向图和有向图
#define MaxVertexNum 100
typedef struct{
	char Vex[MaxVertexNum];
	int Edge[MaxVertexNum][MaxVertexNum];
	int vexNum,arcNum;
}MGraph;
//邻接矩阵存储带权图（网）
#define MaxVertexNum 100         //顶点数量最大值
#define INFINITY int的最大值     //宏定义常量无穷
typedef char VextexType;         //顶点数据类型
typedef int EdgeType;            //带权图边上权值数据类型
typedef struct{
	char Vex[MaxVertexNum];
	int Edge[MaxVertexNum][MaxVertexNum];
	int vexNum,arcNum;
}MGraph;
//邻接表法（顺序+链式存储）
//用邻接表法存储的图
#define MaxVertexNum 100 
typedef struct{
	AdjList vertices;//领接表
	int vernum,arcnum;//顶点数和边数
}ALGraph;//领接表存储的图类型
//顶点
typedef struct VNode{       //顶点表结点
	VextexType data;        //顶点信息
	ArcNode *first;         //指向第一条边
}VNode,AdjList[MaxVertexNum];
//边
typedef struct ArcNode{
	int adjvex;//边指向的顶点位置
	struct ArcNode *next;//指向下一条边指针
	//InfoType Info;//边权值
}ArcNode;
//图的基本操作
/*Adjacent(G,x,y);
Neighbors(G,x);
InsertVertex(G,x);
DeleteVertex(G,x);
AddEdge(G,x,y);
RemoveEdge(G,x,y);
FirstNeighbor(G,x);
NextNeighbor(G,x,y);
Get_edge_value(G,x,y);
Set_edge_value(G,x,y);*/

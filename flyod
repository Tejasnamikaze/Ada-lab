#include<stdio.h>
int n;
void display(int dist[][n]);
void floyd (int graph[][n])
{
	int dist[n][n], i, j, k;

	for (i = 0; i < n; i++)
		for (j = 0; j < n; j++)
			dist[i][j] = graph[i][j];

	for (k = 0; k < n; k++)
	{
		for (i = 0; i < n; i++)
		{
			for (j = 0; j < n; j++)
			{
				if (dist[i][k] + dist[k][j] < dist[i][j])
					dist[i][j] = dist[i][k] + dist[k][j];
			}
		}
	}

	display(dist);
}

void display(int dist[][n])
{
	printf ("DISTANCE MATRIX \n");
	for (int i = 0; i < n; i++)
	{
		for (int j = 0; j < n; j++)
		{
			if (dist[i][j] == 99)
				printf("99 ");
			else
				printf ("%d ", dist[i][j]);
		}
		printf("\n");
	}
}

int main()
{
    printf("ENTER ORDER OF MATRIX \n");
    scanf("%d",&n);
    int graph[n][n];
    printf("ENTER ELEMENTS OF MATRIX and 99 FOR INFINITY\n");
    for(int i = 0;i < n;i++)
    {
        for(int j = 0;j < n; j++)
        {
            scanf("%d",&graph[i][j]);
        }
    }
	floyd(graph);
	return 0;
}

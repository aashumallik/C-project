# C-project// SE 185 Lab 8
#include <stdio.h>
# © Aashutosh Mallik

#define MAXPOINTS 10000

// compute the average of the first num_items of buffer
double avg(double buffer[], int num_items);

//update the max and min of the first num_items of array
void maxmin(double array[], int num_items, double* max, double* min);

//shift length-1 elements of the buffer to the left and put the 
//new_item on the right.
void updatebuffer(double buffer[], int length, double new_item);



int main(int argc, char* argv[]) {
	
	/* DO NOT CHANGE THIS PART OF THE CODE */

	double x[MAXPOINTS], y[MAXPOINTS], z[MAXPOINTS]; 													
	int lengthofavg = 0;
	if (argc>1) {																												
		sscanf(argv[1], "%d", &lengthofavg );
		printf("You entered a buffer length of %d\n", lengthofavg);
	}
	else {
		printf("Enter a length on the command line\n");
		return -1;
	}
	if (lengthofavg <1 || lengthofavg >MAXPOINTS) {
		printf("Invalid length\n");
		return -1;
	}


	
	double g_x, g_y, g_z;
	int b1, b2, b3, b4; 
	double maxVal, minVal;
	double avgX, avgY, avgZ;
	int i = 0;
	
	
	for(i = 0; i < lengthofavg; i++){                                                                        
		scanf("%lf, %lf, %lf, %d, %d, %d, %d", &g_x, &g_y, &g_z, &b1, &b2, &b3, &b4);
		updatebuffer(x, lengthofavg, g_x);
		updatebuffer(y, lengthofavg, g_y);
		updatebuffer(z, lengthofavg, g_z);	
	}
	
	do{
		scanf("%lf, %lf, %lf, %d, %d, %d, %d", &g_x, &g_y, &g_z, &b1, &b2, &b3, &b4);
		updatebuffer(x, lengthofavg, g_x);
		updatebuffer(y, lengthofavg, g_y);
		updatebuffer(z, lengthofavg, g_z);
		
		
		avgX = avg(x, lengthofavg);
		avgY = avg(y, lengthofavg);
		avgZ = avg(z, lengthofavg);
		
		printf("%lf, ", avgX);
		printf("%lf, ", avgY);
		printf("%lf, ", avgZ);
		
		printf("%lf, ", g_x);
		printf("%lf, ", g_y);
		printf("%lf, ", g_z);
		
		maxmin(x, lengthofavg, &maxVal, &minVal);
		printf("%lf, %lf, ", maxVal, minVal);
		
		maxmin(y, lengthofavg, &maxVal, &minVal);
		printf("%lf, %lf, ", maxVal, minVal);
		
		maxmin(z, lengthofavg, &maxVal, &minVal);
		printf("%lf, %lf", maxVal, minVal);
		
		printf("\n");
		fflush(stdout);
		
		
	}
	while(b4 != 1);
	
	



}
/* Grabs the average inside the array until num_items */
double avg(double buffer[], int num_items){
	int i = 0;                               
	double avgValue = 0, sum = 0;
	for(i = 0; i <= num_items; i++){
		sum = sum + buffer[i];
	}
	avgValue = sum / num_items;
	return avgValue;
}

void maxmin(double array[], int num_items, double* max, double* min){
	int i = 0;
	*max = array[0];
	*min = array[0];
	
	for (i = 0; i < num_items; i++){
		if(array[i] > *max){
			*max = array[i];
		}
		if(array[i] < *min){
			*min = array[i]; 
		}
	}
	
}

void updatebuffer(double buffer[], int length, double new_item){
	int i = 0;
	for (i = 0; i < length; i++){
		buffer[i] = buffer[i+1];
	}
	buffer[length-1] = new_item;
}



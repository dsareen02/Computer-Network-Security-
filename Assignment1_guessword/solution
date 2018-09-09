# include <stdio.h>
#include <stdlib.h>
#include<string.h>
#include<unistd.h>
//global variables
/*struct user{
	cha username[6], name[10], surname[10],password[100];
}*/
//argc will be the number of strings pointed to by argv
int main(int argc, char *argv[]){
char *line_pointer=NULL;
size_t buffer_length=0;
ssize_t each_line_pass_file;
char val1[20],val2[20],val3[20],pass_extracted[100];
//setting pointer of type file.
	//ptr=fopen("filename", "mode");
	//or FILE *ptr=fopen("filename", "mode");
	/*for(int i=0;i<argc;i++){
		printf(argv[i]);
		printf(" ");
	}
*/
//argv[1]=password file, argv[2]= shadow file
FILE *read_password_file=fopen(argv[1],"r");

FILE *write_temp_dictionary=fopen("temp_dictionary.txt","w");

while((each_line_pass_file=getline(&line_pointer, &buffer_length,read_password_file))!=-1){
	//scanf - read from standard input device
//sscanf - read from a string
	sscanf(line_pointer,"%s%s%s%s",val1,val2,val3,pass_extracted);
	fputs(pass_extracted, write_temp_dictionary);
	fputs("%s\n",write_temp_dictionary);

}  

fclose(read_password_file);
fclose(write_temp_dictionary);

}

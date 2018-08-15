# openGL
// openGLTest.cpp: 定义控制台应用程序的入口点。
//

#include "stdafx.h"
#include <Windows.h>
#include <gl/GL.h>
#include <GL/GLU.h>
#include <GL/glut.h>

 void  init(void)
{
	glClearColor(1.0, 1.0, 1.0, 0.0);																																								
	glMatrixMode(GL_PROJECTION);
	gluOrtho2D(0.0, 200.0, 0.0, 150.0);
} 

 void lineSegment(void)
{
	 glClear(GL_COLOR_BUFFER_BIT);
	 glColor3f(0.0, 0.0, 0.0);
	 glBegin(GL_LINES);
			glVertex2i(180, 15);
	        glVertex2i(10, 145);
	 glEnd();
	 glFlush();
}
int main(int argc, char** argv)
{
	glutInit(&argc, argv);
	glutInitDisplayMode(GLUT_SINGLE | GLUT_RGB);
	glutInitWindowPosition(50, 100);
	glutInitWindowSize(400,300);
	glutCreateWindow("Example");
	glutDisplayFunc(lineSegment);
	init();
	glutMainLoop();
}



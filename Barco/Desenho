//Classe Desenho
package barco;

import java.awt.Graphics;
import javax.swing.JComponent;

public class Desenho extends JComponent{
   
    public void paint(Graphics g){
           
        //Mastro:
        coordenadas(g,280,220,281,500); //lateral esquerda
        coordenadas(g,281,220,282,500); //lateral esquerda 2
        coordenadas(g,300,220,301,500); //lateral direita
        coordenadas(g,301,220,302,500); //lateral direita 2
        coordenadas(g,280,220,300,221); //parte superior
       
        //Casco:
       
        coordenadas(g,20,500,120,600); //lateral esquerda
        coordenadas(g,120,600,500,601); //parte inferior
        coordenadas(g,121,600,501,601); //parte inferior 2
        coordenadas(g,500,600,600,500); //lateral direita
        coordenadas(g,20,500,600,501); //parte superior
        coordenadas(g,20,501,600,502); //parte superior
       
       
        //Bandeira
       
        coordenadas(g,274,225,275,255); //lateral direita
        coordenadas(g,224,225,274,226); //lateral superior
        coordenadas(g,224,255,274,256); //lateral inferior
        coordenadas(g,224,255,239,240); //corte superior
        coordenadas(g,224,225,239,240); //corte inferior
       
       
        //Vela direita:
       
        coordenadas(g,306,218,550,462); //lateral direita
        coordenadas(g,307,218,551,462); //lateral direita 2
        coordenadas(g,306,218,307,462); //lateral esquerda
        coordenadas(g,307,218,308,462); //lateral esquerda 2
        coordenadas(g,306,462,550,463); //lateral inferior
        coordenadas(g,306,463,550,464); //lateral inferior 2
       
       
        //Vela esquerda:
       
        coordenadas(g,274,262,275,462); //lateral direita
        coordenadas(g,275,262,276,462); //lateral direita 2
        coordenadas(g,274,262,74,462); //lateral esquerda
        coordenadas(g,275,262,75,462); //lateral esquerda 2
        coordenadas(g,74,462,274,463); //lateral inferior
        coordenadas(g,74,463,274,464); //lateral inferior 2
       
       
        //PINTURA CASCO:
        // y1 = y1 +3, y2 = y2 + 3, x1 = x1 + 3 , x2 = x2-3  enquanto y2 < 601
        //Inicial:  coordenadas(g,20,500,600,501);
 
        int x1,x2,y1,y2;
        for( x1= 20,  x2 = 600, y1 = 500, y2 = 501; y2 < 601; y1= y1+3, y2 = y2 +3, x1 = x1+3, x2 = x2 -3 )
        {
            coordenadas(g,x1,y1,x2,y2);
        }
     
       
        //PINTURA VELA DIREITA:
       
        //inicial: coordenadas(g,306,218,550,462);
       
        for(x1 = 306, x2 = 550, y1 = 218, y2=462; x2 > 306; y1= y1+20, x2 = x2 -20 )
        {
           coordenadas(g,x1,y1,x2,y2);  
        }
       
       
        //PINTURA VELA ESQUERDA:
        //inicial: coordenadas(g,274,262,74,462);
        for(x1 = 274, x2 = 74, y1 = 262, y2=462; x2 < 274; y1= y1+20, x2 = x2 +20 )
        {
           coordenadas(g,x1,y1,x2,y2);  
        }
       
       
       
        //Pintura mastro:
        //coordenadas(g,280,220,301,221); //parte superior
       
        //Riscas horizontais duplas:
       for(x1 = 280, x2 = 300, y1 = 220, y2=221; y2 < 501; y1= y1+30, y2=y2+30  )
        {
           coordenadas(g,x1,y1,x2,y2);
           coordenadas(g,x1,y1+1,x2,y2+1);
        }
       
       //riscas horizontais menores:
       for(x1 = 285, x2 = 300, y1 = 220, y2=221; y2 < 501; y1= y1+5, y2=y2+5  )
        {
           coordenadas(g,x1,y1,x2,y2);
           
        }
       
       //risca vertical 3x:
       coordenadas(g,291,220,292,500);
       coordenadas(g,290,220,291,500);
       coordenadas(g,289,220,290,500);
       
        //PINTURA BANDEIRA PARTE SUPERIOR:
        //inicial: coordenadas(g,224,225,274,226);
       
        for(x1 = 224, x2 = 274, y1 = 225, y2=226; y1 < 240; x1 = x1+1, y1= y1+1, y2= y2+1 )
        {
           coordenadas(g,x1,y1,x2,y2);  
        }
       
        //PINTURA BANDEIRA PARTE INFERIOR:
        //inicial: coordenadas(g,224,255,274,256);
        for(x1 = 224, x2 = 274, y1 = 255, y2 = 256; y1 > 239; x1 = x1+1, y1= y1-1, y2= y2-1 )
        {
           coordenadas(g,x1,y1,x2,y2);  
        }
       
       
       
       
       
       
    }
   
    private void putPixel(Graphics g, int x, int y){
        g.drawLine(x, y, x, y);
    }
   
    private void coordenadas(Graphics g, int xi, int yi, int xf, int yf){
       
        int x=xi, y=yi;
        int dx = xf - xi;
        int dy = yf - yi;
       
        int steps = (dx > dy) ? dx : dy;
       
        float xinc = dx / steps;
        float yinc = dy / steps;
       
        for(int i=0; i<steps;i++) {
            x += xinc;
            y += yinc;
            putPixel(g,x,y);
        }
       
    }
   
}

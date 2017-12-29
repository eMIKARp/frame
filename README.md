# frame
a piece of code that displays a simple frame on your screen 

package frame;

import javax.swing.*;
import java.awt.*;

public class Main extends JFrame
{
    public Main()                                
    {
        
        int scrHeight = Toolkit.getDefaultToolkit().getScreenSize().height; // obtaining screen size 
        int scrWidth = Toolkit.getDefaultToolkit().getScreenSize().width;
        
        this.setSize(scrWidth / 2, scrHeight / 2);   // defining size of a frame we want to create
        
        int fraWidth = this.getSize().width;
        int fraHeight = this.getSize().height;
        
        this.setLocation((scrWidth - fraWidth)/2, (scrHeight - fraHeight)/2);   // setting location of a frame to center 
                                                                                // regardess of the screen and frame size 
        this.setTitle("It's Alive !!!");
        this.setIconImage(Toolkit.getDefaultToolkit().getImage("anonymous.png"));
        this.setResizable(false);
        this.setDefaultCloseOperation(3);
    }
    
    public static void main(String[] args) 
    {
        new Main().setVisible(true);                  
        
    }
    
}


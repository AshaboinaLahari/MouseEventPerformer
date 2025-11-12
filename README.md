# MouseEventPerformer
This program that handles all mouse events and shows the event name at the window when a mouse event is fired
import java.awt.FlowLayout;
import java.awt.event.MouseEvent;
import java.awt.event.MouseListener;

import javax.swing.JFrame;
import javax.swing.JLabel;

public class MouseEventPerformer extends JFrame implements MouseListener
{
	JLabel l1;	
	
	public MouseEventPerformer()
	{
		setVisible(true);
		setSize(500,500);
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setLayout(new FlowLayout());
		
		l1=new JLabel();
		add(l1);
		addMouseListener(this);
		
	}


	public static void main(String[] args)
	{
		MouseEventPerformer m=new MouseEventPerformer();
	}


	@Override
	public void mouseClicked(MouseEvent e)
	{
		l1.setText("Mouse clicked");
	}


	@Override
	public void mousePressed(MouseEvent e)
	{
		l1.setText("Mouse Pressed");	
	}


	@Override
	public void mouseReleased(MouseEvent e)
	{
		l1.setText("Mouse entered");
	}


	@Override
	public void mouseEntered(MouseEvent e) 
	{
	
		l1.setText("Mouse exit");
	}


	@Override
	public void mouseExited(MouseEvent e) {
		// TODO Auto-generated method stub
		
	}
}

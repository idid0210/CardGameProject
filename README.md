package Login;

import javax.swing.*;
import javax.swing.event.*;
import java.awt.*;
import java.awt.event.*;

public class FirstPage extends JFrame implements ActionListener{
	JLabel textLabel;
	JLabel imageLabel;
	JButton login;
	JButton exit;
	
	public FirstPage(){
		this.setTitle("짝 맞추기 게임 - by.PLUS");
		this.setSize(600, 600);	//setSize 창의 크기 지정하는 메소드
		this.setLocation(200,200);	//윈도우화면에서 창의 위치정하는 메소드(좌표 x, y)
		this.setDefaultCloseOperation(DISPOSE_ON_CLOSE); //창 닫을때 프로그램 종료시킴
		this.setContentPane(new MyPanel());
		this.setLayout(new FlowLayout());
		
//		textLabel = new JLabel("고스톱 짝 맞추기!!");
		
		ImageIcon img = new ImageIcon("images/38dd.jpg");
		JLabel imageLabel = new JLabel(img);
		
//		this.add(textLabel);
		this.add(imageLabel);
		
		
		
		this.setVisible(true);
		
	}
	class MyPanel extends JPanel{
		public void paintComponent(Graphics g){
			super.paintComponent(g);
			g.setFont(new Font("Arial",Font.ITALIC,30));
			g.drawString("고스톱 게임!", 250, 0);
		}
	}
	
	public static void main(String[] args) {
		new FirstPage();
	}

	@Override
	public void actionPerformed(ActionEvent e) {
		// TODO Auto-generated method stub
		
	}

}

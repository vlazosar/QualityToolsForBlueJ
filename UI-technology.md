                                          Swing
Swing is a good user interface technoly for this blue J project.

Definition of Swing: 

Swing is a framework in java that create user interface.Since it is based on java language, it is object oriented. It contains various classes that extend one another, and the notion of extending a base class to add required functionality to that class is key to user interface programming in Java (and indeed in other languages). Another key part of Swing programming is the notion of listeners: classes or components that "listen out for" a particular event happening such as a button being clicked. And listeners are generally implemented as Java interfaces.The class of swing start with letter J. For example, JFrame, JButton, JPanel etc. Let's view thw swing components,

1.JFrame:
a jframe is a top levl window with a title and a border. The size of the frame window contain any area and it can invoke inside the method. Here is the simple class for the jframe:

class MyFrame extends Jframe{

JFrame frame = new JFrame("frame");

}

Some important method JFrame:<br>
frame,setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE); It will determine what happens after the window close.
frame.getContentPanel().add(emptyLabel.BorderLaout.CENTER); it helps to add created component into the JFrame.
frame.pack(): it size the frame.<br>
frame.setVisible(true): it allows the frame appears on the screen.<br>
Frame.setLocation(int dimentions, int dimention): it sets the location of the frame on the screen.

2.JLabel:<br>
It makes to apear single line of words on the Jframe.<br>
Given below is the objective way of creatin new JLable<br>
JLable lable = new JLable();<br>

Some important methods are:<br>
a)String getText();<br>
b)void setText(String text);<br>
c)void setHorizontalAlignment(int alignment);<br>
d)Icon getIcon();<br>
e)int getHorizontalAlignment();<br>

3.JTextField:<br>
JTextField helps to get text from the user. Here is the simple way of writing code<br>

public class JTextField extends JTextComponent{
}

<br>
Here are the import methods of JTextField class:<br>
a)void addActionListener(ActionListerner);<br>
b)Action getAction();<br>
c)Void setFont(Font f)<br>
d)void removeActionListener(ActionListener I);<br>


4.JBotton:<br>
public class JButton extends AbstractButton<br>
JBotton use to click and to do whatever it assigned.<br>
Some important methods are:<br>
a)void setText(String s);<br>
b) String getText();<br>
c)void setEnabled(boolean b);<br>
d)void setIcon(Icon b)<br>
e)Icon getIcon();<br>
d)void setMnemonic(int a);<br>
e)void addActionListener(ActionListener a);<br>

5.JRadioButton<br>
JRadioButton is usefull where there is a need os many button at once.<br>
a)getAccessibleContext();<br>
b)String getUICassID()<br>
c)protected String paramString()<br>
d)void updateUI();<br>

other componets are:<br>
JEditorPane,JDaiLog,JDesktopPane, JTree, JProgressBar, JTogglebButton, JToolBar,JMenuBar, JComboBox,JCheckBox<br>

Reasons to use swing in quality tool to Bluej:<br>
It provides the graphical interface that work for all operating system. Since it is a object oriented, it is easy to implement. Listners does that extention has to do as long as it is clicked. It also has the method that close the window as long as it is clicked. Overall swing provides nice interface that interact with user.

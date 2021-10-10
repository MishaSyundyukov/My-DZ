import javax.swing.*;
import java.awt.*;
class Example {
    public static void main(String args[]) {

        JFrame frame = new JFrame("Chat Frame");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(600, 600);
        JPanel panel = new JPanel();
        JLabel label = new JLabel("Текст");
        JTextField tf = new JTextField(100);
        JButton send = new JButton("Отпрвить");
        panel.add(label);
        panel.add(label);
        panel.add(tf);
        panel.add(send);
        JTextArea ta = new JTextArea();
        frame.getContentPane().add(BorderLayout.SOUTH, panel);
        frame.getContentPane().add(BorderLayout.NORTH, tf);
        frame.getContentPane().add(BorderLayout.CENTER, ta);
        frame.setVisible(true);
    }
}

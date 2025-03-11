using System;
using System.Windows.Forms;

public class MyForm : Form
{
    public MyForm()
    {
        // Set the title of the form
        this.Text = "My First UI";

        // Create a label
        Label label = new Label();
        label.Text = "Hello, World!";
        label.Location = new System.Drawing.Point(10, 10);
        this.Controls.Add(label);

        // Create a button
        Button button = new Button();
        button.Text = "Click me!";
        button.Location = new System.Drawing.Point(10, 40);
        button.Click += new EventHandler(Button_Click);
        this.Controls.Add(button);
    }

    private void Button_Click(object sender, EventArgs e)
    {
        MessageBox.Show("Button clicked!");
    }

    [STAThread]
    static void Main()
    {
        Application.EnableVisualStyles();
        Application.SetCompatibleTextRenderingDefault(false);
        Application.Run(new MyForm());
    }
}
<!---
Koketsotjeta89/Koketsotjeta89 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

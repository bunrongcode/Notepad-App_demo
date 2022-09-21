namespace Create_Notepad
{
    public partial class Form1 : Form
    {
        String path = String.Empty;
        public Form1()
        {
            InitializeComponent();
        }

        private void exitPrompt()
        {
            DialogResult = MessageBox.Show("Do you want to save current file?",
                "Notepad",
                MessageBoxButtons.YesNoCancel,
                MessageBoxIcon.Question,
                MessageBoxDefaultButton.Button2);
        }
        private void newTool_Click(object sender, EventArgs e)
        {
            if (!String.IsNullOrWhiteSpace(richTextBox1.Text))
            {
                exitPrompt();

                if (DialogResult == DialogResult.Yes)
                {
                    saveTool_Click(sender, e);
                    richTextBox1.Text = String.Empty;
                    path = String.Empty; ;
                }
                else if (DialogResult == DialogResult.No)
                {
                    richTextBox1.Text = String.Empty; ;
                    path = String.Empty; ;
                }
            }
        }

        private void saveTool_Click(object sender, EventArgs e)
        {
            if (!String.IsNullOrWhiteSpace(path))
            {
                File.WriteAllText(path, richTextBox1.Text);
            }
            else
            {
                saveAsToolStripMenuItem_Click(sender, e);
            }
        }

        private void openTool_Click(object sender, EventArgs e)
        {
            OpenFileDialog ofd = new OpenFileDialog();
            if (ofd.ShowDialog() == DialogResult.OK)
            {
                richTextBox1.Text = File.ReadAllText(path = ofd.FileName);
                string[] SplitExtension = ofd.FileName.Split('.');
                //labelFormat.Text = ReturnMessageFromFormat(SplitExtension[1]);

            }
        }

        private void saveAsToolStripMenuItem_Click(object sender, EventArgs e)
        {
            SaveFileDialog sfd = new SaveFileDialog();
            if (sfd.ShowDialog() == DialogResult.OK)
            {
                File.WriteAllText(path = sfd.FileName, richTextBox1.Text);
            }
        }

        private void exitTool_Click(object sender, EventArgs e)
        {
            Application.Exit();
        }

        private void formatToolStripMenuItem_Click(object sender, EventArgs e)
        {

        }

        private void undoTool_Click(object sender, EventArgs e)
        {
            richTextBox1.Undo();
        }

        private void redoTool_Click(object sender, EventArgs e)
        {
            richTextBox1.Redo();
        }

        private void cutTool_Click(object sender, EventArgs e)
        {
            richTextBox1.Cut();
        }

        private void copyTool_Click(object sender, EventArgs e)
        {
            richTextBox1.Copy();
        }

        private void pasteTool_Click(object sender, EventArgs e)
        {
            richTextBox1.Paste();
        }

        private void selectAllTool_Click(object sender, EventArgs e)
        {
            richTextBox1.SelectAll();
        }

        private void timeDateTool_Click(object sender, EventArgs e)
        {
            richTextBox1.Text = System.DateTime.Now.ToString();
        }

        private void fontTool_Click(object sender, EventArgs e)
        {
            FontDialog fd = new FontDialog();
            if (fd.ShowDialog() == DialogResult.OK)
            {
                richTextBox1.Font = richTextBox1.Font = new Font(fd.Font, fd.Font.Style);
                richTextBox1.ForeColor = fd.Color;
            }
        }

        private void wordWrapTool_Click(object sender, EventArgs e)
        {
            if (wordWrapTool.Checked == true)
            {
                richTextBox1.WordWrap = false;
                //richTextBox1.ScrollBars = ScrollBars.Both;
                wordWrapTool.Checked = false;
            }
            else
            {
                richTextBox1.WordWrap = true;
                //richTextBox1.ScrollBars = ScrollBars.Vertical;
                wordWrapTool.Checked = true;
            }
        }

        private void deleteTool_Click(object sender, EventArgs e)
        {
            richTextBox1.SelectedText = String.Empty;
        }

        private void editToolStripMenuItem_Click(object sender, EventArgs e)
        {

        }

        private void colorTool_Click(object sender, EventArgs e)
        {
            ColorDialog cd = new ColorDialog();
            if (cd.ShowDialog() == DialogResult.OK)
            {
                richTextBox1.ForeColor = cd.Color;
            }
        }

        private void findTool_Click(object sender, EventArgs e)
        {

        }
    }
}

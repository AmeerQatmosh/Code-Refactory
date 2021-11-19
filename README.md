# Advanced Software Development
# Code Refactory

This refactored code addresses the following problems:

1. Poor variable naming
2. Magic Numbers
3. No needed classes and methods 
4. No needed libraries

## 1. Poor variable naming
## 2. Magic Numbers
## 3. No needed classes and methods
example 1: 
class saveAsText in this part of code:

private void saveAsText(String dialogTitle) {
		JFileChooser dialog = new JFileChooser(System.getProperty("user.home"));
		dialog.setDialogTitle(dialogTitle);
		int result = dialog.showSaveDialog(this);
		if (result != approve)
			return;
		file = dialog.getSelectedFile();
		try (PrintWriter writer = new PrintWriter(file);){
			writer.write(TP.getText());
			changed = false;
			setTitle(Strings.saveAsMsg + file.getName());
		} catch (FileNotFoundException e) {
			e.printStackTrace();
		}    
      }
  
 example 2: 	
 method move in this part of code:
 move = new JMenuItem("Move"); 
 move.setMnemonic('M');
 move.setAccelerator(KeyStroke.getKeyStroke(KeyEvent.VK_V, InputEvent.CTRL_DOWN_MASK));
 edit.add(move);
 move.addActionListener(this);
   
## 4. No needed libraries
example: java.awt.BorderLayout


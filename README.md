/*
 * RaCoc9605
 * pizzaPriceCalculator.java
 * This calculates the price of a pizza given any diameter.
 */

/**
 *
 * @author RaCoc9605
 */
public class pizzaPriceCalculator extends javax.swing.JFrame {

    /**
     * Creates new form pizzaPriceCalculator
     */
    public pizzaPriceCalculator() {
        initComponents();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        diameter = new javax.swing.JLabel();
        title = new javax.swing.JLabel();
        sizeInput = new javax.swing.JTextField();
        answerLabel = new javax.swing.JLabel();
        calculateButton = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        diameter.setFont(new java.awt.Font("Tahoma", 0, 24)); // NOI18N
        diameter.setText("Diameter of Pizza (inches)");

        title.setFont(new java.awt.Font("Tahoma", 0, 48)); // NOI18N
        title.setText("Pizza Price Calculator");

        sizeInput.setFont(new java.awt.Font("Tahoma", 0, 15)); // NOI18N
        sizeInput.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                sizeInputActionPerformed(evt);
            }
        });

        answerLabel.setFont(new java.awt.Font("Tahoma", 0, 14)); // NOI18N
        answerLabel.setText("Enter the diameter of your pizza and hit the calculate button!");

        calculateButton.setFont(new java.awt.Font("Tahoma", 0, 12)); // NOI18N
        calculateButton.setText("Calculate");
        calculateButton.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                calculateButtonActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(80, 80, 80)
                .addComponent(title)
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addContainerGap(51, Short.MAX_VALUE)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(answerLabel)
                    .addGroup(layout.createSequentialGroup()
                        .addComponent(diameter)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addGroup(layout.createSequentialGroup()
                                .addGap(63, 63, 63)
                                .addComponent(calculateButton)
                                .addGap(16, 16, 16))
                            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addComponent(sizeInput, javax.swing.GroupLayout.PREFERRED_SIZE, 115, javax.swing.GroupLayout.PREFERRED_SIZE)))))
                .addGap(117, 117, 117))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(38, 38, 38)
                .addComponent(title)
                .addGap(32, 32, 32)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(diameter)
                    .addComponent(sizeInput, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(30, 30, 30)
                .addComponent(calculateButton)
                .addGap(45, 45, 45)
                .addComponent(answerLabel)
                .addContainerGap(58, Short.MAX_VALUE))
        );

        pack();
    }// </editor-fold>                        

    private void calculateButtonActionPerformed(java.awt.event.ActionEvent evt) {                                                
        double labour = 1.00;
        double storeCost = 1.50;
        double diameter = Double.parseDouble(sizeInput.getText());
        double materials = diameter * 0.50;
        
        //This algorithm will calcuate the price of the pizza.
        double pizzaPrice = labour + storeCost + materials;
        
        String name;
        name = sizeInput.getText();
        
        answerLabel.setText ("Your pizza will cost " + pizzaPrice + " dollars.");
    }                                               

    private void sizeInputActionPerformed(java.awt.event.ActionEvent evt) {                                          

    }                                         

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(pizzaPriceCalculator.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(pizzaPriceCalculator.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(pizzaPriceCalculator.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(pizzaPriceCalculator.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new pizzaPriceCalculator().setVisible(true);
            }
        });
        
        
        
    }

    // Variables declaration - do not modify                     
    private javax.swing.JLabel answerLabel;
    private javax.swing.JButton calculateButton;
    private javax.swing.JLabel diameter;
    private javax.swing.JTextField sizeInput;
    private javax.swing.JLabel title;
    // End of variables declaration                   
}

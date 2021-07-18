
package hangmangame;


public class HANGMANGAME {

   
    public static void main(String[] args) {
                
        
        DESIGNFLASHSCREEN splash = new DESIGNFLASHSCREEN();
        start st= new start();
        splash.setVisible(true);
       
        
        try {
            for(int i=0; i<=100;i++){
                Thread.sleep(20);
                splash.percent.setText(Integer.toString(i)+ "%");
                splash.loading.setValue(i);
                if(i==100){
                    splash.setVisible(false);
                   st.setVisible(true);
                }

            }
        } catch (Exception e) {
        }
    }
    
}

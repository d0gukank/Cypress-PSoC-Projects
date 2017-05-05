/* ========================================
 *
 * Copyright YOUR COMPANY, THE YEAR
 * All Rights Reserved
 * UNPUBLISHED, LICENSED SOFTWARE.
 *
 * CONFIDENTIAL AND PROPRIETARY INFORMATION
 * WHICH IS THE PROPERTY OF your company.
 *
 * ========================================
*/
#include <project.h> 
#include <stdio.h>

int main()
{ 
    int centigrados ;  
    LCD_Start();  
    char VARIABLESCKF [15]; 
    int K,F; 
    float32 conversion1; 
     CyGlobalIntEnable;   
    ADC1_Start(); 
    ADC1_StartConvert(); 
    ADC1_IsEndConversion (ADC1_WAIT_FOR_RESULT); 
     
    for (;;) 
    { 
        LCD_Position(0,0);
        LCD_PrintString("  TEMPERATURA  "); 
        conversion1 = ADC1_GetResult16(0);          
       // conversion1 = (conversion1/255)*5000; 
        centigrados = (conversion1*0.04395); 
        K = centigrados+273; 
        F = centigrados*1.8+32; 
        sprintf(VARIABLESCKF,"%dC %dK %dF", centigrados,K,F); 
        LCD_Position(1,0); 
        LCD_PrintString(VARIABLESCKF); 
        CyDelay(300); 
        
    
    }
}

/* [] END OF FILE */

Rampas ou placas compatíveis com firmware Marlin
================================================



.. Note:: O firmware Marlin é usado para controlar o embosseuse Braille. Nous usa a configuração CNC para controlar o sistema elétrico com comandos associados ao motor de CNC / stylo / laser (GCODE M3 e M4)


Configuração Marlin
-------------------

em configuration.h 

Configuração da placa-mãe ::

   #ifndef MOTHERBOARD
     //#define MOTHERBOARD BOARD_RAMPS_14_EFB
     #define MOTHERBOARD BOARD_RAMPS_14_SF
   #endif

Configuração de fuso / laser / caneta ::

   // BRAILLE RAP CONFIG
   #define SPINDLE_LASER_ENABLE
   #define SPINDLE_LASER_ENABLE_PIN  RAMPS_D8_PIN      // !!! for BED MOSFET
   #define SPINDLE_LASER_PWM_PIN     RAMPS_D10_PIN     // !!! for E0 MOSFET 
   #define SPINDLE_DIR_PIN           5                 // pin servo


Configuração de parada final ::

   // O fim de curso mecânico com COM para aterrar e NC para Sinal usa "false" aqui (configuração mais comum).
   #define X_MIN_ENDSTOP_INVERTING false // set to true to invert the logic of the endstop.
   #define Y_MIN_ENDSTOP_INVERTING false // set to true to invert the logic of the endstop.
   #define Z_MIN_ENDSTOP_INVERTING false // set to true to invert the logic of the endstop.
   #define X_MAX_ENDSTOP_INVERTING false // set to true to invert the logic of the endstop.
   #define Y_MAX_ENDSTOP_INVERTING false // set to true to invert the logic of the endstop.
   #define Z_MAX_ENDSTOP_INVERTING false // set to true to invert the logic of the endstop.
   #define Z_MIN_PROBE_ENDSTOP_INVERTING false // set to true to invert the logic of the probe.


Passo do motor / mm ::

   #define DEFAULT_AXIS_STEPS_PER_UNIT   { 80, 46, 4000, 500 }

Velocidade máxima de alimentação ::

   #define DEFAULT_MAX_FEEDRATE          { 300, 300, 5, 25 }

Aceleração ::

   #define DEFAULT_MAX_ACCELERATION      { 1500, 1500, 100, 10000 }

   #define DEFAULT_ACCELERATION          1500    // X, Y, Z and E acceleration for printing moves
   #define DEFAULT_RETRACT_ACCELERATION  1500    // E acceleration for retracts
   #define DEFAULT_TRAVEL_ACCELERATION   1500    // X, Y, Z acceleration for travel (non printing) moves

Empurrão ::

   #define DEFAULT_XJERK                 5.0
   #define DEFAULT_YJERK                 5.0
   #define DEFAULT_ZJERK                 0.3
   #define DEFAULT_EJERK                 5.0

Na versão atual do github BrailleRap-SP, outros arquivos foram modificados para lidar com a posição da folha de papel com o ponto final em Y.
 
 





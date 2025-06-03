За 30 эпох имеем соответствующие результаты:

*U-Net Model*

        Class    IoU
        
           Sky 0.8553
           
      Building 0.9383
      
          Pole 0.8644
          
          Road 0.9868
          
      Pavement 0.9822
      
          Tree 0.2263
          
    SignSymbol 0.7559
    
         Fence 0.7717
         
           Car 0.9621
           
    Pedestrian 0.9934
    
     Bicyclist 0.0006
     
    Unlabelled    N/A
    
      Mean IoU 0.7579
      
Pixel Accuracy 0.9875


*Transformer*

         Class   IoU
         
           Sky 0.9471
           
      Building 0.9688
      
          Pole 0.9835
          
          Road 0.9829
          
      Pavement 0.7079
      
          Tree 0.7735
          
    SignSymbol 0.6892
    
         Fence 0.9579
         
           Car 0.9918
           
    Pedestrian 0.7356
    
     Bicyclist    N/A
     
    Unlabelled    N/A
    
      Mean IoU 0.8738
      
Pixel Accuracy 0.9854


- Трансформер здесь явно выигрывает на любых объектах, показатели достаточны высоки. Отличные показатели на Pole, Road, Car.
  
- А вот Ю-нетовская модель очень слаба на Tree, Bicyclist, у неё явно меньше Mean IoU.
  
- Pixel Accuracy одинакова. Я считаю, что 2 тысячными можно пренебречь.
  
- Поэтому могу сделать вывод, что в большинстве своём выигрывает трансформер. Да, по времени он явно обучается дольше и иногда требует немного больше памяти, но зато он продуктивней и содержит раз в 7 меньше параметров.

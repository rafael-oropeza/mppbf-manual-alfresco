Modelo din�mico
=========

�Qu� es el modelo din�mico ?
-------
El *modelo din�mico* es un **conjunto de ecuaciones que describen la actitud y posici�n del dispositivo.**

concepto quadrotor
-------
El robot [Erle](http://erlerobot.com) es un *quadric�ptero*:

> Un quadric�ptero, tambi�n llamado un helic�ptero quadrotor , quadrotor , es un helic�ptero multirotor que es levantado y propulsado por cuatro rotores. Quadcopters se clasifican como helic�pteros , en oposici�n a las aeronaves de ala fija , porque su elevaci�n es generada por un conjunto de perfiles de ala giratoria estrecha - acordes.

Desde el � D�as RST en el desarrollo del helic�ptero, el dise�o quadrotor fue visto como una alternativa. En un helic�ptero Coni � regular? ? Guraci�n del par es contrarrestado por el rotor de cola . Cuando se utilizan dos rotores de los pares de los rotores pueden compensado por unos a otros . Pero dos rotores crear a�n tiene desaf�os en el control como los movimientos de rotaci�n y traslaci�n son a�n altamente acoplados .

Con cuatro rotores del control se hace m�s f�cil y los movimientos de rotaci�n se puede desacoplar de los � IE � ects girosc�picos . Movimientos de traslaci�n se logran por la inclinaci�n del veh�culo . En la disposici�n m�s com�n para quadrotor , los * dos pares de rotores ( 1 , 3 ) y ( 2 , 4 ) a su vez en direcciones opuestas * como se muestra en la figura:

![quad](../img/quad.png)

Mediante la variaci�n de la velocidad del rotor, uno puede cambiar las fuerzas de elevaci�n y crear movimiento. El aumento o la disminuci�n de las cuatro velocidades de rotor juntos genera un movimiento vertical. El cambio de los 2 y 4 h�lices aceleran produce a la inversa ** ** rollo rotaci�n , junto con el movimiento lateral. Paso ** ** rotaci�n y el resultado de movimiento lateral correspondiente de 1 y 3 h�lices de velocidad inversa modii � ? Ed. Yaw ** ** Resultados de rotaci�n del � Dii � rencia en la lucha contra el par entre los pares de rotores .

### Ventajas y desventajas
Puesto que s�lo empuj� el control se puede utilizar para cambiar de posici�n, control de la hoja de paso de los rotores no es necesario y por lo tanto la mec�nica del rotor * son simpli� � ? Ed , que hacen que el dise�o quadrotor interesante para los m�s peque�os de tama�o vertical / Short Take O� � � y aterrizaje UAVs ( V / STOL ) ( Unmanned Aerial Vehicles ) * . Otra ventaja es
que con un quadrotor el empuje se utiliza �nicamente para compensar el peso y no para contrarrestar el par de torsi�n , debido a que los cuatro rotores eliminar el IE girosc�pico � � ect , de modo de empuje se utiliza completamente para llevar la carga �til .

Para micro UAVs , cuatro resultados rotores en un di�metro muy peque�o rotor , que penaliza la IE � �ciency y aumenta el consumo de energ�a para conseguir la elevaci�n similar. Tambi�n el tama�o y el peso de una carga �til con quadrotor similares es m�s alto que un helic�ptero normal. El � simpli� ? Cationes en la construcci�n y control que es o� � � Ered por el concepto , hace que sea todav�a un dise�o muy favorable para UAVs .

Modelo din�mico de un quadrotor
-------

El modelo din�mico * del * quadrotor es b�sicamente la de un cuerpo r�gido que rota con seis grados de libertad y cuatro entradas .

De acuerdo con [ QuadCopter Dynamics, simulaci�n y Control](http://andrew.gibiansky.com/downloads/pdf/Quadcopter%20Dynamics,%20Simulation,%20and%20Control.pdf):

> El desarrollo de quadcopters ha estancado hasta hace muy poco , porque ** controlar cuatro rotores independientes ha demostrado ser incre�blemente dif�cil ** e imposible sin la ayuda electr�nica. La disminuci�n del costo de los microprocesadores modernos ha hecho del control electr�nico e incluso completamente aut�noma de quadcopters viables para fines comerciales, militares , e incluso aficionados .
>
> Quadcopter de control es un problema fundamentalmente dif�cil e interesante :
>
> Con * los seis grados de libertad * (tres de traslaci�n y tres de rotaci�n ) y s�lo * cuatro entradas independientes * (velocidades de rotor ) , quadcopters est�n severamente subactuado ** . **
Con el fin de lograr seis grados de libertad , un movimiento de rotaci�n y de traslaci�n est�n acoplados . Las din�micas resultantes son altamente no lineales , sobre todo despu�s de considerar los efectos aerodin�micos complicados. Por otra parte , a diferencia de los veh�culos de tierra , los helic�pteros tienen muy poca fricci�n para evitar su movimiento , por lo que deben proporcionar su propio amortiguaci�n con el fin de dejar de moverse y se mantienen estables.
>
> En conjunto, estos factores crean un problema de control muy interesante.

Hay muchos art�culos , ponencias y tesis que discuten el modelo din�mico del quadcopter pero nos gusta personalmente [ Dise�o, implementaci�n y � � , ight prueba de la navegaci�n interior y sistema de control para un UAV quadrotor ] ( http://www.st . ewi.tudelft.nl / ~ koen/in4073/Resources/MSc_thesis_X-UFO.pdf ) .

Fuentes
-----
- [ Dise�o, implementaci�n y � � , ight prueba de la navegaci�n interior y sistema de control para un UAV quadrotor ] ( http://www.st.ewi.tudelft.nl/ ~ koen/in4073/Resources/MSc_thesis_X-UFO.pdf )
- [ Quadcopter Din�mica , Simulaci�n y Control](http://andrew.gibiansky.com/downloads/pdf/Quadcopter%20Dynamics,%20Simulation,%20and%20Control.pdf)
- [ Quadcopter ] ( http://en.wikipedia.org/wiki/Quadcopter )



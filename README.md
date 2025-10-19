# Calculadora

### Comentarios:

- Mi plan inicial era hacer la barra del resultado y de ahi colgar el primer numero, pero no se que View es, asumo que es un textView pero no se que ponerle dentro
- Me pareció un poco raro crear las strings como "uno" valor 1, ya que es algo fíjo
- Para los numeros decidí colgarlos por filas, el 1 es con respecto a la pantalla, el 4 respecto al 1 dejando 8px por arriba, y el 7 del 4. Los demas son respecto a su primer numero en la fila
- Para el Style lo cambie a uno que no tenia bordes redondeados
- Intente cambiar los colores pero no me funcionaba, como no es el objetivo de la practica he separado los + - etc, con 24 horizontalmente en vez de con 8

### Captura ejecución

![Captura de la ejecucion](/doc/CapturaVistas.PNG)

En esta captura se ve a la izquierda del todo la vista diseño donde he creado todo, y en la derecha del todo la ejecución, he resaltado con azul un espacio en blanco que no se corresponde con el diseño

Esto se tiene que deber a la relacion de altura, para que se viese bien tendria que colocarlo abajo

***Arreglado:***

En vez de poner que el 1 se vinculase con la parte superior, hize que la parte inferior de 1 se vinculase con la parte inferior de la pantalla, y como lo demas lo sigue se ve bien

![Captura de la ejecucion](/doc/CapturaVistas2.PNG)

Otro problema a la hora de hacer el git, es que no se porque se inicializó mal o algo, todo lo hize desde android estudio asique no se lo que pasó.

### Codigo XML

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity" >

    <Button
        android:id="@+id/button1"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginStart="16dp"
        android:layout_marginBottom="280dp"
        android:text="@string/uno"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/button2"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginStart="8dp"
        android:text="@string/dos"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button1"
        app:layout_constraintTop_toTopOf="@+id/button1"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/button3"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginStart="8dp"
        android:text="@string/tres"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button2"
        app:layout_constraintTop_toTopOf="@+id/button1"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/button4"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginTop="8dp"
        android:text="@string/cuatro"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toStartOf="@+id/button1"
        app:layout_constraintTop_toBottomOf="@+id/button1"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/button5"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginStart="8dp"
        android:text="@string/cinco"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button4"
        app:layout_constraintTop_toTopOf="@+id/button4"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/button6"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginStart="8dp"
        android:text="@string/seis"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button5"
        app:layout_constraintTop_toTopOf="@+id/button4"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/button7"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginTop="8dp"
        android:text="@string/siete"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toStartOf="@+id/button4"
        app:layout_constraintTop_toBottomOf="@+id/button4"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/button8"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginStart="8dp"
        android:text="@string/ocho"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button7"
        app:layout_constraintTop_toTopOf="@+id/button7"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/button9"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginStart="8dp"
        android:text="@string/nueve"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button8"
        app:layout_constraintTop_toTopOf="@+id/button7"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/buttonDecimal"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginTop="8dp"
        android:text="@string/decimal"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toStartOf="@+id/button7"
        app:layout_constraintTop_toBottomOf="@+id/button7"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/button0"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginStart="8dp"
        android:text="@string/cero"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/buttonDecimal"
        app:layout_constraintTop_toTopOf="@+id/buttonDecimal"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/buttonIgual"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="77dp"
        android:layout_height="58dp"
        android:layout_marginTop="8dp"
        android:text="@string/igual"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toStartOf="@+id/button9"
        app:layout_constraintTop_toBottomOf="@+id/button0"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/buttonMas"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="104dp"
        android:layout_height="56dp"
        android:layout_marginStart="24dp"
        android:text="@string/mas"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button3"
        app:layout_constraintTop_toTopOf="@+id/button1"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/buttonMenos"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="104dp"
        android:layout_height="56dp"
        android:layout_marginStart="24dp"
        android:text="@string/menos"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button3"
        app:layout_constraintTop_toTopOf="@+id/button4"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/buttonMultiplicar"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="104dp"
        android:layout_height="56dp"
        android:layout_marginStart="24dp"
        android:text="@string/multiplicar"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button3"
        app:layout_constraintTop_toTopOf="@+id/button7"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/buttonDividir"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="104dp"
        android:layout_height="56dp"
        android:layout_marginStart="24dp"
        android:text="@string/dividir"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button3"
        app:layout_constraintTop_toTopOf="@+id/buttonDecimal"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <Button
        android:id="@+id/buttonLimpiar"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="104dp"
        android:layout_height="56dp"
        android:layout_marginStart="24dp"
        android:text="@string/limpiar"
        app:iconTint="@color/material_dynamic_neutral30"
        app:layout_constraintStart_toEndOf="@+id/button3"
        app:layout_constraintTop_toTopOf="@+id/buttonIgual"
        app:rippleColor="@color/material_dynamic_neutral20" />

    <EditText
        android:id="@+id/escribir"
        android:layout_width="371dp"
        android:layout_height="48dp"
        android:layout_marginBottom="28dp"
        android:ems="10"
        android:inputType="text"
        app:layout_constraintBottom_toTopOf="@+id/button1"
        app:layout_constraintEnd_toEndOf="@+id/buttonMas"
        app:layout_constraintHorizontal_bias="1.0"
        app:layout_constraintStart_toStartOf="@+id/button1" />

</androidx.constraintlayout.widget.ConstraintLayout>

```
# COUNTING-APP-
package com.example.countingapp;

import androidx.appcompat.app.AppCompatActivity;

import android.media.MediaPlayer;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {


    MediaPlayer mediaPlayer;
    public void onLanguageclick(View view){
        Button buttonclicked = (Button)view;
        mediaPlayer = MediaPlayer.create(this,getResources().getIdentifier(buttonclicked.getTag().toString(),"raw",getPackageName()));
        mediaPlayer.start();
    }
    public  void onStopClick(View view){

            mediaPlayer.stop();

    }

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
}

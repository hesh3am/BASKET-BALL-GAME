package com.example.android.courtcounter;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    int number ;
    int number2;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

    @Override
    protected void onResume() {
        super.onResume();
    }

    /**
     * Displays the given score for Team A.
     */
    public void displayForTeamA(int score) {
        TextView scoreView = (TextView) findViewById(R.id.team_a_score);
        scoreView.setText(String.valueOf(score));
    }

    public void Points3(View view) {
        number = number + 3;
        displayForTeamA(number);
    }

    public void Points2(View view) {
        number = number + 2;
        displayForTeamA(number);
    }

    public void Freethrow(View view) {
        number = number + 1;

        displayForTeamA(number);
    }

    /////////////////////////////////////////////////////// team B
    public void displayForTeamB(int score) {
        TextView scoreView = (TextView) findViewById(R.id.team_b_score);
        scoreView.setText(String.valueOf(score));
    }

    public void Points3B(View view) {
        number2 = number2 + 3;
        displayForTeamB(number2);
    }

    public void Points2B(View view) {
        number2 = number2 + 2;
        displayForTeamB(number2);
    }

    public void FreethrowB(View view) {
        number2 = number2 + 1;
        displayForTeamB(number2);
    }

    ///////////////////////////////////////////////// Reset
    public void resetZero() {
        number = 0;
        number2 = 0;
    }

    public void Reset(View view) {
        resetZero();
        displayForTeamB(number2);
        displayForTeamA(number);
    }
}

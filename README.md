# Interfaz_Deber3-

package Deber3;

import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.geometry.Pos;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.ColorPicker;
import javafx.scene.control.DatePicker;
import javafx.scene.control.Label;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class InterfzaGUI extends Application {

    @Override
    public void start(Stage primaryStage) {
        Label fechaLabel = new Label("Selecciona una fecha:");
        DatePicker fechaPicker = new DatePicker();
        Label colorLabel = new Label("Selecciona un color:");
        ColorPicker colorPicker = new ColorPicker();
        Button botonConfirmar = new Button("Confirmar");
        Label resultadoLabel = new Label("Resultado:");

        VBox root = new VBox(10);
        root.setPadding(new Insets(10));
        root.setAlignment(Pos.CENTER);

        root.getChildren().addAll(fechaLabel, fechaPicker, colorLabel, colorPicker, botonConfirmar, resultadoLabel);

        botonConfirmar.setOnAction(e -> {
            String fechaSeleccionada = fechaPicker.getValue().toString();
            String colorSeleccionado = colorPicker.getValue().toString();
            resultadoLabel.setText("Fecha seleccionada: " + fechaSeleccionada + "\nColor seleccionado: " + colorSeleccionado);
            System.out.println("Fecha seleccionada: " + fechaSeleccionada + ", Color seleccionado: " + colorSeleccionado);
        });

        Scene scene = new Scene(root, 300, 250);
        primaryStage.setTitle("Fecha y Color GUI");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args); 
    }
}

![imagen](https://github.com/CristopherJimenezt/Interfaz_Deber3-/assets/169114304/4d0bc2a2-5fe8-4e03-9892-482c83278f92)

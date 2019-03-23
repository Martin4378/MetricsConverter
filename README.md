# MetricsConverter

import java.util.Scanner;

public class P24_MetricsConverter {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        double imputMetricNumber = Double.parseDouble(scanner.nextLine());

        String imputMetric = scanner.nextLine();
        String outputMetric = scanner.nextLine();

        double convertedToMeter = 0;
        double convertedtoOutputMeter = 0;

        if ("m".equalsIgnoreCase(imputMetric)) {
            convertedToMeter = imputMetricNumber;
        } else if ("mm".equalsIgnoreCase(imputMetric)) {
            convertedToMeter = imputMetricNumber / 1000;
        } else if ("cm".equalsIgnoreCase(imputMetric)) {
            convertedToMeter = imputMetricNumber / 100;
        } else if ("mi".equalsIgnoreCase(imputMetric)) {
            convertedToMeter = imputMetricNumber / 0.000621371192;
        } else if ("in".equalsIgnoreCase(imputMetric)) {
            convertedToMeter = imputMetricNumber / 39.3700787;
        } else if ("km".equalsIgnoreCase(imputMetric)) {
            convertedToMeter = imputMetricNumber * 1000;
        } else if ("ft".equalsIgnoreCase(imputMetric)) {
            convertedToMeter = imputMetricNumber / 3.2808399;
        } else if ("yd".equalsIgnoreCase(imputMetric)) {
            convertedToMeter = imputMetricNumber / 1.0936133;
        }

        if ("m".equalsIgnoreCase(outputMetric)) {
            convertedtoOutputMeter = convertedToMeter;
        } else if ("mm".equalsIgnoreCase(outputMetric)) {
            convertedtoOutputMeter = convertedToMeter * 1000;
        } else if ("cm".equalsIgnoreCase(outputMetric)) {
            convertedtoOutputMeter = convertedToMeter * 100;
        } else if ("mi".equalsIgnoreCase(outputMetric)) {
            convertedtoOutputMeter = convertedToMeter * 0.000621371192;
        } else if ("in".equalsIgnoreCase(outputMetric)) {
            convertedtoOutputMeter = convertedToMeter * 39.3700787;
        } else if ("km".equalsIgnoreCase(outputMetric)) {
            convertedtoOutputMeter = convertedToMeter / 1000;
        } else if ("ft".equalsIgnoreCase(outputMetric)) {
            convertedtoOutputMeter = convertedToMeter * 3.2808399;
        } else if ("yd".equalsIgnoreCase(outputMetric)) {
            convertedtoOutputMeter = convertedToMeter * 1.0936133;
        }
        System.out.printf("%.8f", convertedtoOutputMeter);

    }

}

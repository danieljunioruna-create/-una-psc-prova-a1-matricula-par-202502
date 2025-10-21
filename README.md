public class ArattaiGrowthTracker {
    public static void main(String[] args) {
    //Aqui sao os DOWNLOADOS DO DIA 
        int[] downloadsDiarios = {850000, 1050000, 1100000, 950000, 1200000, 1000000, 850000};
        String[] diasDaSemana = {"Dom", "Seg", "Ter", "Qua", "Qui", "Sex", "Sáb"};
//aqui em cima sao os DIAS DA SEMANA 
        
        int totalDownloads = 0;
        for (int downloads : downloadsDiarios) {
            totalDownloads += downloads;
        }// aqui mostra o TOTAL DE DOWNLOADS 
        System.out.printf("Total de Downloads na Semana: %,d%n", totalDownloads);


        int pico = downloadsDiarios[0];
        int minimo = downloadsDiarios[0];
        String diaPico = diasDaSemana[0];
        String diaMinimo = diasDaSemana[0];

        for (int i = 1; i < downloadsDiarios.length; i++) {
            if (downloadsDiarios[i] > pico) {
                pico = downloadsDiarios[i];
                diaPico = diasDaSemana[i];
            }
            if (downloadsDiarios[i] < minimo) {
                minimo = downloadsDiarios[i];
                diaMinimo = diasDaSemana[i];
            }
        }

        //Aqui vai mostra o dia com mais downloads
        System.out.printf("Dia com maior número de downloads: %s (%,d downloads)%n", diaPico, pico);
        System.out.printf("Dia com menor número de downloads: %s (%,d downloads)%n", diaMinimo, minimo);
    }
}

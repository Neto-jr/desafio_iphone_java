# desafio_iphone_java
public class iPhone {
    private String modelo;
    private int capacidade; // em GB
    private int bateria; // em porcentagem
    // Construtor
    public iPhone(String modelo, int capacidade, int bateria) {
        this.modelo = modelo;
        this.capacidade = capacidade;
        this.bateria = bateria;
    }
    // Método para tocar música
    public void tocarMusica(String musica) {
        if (bateria > 0) {
            System.out.println("Tocando música: " + musica);
            bateria -= 3; // Reduz bateria ao tocar música
        } else {
            System.out.println("Bateria baixa. Carregue o iPhone.");
        }
    }
    // Método para fazer uma chamada
    public void fazerChamada(String numero) {
        if (bateria > 0) {
            System.out.println("Ligando para: " + numero);
            bateria -= 4; // Reduz bateria ao fazer chamada
        } else {
            System.out.println("Bateria baixa. Carregue o iPhone.");
        }
    }
    // Método para navegar na internet
    public void navegarInternet(String url) {
        if (bateria > 0) {
            System.out.println("Navegando para: " + url);
            bateria -= 5; // Reduz bateria ao navegar
        } else {
            System.out.println("Bateria baixa. Carregue o iPhone.");
        }
    }
    // Getters e Setters (opcionais)
    public String getModelo() {
        return modelo;
    }

    public void setModelo(String modelo) {
        this.modelo = modelo;
    }

    public int getCapacidade() {
        return capacidade;
    }

    public void setCapacidade(int capacidade) {
        this.capacidade = capacidade;
    }
    public int getBateria() {
        return bateria;
    }
    public void carregarBateria(int carga) {
        this.bateria += carga;
        if (bateria > 100) {
            bateria = 100; // Limitar a bateria a 100%
        }
    }
    public static void main(String[] args) {
        iPhone meuIphone = new iPhone("iPhone 14", 128, 50);
        meuIphone.tocarMusica("Shape of You");
        meuIphone.fazerChamada("123-456-789");
        meuIphone.navegarInternet("www.exemplo.com");
    }
}

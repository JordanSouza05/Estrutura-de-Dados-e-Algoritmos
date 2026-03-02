public class Vetor {

    private String[] elementos;
    private int tamanho;

    public Vetor(int capacidade) {
        this.elementos = new String[capacidade];
        this.tamanho = 0;
    }

    public boolean estaVazia() {
        return tamanho == 0;
    }

    public String ultimo() {
        if (estaVazia()) {
            throw new IllegalStateException("O vetor está vazio.");
        }
        return elementos[tamanho - 1];
    }

    public void imprimeUmPorLinha() {
        for (int i = 0; i < tamanho; i++) {
            System.out.println(elementos[i]);
        }
    }

    public boolean contem(String elemento) {
        for (int i = 0; i < tamanho; i++) {
            if (elementos[i].equals(elemento)) {
                return true;
            }
        }
        return false;
    }
}

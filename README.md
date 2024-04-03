<?php
class Filme {
    private $titulo;
    private $duracao;

    public function __construct($titulo, $duracao) {
        $this->titulo = $titulo;
        $this->duracao = $duracao;
    }

    public function getTitulo() {
        return $this->titulo;
    }

    public function getDuracao() {
        return $this->duracao;
    }
}

class Sala {
    private $numero;
    private $capacidade;

    public function __construct($numero, $capacidade) {
        $this->numero = $numero;
        $this->capacidade = $capacidade;
    }

    public function getNumero() {
        return $this->numero;
    }

    public function getCapacidade() {
        return $this->capacidade;
    }
}

class Ingresso {
    private $filme;
    private $sala;
    private $preco;

    public function __construct($filme, $sala, $preco) {
        $this->filme = $filme;
        $this->sala = $sala;
        $this->preco = $preco;
    }

    public function getFilme() {
        return $this->filme;
    }

    public function getSala() {
        return $this->sala;
    }

    public function getPreco() {
        return $this->preco;
    }
}

class Cliente {
    private $nome;
    private $idade;

    public function __construct($nome, $idade) {
        $this->nome = $nome;
        $this->idade = $idade;
    }

    public function getNome() {
        return $this->nome;
    }

    public function getIdade() {
        return $this->idade;
    }
}

$filme = new Filme("Barbie", 150);
$sala = new Sala(1, 100);
$ingresso = new Ingresso($filme, $sala, 38);
$cliente = new Cliente("João", 20);

echo "Informações do ingresso:\n";
echo "Filme: " . $ingresso->getFilme()->getTitulo() . "\n";
echo "Sala: " . $ingresso->getSala()->getNumero() . "\n";
echo "Preço: R$" . $ingresso->getPreco() . "\n";
echo "\n";
echo "Informações do cliente:\n";
echo "Nome: " . $cliente->getNome() . "\n";
echo "Idade: " . $cliente->getIdade() . "\n";

?>

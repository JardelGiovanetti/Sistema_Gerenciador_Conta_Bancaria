# Sistema_Gerenciador_Conta_Bancaria
package banco;

public class Principal {

	public static void main(String[] args) {
		
		Endereco end1 = new Endereco("Monteiro Lobato", 777, "PG", "PR");
		
		ClienteCpf titularCpf1 = new ClienteCpf("Joao das Couves", "42 998122-6532", end1, 123399, "2387444");
		
		Cartao cartao1 = new Cartao(45674234, 0);
		
		ContaCorrente conta1 = new ContaCorrente(45453, 34234, 555, titularCpf1, cartao1);		
		//public ContaCorrente(int numAgencia, int numConta, int senha, Cliente titularConta, Cartao cartao) {
		
		
		conta1.realizarDeposito(200);
		conta1.realizarSaque (5, 555);
		conta1.realizarPagamento(555, 34234, 45453, 10);
		conta1.solicitarCartao(555, 34234, 45453);
		conta1.realizarTransferencia(555, 34234, 45453, 333, 562432, 20);
		conta1.verificarExtrato(555, 34234, 45453, 123399, 0);
		conta1.cancelarCartao(555, 34234, 45453);
		
		
	}
}


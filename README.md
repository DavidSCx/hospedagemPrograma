
public abstract class Hospedagem {
	protected String nome;
	protected int quartos ;
	protected int quartosOcupados;
	protected int leitos;
	protected int leitosOcupados;
	
	public String getNome() {
		return nome;
	}
	public int getQuartos() {
		return quartos;
	}
	public int getQuartosOcupados() {
		return quartosOcupados;
	}
	public int getLeitos() {
		return leitos;
	}
	public int getLeitosOcupados() {
		return leitosOcupados;
	}
	public Hospedagem (String nome, int quartos, int leitos) {
		this.nome=nome;
		this.quartos=quartos;
		this.leitos=leitos;
	}
	
	
	public void checkIn (int leitos) {
		int leitosMaximo = 0;
		if (leitosMaximo<=200) 
	System.out.println ("Check in não Efetuado");
		else
			this.quartosOcupados=this.quartosOcupados+1;
		this.leitosOcupados=this.leitosOcupados+leitos;
			System.out.println ("Check in Efetuado Com Sucesso");
	}
		
	
	public void checkOut (int leitos) {
		int leitosMaximo = 0;
			if (leitosMaximo>=200) 
				System.out.println ("Check Out não Efetuado");
			
			else
			this.quartosOcupados=this.quartosOcupados-1;
			this.leitosOcupados=this.leitosOcupados-leitos;
				System.out.println ("Check Out Efetuado Com Sucesso");
				
			
		}
	public abstract double taxaOcupacao();
	
 
}

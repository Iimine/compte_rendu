# compte_rendu



public class Compte {
	private int numero;
	private double solde;
	private static final int nbmax=1000;
	public int nbcompteconstruit=0;
	public Compte() {
		numero=0;
		solde=0.0;
		nbcompteconstruit++;
		
		}
	public Compte(int numero,double solde) {
		this.numero=numero;
		this.solde=soldpuble;
		nbcompteconstruit++;}
	solde=0.0
	public void depot( double valeur) {
		this.solde = solde+ valeur ;
	
	}
	public void retrait ( double valeur) {
		if ( valeur>0 && valeur<=solde) {
			this.solde=solde-valeur;}
		else {
			Systeme.out.println("solde insuffissant";)
		}
		public double getSolde() {
			return solde;}
		public void affiche() {
			Systeme.out.println("le solde est"+solde);
		}
		public void  setSolde(double s) {
			if (s>0) {
				solde=s;
			}
			else {
				Syteme.out.println("doit etre positive");
			}
			}
		public String toSting() {
			return "les solde est"+solde+"le numero"+numero;
		}
		public void virer(float valeur,Compte destinataire) 
		{
			if (valeur>0 && valeur<=solde) {
				
		     	retrait(valeur);
		    	destinataire.depot(valeur);
			    Systeme.out.println("virement de"+valeur+"du compte"+numero+"vers lz comptes"+destinataire.numero);
			}
			else {
				Systeme.out.println("insufisante");
		}			
		public static Compte plusSolde(Comptec1,Comptec2) {
			if (c1.solde>c2.solde) {
				return c1.numero+c1.solde;
			}
			else  {
				return c2.numero+c2.solde;}
			public boolean equals (objet o) {
				if (this==o) return true;
				if (o==null)|| getClass()!=o.getClass()) return false;
				Compte compte=(compte) o;
				return numero==compte.numero;
				//le solde auusi
						
			}
		}
		
			}
				
			
		}
  //client

  
  public class Client {
	private Compte[] comptes;
	private String nom;
	private int nbcompte;
	public Client (String nom,int nbmax) {
		this.nom=nom;
		comptes=new Compte[nbmax];
		nbcompte=0;
		public void ajouterCompte(Compte nouveauCompte) { 
			if (nbComptes < comptes.length) {
				this.comptes[nbComptes++] = nouveauCompte; } 
			else { System.out.println("Le nombre maximum de comptes est atteint pour ce client."); }
		}
		
	}
	public double getSolde() 
	{ double soldeTotal = 0; 
	for (int i = 0; i < nbComptes; i++) { 
		soldeTotal += comptes[i].getSolde(); } return soldeTotal; }
	public String getNom() { 
		return this.nom; }
	public void afficherSolde() {
		System.out.println("Solde total du client " + this.nom + ": " + this.getSolde()); }
	public boolean equals(Object o) { 
		if (this == o) 
			return true; 
		if (o == null || getClass() != o.getClass())
			return false; Client client = (Client) o; 
			return nom.equals(client.nom); } 
	public String toString() { return "Client{" + "nom='" + nom + '\'' + ", nbComptes=" + nbComptes + '}'; } } 
	
}
 //banque
 public class Banque {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Compte compte1 = new Compte(128,1000); 
		Compte compte2 = new Compte(125,500);
		Client client1 = new Client("Alice", 2); 
		client1.ajouterCompte(compte1); 
		client1.ajouterCompte(compte2); Compte compte3 = new Compte(2000); 
		Compte compte4 = new Compte(1500);
		Client client2 = new Client("Bob", 2); 
		client2.ajouterCompte(compte3);
		qclient2.ajouterCompte(compte4); // Test des méthodes compte1.afficherSolde(); compte2.depot(200); compte2.afficherSolde(); client1.afficherSolde(); client2.afficherSolde(); } }
		

	}

}

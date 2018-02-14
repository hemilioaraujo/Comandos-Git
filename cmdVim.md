### Comandos Editor vim absorvidos dos vídeos do canal LinuxTips

[Canal LinuxTips](https://www.youtube.com/channel/UCJnKVGmXRXrH49Tvrx5X0Sw)

Abrir aqruivos:

	vim nomeDoArquivo.extensão


### Comandos:

Inserir Dados:

	i			Entra em modo de Inserção(edição);

	I			Modo Inserção no início da linha;

	Esc			Sai do modo Inserção;

	a			Modo Inserção um caracter a frente do cursor;

	A			Modo Inserção no fim da linha;

	o			Modo Inserção na linha de baixo;

	O			Modo Inserção na linha de cima;

	S			Modo Inserção apagando linha do cursor;

Editar Dados:

	yy			Copia toda a linha;
                                  
	Xyy			Copia X linhas;

	yw			Copia uma palavra;

	Xyw			Copia X palavras;
                                  
	dd			Recortar;
                                  
	Xdd			Recorta X linhas;
                                  
	p			Cola;
                                  
	v			Modo Visual para selecionar partes do texto
		 		e não somente linhas;

	Ctrl + v		Seleção em bloco(Seleção vertical);
	
	x			Del;

	X			BackSpace;


Salvar Arquivo:

	:w			Salva arquivo;

	:w novoNome		Salvar como(cria um novo arquivo com o nome
				definido);

	:wq			Salva e sai do arquivo;

	:x			Faz o mesmo que o anterior;

	ZZ			Faz o mesmo que os anteriores;

	:q!			Sair sem salvar;


Ferramentas:

	:split nomeDoArquivo			Divide a tela em duas com os arquivos abertos
						um em cada tela;

	Ctrl + ww				Alt + Tab (Alterna entre as páginas editores);
	
	:r nomeDoArquivo			traz todo o texto do arquivo selecionado para
						o arquivo aberto;
	
	/palavra				Pesquisa de cima para baixo pela palavra desejada
						por todo arquivo.
						Para ir alternando entre as repetições da palavra,
						é só apertar n;
	
	?palavra				Pesquisa de baixo para cima pela palavra desejada;

	:x,y/antiga/nova/			Substitui a palavra antiga que estiver dentre as
						linhas x e y pela palavra nova;

	:%s/antiga/nova/			Substitui todas as palavras antigas pela nova;

	:%s/antiga/nova/g			Substitui todas as palavras antigas pela nova.
						Substitui apenas uma por linha se hoverem duas;
	
	:syntax on/off				Liga ou desliga reconhecimento da syntax da 
						linguagem. Arquivo precisa ter a extensão;

	:set number				Exibe número de linhas do arquivo;

	:set nonu				Oculta número de linhas do arquivo;

	:ab abreviação oQueSeráAbreviado	gera a abreviação de um texto longo que desejar;

	:set ai					Habilita auto identação;

	:set noai				Desabilita auto identação;
	
	:set visualbell				Desabilita sinal sonoro e deixa visual;

	:set ic					Ignora case sensitive na pesquisa de palavras;

	:set noic				Desabilita o ignore case;

	:set bg=dark				Altera o background para dark;

	:set bg=light				Altera o background para light;

	:set tabstop=x				Define o tamanho do TAB;

	batata
	goiaba
	manga
	amora
	genipapo




[Ponto de parada](https://www.youtube.com/watch?v=_qShvkx8jK0)








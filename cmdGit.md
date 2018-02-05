### Material retirado com base no curso Git e Github para iniciantes(Willian Justen de Vasconcellos)

Link para o curso no portal Udemy:
	https://www.udemy.com/git-e-github-para-iniciantes

	
	
Download Git:
	https://git-scm.com/
	
	
	
Configurando Git:
	
	Username
		git config --global user.name "HLAM"

	email
		git config --global user.email "hemilioaraujo@gmail.com"
	
	editor padrão(se não configurado ele utiliza vim)
		git config --global core.editor (emacs,vim)
	
	exibir configurações utilizadas
		git config chave		chave = user.name, user.email, core.editor	
		git config --list		exibe todas as configurações

		
		
Gerenciar Pastas:
		
	Criar Pasta Repositório Local:
		mkdir nomeDaPasta
	
	Deslocamento Entre Diretórios(cd ou dir):
		
		cd nomeDaPasta		entra no diretório;
			
		cd			retorna para diretório raiz;
		
		cd ..			retorna para diretório anterior;
		
	Obs.: diretório .git contém todos os dados sobre o repositório;

	
	
Status Dos Arquivos No Repositório:

	untracked		arquivo recém adicionado no repositório mas o 
				git ainda não conhece nenhuma versão deste arquivo;
	
	unmodified		arquivo recém adicionado no git porém nunca modificado;

	modified		arquivo já modificado anteriormente;
	
	staged			momento em que é criada a versão do arquivo(commit).
				Quando é realizado o commit, o arquivo volta para o modo de unmodified;

					

Comandos Git:


	git init				Inicializar Repositório(monitorar alterações do diretório);	
		
	ls -la				  	exibe diretórios;

	ls 					exibe arquivos;

	git status				exibe o status do repositório(em qual branch(diretório),
						se existe algum commit pendente);
	
	git add nomeDoArquivo			adiciona o arquivo ao repositório;
	
	git rm nomeDoArquivo			deleta o arquivo do repositório;

	git rm -f nomeDoArquivo			deleta o arquivo do repositório(force);
	
	git commit -m "comentário"		confirma todas alterações e commita(arquivo recém criado);
	
	git commit -am "comentário"		confirma todas alterações e commita(arquivo já existente);
	
	clear					limpa prompt;

	
Log's:	
	
	git log					exibe todos os commits;
	
	git log --author="Joaquim"		somente commits do autor Joaquim;
	
	git log --since=2.weeks			somente commits das ultimas 2 semanas;
	
	git log -n				exibe os ultimos n commits;
	
	git shortlog				exibe um resumo dos commits;
	
	git shortlog -sn			exibe somente os nomes de usuário e quantos commits eles realizaram;
	
	git show hash				exibe alterações realizadas no commit;

	
Diferênças Entre Aruivo Unmodified e Modified:
	
	git diff				exibe diferenças entre original e o arquivo a ser commitado;
	
	git diff --name-only			exibe apenas o nome dos arquivos alterados;

	
Reset Commit:
	
	git checkout nomeDoArquivo		retorna o arquivo modified para unmodified(not staged);
	
	git reset HEAD hash			retira arquivo editado do staged(para ser realmente excluído,
						executa o checkout após o reset);
	
	git reset --soft hash			desfaz o commit e fica a ponto de commitar novamente (staged);
	
	git reset --mixed hash			desfaz o commit e volta para modified;
	
	git reset --hard hash			acaba com toda edição feita pelo commit e retorna para o commit anterior;
	
	

	
Repositório remoto (GitHub):

	git remote add origin https://github.com/hemilioaraujo/cmdGit.git	este comando adiciona um repositório remoto, 
										com o nome origin(pode ser qualquer nome);
	
	git remote								exibe repositório remoto;
	
	git remote -v								exibe repositório remoto e seu endereço;
	
	git push -u origin master						copia todos os dados e arquivos master(origem) 
										para o origin(destino).
										O comando -u faz um track, e das próximas vezes,
										só é nescessário o git push;

	git clone git@github.com:hemilioaraujo/cmdGit.git nomePasta		clona repositório do endereço remoto(quando o repositório é pessoal)
										quando não se é pessoal é necessário realizar um fork 
										do repositório para um repositório pessoal;
	
Gerenciando Chaves SSH:

	ls -la ~/.ssh								verifica existência de chaves no repositório(id_rsa, id_rsa.pub);

	cat id_rsa.pub // more id_rsa.pub // vim id_rsa.pub			exibe a chave SSH(tem de ser executado no diretório "~/.ssh");

	ssh-keygen -t rsa -b 4096 -C "your_email@example.com" -> enter 2x	gera a chave SSH no repositório local;


Adicionando Chave SSH GitHub:

	Copia a chave com o comando cat no diretório "~/.ssh" e acessa https://github.com/settings/keys -> new SSH key -> da um nome e cola a chave;

Branch's(Snapshot):

	git checkout -b nomeBranch		Cria um novo branch com o nome que quiser;

	git branch				Exibe os branchs existentes(O * indica posição atual);

	git checkout nomeBranchExistente	Alterna entre os branchs;

	git branch -D nomeBranch		Deleta branch selecionado;
	

Rebase e Merge
	
	git merge nomeDoBranch			Realiza o merge dos branches atual e o que é dado o nome.
						O merge gera um commit extra para a junção.


	Obs.: 	É sempre rebase para sincronizar o código do Branch com o master(qusndo não é interessante ter o commit desta sincronização ou junção)
	      	e merge quando for incluir um código de um branch separado (feature) no master e gerar um commit.


.gitignore:

	O arquivo .gitignore é usado quando você tem arquivos que são necessários no repositório mas você não quer que eles subam para o repositório
	online(track).
	
	Obs.: Dentro do arquivo podem ser adicionados os nomes dos arquivos a não serem trackeados ou até mesmo o tipo de extenção 
	que não deve ser trackeada.

	vim .gitignore				gera o arquivo gitignore;

	*.json					(* = tudo) tudo que for .json não é trackeado;

	exemplo.xls				O arquivo exemplo.xls não é trackeado;
	

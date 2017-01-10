# Quicknotes

1- todo repositório clonado é automáticamente um branch
2 - tb é local
logo as operações comuns são bem mais rápidas já q não precisam do servidor pra acontecer
3 - branches, branches everywhere
4 - peer-to-peer - Já q é distribuído vc pode ter remotes que apontam pra outra maquina, no caso de vc estar trabalhando em um branch com outro amiguinho, logo vc não precisa jogar td pro servidor
5 - tamanho - como acabei de ver aqui um clone de um repo do git tem metade do tamanho de um working copy do svn
6 - estrutura do repositório - git é um grapho e o svn é uma árvore unidimensional - no caso do grapho vc pode ter ramificações que podem voltar para o ramo principal ou não e vc consegue traçar o caminho das modificações
6 - cont. - no caso da árvore do svn vc pode até ter ramificações, mas pra traçar o caminho das modificações é um trabalho monstro
(desculpa, acabei usando vc pra fazer meu brainstorm aqui XD)
7 - o git é gordo e guarda os snapshots dos arquivos inteiros para cada commit
eu não sei pq (provavelmente mt eu sou um acumulador digital) mas eu acho isso bem mais interessante e até seguro doq guardar só um delta da modificação
já tive vários problemas de merge por causa desse mecanismo do svn
mt embora ele até se ache bem no merge ele já teve umas cãimbras meio locas e zoou o arquivo todo
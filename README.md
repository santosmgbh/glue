# GIT
PUSH:
-- cria copia da master local em uma nova branch local chamada working (pular este passo se a branch local de trabalho já estiver criada e selecionada)
git checkout -b working 
-- primeiro comita na working
git commit -am "mensagem"(comita local na working)
-- sincronizar sua master local com a master remota
git checkout master(troca pra branch local master)
git pull origin master(pull para atualizar a sua master local)
-- jogar alterações da master local na working
git rebase master working(isso faz voltar pra working)
-- faz o merge da sua master local com a sua working local
git checkout master(voltando pra master)
git merge working
-- faz o push a sua master local pra master remota
git push origin master
git checkout working

PULL:

git checkout master(seleciona branch master local)
git pull origin master(pega alterações da master remota e joga na master local)
git rebase master working(pega alterações da master local e joga na working)


## STASH
  O código vai para uma pilha local e permite mudar de branch.
  depois com o git stash pop ele vai colocar o código na branch atual.

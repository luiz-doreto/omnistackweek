# omnistackweek

Como trabalhar com repositórios subtrees.

- Criar todos os repositorios separados (raiz e filhos);
- Clona o repo raiz e acessa a pasta;
- Cria remotes dos filhos:
    - ```git remote add omnistackweek-backend https://github.com/luiz-doreto/omnistackweek-backend.git```
- adiciona os filhos ao projeto:
    - ```git subtree add --prefix=backend/ omnistackweek-backend master```

Todos os commits e alterações ficarão no repositório raiz. Caso quiser mandar as alterações para os repositórios filhos é só fazer um push:

- ```git subtree push --prefix=backend/ omnistackweek-backend master```

Ou caso alguma alteração foi feita diretamente no filho e quer mandar essa alteração para o repositório raiz tbm, é só dar um pull:

- ```git subtree pull --prefix=backend/ omnistackweek-backend master```
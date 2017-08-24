<p align="center">
  <img src="https://git-scm.com/images/logo@2x.png" width="100" heigh="50"/>
</p>

# Tutorial Git

### O que é Git?
Git é um sistema de controle de versão de arquivos. Através deles podemos desenvolver projetos na qual diversas pessoas podem contribuir simultaneamente no mesmo, editando e criando novos arquivos e permitindo que os mesmos possam existir sem o risco de suas alterações serem sobrescritas.

### O que é Repositório?
É o local onde seu projeto estará armazenado, existem alguns repositórios online gratuitos e os mais conhecidos são: GitHub, GitLab, BitBucket, os dois últimos permitem ter projetos privados gratuitamente.

### O que são Issues?
São uma espécie de solicitação. As issues são utilizadas normalmente, para relatar algum problema ou sugerir uma nova funcionalidade ao projeto.

##### Por que utilizar as issues?
Para facilitar o trabalho, registrar a demanda de trabalho e gerar um histórico de tudo o que foi feito.

#### Trabalhando com Issues
Acesse o seu repositório online e procure a área de Issues e abra uma nova issue, será gerado um número automaticamente com # na frente
exemplo: #1 ou #666.
Após crie uma branch em seu repositório local com o mesmo número da issue aberta, e ao fazer o commit, mencione a issue no comentário para linka-lo a issue especifica.
exemplo:
```bash
$ git commit -m "[#numerodaissue]Descrição do commit"
```

### O que são Branches?
Branches são como os "ramos" de uma árvore e a branch master é como se fosse o tronco, as branches são uma cópia do ramo principal onde você poderá fazer suas alterações sem interferir diretamente na MASTER.

##### Por que usar branches?
Porque, o servidor pode estar linkado para realizar o deploy automáticamente sempre que houver alguma alteração na master e caso seja enviando algum código incompleto por exemplo, o projeto que está na web ficará com errors.

##### Trabalhando com branches
Antes de criar uma nova branch, você deve observar se o projeto local está na branch master, caso o contrário será criado branch dentro de outra branch.
Para criar uma branch no seu repositório local com o numéro da issue digite:
```sh
$ git checkout -b "[#numerodaissue]"
```

Ou para criar a branch com um nome específico digite:
```sh
$ git checkout -b nomedabranch
```
Ao concluir o trabalho nesta branch e adicionar os arquivos e commitar,
você deve fazer o push para o repositório, informando o número da issue.

```sh
$ git push origin "#numerodaissue"
```

Após isso, você deve solicitar o Pull (Merge) Request para mesclar suas alterações com o branch master ou develop.

### O que é Pull ou Merge Request?
É a ação de solicitar ao Admin do repositório para aceitar a sua contribuição ao projeto, ao solicitar o PR ele ficará pendente aguardando o aceite, assim o Admin poderá revisar o código, verificar se há conflitos, e ele pode aceitar ou não a sua contribuição.

#### Por que trabalhar usando o Pull Request?
Já pensou se alguém que você não conhece, envia uma alteração para o seu branch master sem passar por uma revisão sua e nessa alteração o "cara" apaga uma parte importante ou todo o seu projeto? Esse é só um exemplo de porquê usar o PR.

#### Isso é tudo pessoal :)
Para mais informações vide: [Documentação do Git](https://git-scm.com/book/pt-br/v1/Primeiros-passos-No%C3%A7%C3%B5es-B%C3%A1sicas-de-Git)

---
Feito com <3 por [Evando Junior](https://github.com/evandojunior)

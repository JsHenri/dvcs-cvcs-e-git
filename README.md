Nome do estagiario: José Henrique Bernardes Vieira<br>
Data: 05/08/2024

# O que é CVCS

CVCS significa Centralized Version Control System (Sistema de Controle de Versão Centralizado). Em um CVCS existe um servidor central que contem todas as informações de histórico de todas as versões e arquivos. Os desenvolvedores fazem Check-Out dos arquivos a partir desse servidor central em suas máquinas, e depois fazem as suas alterações e então sobem de volta as modificações em forma de commits para esse servidor central.

## Caracteristicas principais do CVCS:

- Servidor Central: Todos os dados e o histórico de versões estão armazenados em um único servidor central.

- Check-out e Commit: Os desenvolvedores fazem check-out dos arquivos do servidor, trabalham neles localmente e fazem commit das alterações de volta ao servidor central.

- Controle de Acesso: O servidor central pode controlar quem tem permissão para acessar e modificar os arquivos, facilitando a gestão de permissões.

## Exemplo de CVCS:

- Subversion(SVN): Um dos CVCS mais populares, muito utilizados em projetos de código aberto e comerciais.

- CVS (Concurrent Versions System): Um sistema de controle de versão antigo, que influenciou muitos sistemas posteriores, como Subversion, Git, Perforce e muitos outros.

- Perforce: Um sistema de controle de versão comercial amplamente usado em grandes empresas de software.

## Beneficios do CVCS:

- Simplicidade: Para projetos pequenos ou equipes centralizadas, o CVCS consegue ser fácil de entender e de gerenciar.

- Controle: O servidor central pode impor politicas de acesso e garantir a integridade dos dados.

- Backup: Um único ponto para backup, entretanto, isso tambem pode ser uma desvantagem.

## Desvantagem do CVCS:

- Ponto único de falha: Se o servidor central falhar ou ficar inacessivel, os desenvolvedores não poderão obter o histórico e nem fazer commits

- Performance: Pode haver atraso nas operações de commits e commits, se a rede estiver lenta ou o servidor estiver sobrecarregado,

- Escabilidade: Menos eficientes para equipes distribuidas em grandes distancias, como fora do pais, ou projetos maiores em comparação a sistemas distribuidos.

## Exemplo:
Um desenvolvedor usa um servidor CVCS como o Subversion para fazer check-out(que significa o processo de trazer uma cópia do que esta no repositório remóto para repositório local) dos arquivos do repositório central. Após fazer modificações, o desenvolvedor faz os commits para o servidor central onde os outros desenvolvedores podem acessar e atualizar seus trabalhos.

# Versionamento de Branches
As Branches também conhecidas como ramificações no Git são estados salvos de um projeto desenvolvido ou em desenvolvimennto dentro de um repositório. As versões permitem que seja possivel trabalhar em diferentes funcionalidades, correções de bugs ou experimentos de uma maneira isolada.

# O que é DVCS
DVCS significa Distributed Version Control System (Sistema de Controle de Versão Distribuído). É um tipo de sistema de controle de versão onde o repositório é completo de código, que inclui todo histórico de mudanças, e tudo nele é clonado para cada usuario que trabalha no projeto.

## Caracteristicas principais do DVCS:

- Distruibuido: Cada desenvolvedor recebe uma cópia do projeto dentro da sua maquina e mais todo o histórico de mudanças. O que permite que o desenvolvedor faça operações de versionamento como, commits, diffs e reverts, sem a necessidade de uma conexão com um servidor central.

- Colaboração: Facilita a Colaboração entre desenvolvedores, já que, as alterações podem ser feitas diretamente entre repositórios locais sem a necessidade de um servidor central.

- Resiliencia: A ausência de um único ponto de falha. Mesmo que o servidor central esteja inacessivel, as alterações ficam salvas no repositório local, assim podendo trabalhar sem interrupções localmente.

## Exemplos de DVCS:

- Git: O sistema de controle de versão distribuído mais popular, criado por Linus Torvalds para o desenvolvimento do kernel do Linux.

- Mercurial: Outro DVCS popular, conhecido por sua simplicidade e eficiência em grandes projetos.

- Bazaar: Um DVCS focado em usabilidade, criado pela Canonical para o desenvolvimento do Ubuntu.

## Beneficios do DVCS:

- Velocidade: Operações Locais são rapidas por não necessitarem de um servidor central.

- Flexibilidade: Desenvolvedores podem criar branches e mesclar mudanças localmente sem impactar no repositório local.

- Backup: Cada cópia do repositório serve como um backup completo, aumentando a segurança dos dados.

## Exemplo de Uso:
Um desenvolvedor pode clonar um repositório Git, trabalhar em uma nova funcionalidade em uma branch local, fazer commits e, quando estiver satisfeito, enviar (push) essas mudanças para o repositório central ou compartilhar diretamente com outros desenvolvedores.

## Como funciona:

- Branch Principal(main): É a branch principal onde o projeto final é mantido.

- Branches de funcionalidade: essas branches são criadas a partir da branch como por exemplo a principal e nelas é possivel fazer alterações no código sem alterar o projeto final. Por exempolo criar uma `feature` para implementar uma nova funcionalidade. 

- Merge: É quando a funcionalidade está testada e pronta, assim ela é mesclada (merge) na branch principal que recebe as suas funcionalidades.

## Beneficios do versionamento de branches

- Isolamento de Trabalho: Permite que varias pessoas possam trabalhar no mesmo projeto simultaneamente sem que haja alterações no trabalho de cada um.
- Facilidade de integração: as mudanças podem ser revisadas e integradas de maneira mais controlada.
- Histórico claro: Mantem um histórico claro que mostra onde e quando cada alteração foi desenvolvida e integrada.

# Git

## O que é Git

O Git é um Sistema de Controle de Versão Distrubuido (Distributed Version Control System ou DVCS), ele é muito utilizado no desenvolvimento de softwares ou sistemas. Ele faz com que varias pessoas possam trabalhar em um mesmo projéto ao mesmo tempo sem que um altere o trabalho do outro. O Git tambem conta com um histórico de alterações facilitando consultas ou mudanças, onde é possivel voltar os trabalhos que foram alterados e enviados em um repositório remóto.

>## Principais Caracteristicas:
>
>- Distribuído: Cada desenvolvedor possui uma cópia completa do repositório, incluindo seu histórico.
>
>-  Eficiência: Git é rápido e eficiente no gerenciamento de versões e no acompanhamento de mudanças.
>
>-  Segurança: Os dados em Git são armazenados de forma segura, usando algoritmos de hashing para garantir a integridade dos dados.

## Exemplo de Uso

Se está desenvolvendo um aplicativo web ou algum sistema novo de transação, o Git permite que sejá possivel salvar commits do seu código em pontos e estados diferentes. Se algo der errado é possivel voltar aos commits para uma versão anterior do código.

## Clonagem e Remoto
### Clonar um Repositório

```Bash
git clone "url do repositório no github" "novo nome do arquivo"
```
Descrição: Clona o repositório localizado na URL fornecida para um diretório local com o nome especificado.


```Bash
git remote -v
```

Descrição: Lista todos os repositórios remotos configurados para o repositório local atual.

### Adicionar um Repositório Remoto

```
git remote add origin "url do repositório github"
```

Descrição: Adiciona um novo repositório remoto chamado origin com a URL fornecida.

## Status e Modificações
### Verificar o Status do Repositório

```Bash
git status
```
Descrição: Mostra o estado atual do repositório, incluindo arquivos modificados, adicionados ou excluídos.

### Criar um Novo Arquivo

```Bash
touch "nome do arquivo + tipo"
```
Descrição: Cria um novo arquivo vazio com o nome e tipo especificado.

Exemplo: touch novo-arquivo.txt

## Histórico e Ignorar Arquivos
### Visualizar o Log de Commits

```Bash
git log
```
Descrição: Exibe o histórico de commits do repositório.
Adicionar Arquivo ao .gitignore

```Bash
echo "nome do arquivo" > .gitignore
```
Descrição: Adiciona o nome do arquivo ao arquivo .gitignore, indicando que ele deve ser ignorado pelo Git.

### Limpar o .gitignore

```Bash
echo > .gitignore
```

Descrição: Limpa todo o conteúdo do arquivo .gitignore.


## Remoção, Restauração, Adicionar e Verificação
### Remover o Diretório Git

```Bash
rm -rf .git
```
Descrição: Remove o diretório .git, efetivamente desvinculando o repositório local do Git.

### Restaurar um Arquivo Modificado

```Bash
git restore "nome do arquivo"
```
Descrição: Restaura o arquivo especificado para seu estado no último commit.
Commits e Resets

### Alterar a Mensagem do Último Commit

```Bash
git commit --amend -m "novo nome"
```

Descrição: Modifica a mensagem do último commit.

### Resetar para um Commit Específico (Suave)

```Bash
git reset --soft "código da hash"
```

Descrição: Reseta o histórico do Git para o commit especificado, mantendo as mudanças no índice.

### Resetar para um Commit Específico (Misto)

```Bash
git reset --mixed "código hash"
```
Descrição: Reseta o histórico do Git para o commit especificado, mantendo as mudanças no diretório de trabalho, mas não no índice.

### Adicionar e Comitar Arquivos
```Bash
git add *
```
```Bash
git commit -m "nome"
```
Descrição: Adiciona todos os arquivos ao índice e faz um commit com a mensagem especificada.

### Resetar para um Commit Específico (Forte)

```Bash
git reset --hard "código hash"
```

Descrição: Reseta o histórico do Git para o commit especificado, descartando todas as mudanças no índice e no diretório de trabalho.

### Verificar o Reflog

```Bash
git reflog
```

Descrição: Mostra um log de todas as operações de referência (commits, resets, checkouts) realizadas no repositório.

## Branches

### Criar e Mudar para uma Nova Branch

```Bash
git checkout -b "nome da nova branch"
```

Descrição: Cria uma nova branch com o nome especificado e muda para essa branch.

### Mudar para uma Branch Existente

```Bash
git checkout "nome da branch"
```

Descrição: Muda para a branch especificada.

### Verificar Branches

```Bash
git branch -v
```

Descrição: Lista todas as branches e mostra o commit mais recente em cada uma.

### Mesclar uma Branch

```Bash
git merge "nome da branch"
```

Descrição: Mescla a branch especificada na branch atual.

### Deletar uma Branch

```Bash
git branch -d "nome da branch"
```

Descrição: Deleta a branch especificada.

## Atualizações e Diferenciação

Puxar Atualizações do Repositório Remoto

```Bash
git pull
```

Descrição: Busca (fetch) e integra (merge) mudanças do repositório remoto na branch atual.

### Buscar Atualizações do Repositório Remoto

```Bash
git fetch
```

Descrição: Busca mudanças do repositório remoto, mas não as integra automaticamente.

### Mostrar Diferenças

```Bash
git diff
```

Descrição: Mostra as diferenças entre o estado atual do diretório de trabalho e o índice.

### Mesclar com a Branch Principal

```Bash
git merge origin/main
```

Descrição: Mescla a branch principal (main) do repositório remoto na branch atual.

## Stash

### Salvar Mudanças Temporariamente

```Bash
git stash
```

Descrição: Salva mudanças não comitadas em um stash temporário.

### Listar Stashes

```Bash
git stash list
```

Descrição: Lista todos os stashes salvos.

### Criar e Mudar para uma Nova Branch, Aplicar Stash

```Bash
git checkout -b "nome da nova branch"
```

```Bash
git stash pop
```

Descrição: Cria uma nova branch e aplica as mudanças salvas no stash mais recente.

### Aplicar um Stash

```Bash
git stash apply
```

Descrição: Aplica as mudanças salvas no stash mais recente, mas não remove o stash.

## Atualizações Remotas

### Adicionar um Repositório Upstream

```Bash
git remote add upstream "o link do repositório remoto que deseja estar recebendo atualizações dele"
```

Descrição: Adiciona um repositório remoto chamado upstream para receber atualizações dele.

### Puxar Atualizações do Upstream

```Bash
git pull upstream "nome da branch"
```

Descrição: Puxa atualizações da branch especificada do repositório upstream e integra na branch atual.

### Puxar Atualizações de uma branch

```Bash
git pull origin "nome da branch"
```

Descrição: Puxa atualizações da branch especificada e integra na branch atual.

# O que é Gitflow

Gitflow é um modelo de fluxo de trabalho para Git que define uma maneira clara para o desenvolvimento de projetos. Uma ideia proposta por Vincent Driessen em 2010 e é amplamente adotada por equipes que usam o Git como controle de versão. A ideia principal do gitflow é utilizar diferentes branches para organizar um trabalho de maneira mais eficiente e estruturada.

## Principais componentes do Gitflow

### Principais Branches
- **Main:** é a primeira branch criada é quem a branch develop copia e contém o histórico oficial das releases do projeto. A branch main é quem recebe as versões estaveis do projeto a partir da develop.

- **Develop:** Serve como a branch de integração onde todas as features irão pegar seu estado e serão implementadas quando terminadas. Essa branch é a que reflete o estado mais recente do desevolvimento.

### Branches de suporte

- **Feature Branches:** Usadas para desenvolver novas funcionalidades que serão adicionadas para a proxima release. São branches criadas a partir da develop e quando terminadas suas funcionalidades são implementadas de volta para a develop e após isso apagadas.

- **Release Branches:** São branches criadas para preparar novas versões do projeto. Permitem aplicar pequenas correções e ajustes antes do lançamento. São criadas a partir da develop e após a finalização, são mescladas tanto na master quanto na develop e a branch é deletada.

- **Hotfix Branches:** São branches criadas para cirrigir problemas criticos rapidamente na produção. São criadas a partir da main e após sua finalização as mudanças são mascladas na main e na develop e a branch é deletada.

## Fluxo de Trabalho:

### Desenvolvendo Funcionalidades
 - Após a branch develop ser criada a partir da main, os desenvolvedores começam a criar branches feature a partir da develop para desenvolver as suas funcionalidades.

 - Quando completo as features com a funcionalidades são mescladas de volta na branch develop e logo após isso a features são deletadas.

 ### Preparação de Releases
- Quando asfuncionalidades estão prontas para ser lançadas, é criada uma release a partir da develop.

- Pequenas correções e ajustes podem ser feitas nessa branch.

- A release branch com as pequenas modificações são mescladas na branch main e também na develop, e uma tag é marcada na branch main para que marcar a nova versão e após isso a branch release é deletada.

### Correção de bugs em produção

- Se houver problemas cirticos na produção, uma branch hotfix é criada a partir da main

- Após a correção a branch hotfix será mesclada na branch main e na brach develop, assim garantindo que as modificações estejam disponiveis em ambas as branches.

### Vantagens do Gitflow
- **Organização:** Proporciona uma estrutura clara para organizar o trabalho de desenvolvimento e lançamento.

- **Paralelismo:** Permite que múltiplas funcionalidades e correções sejam desenvolvidas em paralelo.
- **Controle de Qualidade:** Facilita o controle de qualidade ao isolar o desenvolvimento de funcionalidades, preparação de releases e correções críticas.

### Desvantagens do Gitflow
- **Complexidade:** Pode ser complexo e excessivo para projetos pequenos ou equipes menores.

- **Overhead:** Introduz overhead adicional em termos de criação e manutenção de múltiplas branches.

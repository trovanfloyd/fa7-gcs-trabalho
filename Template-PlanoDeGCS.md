SMART
=================
Plano de Gerenciamento de Configuração
======================================
Versão 1.0
------------------


Histórico de Versões
--------------------

|Data                |Versão       |Descrição               |Autor          |
|--------------------|-------------|------------------------|---------------|
|15/12/2014|1.0|Versão inicial do plano|Gustavo Salomão 
Andre Belarmino
Josilene Santos
Francisco Chagas
Hildo Costa|
|_&lt;dd/mm/aaaa&gt;_|_&lt;1.1&gt;_|_&lt;Outra versão&gt;_  |_&lt;autor&gt;_|



1. Introdução
==============

O Plano de Gerenciamento de Configuração tem como objetivo tornar claras as atividades a serem desempenhadas pelos envolvidos (Partes atuantes, Partes interessadas, Diretoria e a Coordenação) no que diz respeito a criação, atualização e manutenção de artefatos, documentos, processos e quaisquer outros tipos de informações sobre o projeto, durante seu ciclo de vida, tomando como referencia as regras definidas neste para nomenclatura de documentos, locais onde serão armazenados os artefatos e as referências dos termos utilizados na descrição das solicitações (vide Glossário de Termos).

1.1 Finalidade
---------------
A finalidade deste documento é apresentar um conjunto de regras e definições sobre o controle, nomenclatura e responsáveis pela manutenção de artefatos relativos ao projeto e ditar como as mudanças ocorrerão durante o desenvolvimento do ciclo de vida do projeto, determinando quais são os membros responsáveis por mantê-los.

1.2 Escopo
----------
A atuação da Configuração de Mudanças deverá ocorrer desde o momento do Termo de Abertura do Projeto (ou reunião de Kick-off), até o seu encerramento, usando como marco a Reunião de Encerramento do Projeto (ou o Relatório de Lições Aprendidas). Durante o ciclo de vida do projeto, os modelos de documentos de especificação de analise de sistemas, documento de interface do projeto, documentos de casos de uso, relatórios, atas de reuniões e documentos de casos de teste deverão ser manipulados conforme as atribuições da equipe, de acordo com estrutura proposta pela Diretoria (vide Item 2.2.2).

1.3 Definições, Acrônimos e Abreviações
---------------------------------------
Utilizando como critério a necessidade de monitorar as mudanças aplicadas aos itens de configuração diretamente associados ao produto a ser desenvolvido, serão aplicados acrônimos, abreviações sob os itens de configuração relativos a:
* Especificações de Casos de Uso;
* Especificações de Casos de Testes;
* Desenhos de Ícones e Regras de layout (CSS);
* Modelos de dados, Desenhos e Especificações de Arquitetura;
* Provas de Conceito;
* Planilhas de Estimativa, Controle de Tempo e Custo;
* Auditorias, Revisões e Inspeções de Código e Processos;
* Requisitos Funcionais;
* Requisitos Não Funcionais;
* Regras de Negócio;
* Regras de Banco de Dados;
* Testes Funcionais;
* Testes de Interface;
* Testes de Carga;
* Testes de Performance;
* Tags para Commits;
* Tags para Acertos / Correções;
* Tags para Adição de Novos Componentes / Elementos;
* Tags para Criação de Versões com correção de Bugs (Fix);
* Tags para Criação de Novas Versões com Novas Funções (Candidatas a Release - RC).

Vide detalhes no item (3).

1.4 Referências
---------------
Vide referências aos documentos citados nas seguintes templates:
* Template de Caso de Uso (Documento guia padrão, que explana em detalhes, como ocorrerá a análise do produto);
* Template de Caso de Teste (Documento guia padrão, que contém as explanações de como deverão proceder as análises e inferencias sobre os testes a serem realizados);
* Template de Prova de Conceito (Documento guia padrão, que explana quais são os passos a serem expostos para a equipe sobre o conhecimento adquirido no estudo e análise de uma nova tecnologia);
* Template de Interface (Documento guia padrão, responsável por explanar e manter como padrões os comportamentos de usabilidade ditados pela Diretoria, na aceitação do produto);

Vide informações gerais associadas a Gerencia de Configuração nos seguintes documentos:
* Documento de Glossário de Termos (que possui a descrição e explanação sobre os demais termos utilizados neste documento como nos demais artefatos produzidos no ciclo de vida do projeto).

1.5 Visão Geral
---------------
O documento está organizado em tópicos, que detalham os demais pontos da Gerencia de Configuração de Mudanças:
O item (2) irá expor como e quais são os responsáveis por manter os itens de configuração do projeto, bem como onde serão armazenadas as informações e quais são os repositórios designados as mesmas; O item (3) explana como ocorrerão as rotinas de gerenciamento de configuração, no que diz respeito aos padrões de nomenclaturas, acronimos e demais determinações de controle sobre os artefatos; Os procedimentos e rotinas de fluxo de atividades dos respectivos responsáveis sobre os itens de configuração serão descritos pelo item (4) e, por fim, os itens (5) e (6) detalham, respectivamente, sobre as necessidades de treinamento para capacitação da equipe e a execução das rotinas de auditorias, a fim de realizar uma análise sobre como vai o desenvolvimento, o monitoramento e o controle das solicitações de mudança, com base no ciclo de vida do projeto.


2. Gerenciamento de Configuração de Software
============================================

2.1 Organização, Responsabilidades e Interfaces
------------------------------------------------
A equipe do departamento de TI executa a função de Gerenciador de Configuração para todos os projetos. Cada projeto terá uma ou mais pessoas designadas à função do Gerenciador de Controle de Mudanças.

2.2 Ferramentas, Ambiente e Infra-estrutura
-------------------------------------------

2.2.1 Ferramentas:

  As ferramentas utilizadas para a operacionalização da Gestão de Configuração são:
* Git: Ferramenta utilizada para controle de versão de documentos e códigos-fontes em todo o ciclo de vida do projeto.
* Gitlab: Servidor central para armazenamento dos repositórios.
* Pacote Microsoft Office: Pacote utilizado para a confecção dos documentos de Gestão de Configuração. 
* Jira: Ferramenta para controle de mudanças.

2.2.2 Ambientes:

* Ambiente de Desenvolvimento

  É o ambiente no qual ocorre a edição dos itens de configuração. Toda a equipe tem acesso a este ambiente. A sua estrutura é composta de 3 diretórios:
  
  /principal: Guarda a versão dos itens de configuração em desenvolvimento.
  
  /temp: Usado pelos desenvolvedores para armazenar temporariamente alterações e testes, sem comprometer a versão principal
  
  /versoes: Armazena versões estáveis do sistema que serão disponibilizadas para teste ou mesmo para reprodução.

* Ambiente de Testes/Homologação
  
  Este ambiente contém versões do sistema disponibilizadas para testes e homologação. Apenas as equipes de teste e homologação possuem permissão de escrita. 

* Ambiente de Produção

  Contém apenas versões do sistema autorizadas pelo Gerente do Sistema. Apenas a equipe de implantação possui permissão de escrita.

2.2.3 Infra-estrutura:

  O setor de infra-estrutura é responsável pela manutenção dos servidores, sendo responsável pelas suas configurações, controle de acesso, backup, atualizações, etc.

  Existem 4 servidores:
* 1 para cada ambiente (Desenvolvimento, Teste/Homologação e Produção), no qual é disponibilizado acesso remoto via Terminal Service para os membros de cada equipe.
* 1 servidor com Gitlab, que é utilizado como repositório central.


3. O Programa de Gerenciamento de Configuração
==============================================

3.1 Identificação da Configuração
---------------------------------
### 3.1.1 Métodos de Identificação
----------------------------------
__Regra de Formação de Nomes de Artefatos__

Os nomes dos artefatos de um projeto devem seguir a regra:
* &lt;CÓDIGO_SISTEMA&gt;_&lt;MÓDULO SISTEMA&gt;_&lt;NOME_ARTEFATO&gt;_&lt;DETALHES&gt;.EXT
Onde:
* &lt;CÓDIGO_SISTEMA&gt;:
letra “S” seguida dos três números que compõem o código do sistema (OBRIGATÓRIO). Ex.: S344.
* &lt;MÓDULO_SISTEMA&gt;:
nome do módulo do sistema com letras maiúsculas (OBRIGATÓRIO, apenas quando houver). Quando o nome do módulo for composto por mais de uma palavra, separá-las por undescore ( _ )
Ex.: S400_GRUPO_ECONOMICO.

* &lt;NOME_ARTEFATO&gt;:
um conjunto de caracteres alfanuméricos, sendo a primeira letra de cada palavra maiúscula e as demais minúsculas (OBRIGATÓRIO), para os artefatos definidos no RUP-BNB. Os elementos de ligação como “de” e “do” devem ser suprimidos e deverá ser usado o undescore (_) para separar as palavras. Veja a nomenclatura de identificação dos artefatos na tabela 2.

* &lt;DETALHES&gt;:
um conjunto de caracteres alfanuméricos, sendo a primeira letra de cada palavra maiúscula e as demais minúsculas (OPCIONAL). O detalhe pode conter uma descrição sobre o que trata o documento e as palavras devem ser separadas por undescore (_).Para artefatos que envolvam data em sua identificação, colocar a data invertida segundo o formato aaaammdd. No caso dos artefatos definidos na tabela 2, o detalhe deve conter o número e o nome do caso de uso.
EXT :
Extensão do arquivo que representa o artefato.]_

### 3.1.2 Itens de Configuração
Relacionar os artefatos ou grupos de artefatos, separando por tipo, modulo ou subsistema, responsável ou momento em que deverão ser incluídos em baselines.

* _“Inclusão em Baseline” em branco significa que o grupo de artefatos não participará de baseline. Pode ser expresso como uma data ou identificador de uma baseline, fase ou ponto de controle_
* _“Responsável”: indicar nominalmente, sempre que possível]_

| Item (ou Tipo de Item)                 | Responsável na equipe	     | Inclusão em Baseline |
|----------------------------------------|----------------------------- |----------------------|
|Especificação de requisitos             |Victor(Analista de Requisitos)|            Sim       |
|Plano do projeto                        |Hildo(Gerente do projeto)     |            Sim       |
|Documento de visão                      |Pedro(Estagiário)             |                      |

### 3.1.3 Baselines do Projeto
As baselines funcionam como um padrão oficial no qual os trabalhos subseqüentes são baseados. Somente mudanças autorizadas podem ser efetuadas nas baselines.

__Baseline de Planejamento Composição__
Dados do Projeto na Ferramenta de Gestão de Projetos:
- Cronograma
- Data Planejada de Início do Projeto
- Data Planejada de Término do Projeto
- Percentual Concluído
- Duração Planejada
- Duração Real
- Esforço Planejado
- Esforço Real
- Custo Planejado
- Custo Real Em que momento é Gerada
Após aprovação do Plano de Projeto.
Após planejamento de iteração.


__Baseline de Artefatos Composição__
- Documento de Visão
- Declaração de Escopo
- Especificação Casos de Uso Em que momento é Gerada
A cada Homologação de artefato pelo Cliente. Desta forma, pode ser criada uma baseline para cada artefato homologado ou para um conjunto de artefatos homologados.


__Baseline de Mudança Composição__
Quaisquer itens que componham baseline e que precisem ser alterados.
Os itens de configuração que compõem Baseline somente poderão ser alterados mediante uma Solicitação de Mudança APROVADA na Ferramenta de Gestão de Projetos. Em que momento é Gerada
A cada alteração de itens de baseline.

Antes de ser criada, a baseline precisa ser aprovada pelo comitê de mudanças, composto pelo lider do projeto, gerente, arquiteto e do analista de testes.

### 3.1.4 Estrutura do Repositório de Versões
Os projetos deverão seguir a seguinte estrutura de pastas no repositório:
Projeto
   -Sigla do projeto
     Analise e design
     Encerramento
     Gerenciamento de Configuração
     Homologacao
     Implantação
     Implementação

    -Planejamento e Controle
       -Artefatos nao controlados
          Cliente
          Internos

       -Atas de Reuniao
          Cliente
          Equipe
          Gerencia
          Grupos de Apoio
        Avaliacoes
        Mudancas
        Relatorio de Status

    -Requisitos
        Atas de reuniao
        Casos de uso
        prototipo

    -Teste
        Caso de teste]_

3.2 Controle de Configuração e Mudança
--------------------------------------

### 3.2.1 Processamento e Aprovação de Solicitações de Mudança
Será seguigo as atividades do RUP: Gerenciar Controles de Mudanças e Alterar & Entregar Itens de Configuração, com os seguintes refinamentos.

Artefato: Ordem de Trabalho é mesclado com Artefato: Controle de Mudanças (CR) .  Portanto, o status das ordens de trabalho é gerenciado pelo rastreio do status de CRs.

Uma atividade UCM é mapeada para o Artefato: Controle de Mudanças (CR). O termo CR será aplicado para o restante desse documento para consultar uma Atividade UCM. A Empresa segue o esquema UCM ClearQuest padrão.

As atividades e os estados utilizados pela Empresa para gerenciar CRs estão descritas em Conceitos: Gerenciamento do Controle de Mudanças.

Os campos requeridos para um CR são impostos pelo esquema ClearQuest e, portanto, não precisam ser documentados aqui.

O seguinte define as tarefas aplicáveis e mentores de ferramentas.

Função	Tarefas do Rational Unified Process	Mentores da Ferramenta Rational	Notas/Ajuste
Qualquer Função	Tarefa: Submeter Controle de Mudanças
Tarefa: Atualizar Controle de Mudanças	Submetendo os Controles de Mudanças
Gerenciador de Controle de Mudanças	Tarefa: Rever Controle de Mudanças 
Tarefa: Confirma CR Duplicado ou Rejeitado	Relatando o Status de Revisão e de Trabalho	
A Empresa não requer o uso de um Quadro de Controle de Configuração.  Os Controles de Mudança são revisados e aprovados por um membro do projeto, o Gerente de Controle de Mudança, que geralmente também é o Gerente de Projetos, Líder da Equipe ou Arquiteto do Software.

Coordenador de Projeto	Tarefa: Planejar e Designar o Trabalho	 	Artefato: A Ordem de Trabalho é mesclada com o Artefato: Controle de Mudanças (CR). A designação de trabalho é executada, designando o CR. Consulte os Conceitos: Gerenciamento do Controle de Mudanças para obter detalhes.
Qualquer Função	Tarefa: Efetuar Alterações	Utilizando os Conjuntos de Mudanças do UCM
Qualquer Função	Tarefa: Entregar Alterações 	Entregando Seu Trabalho	"Qualquer Função" (quem efetuou as alterações) deve assegurar que os procedimentos de revisão aplicáveis foram seguidos e a revisão tenha sido transmitida, antes de fornecer qualquer alteração.
Os procedimentos de revisão aplicáveis são especificados no Caso de Desenvolvimento.

Integrador	Tarefa: Verificar Mudanças na Construção
 

### 3.2.2 Comitê de Controle de Mudança (CCB)
CCB (Conselho de Controle de Mudanças (ou Configuração)) - O conselho que supervisiona o processo de alteração que consiste em representantes de todas as partes interessadas, incluindo clientes, desenvolvedores e usuários. Em projetos pequenos, um único membro da equipe, como o coordenador de projeto ou o arquiteto de software, pode desempenhar essa função. No Rational Unified Process, isso é mostrado pela função de Gerenciador do Controle de Mudanças.

Reunião de Revisão de CCB - A função desta reunião é revisar os Controles de Mudanças Enviados. Uma revisão inicial do conteúdo do Controle de Mudanças é feita na reunião para determinar se o pedido é válido. Se for, será decidido se a mudança está dentro ou fora do escopo das liberações atuais, de acordo com prioridade, planejamento, recursos, nível de esforço, risco, gravidade e outros critérios relevantes definidos pelo grupo. Geralmente, essa reunião ocorre uma vez por semana. Se o volume de Controles de Mudanças aumentar significativamente ou quando o ciclo de liberação está perto do fim, a reunião pode ser mais freqüente, até mesmo diária. Os membros que normalmente participam da Reunião de Revisão do CCB são o Gerenciador de Teste, o Gerenciador de Desenvolvimento e um membro do Departamento de Marketing. É possível que participantes adicionais sejam requisitados pelos membros, caso os julguem "necessários".

Formulário de Envio de Controle de Mudanças - Esse formulário é exibido quando um Controle de Mudanças está sendo Enviado pela primeira vez. Somente os campos necessários deverão ser preenchidos pelo solicitante, como exibido no formulário.

Formulário Combinado de Controle de Mudanças - Esse formulário é exibido quando você está revisando um Controle de Mudanças que já foi enviado. Ele contém todos os campos necessários para descrever o Controle de Mudanças.

O contorno do processo de Controle de Mudanças a seguir descreve os estados e os status dos Controles de Mudanças durante seu processo geral e quem precisa ser notificado durante o ciclo de vida do Controle de Mudanças. O processo geral associado a Controles de Mudanças está descrito em Tarefa: Estabelecer Processo de Controle de Mudanças.

4. Padrões e Procedimentos
==========================
4.1 Padrão de nomeclatura dos artefatos
---------------------------------------
A Gestão de Configuração define qual a nomenclatura padrão a ser seguida pelos itens de configuração. Os documentos devem ser nomeados com as letras iniciais sempre em maiúsculo, sem acentos ou cedilhas e eliminando as preposições e espaços, os espaços serão substituídos por underscore (_).

| Artefato/Projeto |	Regra |	Exemplo |
|------------------|-------|---------|
| Documentos em geral sem modelo previsto	| <_NomeProjeto_>_<_NomeDocumento_> |	PRJ_PlanoAcao |
| Documentos em geral com modelo previsto |	De forma geral, os nomes dos arquivos devem seguir sempre o padrão: <_NomeProjeto_>_<_NomeModelo_>	| Exemplo: PRJ_TermoAberturaProjeto PRJ_EspecificacaoRequisitos |
|------------------|-------|---------|

4.2 Procedimento de backup
--------------------------
### 4.2.1 Rotina de backup
A rotina de backup consiste em realizar cópias controladas de todo o repositório do projeto, no intuito de preservar as informações e permitir a recuperação das mesmas, em caso de falhas.
A recuperação das informações deve ser realizada conforme a estrutura de pastas definidas no repositório do projeto e observando-se os níveis de segurança determinados na Ferramenta de Gestão de Configuração.

### 4.2.2 Procedimento de descarte
Não há descarte de artefatos do projeto.

5. Treinamento e Recursos
=========================
Os seguintes cursos são recomendados de acordo com a função

| Treinamento                 | Ferramenta	     | Função |
|----------------------------------------|-----------------------------|----------------------|
|Controle de Versão com o GIT|GIT|Qualquer função que altere os itens de configuração|
|Administrando o GitLab|GITLAB|Administrador do GitLab|
|Controle de Mudanças com o JIRA|JIRA|Integrantes do CCB|

6. Auditorias de Configuração
=============================
Esta atividade tem por objetivo assegurar se o produto esta de acordo com os requisitos pré-estabelecidos e que correspondam as informações de configuração de produto. 
As auditorias de configuração devem ser realizadas para cada ciclo do processo de desenvolvimento de forma a garantir que o processo de gerência de configuração estão sendo aplicados corretamente. Os artefatos gerados devem armazenados no repositório do projeto e devem ser acompanhados pelos Gerentes do Projeto.

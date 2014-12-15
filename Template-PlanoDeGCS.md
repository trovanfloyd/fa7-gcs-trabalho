<Nome do Projeto>
=================
Plano de Gerenciamento de Configuração
======================================
Versão &lt;1.0&gt;
------------------

_[Observação: O template a seguir é fornecido para uso com o Rational Unified Process (RUP).  O texto exibido entre colchetes e em itálico foi incluído para orientar o autor e deve ser excluído antes da publicação do documento._

_Este documento utiliza a formatação da linguagem [Markdown] (http://daringfireball.net/projects/markdown/). Você pode encontrar um guia de referência rápido [aqui] (https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).]_

Histórico de Versões
--------------------

|Data                |Versão       |Descrição               |Autor          |
|--------------------|-------------|------------------------|---------------|
|_&lt;dd/mm/aaaa&gt;_|_&lt;1.0&gt;_|_&lt;Versão inicial&gt;_|_&lt;autor&gt;_|
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
Serão aplicados acrônimos, abreviações sob os itens de configuração relativos a:
(01) Especificações de Casos de Uso; (02) Especificações de Casos de Testes; (03) Desenhos de Ícones e Regras de layout (CSS); (04) Modelos de dados, Desenhos e Especificações de Arquitetura; (05) Provas de Conceito; (06) Planilhas de Estimativa, Controle de Tempo e Custo; (07) Auditorias, Revisões e Inspeções de Código e Processos; (08) Requisitos Funcionais; (09) Requisitos Não Funcionais; (10) Regras de Negócio; (11) Regras de Banco de Dados; (12) Testes Funcionais; (13) Testes de Interface; (14) Testes de Carga; (15) Testes de Performance; (16) Tags para Commits; (17) Tags para Acertos / Correções; (18) Tags para Adição de Novos Componentes / Elementos; (19) Tags para Criação de Versões com correção de Bugs (Fix); (20) Tags para Criação de Novas Versões com Novas Funções (Candidatas a Release - RC).

Vide detalhes no item (3).

1.4 Referências
---------------
Vide referências aos documentos citados nas seguintes templates:
(01) Template de Caso de Uso (Documento guia padrão, que explana em detalhes, como ocorrerá a análise do produto);
(02) Template de Caso de Teste (Documento guia padrão, que contém as explanações de como deverão proceder as análises e inferencias sobre os testes a serem realizados);
(03) Template de Prova de Conceito (Documento guia padrão, que explana quais são os passos a serem expostos para a equipe sobre o conhecimento adquirido no estudo e análise de uma nova tecnologia);
(04) Template de Interface (Documento guia padrão, responsável por explanar e manter como padrões os comportamentos de usabilidade ditados pela Diretoria, na aceitação do produto);

Vide informações gerais associadas a Gerencia de Configuração nos seguintes documentos:
(05) Documento de Glossário de Termos (que possui a descrição e explanação sobre os demais termos utilizados neste documento como nos demais artefatos produzidos no ciclo de vida do projeto).

1.5 Visão Geral
---------------
O documento está organizado em tópicos, que detalham os demais pontos da Gerencia de Configuração de Mudanças:
O item (2) irá expor como e quais são os responsáveis por manter os itens de configuração do projeto, bem como onde serão armazenadas as informações e quais são os repositórios designados as mesmas; O item (3) explana como ocorrerão as rotinas de gerenciamento de configuração, no que diz respeito aos padrões de nomenclaturas, acronimos e demais determinações de controle sobre os artefatos; Os procedimentos e rotinas de fluxo de atividades dos respectivos responsáveis sobre os itens de configuração serão descritos pelo item (4) e, por fim, os itens (5) e (6) detalham, respectivamente, sobre as necessidades de treinamento para capacitação da equipe e a execução das rotinas de auditorias, a fim de realizar uma análise sobre como vai o desenvolvimento, o monitoramento e o controle das solicitações de mudança, com base no ciclo de vida do projeto.


2. Gerenciamento de Configuração de Software
============================================

2.1 Organização, Responsabilidades e Interfaces
------------------------------------------------
_[Descreva quem será o responsável pela execução das diversas atividades de Gerenciamento de Configuração (CM) descritas no Processo de CM.]_

2.2 Ferramentas, Ambiente e Infra-estrutura
-------------------------------------------
_[Descreva o ambiente de computação e as ferramentas de software a serem utilizadas para desempenhar as funções de CM em todo o ciclo de vida do projeto ou produto._
_Descreva as ferramentas e os procedimentos necessários utilizados para o controle de versão dos itens de configuração gerados no ciclo de vida do projeto ou produto._
_As questões envolvidas na configuração do ambiente de CM incluem:_
* _tamanho previsto dos dados do produto_
* _distribuição da equipe do produto_
* _localização física dos servidores e clientes]_
 


3. O Programa de Gerenciamento de Configuração
==============================================

3.1 Identificação da Configuração
---------------------------------
### 3.1.1 Métodos de Identificação
----------------------------------
_[Descreva como os artefatos do projeto ou produto devem ser nomeados, marcados e numerados. O esquema de identificação deve abranger o hardware, o software do sistema, os produtos de terceiros (COTS) e todos os artefatos de desenvolvimento de aplicativos listados na estrutura de diretórios do produto; por exemplo, planos, modelos, componentes, software de teste, resultados e dados, executáveis e assim por diante.]_

### 3.1.2 Itens de Configuração
_[Relacionar os artefatos ou grupos de artefatos, separando por tipo, modulo ou subsistema, responsável ou momento em que deverão ser incluídos em baselines._
* _“Inclusão em Baseline” em branco significa que o grupo de artefatos não participará de baseline. Pode ser expresso como uma data ou identificador de uma baseline, fase ou ponto de controle_
* _“Responsável”: indicar nominalmente, sempre que possível]_

| Item (ou Tipo de Item)                 | Responsável na equipe	     | Inclusão em Baseline |
|----------------------------------------|-----------------------------|----------------------|
|_&lt;grupo de itens de configuração&gt;_|_&lt;nome do responsável&gt;_|_&lt;momento a partir do qual o conjunto de artefatos será incluído em baseline&gt;_|


### 3.1.3 Baselines do Projeto

_[As baselines funcionam como um padrão oficial no qual os trabalhos subseqüentes são baseados. Somente mudanças autorizadas podem ser efetuadas nas baselines._
_Descreva em que pontos do ciclo de vida do projeto ou produto as baselines devem ser estabelecidas. As baselines mais comuns devem ser definidas ao final de cada uma das fases de Iniciação, Elaboração, Construção e Transição. Elas também podem ser geradas no final de iterações ocorridas dentro das várias fases ou com freqüência ainda maior._
_Descreva quem autoriza uma baseline e o que ela contém.]_

### 3.1.4 Estrutura do Repositório de Versões
_[Descreva a organização de diretórios do seu repositório e que itens/arquivos devem ser armazenados em cada diretório.]_

3.2 Controle de Configuração e Mudança
--------------------------------------

### 3.2.1 Processamento e Aprovação de Solicitações de Mudança
_[Descreva o processo pelo qual os problemas e as mudanças são submetidos, revisados e dispostos. Inclua como funciona a transição de estados de uma solicitação de mudança]_

### 3.2.2 Comitê de Controle de Mudança (CCB)
_[Descreva a participação e os procedimentos para processar solicitações e aprovações de mudança a serem seguidos pelo CCB. Informe quem são os membros do CCB e suas responsabilidades.]_



4. Padrões e Procedimentos
==========================
_[Descreva os padrões e procedimentos que devem ser seguidos no projeto. Crie subseções se achar necessário, para organizá-los melhor.]_



5. Treinamento e Recursos
=========================
_[Descreva as ferramentas de software, o pessoal e o treinamento necessários para implementar as atividades de CM especificadas.]_



6. Auditorias de Configuração
=============================
_[Descreva o cronograma das auditorias de configuração e o que será verificado. Informe também como serão reportados os problemas encontrados e onde sera feito o acompanhamento dos itens corretivos.]_

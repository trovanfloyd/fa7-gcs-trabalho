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

_[A introdução do Plano de Gerenciamento de Configuração  oferece uma visão geral de todo o documento. 
Ela inclui a finalidade, o escopo, as definições, os acrônimos, as abreviações, as referências e uma visão geral deste
Plano de Gerenciamento de Configuração.]_

1.1 Finalidade
---------------
_[Especifique a finalidade deste Plano de Gerenciamento de Configuração.]_

1.2 Escopo
----------
_[Uma breve descrição do escopo deste Plano de Gerenciamento de Configuração; o modelo ao qual ele está associado e tudo o que é afetado ou influenciado por este documento.]_

1.3 Definições, Acrônimos e Abreviações
---------------------------------------
_[Esta subseção apresenta as definições de todos os termos, acrônimos e abreviações necessários para a correta interpretação do Plano de Gerenciamento de Configuração.  Essas informações podem ser fornecidas mediante referência ao Glossário do projeto.]_

1.4 Referências
---------------
_[Esta subseção apresenta uma lista completa de todos os documentos mencionados no Plano de Gerenciamento de Configuração. Identifique os documentos por título, número de relatório (se aplicável), data e organização responsável pela publicação. Especifique as fontes a partir das quais as referências podem ser obtidas. Essas informações podem ser fornecidas por um anexo ou outro documento.]_

1.5 Visão Geral
---------------
_[Esta subseção descreve o conteúdo restante do Plano de Gerenciamento de Configuração e explica como o documento está organizado.]_



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
_[Regra de Formação de Nomes de Artefatos

Os nomes dos artefatos de um projeto devem seguir a regra:
<CÓDIGO_SISTEMA>_<MÓDULO SISTEMA>_<NOME_ARTEFATO>_<DETALHES>.EXT
Onde:

<CÓDIGO_SISTEMA>:
letra “S” seguida dos três números que compõem o código do sistema (OBRIGATÓRIO). Ex.: S344.
<MÓDULO_SISTEMA>:
nome do módulo do sistema com letras maiúsculas (OBRIGATÓRIO, apenas quando houver). Quando o nome do módulo for composto por mais de uma palavra, separá-las por undescore ( _ )
Ex.: S400_GRUPO_ECONOMICO.

<NOME_ARTEFATO>:
um conjunto de caracteres alfanuméricos, sendo a primeira letra de cada palavra maiúscula e as demais minúsculas (OBRIGATÓRIO), para os artefatos definidos no RUP-BNB. Os elementos de ligação como “de” e “do” devem ser suprimidos e deverá ser usado o undescore (_) para separar as palavras. Veja a nomenclatura de identificação dos artefatos na tabela 2.

<DETALHES>:
um conjunto de caracteres alfanuméricos, sendo a primeira letra de cada palavra maiúscula e as demais minúsculas (OPCIONAL). O detalhe pode conter uma descrição sobre o que trata o documento e as palavras devem ser separadas por undescore (_).Para artefatos que envolvam data em sua identificação, colocar a data invertida segundo o formato aaaammdd. No caso dos artefatos definidos na tabela 2, o detalhe deve conter o número e o nome do caso de uso.
EXT :
Extensão do arquivo que representa o artefato.]_

### 3.1.2 Itens de Configuração
_[Relacionar os artefatos ou grupos de artefatos, separando por tipo, modulo ou subsistema, responsável ou momento em que deverão ser incluídos em baselines._
* _“Inclusão em Baseline” em branco significa que o grupo de artefatos não participará de baseline. Pode ser expresso como uma data ou identificador de uma baseline, fase ou ponto de controle_
* _“Responsável”: indicar nominalmente, sempre que possível]_

| Item (ou Tipo de Item)                 | Responsável na equipe	     | Inclusão em Baseline |
|----------------------------------------|----------------------------- |----------------------|
|Especificação de requisitos             |Victor(Analista de Requisitos)|            Sim       |
|Plano do projeto                        |Hildo(Gerente do projeto)     |            Sim       |
|Documento de visão                      |Pedro(Estagiário)             |                      |

### 3.1.3 Baselines do Projeto

_[As baselines funcionam como um padrão oficial no qual os trabalhos subseqüentes são baseados. Somente mudanças autorizadas podem ser efetuadas nas baselines._

Baseline de Planejamento Composição
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


Baseline de Artefatos Composição
- Documento de Visão
- Declaração de Escopo
- Especificação Casos de Uso Em que momento é Gerada
A cada Homologação de artefato pelo Cliente. Desta forma, pode ser criada uma baseline para cada artefato homologado ou para um conjunto de artefatos homologados.


Baseline de Mudança Composição
Quaisquer itens que componham baseline e que precisem ser alterados.
Os itens de configuração que compõem Baseline somente poderão ser alterados mediante uma Solicitação de Mudança APROVADA na Ferramenta de Gestão de Projetos. Em que momento é Gerada
A cada alteração de itens de baseline.

Antes de ser criada, a baseline precisa ser aprovada pelo comitê de mudanças, composto pelo lider do projeto, gerente, arquiteto e do analista de testes.

### 3.1.4 Estrutura do Repositório de Versões
_[Os projetos deverão seguir a seguinte estrutura de pastas no repositóri:
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

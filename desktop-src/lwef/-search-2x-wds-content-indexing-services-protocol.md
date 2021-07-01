---
title: Protocolo de serviços de indexação de conteúdo
description: Este documento é uma especificação do Protocolo de Serviço de Indexação de Conteúdo.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14573dac5a7a6818234c086d05b52e5b81c2a1c1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119731"
---
# <a name="content-indexing-services-protocol"></a>Protocolo de serviços de indexação de conteúdo

> [!NOTE]
> O Windows Desktop Search 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

Especificação de protocolo, versão 0.12

-   [1 Introdução](#1-introduction)
    -   [1.1 Glossário](#11-glossary)
    -   [1.2 Referências](#12-references)
    -   [1.3 Visão geral do protocolo (Synopsis)](#13-protocol-overview-synopsis)
    -   [1.4 Relacionamento com outros protocolos](#14-relationship-to-other-protocols)
    -   [1.5 Pré-requisitos e pré-condições](#15-prerequisites-and-preconditions)
    -   [1.6 Applicability Statement](#16-applicability-statement)
    -   [1.7 Controle de versão e negociação de capacidade](#17-versioning-and-capability-negotiation)
    -   [1.8 Campos extensíveis para fornecedor](#18-vendor-extensible-fields)
    -   [1.9 Atribuições standard](#19-standards-assignments)
-   [2 Mensagens](#2-messages)
    -   [2.1 Transporte](#21-transport)
    -   [2.2 Sintaxe da mensagem](#22-message-syntax)
-   [3 Detalhes do protocolo](#3-protocol-details)
    -   [3.1 Detalhes do servidor](#31-server-details)
    -   [3.2 Detalhes do cliente](#32-client-details)
-   [4 Exemplos de protocolo](#4-protocol-examples)
    -   [4.1 Exemplo 1](#41-example-1)
    -   [4.2 Exemplo 2](#42-example-2)
-   [5 Segurança](#5-security)
    -   [5.1 Considerações de segurança para implementadores](#51-security-considerations-for-implementers)
    -   [5.2 Índice de parâmetros de segurança](#52-index-of-security-parameters)
-   [6 Índice de comportamento específico da versão](#6-index-of-version-specific-behavior)

Este documento é uma especificação do Protocolo de Serviço de Indexação de Conteúdo.

A documentação do WSPP (Workgroup Server Protocol Program) destina-se a ser usada em conjunto com a documentação de padrões públicos, a arte de programação de rede e os conceitos de sistemas distribuídos do grupo de trabalho do Windows e pressupo que o leitor está familiarizado com o material mencionado acima ou tem acesso imediato a ele.

Uma especificação de protocolo WSPP não exige o uso de ferramentas de programação da Microsoft ou ambientes de programação para que um licença desenvolva uma implementação. Os licenças que têm acesso a ambientes e ferramentas de programação da Microsoft são gratuitos para tirar proveito deles.

## <a name="1-introduction"></a>1 Introdução

-   [1.1 Glossário](#11-glossary)
-   [1.2 Referências](#12-references)
-   [1.3 Visão geral do protocolo (Synopsis)](#13-protocol-overview-synopsis)
-   [1.4 Relacionamento com outros protocolos](#14-relationship-to-other-protocols)
-   [1.5 Pré-requisitos e pré-condições](#15-prerequisites-and-preconditions)
-   [1.6 Applicability Statement](#16-applicability-statement)
-   [1.7 Controle de versão e negociação de capacidade](#17-versioning-and-capability-negotiation)
-   [1.8 Campos extensíveis para fornecedor](#18-vendor-extensible-fields)
-   [1.9 Atribuições standard](#19-standards-assignments)

### <a name="11-glossary"></a>1.1 Glossário

> [!Note]  
> Os seguintes termos são definidos na seção Glossário \[ do MS-SYS: \]
>
> -   GUID
> -   Little Endian
> -   Pipe nomeado
> -   Caminho

 

**Associação:** uma solicitação para incluir uma coluna **específica** em um conjuntos **de linhas retornado.** A **associação** especifica uma propriedade a ser incluída nos resultados da pesquisa.

**Indicador:** um marcador que identifica exclusivamente uma linha dentro de um conjunto de linhas.

**Catálogo:** a unidade de nível mais alto da organização no serviço de indexação. Ele representa um conjunto de documentos indexados nos quais as consultas podem ser executadas usando o Protocolo de Serviço de Indexação de Conteúdo.

**Categoria:** um grupo hierárquico de linhas. Por exemplo, um resultado de consulta que contém colunas de autor e título pode ser categorizado com base no autor. Cada grupo de linhas que contém o mesmo valor para autor constituiria uma categoria.

**Capítulo** : um intervalo **de linhas dentro** de um conjunto de **linhas** .

**Coluna**: o contêiner para um único tipo de informação em uma **linha** . As colunas são mapeadas para nomes de propriedade e  especificam quais propriedades são usadas para os elementos da árvore de comandos da consulta **de** pesquisa.

**Árvore de** Comandos: uma combinação de **restrições,** **categorias** e **ordens de classificação** especificadas para a consulta de pesquisa.

**Cursor**: uma entidade usada como um  mecanismo para trabalhar  com uma linha ou um pequeno bloco de linhas por vez em um conjunto de dados retornados em um conjunto de resultados. Um **cursor** é posicionado em uma única **linha dentro** do conjunto de resultados. Depois que **o cursor** é posicionado em uma linha, as operações podem ser **executadas** nessa linha **ou** em um bloco de linhas começando nessa posição.

**Identificador:** um token que pode ser usado para identificar e acessar **cursores** , **capítulos** e **indicadores** .

**Índice:** uma estrutura persistente que contém o conteúdo de texto retirado dos arquivos por um **serviço de indexação** . Isso inclui a lista de palavras, que são armazenadas junto com o nome do arquivo que contém, o local da palavra e **a localidade** .

**Indexação:** o processo de extrair texto e propriedades de arquivos e armazenar os valores extraídos nos índices **(para** texto) e o **cache** de propriedades (para propriedades).

**Serviço de Indexação:** um serviço que cria **catálogos indexados** para o conteúdo e as propriedades dos sistemas de arquivos. Os aplicativos podem pesquisar nos catálogos informações dos arquivos no sistema de arquivos indexado.

**Localidade :** um identificador, conforme especificado no \[ Apêndice A do MS-GPSI, que especifica as \] preferências relacionadas ao idioma. Essas preferências indicam como datas e horas devem ser formatadas, os itens devem ser ordenados em ordem alfabética, cadeias de caracteres devem ser comparadas e assim por diante.

**Consulta de linguagem natural:** uma consulta construída usando linguagem humana em vez da sintaxe de consulta.

**Palavra de** ruído: uma palavra ignorada pelo serviço  de indexação quando presente nas restrições especificadas para a consulta de pesquisa porque ela tem pouco valor discriminatório. Os exemplos em inglês incluem "a", "and" e "the".

**Cache de** propriedades: um cache de propriedades de arquivo extraídas por um **serviço de indexação** .

**Indexação de** propriedade: o  processo  de criação de um índice de propriedades de tipo de valor de um documento, incluindo autor, assunto, tipo, contagem de palavras, contagem de páginas impressas e qualquer outra propriedade.

**Restrição:** um conjunto de condições que um arquivo deve atender para ser incluído nos resultados da pesquisa retornados pelo serviço de **indexação** em resposta a uma consulta de pesquisa. Uma **restrição** restringe o foco de uma consulta de pesquisa, limitando os arquivos que o serviço de **indexação** incluirá nos resultados da pesquisa somente àqueles que corresponderem às condições.

**Linha**: a coleção de **colunas** , que contém os valores de propriedade  que descrevem um único arquivo do conjunto de arquivos que corresponderam às restrições especificadas na consulta de pesquisa enviada ao serviço **de indexação** .

**Conjunto de** linhas: um conjunto **de linhas retornado** nos resultados da pesquisa.

**Ordem de** Classificação: o conjunto de regras em uma consulta de pesquisa que define a ordenação de linhas no resultado da pesquisa. Cada regra consiste em uma propriedade (nome, tamanho etc.) e uma direção para a ordenação (crescente ou decrescente). Várias regras são aplicadas sequencialmente

**Propriedade de tipo de** texto: uma propriedade que descreve o conteúdo de um documento e tem apenas texto não formatado associado ao seu nome.

**Propriedade de tipo de** valor: uma propriedade que descreve um único atributo de um documento inteiro. Uma propriedade de tipo de valor tem uma ID de tipo de dados e um valor desse tipo de dados associado a seu nome.

**Raiz Virtual:** um caminho alternativo para uma pasta. Uma pasta física pode ter zero ou mais raízes virtuais. Os caminhos que começam com uma raiz virtual são chamados de caminhos virtuais. Por exemplo, /server/vanityroot pode ser uma raiz virtual de C: \\ pasta web do \\ IIS1. \\ Em seguida, o arquivo C: pasta web do IIS1default.htm teria um caminho \\ \\ virtual de \\ \\ /server/vanityroot/default.htm.

**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** esses termos (em todos os limites) são usados conforme descrito em \[ RFC2119 \] . Todas as instruções de comportamento opcional utilizam PODE, DEVERIA OU NÃO DEVERIA.

### <a name="12-references"></a>1.2 Referências

### <a name="121-normative-references"></a>1.2.1 Referências normativas

\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, outubro de 1985, https://standards.ieee.org/standard/754-1985.html

\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", junho de 2006.

\[MS-GPSI \] Microsoft Corporation, "extensão Política de Grupo de Instalação de Software", junho de 2006.

\[MS-SMB \] Microsoft Corporation, "Protocolo SMB (Bloco de Mensagens do Microsoft Server) e Extensões", maio de 2006.

\[MS-SYS \] Microsoft Corporation, "visão geral do sistema v4", julho de 2006.

\[Sale \] saltize, G., "processamento de texto automático: a análise de transformação e a recuperação de informações por computador", 1988, ISBN 0-201-2227-8.

\[UNICODE \] consórcio Unicode, "o padrão Unicode, versão 2,0", 1996, https://www.unicode.org

### <a name="122-informative-references"></a>1.2.2 Referências informativas

\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .

\[MSDN-QUERYERR \] Microsoft Corporation, valores de Query-Execution, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp

### <a name="13-protocol-overview-synopsis"></a>1,3 visão geral do protocolo (Sinopse)

Um **serviço de indexação** de conteúdo ajuda a organizar com eficiência os recursos extraídos de uma coleção de documentos. O CISP (Content Indexing Service Protocol) permite que um cliente se comunique com um servidor que hospeda um serviço de indexação para emitir consultas e permitir que um administrador gerencie o servidor de indexação.

Ao processar arquivos, um serviço de indexação analisa um conjunto de documentos e reorganiza seu conteúdo de forma que **as propriedades** desses documentos possam ser retornadas de forma eficiente em resposta a consultas. Uma coleção de documentos que podem ser consultados abrange um **Catálogo** . Um catálogo pode conter um **índice** (para referência rápida a texto) e um **cache de propriedades** (para recuperação rápida de valores de propriedade).

Conceitualmente, um catálogo consiste em uma "tabela" lógica de propriedades com o texto ou o valor e a localidade correspondente armazenada em **colunas** da tabela. Cada "linha" da tabela corresponde a um documento separado no escopo do catálogo e cada "coluna" da tabela corresponde a uma propriedade.

As tarefas específicas executadas pelo CISP são agrupadas em duas áreas funcionais:

-   Administração remota da indexação de catálogos de serviço,
-   Consulta remota de catálogos de serviço de indexação.

### <a name="131-remote-administration-tasks"></a>Tarefas de administração remota do 1.3.1

O CISP habilita as seguintes tarefas de gerenciamento de catálogo do serviço de indexação de um cliente:

-   Consulte o estado atual de um catálogo de serviço de indexação no servidor.
-   Atualize o estado de um catálogo de serviço de indexação.
-   Inicie o processo de indexação para um determinado conjunto de arquivos.
-   Inicie a otimização de um índice para melhorar o desempenho da consulta.

Todas as tarefas de administração remota seguem um modelo simples de solicitação/resposta. Nenhum estado é mantido no cliente para qualquer chamada de administração e chamadas administrativas podem ser feitas em qualquer ordem.

### <a name="132-remote-querying"></a>Consulta remota 1.3.2

O CISP permite que os clientes executem consultas de pesquisa em um servidor remoto que hospeda um serviço de indexação.

O envio de uma consulta de pesquisa é um processo de várias etapas iniciado pelo cliente. As etapas são as seguintes:

1.  O cliente solicita uma conexão a um servidor que hospeda um serviço de indexação.
2.  O cliente envia os parâmetros para a consulta de pesquisa, que incluem:
    -   As **restrições** para especificar quais documentos devem ser incluídos e/ou excluídos dos resultados da pesquisa.
    -   A ordem na qual os resultados da pesquisa devem ser retornados.
    -   As colunas a serem retornadas no conjunto de resultados.
    -   O número máximo de **linhas** que devem ser retornadas para a consulta.
    -   O tempo máximo para a execução da consulta.

        Depois que o servidor tiver confirmado a solicitação do cliente para iniciar a consulta, o cliente poderá solicitar informações de status sobre a consulta, mas essa não é uma etapa necessária.

3.  O cliente especifica quais propriedades o servidor deve incluir nos resultados da pesquisa.
4.  O cliente solicita um conjunto de resultados do servidor e o servidor responde enviando ao cliente os valores de propriedade dos arquivos que foram incluídos nos resultados para a consulta de pesquisa do cliente. Se o valor de uma propriedade for muito grande para caber em um único buffer de resposta, o servidor não enviará a propriedade, mas, em vez disso, definirá o status da propriedade como adiada. Em seguida, o cliente solicita o valor da propriedade separadamente usando uma série de solicitações para partes sucessivas do valor e, em seguida, retoma a solicitação de outros valores.
5.  Depois que o cliente for concluído com a consulta de pesquisa e não exigir mais resultados adicionais, o cliente entrará em contato com o servidor para liberar a consulta.
6.  Depois que o servidor tiver lançado a consulta, o cliente poderá enviar uma solicitação para desconectar-se do servidor. A conexão é fechada. Como alternativa, o cliente pode emitir outra consulta e repetir a sequência da etapa 2.

Comportamento do Windows: esse protocolo é implementado no Windows 2000, no Windows XP, no Windows Server 2003 e no Windows Vista.

### <a name="14-relationship-to-other-protocols"></a>1.4 Relacionamento com outros protocolos

O CISP se baseia no protocolo SMB \[ MS-SMB \] para transporte de mensagens. Nenhum outro protocolo depende diretamente do protocolo de serviço de indexação de conteúdo.

*Comportamento do Windows: normalmente, os aplicativos interagem com um wrapper de interface OLE DB \[ msdn-OLEDB \] (por exemplo, um cliente de protocolo) e não diretamente com o protocolo.*

### <a name="15-prerequisites-and-preconditions"></a>1,5 pré-requisitos e pré-condições

Supõe-se que o cliente tenha obtido o nome do servidor e um nome de catálogo antes que esse protocolo seja invocado. Como um cliente faz isso está fora do escopo desta especificação.

Também pressupõe-se que o cliente e o servidor tenham uma associação de segurança utilizável com pipes nomeados \[ MS-SMB \] .

### <a name="16-applicability-statement"></a>1.6 Applicability Statement

O CISP é projetado para consultar e gerenciar catálogos em um servidor remoto a partir de um cliente. O CISP foi preterido no Windows Vista.

### <a name="17-versioning-and-capability-negotiation"></a>1.7 Controle de versão e negociação de capacidade

Esse protocolo não possui controle de versão ou mecanismos de negociação de capacidade.

### <a name="18-vendor-extensible-fields"></a>1.8 Campos extensíveis para fornecedor

Esse protocolo usa HRESULTs que são extensíveis pelo fornecedor. Os fornecedores são livres para escolher seus próprios valores para esse campo, desde que o C bit (0x20000000) esteja definido conforme especificado na seção 4.1.1 do \[ MS-sys \] , indicando que ele é um código de cliente.

Esse protocolo também usa valores de NTSTATUS obtidos do espaço de número NTSTATUS definido em \[ MS-sys \] . Os fornecedores devem reutilizar esses valores com o significado indicado. Escolher qualquer outro valor executará o risco de uma colisão no futuro.

*Comportamento do Windows: o Windows usa apenas os valores especificados na seção 4.1.3 do \[ MS-sys \] .*

### <a name="181-property-ids"></a>IDs da propriedade 1.8.1

As propriedades são representadas por IDs conhecidas como IDs de propriedade. Cada propriedade deve ter um identificador global exclusivo. Esse identificador consiste em um **GUID** que representa uma coleção de propriedades chamada um conjunto de propriedades, além de uma cadeia de caracteres ou um inteiro de 32 bits para identificar a propriedade dentro do conjunto. Se o formulário inteiro da ID for usado, os valores 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE serão considerados inválidos.

Os fornecedores podem garantir que suas propriedades sejam definidas exclusivamente colocando-as em um conjunto de propriedades definido por seu próprio GUID.

### <a name="19-standards-assignments"></a>1.9 Atribuições standard

Esse protocolo não tem nenhuma atribuição de padrões, somente atribuições privadas feitas pela Microsoft usando os procedimentos de alocação especificados em outros protocolos.

A Microsoft alocou esse protocolo como um pipe nomeado, conforme especificado em \[ MS-SMB \] . A atribuição é:



| Parâmetro | Valor             | Referência  |
|-----------|-------------------|------------|
| Nome do pipe | \\\\SKADS de CI de pipe \_ | \[MS-SMB\] |



 

## <a name="2-messages"></a>2 Mensagens

-   [2.1 Transporte](#21-transport)
-   [2.2 Sintaxe da mensagem](#22-message-syntax)

### <a name="21-transport"></a>2.1 Transporte

Todas as mensagens devem ser transportadas usando um pipe nomeado, conforme especificado em \[ MS-SMB \] . O seguinte nome de pipe é usado:

-   \\\\SKADS de CI de pipe \_

Esse protocolo usa o protocolo de pipe nomeado SMB subjacente para recuperar a identidade do chamador que fez a conexão, conforme especificado na seção 2.2.8 do \[ MS-SMB \] ; o cliente deve definir a identificação de segurança \_ como o ImpersonationLevel na solicitação para abrir o pipe nomeado.

### <a name="22-message-syntax"></a>2.2 Sintaxe da mensagem

Várias estruturas e mensagens nas seções a seguir referem-se aos identificadores de capítulo ou indicador. Um identificador é uma estrutura opaca de longa de 32 bits que identifica exclusivamente um capítulo ou indicador. Normalmente, os aplicativos cliente recebem valores de identificador por meio de chamadas de método; no entanto, há vários valores bem conhecidos que não precisam ser obtidos de um servidor, o significado do que é especificado na tabela a seguir:



| Valor                         | Significado                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| DB \_ NULL \_ HCHAPTER 0x00000000 | Um capítulo manipula o conjunto de linhas sem capítulos, que contém todos os resultados da consulta.    |
| DBBMK \_ primeiro 0x00000001       | Um identificador de indicador para um indicador que identifica a primeira linha no conjunto de linhas. |
| DBBMK \_ último 0x00000002        | Um identificador de indicador para um indicador que identifica a última linha no conjunto de linhas.  |



 

### <a name="221-structures"></a>estruturas 2.2.1

Esta seção detalha as estruturas de dados que são definidas e usadas pelo CISP.

Todos os inteiros de 2, 4 e 8 bytes assinados e não assinados nas seguintes estruturas devem ser transferidos em ordem de byte little-endian.

A tabela a seguir resume as estruturas de dados definidas nesta seção.



| Estrutura                    | Descrição                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| CBaseStorageVariant          | Contém o valor no qual executar uma operação de correspondência para uma propriedade especificada em uma estrutura CPropertyRestriction. |
| SAFEARRAY, SAFEARRAY2        | Contém uma matriz multidimensional.                                                                                     |
| SAFEARRAYBOUND               | Representa os limites de uma dimensão de uma matriz especificada em uma estrutura SAFEARRAY.                                  |
| CFullPropSpec                | Contém uma especificação de propriedade.                                                                                     |
| CContentRestriction          | Contém uma cadeia de caracteres para corresponder a um valor de propriedade no cache de propriedades.                                                 |
| CKey                         | Contém um valor de propriedade.                                                                                             |
| CInternalPropertyRestriction | Contém um valor de propriedade para corresponder a uma operação.                                                                  |
| CNatLanguageRestriction      | Contém uma correspondência de consulta de idioma natural para uma propriedade.                                                                |
| CNodeRestriction             | Contém uma matriz de nós de árvore de comando especificando as restrições para uma consulta.                                       |
| COccRestriction              | Contém o local de uma palavra em uma frase.                                                                           |
| CPropertyRestriction         | Contém um valor de propriedade para corresponder a uma operação.                                                                  |
| CRangeRestriction            | Contém uma restrição em um intervalo de valores.                                                                           |
| CScopeRestriction            | Contém uma restrição sobre os arquivos a serem pesquisados.                                                                    |
| CSort                        | Identifica uma coluna a ser classificada.                                                                                           |
| CSynRestriction              | Contém uma palavra ou seus sinônimos para uma frase de consulta.                                                                    |
| CVectorRestriction           | Contém uma operação ponderada ou em um nó de árvore de comandos.                                                               |
| CWordRestriction             | Contém uma palavra para uma frase de consulta.                                                                                    |
| CRestriction                 | Contém um nó de uma árvore de comando de consulta.                                                                               |
| CColumnSet                   | Indica o número de colunas a serem retornadas.                                                                             |
| CCategorizationSet           | Contém informações sobre o agrupamento de um conjunto de resultados de consulta.                                                     |
| CCategorizationSpec          | Contém uma definição de categorias nas quais os resultados da consulta serão categorizados.                                      |
| CDbColId                     | Contém uma coluna.                                                                                                     |
| CDbProp                      | Contém uma propriedade.                                                                                                   |
| CDbPropSet                   | Contém um conjunto de propriedades.                                                                                          |
| CPidMapper                   | Contém uma matriz de IDs de propriedade especificando as propriedades a serem retornadas em um conjunto de linhas.                                     |
| CRowSeekAt                   | Contém o deslocamento no qual recuperar linhas em uma mensagem CPMGetRowsIn                                                |
| CRowSeekAtRatio              | Identifica o ponto no qual iniciar a recuperação para uma mensagem CPMGetRowsIn.                                           |
| CRowSeekByBookmark           | Identifica os indicadores dos quais recuperar linhas para uma mensagem CPMGetRowsIn.                                       |
| CRowSeekNext                 | Contém o número de linhas a serem ignoradas em uma mensagem CPMGetRowsIn.                                                         |
| CRowsetProperties            | Contém as informações de configuração de uma consulta.                                                                    |
| CSortSet                     | Contém a ordem de classificação para uma consulta.                                                                                   |
| CTableColumn                 | Contém uma coluna para a mensagem CPMSetBindings.                                                                      |
| SERIALIZEDPROPERTYVALUE      | Contém um valor serializado.                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a>2.2.1.1 CBaseStorageVariant

A estrutura CBaseStorageVariant contém o valor no qual executar uma operação de correspondência para uma propriedade especificada na estrutura CPropertyRestriction.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

vData1

vData2

vValue (variável)



 

**vType:** um indicador de tipo que indica o tipo de vValue. Ele DEVE ser um dos valores VARENUM especificados na tabela a seguir.



| Valor                 | Significado                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY (0x0000)    | vValue não está presente.                                                                                                               |
| VT \_ NULL (0x0001)     | vValue não está presente.                                                                                                               |
| VT \_ I1 (0x0010)       | Um inteiro de um byte com sinal.                                                                                                             |
| VT \_ UI1 (0x0011)      | Um inteiro de um byte sem sinal.                                                                                                           |
| VT \_ I2 (0x0002)       | Um inteiro de dois bytes com sinal.                                                                                                             |
| VT \_ UI2 (0x0012)      | Um inteiro de dois bytes sem sinal.                                                                                                           |
| VT \_ BOOL (0x000B)     | Um valor booliana; um inteiro de 2 byte que contém 0x0000 (FALSE) ou 0xFFFF (TRUE).                                                        |
| VT \_ I4 (0x0003)       | Um inteiro de quatro bytes com sinal.                                                                                                             |
| VT \_ UI4 (0x0013)      | Um inteiro de quatro bytes sem sinal.                                                                                                           |
| VT \_ R4 (0x0004)       | Um número de ponto flutuante IEEE de 32 bits, conforme definido em \[ IEEE754. \]                                                                     |
| VT \_ INT (0x0016)      | Um inteiro de quatro bytes com sinal.                                                                                                             |
| VT \_ UINT (0x0017)     | Um inteiro de quatro bytes sem sinal.                                                                                                           |
| ERRO de VT \_ (0x000A)    | Um inteiro sem sinal de 4 byte que contém um HRESULT, conforme especificado em \[ MS-SYS \] .                                                         |
| VT \_ I8 (0x0014)       | Um inteiro com sinal de 8 byte.                                                                                                            |
| VT \_ UI8 (0x0015)      | Um inteiro de oito bytes sem sinal.                                                                                                          |
| VT \_ R8 (0x0005)       | Um número de ponto flutuante IEEE de 64 bits conforme definido em \[ IEEE754. \]                                                                      |
| VT \_ CY (0x0006)       | Um inteiro de complemento de dois de 8 byte (dimensionado em 10.000).                                                                               |
| DATA DA VT \_ (0x0007)     | Um número de ponto flutuante de 64 bits que representa o número de dias desde 00:00:00 em 31 de dezembro de 1899 (Tempo Universal Coordenado).     |
| VT \_ FILETIME (0x0040) | Um inteiro de 64 bits que representa o número de intervalos de 100 nanossegundos desde 00:00:00 em 1º de janeiro de 1601 (Tempo Universal Coordenado). |
| DECIMAL da VT \_ (0x000E)  | Uma estrutura DECIMAL, conforme especificado na seção 2.2.1.1.1.1.                                                                             |
| CLSID da VT \_ (0x0048)    | Um valor binário de 16 byte que contém um GUID.                                                                                            |
| BLOB de VT \_ (0x0041)     | Uma contagem de inteiros sem sinal de 4 bytes no blob, seguida por muitos bytes de dados.                                           |
| VT \_ BSTR (0x0008)     | Uma contagem de inteiros sem sinal de 4 bytes na cadeia de caracteres, seguida por uma cadeia de caracteres, conforme especificado abaixo em vValue.                       |
| VT \_ LPSTR (0x001E)    | Uma cadeia de caracteres ANSI terminada em nulo.                                                                                                       |
| VT \_ LPWSTR (0x001F)   | Uma cadeia de caracteres UNICODE Unicode terminada \[ em \] nulo.                                                                                        |
| VT \_ VARIANT (0x000C)  | CBaseStorageVariant. DEVE ser combinado com um modificador de tipo de VT \_ ARRAY ou VT \_ VECTOR.                                               |



 

A tabela a seguir especifica os modificadores de tipo para vType. Os modificadores de tipo podem ser binários ORed com vType, para alterar o significado de vValue para indicar que ele é um dos dois tipos de matriz possíveis.



| Valor               | Significado                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ VECTOR (0x1000) | Se o indicador de tipo for combinado com vT VECTOR usando um operador OR, vValue será uma matriz contada de valores \_ do tipo indicado. Consulte a seção 2.2.1.1.1.2 para obter detalhes. <br/> Esse modificador de tipo NÃO DEVE ser combinado com os seguintes tipos: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, \_ VT BLOB, OBJETO \_ BLOB \_ VT.<br/>                                    |
| MATRIZ VT \_ (0x2000)  | Se o indicador de tipo for combinado com VT ARRAY por um operador OR, o valor será um SAFEARRAY (conforme especificado na seção \_ 2.2.1.1.1.3) que contém valores do tipo indicado. <br/> Esse modificador de tipo NÃO DEVE ser combinado com os seguintes tipos: VT \_ I8, VT \_ UI8, VT \_ FILETIME, \_ CLSID VT, \_ BLOB VT, OBJETO \_ DE BLOB \_ VT, VT \_ LPSTR, VT \_ LPWSTR. <br/> |



 

**vData1:** quando vType é VT DECIMAL, o valor desse campo é especificado como o campo Escala na \_ seção 2.2.1.1.1.1. Para todos os outros vTypes, o valor DEVE ser definido como 0x00.

**vData2:** quando vType é VT DECIMAL, o valor desse campo é especificado como o campo Entrar na \_ seção 2.2.1.1.1.1. Para todos os outros vTypes, o valor DEVE ser definido como 0x00.

**vValue:** o valor da operação de match. A sintaxe DEVE ser conforme indicado no campo vType.

A tabela a seguir resume os tamanhos do campo vValue, dependendo do campo vType para tipos de dados de comprimento fixo. O tamanho é em bytes.



| vType                                                   | Tamanho |
|---------------------------------------------------------|------|
| VT \_ I1, VT, \_ UI1                                        | 1    |
| VT \_ I2, VT \_ UI2, VT \_ BOOL                               | 2    |
| VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, ERRO de VT \_   | 4    |
| VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME | 8    |
| VT \_ DECIMAL, \_ CLSID da VT                                  | 16   |



 

Se vType for definido como \_ VT BLOB, VT BSTR ou VT LPSTR, a estrutura de vValue será \_ especificada no diagrama a \_ seguir:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbSize

blobData (variável, opcional)



 

**cbSize:** inteiro de 32 bits sem sinal, indicando o tamanho do campo blobData em bytes. Se vType for definido como VT BSTR ou \_ VT LPSTR, cbSize DEVERÁ ser definido como 0x00000000 quando a cadeia de caracteres representada for uma cadeia de caracteres \_ vazia.

**blobData:** DEVE ser de comprimento cbSize em bytes.

Para vType definido como BLOB de \_ VT, esse campo são dados de blob binário opacos.

Para vType definido como VT BSTR, esse campo é um conjunto de caracteres em um \_ conjunto de caracteres selecionado por OEM. O cliente e o servidor DEVEM ser configurados para ter conjuntos de caracteres interoperáveis (fora da banda do protocolo). Não há nenhum requisito de que ela seja terminada em nulo.

Para vType definido como VT LPSTR, esse campo é uma cadeia de caracteres terminada em nulo em um conjunto de caracteres selecionado \_ OEM. O cliente e o servidor DEVEM ser configurados para ter conjuntos de caracteres interoperáveis (fora da banda do protocolo).

Se vType for definido como VT \_ LPWSTR, a estrutura de vValue será especificada no diagrama a seguir:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

ccLen

cadeia de caracteres (variável, opcional)



 

**ccLen:** inteiro de 32 bits sem sinal, indicando o tamanho do campo de cadeia de caracteres em caracteres Unicode. DEVE ser definido como 0x00000000 para uma cadeia de caracteres vazia.

**cadeia** de caracteres : cadeia de caracteres Unicode terminada em nulo.

### <a name="22111-cbasestoragevariant-structures"></a>2.2.1.1.1 Estruturas CBaseStorageVariant

As estruturas a seguir são usadas na estrutura CBaseStorageVariant.

### <a name="221111-decimal"></a>2.2.1.1.1.1 DECIMAL

DECIMAL é usado para representar um valor numérico exato com uma precisão fixa e uma escala fixa.

Quando vType é definido como VT DECIMAL (0x0000E), os campos \_ vData1 e vData2 de CBaseStorageVariant DEVEM ser interpretados da seguinte maneira:

**vData1:** o número de dígitos à direita do ponto decimal. DEVE estar no intervalo de 0 a 28.

**vData2:** o sinal do valor numérico. Definido como 0x00 se for positivo, 0x80 se for negativo.

O formato do campo vValue é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Hi32

Lo32

Mid32



 

**Hi32**: os mais de 32 bits do número inteiro de 96 bits.

**Lo32**: os mais baixos 32 bits do número inteiro de 96 bits.

**Mid32**: os bits do meio 32 do número inteiro de 96 bits.

### <a name="221112-vt_vector"></a>vetor VT 2.2.1.1.1.2 \_

O \_ vetor VT é usado para passar matrizes unidimensionais.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vVectorElements

vVectorData



 

**vVectorElements**: inteiro de 32 bits sem sinal, indicando o número de elementos no campo vVectorData.

**vVectorData**: uma matriz de itens que têm um tipo indicado por vType com o bit 0x1000 limpo. O tamanho de um item de comprimento fixo individual pode ser obtido da tabela de tipos de dados de comprimento fixo, conforme especificado na seção 2.2.1.1. O comprimento desse campo, em bytes, pode ser calculado multiplicando vVectorElements pelo tamanho de um item individual.

Para tipos de dados de comprimento variável, vVectorData contém uma sequência de tipos simples com marshaling consecutivo em que o tipo é indicado por vType com o bit 0x1000 limpo. Isso inclui um caso especial indicado pela variante da \_ matriz \| VT vType VT \_ (ou seja, 0x100C).

Os elementos no campo vVectorData devem ser separados por 0 a 3 bytes de preenchimento, de modo que cada elemento comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa matriz. Se os bytes de preenchimento estiverem presentes, o valor que eles contêm será arbitrário. O conteúdo dos bytes de preenchimento deve ser ignorado pelo destinatário.

Para um vType definido como \_ variante de matriz VT de VT \| \_ , o tipo de itens nesta sequência é CBaseStorageVariant.

### <a name="221113-safearray"></a>2.2.1.1.1.3 SAFEARRAY

SAFEARRAY é usado para passar matrizes multidimensionais. A estrutura contém informações de tamanho de matriz, bem como os dados na matriz.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

fFeatures

cbElements

Rgsabound (variável)

vData (variável)



 

**cDims**: inteiro de 16 bits não assinado, indicando o número de dimensões da matriz multidimensional.

**fFeatures**: um tele-bit de 16 bits. Os valores representam recursos, definidos por aplicativos de camada superior e devem ser ignorados.

**cbElements**: um inteiro de 32 bits sem sinal especificando o tamanho de cada elemento da matriz.

**Rgsabound**: uma matriz que contém uma estrutura SAFEARRAYBOUND, conforme especificado na seção 2.2.1.1.1.4, por dimensão em SafeArray. Essa matriz tem a dimensão mais à esquerda primeiro e a dimensão mais à direita por último.

**vData**: um vetor de itens empacotados de um tipo específico, indicado pelo VType do CBaseStorageVariant que o contém, com o bit 0x2000 limpo.

o vData é empacotado de forma semelhante ao \_ vetor VT, conforme especificado na seção 2.2.1.1.1.2, com a diferença de que o número de itens não é armazenado na frente do vetor. Em vez disso, o número de itens é calculado multiplicando-se o valor cElements por todos os limites de matrizes seguros fornecidos no campo rgsabound. Os elementos são armazenados em um vetor em ordem de dimensões, iterando começando com a dimensão mais à direita.

O diagrama a seguir representa visualmente uma matriz bidimensional de exemplo. A primeira dimensão tem cElements igual a 4 (representada horizontalmente) e lLbound igual a 0, e a segunda dimensão tem cElements igual a 2 (representada verticalmente) e lLbound igual a 0.

:::row:::
    :::column:::
        0x00000001
    :::column-end:::
    :::column:::
        0x00000002
    :::column-end:::
    :::column:::
        0x00000003
    :::column-end:::
    :::column:::
        0x00000005
    :::column-end:::
:::row-end:::

:: Row:::
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

Usando o diagrama acima, vData conterá a seguinte sequência: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (Iterando primeiro pela dimensão mais à direita e, em seguida, incrementando a próxima dimensão). O rgsabound anterior (que registra cElements e LBound) seria: 0x00000004, 0x00000000, 0x00000002, 0x00000000.

### <a name="221114-safearraybound"></a>2.2.1.1.1.4 SAFEARRAYBOUND

A estrutura SAFEARRAYBOUND representa os limites de uma dimensão de um SAFEARRAY ou SAFEARRAY2. Seu formato é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cElements

lLbound



 

**cElements**: um inteiro sem sinal de 32 bits, especificando o número de elementos na dimensão.

**lLbound**: um inteiro sem sinal de 32 bits, especificando o limite inferior da dimensão.

### <a name="221115-safearray2"></a>2.2.1.1.1.5 SAFEARRAY2

SAFEARRAY2 é usado para passar matrizes multidimensionais em SERIALIZEDPROPERTYVALUE. A estrutura contém informações de limite, bem como os dados.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

Rgsabound (variável)

vData (variável)



 

**cDims:** inteiro de 32 bits sem sinal, indicando o número de dimensões do SAFEARRAY2.

**Rgsabound:** uma matriz que contém uma estrutura SAFEARRAYBOUND, conforme especificado na seção 2.2.1.1.1.4 por dimensão em SAFEARRAY2. Essa matriz tem a dimensão mais à esquerda primeiro e a dimensão mais à direita por último.

**vData:** um vetor de itens com marshaling de um tipo específico, indicado pelo dwType do que contém SERIALIZEDPROPERTYVALUE, com o bit 0x2000 limpo. O formato de vData igual ao especificado para o campo vData de SAFEARRAY na Seção 2.2.1.1.1.3.

### <a name="2212-cfullpropspec"></a>2.2.1.2 CFullPropSpec

A estrutura CFullPropSpec contém um GUID do conjunto de propriedades e um identificador de propriedade para identificar exclusivamente a propriedade.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_guidPropSet

...

...

...

ulKind

PrSpec

Nome da propriedade (variável)



 

**\_ guidPropSet:** o GUID do conjunto de propriedades ao qual a propriedade pertence.

**ulKind:** um inteiro sem sinal de 32 bits. Um dos seguintes valores abaixo, que indica o conteúdo de PrSpec.



| Valor                                            | Significado                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| PRSPEC \_ LPWSTR<br/> 0x00000000<br/> | O campo PrSpec especifica o número de caracteres não NULL no campo Nome da propriedade. |
| PRSPEC \_ PROPID<br/> 0x00000001<br/>  | O campo PrSpec especifica a ID da propriedade (PROPID).                                     |



 

**PrSpec:** um inteiro sem sinal de 32 bits com um significado conforme indicado pelo campo ulKind.

**Nome da** propriedade: se ulKind for definido como PRSPEC \_ PROPID, esse campo NÃO DEVERÁ estar presente. Se ulKind for definido como PRSPEC LPWSTR, esse campo DEVERÁ conter uma matriz de caracteres Unicode não nulos PrSpec, contendo o nome da \_ propriedade.

### <a name="2213-ccontentrestriction"></a>2.2.1.3 CContentRestriction

A estrutura CContentRestriction contém uma cadeia de caracteres para corresponder a uma propriedade no cache de propriedades.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Propriedade (variável)

...

Padding1 (variável)

Cc

\_pwcsPhrase (variável)

...

Padding2 (variável)

lcid

\_ulGenerateMethod



 

**\_ Propriedade**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.2. Este campo indica a propriedade na qual executar uma operação de correspondência.

**Padding1**: esse campo deve ter de 0 a 3 bytes de comprimento. O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura. Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário. O conteúdo deste campo deve ser ignorado pelo destinatário.

**CC**: um inteiro de 32 bits sem sinal, especificando o número de caracteres no \_ campo pwcsPhrase.

**\_ pwcsPhrase**: uma cadeia de caracteres Unicode não terminada em nulo que representa a palavra ou frase para corresponder à propriedade. Este campo não deve estar vazio. O campo Cc contém o comprimento da cadeia de caracteres.

**Padding2**: esse campo deve ter de 0 a 3 bytes de comprimento. O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura. Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário. O conteúdo deste campo deve ser ignorado pelo destinatário.

**LCID**: um inteiro sem sinal de 32 bits, indicando a localidade de \_ pwcsPhrase, conforme especificado em \[ MS-GPSI \] Apêndice A.

**\_ ulGenerateMethod**: um inteiro sem sinal de 32 bits, especificando o método a ser usado ao gerar formulários alternativos de palavra



| Valor                                                       | Significado                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GERAR \_ método \_ exato<br/> 0x00000000<br/>    | Correspondência exata.                                                                                                                                                                                                                                                                                      |
| GERAR \_ prefixo de método \_<br/> 0x00000001 <br/>  | Correspondência de prefixo.                                                                                                                                                                                                                                                                                     |
| GERAR \_ método \_ INFLECT <br/> 0x00000002<br/> | Faz a correspondência de inflexões de uma palavra. Uma inflexão de uma palavra é uma variante da palavra raiz na mesma parte da fala que foi modificada de acordo com as regras linguísticas de um determinado idioma. Por exemplo, as inflexidades do verbo "nada" em inglês incluem "nada", "nada", "nada" e "Swam". |



 

### <a name="2214-ckey"></a>2.2.1.4 CKey

A estrutura CKey contém um valor de propriedade.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Propid

Cb

buf (variável)



 

**PROPID:** um inteiro sem sinal de 32 bits, que representa a ID da propriedade, conforme discutido na seção 1.8.1. Os valores conhecidos são:



| Valor      | Significado                                                 |
|------------|---------------------------------------------------------|
| 0xFFFFFFFF | Representa uma ID de propriedade inválida e NÃO DEVE ser usado. |
| 0xFFFFFFFE | Representa uma ID de propriedade inválida e NÃO DEVE ser usado. |
| 0x00000000 | Representa qualquer ID de propriedade.                             |



 

**Cb:** um inteiro sem sinal de 32 bits que contém o comprimento de buf, em bytes.

**buf**: uma sequência de bytes que representa o valor da propriedade .

### <a name="2215-cinternalpropertyrestriction"></a>2.2.1.5 CInternalPropertyRestriction

A estrutura CInternalPropertyRestriction contém um valor da propriedade para corresponder a uma operação.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_reope

\_Pid

\_prval (variável)

restrictionPresent

nextRestriction (variável)



 

**\_ reope:** um inteiro de 32 bits que especifica a relação a ser executar na propriedade . DEVE ser um dos seguintes valores:



| Valor                 | Significado                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PrLT 0x00000000       | Uma comparação menor que.                                                                                           |
| PRLE 0x00000001       | Uma comparação menor ou igual a.                                                                               |
| PRGT 0x00000002       | Uma comparação maior que.                                                                                        |
| PrGE 0x00000003       | Uma comparação maior ou igual a.                                                                            |
| PREQ 0x00000004       | Uma comparação de igualdade.                                                                                           |
| PRNE 0x00000005       | Uma comparação não igual.                                                                                           |
| PRRE 0x00000006       | Uma comparação de expressão regular.                                                                                  |
| PRAllBits 0x00000007  | Um AND bit a bit que retorna o operand direito.                                                                     |
| PRSomeBits 0x00000008 | Um AND bit a bit que retorna um valor diferente de zero.                                                                       |
| PRAll 0x00000100      | A operação deve ser executada em uma coluna de um conjuntos de linhas e só será verdadeira se a operação for verdadeira para todas as linhas. |
| PrAny 0x00000200      | A operação deve ser executada em uma coluna de um conjuntos de linhas e será verdadeira se a operação for verdadeira para qualquer linha.       |



 

**\_ pid:** um inteiro sem sinal de 32 bits, que representa a ID da propriedade (consulte PROPID na seção 2.2.1.4).

**\_ prval:** um CBaseStorageVariant que contém o valor a ser relacionado à propriedade .

**restrictionPresent:** um valor de byte que indica se o campo nextRestriction está presente. DEVE ser definido como 0x00 ou 0x01. Se definido como 0x01, restrictionPresent indica que o campo nextRestriction está presente. Se definido como 0x00, restrictionPresent indica que o campo nextRestriction não está presente.

**nextRestriction:** uma estrutura CRestriction, conforme especificado na seção 2.2.1.16, especificando uma restrição posterior.

### <a name="2216-cnatlanguagerestriction"></a>2.2.1.6 CNatLanguageRestriction

A estrutura CNatLanguageRestriction contém uma combinação de consulta **de idioma natural** para uma propriedade .



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Propriedade (variável)

...

\_preenchimento \_ de CC (variável)

Cc

\_pwcsPhrase (variável)

...

\_\_LCID de preenchimento (variável)

Lcid



 

**\_ Propriedade**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.3. Este campo indica a propriedade na qual executar a operação de correspondência.

**\_ preenchimento \_ CC**: esse campo deve ter de 0 a 3 bytes de comprimento. O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura. Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário. O conteúdo deste campo deve ser ignorado pelo destinatário.

**CC**: um inteiro de 32 bits sem sinal. O número de caracteres no \_ campo pwcsPhrase.

**\_ pwcsPhrase**: uma cadeia de caracteres Unicode não terminada em nulo que representa a palavra ou frase para corresponder à propriedade. Não deve ficar vazio. O campo Cc contém o comprimento da cadeia de caracteres.

**\_ \_ LCID de preenchimento**: esse campo deve ter de 0 a 3 bytes de comprimento. O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura. Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário. O conteúdo deste campo deve ser ignorado pelo destinatário.

**LCID**: um inteiro de 32 bits sem sinal indicando a localidade de \_ pwcsPhrase, conforme especificado no \[ Apêndice a do MS-GPSI \] .

### <a name="2217-cnoderestriction"></a>2.2.1.7 CNodeRestriction

A estrutura CNodeRestriction contém uma matriz de nós de **árvore de comando** que especificam as restrições para a consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cNode

\_paNode (variável)



 

**\_ cNode**: um inteiro sem sinal de 32 bits especificando o número de estruturas CRestriction contidas no \_ campo paNode.

**\_ paNode**: uma matriz de estruturas CRestriction. As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa matriz. Se os bytes de preenchimento estiverem presentes, o valor que eles contêm será arbitrário. O conteúdo dos bytes de preenchimento deve ser ignorado pelo destinatário.

### <a name="2218-coccrestriction"></a>2.2.1.8 COccRestriction

A estrutura COccRestriction contém o local de uma palavra em uma frase.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Occ

\_cPrevNoiseWords

\_cNextNoiseWords



 

**\_ occ:** um inteiro sem sinal de 32 bits que especifica o deslocamento da palavra em uma cadeia de caracteres de consulta, em unidades de palavras. Uma palavra, conforme usada nesta especificação, é uma unidade de linguagem em qualquer localidade que tem significado.

**\_ cPrevNoiseWords:** um inteiro sem sinal de 32  bits que contém o número de palavras de ruído que ocorrem entre essa palavra e a palavra anterior na frase.

**\_ cNextNoiseWords:** um inteiro sem sinal de 32 bits que contém o número de palavras de ruído que ocorrem entre essa palavra e a próxima palavra na frase.

### <a name="2219-cpropertyrestriction"></a>2.2.1.9 CPropertyRestriction

A estrutura CPropertyRestriction contém um valor da propriedade para corresponder a uma operação.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_reope

\_Propriedade (variável)

\_prval (variável)



 

**\_ relop:** um inteiro sem sinal de 32 bits que especifica a relação a ser executar na propriedade . DEVE ser um dos valores a seguir.



| Valor                 | Significado                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PrLT 0x00000000       | Uma comparação menor que.                                                                                           |
| PRLE 0x00000001       | Uma comparação menor ou igual a.                                                                               |
| PRGT 0x00000002       | Uma comparação maior que.                                                                                        |
| PrGE 0x00000003       | Uma comparação maior ou igual a.                                                                            |
| PREQ 0x00000004       | Uma comparação de igualdade.                                                                                           |
| PRNE 0x00000005       | Uma comparação não igual.                                                                                           |
| PRRE 0x00000006       | Uma comparação de expressão regular.                                                                                  |
| PRAllBits 0x00000007  | Um operador e bit que retorna o operando à direita.                                                                     |
| PRSomeBits 0x00000008 | Um valor bit e AND que retorna um Value diferente de zero.                                                                       |
| PRAll 0x00000100      | A operação deve ser executada em uma coluna de um conjunto de linhas e só será verdadeira se a operação for verdadeira para todas as linhas. |
| PRAny 0x00000200      | A operação deve ser executada em uma coluna de um conjunto de linhas e será true se a operação for verdadeira para qualquer linha.       |



 

**\_ Propriedade**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.2, indicando a propriedade na qual executar uma operação de correspondência.

**\_ prval**: uma estrutura CBaseStorageVariant, conforme especificado na seção 2.2.1.1, que contém o valor a ser relacionado à propriedade.

### <a name="22110-crangerestriction"></a>2.2.1.10 CRangeRestriction

A estrutura CRangeRestriction contém uma restrição em um intervalo de valores.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_keystart (variável)

\_keyEnd (variável)



 

**\_ keystart**: uma estrutura CKey, conforme especificado na seção 2.2.1.4, que contém o início do intervalo.

**\_ keyEnd**: uma estrutura CKey que contém o final do intervalo.

### <a name="22111-cscoperestriction"></a>2.2.1.11 CScopeRestriction

A estrutura CScopeRestriction contém uma restrição nos arquivos a serem pesquisados



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CcLowerPath

\_lowerPath (variável)

...

\_preenchimento (variável)

\_muito

\_fRecursive

\_fVirtual



 

**CcLowerPath**: um inteiro sem sinal de 32 bits contendo o número de caracteres Unicode no \_ campo lowerPath.

**\_ lowerPath**: uma cadeia de caracteres Unicode não terminada em nulo que representa o **caminho** para o qual a consulta deve ser restrita. O campo CcLowerPath contém o comprimento da cadeia de caracteres.

**\_ preenchimento**: esse campo deve ter de 0 a 3 bytes de comprimento. O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura. Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário. O conteúdo deste campo deve ser ignorado pelo destinatário.

**\_ comprimento**: um inteiro sem sinal de 32 bits contendo o comprimento de \_ LowerPath, em caracteres Unicode. DEVE ser o mesmo valor que CcLowerPath.

**\_ fRecursive**: um inteiro sem sinal de 32 bits. DEVE ser definido como 0x00000001 ou 0x00000000. Se definido como 0x00000001, o servidor deve examinar recursivamente todos os subdiretórios do caminho. Se definido como 0x00000000, o servidor não examinará nenhum subdiretório.

**\_ fVirtual**: um inteiro sem sinal de 32 bits. DEVE ser definido como 0x00000001 ou 0x00000000. Se definido como 0x00000001, \_ lowerPath é um caminho virtual (o Uniform Resource Locator (URL) associado a um diretório físico no sistema de arquivos) para um site da Web. Se definido como 0x00000000, \_ lowerPath é um caminho do sistema de arquivos.

### <a name="22112-csort"></a>2.2.1.12 CSort

A estrutura CSort identifica uma coluna a ser classificada.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

pidColumn

dwOrd

localidade



 

**pidColumn**: um inteiro sem sinal de 32 bits. O número da coluna pela qual classificar.

**dwOrder**: um inteiro sem sinal de 32 bits. DEVE ser um dos valores a seguir, especificando como classificar com base na coluna.



| Valor                        | Significado                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| CONSULTAR \_ SORTASCEND 0x00000000 | As linhas devem ser classificadas em ordem crescente com base nos valores da coluna especificada.  |
| CONSULTA \_ descendente 0x00000001    | As linhas devem ser classificadas em ordem decrescente com base nos valores da coluna especificada. |



 

**localidade**: um inteiro de 32 bits sem sinal indicando a localidade, conforme especificado no \[ Apêndice a do MS-GPSI \] , da coluna.

### <a name="22113-csynrestriction"></a>2.2.1.13 CSynRestriction

A estrutura CSynRestriction contém uma palavra ou seus sinônimos para uma frase de consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Restrição

...

...

cKey

\_keyarray (variável)

\_ISRANGE



 

**Restrição**: uma estrutura COccRestriction que especifica o local da palavra.

**cKey**: um inteiro sem sinal de 32 bits especificando o número de elementos na \_ matriz keyarray.

**\_ keyarray**: uma matriz de estruturas CKey que especificam uma palavra e seus sinônimos.

**\_ ISRANGE**: se definido como 0x01, as chaves são prefixos para correspondência. Se definido como 0x00, as chaves são valores exatos para corresponder. \_ISRANGE não deve ser definido para nenhum outro valor.

### <a name="22114-cvectorrestriction"></a>2.2.1.14 CVectorRestriction

A estrutura CVectorRestriction contém uma operação ponderada ou em um nó de árvore de comandos.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Pres (variável)

...

\_preenchimento (variável)

\_ulRankMethod



 

**\_ Pres**: uma árvore de comandos CNodeRestriction na qual uma classificação ou operação deve ser executada.

**\_ preenchimento**: esse campo deve ter de 0 a 3 bytes de comprimento. O comprimento deste campo deve ser de modo que o seguinte campo comece em um deslocamento que seja um múltiplo de 4 bytes do início da mensagem que contém essa estrutura. Se esse campo estiver presente (ou seja, comprimento diferente de zero), o valor que ele contém será arbitrário. O conteúdo deste campo deve ser ignorado pelo destinatário.

**\_ ulRankMethod**: um inteiro sem sinal de 32 bits especificando um algoritmo de classificação. DEVE ser definido como um dos valores a seguir.



| Valor                            | Significado                                       |
|----------------------------------|-----------------------------------------------|
| Classificação de vetor \_ \_ mín. 0x00000000     | Usar Salt de algoritmo mínimo \[ \] .             |
| Classificação de vetor \_ \_ máx. 0x00000001     | Use o Salt máximo do algoritmo \[ \] .             |
| \_0x00000002 interno de classificação de vetor \_   | Usar a saltização do algoritmo de produto interno \[ \] .       |
| \_0x00000003 de classificação de vetor \_    | Use a saltização do algoritmo de coeficiente de um \[ \] .    |
| Classificação de vetor \_ \_ Jaccard 0x00000004 | Use a saltização do algoritmo de coeficiente Jaccard \[ \] . |



 

### <a name="22115-cwordrestriction"></a>2.2.1.15 CWordRestriction

A estrutura CWordRestriction contém uma palavra para uma frase de consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

restriction

...

...

\_key (variável)

\_isRange



 

**restriction:** uma estrutura COccRestriction que especifica o local da palavra.

**\_ key:** uma estrutura CKey especificando uma palavra.

**\_ isRange:** se definido como 0x01, a chave será um prefixo para corresponder. Se definido como 0x00, a chave será um valor exato para corresponder. \_isRange NÃO DEVE ser definido como nenhum outro valor.

### <a name="22116-crestriction"></a>2.2.1.16 CRestriction

A estrutura CRestriction contém um nó de uma árvore de comandos de consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ulType

Peso

Restrição



 

**\_ ulType:** um inteiro sem sinal de 32 bits que indica o tipo de restrição usado para o nó da árvore de comandos. DEVE ser definido como um dos valores a seguir.



| Valor                    | Significado                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| RTNone 0x00000000        | O nó representa uma palavra de ruído em uma consulta de vetor.                                         |
| RTAnd 0x00000001         | O nó contém uma CNodeRestriction na qual uma operação AND lógica a ser executada. |
| RTOr 0x00000002          | O nó contém uma CNodeRestriction na qual uma operação OR lógica deve ser executada.  |
| RTNot 0x00000003         | O nó contém uma CRestriction na qual uma operação NOT deve ser executada.             |
| RTContent 0x00000004     | O nó contém um CContentRestriction.                                                    |
| RTProperty 0x00000005    | O nó contém uma CPropertyRestriction.                                                   |
| RTProximity 0x00000006   | O nó contém uma CNodeRestriction na qual uma classificação de proximidade deve ser executada,     |
| RTVector 0x00000007      | O nó contém um CVectorRestriction.                                                     |
| RTNatLanguage 0x00000008 | O nó contém uma CNatLanguageRestriction.                                                |
| RTScope 0x00000009       | O nó contém um CScopeRestriction.                                                      |
| PrAny 0xFFFFFFFA         | O nó contém um CInternalPropertyRestriction.                                           |
| RTRange 0xFFFFFFFC       | O nó contém um CRangeRestriction.                                                      |
| RTPhrase 0xFFFFFFFD      | O nó contém uma CNodeRestriction na qual uma combinação de frases deve ser executada.          |
| RTSynonym 0xFFFFFFFE     | O nó contém uma CSynRestriction.                                                        |
| RTWord 0xFFFFFFFF        | O nó contém uma CWordRestriction.                                                       |



 

**Peso:** um inteiro sem sinal de 32 bits que representa o peso do nó. Peso indica a importância do nó em relação a outros nós na árvore de comandos de consulta. Valores de peso mais altos são mais importantes.

**Restrição:** o tipo de restrição para o nó da árvore de comandos. A sintaxe DEVE ser conforme indicado pelo \_ campo ulType.

### <a name="22117-ccolumnset"></a>2.2.1.17 CColumnSet

A estrutura CColumnSet especifica os números de coluna a serem retornados. Essa estrutura é sempre usada em referência a uma estrutura CPidMapper específica (seção 2.2.1.23).



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

índices (variável)



 

**Count**: um inteiro de 32 bits sem sinal especificando o número de elementos na matriz de índices.

**índices**: matriz de inteiros sem sinal de 4 bytes que representam índices baseados em zero na matriz aPropSpec na estrutura CPidMapper correspondente.

### <a name="22118-ccategorizationset"></a>2.2.1.18 CCategorizationSet

A estrutura CCategorizationSet contém informações sobre o agrupamento de um conjunto de resultados de consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

Categorias (variável)



 

**Count**: um inteiro sem sinal de 32 bits contendo o número de elementos na matriz Categories.

**categorias**: matriz de estruturas CCategorizationSpec especificando o agrupamento da consulta.

### <a name="22119-ccategorizationspec"></a>2.2.1.19 CCategorizationSpec

A estrutura CCategorizationSpec contém um agrupamento para um conjunto de resultados de consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_csColumns (variável)

\_ulCategType



 

**\_ csColumns:** uma estrutura CColumnSet que indica as colunas pelas quais agrupar a consulta.

**\_ ulCategType:** um inteiro sem sinal de 32 bits. DEVE ser definido como 0x00000000.

### <a name="22120-cdbcolid"></a>2.2.1.20 CDbColId

A estrutura CDbColId contém uma coluna.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

eKind

GUID

...

...

...

ulId

vString (variável)



 

**eKind**: DEVE ser definido como um dos valores abaixo que indica o conteúdo de GUID e vValue.



| Valor                            | Significado                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| NOME DO GUID DBKIND \_ \_ 0x00000000    | vString contém um nome de propriedade.                                                                               |
| DBKIND \_ GUID \_ PROPID 0x00000001  | ulId contém um inteiro de 4 byte que indica a ID da propriedade.                                                      |
| DBKIND \_ PGUID \_ NAME 0x00000003   | vString contém um nome de propriedade. Esse valor DEVE ser tratado da mesma forma que DBKIND \_ GUID \_ NAME.                    |
| DBKIND \_ PGUID \_ PROPID 0x00000004 | ulId contém um inteiro de 4 byte que indica a ID da propriedade. Esse valor DEVE ser o mesmo que DBKIND \_ GUID \_ PROPID. |



 

**GUID:** o GUID da propriedade.

**ulId**: se eKind for DBKIND GUID PROPID ou DBKIND PGUID PROPID, esse campo conterá um inteiro sem \_ \_ \_ \_ sinal, especificando a ID da propriedade. Se eKind for DBKIND GUID NAME ou DBKIND PGUID NAME, esse campo conterá um inteiro sem sinal especificando o número de caracteres Unicode contidos no campo \_ \_ \_ \_ vString.

**vString:** uma cadeia de caracteres Unicode não terminada em nulo que representa o nome da propriedade. Ele DEVE ser omitido, a menos que o campo eKind esteja definido como DBKIND \_ GUID \_ NAME ou DBKIND \_ PGUID \_ NAME.

### <a name="22121-cdbprop"></a>2.2.1.21 CDbProp

A estrutura CDbProp contém uma propriedade .



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

DBPROPID

DBPROPOPTIONS

DBPROPSTATUS

colid (variável)

vValue (variável)



 

**DBPROPID:** um inteiro sem sinal de 32 bits, indicando a ID da propriedade.

**DBPROPOPTIONS:** deve ser definido como 0x00000000.

**DBPROPSTATUS:** deve ser definido como 0x00000000.

**colid**: uma estrutura CDbColId, conforme especificado na seção 2.2.1.20, indicando a coluna à qual a propriedade se aplica.

**vValue:** um CBaseStorageVariant que contém o valor da propriedade.

### <a name="221211-properties"></a>2.2.1.21.1 Propriedades

Esta seção detalha as propriedades usadas pelo CISP. Essas propriedades são agrupadas em três conjuntos de propriedades, ident2.2.1.21.1, no campo guidPropertySet da estrutura CDbPropSet (Seção 2.2.1.22).

A tabela a seguir lista as propriedades que fazem parte do conjunto de propriedades DBPROPSET \_ FSCIFRMWRK \_ EXT.



| Valor                                  | Significado                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| NOME DO \_ CATÁLOGO DBPROP CI \_ \_ 0x00000002   | Especifica o nome do catálogo ou catálogos a ser consultado. O valor DEVE ser um VT \_ LPWSTR ou um \_ VT VECTOR \| VT \_ LPWSTR                                   |
| DBPROP \_ CI \_ INCLUDE \_ SCOPES 0X00000003 | Especifica um ou mais caminhos a serem incluídos na consulta. O valor DEVE ser um VT \_ LPWSTR ou um \_ VT VECTOR \| VT \_ LPWSTR.                                 |
| SINALIZADORES DE \_ ESCOPO DE CI \_ \_ DBPROP 0X00000004    | Especifica como os caminhos especificados pela propriedade DBPROP \_ CI \_ INCLUDE \_ SCOPES devem ser tratados. O valor DEVE ser uma VT \_ I4 ou uma \_ VT VECTOR \| VT \_ I4. |
| TIPO DE \_ CONSULTA DBPROP CI \_ \_ 0X00000007     | Especifica o tipo de consulta. O CDbColId DEVE ser definido como DB \_ NULLID.                                                                               |



 

A tabela a seguir lista os sinalizadores para a propriedade DBPROP \_ CI \_ SCOPE \_ FLAGS:



| Valor                     | Significado                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONSULTA PROFUNDA \_ 0X01          | Se definido, indica que os arquivos no diretório de escopo e todos os subdireários estão incluídos nos resultados. Se estiver claro, somente os arquivos no diretório de escopo serão incluídos nos resultados. NÃO DEVE ser combinado com A CONSULTA \_ PROFUNDA. |
| CONSULTA DE \_ CAMINHO VIRTUAL \_ 0X02 | Se definido, indica que o escopo é um caminho virtual. Se estiver claro, indica que o escopo é um diretório físico.                                                                                                         |



 

A tabela a seguir lista os tipos de consulta para a propriedade DBPROP \_ CI \_ QUERY \_ TYPE:



| Valor                     | Significado                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| CiNormal 0x00000000       | Uma consulta regular.                                                                                                   |
| CiVirtualRoots 0x00000001 | A consulta está solicitando uma lista das raízes virtuais do catálogo. Esse valor requer privilégios administrativos. |
| CiProperties 0x00000003   | A consulta está solicitando uma lista de todas as propriedades com suporte pelo serviço de indexação.                            |
| CiAdminOp 0x00000004      | A consulta é uma operação administrativa. Esse valor requer privilégios administrativos.                           |



 

A tabela a seguir lista as propriedades que fazem parte do conjunto de propriedades DBPROPSET \_ QUERYEXT.



| Valor                                      | Significado                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ USECONTENTINDEX 0x00000002         | Especifica como o serviço de indexação é para lidar com consultas lentas. O valor DEVE ser um BOOL de \_ VT. Se TRUE, o servidor poderá falhar nessas consultas.                                                                                    |
| DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003 | Indica se o serviço de indexação deve executar o corte de resultados. Se TRUE, o servidor deve considerar a execução de corte de resultados de uma maneira que otimize o tempo de resposta para o cliente. O valor DEVE ser um BOOL de \_ VT.             |
| DBPROP \_ USEEXTENDEDDBTYPES 0x00000004      | Indica se o cliente dá suporte a tipos de dados \_ VECTOR VT. Se TRUE, o cliente dá suporte a VECTOR VT; se FALSE, o servidor deve converter tipos de dados VECTOR VT em tipos de \_ \_ dados VT \_ ARRAY.  O valor DEVE ser um BOOL de \_ VT. |
| DBPROP \_ FIRSTROWS 0x00000007               | Indica as correspondeções de linha a retornar. Se TRUE, o servidor deve retornar o primeiro conjunto de linhas correspondentes. Se FOR FALSE, as melhores linhas correspondentes deverão ser retornadas. O valor DEVE ser um BOOL de \_ VT.                                             |



 

A tabela a seguir lista as propriedades que fazem parte do conjunto de propriedades DBPROPSET \_ CIFRMWRKCORE \_ EXT.



| Value/DBPROPID                 | Significado                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ MACHINE 0x00000002       | Especifica os nomes dos computadores nos quais uma consulta deve ser processada. O valor DEVE ser VT \_ BSTR ou VT \_ ARRAY \| VT \_ BSTR. |
| DBPROP \_ CLIENT \_ CLSID 0x00000003 | Especifica uma constante de conexão para o serviço de indexação. O valor DEVE ser uma CLSID de VT \_ que contém 0x2A4880706FD911D0A80800A0C906241A.  |



 

### <a name="22122-cdbpropset"></a>2.2.1.22 CDbPropSet

A estrutura CDbPropSet contém um conjunto de propriedades. Observe que o primeiro campo é de tamanho fixo, mas pode não estar alinhado a um deslocamento que é um múltiplo de 4 byte desde o início da mensagem que contém essa estrutura. No entanto, o campo cProperties é alinhado como tal e, portanto, o formato é representado da seguinte forma:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Guidpropertyset

...

...

...

...

\_preenchimento (variável)

cProperties

aProps (variável)



 

**guidPropertySet:** um GUID que identifica o conjunto de propriedades. DEVE ser definido como o formulário binário correspondente a um dos valores a seguir (mostrado no formulário de representação de cadeia de caracteres), identificando o conjunto de propriedades das propriedades contidas no campo aProps.



| Valor/GUID                                                                              | Nome                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| DBPROPSET \_ FSCIFRMWRK \_ EXT<br/> {A9BD1526-6A80-11D0-8C9D-0020AF1D740E}<br/>   | Conjunto de propriedades da estrutura de índice de conteúdo do sistema de arquivos |
| DBPROPSET \_ QUERYEXT<br/> {A7AC77ED-F8D7-11CE-A798-0020F8008025}<br/>          | Conjunto de propriedades da extensão de consulta                     |
| DBPROPSET \_ CIFRMWRKCORE \_ EXT<br/> {AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}<br/> | Conjunto de propriedades do Content Index Framework Core        |



 

**\_ preenchimento:** esse campo DEVE ter de 0 a 3 bytes de comprimento. O comprimento desse campo DEVE ser tal que o campo a seguir comece em um deslocamento que é um múltiplo de 4 bytes do início da mensagem que contém essa estrutura. Se esse campo estiver presente (ou seja, comprimento não zero), o valor que ele contém será arbitrário. O conteúdo desse campo DEVE ser ignorado pelo receptor.

**cProperties:** um inteiro sem sinal de 32 bits que contém o número de elementos na matriz aProps.

**aProps:** uma matriz de estruturas CDbProp, conforme especificado na seção 0, que contém propriedades. As estruturas na matriz DEVEM ser separadas por 0 a 3 bytes de preenchimento, de forma que cada estrutura comece em um deslocamento que é um múltiplo de 4 bytes do início da mensagem que contém essa matriz. Se bytes de preenchimento estão presentes, o valor que eles contêm é arbitrário. O conteúdo dos bytes de preenchimento DEVE ser ignorado pelo receptor.

### <a name="22123-cpidmapper"></a>2.2.1.23 CPidMapper

A estrutura CPidMapper contém uma matriz de IDs de propriedade especificando as propriedades a retornar em um conjunto de linhas.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

count

aPropSpec

... (variável)



 

**count:** um inteiro sem sinal de 32 bits que contém o número de elementos na matriz aPropSpec.

**aPropSpec**: matriz de estruturas CFullPropSpec que indica as propriedades a serem retornadas. As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura tenha um alinhamento de 4 bytes desde o início de uma mensagem. Esses bytes de preenchimento podem ser qualquer valor arbitrário e devem ser ignorados no recebimento.

### <a name="22124-crowseekat"></a>2.2.1.24 CRowSeekAt

A estrutura CRowSeekAt contém o deslocamento no qual recuperar linhas em uma mensagem CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cskip

\_bmkOffset



 

**\_ hRegion**: deve ser definido como 0x00000000 e deve ser ignorado.

**\_ cskip**: um inteiro sem sinal de 32 bits contendo o número de linhas a serem ignoradas no conjunto de linhas.

**\_ bmkOffset**: um valor de 32 bits que representa o identificador do **indicador** que indica a posição inicial a partir da qual ignorar o número de linhas especificado em \_ cskip, antes de iniciar a recuperação.

### <a name="22125-crowseekatratio"></a>2.2.1.25 CRowSeekAtRatio

A estrutura CRowSeekAtRatio identifica o ponto no qual iniciar a recuperação para uma mensagem CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_ulNumerator

\_ulDenominator



 

**CiTblChapt**: um inteiro de 32 bits sem sinal indicando o capítulo do conjunto de linhas do qual recuperar linhas.

**\_ hRegion**: deve ser definido como 0x00000000 e deve ser ignorado.

**\_ ulNumerator**: inteiro de 32 bits sem sinal que representa o numerador da proporção de linhas no capítulo no qual iniciar a recuperação.

**\_ ulDenominator**: inteiro de 32 bits sem sinal que representa o denominador da proporção de linhas no capítulo no qual iniciar a recuperação. DEVE ser maior que zero.

### <a name="22126-crowseekbybookmark"></a>2.2.1.26 CRowSeekByBookmark

A estrutura CRowSeekByBookmark identifica os indicadores dos quais começar a recuperar linhas para uma mensagem CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cBookmarks

\_maxRet

\_cValidRet

\_aBookmarks (variável)

\_ascRet (variável)



 

**\_ hRegion**: DEVE ser definido como 0x00000000 e DEVE ser ignorado.

**\_ cBookmarks:** inteiro de 32 bits sem sinal que representa o número de elementos na \_ matriz aBookmarks.

**\_ maxRet:** inteiro de 32 bits sem sinal que representa o número de elementos na \_ matriz ascRet.

**\_ cValidRet:** inteiro de 32 bits sem sinal que representa o número de elementos na \_ matriz ascRet que são válidos. Elementos válidos foram definidos na matriz, enquanto elementos inválidos são indefinido.

**\_ aBookmarks:** uma matriz de alças de indicador (cada uma representada por 4 bytes), conforme obtido de uma mensagem CPMGetRowsOut.

**\_ ascRet:** uma matriz de valores HRESULT. Quando o CRowSeekByBookMark é enviado como parte da solicitação CPMGetRowsIn, o número de entradas na matriz DEVE ser igual a \_ cBookMarks. Quando enviados pelo cliente, os valores DEVEM ser definidos como zero e o servidor DEVE ignorar o conteúdo da matriz. Quando enviados pelo servidor (como parte da mensagem CPMGetRowsOut), os valores na matriz indicam o status do resultado para cada recuperação de linha.

### <a name="22127-crowseeknext"></a>2.2.1.27 CRowSeekNext

A estrutura CRowSeekNext contém o número de linhas a ignorar em uma mensagem CPMGetRowsIn.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_cskip



 

**CiTblChapt:** inteiro de 32 bits sem sinal especificando o capítulo de conjuntos de linhas do qual recuperar linhas.

**\_ hRegion**: DEVE ser definido como 0x00000000 e DEVE ser ignorado.

**\_ cskip:** inteiro de 32 bits sem sinal que representa o número de linhas a ignorar no conjuntos de linhas.

### <a name="22128-crowsetproperties"></a>2.2.1.28 CRowsetProperties

A estrutura CRowsetProperties contém informações de configuração para uma consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_uBooleanOptions

\_ulMaxOpenRows

\_ulMemoryUsage

\_cMaxResults

\_cCmdTimeout



 

**\_ uBooleanOptions:** os três bits menos significativos desse campo DEVEM conter um dos três valores a seguir:



| Valor                  | Significado                                                             |
|------------------------|---------------------------------------------------------------------|
| eSequential 0x00000001 | O cursor só pode ser movido para frente.                              |
| eLocatable 0x00000003  | O cursor pode ser movido para qualquer posição.                            |
| eScrollable 0x00000007 | O cursor pode ser movido para qualquer posição e buscar em qualquer direção. |



 

Os bits restantes podem ser claros ou definidos como qualquer combinação dos seguintes valores logicamente OR'd juntos:



| Valor                     | Significado                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| eAsynchronous 0x00000008  | O cliente não aguardará a conclusão da execução.                                                          |
| eFirstRows 0x00000080     | Retornar as primeiras linhas encontradas, não as melhores.                                                    |
| eHoldRows 0x00000200      | O servidor NÃO DEVE descartar linhas até que o cliente seja feito com uma consulta.                                     |
| eChaptered 0x00000800     | O rowset dá suporte a capítulos.                                                                               |
| eUseCI 0x00001000         | Responda apenas à consulta do índice, não do sistema de arquivos.                                                  |
| eDeferTrimming 0x00002000 | O serviço de indexação é considerar a otimização do tempo de resposta para o cliente ao executar a remoção de resultados. |



 

**\_ ulMaxOpenRows:** inteiro de 32 bits sem sinal. Deve ser definido como 0x00000000. Não usado e DEVE ser ignorado.

**\_ ulMemoryUsage:** inteiro de 32 bits sem sinal. Deve ser definido como 0x00000000. Não usado e DEVE ser ignorado.

**\_ cMaxResults:** um inteiro sem sinal de 32 bits que especifica o número máximo de linhas que devem ser retornadas para a consulta.

**\_ cCmdTimeout:** um inteiro sem sinal de 32 bits, especificando o número de segundos em que uma consulta deve ser encerrada e encerrada automaticamente, contando a partir do momento em que a consulta começa a ser executada no servidor. Um valor de 0x00000000 significa que a consulta não deve ter o tempo máximo.

### <a name="22129-crowvariant"></a>2.2.1.29 CRowVariant

A estrutura CRowVariant contém a parte de tamanho fixo de um tipo de dados de comprimento variável armazenado na mensagem CPMGetRowsOut.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

reserved1

reserved2

Deslocamento (opcional)



 

**vType**: um indicador de tipo, que indica o tipo de vValue. Ele deve ser um dos valores de VARENUM especificados na seção 2.2.1.1.

**reserved1**: não usado. O valor pode ser definido como qualquer valor arbitrário e deve ser ignorado no recebimento.

**reserved2**: não usado. O valor pode ser definido como qualquer valor arbitrário e deve ser ignorado no recebimento.

**Offset**: um deslocamento para dados de comprimento variável (por exemplo, uma cadeia de caracteres).  Esse deve ser um valor de 32 bits (4 bytes de comprimento) se os deslocamentos de 32 bits estiverem sendo usados (de acordo com as regras na seção 2.2.3.16) ou um valor de 64 byte (8 bytes de comprimento) se os deslocamentos de 64 bits estiverem sendo usados.

### <a name="22130-csortset"></a>2.2.1.30 CSortSet

A estrutura CSortSet contém a ordem de classificação da consulta.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Contagem

sortArray (variável)



 

**Count**: um inteiro sem sinal de 32 bits especificando o número de elementos em sortArray.

**sortArray**: uma matriz de estruturas CSort que descreve a ordem na qual os resultados da consulta são classificados. As estruturas na matriz devem ser separadas por 0 a 3 bytes de preenchimento, de modo que cada estrutura tenha um alinhamento de 4 bytes desde o início de uma mensagem. Esses bytes de preenchimento podem ser qualquer valor arbitrário e devem ser ignorados no recebimento.

### <a name="22131-ctablecolumn"></a>2.2.1.31 CTableColumn

A estrutura CTableColumn contém uma coluna de uma mensagem CPMSetBindingsIn



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PropSpec

... Ela

vType

ValueUsed

\_padding1 (opcional)

ValueOffset (opcional)

Valores (opcional)

StatusUsed

\_padding2 (opcional)

StatusOffset (opcional)

LengthUsed

\_padding3 (opcional)

LengthOffset (opcional)



 

**PropSpec**: uma estrutura CFullPropSpec, conforme especificado na seção 2.2.1.3.

**vType**: especifica o tipo de valor de dados contido na coluna. Consulte o campo vType na seção 2.2.1.1 para obter a lista de valores para esse campo.

**ValueUsed**: um campo de um byte que deve ser definido como 0x01 ou 0x00. Se definido como 0x01, a coluna será transferida dentro da linha de tamanho fixo. Se definido como 0x00, o valor da coluna será transferido na seção de comprimento variável no final do buffer.

**\_ padding1**: um campo de um byte que deve ser inserido antes de ValueOffset se, sem ele, ValueOffset não começaria em um deslocamento par do início da mensagem. O valor desse byte é arbitrário e deve ser ignorado. Se ValueUsed for definido como 0x00, esse campo não deverá estar presente.

**ValueOffset**: um inteiro de 2 bytes não assinado que especifica o deslocamento do valor da coluna na linha. Se ValueUsed for definido como 0x00, esse campo não deverá estar presente.

**Values**: um inteiro de 2 bytes sem sinal especificando o tamanho do valor da coluna em bytes. Se ValueUsed for definido como 0x00, esse campo não deverá estar presente.

**StatusUsed**: um campo de um byte que deve ser definido como 0x01 ou 0x00. Se definido como 0x01, o status da coluna será transferido dentro da linha. Se 0x00, o status da coluna não será transferido dentro da linha.

**\_ padding2**: um campo de um byte que deve ser inserido antes de StatusOffset se, sem ele, o campo StatusOffset não começaria em um deslocamento par do início da mensagem. O valor desse byte é arbitrário e deve ser ignorado. Se StatusUsed for definido como 0x00, esse campo não deverá estar presente.

**StatusOffset**: um inteiro de 2 bytes não assinado que especifica o deslocamento do status da coluna na linha. Se StatusUsed for definido como 0x00, esse campo não deverá estar presente.

**LengthUsed**: um campo de um byte que deve ser definido como 0x01 ou 0x00. Se definido como 0x01, o comprimento da coluna é transferido dentro da linha. Se 0x00, o comprimento da coluna não deve ser transferido dentro da linha.

**\_ padding3**: um campo de um byte que deve ser inserido antes de LengthOffset se, sem ele, LengthOffset não começaria em um deslocamento par do início de uma mensagem. O valor desse byte é arbitrário e deve ser ignorado. Se LengthUsed for definido como 0x00, esse campo não deverá estar presente.

**LengthOffset**: um inteiro de 2 bytes não assinado que especifica o deslocamento do comprimento da coluna na linha. Se LengthUsed for definido como 0x00, esse campo não deverá estar presente.

### <a name="22132-serializedpropertyvalue"></a>2.2.1.32 SERIALIZEDPROPERTYVALUE

A estrutura SERIALIZEDPROPERTYVALUE contém um valor serializado.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

dwType

RGB (variável)



 

**dwType**: um dos tipos variantes, definidos na seção 2.2.1.1, que podem ser combinados com modificadores de tipo Variant. Para todos os tipos de variantes, exceto aqueles combinados com \_ a matriz VT, SERIALIZEDPROPERTYVALUE tem o mesmo layout que CBaseStorageVariant, conforme especificado na seção 2.2.1.1. Se o tipo Variant for combinado com o \_ modificador de tipo de matriz VT, SAFEARRAY2, especificado na seção 2.2.1.2.1.1, será usado em vez de SAFEARRAY no campo vValue de CBaseStorageVariant.

**RGB**: valor serializado. Veja detalhes de serialização para vValue em 2.2.1.1.

### <a name="222-message-headers"></a>Cabeçalhos de mensagem 2.2.2

Todas as mensagens do protocolo de serviço de indexação de conteúdo têm um cabeçalho de 16 bytes.

Veja abaixo um diagrama que mostra o formato de cabeçalho da mensagem do protocolo de serviço de indexação de conteúdo.



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_MSG

\_Estado

\_ulChecksum

\_ulReserved2



 

\_**msg**: um inteiro de 32 bits que identifica o tipo de mensagem após o cabeçalho. A tabela a seguir lista as mensagens do protocolo de serviço de indexação de conteúdo e os valores inteiros especificados para cada mensagem. Conforme mostrado na tabela, alguns valores identificam 2 mensagens na tabela. Nessas instâncias, a mensagem após o cabeçalho pode ser identificada pela direção do fluxo de mensagens. Se a direção for cliente para servidor, a mensagem com "in" acrescentado ao nome da mensagem será indicada. Se a direção for servidor para cliente, a mensagem com "out" anexado ao nome da mensagem será indicada.



| Valor      | Significado                                                     |
|------------|-------------------------------------------------------------|
| 0x000000C8 | CPMConnectIn ou CPMConnectOut                               |
| 0x000000C9 | CPMDisconnect                                               |
| 0x000000CA | CPMCreateQueryIn ou CPMCreateQueryOut                       |
| 0x000000CB | CPMFreeCursorIn ou CPMFreeCursorOut                         |
| 0x000000CC | CPMGetRowsIn ou CPMGetRowsOut                               |
| 0x000000CD | CPMRatioFinishedIn ou CPMRatioFinishedOut                   |
| 0x000000CE | CPMCompareBmkIn ou CPMCompareBmkOut                         |
| 0x000000CF | CPMGetApproximatePositionIn ou CPMGetApproximatePositionOut |
| 0x000000D0 | CPMSetBindingsIn                                            |
| 0x000000D1 | CPMGetNotify                                                |
| 0x000000D2 | CPMSendNotifyOut                                            |
| 0x000000D7 | CPMGetQueryStatusIn ou CPMGetQueryStatusOut                 |
| 0x000000D9 | CPMCiStateInOut                                             |
| 0x000000E1 | CPMForceMergeIn                                             |
| 0x000000E4 | CPMFetchValueIn ou CPMFetchValueOut                         |
| 0x000000E6 | CPMUpdateDocumentsIn                                        |
| 0x000000E7 | CPMGetQueryStatusExIn ou PMGetQueryStatusExOut              |
| 0x000000E8 | CPMRestartPositionIn                                        |
| 0x000000E9 | CPMStopAsynchIn                                             |
| 0x000000EC | CPMSetCatStateIn ou CPMSetCatStateOut                       |



 

\_**status**: um HRESULT \[ MS-sys \] , que indica o status da operação solicitada.

\* *

*Comportamento do Windows: o cliente sempre define o \_ campo status como 0x00000000.*

**\_ ulChecksum**: o \_ ulChecksum deve ser calculado conforme especificado na seção 3.2.4 para as seguintes mensagens:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMSetBindingsIn
-   CPMGetRowsIn
-   CPMFetchValueIn

Para todas as outras mensagens, \_ ULCHECKSUM deve ser definido como 0x00000000. Um cliente deve ignorar o \_ campo ulChecksum.

**\_ ulReserved2**: deve ser definido como 0 e ignorado pelo destinatário.

### <a name="223-messages"></a>mensagens 2.2.3

### <a name="2231-cpmcistateinout"></a>2.2.3.1 CPMCiStateInOut

A mensagem CPMCiStateInOut contém informações sobre o estado do serviço de indexação. O formato da mensagem CPMCiStateInOut que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbStruct

cWordList

cPersistentIndex

cQueries

cDocuments

cFreshTest

dwMergeProgress

Imóveis

cFilteredDocuments

cTotalDocuments

cPendingScans

dwIndexSize

cUniqueKeys

cSecQDocuments

dwPropCacheSize



 

**cbStruct**: um inteiro sem sinal de 32 bits. O tamanho em bytes desta mensagem (excluindo o cabeçalho comum). DEVE ser definido como 0x0000003C.

**cWordList**: um inteiro de 32 bits sem sinal indicando a contagem de índices iniciais criados para documentos indexados recentemente.

**cPersistentIndex**: um inteiro de 32 bits sem sinal indicando a contagem de índices persistentes.

**cQueries**: um inteiro de 32 bits sem sinal indicando um número de consultas em execução ativamente.

**cDocuments**: um inteiro de 32 bits sem sinal indicando o número total de documentos aguardando para serem indexados.

**cFreshTest**: um inteiro sem sinal de 32 bits que indica o número de documentos exclusivos com informações em índices que não são totalmente otimizados para desempenho.

**dwMergeProgress**: inteiro de 32 bits sem sinal especificando a porcentagem de conclusão da otimização total atual de índices, se a otimização estiver em andamento no momento. DEVE ser menor ou igual a 100.

**imobiliária**: estado da indexação de conteúdo, conforme fornecido por uma ou mais das \_ constantes de estado de CI \_ \* , definidas na tabela a seguir.



| Valor                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Mesclagem de sombra de estado de CI \_ \_ 0x00000001           | O serviço de indexação está no processo de otimização de alguns dos índices para reduzir o uso de memória e melhorar o desempenho da consulta.                                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ Mesclagem mestra de estado CI \_ 0x00000002           | O serviço de indexação está no processo de Otimização total para todos os índices.                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \_Exame de conteúdo de estado CI \_ \_ \_ necessário 0x00000004 | Alguns documentos no índice foram alterados e o serviço de indexação precisa determinar quais foram adicionados, alterados ou excluídos.                                                                                                                                                                                                                                                                                                                                                              |
| CI \_ estado \_ recozimento \_ mesclar 0x00000008        | O serviço de indexação está no processo de otimização de índices para reduzir o uso de memória e melhorar o desempenho da consulta. Esse processo é mais abrangente do que aquele identificado pelo valor de \_ mesclagem de sombra de estado de CI \_ \_ , mas não é tão abrangente quanto o especificado pelo \_ valor de \_ mesclagem mestre de estado CI \_ . Essas otimizações são específicas da implementação, pois dependem da maneira como os dados são armazenados internamente; as otimizações não afetam o protocolo de nenhuma forma que não seja o tempo de resposta. |
| \_Verificação de estado CI \_ 0x00000010                | O serviço de indexação está examinando um diretório ou um conjunto de diretórios para ver se algum arquivo foi adicionado, excluído ou atualizado desde a última vez em que o diretório foi indexado.                                                                                                                                                                                                                                                                                                                 |
| O \_ estado de CI \_ recuperando 0x00000020              | O serviço está sendo iniciado a partir do último estado salvo e está no processo de recuperação.                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_0x00000080 de \_ memória insuficiente do estado de CI \_             | A maior parte da memória virtual do servidor está em uso.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Estado de CI de \_ \_ alta \_ e/s 0x00000100                | O nível de atividade de entrada/saída (e/s) no servidor é relativamente alto.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \_Mesclagem mestra de estado CI em \_ \_ \_ pausa 0x00000200   | O processo de otimização completa de todos os índices que estavam em andamento foi pausado. Isso é fornecido apenas para fins informativos e não afeta CISP.                                                                                                                                                                                                                                                                                                                                  |
| \_ \_ 0x00000400 somente leitura do estado CI \_              | A parte do serviço de indexação que obtém novos documentos para o índice foi pausada. Isso é fornecido apenas para fins informativos e não afeta CISP.                                                                                                                                                                                                                                                                                                                               |
| Estado de CI de \_ \_ energia da bateria \_ 0x00000800          | A parte do serviço de indexação que obtém novos documentos para o índice foi pausada para conservar o tempo de vida da bateria, mas ainda responde às consultas. Isso é fornecido apenas para fins informativos e não afeta CISP.                                                                                                                                                                                                                                                                 |
| 0x00001000 de usuário de estado de CI \_ \_ \_ ativo            | A parte do serviço de indexação que obtém novos documentos para o índice foi pausada devido à alta atividade pelo usuário (teclado ou mouse), mas ainda responde às consultas. Isso é fornecido apenas para fins informativos e não afeta CISP.                                                                                                                                                                                                                                         |
| Estado de CI \_ \_ iniciando 0x00002000                | O serviço está iniciando. As consultas podem ser executadas, mas a verificação e a notificação ainda não foram habilitadas. Isso é fornecido apenas para fins informativos e não afeta CISP.                                                                                                                                                                                                                                                                                                                   |
| \_Estado CI \_ lendo \_ USNs 0x00004000           | O serviço não leu o log mantido pelo sistema de arquivos para manter o controle das alterações em arquivos ou diretórios em um volume, de modo que o índice pode não estar atualizado.                                                                                                                                                                                                                                                                                                                                  |



 

**cFilteredDocuments**: um inteiro de 32 bits sem sinal indicando o número de documentos indexados desde que a indexação de conteúdo foi iniciada.

**cTotalDocuments**: um inteiro de 32 bits sem sinal indicando o número total de documentos no sistema.

**cPendingScans**: um inteiro de 32 bits sem sinal indicando o número de operações pendentes de indexação de alto nível. O significado desse valor é específico do provedor, mas números maiores são esperados para indicar que mais indexação permanece.

*Comportamento do Windows*: esse valor geralmente é zero, exceto imediatamente após a indexação ter sido iniciada ou após o estouro de uma fila de notificação.

**dwIndexSize**: um inteiro de 32 bits sem sinal indicando o tamanho, em megabytes, do índice (excluindo o cache de propriedades).

**cUniqueKeys**: um inteiro de 32 bits sem sinal indicando o número aproximado de chaves exclusivas no catálogo.

**cSecQDocuments**: um inteiro de 32 bits sem sinal indicando o número de documentos que o serviço de indexação tentará indexar devido a uma falha durante a tentativa de indexação inicial.

**dwPropCacheSize**: um inteiro de 32 bits sem sinal indicando o tamanho, em megabytes, do cache de propriedade.

### <a name="2232-cpmsetcatstatein"></a>2.2.3.2 CPMSetCatStateIn

A mensagem CPMSetCatStateIn define o estado de um catálogo. O formato da mensagem CPMSetCatStateIn que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partID

\_dwNewState

\_CatName (variável, opcional)



 

**\_ partID**: DEVE ser definido como 0x00000001.

**\_ dwNewState**: DEVE ser definido como um dos seguintes valores, indicando o novo estado do catálogo.



| Valor                         | Significado                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CICAT \_ PARADO 0X00000001     | O catálogo é interrompido. Esse estado significa que nenhum novo arquivo deve ser indexado e nenhuma consulta de pesquisa deve ser processada.                                                     |
| CICAT \_ READONLY 0x00000002    | O catálogo é somente leitura. Nenhum arquivo novo deve ser indexado.                                                                                                               |
| CICAT \_ WRITABLE 0X00000004    | O catálogo pode ser escrito. Novos arquivos podem ser indexados e as consultas de pesquisa devem ser processadas.                                                                              |
| CICAT \_ NO \_ QUERY 0X00000008   | O catálogo não está disponível para consulta.                                                                                                                              |
| CICAT \_ GET \_ STATE 0x00000010  | O estado do catálogo não deve ser alterado, apenas recuperado.                                                                                                          |
| CICAT \_ ALL \_ OPENED 0X00000020 | Uma verificação para ver se todos os catálogos foram iniciados. Nesse caso, o campo dwOldState enviado na resposta CPMSetCatStateOut para essa mensagem \_ será relatado como diferente de zero. |



 

**\_ CatName:** o nome do catálogo que deve ter seu estado modificado. O nome DEVE ser uma cadeia de caracteres Unicode terminada em nulo. Esse campo DEVERÁ ser omitido se \_ dwNewState estiver definido como CICAT \_ ALL \_ OPENED.

### <a name="2233-cpmsetcatstateout"></a>2.2.3.3 CPMSetCatStateOut

A mensagem CPMSetCatStateOut é uma resposta a uma mensagem CPMSetCatStateIn com o estado antigo do catálogo. O formato da mensagem CPMSetCatStateOut que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwOldState



 

**\_ dwOldState:** um dos valores a seguir, indicando o estado antigo do catálogo.



| Valor                       | Significado                                    |
|-----------------------------|--------------------------------------------|
| CICAT \_ PARADO 0X00000001   | O catálogo é interrompido.                    |
| CICAT \_ READONLY 0x00000002  | O catálogo é somente leitura.                  |
| CICAT \_ gravável 0x00000004  | O catálogo é gravável.                   |
| CICAT \_ sem \_ 0x00000008 de consulta | O catálogo não está disponível para consulta. |



 

### <a name="2234-cpmupdatedocumentsin"></a>2.2.3.4 CPMUpdateDocumentsIn

A mensagem CPMUpdateDocumentsIn direciona o servidor para indexar o caminho especificado.

O servidor responderá com o cabeçalho da mensagem CPMUpdateDocumentsOut, com os resultados da solicitação contida no \_ campo status do cabeçalho da mensagem.

O formato da mensagem CPMUpdateDocumentsIn que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_sinalizador (opcional)

\_fRootPath (opcional)

RootPath (variável, opcional)



 

**\_ sinalizador**: o tipo de atualização a ser executada. Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor. Esse campo deve ser definido como um dos seguintes valores:



| Valor                  | Significado                                   |
|------------------------|-------------------------------------------|
| UPD \_ INCREM 0x00000000 | Uma atualização incremental deve ser executada. |
| UPD \_ completo 0x00000001   | Uma atualização completa deve ser executada.         |
| UPD \_ init 0x00000002   | Uma nova inicialização deve ser executada.  |



 

**\_ fRootPath**: um valor booliano que indica se o campo RootPath especifica um caminho no qual executar a atualização. Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor. Esse campo deve ser definido como 0x00000001 ou 0x00000000. Se definido como 0x00000001, um caminho no qual executar a atualização será incluído em RootPath. Se definido como 0x00000000, a atualização será executada em todos os caminhos indexados.

**RootPath**: o nome do caminho a ser atualizado. Esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor. O nome deve ser uma cadeia de caracteres Unicode terminada em nulo. Esse campo deve ser omitido se \_ fRootPath for definido como 0x00000000.

### <a name="2235-cpmforcemergein"></a>2.2.3.5 CPMForceMergeIn

A mensagem CPMForceMergeIn solicita que um servidor execute qualquer manutenção necessária para melhorar o desempenho da consulta. O servidor responderá com o cabeçalho da mensagem CPMForceMergeIn, com os resultados da solicitação contida no \_ campo status.

O formato da mensagem CPMForceMergeIn que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partid (opcional)



 

**\_ partid**: esse campo deve estar presente quando a mensagem é enviada pelo cliente e deve estar ausente quando a mensagem é enviada pelo servidor. Quando esse campo estiver presente, ele deverá ser definido como 0x00000001.

### <a name="2236-cpmconnectin"></a>2.2.3.6 CPMConnectIn

A mensagem CPMConnectIn inicia uma sessão entre o cliente e o servidor.

O formato da mensagem CPMConnectIn que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_iClientVersion

\_fClientIsRemote

\_cbBlob1

\_cbBlob2

\_margem

...

...

MachineName

... Ela

UserName

... Ela

\_paddingcPropSets (opcional, variável)

cPropSets

PropertySet1 (variável)

PropertySet2 (variável)

\_paddingExtPropset (opcional, variável)

cExtPropSet

aPropertySets (variável)



 

**\_ iClientVersion**: um inteiro de 32 bits que indica se o servidor deve validar o valor de soma de verificação especificado no \_ campo ulChecksum dos cabeçalhos de mensagem para as mensagens enviadas pelo cliente. Se o \_ campo iClientVersion for definido como 0x00000008 ou superior, o servidor deverá validar o \_ valor do campo ulChecksum para as seguintes mensagens:

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMFetchValueIn
-   CPMGetRowsIn
-   CPMSetBindingsIn

Para obter detalhes sobre como o servidor valida o valor especificado pelo cliente no campo ulChecksum para as mensagens listadas acima, consulte a seção 3.2.5.

Se o valor for maior que 0x00000008, o cliente será considerado capaz de manipular deslocamentos de 64 bits em mensagens CPMGetRowsOut. Consulte a seção 2.2.3.16 para obter detalhes.

*Comportamento do Windows: em clientes Windows, o iClientVersion é definido da seguinte maneira*:



| Valor      | Significado                                                              |
|------------|----------------------------------------------------------------------|
| 0x00000005 | O sistema operacional do cliente é o Windows 2000.                                           |
| 0x00000008 | O sistema operacional do cliente é o Windows XP de 32 bits ou o Windows Server 2003 de 32 bits. |
| 0x00010008 | O sistema operacional do cliente é o Windows XP de 64 bits ou o Windows Server 2003 de 64 bits. |



 

\_**fClientIsRemote**: um valor booliano que indica se o cliente está sendo executado em um computador diferente do servidor. DEVE ser definido como 0x00000001.

\_**cbBlob1**: um inteiro de 32 bits sem sinal indicando o tamanho em bytes dos campos CPropSet, PropertySet1 e PropertySet2, combinados.

\_**cbBlob2**: um inteiro de 32 bits sem sinal indicando o tamanho em bytes dos campos CExPropSet e aPropertySet, combinados.

\_**preenchimento**: 12 bytes de preenchimento que podem conter valores arbitrários e devem ser ignorados.

**MachineName**: o nome do computador do cliente. A cadeia de caracteres de nome deve ser uma matriz com terminação nula de menos de 512 caracteres Unicode, incluindo o terminador nulo.

**Username**: uma cadeia de caracteres que representa o nome de usuário da pessoa que está executando o aplicativo que invocou esse protocolo. A cadeia de caracteres de nome deve ser uma matriz com terminação nula de menos de 512 caracteres Unicode quando concatenada com MachineName.

**\_ paddingcPropSets**: esse campo deve ter de 0 a 7 bytes de comprimento. O número de bytes deve ser o número necessário para fazer o deslocamento de bytes do campo cPropSets do início da mensagem que contém essa estrutura ser um múltiplo de 8. O valor dos bytes pode ser qualquer valor arbitrário e deve ser ignorado pelo destinatário.

**cPropSets**: um inteiro de 32 bits sem sinal indicando o número de estruturas CDbPropSet após este campo. Esse valor deve ser definido como 0x0000002.

**PropertySet1**: uma estrutura CDbPropSet com guidPropertySet que contém DBPROPSET \_ FSCIFRMWRK \_ ext (consulte A seção 2.2.1.22).

**PropertySet2**: uma estrutura CDbPropSet com guidPropertySet que contém DBPROPSET \_ CIFRMWRKCORE \_ ext (consulte A seção 2.2.1.22).

\_**PaddingExtPropset**: esse campo deve ter de 0 a 7 bytes de comprimento. O número de bytes deve ser o número necessário para fazer o deslocamento de bytes do campo cExtPropSets do início da mensagem que contém essa estrutura ser um múltiplo de 8. O valor dos bytes pode ser qualquer valor arbitrário e DEVE ser ignorado pelo receptor.

**cExtPropSet:** um inteiro sem sinal de 32 bits que indica o número de estruturas CDbPropSet após esse campo.

**aPropertySets:** uma matriz de estruturas CDbPropSet especificando outras propriedades. O número de elementos nessa matriz DEVE ser igual a cExtPropSet.

### <a name="2237-cpmconnectout"></a>2.2.3.7 CPMConnectOut

A mensagem CPMConnectOut contém uma resposta a uma mensagem CPMConnectIn.

O formato da mensagem CPMConnectOut que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Versão do servidor

\_reservado (variável)



 

**\_ serverVersion:**

Um inteiro de 32 bits, indicando se o servidor pode dar suporte a deslocamentos de 64 *bits.* Consulte a seção 2.2.3.16 para obter detalhes.



| Valor      | Significado                                 |
|------------|-----------------------------------------|
| 0x00000007 | O servidor só pode enviar deslocamentos de 32 bits. |
| 0x00010007 | O servidor pode enviar deslocamentos de 32 ou 64 bits.   |



 

**\_ reservado:** Reservado. O servidor PODE enviar um número arbitrário de valores arbitrários e o cliente DEVERÁ ignorar esses valores se estiver presente.

### <a name="2238-cpmcreatequeryin"></a>2.2.3.8 CPMCreateQueryIn

A mensagem CPMCreateQueryIn cria uma nova consulta. O formato da mensagem CPMCreateQueryIn que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Tamanho

CColumnSetPresent

ColumnSet (opcional)

... (variável)

CRestrictionPresent.

Restrição (opcional)

... (variável)

CSortSetPresent

SortSet (opcional)

... (variável)

CCategorizationSetPresent

CategorizationSet (opcional)

... (variável)

RowSetProperties

...

...

...

...

PidMapper (variável)



 

**Tamanho:** um inteiro sem sinal de 32 bits que indica o número de bytes do início deste campo até o final da mensagem.

**CColumnSetPresent:** um campo de byte que indica se o campo ColumnSet está presente. Esse campo DEVE ser definido como 0x01 ou 0x00. Se definido como 0x01 o campo CColumnSet DEVERÁ estar presente. Se definido como 0x00, ele DEVERÁ estar ausente.

**ColumnSet:** uma estrutura CColumnSet que contém os números de coluna em que as propriedades de CPidMapper devem ser retornadas.

**CRestrictionPresent:** um campo de byte que indica se o campo Restrição está presente. Se definido como qualquer valor que não seja zero, o campo Restrição DEVERÁ estar presente. Se definido como 0x00, a restrição DEVERÁ estar ausente.

**Restrição:** uma estrutura CRestriction que contém a árvore de comandos da consulta.

**CSortSetPresent:** um campo de byte que indica se o campo SortSet está presente. Se definido como qualquer valor diferente de zero, o campo SortSet DEVERÁ estar presente. Se definido como 0x00, SortSet DEVERÁ estar ausente.

**SortSet:** uma estrutura CSortSet que indica a ordem de classificação da consulta.

**CCategorizationSetPresent:** um campo de byte que indica se o campo CCategorizationSet está presente. Se definido como qualquer valor diferente de zero, o campo CCategorizationSet DEVERÁ estar presente. Se definido como 0x00, CCategorizationSet DEVERÁ estar ausente.

**CCategorizationSet:** uma estrutura CCategorizationSet que contém os grupos para a consulta.

**RowSetProperties:** uma estrutura CRowsetProperties que fornece informações de configuração para a consulta.

**PidMapper:** uma estrutura CPidMapper que contém propriedades a retornar em um conjuntos de linhas.

### <a name="2239-cpmcreatequeryout"></a>2.2.3.9 CPMCreateQueryOut

A mensagem CPMCreateQueryOut contém uma resposta a uma mensagem CPMCreateQueryIn.

O formato da mensagem CPMCreateQueryOut que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_fTrueSequential

\_fWorkIdUnique

aCursors



 

**\_ fTrueSequential:** um valor booliano informativo que indica se a consulta pode fornecer resultados mais rapidamente. Quando definido como 0x00000001 para a consulta fornecida em CPMCreateQueryIn, o servidor pode usar o índice de forma que os resultados da consulta provavelmente serão entregues mais rapidamente. Quando definido como 0x00000000, haverá uma latência maior na entrega dos resultados da consulta. NÃO DEVE ser definido como nenhum outro valor.

**\_ fWorkIdUnique:** um valor booliana que indica se os identificadores de documento apontados pelos cursores são exclusivos em todos os resultados da consulta. Se definido como 0x00000001, os identificadores serão exclusivos. Se definido como 0x00000000, eles serão exclusivos somente em todo o conjunto de linhas.

**aCursors:** uma matriz de inteiros sem sinal de 32 bits que representa os alças para cursores, com o número de elementos iguais ao número de categorias no campo CategorizationSet da mensagem CPMCreateQueryIn.

### <a name="22310-cpmgetquerystatusin"></a>2.2.3.10 CPMGetQueryStatusIn

A mensagem CPMGetQueryStatusIn solicita o status de uma consulta. O formato da mensagem CPMGetQueryStatusIn que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor**: um inteiro sem sinal de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual recuperar informações de status.

### <a name="22311-cpmgetquerystatusout"></a>2.2.3.11 CPMGetQueryStatusOut

A mensagem CPMGetQueryStatusOut responde a uma mensagem CPMGetQueryStatusIn com o status da consulta. O formato da mensagem CPMGetQueryStatusOut que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Status



 

**\_ Status**: uma bitmask de valores definida nas tabelas abaixo, que descreve a consulta.

A tabela a seguir lista \_ \* os valores de stat obtidos com a execução de uma operação and bit a bit no \_ status com 0x00000007. O resultado deve ser um dos seguintes:



| Constante                 | Significado                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| STAT \_ ocupado 0x00000000    | A consulta assíncrona ainda está em execução.                                          |
| Erro de STAT \_ 0x00000001   | A consulta está em um estado de erro.                                                   |
| STAT \_ concluído 0x00000002    | A consulta foi concluída.                                                            |
| STAT \_ Refresh 0x00000003 | A consulta foi concluída, mas as atualizações estão resultando em computação de consulta adicional. |



 

A tabela a seguir lista bits de estatística adicionais \_ \* que podem ser definidos de forma independente.



| Constante                                    | Significado                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| STATar \_ palavras de ruído \_ 0x00000010               | Palavras de ruído foram substituídas por caracteres curinga na consulta de conteúdo.                                                              |
| \_Conteúdo \_ de stat fora \_ da \_ Data 0x00000020     | Os resultados da consulta podem estar incorretos porque a consulta envolvia arquivos modificados, mas não indexados.                             |
| STAT \_ Atualizar \_ 0x00000040 incompleta        | Os resultados da consulta podem estar incorretos porque a consulta envolvia arquivos modificados e reindexados cujo conteúdo não foi incluído. |
| 0x00000080 de consulta de conteúdo de STAT \_ \_ \_ incompleto | A consulta de conteúdo era muito complexa para concluir ou requerido a enumeração em vez de usar o índice de conteúdo.                          |
| O \_ limite de tempo de stat \_ \_ excedeu 0x00000100      | Os resultados da consulta podem estar incorretos porque o tempo de execução da consulta atingiu o tempo máximo permitido.                    |



 

### <a name="22312-cpmgetquerystatusexin"></a>2.2.3.12 CPMGetQueryStatusExIn

A mensagem CPMGetQueryStatusExIn solicita o status de uma consulta e informações adicionais, como o número de documentos que foram indexados, o número de documentos restantes a serem indexados e assim por diante. O formato da mensagem CPMGetQueryStatusExIn que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_bmk



 

**\_ hCursor**: um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual recuperar informações de status.

**\_ BMK**: um valor de 32 bits que indica o identificador de um indicador cuja posição deve ser recuperada.

### <a name="22313-cpmgetquerystatusexout"></a>2.2.3.13 CPMGetQueryStatusExOut

A mensagem CPMGetQueryStatusExOut responde a uma mensagem CPMGetQueryStatusExIn com o status da consulta e outras informações de status, conforme descrito no diagrama a seguir. O formato da mensagem CPMGetQueryStatusExOut que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Status

\_cFilteredDocuments

\_cDocumentsToFilter

\_dwRatioFinishedDenominator

\_dwRatioFinishedNumerator

\_iRowBmk

\_cRowsTotal



 

**\_ Status**: um dos stats \_ \* valores especificados na seção 2.2.3.11.

**\_ cFilteredDocuments**: um inteiro sem sinal de 32 bits indicando o número de documentos que foram indexados

**\_ cDocumentsToFilter**: um inteiro de 32 bits sem sinal indicando o número de documentos que ainda permanecem para serem indexados.

**\_ dwRatioFinishedDenominator**: um inteiro de 32 bits sem sinal indicando o denominador da proporção de documentos que a consulta concluiu o processamento.

**\_ dwRatioFinishedNumerator**: um inteiro de 32 bits sem sinal indicando o numerador da proporção de documentos que a consulta concluiu o processamento.

**\_ iRowBmk**: um inteiro de 32 bits sem sinal indicando a posição aproximada do indicador no conjunto de linhas em termos de linhas.

**\_ cRowsTotal**: um inteiro de 32 bits sem sinal especificando o número total de linhas no conjunto de linhas.

### <a name="22314-cpmsetbindingsin"></a>2.2.3.14 CPMSetBindingsIn

A mensagem CPMSetBindingsIn solicita a associação de colunas a um conjunto de linhas. O servidor responderá à mensagem de solicitação CPMSetBindingsIn usando a seção de cabeçalho da mensagem CPMBindingsIn com os resultados da solicitação contida no \_ campo status. O formato da mensagem CPMSetBindingsIn que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (opcional)

\_cbRow (opcional)

\_cbBindingDesc (opcional)

\_fictício (opcional)

cColumns (opcional)

aColumns (variável, opcional)



 

**\_ hCursor:** um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a linha para a qual definir as vinculações. Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.

**\_ cbRow:** um inteiro sem sinal de 32 bits que indica o tamanho, em bytes, de uma linha. Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.

**\_ cbBindingDesc:** um inteiro sem sinal de 32 bits que indica o comprimento, em bytes, dos campos após o \_ campo fictício. Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.

**\_ fictício:** esse campo não está sendo usada e DEVE ser ignorado. Ele pode ser definido como qualquer valor arbitrário. Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.

**cColumns:** um inteiro sem sinal de 32 bits que indica o número de elementos na matriz aColumns. Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.

**aColumns:** uma matriz das estruturas CTableColumn que descrevem as colunas de uma linha no conjunto de linhas. Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor. As estruturas na matriz DEVEM ser separadas por 0 a 3 bytes de preenchimento, de forma que cada estrutura tenha um alinhamento de 4 bytes do início de uma mensagem. Esses bytes de preenchimento podem ser qualquer valor arbitrário e DEVEM ser ignorados no recebimento.

### <a name="22315-cpmgetrowsin"></a>2.2.3.15 CPMGetRowsIn

A mensagem CPMGetRowsIn solicita linhas de uma consulta. O formato da mensagem CPMGetRowsIn que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Hcursor

\_cRowsToTransfer

\_cbRowWidth

\_cbSeek

\_cbReserved

\_cbReadBuffer

\_ulClientBase

\_fBwdFetch

Etype

\_chapt

SeekDescription

...

... (variável)



 

**\_ hCursor:** um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual recuperar linhas.

**\_ cRowsToTransfer:** um inteiro sem sinal de 32 bits que indica o número máximo de linhas que o cliente deseja receber em resposta a essa mensagem.

**\_ cbRowWidth:** um inteiro sem sinal de 32 bits que indica o comprimento de uma linha, em bytes.

**\_ cbSeek:** um inteiro sem sinal de 32 bits que indica o tamanho da mensagem que começa com eType.

**\_ cbReserved:** um inteiro sem sinal de 32 bits que indica o tamanho, em bytes, de uma mensagem CPMGetRowsOut (sem os campos Linhas e SeekDescriptions). Esse valor nesse campo é adicionado ao valor do campo cbSeek e, em seguida, deve ser usado para calcular o deslocamento do campo Linhas na mensagem \_ CPMGetRowsOut.

**\_ cbReadBuffer:** um inteiro sem sinal de 32 bits que DEVE ser definido como o máximo do valor \_ de cbRowWidth ou 1000 vezes o valor de cRowsToTransfer, arredondado para o múltiplo de \_ 512 byte mais próximo. O valor NÃO DEVE exceder 0x00004000.

**\_ ulClientBase:** um inteiro sem sinal de 32 bits que indica o valor base a ser usado para cálculos de ponteiro no buffer de linha. Se deslocamentos de 64 bits estão sendo usados, o campo reservado2 do header da mensagem é usado como os 32 bits superiores e ulClientBase como os 32 bits inferiores de um valor de \_ 64 bits. Consulte a seção 2.2.3.16 para obter detalhes.

**\_ fBwdFetch:** um inteiro sem sinal de 32 bits que indica a ordem na qual buscar as linhas. Se definido como 0x00000001, as linhas deverão ser buscadas na ordem inversa. Se definido como 0x00000000, as linhas deverão ser buscadas na ordem de encaminhamento. Não deve ser definido para nenhum outro valor.

**ETYPE**: um inteiro sem sinal de 32 bits contendo um dos valores a seguir para indicar o tipo de operação a ser executada.



| Valor                         | Significado                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowSeekNext 0x00000001       | SeekDescription contém uma estrutura CRowSeekNext.       |
| eRowSeekAt 0x00000002         | SeekDescription contém uma estrutura CRowSeekAt.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription contém uma estrutura CRowSeekAtRatio.    |
| eRowSeekByBookmark 0x00000004 | SeekDescription contém uma estrutura CRowSeekByBookmark. |



 

**\_ chapt**: um valor de 32 bits que representa o identificador do capítulo do conjunto de linhas.

**SeekDescription**: esse campo deve conter uma estrutura do tipo indicado pelo valor de ETYPE.

### <a name="22316-cpmgetrowsout"></a>2.2.3.16 CPMGetRowsOut

A mensagem CPMGetRowsOut responde a uma mensagem CPMGetRowsIn com as linhas de uma consulta. Os servidores devem Formatar deslocamentos para tipos de dados de comprimento variável no campo linhas da seguinte maneira:

-   O cliente indicou que era um sistema de 32 bits (0x00000008 ou menos no campo iClientVersion de CPMConnectIn): os deslocamentos são inteiros de 32 bits.
-   O cliente indicou que era um sistema de 64 bits ( \_ iClientVersion > 0x00000008 no CPMConnectIn) e o servidor indicou que era um sistema de 32 bits ( \_ serverVersion definido como 0X00000007 em CPMConnectOut): os deslocamentos são inteiros de 32 bits
-   O cliente indicou que era um sistema de 64 bits ( \_ iClientVersion > 0x00000008 no CPMConnectIn) e o servidor indicou que era um sistema de 64 bits ( \_ serverVersion definido como 0X00010007 em CPMConnectOut): os deslocamentos são inteiros de 64 bits

O formato da mensagem CPMGetRowsOut que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cRowsReturned

eType

\_chapt

SeekDescription (opcional, variável)

...

...

paddingRows (opcional, variável)

Linhas



 

**\_ cRowsReturned**: um inteiro de 32 bits sem sinal indicando o número de linhas retornadas em linhas.

**ETYPE**: um inteiro sem sinal de 32 bits contendo um dos seguintes valores para indicar o tipo de operação de busca a ser executada



| Valor                         | Significado                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowsSeekNone 0x00000000      | Sem SeekDescription, ignore o campo SeekDescription.        |
| eRowSeekNext 0x00000001       | SeekDescription contém uma estrutura CRowSeekNext.       |
| eRowSeekAt 0x00000002         | SeekDescription contém uma estrutura CRowSeekAt.         |
| eRowSeekAtRatio 0x00000003    | SeekDescription contém uma estrutura CRowSeekAtRatio.    |
| eRowSeekByBookmark 0x00000004 | SeekDescription contém uma estrutura CRowSeekByBookmark. |



 

**\_ chapt**: um valor de 32 bits que representa o identificador do capítulo do conjunto de linhas.

**SeekDescription**: esse campo deve conter uma estrutura do tipo indicado pelo campo ETYPE.

**paddingRows**: esse campo deve ter comprimento suficiente (0 a \_ cbReserved-1 bytes) para preencher o campo de linhas para o \_ deslocamento de cbReserved do início de uma mensagem, em que \_ cbReserved é o valor na mensagem CPMGetRowsIn. Os bytes de preenchimento usados nesse campo podem ser de qualquer valor arbitrário. Este campo deve ser ignorado pelo destinatário.

**Linhas**: dados de linha, são formatados conforme prescrito pelas informações de coluna na mensagem CPMSetBindingsIn mais recente. As linhas devem ser armazenadas na ordem de encaminhamento (por exemplo, linha 1 antes da linha 2).

Colunas de tamanho fixo devem ser armazenadas nos deslocamentos especificados pela mensagem CPMSetBindingsIn mais recente.

Colunas de tamanho variável (por exemplo, cadeias de caracteres) devem ser armazenadas da seguinte maneira:

-   A variável de dados em si (por exemplo, a cadeia de caracteres) é armazenada perto do final do buffer em ordem decrescente (por exemplo, a coleção de todos os dados da variável para a linha 1 está no final, linha 2 mais próxima, etc.).
-   A área de tamanho fixo (no início do buffer de linha) deve conter um CRowVariant para cada coluna, armazenado no deslocamento especificado na mensagem de CPMSetBindingsIn mais recente. vType deve conter o tipo de dados (ex: VT \_ LPWSTR). Se, conforme determinado pelas regras no início da seção, esta seção, os deslocamentos de 32 bits estão sendo usados, o campo de deslocamento em CRowVariant deve conter um valor de 32 bits que é o deslocamento dos dados da variável do início da mensagem CPMGetRowsOut, mais o valor de \_ ulClientBase especificado na mensagem de CPMGetRowsIn mais recente. Se os deslocamentos de 64 bits estiverem sendo usados, o campo de deslocamento em CRowVariant deverá conter um valor de 64 bits que é o deslocamento do início da mensagem CPMGetRowsOut, adicionado a um valor de 64 bits composto por meio de \_ ulClientBase como baixo 32-bits e \_ ulReserved2 como o alto 32 bits.

Por exemplo, se a mensagem CPMSetBindingsIn especificou duas colunas-size (VT \_ i4) e Title (VT \_ LPWSTR)-e \_ ulClientBase de CPMGetRowsIn for 0x10000, duas linhas aparecerão da seguinte maneira. A seção marcada em cinza é a parte de comprimento fixo do buffer.

![exemplo de mensagem cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a>2.2.3.17 CPMRatioFinishedIn

A mensagem CPMRatioFinishedIn solicita a porcentagem de conclusão de uma consulta. O formato da mensagem CPMRatioFinishedIn que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Hcursor

\_fQuick



 

**\_ hCursor:** o identificador da mensagem CPMCreateQueryOut que identifica a consulta para a qual solicitar informações de conclusão.

**\_ fQuick**: DEVE ser definido como 0x00000001. Não usada e DEVE ser ignorada pelo servidor.

### <a name="22318-cpmratiofinishedout"></a>2.2.3.18 CPMRatioFinishedOut

A mensagem CPMRatioFinishedOut responde a uma mensagem CPMRatioFinishedIn com a taxa de conclusão de uma consulta. O formato da mensagem CPMRatioFinishedOut que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ ulNumerator

\_ulDenominator

\_Corvos

\_fNewRows



 

**\_ ulNumerator:** um inteiro sem sinal de 32 bits que indica o numerador da taxa de conclusão em termos de linhas.

**\_ ulDenominator:** um inteiro sem sinal de 32 bits que indica o denominador da taxa de conclusão em termos de linhas. DEVE ser maior que zero.

**\_ cRows:** um inteiro sem sinal de 32 bits que indica o número total de linhas para a consulta.

**\_ fNewRows:** um valor booliana que indica se há novas linhas disponíveis. Um valor de 0x00000001 indica que novas linhas estão disponíveis no conjuntos de linhas. Um valor de 0x00000000 indica que o conjuntos de linhas não contém nenhuma nova linha. Esse campo NÃO DEVE ser definido como nenhum outro valor.

### <a name="22319-cpmfetchvaluein"></a>2.2.3.19 CPMFetchValueIn

A mensagem CPMFetchValueIn solicita um valor de propriedade muito grande para retornar em um conjuntos de linhas. Conforme especificado na seção 3.2.4.2.5, essa mensagem é enviada repetidamente para recuperar todos os bytes da propriedade, atualizando cbSoFar para cada um, até que o campo fMoreExists da mensagem \_ \_ CPMFetchValueOut seja definido como **FALSE.**

O formato da mensagem CPMFetchValueIn que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Wid

\_cbSoFar

\_cbPropSpec

\_cbChunk

PropSpec (variável)

...

\_preenchimento (variável)



 

**\_ wid:** um inteiro sem sinal de 32 bits que contém informações sobre a ID do documento que identifica o documento para o qual uma propriedade deve ser buscada.

**\_ cbSoFar:** um inteiro sem sinal de 32 bits que contém o número de bytes transferidos anteriormente para essa propriedade. DEVE ser definido como 0x00000000 na primeira mensagem.

**\_ cbPropSpec:** um inteiro sem sinal de 32 bits que contém o tamanho do campo PropSpec, em bytes.

**\_ cbChunk:** um inteiro sem sinal de 32 bits que contém o número máximo de bytes que o remetente pode aceitar em uma mensagem CPMFetchValueOut.

*Comportamento do Windows: esse campo é definido como 0x00004000 para todas as versões do Windows.*

**PropSpec:** uma estrutura CFullPropSpec especificando a propriedade a ser recuperada.

**\_ preenchimento:** esse campo DEVE ter o comprimento necessário (de 0 a 3 bytes) para pad da mensagem para um múltiplo de 4 bytes de comprimento. O valor dos bytes de preenchimento pode ser qualquer valor arbitrário. Esse campo DEVE ser ignorado pelo receptor.

### <a name="22320-cpmfetchvalueout"></a>2.2.3.20 CPMFetchValueOut

A mensagem CPMFetchValueOut responde a uma mensagem CPMFetchValueIn com um valor de propriedade de uma consulta anterior. Conforme especificado na seção 3.1.5.2.8, essa mensagem é enviada após cada mensagem CPMFetchValueIn até que todos os bytes da propriedade sejam transferidos.

O formato da mensagem CPMFetchValueOut que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Cbvalue

\_fMoreExists

\_fValueExists

vType

vValue (variável)



 

**\_ cbValue:** um inteiro sem sinal de 32 bits que contém o tamanho total, em bytes em vValue.

**\_ fMoreExists:** um valor booliana que indica se há mensagens CPMFetchValueOut adicionais disponíveis. Se definido como 0x00000001, haverá mensagens CPMFetchValueOut adicionais. Se definido como 0x00000000, não haverá mensagens CPMFetchValueOut adicionais disponíveis.

**\_ fValueExists:** um valor booliana que indica se há um valor para a propriedade . Se definido como 0x00000001, existe um valor para a propriedade . Se definido como 0x00000000, um valor para a propriedade não existirá.

**vType:** um valor da enumeração VARENUM, consulte a Seção 2.2.1.1 para obter detalhes, descrevendo o tipo da propriedade.

**vValue:** uma parte de uma matriz de byte que contém uma estrutura SERIALIZEDPROPERTYVALUE, conforme especificado na seção 2.2.1.32, em que o deslocamento do início da parte é o valor \_ de cbSoFar em CPMFetchValueIn. O comprimento da parte, indicado pelo campo cbValue, DEVE ser igual ao valor de \_ \_ cbChunk em CPMFetchValueIn se fMoreExists estiver definido como 0x00000001 e DEVE ser menor ou igual ao valor \_ de \_ cbChunk, caso contrário.

### <a name="22321-cpmgetnotify"></a>2.2.3.21 CPMGetNotify

A mensagem CPMGetNotify solicita que o cliente queira ser notificado sobre alterações no conjuntos de linhas.

A mensagem NÃO DEVE incluir um corpo; somente o header da mensagem, conforme especificado na Seção 2.2.2, deve ser enviado.

### <a name="22322-cpmsendnotifyout"></a>2.2.3.22 CPMSendNotifyOut

A mensagem CPMSendNotifyOut notifica o cliente de uma alteração nos resultados de uma consulta.

Essa mensagem só é enviada quando ocorre uma alteração. O formato da mensagem CPMSendNotifyOut que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_watchNotify



 

**\_ watchNotify:** a alteração na consulta. Ele DEVE ser um dos seguintes valores:



| Valor                                     | Significado                                             |
|-------------------------------------------|-----------------------------------------------------|
| DBWATCHNOTIFY \_ ROWSCHANGED 0X00000001     | O número de linhas no conjuntos de linhas de consulta foi alterado. |
| DBWATCHNOTIFY \_ QUERYDONE 0x00000002       | A consulta foi concluída.                            |
| DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003 | A consulta foi executada de uma vez.                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a>2.2.3.23 CPMGetApproximatePositionIn

A mensagem CPMGetApproximatePositionIn solicita a posição aproximada de um indicador em um capítulo. O formato da mensagem CPMGetApproximatePositionIn que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Hcursor

\_chapt

\_Bmk



 

**\_ hCursor:** um valor de 32 bits que representa o cursor de consulta obtido de CPMCreateQueryOut para o conjuntos de linhas que contém o indicador.

**\_ chapt:** um valor de 32 bits que representa o handle para o capítulo que contém o indicador.

**\_ bmk:** um valor de 32 bits que representa o indicador para o qual recuperar a posição aproximada.

### <a name="22324-cpmgetapproximatepositionout"></a>2.2.3.24 CPMGetApproximatePositionOut

A mensagem CPMGetApproximatePositionOut responde a uma mensagem CPMGetApproximatePositionIn que descreve a posição aproximada do indicador no capítulo. O formato da mensagem CPMGetApproximatePositionOut que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_numerator

\_denominator



 

**\_ numerador**: um inteiro de 32 bits sem sinal contendo o número de linha do indicador no conjunto de linhas. Se não houver linhas, esse campo deverá ser definido como 0x00000000.

**\_ denominador**: um inteiro sem sinal de 32 bits contendo o número de linhas no conjunto de linhas.

### <a name="22325-cpmcomparebmkin"></a>2.2.3.25 CPMCompareBmkIn

A mensagem CPMCompareBmkIn solicita uma comparação de dois indicadores em um capítulo.

O formato da mensagem CPMCompareBmkIn que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chapt

\_bmkFirst

\_bmkSecond



 

\_**hCursor**: um valor de 32 bits que representa o identificador da mensagem CPMCreateQueryOut para o conjunto de linhas que contém os indicadores.

\_**chapt**: um valor de 32 bits que representa o identificador do capítulo que contém os indicadores a serem comparados.

\_**bmkFirst**: um valor de 32 bits que representa o identificador para o primeiro indicador a ser comparado.

\_**bmkSecond**: um valor de 32 bits que representa o identificador para o segundo indicador a ser comparado.

### <a name="22326-cpmcomparebmkout"></a>2.2.3.26 CPMCompareBmkOut

A mensagem CPMCompareBmkOut responde a uma mensagem CPMCompareBmkIn com a comparação dos dois indicadores no capítulo. O formato da mensagem CPMCompareBmkOut que segue o cabeçalho é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwComparison



 

\_**dwComparison**: um dos valores a seguir, indicando as posições relativas dos dois indicadores no capítulo.



| Valor                               | Significado                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| DBCOMPARE \_ LT 0x00000000            | O primeiro indicador é posicionado antes do segundo.               |
| DbCOMPARE \_ EQ 0x00000001            | O primeiro indicador tem a mesma posição que o segundo.           |
| DBCOMPARE \_ GT 0x00000002            | O primeiro indicador é posicionado após o segundo.                |
| DBCOMPARE \_ NE 0x00000003            | O primeiro indicador não tem a mesma posição que o segundo. |
| DBCOMPARE \_ NOTCOMPARABLE 0X00000004 | O primeiro indicador não é comparável ao segundo.               |



 

### <a name="22327-cpmrestartpositionin"></a>2.2.3.27 CPMRestartPositionIn

A mensagem CPMRestartPositionIn move a posição de busca de um cursor para o início do capítulo. Conforme especificado na seção 3.1.5.2.12, o servidor responderá usando a mesma mensagem, com os resultados da solicitação contidos no campo de status do \_ header do CISP.

O formato da mensagem CPMRestartPositionIn que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (opcional)

\_chapt (opcional)



 

**\_ hCursor:** um valor de 32 bits que representa o identificador, obtido de uma mensagem CPMCreateQueryOut, que identifica a consulta para a qual reiniciar a posição. Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.

**\_ chapt:** um valor de 32 bits que representa o alça de um capítulo do qual recuperar linhas. Esse campo DEVE estar presente quando a mensagem é enviada pelo cliente e DEVE estar ausente quando a mensagem é enviada pelo servidor.

### <a name="22328-cpmfreecursorin"></a>2.2.3.28 CPMFreeCursorIn

A mensagem CPMFreeCursorIn solicita a liberação de um cursor. O formato da mensagem CPMFreeCursorIn que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Hcursor



 

**\_ hCursor:** um valor de 32 bits que representa o handle do cursor da mensagem CPMCreateQueryOut a ser liberado.

### <a name="22329-cpmfreecursorout"></a>2.2.3.29 CPMFreeCursorOut

A mensagem CPMFreeCursorOut responde a uma mensagem CPMFreeCursorIn com os resultados da liberação de um cursor. O formato da mensagem CPMFreeCursorOut que segue o header é:



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cCursorsRemaining



 

**\_ cCursorsRemaining:** um inteiro sem sinal de 32 bits que indica o número de cursores ainda em uso para a consulta.

### <a name="22330-cpmdisconnect"></a>2.2.3.30 CPMDisconnect

A mensagem CPMDisconnect encerra a conexão com o servidor

A mensagem NÃO DEVE incluir um corpo; somente o header da mensagem, conforme especificado na Seção 2.2.2 deve ser enviado.

### <a name="224-errors"></a>2.2.4 Erros

Todas as mensagens do Protocolo do Serviço de Indexação de Conteúdo DEVEM retornar 0x00000000 êxito; caso contrário, eles retornarão um código de erro de 32 bits diferente de zero que pode ser um HRESULT ou um valor NTSTATUS (consulte a seção 1.8). Se um buffer for muito pequeno para se ajustar a um resultado, um código de status de STATUS \_ INSUFFICIENT RESOURCES (0xC0000009A) DEVERÁ ser retornado e a operação com falha deverá ser recuperada com um \_ buffer maior.

Todos os outros valores de erro DEVEM ser tratados da mesma forma.

(Observe que, atualmente, os espaços de numeração HRESULT e NTSTATUS não se sobrepõem, exceto com valores de significado idêntico, mas mesmo se fossem conflitos no futuro, isso não causaria problemas de protocolo, desde que o valor para STATUS \_ RECURSOS \_ INSUFICIENTES permanecem exclusivos, pois todos os outros valores de erro são tratados da mesma forma.)

## <a name="3-protocol-details"></a>3 Detalhes do protocolo

-   [3.1 Detalhes do servidor](#31-server-details)
-   [3.2 Detalhes do cliente](#32-client-details)

As solicitações de mensagem cisp para consultar remotamente os catálogos de serviço de indexação não exigem nenhuma sequência específica. No entanto, é aconselhável que a camada superior adera a uma sequência de mensagens significativa, quanto às mensagens recebidas fora dessa sequência ou com dados inválidos, o servidor responderá com um erro. Algumas mensagens também dependem da camada superior, fornecendo dados válidos que foram recebidos em mensagens anteriormente na sequência.

Uma sequência de mensagens típica para uma consulta simples de um cliente para um computador remoto é ilustrada no diagrama a seguir.

![sequência de mensagens para consulta simples](images/protocoldetails.jpg)

As mensagens representadas no diagrama anterior representam um subconjunto de todas as mensagens CISP usadas para consultar um catálogo de serviços de indexação remota.

### <a name="31-server-details"></a>3.1 Detalhes do servidor

### <a name="311-abstract-data-model"></a>3.1.1 Modelo de dados abstratos

A seção a seguir especifica os dados e o estado mantidos pelo servidor CISP. Os dados fornecidos aqui são para facilitar a explicação de como o protocolo se comporta. Esta seção não determina que as implementações aderam a esse modelo, desde que seu comportamento externo seja consistente com o descrito neste documento.

Um serviço de indexação que implementa o CISP DEVE manter os seguintes elementos de dados abstratos:

-   A lista de clientes conectados ao servidor
-   Informações sobre cada cliente, que inclui:
-   -   Versão do cliente (conforme indicado na mensagem CPMConnectIn especificada na seção 2.2.3.6)
    -   Catálogo associado ao cliente (por uma mensagem CPMConnectIn)
    -   Propriedades adicionais do cliente, conforme especificado na seção 2.2.1.21.1.
    -   Consulta de pesquisa do cliente
    -   Lista de alças de cursor para a consulta e a posição no conjunto de resultados para cada alça.
    -   Conjunto atual de vinculações
    -   Status atual da consulta que inclui (para cada cursor):
    -   -   Número de linhas no resultado da consulta
        -   Numerador e denominador da conclusão da consulta
        -   Último número de linhas, relatado pela mensagem CPMRatioFinishedOut mais recente para este cursor
        -   Se a consulta é monitorada pelo servidor quanto a alterações nos resultados da consulta e se ela é monitorada, o que mudou nos resultados da consulta desde que foi relatado pela última vez ao cliente pelo CPMSendNotifyOut
        -   Lista de alças de capítulos, atendidas por essa consulta a um cliente.
        -   Lista de alças de indicador para cada cursor, atendida por essa consulta a um cliente.

-   O estado atual do serviço de indexação, que pode ser "não inicializado", "em execução" ou "desligando". Observe que, na maioria das vezes, o servidor está no estado "em execução". A seguir está o diagrama do computador de estado para o servidor:

    ![diagrama do computador de estado do servidor de serviço de indexação](images/abstractdatamodel.jpg)

-   Informações por catálogo: número de documentos indexados, tamanho do índice, número de chaves exclusivas, etc (consulte a seção 2.2.3.1 para obter a lista completa), estado (que corresponde aos valores de dwNewState na seção 2.2.3.2).
-   Para cada idioma com suporte, um banco de dados de variações de palavras, conforme discutido na seção 2.2.1.3.

### <a name="312-timers"></a>3.1.2 Temporizadores

Nenhum temporizador de protocolo é necessário.

### <a name="313-initialization"></a>3.1.3 Inicialização

Na inicialização, o servidor deve definir seu estado como "não inicializado" e começar a escutar mensagens no pipe nomeado especificado na seção 1,9. Depois de fazer qualquer outra inicialização interna, ela deve fazer a transição para o estado "em execução".

### <a name="314-higher-layer-triggered-events"></a>3.1.4 Eventos disparados de camada superior

Nenhum.

### <a name="315-message-processing-and-sequencing-rules"></a>Processamento de mensagens 3.1.5 e regras de sequenciamento

Sempre que ocorrer um erro durante o processamento de uma mensagem enviada por um cliente, o servidor deverá relatar um erro de volta ao cliente da seguinte maneira:

-   Parar o processamento da mensagem enviada pelo cliente
-   Responda com o cabeçalho da mensagem (somente) da mensagem enviada pelo cliente, mantendo o \_ campo msg intacto.
-   Defina o \_ campo status para o valor do código de erro.

Quando uma mensagem chega, o servidor deve verificar o \_ valor do campo msg para ver se ele é um tipo conhecido (consulte a seção 2.2.2). Se o tipo não for conhecido, ele deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.

O servidor deve validar o \_ valor do campo ulChecksum se o tipo de mensagem for um dos seguintes:

-   CPMConnectIn (0x000000C8)
-   CPMCreateQueryIn (0x000000CA)
-   CPMSetBindingsIn (0x000000D0)
-   CPMGetRowsIn (0x000000CC)
-   CPMFetchValueIn (0x000000E4)

Para validar o \_ valor do campo ulChecksum, o servidor deve verificar o valor especificado pelo cliente no \_ campo iClientVersion da mensagem CPMConnectIn.

Se o \_ campo iClientVersion não estiver definido como 0x00000008 e o \_ campo ulChecksum não estiver definido como 0x00000000, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status. O servidor não deve validar o \_ campo ulChecksum para clientes defina o \_ campo iClientVersion com um valor menor que 0x00000008.

Se o \_ valor do campo iClientVersionfield for 0x00000008 ou superior, o servidor deverá validar que o \_ campo ulChecksum foi calculado conforme especificado na seção 3.2.4. Se o \_ valor de ulChecksum for inválido, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0XC000000D) de status.

Em seguida, o servidor verifica em qual estado ele está. Se seu estado for "não inicializado", o servidor deverá relatar \_ um \_ erro CI E não \_ inicializado (0x8004180B). Se o estado for "desligando", o servidor deverá relatar \_ um \_ erro de desligamento CI E Shutdown (0x80041812).

Depois que um cabeçalho for determinado como válido e o servidor estar no estado "em execução", o processamento adicional específico à mensagem deverá ser feito conforme especificado nas subseções abaixo.

### <a name="3151-remote-indexing-service-catalog-management"></a>Gerenciamento de catálogo do serviço de indexação remota do 3.1.5.1

### <a name="31511-receiving-a-cpmcistateinout-request"></a>3.1.5.1.1 recebendo uma solicitação CPMCiStateInOut

Quando o servidor recebe uma solicitação de mensagem CPMCIStateInOut do cliente, o servidor deve primeiro verificar se o cliente está em uma lista de clientes conectados. Se o cliente não estiver na lista, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status. Caso contrário, ele deve responder ao cliente com uma mensagem CPMCIStateInOut, preenchendo-o com informações sobre o catálogo associado do cliente, conforme especificado na seção 2.2.3.1.

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a>3.1.5.1.2 recebendo uma solicitação CPMSetCatStateIn

Quando o servidor recebe uma solicitação de mensagem CPMSetCatStateIn do cliente, o servidor deve fazer o seguinte:

-   Verifique se o cliente tem acesso administrativo. Se o cliente não tiver acesso administrativo, o servidor deverá relatar um erro de STATUS de \_ acesso \_ negado (0xC0000022).
-   Se \_ dwNewState não for igual a CICAT \_ todos \_ abertos, altere o estado do catálogo especificado no campo CatName conforme especificado pelo \_ campo dwNewState. Consulte a seção 2.2.3.2 para obter mais detalhes. Se o servidor não localizar um catálogo com o nome especificado no campo CatName, o servidor deverá retornar um \_ erro de parâmetro inválido \_ (0xC000000D) de status.
-   Responda ao cliente com uma mensagem CPMSetCatStateOut, em que \_ DWOLDSTATE deve ser definido como o estado anterior do catálogo. Se \_ dwNewState for igual a CICAT \_ todos \_ abertos, o servidor deverá verificar o status de todos os catálogos e, se todos eles forem iniciados, ele deverá definir \_ dwOldState como 0x00000001 e, caso contrário, definirá \_ dwOldState como 0x00000000.

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a>3.1.5.1.3 recebendo uma solicitação CPMUpdateDocumentsIn

Quando o servidor recebe uma solicitação de mensagem CPMUpdateDocumentsIn, o servidor deve fazer o seguinte:

-   Verifique se o cliente está em uma lista de clientes conectados (que têm um catálogo associado). Se o cliente não estiver na lista, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.
-   Verifique se o cliente tem acesso administrativo. Se o cliente não tiver acesso administrativo ao servidor, o servidor deverá relatar um erro de STATUS de \_ acesso \_ negado (0xC0000022).
-   Inicie o processo de indexação do caminho especificado pelo cliente, fazendo uma verificação completa ou incremental, dependendo do valor do \_ campo sinalizador na mensagem CPMUpdateDocumentsIn. Se o caminho não tiver sido indexado anteriormente, ele deverá ser adicionado à coleção de locais indexados e uma verificação completa realizada. Se um valor ilegal do \_ campo flag for especificado, o servidor deverá agir como se o \_ sinalizador fosse definido como UPD \_ init e executar uma verificação completa. Esta operação deve ser executada no catálogo associado ao cliente.
-   Responda ao cliente com o cabeçalho da mensagem para o CPMUpdateDocumentsIn e defina o \_ campo status para os resultados da solicitação.

### <a name="31514-receiving-a-cpmforcemergein-request"></a>3.1.5.1.4 recebendo uma solicitação CPMForceMergeIn

Quando o servidor recebe uma solicitação de mensagem CPMForceMergeIn, o servidor deve fazer o seguinte:

-   Verifique se o cliente está em uma lista de clientes conectados (que têm um catálogo associado). Se o cliente não estiver na lista, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.
-   Verifique se o cliente tem acesso administrativo. Se o cliente não tiver acesso administrativo, o servidor deverá relatar um erro de STATUS de \_ acesso \_ negado (0xC0000022).
-   Inicie qualquer processo de manutenção necessário para melhorar o desempenho de consulta em um catálogo, associado ao cliente.
-   Responda ao cliente com um cabeçalho de mensagem para o CPMForceMergeIn e defina o \_ campo status para os resultados da solicitação.

Observe que o processo de manutenção é assíncrono e pode continuar depois que o cliente recebe a mensagem de resposta. Esse processo não afeta diretamente o protocolo de nenhuma forma (além do tempo de resposta).

### <a name="3152-remote-indexing-service-querying"></a>Consulta do serviço de indexação remota do 3.1.5.2

### <a name="31521-receiving-a-cpmconnectin-request"></a>3.1.5.2.1 recebendo uma solicitação CPMConnectIn

Quando o servidor recebe uma solicitação CPMConnectIn de um cliente, o servidor deve fazer o seguinte:

-   Verifique se o cliente está na lista de clientes conectados. Se esse for o caso, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.
-   Verifica se o catálogo especificado existe e não está no estado parado. Se esse não for o caso, o servidor deverá ter um erro de CI \_ E \_ nenhum \_ catálogo (0x8004181D) de relatório.
-   Adicione o cliente à lista de clientes conectados.
-   Associe o catálogo ao cliente.
-   Armazene as informações passadas na mensagem CPMConnectIn (como nome do catálogo, versão do cliente, etc.) no estado do cliente.
-   Responda ao cliente com uma mensagem CPMConnectOut.

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a>3.1.5.2.2 recebendo uma solicitação CPMCreateQueryIn

Quando o servidor recebe uma solicitação de mensagem CPMCreateQueryIn de um cliente, o servidor deve fazer o seguinte:

-   Verifique se o cliente está na lista de clientes conectados. Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.
-   Verifique se o cliente já tem uma consulta associada a ele. Se esse for o caso, o servidor deverá relatar um \_ erro de \_ parâmetro inválido (0xC000000D) de status.
-   Verifique se o catálogo associado ao cliente está no estado que permite que a consulta seja processada (CICAT \_ ReadOnly ou CICAT \_ gravável). Se esse não for o caso, o servidor deverá relatar um \_ erro de \_ 0x8004160C (consulta S sem \_ consulta).
-   Analise o conjunto de restrições, as ordens de classificação e os agrupamentos especificados na consulta. Se o servidor encontrar um erro, ele deverá relatar um erro apropriado. Se essa etapa falhar por qualquer outro motivo, o servidor deverá relatar o erro encontrado. Para obter informações sobre erros de consulta de serviço de indexação, consulte \[ msdn-QUERYERR \] .
-   Salve a consulta de pesquisa no estado do cliente.
-   Faça qualquer preparação necessária para atender linhas a um cliente e associar a consulta a identificadores de cursor apropriados (dependendo das informações passadas na mensagem CPMCreateQueryIn).
-   Adicione esses identificadores à lista de identificadores de cursor do cliente e inicialize as listas de identificadores e indicadores de capítulo.
-   Inicializar a lista de identificadores de capítulo para cada cursor nesta consulta para DB \_ NULL \_ HCHAPTER
-   Inicializar a lista de identificadores de indicadores para cada cursor nesta consulta para um conjunto de DBBMK \_ First e DBBMK \_ Last.
-   Marque a consulta como não monitorado para alterações.
-   Inicialize o número de linhas para o número de linhas calculado no momento (que pode ser 0 se a consulta não começar a ser executada ou algum número se a consulta estiver em um processo de execução) e inicialize o numerador e o denominador da conclusão da consulta.
-   Responda ao cliente com uma mensagem CPMCreateQueryOut.

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a>3.1.5.2.3 recebendo uma solicitação CPMGetQueryStatusIn

Quando o servidor recebe uma solicitação de mensagem CPMGetQueryStatusIn de um cliente, o servidor deve fazer o seguinte:

-   Verifique se o cliente tem a consulta associada a ele. Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Verifique se o cursor handle está em uma lista de alças de cursor do cliente. Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).
-   Prepare uma mensagem CPMGetQueryStatusOut. O servidor DEVE recuperar o status atual da consulta e defini-lo no campo \_ QStatus (consulte 2.2.3.11 para obter valores possíveis). Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar um erro.
-   Responda ao cliente com a mensagem CPMGetQueryStatusOut.

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a>3.1.5.2.4 Recebendo uma solicitação CPMGetQueryStatusExIn

Quando o servidor recebe uma solicitação de mensagem CPMGetQueryStatusExIn de um cliente, o servidor DEVE fazer o seguinte:

-   Verifique se o cliente tem uma consulta associada a ele. Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Verifique se o cursor passado está em uma lista de alças de cursor do cliente. Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).
-   Prepare uma mensagem CPMGetQueryStatusExOut. O servidor DEVE recuperar o status atual da consulta e o progresso da consulta e definir QStatus (consulte 2.2.3.11 para obter valores possíveis), \_ dwRatioFinishedDenominator e \_ dwRatioFinishedNumerator, respectivamente. Em seguida, ele DEVE definir o número de linhas nos resultados da consulta \_ como cRowsTotal. Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.
-   Recupere informações sobre o catálogo do cliente e preencha \_ cFilteredDocuments e \_ cDocumentsToFilter. Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.
-   Recupere a posição do indicador indicada pelo handle no campo bmk e preencha o campo iRowBmk restante na mensagem \_ \_ CPMGetQueryStatusExOut. Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.
-   Responda ao cliente com a mensagem CPMGetQueryStatusExOut.

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a>3.1.5.2.5 Recebendo uma solicitação CPMRatioFinishedIn

Quando o servidor recebe uma solicitação de mensagem CPMRatioFinishedIn de um cliente, o servidor DEVE fazer o seguinte:

-   Verifique se o cliente tem uma consulta associada a ele. Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Verifique se o cursor passado está na lista de alças de cursor do cliente. Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).
-   Prepare uma mensagem CPMRatioFinishedOut. O servidor DEVE recuperar o status da consulta do cliente e preencher os campos \_ ulNumerator, \_ ulDenominator e \_ cRows. Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.
-   Se cRows for igual ao último número relatado de linhas para essa consulta, de definido \_ fNewRows como 0x00000000, caso contrário, de definido como \_ 0x00000001.
-   Atualize o último número relatado de linhas para essa consulta para o valor \_ de cRows.
-   Responda ao cliente com a mensagem CPMRatioFinishedOut.

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a>3.1.5.2.6 Recebendo uma solicitação CPMSetBindingsIn

Quando o servidor recebe uma solicitação de mensagem CPMSetBindingsIn de um cliente, o servidor DEVE fazer o seguinte:

-   Verifique se o cliente tem uma consulta associada a ele. Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Verifique se o cursor passado está na lista de alças de cursor do cliente. Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).
-   Verifique se as informações de associação são válidas (ou seja, a coluna pelo menos especifica o valor, o comprimento ou o status a ser retornado; nenhuma sobreposição nas vinculações para valor, tamanho ou status; e valor, tamanho e status se ajustam ao tamanho da linha especificado) e, se não relatar um erro de BD \_ \_ E BADBINDINFO (0x80040E08).
-   Salve as informações de associação associadas às colunas especificadas no campo aColumns. Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.
-   Responda ao cliente com um header de mensagem (somente) com msg definido como \_ CPMSetBindingsIn e status definido como os resultados da \_ associação especificada.

### <a name="31527-receiving-a-cpmgetrowsin-request"></a>3.1.5.2.7 Recebendo uma solicitação CPMGetRowsIn

Quando o servidor recebe uma solicitação de mensagem CPMGetRowsIn de um cliente, o servidor DEVE fazer o seguinte:

-   Verifique se o cliente tem uma consulta associada a ele. Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Verifique se o cursor passado está na lista de alças de cursor do cliente. Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).
-   Verifique se o cliente tem um conjunto atual de vinculações. Se esse não for o caso, o servidor DEVERÁ relatar um erro E \_ FAIL (0x80004005).
-   Prepare uma mensagem CPMGetRowsOut. O servidor DEVE posicionar o cursor nos resultados da consulta, conforme indicado pela descrição da busca. Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.
-   Busque quantas linhas cabem em um buffer, o tamanho do qual é indicado por cbReadBuffer, mas não mais do que indicado \_ por \_ cRowsToTransfer. Ao buscar linhas, o servidor DEVE comparar o tipo de valor da propriedade de cada coluna selecionada com o tipo especificado no conjunto atual de vinculações do cliente (seção 3.1.1). Se o tipo na associação não for VT VARIANT, o servidor DEVERÁ tentar converter o valor da propriedade da coluna \_ nesse tipo. Caso contrário, se o sinalizador DBPROP USEEXTENDEDDBTYPES for definido no conjunto de propriedades \_ DBPROPSET QUERYEXT do cliente ou se o valor da propriedade da coluna não for um tipo VT VECTOR, o valor da propriedade DEVERÁ ser retornado em seu \_ \_ tipo normal. Se nenhum deles for o caso (ou seja, o servidor tiver um tipo VECTOR VT e o cliente não dá suporte a VECTOR VT), o servidor DEVERÁ tentar convertê-lo em um tipo VT ARRAY da seguinte \_ \_ \_ forma: VT \_ I8, VT \_ UI8, VT FILETIME e elementos de matriz \_ \_ CLSID VT não poderão ser convertidos e falharão; Os elementos da matriz VT LPSTR e VT LPWSTR DEVEM ser convertidos em VT BSTR; os elementos de matriz de todos os outros \_ \_ tipos DEVEM permanecer \_ inalterados. Por fim, se as colunas de linha contêm alças de capítulo ou alças de indicador, o servidor DEVE atualizar as listas correspondentes. Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar que um erro foi encontrado.
-   Armazene o número real de linhas buscadas em \_ cRowsReturned.
-   Copie a descrição de busca e o campo de capítulo de CPMGetRowsIn para uma mensagem CPMGetRowsOut a ser enviada.
-   Armazene linhas buscadas no campo Linhas (consulte a observação sobre o byte de status abaixo e a seção 2.2.3.16 na estrutura do campo Linhas).
-   Responda ao cliente com a mensagem CPMGetRowsOut.

Observação no campo de byte de status:

Se StatusUsed estiver definido como 0x01 na CTableColumn da mensagem CPMSetBindingIn para a coluna, o servidor DEVERÁ definir o byte de status (localizado em StatusOffset do início da linha) para essa coluna como um dos seguintes valores:



| Valor | Significado        |
|-------|----------------|
| 0x00  | StatusOK       |
| 0x01  | StatusDeferido |
| 0x02  | StatusNull     |



 

Se o valor da propriedade estiver ausente para essa linha, o servidor DEVERÁ definir o byte de status como StatusNull. Se o valor for muito grande para ser transferido na mensagem CPMGetRowsOut, o servidor DEVERÁ definir o byte de status como StatusDeferred. Caso contrário, o servidor DEVERÁ definir o byte de status como StatusOK.

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a>3.1.5.2.8 Recebendo uma solicitação CPMFetchValueIn

Quando o servidor recebe uma solicitação de mensagem CPMFetchValueIn de um cliente, o servidor DEVE fazer o seguinte:

-   Verifique se o cliente tem uma consulta associada a ele. Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Prepare uma mensagem CPMFetchValueOut. Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar um erro.
-   Localize o documento indicado pelo campo wid e verifique se a ID da propriedade deste documento (posteriormente conhecida como 'valor da propriedade') indicada pela estrutura PropSpec está disponível para \_ esse cliente. Se esse valor não estiver disponível, o servidor DEVERÁ definir fValueExists como 0x00000000 e, de outra \_ forma, \_ definir fValueExists como 0x00000001. Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar um erro.
-   Se \_ fValueExists for igual a 0x00000001 o servidor DEVERÁ fazer o seguinte:
-   -   Serialize o valor da propriedade para uma estrutura SERIALIZEDPROPERTYVALUE e copie, começando no deslocamento \_ cbSoFar, no máximo bytes cbChunk (mas não após o final da propriedade serializada) para o campo \_ vValue. Se essa etapa falhar por qualquer motivo, o servidor DEVERÁ relatar um erro.
    -   De \_ definir cbValue como o número de bytes copiados na etapa anterior.
    -   De definir vType como o tipo de propriedade do valor da propriedade.
    -   Se o comprimento da propriedade serializada for maior que cbSoFar adicionado a cbValue, de definir \_ \_ fMoreExists como 0x00000001, caso contrário, de definido como \_ 0x00000000.

-   Responder ao cliente com a mensagem CPMFetchValueOut

### <a name="31529-receiving-a-cpmgetnotify-request"></a>3.1.5.2.9 Recebendo uma solicitação CPMGetNotify

Quando o servidor recebe uma mensagem CPMGetNotify de um cliente, o servidor DEVE fazer o seguinte:

-   Verifique se o cliente tem uma consulta associada a ele. Se esse não for o caso, o servidor DEVERÁ relatar um erro STATUS \_ INVALID \_ PARAMETER (0xC000000D).
-   Se não houver nenhuma alteração no conjunto de resultados da consulta desde a última mensagem CPMSendNotifyOut para esse cliente ou se a consulta não estiver monitorada no momento para alterações no conjunto de resultados, o servidor DEVERÁ responder com a mensagem CPMGetNotify e começar a monitorar a consulta em busca de alterações no conjunto de resultados. Se, em um momento posterior, houver uma alteração no conjunto de resultados da consulta, o servidor deverá enviar exatamente uma mensagem CPMSendNotifyOut para o cliente e deve especificar a alteração no \_ campo watchNotify.
-   Se houver alterações no conjunto de resultados da consulta desde a última mensagem CPMSendNotifyOut, o servidor deverá responder com CPMSendNotifyOut e deverá especificar a alteração no \_ campo watchNotify. Observe que, no caso de muitas alterações nos resultados da consulta, DBWATCHNOTIFY \_ rowschanged tem prioridade (ou seja, se a consulta foi feita, executada novamente e, em seguida, o número de linhas alteradas e a consulta foi feita novamente, o evento relatado seria DBWATCHNOTIFY \_ rowschanged).

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a>3.1.5.2.10 recebendo uma solicitação CPMGetApproximatePositionIn

Quando o servidor recebe uma solicitação de mensagem CPMGetApproximatePositionIn do cliente, o servidor deve fazer o seguinte:

-   Verifique se o cliente tem uma consulta associada a ele. Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.
-   Verifique se a alça do cursor, o identificador do capítulo e o identificador do indicador aprovado estão nas listas correspondentes. Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).
-   Localize uma linha que esteja associada ao identificador de indicador nos resultados da consulta e aproximar a posição da linha no conjunto de linhas, referenciada pelo identificador de capítulo, e determine o numerador e o denominador para a posição. Observe que, quando o identificador do capítulo é DB \_ NULL \_ HCHAPTER, o capítulo correspondente é o principal conjunto de linhas da consulta. Se essa etapa falhar por algum motivo, o servidor deverá relatar um erro.
-   Responda ao cliente com uma mensagem CPMFetchValueOut.

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a>3.1.5.2.11 recebendo uma solicitação CPMCompareBmkIn

Quando o servidor recebe uma solicitação de mensagem CPMCompareBmkIn do cliente, o servidor deve fazer o seguinte:

-   Verifique se o cliente tem uma consulta associada a ele. Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.
-   Verifique se a alça do cursor, o identificador do capítulo e os identificadores de indicador passados estão nas listas correspondentes. Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).
-   Prepare uma mensagem CPMCompareBmkOut.
-   Se as alças de indicador forem iguais, \_ DWCOMPARISON deverá ser definido como DBCOMPARE \_ EQ.
-   Caso contrário, se um dos indicadores identificadores for DBBMK \_ First ou DBBMK \_ Last, \_ dwComparison deverá ser definido como DBCOMPARE \_ ne.
-   Caso contrário, o servidor deverá fazer o seguinte:
-   -   Localizar linhas que são referenciadas por cada identificador de indicador nos resultados da consulta
    -   Se qualquer uma das linhas não estiver no capítulo indicado pelo identificador de capítulo em CPMCompareBmkIn, \_ DWCOMPARISON deverá ser definido como DBCOMPARE não \_ comparável.
    -   Caso contrário, quando ambas as linhas estiverem no mesmo capítulo, o servidor deverá aproximar uma posição dessas linhas no conjunto de linhas referido pela alça deste capítulo. Em seguida, ele deve comparar valores de posição e definir \_ dwComparison como DBCOMPARE \_ lt se a posição da primeira linha for menor que a posição da segunda linha; caso contrário, \_ dwComparison deverá ser definido como DBCOMPARE \_ gt.

-   Responda ao cliente com a mensagem CPMCompareBmkOut preenchida.

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a>3.1.5.2.12 recebendo uma solicitação CPMRestartPositionIn

Quando o servidor recebe a solicitação de mensagem CPMRestartPositionIn do cliente, o servidor deve fazer o seguinte:

-   Verifique se o cliente tem uma consulta associada a ele. Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.
-   Verifique se o identificador do cursor e o identificador do capítulo aprovado estão nas listas correspondentes. Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).
-   Mova o cursor para o início do capítulo, identificado pelo identificador de capítulo. Observe que, quando o identificador do capítulo é DB \_ NULL \_ HCHAPTER, o capítulo correspondente é o principal conjunto de linhas da consulta. Se essa etapa falhar por algum motivo, o servidor deverá relatar um erro.
-   Responda ao cliente com uma mensagem CPMRestartPositionIn.

### <a name="315213-receiving-a-cpmfreecursorin-request"></a>3.1.5.2.13 recebendo uma solicitação CPMFreeCursorIn

Quando o servidor recebe uma solicitação de mensagem CPMFreeCursorIn do cliente, o servidor deve fazer o seguinte:

-   Verifique se o cliente tem uma consulta associada a ele. Se esse não for o caso, o servidor deverá relatar um \_ \_ erro de parâmetro inválido (0xC000000D) de status.
-   Verifique se o identificador de cursor passado está na lista de identificadores de cursor do cliente. Se esse não for o caso, o servidor deverá relatar um erro de E de \_ falha (0x80004005).
-   Libere o cursor e os recursos associados (consulte a seção 3.1.1 para obter a lista completa) para esse identificador de cursor.
-   Remova o cursor da lista de cursores para esse cliente.
-   Responda com uma mensagem CPMFreeCursorOut, definindo o \_ campo cCursorsRemaining com o número de cursores restantes. na lista deste cliente.
-   Se não houver mais cursores para esse cliente, o servidor deverá liberar a consulta e os recursos associados (consulte a seção 3.1.1).

### <a name="315214-receiving-a-cpmdisconnect-request"></a>3.1.5.2.14 recebendo uma solicitação CPMDisconnect

Quando o servidor recebe uma solicitação de mensagem CPMDisconnect do cliente, o servidor deve remover o cliente da lista de clientes conectados e liberar todos os recursos associados ao cliente.

### <a name="316-timer-events"></a>Eventos de timer 3.1.6

Nenhum.

### <a name="317-other-local-events"></a>3.1.7 outros eventos locais

Quando o servidor é interrompido, ele deve primeiro fazer a transição para o estado "desligando". Em seguida, ele deve parar de escutar o pipe, executar outras tarefas de desligamento específicas da implementação e, em seguida, fazer a transição para o estado "Stopped".

### <a name="32-client-details"></a>3,2 detalhes do cliente

### <a name="321-abstract-data-model"></a>3.2.1 modelo de dados abstratos

A seção a seguir especifica os dados e o estado mantidos pelo cliente do protocolo do serviço de indexação de conteúdo. Os dados fornecidos são para facilitar a explicação de como o protocolo se comporta. Esta seção não exige que as implementações sigam esse modelo, desde que seu comportamento externo seja consistente com o descrito neste documento.

Um cliente tem o seguinte estado abstrato:

-   **Última mensagem enviada**: uma cópia da última mensagem enviada ao servidor.
-   **Valor da propriedade atual**: um valor parcial de uma propriedade "adiada", que está no processo de ser recuperado.
-   **Bytes atuais recebidos**: o número de bytes recebidos para o valor da propriedade atual até o momento.
-   **Estado de conexão do pipe nomeado**: uma conexão com o servidor

### <a name="322-timers"></a>temporizadores de 3.2.2

Nenhum temporizador de protocolo é necessário.

### <a name="323-initialization"></a>inicialização do 3.2.3

Nenhuma ação é executada até que uma solicitação de camada superior seja recebida.

### <a name="324-higher-layer-triggered-events"></a>Eventos disparados Higher-Layer 3.2.4

Quando uma solicitação é recebida de uma camada superior, o cliente deve criar uma conexão de pipe nomeado para o servidor, usando os detalhes especificados na seção 2,1. Se não for possível fazer isso, a solicitação de camada superior deverá ter falhado. Ou seja, no caso de uma falha ao se conectar, é responsabilidade do nível mais alto tentar novamente, se desejado.

Um cabeçalho deve ser semipendente com campos definidos conforme especificado na seção 2.2.2.

Para mensagens que são especificadas como exigindo uma soma de verificação diferente de zero, o \_ valor de ULCHECKSUM deve ser calculado da seguinte maneira:

1.  O conteúdo da mensagem após o \_ campo ulReserved2 no cabeçalho da mensagem deve ser interpretado como uma sequência de inteiros de 32 bits. O cliente deve calcular a soma dos valores numéricos fornecidos por esses inteiros.
2.  Calcule o XOR bit a bit desse valor com 0x59533959.
3.  Subtraia o valor fornecido pela \_ mensagem do valor que resulta do XOR bit a bit.

### <a name="3241-remote-indexing-service-catalog-management"></a>Gerenciamento de catálogo do serviço de indexação remota do 3.2.4.1

Cada mensagem é disparada por uma solicitação da camada superior. Não há nenhuma sequência de mensagens imposta pelo cliente para solicitações de mensagens CISP para gerenciar catálogos remotamente, mas (com exceção de uma mensagem CPMSetCatStateIn) o servidor responderá com êxito somente se o cliente tiver se conectado anteriormente por meio de uma mensagem CPMConnectIn.

### <a name="32411-sending-a-cpmcistateinout-request"></a>3.2.4.1.1 enviando uma solicitação CPMCiStateInOut

Normalmente, a camada superior solicita que o cliente de protocolo envie uma mensagem CPMCiStateInOut quando requer informações sobre a indexação de serviços no servidor.

Quando solicitado a enviar esta mensagem, o cliente deve fazer o seguinte:

-   Envie uma mensagem CPMCiStateInOut conforme especificado na seção 2.2.3.1 para o servidor.
-   Aguarde para receber a mensagem CPMCiStateInOut do servidor, descartando silenciosamente todas as outras mensagens.
-   Relate o valor do \_ campo status da resposta e, se tiver êxito, a estrutura informativa de volta à camada mais alta.

### <a name="32412-sending-a-cpmsetcatstatein-request"></a>3.2.4.1.2 enviando uma solicitação CPMSetCatStateIn

Normalmente, a camada superior solicita que o cliente de protocolo envie uma mensagem CPMSetCatStateIn quando requer informações sobre um catálogo ou todos os catálogos. Para essa mensagem, a camada superior precisa fornecer ao cliente de protocolo um valor para \_ dwNewState e, se necessário, o nome do catálogo.

Quando solicitado a enviar esta mensagem, o cliente deve fazer o seguinte:

-   Envie uma mensagem CPMSetCatStateIn conforme especificado em 2.2.3.2 para o servidor.
-   Aguarde para receber uma mensagem CPMSetCatStateOut do servidor, descartando silenciosamente todas as outras mensagens.
-   Relate o valor do \_ campo status da resposta e, se tiver sido bem-sucedida, o \_ dwOldState de volta para a camada superior.

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a>3.2.4.1.3 enviando uma solicitação CPMUpdateDocumentsIn

A camada mais alta normalmente solicita o envio dessa mensagem quando precisa atualizar documentos no caminho existente ou adicionar um novo caminho de arquivo ao índice. Portanto, a camada mais alta é fornecer o caminho e o tipo de uma verificação, que é especificado como na seção 2.2.3.4, em que uma atualização incremental ou completa é destinada a caminhos existentes, e a nova inicialização é destinada a novos caminhos.

Para atender à solicitação de camada superior, o cliente deve fazer o seguinte:

-   Envie uma mensagem CPMUpdateDocumentsIn conforme especificado na seção 2.2.3.4 para o servidor.
-   Aguarde para receber a mensagem CPMUpdateDocumentsIn de volta do servidor, descartando silenciosamente todas as outras mensagens.
-   Relate o valor do \_ campo status da resposta de volta para a camada superior.

### <a name="32414-sending-a-cpmforcemergein-request"></a>3.2.4.1.4 enviando uma solicitação CPMForceMergeIn

Normalmente, as solicitações de camada mais alta para enviar essa mensagem quando há necessidade de melhorar o desempenho da consulta ou fazem parte da manutenção agendada do serviço de indexação.

Para atender à camada mais alta, o cliente deve fazer o seguinte:

-   Envie a mensagem CPMForceMergeIn conforme especificado pela seção 2.2.3.5 para o servidor.
-   Aguarde para receber uma mensagem CPMUpdateDocumentsIn de volta do servidor, descartando silenciosamente todas as outras mensagens.
-   Relate o valor do \_ campo status da resposta de volta para a camada superior.

### <a name="3242-remote-indexing-service-catalog-query-messages"></a>Mensagens de consulta do catálogo de serviço de indexação remota do 3.2.4.2

Com exceção de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, há uma relação um-para-um entre as mensagens CISP e as solicitações de camada superior. Para as duas exceções mencionadas acima, pode haver várias mensagens geradas pelo cliente para atender aos requisitos de tamanho ou para recuperar uma propriedade completa. Normalmente, a camada superior controla todas as informações específicas de consulta (como identificadores de cursor abertos, valores válidos para identificadores de indicador e capítulo, valores de wid para valores de propriedade adiados, etc.) e também controla se o cliente está em um estado conectado, mas isso não é imposto de nenhuma forma pelo cliente.

Para fins ilustrativos, a parte de cliente do diagrama na seção 3 ilustra essa sequência para uma consulta de serviço de indexação simples.

### <a name="32421-sending-a-cpmconnectin-request"></a>3.2.4.2.1 enviando uma solicitação CPMConnectIn

Essa mensagem é normalmente a primeira solicitação da camada superior (como se o cliente não estiver conectado, o servidor falhará na maioria das mensagens com exceção de CPMSetCatStateIn). O nível mais alto fornece ao cliente de protocolo as informações necessárias para se conectar.

Para atender à camada mais alta, o cliente deve fazer o seguinte:

-   Preencha a mensagem, usando informações que o cliente de camada superior forneceu (consulte a seção 2.2.3.6) em \_ iClientVersion, MachineName, username, PropertySet1, PropertySet2 e aPropertySet.
-   Defina \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet e cExtPropSet conforme especificado em 2.2.3.6.
-   Defina a soma de verificação no \_ campo ulChecksum.
-   Envie a mensagem CPMConnectIn para o servidor.
-   Aguarde para receber uma mensagem CPMConnectOut de volta do servidor, descartando silenciosamente todas as outras mensagens.
-   Relate o valor do \_ campo status da resposta e, se tiver sido bem-sucedida, o \_ serverVersion de volta para a camada superior.

Para fins informativos, espera-se que as camadas mais altas normalmente realizem as seguintes ações após a conexão bem-sucedida, mas elas não são impostas pelo cliente CISP:

-   Usar mensagens de gerenciamento de catálogo de serviço de indexação remota para tarefas administrativas
-   Use uma solicitação CPMCreateQueryIn para criar uma consulta de pesquisa com a finalidade de recuperar os resultados do catálogo.

### <a name="32422-sending-a-cpmcreatequeryin-request"></a>3.2.4.2.2 enviando uma solicitação CPMCreateQueryIn

A camada superior normalmente fornecerá informações para a criação da consulta quando o cliente do protocolo estiver conectado. A camada superior fornece ao cliente um conjunto de restrições, conjunto de colunas, regras de ordem de classificação e conjunto de categorização (cada um deles pode ser omitido), propriedades de conjunto de linhas e estrutura do mapeador de ID de propriedade.

Quando essa solicitação é recebida de uma camada superior, o cliente deve fazer o seguinte:

-   Prepare um CPMCreateQueryOut da seguinte maneira.
-   -   Se um conjunto de colunas estiver presente, defina CColumnsSetPreset como 0x01 e preencha o campo Columnsset.
    -   Se houver restrições, defina CRestrictionPresent como 0x01 e preencha o campo de restrição.
    -   Se um conjunto de classificação estiver presente, preencha o campo de classificação.
    -   Se um conjunto de categorização estiver presente, defina CSortSetPresent como 0x01 e preencha o campo CategorizationSet.
    -   Definir o restante dos campos conforme especificado em 2.2.3.8

-   Calcule \_ o campo ulCheckSum no cabeçalho.
-   Envie a mensagem CPMCreateQueryIn para o servidor.
-   Aguarde para receber a mensagem CPMCreateQueryOut (consulte os detalhes na seção 3.2.5.1.1), descartando silenciosamente todas as outras mensagens.
-   Relate o valor do \_ campo status da resposta e, se tiver êxito, a matriz de identificadores de cursor e valores Boolianos informativos (conforme especificado em 2.2.3.9) de volta para a camada superior.

### <a name="32423-sending-a-cpmsetbindingsin-request"></a>3.2.4.2.3 enviando uma solicitação CPMSetBindingsIn

Normalmente, a camada superior definirá associações para cada coluna a ser retornada nas linhas quando ela já tiver um identificador de cursor válido (depois de receber CPMCreateQueryOut com êxito, consulte a seção 3.2.5.1.1). O valor mais alto é esperado para fornecer uma matriz de estruturas CTableColumn, conforme especificado na seção 2.2.4.31, para o campo aColumns e um identificador de cursor válido.

Quando essa solicitação é recebida da camada superior, o cliente deve fazer o seguinte:

-   Calcule o número de estruturas CTableColumn na matriz aColumns e defina o campo cColumns com esse valor.
-   Calcule o tamanho total em bytes dos campos cColumns e aColumns e defina o \_ campo cbBindingDesc com esse valor.
-   Defina os campos especificados na mensagem CPMSetBindingsIn para os valores fornecidos pela camada de aplicativo superior. Defina o \_ campo ulChecksum para o valor calculado conforme especificado na seção 3.2.5.
-   Envie a mensagem CPMSetBindignsIn concluída para o servidor.
-   Aguarde para receber uma mensagem CPMSetBindingsIn do servidor, descartando outras mensagens.
-   Indique o status do \_ campo status da resposta para a camada superior.

Para fins informativos, espera-se que as camadas mais altas normalmente solicitem que um cliente envie uma mensagem CPMGetRowsIn, mas isso não é imposto pelo protocolo de serviço de indexação de conteúdo.

### <a name="32424-sending-a-cpmgetrowsin-request"></a>3.2.4.2.4 enviando uma solicitação CPMGetRowsIn

Quando a camada mais alta estiver prestes a receber informações de linhas, ele fornecerá ao cliente de protocolo com o cursor e o identificador do capítulo válidos e fornecerá a descrição de busca apropriada. Normalmente, espera-se que uma camada mais alta faça isso quando tem um cursor e/ou identificador de capítulo válido, e as associações foram definidas com a mensagem CPMSetBindingsIn. Para acessar o conjunto de linhas em um capítulo, a camada mais alta é usar o identificador de capítulo recebido do servidor em uma mensagem CPMGetRowsOut anterior.

Quando essa solicitação é recebida da camada superior, o cliente deve fazer o seguinte:

-   Determine qual valor inteiro sem sinal deve ser especificado para o \_ campo cbReadBuffer. Para determinar esse valor, o cliente deve obter o valor máximo do seguinte:
-   -   1000 vezes o valor do campo c \_ RowsToTransfer.
    -   Valor de \_ cbRowWidth, arredondado para o múltiplo de 512 bytes mais próximo.
    -   Pegue os dois valores acima, até o limite de 16K.
    -   Nos casos em que uma única linha é maior que 16K, o servidor não pode retornar resultados para essa consulta.

Especifique uma base de cliente para dados de linha de tamanho variável no espaço de endereço de cliente no \_ campo ulClientBase.

*Comportamento do Windows: para um cliente de 32 bits conversando com um servidor de 32 bits ou um cliente de 64 bits conversando com um servidor de 64 bits, esse valor é definido como um endereço de memória do buffer de recebimento no processo do aplicativo. Isso permite que os ponteiros, recebidos no campo de linhas de CPMGetRowsOut, sejam ponteiros de memória corretos em um processo de aplicativo cliente. Caso contrário, ele será definido como 0x00000000.*

-   Calcule o tamanho da descrição de busca e defina-a no \_ campo cbSeek.
-   Defina o valor de cbReserved (que atuaria como um deslocamento para o início das linhas) para o valor de \_ cbSeek Plus 0x14.
-   Envie uma mensagem CPMConnectIn conforme especificado em 2.2.3.15 para o servidor.

### <a name="32425-sending-a-cpmfetchvaluein-request"></a>3.2.4.2.5 enviando uma solicitação CPMFetchValueIn

Se o cliente receber uma resposta CPMGetRowsOut do servidor com o campo status da coluna definido como StatusDeferred (0x01), isso significa que o valor da propriedade não foi incluído no campo linhas da mensagem CPMGetRowsOut. Nesse caso, a camada mais alta normalmente solicita que o cliente de protocolo recupere o valor por meio da mensagem CPMFetchValueIn e fornece o valor de PropSpec e \_ wid para uma propriedade adiada, que o cliente de protocolo deve usar na primeira mensagem CPMFetchValueIn.

Se esta for a primeira mensagem CPMFetchValueIn que o cliente enviou para solicitar a propriedade especificada, o cliente deverá fazer o seguinte:

-   Defina todos os campos em uma mensagem conforme especificado na seção 2.2.3.19.
-   Defina \_ cbSoFar como 0x00000000.
-   Defina os bytes atuais recebidos como 0.
-   Envie a mensagem CPMFetchValueIn para o servidor.

### <a name="32426-sending-a-cpmfreecursorin-request"></a>3.2.4.2.6 enviando uma solicitação CPMFreeCursorIn

Quando o nível mais alto não estiver mais usando a consulta de pesquisa, ele poderá liberar os recursos no servidor solicitando que o cliente envie uma mensagem CPMFreeCursorIn.

Quando essa solicitação é recebida, o cliente deve enviar uma mensagem CPMFreeCursorIn conforme especificado em 2.2.3.28 para o servidor, contendo o identificador especificado pela camada superior.

### <a name="32427-sending-a-cpmdisconnect-message"></a>3.2.4.2.7 enviando uma mensagem CPMDisconnect

Se a camada superior não tiver mais consultas para o serviço de indexação, para liberar mais recursos do servidor, o aplicativo poderá solicitar que o cliente envie uma mensagem CPMDisconnect ao servidor. Quando essa consulta é recebida, o cliente deve simplesmente enviar a mensagem conforme solicitado. Não há resposta a essa mensagem do servidor.

### <a name="325-message-processing-and-sequencing-rules"></a>Processamento de mensagens 3.2.5 e regras de sequenciamento

Quando o cliente recebe uma resposta de mensagem do servidor, o cliente deve usar a última mensagem enviada para determinar se a mensagem recebida do servidor é a esperada pelo cliente. Todas as mensagens com \_ o campo msg diferente da que está na última mensagem de envio devem ser ignoradas.

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a>3.2.5.1 recebendo uma resposta CPMCreateQueryOut

Quando o cliente recebe uma resposta de mensagem CPMCreateQueryOut do servidor, o cliente deve retornar o \_ status e (se o status for com êxito) os valores de ponteiro de volta para uma camada superior. Todas as ações adicionais são até a camada mais alta.

Como a camada mais alta reconhece a estrutura de consulta, ela sempre esperará o número correto de identificadores de cursor a serem retornados na mensagem CPMCreateOueryOut. As alças de cursor são retornadas na seguinte ordem: o primeiro identificador é para o conjunto de linhas sem capítulos, o segundo é para o primeiro conjunto de linhas com capítulo (que é o agrupamento de resultados com base na primeira categoria especificada no campo CategorizationSet da mensagem CPMCreateQueryIn).

Para fins informativos, espera-se que camadas mais altas possam realizar as seguintes ações, mas elas não são impostas pelo cliente CISP:

-   Use CPMSetBindingsIn para definir associações para colunas individuais e executar ações subsequentes no caminho de consulta
-   Use CPMGetQueryStatusIn para verificar o progresso da execução de uma consulta.
-   Use CPMRatioFinishedIn para solicitar o percentual de conclusão da consulta.

### <a name="3252-receiving-a-cpmgetrowsout-response"></a>3.2.5.2 recebendo uma resposta CPMGetRowsOut

Quando o cliente recebe uma resposta de mensagem CPMGetRowsOut do servidor, o cliente deve fazer o seguinte:

-   Verifique se o \_ campo status no cabeçalho indica êxito ou falha.
-   Se o \_ valor de status for \_ buffer de status \_ muito \_ pequeno (0xC0000023), o cliente deverá verificar o estado da última mensagem enviada. Se ele não contém uma mensagem CPMGetRowsIn, a mensagem recebida DEVE ser ignorada silenciosamente. Caso contrário, o cliente DEVERÁ enviar ao servidor uma nova mensagem CPMGetRowsIn com todos os campos idênticos ao armazenado, exceto que cbReadBuffer DEVE ser aumentado em 512 (mas não maior que \_ 0x4000). Se o status for BUFFER DE STATUS MUITO PEQUENO (0xC0000023) e a Última Mensagem Enviada já tiver \_ \_ \_ \_ \_ cbReadBuffer igual 0x4000 cliente DEVERÁ relatar o erro até o nível superior.
-   Se o valor de status for qualquer outro valor de erro, o cliente DEVERÁ indicar a \_ falha até a camada superior.
-   Se o valor de status indicar êxito, os resultados DEVERÃO ser indicados até a camada superior solicitando as informações e outras ações serão até \_ a camada superior.

Para fins informativos, espera-se que camadas mais altas normalmente faça as seguintes ações, mas elas não são impostas pelo cliente do Protocolo de Serviço de Indexação de Conteúdo:

-   Se os valores em linhas representarem as IDs do documento, o capítulo ou o indicador manipulará a camada superior normalmente os armazenará para uso em operações subsequentes que envolvem IDs de documento válidas, alças de capítulo ou indicador.
-   A camada superior normalmente armazenará ou exibirá ou usará os dados de valores de linha.
-   Para os valores que foram marcados como camada superior adiada, buscará o valor usando mensagens CPMFetchValueIn.
-   A descrição da busca também é retornada para a camada superior e pode ser reutilizada ou examinada pela camada superior.

Para fins informativos, se a camada superior solicitada lidar com capítulos e indicadores que foram recebidos nas linhas, ele poderá fazer o seguinte:

-   Use CPMGetQueryStatusExIn para verificar o progresso da execução de uma consulta, bem como informações de status adicionais, como o número de documentos filtrados, os documentos restantes a serem filtrados, a taxa de documentos processados pela consulta, o número total de linhas na consulta e a posição do indicador no conjuntos de linhas.
-   Use CPMGetNotify para solicitar que o servidor notifique o cliente sobre alterações no conjuntos de linhas.
-   Use CPMGetApproximatePositionIn para solicitar a posição aproximada de um indicador em um capítulo.
-   Use CPMCompareBmkIn para solicitar uma comparação de dois indicadores em um capítulo.
-   Use CPMRestartPositionIn para o servidor para alterar o local do cursor para o início do rowset.

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a>3.2.5.3 Recebendo uma resposta CPMFetchValueOut

Quando o cliente recebe uma resposta de mensagem CPMGetRowsOut do servidor, o cliente DEVE fazer o seguinte:

-   Verifique se o \_ campo de status no header indica êxito ou falha. Em caso de falha, notifique a camada superior. Caso contrário, continue abaixo.
-   Verifique \_ fValueExist e, se definido como 0x00000000 notifique a camada superior de que o valor não foi encontrado.
-   Caso contrário, \_ aenda os bytes cbValue de vValue ao Valor da Propriedade Atual.
-   Se fMoreExists estiver definido como 0x00000001 incrementar Bytes Atuais Recebidos por cbValue e enviar uma mensagem \_ \_ \_ CPMFetchValueIn para o servidor, definindo cbSoFar como o valor de Bytes Atuais Recebidos, cbPropSpec como zero e \_ \_ \_ \_ cbChunk para o tamanho do buffer desejado pela camada superior.
-   Se fMoreExists for definido como 0x00000000, indique o valor da propriedade \_ de Valor da Propriedade Atual para a camada superior.

### <a name="3254-receiving-a-cpmfreecursorout-response"></a>3.2.5.4 Recebendo uma resposta CPMFreeCursorOut

Quando o cliente recebe uma resposta de mensagem CPMFreeCursorOut bem-sucedida do servidor, o cliente DEVE retornar o valor \_ cCursorsRemaining para a camada superior.

As informações a seguir são fornecidas apenas para fins informativos e não são impostas pelo cliente CISP. Espera-se que a camada superior controle os alças de cursor e não use aqueles que já foram liberados. Depois que o número de cCursorsRemaining for igual a 0x00000000, a camada superior poderá usar a conexão para especificar outra consulta (usando uma mensagem \_ CPMCreateQueryIn).

### <a name="326-timer-events"></a>3.2.6 Eventos de temporizador

Nenhum.

### <a name="327-other-local-events"></a>3.2.7 Outros eventos locais

Nenhum.

## <a name="4-protocol-examples"></a>4 Exemplos de protocolo

-   [4.1 Exemplo 1](#41-example-1)
-   [4.2 Exemplo 2](#42-example-2)

### <a name="41-example-1"></a>4.1 Exemplo 1

No exemplo a seguir, consideramos um cenário no qual o usuário JOHN no computador A deseja obter os tamanhos de arquivos que contêm a palavra "Microsoft" do conjunto de documentos armazenados no servidor X no catálogo SYSTEM. Vamos supor que o computador A está executando um sistema operacional Windows XP de 32 bits e o computador X está executando um sistema operacional Windows Server 2003 de 32 bits.

1.  O usuário inicia um aplicativo de pesquisa e entra na consulta de pesquisa. O aplicativo, por sua vez, passa a consulta de pesquisa para o cliente de protocolo.
2.  O cliente de protocolo estabelece uma conexão com o servidor de indexação X. O cliente de protocolo usa o \\ SKADS de CI de pipe \\ nomeado para se conectar ao servidor X por \_ SMB.
3.  Em seguida, o cliente de protocolo prepara uma mensagem CPMConnectIn com os seguintes valores:

    O header da mensagem é populado da seguinte forma:

    -   **\_ msg** é definido como 0x000000C8, indicando que esta é uma mensagem CPMConnectIn.
    -   **\_ status** é definido como 0x00000000.
    -   **\_ ulChecksum** contém a verificação, calculada conforme especificado na Seção 3.2.4.
    -   **\_ ulReserved2** é definido como 0x00000000.

    O corpo da mensagem é populado da seguinte forma:

    -   **\_ iClientVersion é** definido como 0x00000008, indicando que o servidor deve validar o campo de verificação.
    -   **\_ fClientIsRemote** é definido como 0x00000001, indicando que o servidor é um servidor remoto.
    -   **\_ cbBlob1** é definido como o tamanho, em bytes, dos campos cPropSet, PropertySet1 e PropertySet2 combinados.
    -   **\_ cbBlob2 é** definido como 0x00000004 (o que significa que nenhum conjunto de propriedades extra).
    -   **MachineName** está definido como A.
    -   **UserName** é definido como JOHN.
    -   **cPropSets** é definido como 0x00000002.
    -   **O campo PropertySet1** é do tipo CDbPropSet. A estrutura CDbPropSet que inclui o campo PropertySet1 é populada da seguinte forma:
        -   O **campo GuidPropSet** é definido como A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT).
        -   **O campo cProperties** é definido como 0x00000004.
        -   **o campo aProps** é uma matriz de estruturas CDbProp.

            Para o **elemento aProps \[ 0: \]**

            -   **PropId** é definido como 0x00000002 (NOME DO CATÁLOGO \_ DE CI \_ \_ DBPROP).
            -   **DBPROPOPTIONS é** definido como 0x0000000.
            -   **DBPROPSTATUS é** definido como 0x00000000.
            -   Para o **elemento ColId:**
                -   **eKind** é definido como 0x00000001 (DBKIND \_ GUID \_ PROPID)
                -   **GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.
                -   **ulID** é definido como 0x00000000.
            -   Para o **elemento vValue:**
                -   **vType** é definido como 0x001F (VT \_ LPWSTR).
                -   **vValue** é definido como "SYSTEM", o nome do catálogo desejado.

            Para o **elemento aProps \[ 1: \]**

            -   **PropId** é definido como 0x00000007 (TIPO DE CONSULTA \_ CI \_ \_ DBPROP)
            -   **DBPROPOPTIONS é** definido como 0x0000000.
            -   **DBPROPSTATUS é** definido como0x00000000.
            -   Para o **elemento ColId:**
                -   **eKind** é definido como 0x00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.
                -   **ulID** é definido como 0x00000000.
            -   Para o **elemento vValue:**
                -   **vType** é definido como 0x0003 (VT \_ I4).
                -   **vValue** é definido como 0x00000000 (CiNormal), o que significa que é uma consulta regular.

            Para o **elemento aProps \[ 2: \]**

            -   **PropId** é definido como 0x00000004 (SINALIZADORES DE ESCOPO \_ DE CI \_ \_ DBPROP).
            -   **DBPROPOPTIONS é** definido como 0x0000000.
            -   **DBPROPSTATUS é** definido como 0x00000000.
            -   Para o **elemento ColId:**
                -   **eKind** é definido como 0x00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.
                -   **ulID** é definido como 0x00000000.
            -   Para o **elemento vValue:**
                -   **vType:** 0x1003 (VT \_ VECTOR \| VT \_ I4)
                -   **vValue:** 0x00000001/0x00000001 (um elemento com valor 1), o que significa sub pastas de pesquisa

            Para o **elemento aProps \[ 3: \]**

            -   **PropId:** 0x00000003 (ESCOPOS DE \_ INCLUSÃO DE CI DO \_ \_ DBPROP)
            -   **DBPROPOPTIONS:** 0x0000000
            -   **DBPROPSTATUS**: 0x00000000
            -   Para o **elemento ColId:**
                -   **eKind** é definido como 0x00000001 (DBKIND \_ GUID \_ PROPID).
                -   **GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.
                -   **ulID** é definido como 0x00000000
            -   Para o **elemento vValue:**
                -   **vType** é definido como 0x101F (VT \_ VECTOR \| VT \_ LPWSTR).
                -   **vValue** é definido como 0x00000001 /0x00000002 /" (um elemento com uma cadeia de caracteres terminada em nulo de 2 caracteres), o que significa o \\ escopo raiz.

    -   O **campo PropertySet2** é do tipo CDbPropSet.

        A estrutura CDbPropSet que inclui o campo PropertySet1 é populada da seguinte forma:

        -   **GuidPropSet** é definido como AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT).
        -   **O campo cProperties** é definido como 0x00000001.
        -   O **campo aProps** é uma matriz de estruturas CDbProp.

            Para o **elemento aProps \[ 0: \]**

            -   **PropId** é definido como 0x00000002 (DBPROP \_ MACHINE).
            -   **DBPROPOPTIONS é** definido como 0x0000000.
            -   **DBPROPSTATUS é** definido como 0x00000000.
            -   Para o **elemento ColId:**
                -   **eKind** é definido como 0x00000001 (DBKIND \_ GUID \_ PROPID),
                -   **GUID** é nulo (todos os zeros), o que significa que o valor se aplica à consulta, não apenas a uma única coluna.
                -   **ulID** é definido como 0x00000000.
            -   Para **o elemento vValue:**
                -   **vType:** 0x0008 (VT \_ BSTR)
                -   **vValue:** 0x04 /"X" (4 bytes/cadeia de caracteres Unicode terminada em nulo), que significa "X" -name de um servidor.

    -   **O campo cExtPropSet** é definido como 0x00000000.
    -   **A matriz aPropertySets** não existe.
    -   Vários campos de preenchimento são preenchidos conforme necessário. A mensagem é enviada ao servidor.

4.  O servidor verifica se o **\_ ulChecksum** está correto, verifica se o usuário está autorizado a fazer essa solicitação e responde com uma mensagem CPMConnectOut.

    O header da mensagem é populado da seguinte forma:

    -   **\_ msg** é definido como 0x000000C8, indicando que esta é uma mensagem CPMConnectOut.
    -   **\_ status** é definido como 0x0000000 indicando SUCCESS.
    -   **\_ ulChecksum** é definido como 0.
    -   **\_ ulReserved2** é definido como 0x00000000.

    O corpo da mensagem é populado da seguinte forma:

    -   **\_ O campo serverVersion** é definido como 0x00000007 (Windows XP de 32 bits ou Windows Server 2003 de 32 bits).
    -   **\_ Os campos** reservados são preenchidos com dados arbitrários.

5.  O cliente prepara uma mensagem CPMCreateQueryIn.

    O header da mensagem é populado da seguinte forma:

    -   **\_ msg** é definido como 0x000000CA, indicando que esta é uma mensagem CPMCreateQueryIn.
    -   **\_ status** é definido como 0x00000000.
    -   **\_ ulChecksum contém** a verificação, calculada de acordo com 3.2.5.
    -   **\_ ulReserved2** é definido como 0x00000000.

    O corpo da mensagem é populado da seguinte forma:

    -   **O** campo tamanho é definido como o tamanho do restante da mensagem.
    -   **O campo CColumnSetPresent** está definido como 0x01.
    -   **O campo ColumnSet** é do tipo CColumnSet. A estrutura CColumnSet que inclui esse campo é definida da seguinte forma:
        -   **\_ o** campo count é definido como 0x00000001 indicando que uma coluna é retornada.
        -   **A matriz** de índices 0x00000000 indicando a primeira entrada em \_ aPropSpec.
    -   **O campo CRestrictionPresent** é definido como 0x01 indicando que o **campo Restrição** está presente.
    -   **O** campo de restrição é do tipo CRestriction e está definido como:
        -   **\_ ulType** é definido como 0x00000004 (RTContent).
        -   **\_ weight** é definido como 0x00000000.
    -   O restante do campo contém uma estrutura CContentRestriction:
        -   **\_** A propriedade é definida como GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (para PRSPEC PROPID) /0x13 que representa o corpo \_ do documento.
        -   **\_ Cc** é definido como 0x00000009.
        -   **\_ pwcsphrase é** definido como a cadeia de caracteres "Microsoft".
        -   **\_ lcid é** definido como 0x409 (para inglês).
        -   **\_ ulGenerateMethod** é definido como 0x00000000 (combinação exata).
    -   **CSortPresent** é definido como 0x00.
    -   **CCategorizationSetPresent** é definido como 0x00.
    -   **RowSetProperties** é definido da seguinte forma:
        -   **\_ uBooleanOptions** é definido como 0x00000001 (sequencial).
        -   **\_ ulMaxOpenRows** é definido como 0x00000000.
        -   **\_ ulMemoryUsage** é definido como 0x00000000.
        -   \_**cMaxResults** é definido como 0x00000100 (retornam no máximo 256 linhas).
        -   **\_ cCmdTimeOut** é definido como 0x00000000 (nunca o tempoout).
    -   **O PidMapper** está definido como:
        -   **\_ count** é definido como 0x00000001.
        -   **\_ aPropSpec** é definido como GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0x00000001 (para PRSPEC PROPID) /0x0000000c que representa a propriedade \_ de tamanho de arquivo do Windows.

6.  O servidor o processa e responde com uma mensagem CPMCreateQueryOut.

    O header da mensagem é populado da seguinte forma:

    -   **\_ msg** é definido como 0x000000CA, indicando que esta é uma mensagem CPMCreateQueryOut.
    -   **\_ status** é definido como SUCCESS.
    -   **\_ ulChecksum** é definido como 0x00000000 (ou qualquer outro valor arbitrário).
    -   **\_ ulReserved2** é definido como 0x00000000 (ou qualquer outro valor arbitrário).

    O corpo da mensagem é populado da seguinte forma:

    -   **\_ fTrueSeqeuntial** é definido como 0x00000000, indicando que a consulta pode usar um índice.
    -   **\_ fWorkIdUnique** está definido como 0x00000001.
    -   A **matriz aCursors** contém apenas um elemento, representando um alça de cursor para essa consulta. O valor depende do estado do servidor. Vamos supor que o valor retornado seja 0xAAAAAAAA.

7.  O cliente emite uma mensagem de solicitação CPMSetBindingsIn para definir o formato de uma linha.

    O header da mensagem é populado da seguinte forma:

    -   **\_ msg** é definido como 0x000000D0, indicando que esta é uma mensagem CPMSetBindingsIn.
    -   **\_ status** é definido como SUCCESS.
    -   **\_ ulChecksum** é definido como 0x00000000 (ou qualquer outro valor arbitrário).
    -   **\_ ulReserved2** é definido como 0x00000000 (ou qualquer outro valor arbitrário).

    O corpo da mensagem é populado da seguinte forma:

    -   **\_ hCursor** é definido como 0xAAAAAAAA.
    -   **\_ cbRow** é definido como 0x10 (grande o suficiente para ajustar colunas).
    -   **\_ cbBindingDesc** é definido como o tamanho dos campos **\_ cColumns** e **\_ aColumns combinados.**
    -   **\_ cColumns é** definido como 0x00000001.
    -   **\_ a Matriz aColumns** é definida para conter uma estrutura CTableColumn que contém:
    -   -   **\_ PropSpec** é definido como GUID b725f130-47ef-101a-a5-f1-02608c9eebac/0x00000001 (para PRSPEC PROPID) /0x0000000c que representa a propriedade de tamanho de \_ arquivo do Windows.
        -   **\_ vType** é definido como 0x0015 (VT \_ UI8).
        -   **\_ ValueUsed é** definido como 0x01 (coluna transferida em linha).
        -   **\_ ValueOffset** é definido como 0x0002 (no início da linha).
        -   **\_ ValueSize** é definido como 0x08 (tamanho de uma \_ VT UI8).
        -   **\_ StatusUsed** é definido como 0x01.
        -   **\_ StatusOffset** é definido como 0x0A.
        -   **\_ LengthUsed** é definido como 0x00.

8.  O servidor o processa e responde com uma mensagem CPMSetBindingsIn.

    O header da mensagem é populado da seguinte forma:

    -   **\_ msg** é definido como 0x000000D0.
    -   **\_ status** é definido como SUCCESS.
    -   **\_ ulChecksum** é definido como 0x00000000 (ou qualquer outro valor arbitrário).
    -   **\_ ulReserved2** é definido como 0x00000000 (ou qualquer outro valor arbitrário).

9.  O cliente emite uma mensagem de solicitação CPMGetRowsIn. Vamos supor que o cliente está preparado para aceitar 100 linhas neste ponto e deseja-as em ordem crescente.

    O header da mensagem é populado da seguinte forma:

    -   **\_ msg** é definido como 0x000000CC, indicando que esta é uma mensagem CPMGetRowsIn.
    -   **\_ status** é definido como 0x00000000
    -   **\_ ulChecksum contém** a verificação, calculada de acordo com a Seção 0.
    -   **\_ ulReserved2** é definido como 0x00000000.

    O corpo da mensagem é populado da seguinte forma:

    -   **\_ hCursor** é definido como 0xAAAAAAAA.
    -   **\_ cRowsToTransfer** é definido como 0x00000064.
    -   **\_ cRowWidth** é definido como 0x00000010 (de vinculações).
    -   **\_ cbSeek** é definido como 0x14 que é o tamanho dos campos eType, chapt e \_ CRowSeekNext combinados.
    -   **\_ cbReserved** é definido como 0x18 (0x14 mais \_ cbSeek).
    -   **\_ cbReadBuffer** é definido como 0x800 (0x64 0x10 arredondado para o próximo \* múltiplo de 0x200).
    -   **\_ ulClientBase** é definido como 0x00000000.
    -   **\_ fBwdfetch** é definido como 0x00000000 indicando que as linhas devem ser buscadas em ordem de avanço.
    -   **EType** é definido como 0x0000001 indicando que o cliente deseja as próximas linhas.
    -   **\_ chapt** é definido como 0 (não um resultado capítulo).
    -   **SeekDescription é** definido como CRowSeekNext. A estrutura CRowSeekNext contém os seguintes valores:
        -   **CiTblChapt** é definido como 0x00000000.
        -   **\_ hRegion** é definido como 0x00000000.
        -   **\_ cSkip** é definido como 0, indicando que o cliente não deseja ignorar linhas.

10. O servidor o processa e responde com uma mensagem CPMGetRowsOut. Vamos supor que o servidor encontrou 100 documentos que contêm a palavra "Microsoft".

    O header da mensagem é populado da seguinte forma:

    -   **\_ msg** é definido como 0x000000CC, indicando que esta é uma mensagem CPMGetRowsOut.
    -   **\_ status** é definido como SUCCESS.
    -   **\_ ulChecksum** é definido como 0x00000000.
    -   **\_ ulReserved2** é definido como 0x00000000.

    O corpo da mensagem é populado da seguinte forma:

    -   **\_ CRowsReturned** é definido como 0x00000064.
    -   **eType** é definido como 0x00000001.
    -   **\_ chapt** é definido como 0x00000000 (não um resultado capítulo).
    -   **SeekDescription** contém uma estrutura CRowSeekNext, populada da seguinte forma:
        -   **CiTblChapt** é definido como 0x00000000.
        -   **\_ hRegion** é definido como 0x00000000.
        -   **\_ cSkip** é definido como 0, indicando que o cliente não deseja ignorar linhas.
    -   **As linhas** contêm o tamanho dos 100 documentos que contêm a palavra "Microsoft". Como esses dados são de tamanho fixo, eles são simplesmente estruturados como uma lista de inteiros sem sinal de 100, 8 byte.

11. O cliente envia uma mensagem CPMDisconnect para encerrar a conexão.

    O header da mensagem é populado da seguinte forma:

    -   **\_ msg** é definido como 0x000000C9, indicando que esta é uma mensagem CPMDisconnect.
    -   **\_ status** é definido como 0x00000000.
    -   **\_ ulChecksum** é definido como 0x00000000.

12. O servidor processa a mensagem e remove todo o estado do cliente.

### <a name="42-example-2"></a>4.2 Exemplo 2

No exemplo anterior, a consulta era bastante simples. Agora vamos considerar uma consulta um pouco mais complexa. Vamos supor que o usuário deseja recuperar o tamanho dos documentos que contêm as seguintes palavras: "Microsoft" e "Office". Isso é especificado alterando o campo Restrição contido na mensagem CPMCreateQueryIn enviada na etapa 5 da seguinte forma:

O **campo Restrição** é do tipo CRestriction e está definido como:

-   -   **\_ ulType** é definido como 0x00000004 (RTAnd).
    -   **\_ weight** é definido como 0x00000000.

O restante do campo contém uma estrutura CNodeRestriction:

-   -   **\_ cNode** é definido como 0x00000002, indicando que há dois nós na matriz paNode.
    -   O **\_ campo paNode** é uma matriz de duas estruturas CRestriction.

        **\_ paNode \[ 0 \]** contém:

        -   -   **\_ ulType** é definido como 0x00000004 (RTContent).
            -   **\_ weight** é definido como 0x00000000.
            -   O restante do campo contém uma estrutura CContentRestriction:
                -   **\_** A propriedade é definida como GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (para PRSPEC \_ PROPID) /0x13.
                -   **\_ Cc** é definido como 0x00000009.
                -   **\_ pwcsphrase é** definido como a cadeia de caracteres "Microsoft".
                -   **\_ lcid é** definido como 0x409 (para inglês).
                -   **\_ ulGenerateMethod** é definido como 0x00000000 (combinação exata).

        **\_ paNode \[ 1 \]** contém:

        -   -   **\_ ulType** é definido como 0x00000004 (RTContent).
            -   **\_ weight** é definido como 0x00000000.
            -   O restante do campo contém uma estrutura CContentRestriction:
                -   **\_** A propriedade é definida como GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (para PRSPEC \_ PROPID) /0x13.
                -   **\_ Cc** é definido como 0x00000006.
                -   **\_ pwcsphrase é** definido como a cadeia de caracteres "Office".
                -   **\_ lcid é** definido como 0x409 (para inglês).
                -   **\_ ulGenerateMethod** é definido como 0x00000000 (combinação exata).

## <a name="5-security"></a>5 Segurança

### <a name="51-security-considerations-for-implementers"></a>5.1 Considerações de segurança para implementadores

As implementações de indexação que indexam o conteúdo seguro devem considerar o uso do contexto de usuário fornecido pelo SMB MS-SMB para cortar os resultados da pesquisa e retornar somente aqueles acessíveis ao \[ \] chamador.

### <a name="52-index-of-security-parameters"></a>5.2 Índice de parâmetros de segurança



| Parâmetro de segurança  | Seção |
|---------------------|---------|
| Nível de representação | 2.1     |



 

## <a name="6-index-of-version-specific-behavior"></a>6 Índice de comportamento específico da versão



| Comportamento específico da versão                                                                         | Seção   | Windows 2000 | Windows XP | Windows Server 2003 |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| Esse protocolo é implementado no Windows 2000, Windows XP, Windows Server 2003 e Windows Vista. | 1.3.2     | X            | X          | X                   |
| Normalmente, os aplicativos interagem com um wrapper de interface OLE DB                                  | 1.4       | X            | X          | X                   |
| Valores de NTSTATUS                                                                                   | 1.8       | X            | X          | X                   |
| O cliente define o \_ campo status em cada cabeçalho de mensagem.                                        | 2.2.2     | X            | X          | X                   |
| o valor de cPendingScans geralmente é zero                                                               | 2.2.3.1   | X            | X          | X                   |
| valor de iClientVersion                                                                              | 2.2.3.6   | X            | X          | X                   |
| \_valor de cbChunk                                                                                   | 2.2.3.19  | X            | X          | X                   |
| endereços de memória de 32 bits e 64 bits                                                                | 3.2.4.2.4 | X            | X          | X                   |



 

 

 






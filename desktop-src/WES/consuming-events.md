---
title: Consumindo eventos (log de eventos do Windows)
description: Você pode consumir eventos de canais ou de arquivos de log.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb3fb1b36a0cd4ecf836a8893bc1abc14e46451
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105796462"
---
# <a name="consuming-events-windows-event-log"></a>Consumindo eventos (log de eventos do Windows)

Você pode consumir eventos de canais ou de arquivos de log. Para consumir eventos, você pode consumir todos os eventos ou pode especificar uma expressão XPath que identifique os eventos que você deseja consumir. Para determinar os elementos e atributos de um evento que você pode usar em sua expressão XPath, consulte [esquema de evento](eventschema-schema.md).

O log de eventos do Windows dá suporte a um subconjunto do XPath 1,0. Para obter detalhes sobre as limitações, consulte [limitações do XPath 1,0](#xpath-10-limitations).

Os exemplos a seguir mostram expressões XPath simples.


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



Você pode usar as expressões XPath diretamente ao chamar as funções [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ou pode usar uma consulta XML estruturada que contém a expressão XPath. Para consultas simples que consultam eventos de uma única fonte, o uso de uma expressão XPath é bom. Se a expressão XPath for uma expressão composta que contenha mais de 20 expressões ou se você estiver consultando eventos de várias fontes, deverá usar uma consulta XML estruturada. Para obter detalhes sobre os elementos de uma consulta XML estruturada, consulte [esquema de consulta](queryschema-schema.md).

Uma consulta estruturada identifica a origem dos eventos e um ou mais seletores ou supressers. Um seletor contém expressões XPath que selecionam eventos da origem e um supressor contém uma expressão XPath que impede a seleção de eventos. Você pode selecionar eventos de mais de uma fonte. Se um seletor e o supressor identificarem o mesmo evento, o evento não será incluído no resultado.

O seguinte mostra uma consulta XML estruturada que especifica um conjunto de seletores e supressers.


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



O conjunto de resultados da consulta não contém um instantâneo dos eventos no momento da consulta. Em vez disso, o conjunto de resultados inclui os eventos no momento da consulta e também conterá todos os novos eventos que são gerados que correspondam aos critérios de consulta enquanto você está enumerando os resultados.

> [!Note]  
> A ordem dos eventos é preservada para eventos que são gravados pelo mesmo thread. No entanto, é possível que os eventos escritos por threads separados em diferentes processadores de um computador com vários processadores apareçam fora de ordem.

 

Para obter detalhes sobre como consumir eventos, consulte os seguintes tópicos:

-   [Consultando eventos](querying-for-events.md)
-   [Inscrevendo-se em eventos](subscribing-to-events.md)
-   [Renderizando eventos](rendering-events.md)
-   [Formatando mensagens de evento](formatting-event-messages.md)
-   [Eventos de indicador](bookmarking-events.md)

As ferramentas de usuário final padrão para o evento de consumo são:

-   [Visualizador de Eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))
-   O cmdlet [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) do Windows PowerShell
-   [**WevtUtil**](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a>Limitações do XPath 1,0

O log de eventos do Windows dá suporte a um subconjunto do XPath 1,0. A principal restrição é que apenas elementos XML que representam eventos podem ser selecionados por um seletor de eventos. Uma consulta XPath que não seleciona um evento não é válida. Todos os caminhos de seletor válidos começam com \* ou "Event". Todos os caminhos de localização operam nos nós de evento e são compostos por uma série de etapas. Cada etapa é uma estrutura de três partes: o eixo, o teste de nó e o predicado. Para obter mais informações sobre essas partes e sobre o XPath 1,0, consulte [linguagem de caminho XML (XPath)](https://www.w3.org/TR/xpath). O log de eventos do Windows coloca as seguintes restrições na expressão:

-   Axis: há suporte apenas para o eixo filho (padrão) e o atributo (e seu "@") de atalho.
-   Testes de nó: há suporte apenas para os nomes de nó e os testes de NCName. O \* caractere "", que seleciona qualquer caractere, tem suporte.
-   Predicados: qualquer expressão XPath válida será aceitável se os caminhos de localização estiverem em conformidade com as seguintes restrições:
    -   Há suporte para operadores padrão **ou**, **e**, =,! =, <=, <, >=, > e parênteses.
    -   Não há suporte para a geração de um valor de cadeia de caracteres para um nome de nó.
    -   Não há suporte para a avaliação na ordem inversa.
    -   Não há suporte para conjuntos de nós.
    -   Não há suporte para o escopo do namespace.
    -   Não há suporte para namespace, processamento e nós de comentário.
    -   Não há suporte para o tamanho do contexto.
    -   Não há suporte para associações de variáveis.
    -   A função position e sua referência de matriz abreviada têm suporte (somente em nós folha).
    -   Há suporte para a função Band. A função executa um e bit e para dois argumentos de número inteiro. Se o resultado do bit e for diferente de zero, a função será avaliada como true; caso contrário, a função será avaliada como false.
    -   Há suporte para a função TIMEDIFF. A função computa a diferença entre o segundo argumento e o primeiro argumento. Um dos argumentos deve ser um número literal. Os argumentos devem usar a representação FILETIME. O resultado é o número de milissegundos entre as duas vezes. O resultado será positivo se o segundo argumento representar uma hora posterior; caso contrário, será negativo. Quando o segundo argumento não é fornecido, a hora atual do sistema é usada.

 

 

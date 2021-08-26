---
title: Escrevendo um manifesto de instrumentação
description: Aplicativos e DLLs usam um manifesto de instrumentação para identificar seus provedores de instrumentação e os eventos que os provedores escrevem.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc832278772a12195590a4efdb7b65478f22ef4a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812171"
---
# <a name="writing-an-instrumentation-manifest"></a>Escrevendo um manifesto de instrumentação

Aplicativos e DLLs usam um manifesto de instrumentação para identificar seus provedores de instrumentação e os eventos que os provedores escrevem. Um manifesto é um arquivo XML que contém os elementos que identificam seu provedor. A convenção é usar .man como a extensão para o manifesto. O manifesto deve estar em conformidade com o manifesto do evento XSD. Para obter detalhes sobre o esquema, consulte [Esquema EventManifest](eventmanifestschema-schema.md).

Um provedor de instrumentação é qualquer aplicativo ou DLL que chama as funções [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)ou [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) para gravar eventos em uma sessão de rastreamento de ETW [(Rastreamento](/windows/desktop/ETW/event-tracing-portal) de Eventos) ou em um canal de Log de Eventos. Um aplicativo pode definir um único provedor de instrumentação que abrange todos os eventos que ele grava ou pode definir um provedor para o aplicativo e um provedor para cada uma de suas DLLs. O número de provedores que o aplicativo define no manifesto depende apenas de como o aplicativo deseja organizar os eventos que ele grava.

A vantagem de especificar um provedor para cada DLL é que você pode habilitar e desabilitar os provedores individuais e, portanto, os eventos que eles geram. Essa vantagem se aplica somente se o provedor estiver habilitado por uma sessão de rastreamento ETW. Todos os eventos que especificam um canal de log de eventos são sempre gravados nesse canal.

O manifesto deve identificar o provedor e os eventos que ele grava, mas os outros metadados, como canais, níveis e palavras-chave, são opcionais; se você definir os metadados opcionais depende de quem consumirá os eventos. Por exemplo, se os administradores ou a equipe de suporte consumirem os eventos usando uma ferramenta como a Windows Visualizador de Eventos que lê eventos de canais de log de eventos, você deverá definir os canais nos quais os eventos são gravados. No entanto, se o provedor só for habilitado por uma sessão de rastreamento ETW, você não precisará definir canais.

Embora os níveis, tarefas, opcodes e metadados de palavras-chave sejam opcionais, você deve usá-los para agrupar ou agrupar logicamente os eventos. Agrupar os eventos ajuda os consumidores a consumir somente os eventos de interesse. Por exemplo, o consumidor pode consultar todos os eventos em que o nível é "crítico" e a palavra-chave é "write" ou consultar todos os eventos gravados por uma tarefa específica.

Além dos consumidores que usam o nível e palavras-chave para consumir tipos específicos de eventos, uma sessão de rastreamento ETW pode usar os metadados de nível e palavra-chave para dizer ao ETW para limitar os eventos gravados no log de rastreamento de eventos. Por exemplo, a sessão pode limitar os eventos somente a eventos em que level é "error" ou "critical" e a palavra-chave é "read".

Um provedor pode definir filtros que uma sessão usa para filtrar os eventos com base nos dados do evento. Com o nível e as palavras-chave, o ETW determina se o evento é gravado no log, mas com filtros, o provedor usa os critérios de dados de filtro para determinar se ele grava o evento nessa sessão. Os filtros são aplicáveis somente quando uma sessão de rastreamento ETW habilita seu provedor.

As seções a seguir mostram como definir os componentes do manifesto:

-   [Identificando o provedor](identifying-the-provider.md)
-   [Definindo os canais para onde os eventos são gravados](defining-channels.md)
-   [Definindo os níveis de severidade de eventos que o provedor grava](defining-severity-levels.md)
-   [Definindo as tarefas e operações que seu provedor executa](defining-tasks-and-opcodes.md)
-   [Definindo as palavras-chave que classificam os eventos que o provedor grava](defining-keywords-used-to-classify-types-of-events.md)
-   [Definindo os filtros que o provedor usa para filtrar os eventos que ele grava](defining-filters.md)
-   [Definindo os mapas de nome/valor referenciados por seus dados de modelo](defining-name-value-mappings.md)
-   [Definindo os modelos que definem os dados específicos do evento](defining-event-data-templates.md)
-   [Definindo os eventos que o provedor grava](defining-events.md)

Embora seja possível autor de um manifesto de instrumentação manualmente, você deve considerar o uso da ferramenta ECManGen.exe que está incluída na pasta Bin do \\ SDK Windows. A ECManGen.exe usa uma GUI que orienta você pela criação de um manifesto do zero sem precisar usar marcas XML. Ter conhecimento das informações nesta seção e na seção [Esquema eventManifest](eventmanifestschema-schema.md) ajudará ao usar a ferramenta.

Se você usar Visual Studio como seu editor XML, poderá adicionar o esquema [EventManifest](eventmanifestschema-schema.md) ao projeto (consulte o menu XML) para aproveitar o IntelliSense, a validação de esquema em linha e outros recursos para tornar a escrita do manifesto fácil e precisa.

Depois de escrever o manifesto, use o compilador de mensagem para validar o manifesto e gerar os arquivos de recurso e de header que você inclui em seu provedor. Para obter mais informações, consulte [Compilando um manifesto de instrumentação](compiling-an-instrumentation-manifest.md).

O exemplo a seguir mostra o esqueleto de um manifesto de evento totalmente definido.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 

---
title: Definindo modelos de dados de evento
description: Os provedores usam modelos de dados para definir os dados específicos de eventos que eles incluem com um evento e para definir os dados de filtro que uma sessão de rastreamento ETW pode passar para o provedor quando ele habilita o provedor.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5480ca158916801665943bd33b886bfcd5d73015e8730c1dd108123dadc1995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652606"
---
# <a name="defining-event-data-templates"></a>Definindo modelos de dados de evento

Os provedores usam modelos de dados para definir os dados específicos de eventos que eles incluem com um evento e para definir os dados de filtro que uma sessão de rastreamento ETW pode passar para o provedor quando ele habilita o provedor. Se o evento não incluir dados específicos do evento, você não definirá um modelo. Para definir um modelo, use o elemento **Template** . Um modelo inclui um item de dados para cada parte dos dados que o provedor inclui com o evento. Você pode especificar tipos, cadeias de caracteres, matrizes e estruturas integrais. Você deve gravar os dados do evento na ordem em que os itens de dados foram definidos no modelo.

Você também pode incluir no modelo um fragmento XML que os consumidores devem usar para determinar como renderizar os dados do evento. Se você não incluir o fragmento, os consumidores deverão renderizar os dados do evento na ordem em que os itens de dados foram definidos no modelo.

Ao definir um modelo, você deve dar a ele um identificador de modelo que você usa para fazer referência ao modelo em uma definição de evento. Cada item de dados no modelo deve especificar um nome e um tipo de dados de entrada (para obter uma lista de tipos de entrada, consulte a seção comentários do tipo complexo [**InputType**](eventmanifestschema-inputtype-complextype.md) ). Se o tipo de dados de entrada puder ser renderizado em vários formatos, você deverá especificar o tipo de dados de saída que informa aos consumidores como renderizar o item de dados. Por exemplo, um tipo de dados de entrada UInt32 pode ser renderizado como um inteiro não assinado, um identificador de thread, um endereço IPv4 e um código de erro Win32 entre outros. Se você não especificar o tipo de dados de saída, os consumidores deverão usar o tipo de saída padrão do tipo de entrada para renderizar o item de dados.

Para especificar uma matriz, inclua o atributo **Count** no item de dados e defina-o como o número de elementos na matriz. A matriz pode ser uma matriz de tamanho variável ou uma matriz de tamanho fixo. Se a matriz for uma matriz de tamanho fixo, defina **Count** como o tamanho da matriz. Por exemplo, se uma matriz de inteiros tiver um tamanho fixo de 10, defina a **contagem** como 10. Ao gravar a matriz, você deve gravar 40 bytes de dados.

Se a matriz for uma matriz de tamanho variável, defina **Count** como o nome do item de dados que contém o tamanho da matriz. Se a matriz contiver ponteiros, o endereço dos ponteiros será gravado como os dados do evento, não os dados aos quais os ponteiros apontam.

Você deve especificar o atributo **Length** se o item de dados for um blob binário. Você também pode especificar o atributo **Length** para cadeias de caracteres de comprimento fixo.

Especifique o atributo de **mapa** se o item de dados representar um valor de enumeração e você quiser que o consumidor imprima uma cadeia de caracteres para o valor em vez do próprio valor.

Se você incluir estruturas no modelo, deverá escrever os membros da estrutura individualmente em vez de escrever a estrutura, a menos que possa garantir o alinhamento de limites de 8 bytes.

Você deve considerar cuidadosamente as informações que você inclui nos eventos, especialmente quando os eventos são gravados nos canais globais. Como regra geral, você não deve incluir informações particulares nos eventos. Isso inclui senhas de texto sem formatação e informações de usuário pessoal. Além disso, os programas executados pelo usuário, URLs que o usuário visitou e outras informações relacionadas às atividades do usuário no computador devem ser consideradas particulares.

se você precisar registrar URLs e nomes de usuário nos eventos, não os grave nos canais de Windows (sistema e aplicativo), pois esses canais podem ser lidos por todos os usuários autenticados. Em vez disso, grave-os em seus próprios canais operacionais ou analíticos. Defina as permissões de acesso nesses canais para permitir que somente os administradores leiam os eventos. Talvez seja necessário fornecer uma divulgação apropriada para notificar os usuários do fato de que as informações privadas são disponibilizadas para os administradores.

O exemplo a seguir mostra como definir um modelo. Você deve especificar o atributo **tid** do modelo referenciado na definição de evento ou definição de filtro.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>
                    <template tid="t2">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>
                    </template>

                    <template tid="t3">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="ErrorCode" inType="win:Int32" outType="win:HResult"/>
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="BufferSize" inType="win:UInt32" />
                        <data name="Buffer" inType="win:Binary" length="BufferSize"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />
                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Value" inType="win:UInt16" />
                            <data name="Name" inType="win:UnicodeString" />
                        </struct>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

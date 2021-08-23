---
description: Provedores baseados em manifesto usam um manifesto para publicar o esquema para seus eventos.
ms.assetid: 37d1a504-ecc7-4df3-bf31-546debb62123
title: Publicando seu esquema de evento para um provedor baseado em manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d2ffd6d991e90ea19d20e78d3d18faff3d24c158d285834b23838b10e78239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069826"
---
# <a name="publishing-your-event-schema-for-a-manifest-based-provider"></a>Publicando seu esquema de evento para um provedor baseado em manifesto

Provedores [baseados em manifesto](about-event-tracing.md) usam um manifesto para publicar o esquema para seus eventos. O manifesto é inserido no binário do provedor, o que significa que o provedor deve estar disponível no computador para que o consumidor consuma seus eventos. Para obter detalhes completos sobre como escrever um manifesto, consulte [escrevendo um manifesto de instrumentação](../wes/writing-an-instrumentation-manifest.md).

O manifesto a seguir define os eventos que são usados em exemplos na seção [fornecendo eventos](providing-events.md) e [consumindo eventos](consuming-events.md) do documento.

``` syntax
<!-- <?xml version="1.0" encoding="UTF-16"?> -->
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>

            <provider name="Microsoft-Windows-ETWProvider" 
                guid="{D8909C24-5BE9-4502-98CA-AB7BDC24899D}" 
                symbol="ProviderGuid" 
                resourceFileName="c:\code\etw\v2provider\debug\v2provider.exe" 
                messageFileName="c:\code\etw\v2provider\debug\v2provider.exe"
                message="$(string.Provider.Name)"
                >

                <keywords>
                    <keyword name="Read" symbol="READ_KEYWORD" mask="0x1" />
                    <keyword name="Write" symbol="WRITE_KEYWORD" mask="0x2" />
                    <keyword name="Local" symbol="LOCAL_KEYWORD" mask="0x4" />
                    <keyword name="Remote" symbol="REMOTE_KEYWORD" mask="0x8" />
                </keywords>

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.Map.Download)"/>
                        <map value="2" message="$(string.Map.Upload)"/>
                        <map value="3" message="$(string.Map.UploadReply)"/>
                    </valueMap>

                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.Map.Sunday)"/>
                        <map value="0x2" message="$(string.Map.Monday)"/>
                        <map value="0x4" message="$(string.Map.Tuesday)"/>
                        <map value="0x8" message="$(string.Map.Wednesday)"/>
                        <map value="0x10" message="$(string.Map.Thursday)"/>
                        <map value="0x20" message="$(string.Map.Friday)"/>
                        <map value="0x40" message="$(string.Map.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>

                   <template tid="TransferTemplate">
                        <data name="Image" inType="win:Pointer"/>
                        <data name="Scores" inType="win:UInt16" count="3"/>
                        <data name="ID" inType="win:GUID"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />

                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Name" inType="win:UnicodeString" />
                            <data name="Value" inType="win:UInt16" />
                        </struct>

                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>

                        <UserData>
                            <EventData xmlns="ProviderNamespace">
                                <Transfer> %10 </Transfer>
                                <Day> %9 </Day>
                                <ValuesCount> %7 </ValuesCount>
                                <Values> %8 </Values>
                                <Path> %6 </Path>
                                <IsLocal> %5 </IsLocal>
                                <Scores> %2 </Scores>
                                <Image> %1 </Image>
                                <Certificate> %4 </Certificate>
                                <ID> %3 </ID>
                            </EventData>
                        </UserData>
                    </template>

                </templates>

                <events>
                    <event value="1" 
                        level="win:Informational" 
                        template="TransferTemplate" 
                        symbol="TransferEvent"
                        message ="$(string.Event.WhenToTransfer)"
                        keywords="Read Local" />
                </events>


            </provider>

        </events>

    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>

                <string id="Provider.Name" value="Microsoft-Windows-ETWProvider"/>

                <string id="Map.Download" value="Download"/>
                <string id="Map.Upload" value="Upload"/>
                <string id="Map.UploadReply" value="Upload-reply"/> 

                <string id="Map.Sunday" value="Sunday"/>
                <string id="Map.Monday" value="Monday"/>
                <string id="Map.Tuesday" value="Tuesday"/>
                <string id="Map.Wednesday" value="Wednesday"/>
                <string id="Map.Thursday" value="Thursday"/>
                <string id="Map.Friday" value="Friday"/>
                <string id="Map.Saturday" value="Saturday"/>

                <string id="Event.WhenToTransfer" value="The %10 transfer will occur %9."/>

            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

 

 

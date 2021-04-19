---
title: Gravador de XML
description: O gravador de XML é uma API para emitir XML. Essencialmente, um gravador de XML grava um nó XML por vez, mas há APIs auxiliares adicionais para facilitar a gravação de uma seqüência de nós.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Serviços Web de gravador XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085a02b3aca33ffa3b31e4579d47068a683ee4d8
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105771421"
---
# <a name="xml-writer"></a>Gravador de XML

O gravador de XML é uma API para emitir XML. Essencialmente, um gravador de XML grava um [nó XML](xml-node.md) por vez, mas há APIs auxiliares adicionais para facilitar a gravação de uma seqüência de nós.


Há suporte para os seguintes tipos de saída do gravador:

-   [**Um buffer na memória de bytes codificados**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**Um fluxo**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   Um [buffer XML](xml-buffer.md)

Os seguintes retornos de chamada são usados com o gravador de XML:

-   [**\_retorno de \_ chamada de cadeia de caracteres dinâmica WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**\_retorno de \_ chamada de bytes WS pull \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**\_retorno de \_ chamada de bytes do WS Push \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**\_retorno de \_ chamada WS Write**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

As seguintes enumerações são usadas com o gravador de XML:

-   [**conjunto de \_ caracteres WS**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**\_tipo de \_ codificação de gravador \_ \_ do WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**\_tipo de \_ saída do gravador \_ \_ do WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**\_ID da \_ Propriedade do gravador XML \_ do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

As funções a seguir são usadas com o gravador de XML:

-   [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [**WsCreateWriter**](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [**WsFreeWriter**](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [**WsGetPrefixFromNamespace**](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [**WsGetWriterProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [**WsPullBytes**](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [**WsPushBytes**](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [**WsSetOutput**](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [**WsWriteArray**](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [**WsWriteBytes**](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [**WsWriteChars**](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [**WsWriteCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [**WsWriteEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [**WsWriteEndCData**](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [**WsWriteEndElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [**WsWriteQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [**WsWriteStartCData**](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [**WsWriteStartElement**](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [**WsWriteText**](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [**WsWriteValue**](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [**WsWriteXmlnsAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

O identificador a seguir é usado com o gravador de XML:

-   [gravador do WS \_ XML \_](ws-xml-writer.md)

As seguintes estruturas são usadas com o gravador de XML:

-   [**\_ \_ \_ codificação binária de gravador \_ do WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**\_saída do \_ buffer do gravador \_ \_ do WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**\_codificação de \_ gravador de XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**\_codificação de \_ MTOM do gravador de XML do WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**\_saída do \_ gravador de XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**\_Propriedades do \_ gravador \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**\_Propriedade do \_ gravador de XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**\_saída de \_ fluxo do gravador XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**\_codificação de \_ texto de gravador \_ \_ do WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 





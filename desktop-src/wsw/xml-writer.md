---
title: XML Writer
description: O Xml Writer é uma API para emitir XML. Em seu núcleo, um Xml Writer grava um Nó XML por vez, mas há APIs auxiliares adicionais para facilitar a escrita de uma sequência de nós.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Serviços Web do Xml Writer para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75b7937ac6d8f6e9daff40289dd34729eaf235f203a02b91b5d1af3632049b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026054"
---
# <a name="xml-writer"></a>XML Writer

O Xml Writer é uma API para emitir XML. Em seu núcleo, um Xml Writer grava um Nó [XML](xml-node.md) por vez, mas há APIs auxiliares adicionais para facilitar a escrita de uma sequência de nós.


Há suporte para os seguintes tipos de saída do writer:

-   [**Um buffer na memória de bytes codificados**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**Um fluxo**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   Um [buffer XML](xml-buffer.md)

Os retornos de chamada a seguir são usados com o autor xml:

-   [**RETORNO DE CHAMADA \_ DE CADEIA DE \_ \_ CARACTERES DINÂMICA DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**RETORNO DE \_ CHAMADA DE BYTES DE PULL \_ \_ DO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**WS \_ PUSH \_ BYTES \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS \_ WRITE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

As enumerações a seguir são usadas com o autor XML:

-   [**CHARSET do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**TIPO DE CODIFICAÇÃO DO WS \_ XML \_ \_ \_ WRITER**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**TIPO DE SAÍDA \_ DO WS XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**ID DA PROPRIEDADE \_ DO WS XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

As seguintes funções são usadas com o autor XML:

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

O seguinte handle é usado com o autor XML:

-   [WS \_ XML \_ WRITER](ws-xml-writer.md)

As seguintes estruturas são usadas com o autor XML:

-   [**CODIFICAÇÃO BINÁRIA DO WS \_ XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**SAÍDA DO \_ \_ BUFFER DO \_ WS XML WRITER \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**CODIFICAÇÃO \_ \_ DO WS XML WRITER \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**CODIFICAÇÃO \_ \_ \_ MTOM DO \_ WS XML WRITER**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**SAÍDA DO \_ WS XML \_ WRITER \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**PROPRIEDADES DO \_ WS XML \_ WRITER \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**PROPRIEDADE DO \_ WS XML \_ \_ WRITER**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**SAÍDA DE \_ FLUXO DO WS XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**CODIFICAÇÃO DE TEXTO DO WS \_ XML \_ WRITER \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 





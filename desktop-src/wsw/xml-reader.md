---
title: XML Reader
description: O leitor de XML é um cursor sobre uma fonte de entrada de XML. Em seu núcleo, um leitor de XML lê um nó XML por vez, mas há APIs auxiliares adicionais para facilitar a leitura de uma sequência de nós.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- Serviços Web do XML Reader para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a03ef961cd49c481564b6bad1ad86603c9cb576f0c8aeda1a7cd2d6d18aaeef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770866"
---
# <a name="xml-reader"></a>XML Reader

O leitor de XML é um cursor sobre uma fonte de entrada de XML. Em seu núcleo, um leitor de XML lê um [nó XML](xml-node.md) por vez, mas há APIs auxiliares adicionais para facilitar a leitura de uma sequência de nós.


Há suporte para os seguintes tipos de entrada de leitores:

-   [**Um buffer na memória de bytes codificados**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**Um fluxo**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   Um [buffer XML](xml-buffer.md)

### <a name="security"></a>Segurança

O leitor verificará se os atributos presentes em um elemento são exclusivos. O tempo necessário para realizar essa validação é uma função do número de atributos no elemento que pode ser tão grande quanto os [**\_ \_ \_ \_ \_ atributos máximos da propriedade leitor do WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Portanto, o processamento de documentos grandes quando os **\_ \_ \_ \_ \_ atributos máximos da Propriedade do leitor de XML do WS** está definido como um valor grande pode apresentar uma oportunidade para um ataque de negação de serviço.

O leitor mapeará prefixos para namespaces para cada elemento e atributos. O tempo necessário para realizar esse mapeamento é uma função do número de atributos xmlns no escopo que pode ser tão grande quanto os [**\_ \_ \_ \_ \_ namespaces máximos da propriedade leitor do WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Portanto, o processamento de documentos grandes quando essa propriedade é definida como um valor grande pode apresentar uma oportunidade para um ataque de negação de serviço.

Embora o leitor garanta que o documento segue a especificação gramatical do XML e, além disso, que seus aspectos estejam dentro das cotas especificadas, o conteúdo do documento ainda deve ser considerado não confiável ao chegar de uma fonte não confiável. Os usuários do leitor devem verificar todos os nomes de elemento e atributo e namespaces usando [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)ou inspecionando [**nós**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)manualmente.

Algumas outras situações a serem consideradas incluem, mas não estão limitadas a:

-   Os elementos esperados podem estar ausentes
-   Elementos inesperados podem aparecer
-   Atributos esperados podem estar ausentes
-   Atributos inesperados podem aparecer
-   Elementos podem aparecer como elementos vazios
-   O espaço em branco pode aparecer em locais inesperados

Os usuários do leitor não devem alocar memória com base apenas nos valores lidos do documento. Por exemplo, considere o seguinte documento XML:

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

Alocar uma matriz com base no pressuposto de que algum número de elementos será seguido seria um vetor de ataque potencial. O usuário do leitor, nesse caso, deve alocar incrementalmente a memória conforme os elementos aparecem.

O leitor de XML não dá suporte a DTD. O usuário do leitor não precisa se preocupar com a verificação de DTD.

O retorno de chamada a seguir é usado com leitores XML:

-   [**\_retorno de \_ chamada WS Read**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

As seguintes enumerações são usadas com leitores XML:

-   [**\_tipo de \_ codificação de leitor de XML do WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_tipo de \_ entrada do leitor de XML WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [**\_ID de \_ Propriedade do leitor XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

As funções a seguir são usadas com leitores XML:

-   [**WsCreateReader**](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [**WsFreeReader**](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [**WsGetNamespaceFromPrefix**](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [**WsGetReaderNode**](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [**WsGetReaderProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [**WsReadArray**](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [**WsReadBytes**](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [**WsReadChars**](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [**WsReadCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [**WsReadEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [**WsReadQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [**WsReadStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [**WsSetInput**](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [**WsSkipNode**](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

O seguinte identificador é usado com leitores XML:

-   [\_leitor de XML do WS \_](ws-xml-reader.md)

As seguintes estruturas são usadas com leitores XML:

-   [**\_ \_ codificação binária de leitor XML \_ do \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [**\_entrada de \_ buffer de leitor de XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**\_codificação de \_ leitor \_ XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [**\_entrada do \_ leitor de XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [**\_codificação de \_ MTOM do leitor XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [**\_Propriedades do \_ leitor \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [**\_ \_ Propriedade leitor de XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [**\_entrada de \_ fluxo de leitor XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [**\_codificação de \_ texto do leitor XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 





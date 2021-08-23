---
title: Nó XML
description: Um nó XML representa uma única parte do XML, por exemplo, um elemento inicial e seus atributos, um elemento final, um texto ou um \ 0034; digitado \ 0034; conteúdo de texto, como um número inteiro ou matriz de bytes. Os dados em um nó variam de acordo com o \_ tipo de nó do WS XML \_ \_ .
ms.assetid: c514c542-029b-46d1-a796-1f132a41b2ad
keywords:
- Serviços Web do nó XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b851ad0ab0a6a333fedea13036eebf11e8c727a04603c07d8f7e68e66de5ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545646"
---
# <a name="xml-node"></a>Nó XML

Um nó XML representa uma única parte do XML, por exemplo, um elemento inicial e seus atributos, um elemento final, um texto ou um conteúdo de texto "digitado", como um número inteiro ou matriz de bytes. Os dados em um nó variam de acordo com [**o \_ \_ \_ tipo de nó do WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).


Veja a seguir um exemplo de um documento XML específico de codificação representado com estruturas independentes de codificação.

``` syntax
<p:PurchaseOrder xmlns:p="http://tempuri.org" p:id="3891">
    <p:Buyer>Joe</p:Buyer>
</p:PurchaseOrder>
```

``` syntax
WS_XML_STRING purchaseOrder = WS_XML_STRING_VALUE("PurchaseOrder");
WS_XML_STRING id            = WS_XML_STRING_VALUE("id");
WS_XML_STRING prefix        = WS_XML_STRING_VALUE("p");
WS_XML_STRING ns            = WS_XML_STRING_VALUE("http://tempuri.org");

WS_XML_ATTRIBUTE xmlnsAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ TRUE,
    /* prefix      */ &prefix,
    /* localName   */ NULL,
    /* ns          */ &ns,
    /* value       */ NULL
};
WS_XML_INT32_TEXT idText =
{
    /* text  */ { WS_XML_TEXT_TYPE_INT32 },
    /* value */ 3891
};
WS_XML_ATTRIBUTE idAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ FALSE,
    /* prefix      */ &prefix,
    /* localName   */ &id,
    /* ns          */ &ns,
    /* value       */ &idText.text,
};
WS_XML_ATTRIBUTE* attributes[2] =
{
    &xmlnsAttribute,
    &idAttribute
};
WS_XML_ELEMENT_NODE elementNode =
{
    /* node           */ { WS_XML_NODE_TYPE_ELEMENT },
    /* prefix         */ &prefix,
    /* localName      */ &purchaseOrder,
    /* ns             */ &ns,
    /* attributeCount */ 2,
    /* attributes     */ attributes,
    /* isEmpty        */ FALSE,
    /* array          */ NULL,
};
WS_XML_UTF8_TEXT joeText =
{
    /* text  */ { WS_XML_TEXT_TYPE_UTF8 },
    /* value */ WS_XML_STRING_VALUE("Joe")
};
WS_XML_TEXT_NODE textNode =
{
    /* node */ { WS_XML_NODE_TYPE_TEXT },
    /* text */ &joeText.text
};
WS_XML_NODE endElementNode =
{
    WS_XML_NODE_TYPE_END_ELEMENT
};
WS_XML_NODE* nodes[3] =
{
    &elementNode.node,
    &textNode.node,
    &endElementNode
};
```

As seguintes enumerações são usadas com nós XML:

-   [**\_tipo de valor WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [**tipo de nó do WS \_ XML \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [**\_tipo de \_ texto \_ XML do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

As funções a seguir são usadas com nós XML:

-   [**WsTrimXmlWhitespace**](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [**WsVerifyXmlNCName**](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [**WsXmlStringEquals**](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

As macros a seguir são usadas com nós XML:

-   [**\_valor de \_ dicionário de cadeia de caracteres XML do \_ WS \_**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   [**\_cadeia de caracteres XML do WS \_ \_ nula**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))
-   [**\_valor de \_ cadeia de caracteres XML do WS \_**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

As seguintes estruturas são usadas com nós XML:

-   [**\_atributo XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [**\_ \_ Texto base64 do WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [**\_ \_ texto bool do WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [**\_nó de \_ comentário \_ XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [**\_texto de \_ data e hora XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [**\_ \_ texto decimal do WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [**\_dicionário XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [**\_ \_ texto duplo do WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [**\_nó de \_ elemento \_ XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [**\_ \_ texto flutuante do WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [**\_texto de \_ GUID \_ XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [**\_ \_ Texto INT32 XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [**\_ \_ Texto Int64 do WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [**texto de lista do WS \_ XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [**\_nó XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [**QName de WS \_ XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [**texto de QName do WS \_ XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [**\_cadeia de caracteres XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [**\_texto XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [**\_nó de \_ texto \_ XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [**\_texto de \_ TIMESPAN \_ XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [**\_Texto de \_ UINT64 \_ XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [**\_texto de \_ \_ ID exclusivo \_ do WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [**\_ \_ Texto UTF16 do WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [**Texto do WS \_ XML \_ UTF8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 
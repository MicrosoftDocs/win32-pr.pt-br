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
ms.openlocfilehash: ac212205fac02db0ee87d8acbe0b123ffcead921
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105771422"
---
# <a name="xml-node"></a><span data-ttu-id="82580-107">Nó XML</span><span class="sxs-lookup"><span data-stu-id="82580-107">XML Node</span></span>

<span data-ttu-id="82580-108">Um nó XML representa uma única parte do XML, por exemplo, um elemento inicial e seus atributos, um elemento final, um texto ou um conteúdo de texto "digitado", como um número inteiro ou matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="82580-108">An XML Node represents a single piece of XML, for example, a start element and its attributes, an end element, text, or "typed" text content such as an integer or byte array.</span></span> <span data-ttu-id="82580-109">Os dados em um nó variam de acordo com [**o \_ \_ \_ tipo de nó do WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span><span class="sxs-lookup"><span data-stu-id="82580-109">The data in a node varies according to the [**WS\_XML\_NODE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span></span>


<span data-ttu-id="82580-110">Veja a seguir um exemplo de um documento XML específico de codificação representado com estruturas independentes de codificação.</span><span class="sxs-lookup"><span data-stu-id="82580-110">The following shows an example of an encoding specific xml document represented with encoding independent structures.</span></span>

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

<span data-ttu-id="82580-111">As seguintes enumerações são usadas com nós XML:</span><span class="sxs-lookup"><span data-stu-id="82580-111">The following enumerations are used with XML nodes:</span></span>

-   [<span data-ttu-id="82580-112">**\_tipo de valor WS \_**</span><span class="sxs-lookup"><span data-stu-id="82580-112">**WS\_VALUE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [<span data-ttu-id="82580-113">**tipo de nó do WS \_ XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="82580-113">**WS\_XML\_NODE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [<span data-ttu-id="82580-114">**\_tipo de \_ texto \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="82580-114">**WS\_XML\_TEXT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

<span data-ttu-id="82580-115">As funções a seguir são usadas com nós XML:</span><span class="sxs-lookup"><span data-stu-id="82580-115">The following functions are used with XML nodes:</span></span>

-   [<span data-ttu-id="82580-116">**WsTrimXmlWhitespace**</span><span class="sxs-lookup"><span data-stu-id="82580-116">**WsTrimXmlWhitespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [<span data-ttu-id="82580-117">**WsVerifyXmlNCName**</span><span class="sxs-lookup"><span data-stu-id="82580-117">**WsVerifyXmlNCName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [<span data-ttu-id="82580-118">**WsXmlStringEquals**</span><span class="sxs-lookup"><span data-stu-id="82580-118">**WsXmlStringEquals**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

<span data-ttu-id="82580-119">As macros a seguir são usadas com nós XML:</span><span class="sxs-lookup"><span data-stu-id="82580-119">The following macros are used with XML nodes:</span></span>

-   [<span data-ttu-id="82580-120">**\_valor de \_ dicionário de cadeia de caracteres XML do \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="82580-120">**WS\_XML\_STRING\_DICTIONARY\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   <span data-ttu-id="82580-121">[**\_cadeia de caracteres XML do WS \_ \_ nula**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82580-121">[**WS\_XML\_STRING\_NULL**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span></span>
-   [<span data-ttu-id="82580-122">**\_valor de \_ cadeia de caracteres XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="82580-122">**WS\_XML\_STRING\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

<span data-ttu-id="82580-123">As seguintes estruturas são usadas com nós XML:</span><span class="sxs-lookup"><span data-stu-id="82580-123">The following structures are used with XML nodes:</span></span>

-   [<span data-ttu-id="82580-124">**\_atributo XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="82580-124">**WS\_XML\_ATTRIBUTE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [<span data-ttu-id="82580-125">**\_ \_ Texto base64 do WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="82580-125">**WS\_XML\_BASE64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [<span data-ttu-id="82580-126">**\_ \_ texto bool do WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="82580-126">**WS\_XML\_BOOL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [<span data-ttu-id="82580-127">**\_nó de \_ comentário \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="82580-127">**WS\_XML\_COMMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [<span data-ttu-id="82580-128">**\_texto de \_ data e hora XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="82580-128">**WS\_XML\_DATETIME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [<span data-ttu-id="82580-129">**\_ \_ texto decimal do WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="82580-129">**WS\_XML\_DECIMAL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [<span data-ttu-id="82580-130">**\_dicionário XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="82580-130">**WS\_XML\_DICTIONARY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [<span data-ttu-id="82580-131">**\_ \_ texto duplo do WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="82580-131">**WS\_XML\_DOUBLE\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [<span data-ttu-id="82580-132">**\_nó de \_ elemento \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="82580-132">**WS\_XML\_ELEMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [<span data-ttu-id="82580-133">**\_ \_ texto flutuante do WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="82580-133">**WS\_XML\_FLOAT\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [<span data-ttu-id="82580-134">**\_texto de \_ GUID \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="82580-134">**WS\_XML\_GUID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [<span data-ttu-id="82580-135">**\_ \_ Texto INT32 XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="82580-135">**WS\_XML\_INT32\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [<span data-ttu-id="82580-136">**\_ \_ Texto Int64 do WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="82580-136">**WS\_XML\_INT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [<span data-ttu-id="82580-137">**texto de lista do WS \_ XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="82580-137">**WS\_XML\_LIST\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [<span data-ttu-id="82580-138">**\_nó XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="82580-138">**WS\_XML\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [<span data-ttu-id="82580-139">**QName de WS \_ XML \_**</span><span class="sxs-lookup"><span data-stu-id="82580-139">**WS\_XML\_QNAME**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [<span data-ttu-id="82580-140">**texto de QName do WS \_ XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="82580-140">**WS\_XML\_QNAME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [<span data-ttu-id="82580-141">**\_cadeia de caracteres XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="82580-141">**WS\_XML\_STRING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [<span data-ttu-id="82580-142">**\_texto XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="82580-142">**WS\_XML\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [<span data-ttu-id="82580-143">**\_nó de \_ texto \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="82580-143">**WS\_XML\_TEXT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [<span data-ttu-id="82580-144">**\_texto de \_ TIMESPAN \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="82580-144">**WS\_XML\_TIMESPAN\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [<span data-ttu-id="82580-145">**\_Texto de \_ UINT64 \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="82580-145">**WS\_XML\_UINT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [<span data-ttu-id="82580-146">**\_texto de \_ \_ ID exclusivo \_ do WS XML**</span><span class="sxs-lookup"><span data-stu-id="82580-146">**WS\_XML\_UNIQUE\_ID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [<span data-ttu-id="82580-147">**\_ \_ Texto UTF16 do WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="82580-147">**WS\_XML\_UTF16\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [<span data-ttu-id="82580-148">**Texto do WS \_ XML \_ UTF8 \_**</span><span class="sxs-lookup"><span data-stu-id="82580-148">**WS\_XML\_UTF8\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 
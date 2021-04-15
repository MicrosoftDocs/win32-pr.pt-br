---
title: XML Reader
description: O leitor de XML é um cursor sobre uma fonte de entrada de XML. Em seu núcleo, um leitor de XML lê um nó XML por vez, mas há APIs auxiliares adicionais para facilitar a leitura de uma sequência de nós.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- Web Services do XML Reader para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9d9c91b6594ec569536751751a3efca4c32e08
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104454459"
---
# <a name="xml-reader"></a><span data-ttu-id="148d4-107">XML Reader</span><span class="sxs-lookup"><span data-stu-id="148d4-107">XML Reader</span></span>

<span data-ttu-id="148d4-108">O leitor de XML é um cursor sobre uma fonte de entrada de XML.</span><span class="sxs-lookup"><span data-stu-id="148d4-108">XML Reader is a cursor over an input source of XML.</span></span> <span data-ttu-id="148d4-109">Em seu núcleo, um leitor de XML lê um [nó XML](xml-node.md) por vez, mas há APIs auxiliares adicionais para facilitar a leitura de uma sequência de nós.</span><span class="sxs-lookup"><span data-stu-id="148d4-109">At its core, an XML Reader reads one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make reading a sequence of nodes easier.</span></span>


<span data-ttu-id="148d4-110">Há suporte para os seguintes tipos de entrada de leitores:</span><span class="sxs-lookup"><span data-stu-id="148d4-110">The following types of readers input are supported:</span></span>

-   [<span data-ttu-id="148d4-111">**Um buffer na memória de bytes codificados**</span><span class="sxs-lookup"><span data-stu-id="148d4-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="148d4-112">**Um fluxo**</span><span class="sxs-lookup"><span data-stu-id="148d4-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   <span data-ttu-id="148d4-113">Um [buffer XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="148d4-113">An [XML Buffer](xml-buffer.md)</span></span>

### <a name="security"></a><span data-ttu-id="148d4-114">Segurança</span><span class="sxs-lookup"><span data-stu-id="148d4-114">Security</span></span>

<span data-ttu-id="148d4-115">O leitor verificará se os atributos presentes em um elemento são exclusivos.</span><span class="sxs-lookup"><span data-stu-id="148d4-115">The reader will verify that the attributes present on an element are unique.</span></span> <span data-ttu-id="148d4-116">O tempo necessário para realizar essa validação é uma função do número de atributos no elemento que pode ser tão grande quanto os [**\_ \_ \_ \_ \_ atributos máximos da propriedade leitor do WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span><span class="sxs-lookup"><span data-stu-id="148d4-116">The time required to perform this validation is a function of the number of attributes on the element which can be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="148d4-117">Portanto, o processamento de documentos grandes quando os **\_ \_ \_ \_ \_ atributos máximos da Propriedade do leitor de XML do WS** está definido como um valor grande pode apresentar uma oportunidade para um ataque de negação de serviço.</span><span class="sxs-lookup"><span data-stu-id="148d4-117">Therefore, processing large documents when **WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES** is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="148d4-118">O leitor mapeará prefixos para namespaces para cada elemento e atributos.</span><span class="sxs-lookup"><span data-stu-id="148d4-118">The reader will map prefixes to namespaces for each element and attributes.</span></span> <span data-ttu-id="148d4-119">O tempo necessário para realizar esse mapeamento é uma função do número de atributos xmlns no escopo que pode ser tão grande quanto os [**\_ \_ \_ \_ \_ namespaces máximos da propriedade leitor do WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span><span class="sxs-lookup"><span data-stu-id="148d4-119">The time required to perform this mapping is a function of the number of xmlns attributes in scope which may be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_NAMESPACES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="148d4-120">Portanto, o processamento de documentos grandes quando essa propriedade é definida como um valor grande pode apresentar uma oportunidade para um ataque de negação de serviço.</span><span class="sxs-lookup"><span data-stu-id="148d4-120">Therefore, processing large documents when this property is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="148d4-121">Embora o leitor garanta que o documento segue a especificação gramatical do XML e, além disso, que seus aspectos estejam dentro das cotas especificadas, o conteúdo do documento ainda deve ser considerado não confiável ao chegar de uma fonte não confiável.</span><span class="sxs-lookup"><span data-stu-id="148d4-121">While the reader will ensure that the document follows the grammatical specification of xml and furthermore that its aspects are within the quotas specified, the content of the document must still be considered untrusted when coming from an untrusted source.</span></span> <span data-ttu-id="148d4-122">Os usuários do leitor devem verificar todos os nomes de elemento e atributo e namespaces usando [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)ou inspecionando [**nós**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)manualmente.</span><span class="sxs-lookup"><span data-stu-id="148d4-122">Users of the reader should check all element and attribute names and namespaces using [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute), or by manually inspecting [**nodes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span></span>

<span data-ttu-id="148d4-123">Algumas outras situações a serem consideradas incluem, mas não estão limitadas a:</span><span class="sxs-lookup"><span data-stu-id="148d4-123">Some other situations to consider include, but are not limited to:</span></span>

-   <span data-ttu-id="148d4-124">Os elementos esperados podem estar ausentes</span><span class="sxs-lookup"><span data-stu-id="148d4-124">Expected elements may be missing</span></span>
-   <span data-ttu-id="148d4-125">Elementos inesperados podem aparecer</span><span class="sxs-lookup"><span data-stu-id="148d4-125">Unexpected elements may appear</span></span>
-   <span data-ttu-id="148d4-126">Atributos esperados podem estar ausentes</span><span class="sxs-lookup"><span data-stu-id="148d4-126">Expected attributes may be missing</span></span>
-   <span data-ttu-id="148d4-127">Atributos inesperados podem aparecer</span><span class="sxs-lookup"><span data-stu-id="148d4-127">Unexpected attributes may appear</span></span>
-   <span data-ttu-id="148d4-128">Elementos podem aparecer como elementos vazios</span><span class="sxs-lookup"><span data-stu-id="148d4-128">Elements may appear as empty elements</span></span>
-   <span data-ttu-id="148d4-129">O espaço em branco pode aparecer em locais inesperados</span><span class="sxs-lookup"><span data-stu-id="148d4-129">Whitespace may appear in unexpected places</span></span>

<span data-ttu-id="148d4-130">Os usuários do leitor não devem alocar memória com base apenas nos valores lidos do documento.</span><span class="sxs-lookup"><span data-stu-id="148d4-130">Users of the reader should not allocate memory based simply on values read from the document.</span></span> <span data-ttu-id="148d4-131">Por exemplo, considere o seguinte documento XML:</span><span class="sxs-lookup"><span data-stu-id="148d4-131">For example, consider the following xml document:</span></span>

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

<span data-ttu-id="148d4-132">Alocar uma matriz com base no pressuposto de que algum número de elementos será seguido seria um vetor de ataque potencial.</span><span class="sxs-lookup"><span data-stu-id="148d4-132">Allocating an array based soley on the assumption that some number of elements will follow would be a potential attack vector.</span></span> <span data-ttu-id="148d4-133">O usuário do leitor, nesse caso, deve alocar incrementalmente a memória conforme os elementos aparecem.</span><span class="sxs-lookup"><span data-stu-id="148d4-133">The user of the reader in this case should instead incrementally allocate the memory as the elements appear.</span></span>

<span data-ttu-id="148d4-134">O leitor de XML não dá suporte a DTD.</span><span class="sxs-lookup"><span data-stu-id="148d4-134">XML reader does not support DTD.</span></span> <span data-ttu-id="148d4-135">O usuário do leitor não precisa se preocupar com a verificação de DTD.</span><span class="sxs-lookup"><span data-stu-id="148d4-135">The user of the reader does not need to concern about DTD verification.</span></span>

<span data-ttu-id="148d4-136">O retorno de chamada a seguir é usado com leitores XML:</span><span class="sxs-lookup"><span data-stu-id="148d4-136">The following callback is used with XML readers:</span></span>

-   [<span data-ttu-id="148d4-137">**\_retorno de \_ chamada WS Read**</span><span class="sxs-lookup"><span data-stu-id="148d4-137">**WS\_READ\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

<span data-ttu-id="148d4-138">As seguintes enumerações são usadas com leitores XML:</span><span class="sxs-lookup"><span data-stu-id="148d4-138">The following enumerations are used with XML readers:</span></span>

-   [<span data-ttu-id="148d4-139">**\_tipo de \_ codificação de leitor de XML do WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="148d4-139">**WS\_XML\_READER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="148d4-140">**\_tipo de \_ entrada do leitor de XML WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="148d4-140">**WS\_XML\_READER\_INPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [<span data-ttu-id="148d4-141">**\_ID de \_ Propriedade do leitor XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="148d4-141">**WS\_XML\_READER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="148d4-142">As funções a seguir são usadas com leitores XML:</span><span class="sxs-lookup"><span data-stu-id="148d4-142">The following functions are used with XML readers:</span></span>

-   [<span data-ttu-id="148d4-143">**WsCreateReader**</span><span class="sxs-lookup"><span data-stu-id="148d4-143">**WsCreateReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [<span data-ttu-id="148d4-144">**WsFillReader**</span><span class="sxs-lookup"><span data-stu-id="148d4-144">**WsFillReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [<span data-ttu-id="148d4-145">**WsFindAttribute**</span><span class="sxs-lookup"><span data-stu-id="148d4-145">**WsFindAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [<span data-ttu-id="148d4-146">**WsFreeReader**</span><span class="sxs-lookup"><span data-stu-id="148d4-146">**WsFreeReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [<span data-ttu-id="148d4-147">**WsGetNamespaceFromPrefix**</span><span class="sxs-lookup"><span data-stu-id="148d4-147">**WsGetNamespaceFromPrefix**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [<span data-ttu-id="148d4-148">**WsGetReaderNode**</span><span class="sxs-lookup"><span data-stu-id="148d4-148">**WsGetReaderNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [<span data-ttu-id="148d4-149">**WsGetReaderPosition**</span><span class="sxs-lookup"><span data-stu-id="148d4-149">**WsGetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [<span data-ttu-id="148d4-150">**WsGetReaderProperty**</span><span class="sxs-lookup"><span data-stu-id="148d4-150">**WsGetReaderProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [<span data-ttu-id="148d4-151">**WsGetXmlAttribute**</span><span class="sxs-lookup"><span data-stu-id="148d4-151">**WsGetXmlAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [<span data-ttu-id="148d4-152">**WsMoveReader**</span><span class="sxs-lookup"><span data-stu-id="148d4-152">**WsMoveReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [<span data-ttu-id="148d4-153">**WsReadArray**</span><span class="sxs-lookup"><span data-stu-id="148d4-153">**WsReadArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [<span data-ttu-id="148d4-154">**WsReadBytes**</span><span class="sxs-lookup"><span data-stu-id="148d4-154">**WsReadBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [<span data-ttu-id="148d4-155">**WsReadChars**</span><span class="sxs-lookup"><span data-stu-id="148d4-155">**WsReadChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [<span data-ttu-id="148d4-156">**WsReadCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="148d4-156">**WsReadCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [<span data-ttu-id="148d4-157">**WsReadEndAttribute**</span><span class="sxs-lookup"><span data-stu-id="148d4-157">**WsReadEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [<span data-ttu-id="148d4-158">**WsReadEndElement**</span><span class="sxs-lookup"><span data-stu-id="148d4-158">**WsReadEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [<span data-ttu-id="148d4-159">**WsReadNode**</span><span class="sxs-lookup"><span data-stu-id="148d4-159">**WsReadNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [<span data-ttu-id="148d4-160">**WsReadQualifiedName**</span><span class="sxs-lookup"><span data-stu-id="148d4-160">**WsReadQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [<span data-ttu-id="148d4-161">**WsReadStartAttribute**</span><span class="sxs-lookup"><span data-stu-id="148d4-161">**WsReadStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [<span data-ttu-id="148d4-162">**WsReadStartElement**</span><span class="sxs-lookup"><span data-stu-id="148d4-162">**WsReadStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [<span data-ttu-id="148d4-163">**WsReadToStartElement**</span><span class="sxs-lookup"><span data-stu-id="148d4-163">**WsReadToStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [<span data-ttu-id="148d4-164">**WsReadValue**</span><span class="sxs-lookup"><span data-stu-id="148d4-164">**WsReadValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [<span data-ttu-id="148d4-165">**WsSetInput**</span><span class="sxs-lookup"><span data-stu-id="148d4-165">**WsSetInput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [<span data-ttu-id="148d4-166">**WsSetInputToBuffer**</span><span class="sxs-lookup"><span data-stu-id="148d4-166">**WsSetInputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [<span data-ttu-id="148d4-167">**WsSetReaderPosition**</span><span class="sxs-lookup"><span data-stu-id="148d4-167">**WsSetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [<span data-ttu-id="148d4-168">**WsSkipNode**</span><span class="sxs-lookup"><span data-stu-id="148d4-168">**WsSkipNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

<span data-ttu-id="148d4-169">O seguinte identificador é usado com leitores XML:</span><span class="sxs-lookup"><span data-stu-id="148d4-169">The following handle is used with XML readers:</span></span>

-   [<span data-ttu-id="148d4-170">\_leitor de XML do WS \_</span><span class="sxs-lookup"><span data-stu-id="148d4-170">WS\_XML\_READER</span></span>](ws-xml-reader.md)

<span data-ttu-id="148d4-171">As seguintes estruturas são usadas com leitores XML:</span><span class="sxs-lookup"><span data-stu-id="148d4-171">The following structures are used with XML readers:</span></span>

-   [<span data-ttu-id="148d4-172">**\_ \_ codificação binária de leitor XML \_ do \_ WS**</span><span class="sxs-lookup"><span data-stu-id="148d4-172">**WS\_XML\_READER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [<span data-ttu-id="148d4-173">**\_entrada de \_ buffer de leitor de XML WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="148d4-173">**WS\_XML\_READER\_BUFFER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="148d4-174">**\_codificação de \_ leitor \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="148d4-174">**WS\_XML\_READER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [<span data-ttu-id="148d4-175">**\_entrada do \_ leitor de XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="148d4-175">**WS\_XML\_READER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [<span data-ttu-id="148d4-176">**\_codificação de \_ MTOM do leitor XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="148d4-176">**WS\_XML\_READER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [<span data-ttu-id="148d4-177">**\_Propriedades do \_ leitor \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="148d4-177">**WS\_XML\_READER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [<span data-ttu-id="148d4-178">**\_ \_ Propriedade leitor de XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="148d4-178">**WS\_XML\_READER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [<span data-ttu-id="148d4-179">**\_entrada de \_ fluxo de leitor XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="148d4-179">**WS\_XML\_READER\_STREAM\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [<span data-ttu-id="148d4-180">**\_codificação de \_ texto do leitor XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="148d4-180">**WS\_XML\_READER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 





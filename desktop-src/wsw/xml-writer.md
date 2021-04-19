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
# <a name="xml-writer"></a><span data-ttu-id="f5922-107">Gravador de XML</span><span class="sxs-lookup"><span data-stu-id="f5922-107">XML Writer</span></span>

<span data-ttu-id="f5922-108">O gravador de XML é uma API para emitir XML.</span><span class="sxs-lookup"><span data-stu-id="f5922-108">XML Writer is an API for emitting XML.</span></span> <span data-ttu-id="f5922-109">Essencialmente, um gravador de XML grava um [nó XML](xml-node.md) por vez, mas há APIs auxiliares adicionais para facilitar a gravação de uma seqüência de nós.</span><span class="sxs-lookup"><span data-stu-id="f5922-109">At its core, an XML Writer writes one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make writing a sequence of nodes easier.</span></span>


<span data-ttu-id="f5922-110">Há suporte para os seguintes tipos de saída do gravador:</span><span class="sxs-lookup"><span data-stu-id="f5922-110">The following types of writer output are supported:</span></span>

-   [<span data-ttu-id="f5922-111">**Um buffer na memória de bytes codificados**</span><span class="sxs-lookup"><span data-stu-id="f5922-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="f5922-112">**Um fluxo**</span><span class="sxs-lookup"><span data-stu-id="f5922-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   <span data-ttu-id="f5922-113">Um [buffer XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="f5922-113">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="f5922-114">Os seguintes retornos de chamada são usados com o gravador de XML:</span><span class="sxs-lookup"><span data-stu-id="f5922-114">The following callbacks are used with the XML writer:</span></span>

-   [<span data-ttu-id="f5922-115">**\_retorno de \_ chamada de cadeia de caracteres dinâmica WS \_**</span><span class="sxs-lookup"><span data-stu-id="f5922-115">**WS\_DYNAMIC\_STRING\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [<span data-ttu-id="f5922-116">**\_retorno de \_ chamada de bytes WS pull \_**</span><span class="sxs-lookup"><span data-stu-id="f5922-116">**WS\_PULL\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [<span data-ttu-id="f5922-117">**\_retorno de \_ chamada de bytes do WS Push \_**</span><span class="sxs-lookup"><span data-stu-id="f5922-117">**WS\_PUSH\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [<span data-ttu-id="f5922-118">**\_retorno de \_ chamada WS Write**</span><span class="sxs-lookup"><span data-stu-id="f5922-118">**WS\_WRITE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

<span data-ttu-id="f5922-119">As seguintes enumerações são usadas com o gravador de XML:</span><span class="sxs-lookup"><span data-stu-id="f5922-119">The following enumerations are used with the XML writer:</span></span>

-   [<span data-ttu-id="f5922-120">**conjunto de \_ caracteres WS**</span><span class="sxs-lookup"><span data-stu-id="f5922-120">**WS\_CHARSET**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [<span data-ttu-id="f5922-121">**\_tipo de \_ codificação de gravador \_ \_ do WS XML**</span><span class="sxs-lookup"><span data-stu-id="f5922-121">**WS\_XML\_WRITER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="f5922-122">**\_tipo de \_ saída do gravador \_ \_ do WS XML**</span><span class="sxs-lookup"><span data-stu-id="f5922-122">**WS\_XML\_WRITER\_OUTPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [<span data-ttu-id="f5922-123">**\_ID da \_ Propriedade do gravador XML \_ do WS \_**</span><span class="sxs-lookup"><span data-stu-id="f5922-123">**WS\_XML\_WRITER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

<span data-ttu-id="f5922-124">As funções a seguir são usadas com o gravador de XML:</span><span class="sxs-lookup"><span data-stu-id="f5922-124">The following functions are used with the XML writer:</span></span>

-   [<span data-ttu-id="f5922-125">**WsCopyNode**</span><span class="sxs-lookup"><span data-stu-id="f5922-125">**WsCopyNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [<span data-ttu-id="f5922-126">**WsCreateWriter**</span><span class="sxs-lookup"><span data-stu-id="f5922-126">**WsCreateWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [<span data-ttu-id="f5922-127">**WsFlushWriter**</span><span class="sxs-lookup"><span data-stu-id="f5922-127">**WsFlushWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [<span data-ttu-id="f5922-128">**WsFreeWriter**</span><span class="sxs-lookup"><span data-stu-id="f5922-128">**WsFreeWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [<span data-ttu-id="f5922-129">**WsGetPrefixFromNamespace**</span><span class="sxs-lookup"><span data-stu-id="f5922-129">**WsGetPrefixFromNamespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [<span data-ttu-id="f5922-130">**WsGetWriterPosition**</span><span class="sxs-lookup"><span data-stu-id="f5922-130">**WsGetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [<span data-ttu-id="f5922-131">**WsGetWriterProperty**</span><span class="sxs-lookup"><span data-stu-id="f5922-131">**WsGetWriterProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [<span data-ttu-id="f5922-132">**WsMoveWriter**</span><span class="sxs-lookup"><span data-stu-id="f5922-132">**WsMoveWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [<span data-ttu-id="f5922-133">**WsPullBytes**</span><span class="sxs-lookup"><span data-stu-id="f5922-133">**WsPullBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [<span data-ttu-id="f5922-134">**WsPushBytes**</span><span class="sxs-lookup"><span data-stu-id="f5922-134">**WsPushBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [<span data-ttu-id="f5922-135">**WsSetOutput**</span><span class="sxs-lookup"><span data-stu-id="f5922-135">**WsSetOutput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [<span data-ttu-id="f5922-136">**WsSetOutputToBuffer**</span><span class="sxs-lookup"><span data-stu-id="f5922-136">**WsSetOutputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [<span data-ttu-id="f5922-137">**WsSetWriterPosition**</span><span class="sxs-lookup"><span data-stu-id="f5922-137">**WsSetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [<span data-ttu-id="f5922-138">**WsWriteArray**</span><span class="sxs-lookup"><span data-stu-id="f5922-138">**WsWriteArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [<span data-ttu-id="f5922-139">**WsWriteBytes**</span><span class="sxs-lookup"><span data-stu-id="f5922-139">**WsWriteBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [<span data-ttu-id="f5922-140">**WsWriteChars**</span><span class="sxs-lookup"><span data-stu-id="f5922-140">**WsWriteChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [<span data-ttu-id="f5922-141">**WsWriteCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="f5922-141">**WsWriteCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [<span data-ttu-id="f5922-142">**WsWriteEndAttribute**</span><span class="sxs-lookup"><span data-stu-id="f5922-142">**WsWriteEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [<span data-ttu-id="f5922-143">**WsWriteEndCData**</span><span class="sxs-lookup"><span data-stu-id="f5922-143">**WsWriteEndCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [<span data-ttu-id="f5922-144">**WsWriteEndElement**</span><span class="sxs-lookup"><span data-stu-id="f5922-144">**WsWriteEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [<span data-ttu-id="f5922-145">**WsWriteNode**</span><span class="sxs-lookup"><span data-stu-id="f5922-145">**WsWriteNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [<span data-ttu-id="f5922-146">**WsWriteQualifiedName**</span><span class="sxs-lookup"><span data-stu-id="f5922-146">**WsWriteQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [<span data-ttu-id="f5922-147">**WsWriteStartAttribute**</span><span class="sxs-lookup"><span data-stu-id="f5922-147">**WsWriteStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [<span data-ttu-id="f5922-148">**WsWriteStartCData**</span><span class="sxs-lookup"><span data-stu-id="f5922-148">**WsWriteStartCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [<span data-ttu-id="f5922-149">**WsWriteStartElement**</span><span class="sxs-lookup"><span data-stu-id="f5922-149">**WsWriteStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [<span data-ttu-id="f5922-150">**WsWriteText**</span><span class="sxs-lookup"><span data-stu-id="f5922-150">**WsWriteText**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [<span data-ttu-id="f5922-151">**WsWriteValue**</span><span class="sxs-lookup"><span data-stu-id="f5922-151">**WsWriteValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [<span data-ttu-id="f5922-152">**WsWriteXmlnsAttribute**</span><span class="sxs-lookup"><span data-stu-id="f5922-152">**WsWriteXmlnsAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

<span data-ttu-id="f5922-153">O identificador a seguir é usado com o gravador de XML:</span><span class="sxs-lookup"><span data-stu-id="f5922-153">The following handle is used with the XML writer:</span></span>

-   [<span data-ttu-id="f5922-154">gravador do WS \_ XML \_</span><span class="sxs-lookup"><span data-stu-id="f5922-154">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)

<span data-ttu-id="f5922-155">As seguintes estruturas são usadas com o gravador de XML:</span><span class="sxs-lookup"><span data-stu-id="f5922-155">The following structures are used with the XML writer:</span></span>

-   [<span data-ttu-id="f5922-156">**\_ \_ \_ codificação binária de gravador \_ do WS XML**</span><span class="sxs-lookup"><span data-stu-id="f5922-156">**WS\_XML\_WRITER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [<span data-ttu-id="f5922-157">**\_saída do \_ buffer do gravador \_ \_ do WS XML**</span><span class="sxs-lookup"><span data-stu-id="f5922-157">**WS\_XML\_WRITER\_BUFFER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="f5922-158">**\_codificação de \_ gravador de XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="f5922-158">**WS\_XML\_WRITER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [<span data-ttu-id="f5922-159">**\_codificação de \_ MTOM do gravador de XML do WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f5922-159">**WS\_XML\_WRITER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [<span data-ttu-id="f5922-160">**\_saída do \_ gravador de XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="f5922-160">**WS\_XML\_WRITER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [<span data-ttu-id="f5922-161">**\_Propriedades do \_ gravador \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="f5922-161">**WS\_XML\_WRITER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [<span data-ttu-id="f5922-162">**\_Propriedade do \_ gravador de XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="f5922-162">**WS\_XML\_WRITER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [<span data-ttu-id="f5922-163">**\_saída de \_ fluxo do gravador XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="f5922-163">**WS\_XML\_WRITER\_STREAM\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [<span data-ttu-id="f5922-164">**\_codificação de \_ texto de gravador \_ \_ do WS XML**</span><span class="sxs-lookup"><span data-stu-id="f5922-164">**WS\_XML\_WRITER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 





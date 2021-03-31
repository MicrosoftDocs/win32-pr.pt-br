---
title: Visão geral da camada XML
description: A API XML no WWSAPI é baseada nos objetos leitor de XML e gravador XML, que permitem a leitura ou gravação de documentos XML em uma forma somente para frente. A camada XML concede ao aplicativo acesso completo e controle sobre o conteúdo das mensagens.
ms.assetid: 938ca257-fbb8-4569-b791-2148abb1a5a5
keywords:
- Serviços Web de visão geral da camada XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b5d062754adea7b48bd42a6a501ce17d0e332b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635971"
---
# <a name="xml-layer-overview"></a><span data-ttu-id="f0f0a-107">Visão geral da camada XML</span><span class="sxs-lookup"><span data-stu-id="f0f0a-107">XML Layer Overview</span></span>

<span data-ttu-id="f0f0a-108">A API XML no WWSAPI é baseada nos objetos [leitor de XML](xml-reader.md) e [gravador XML](xml-writer.md) , que permitem a leitura ou gravação de documentos XML em uma forma somente para frente.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-108">The XML API in WWSAPI is based on the [XML Reader](xml-reader.md) and [XML Writer](xml-writer.md) objects, which allow reading or writing of XML documents in a forward only fashion.</span></span> <span data-ttu-id="f0f0a-109">A camada XML concede ao aplicativo acesso completo e controle sobre o conteúdo das mensagens.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-109">The XML Layer give the application full access to and control over the content of messages.</span></span>

## <a name="encoding"></a><span data-ttu-id="f0f0a-110">Codificação</span><span class="sxs-lookup"><span data-stu-id="f0f0a-110">Encoding</span></span>

<span data-ttu-id="f0f0a-111">A API XML dá suporte a documentos codificados como:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-111">The XML API supports documents encoded as:</span></span>

-   <span data-ttu-id="f0f0a-112">Text (UTF-8, UTF-16LE, UTF-16BE)</span><span class="sxs-lookup"><span data-stu-id="f0f0a-112">Text (UTF-8, UTF-16LE, UTF-16BE)</span></span>
-   <span data-ttu-id="f0f0a-113">Binário</span><span class="sxs-lookup"><span data-stu-id="f0f0a-113">Binary</span></span>
-   <span data-ttu-id="f0f0a-114">MTOM</span><span class="sxs-lookup"><span data-stu-id="f0f0a-114">MTOM</span></span>

## <a name="storage"></a><span data-ttu-id="f0f0a-115">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="f0f0a-115">Storage</span></span>

<span data-ttu-id="f0f0a-116">A API XML dá suporte ao processamento de documentos armazenados como:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-116">The XML API supports processing documents stored as:</span></span>

-   <span data-ttu-id="f0f0a-117">Um buffer na memória de bytes codificados</span><span class="sxs-lookup"><span data-stu-id="f0f0a-117">An in-memory buffer of encoded bytes</span></span>
-   <span data-ttu-id="f0f0a-118">Um fluxo</span><span class="sxs-lookup"><span data-stu-id="f0f0a-118">A stream</span></span>
-   <span data-ttu-id="f0f0a-119">Um [buffer XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="f0f0a-119">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="f0f0a-120">Um [buffer XML](xml-buffer.md) é uma representação estruturada na memória de um documento XML.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-120">An [XML Buffer](xml-buffer.md) is a structured in-memory representation of an XML document.</span></span> <span data-ttu-id="f0f0a-121">Essa é uma representação mais eficiente do que um documento codificado como bytes.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-121">This is a more efficient representation than a document encoded as bytes.</span></span> <span data-ttu-id="f0f0a-122">Um documento XML armazenado em um buffer XML pode ser navegado, lido ou gravado.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-122">An XML document stored in an An XML Buffer can be navigated, read, or written.</span></span>

## <a name="io"></a><span data-ttu-id="f0f0a-123">E/S</span><span class="sxs-lookup"><span data-stu-id="f0f0a-123">I/O</span></span>

<span data-ttu-id="f0f0a-124">A API XML nunca executará a e/s, a menos que solicitado especificamente.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-124">The XML API will never perform I/O unless specifically requested.</span></span> <span data-ttu-id="f0f0a-125">Além disso, qualquer e/s pode ser iniciada de maneira assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-125">Furthermore, any I/O may be initiated in an asynchronous fashion.</span></span> <span data-ttu-id="f0f0a-126">Consulte [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) e [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) para obter detalhes sobre o processamento assíncrono com a API XML.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-126">See [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) and [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) for details on asynchronous processing with the XML API.</span></span>

## <a name="processing"></a><span data-ttu-id="f0f0a-127">Processing</span><span class="sxs-lookup"><span data-stu-id="f0f0a-127">Processing</span></span>

<span data-ttu-id="f0f0a-128">A API XML tem três níveis distintos nos quais o documento pode ser processado.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-128">The XML API has three distinct levels at which the document may be processed.</span></span>

<span data-ttu-id="f0f0a-129">Um documento pode ser processado em um [**nó**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) por vez.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-129">A document may be processed a [**node**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) at a time.</span></span> <span data-ttu-id="f0f0a-130">Isso oferece a manipulação mais refinada do conteúdo XML e fornece fidelidade completa dos dados do documento.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-130">This offers the most fine-grained handling of the XML content, and provides complete fidelity of data from the document.</span></span> <span data-ttu-id="f0f0a-131">Nesse nível, as funções [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) e [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) e [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) seriam usadas.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-131">At this level, the functions [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) and [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) and [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) would be used.</span></span>

<span data-ttu-id="f0f0a-132">O próximo nível de controle são APIs como [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) e [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span><span class="sxs-lookup"><span data-stu-id="f0f0a-132">The next level of control are APIs like [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) and [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span></span> <span data-ttu-id="f0f0a-133">Essas APIs fornecem vários tipos de validação, ignoram espaços em branco e comentários e normalizam o texto e CDATA para apresentar ao consumidor uma visão mais simples do XML.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-133">These APIs provide numerous kinds of validation, skip whitespace and comments, and normalize text and CDATA to present the consumer with a simpler view of the xml.</span></span>

<span data-ttu-id="f0f0a-134">O nível mais alto de controle é usar a API de serialização.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-134">The highest level of control is to use the Serialization API.</span></span> <span data-ttu-id="f0f0a-135">Essas APIs são acionadas por um mapeamento entre tipos de dados C e XML e podem ler ou gravar uma estrutura complexa na memória em XML e voltar com uma única função como [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) e [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span><span class="sxs-lookup"><span data-stu-id="f0f0a-135">These APIs are driven off a mapping between C data types and XML, and can read or write a complex in-memory structure to xml and back with a single function like [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) and [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span></span>

<span data-ttu-id="f0f0a-136">As APIs de canonização XML podem ser usadas para gerar uma forma canônica de XML que, por sua vez, pode ser usada para gerar assinaturas criptográficas em conteúdo XML.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-136">The XML Canonicalization APIs may be used to generate a canonical form of XML which may in turn be used for generating cryptographic signatures over XML content.</span></span>

## <a name="creating-a-writer"></a><span data-ttu-id="f0f0a-137">Criando um gravador</span><span class="sxs-lookup"><span data-stu-id="f0f0a-137">Creating a writer</span></span>

<span data-ttu-id="f0f0a-138">Para criar e usar um gravador para gravar em um buffer na memória:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-138">To create and use a writer to write to an in-memory buffer:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_BUFFER_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsGetWriterProperty(..., WS_XML_WRITER_PROPERTY_BYTES, ...)  // Get the generated bytes as a single byte array
// Use the generated bytes
WsFreeWriter                // Free the writer
```

<span data-ttu-id="f0f0a-139">Para criar e usar um gravador para gravar em um fluxo:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-139">To create and use a writer to write to a stream:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_STREAM_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsFlushWriter               // Force any buffered data to be written
WsFreeWriter                // Free the writer
```

<span data-ttu-id="f0f0a-140">Para criar e usar um gravador para gravar em um [ \_ \_ buffer XML do WS](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="f0f0a-140">To create and use a writer to write to a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateWriter              // Create an instance of a WS_XML_WRITER
WsSetOutputToBuffer         // Set the output buffer along with any other writer properties
// Write Elements
WsFreeWriter                // Free the writer
// The buffer has the generated document
```

<span data-ttu-id="f0f0a-141">Em todos os casos, o [**recuo da propriedade WS \_ XML \_ Writer \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) da propriedade pode ser incluído para formatar o XML.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-141">In all cases, the property [**WS\_XML\_WRITER\_PROPERTY\_INDENT**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) may be included to format the xml.</span></span>

## <a name="writing-elements"></a><span data-ttu-id="f0f0a-142">Elementos de gravação</span><span class="sxs-lookup"><span data-stu-id="f0f0a-142">Writing Elements</span></span>

<span data-ttu-id="f0f0a-143">Para gravar um elemento em um gravador:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-143">To write an element to a writer:</span></span>

``` syntax
WsWriteStartElement          // Write a start element
for each attribute
{
// Write an attribute using either
WsWriteStartAttribute    // Write a start attribute
// Write Content
WsWriteEndAttribute      // Write an end attribute
// Or one of the following
WsWriteXmlnsAttribute    // Write an explicit xmlns attribute
}
// Write Elements or Content
WsWriteEndElement
```

<span data-ttu-id="f0f0a-144">O seguinte também pode ser usado:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-144">The following may also be used:</span></span>

``` syntax
WsWriteArray                 // Write an array of primitive values as a series of repeated elements
```

## <a name="writing-content"></a><span data-ttu-id="f0f0a-145">Gravando conteúdo</span><span class="sxs-lookup"><span data-stu-id="f0f0a-145">Writing Content</span></span>

<span data-ttu-id="f0f0a-146">Para gravar o conteúdo em um elemento ou atributo, o seguinte pode ser usado:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-146">To write content to an element or attribute, the following may be used:</span></span>

``` syntax
WsWriteChars                 // Write unicode characters from memory
WsWriteCharsUtf8             // Write UTF-8 encoded characters from memory
WsWriteBytes                 // Write binary data encoded as base64
WsPushBytes                  // Direct the writer to request that bytes be written
WsPullBytes                  // Direct the writer to read the bytes to be written
WsWriteValue                 // Write primitive values such as ints and BOOLs
WsWriteText                  // Write an WS_XML_TEXT
WsWriteQualifiedName         // Write a qualified name
```

<span data-ttu-id="f0f0a-147">O seguinte pode ser usado para gravar em um documento, mas não pode ser usado quando estiver dentro de um atributo.</span><span class="sxs-lookup"><span data-stu-id="f0f0a-147">The following can be used to write to a document, but may not be used when within an attribute.</span></span>

``` syntax
WsWriteNode                  // Write a single WS_XML_NODE
WsCopyNode                   // Copy a single node, or an entire WS_XML_ELEMENT_NODE and children from an WS_XML_READER
```

<span data-ttu-id="f0f0a-148">O seguinte pode ser usado para escrever uma seção CDATA em um documento de texto:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-148">The following may be used to write a CDATA section in a text document:</span></span>

``` syntax
WsWriteStartCData            // Start a CDATA section in a text encoding
// Write Content
WsWriteEndCData              // End a CDATA section in text encoding
```

## <a name="miscellaneous"></a><span data-ttu-id="f0f0a-149">Diversos</span><span class="sxs-lookup"><span data-stu-id="f0f0a-149">Miscellaneous</span></span>

``` syntax
WsGetPrefixFromNamespace     // Find a prefix bound to a namespace
```

## <a name="creating-a-reader"></a><span data-ttu-id="f0f0a-150">Criando um leitor</span><span class="sxs-lookup"><span data-stu-id="f0f0a-150">Creating a reader</span></span>

<span data-ttu-id="f0f0a-151">Para criar e usar um leitor para ler de um buffer na memória:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-151">To create and use a reader to read from an in-memory buffer:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="f0f0a-152">Para criar e usar um leitor para leitor de um fluxo:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-152">To create and use a reader to reader from a stream:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_STREAM_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
WsFillReader                // Populate the reader with data from the underlying stream
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="f0f0a-153">Para criar e usar um leitor para ler de um [ \_ \_ buffer XML WS](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="f0f0a-153">To create and use a reader to read from a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateReader              // Create an instance of a WS_XML_READER
WsSetInputToBuffer          // Set the input buffer along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

## <a name="reading-elements"></a><span data-ttu-id="f0f0a-154">Lendo elementos</span><span class="sxs-lookup"><span data-stu-id="f0f0a-154">Reading Elements</span></span>

<span data-ttu-id="f0f0a-155">Para ler um elemento de um leitor:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-155">To read an element from a reader:</span></span>

``` syntax
WsReadToStartElement         // Skip whitespace and comments to position the reader on a specific element
for each attribute of interest
{
WsFindAttribute          // Try Locate the attribute
if (found)
{
WsReadStartAttribute // Set the reader to read the attribute
// Read Content
WsReadEndAttribute   // Return the reader to the element
}
}
WsReadStartElement           // Advance the reader past the current element
// Read Elements or Content
WsWriteEndElement            // Advance the reader past the corresponding end element
```

<span data-ttu-id="f0f0a-156">O seguinte também pode ser usado:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-156">The following may also be used:</span></span>

``` syntax
WsReadArray                  // Read an array of primitive values as a series of repeated elements
```

## <a name="reading-content"></a><span data-ttu-id="f0f0a-157">Lendo o conteúdo</span><span class="sxs-lookup"><span data-stu-id="f0f0a-157">Reading Content</span></span>

<span data-ttu-id="f0f0a-158">Para ler o conteúdo de um elemento ou atributo, o seguinte pode ser usado:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-158">To read content from an element or attribute, the following may be used:</span></span>

``` syntax
WsReadChars                 // Read characters to memory as unicode
WsReadCharsUtf8             // Read characters to memory encoded as UTF-8
WsReadBytes                 // Read binary data encoded as base64
WsReadValue                 // Read primitive values such as ints and BOOLs
WsReadQualifiedName         // Read a qualified name
```

<span data-ttu-id="f0f0a-159">O seguinte pode ser usado para inspecionar o nó atual no qual o leitor está posicionado:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-159">The following may be used to inspect the current node the reader is positioned on:</span></span>

``` syntax
WsGetReaderNode             // Get the current node
```

## <a name="using-a-buffer"></a><span data-ttu-id="f0f0a-160">Usando um buffer</span><span class="sxs-lookup"><span data-stu-id="f0f0a-160">Using a buffer</span></span>

<span data-ttu-id="f0f0a-161">Ao gravar em um [ \_ \_ buffer XML do WS](ws-xml-buffer.md) , o seguinte pode ser usado:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-161">When writing to a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetWriterPosition          // Get the current position of the writer in the document
WsSetWriterPosition          // Set the current position of the writer in the document
WsMoveWriter                 // Move relative to the current position in the document
WsRemoveNode                 // Delete an element or text from a document
```

<span data-ttu-id="f0f0a-162">Ao ler de um [ \_ \_ buffer XML do WS](ws-xml-buffer.md) , o seguinte pode ser usado:</span><span class="sxs-lookup"><span data-stu-id="f0f0a-162">When reading from a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetReaderPosition          // Get the current position of the reader in the document
WsSetReaderPosition          // Set the current position of the reader in the document
WsMoveReader                 // Move relative to the current position in the document
```

<span data-ttu-id="f0f0a-163">O seguinte pode ser usado para modificar um [ \_ \_ buffer XML do WS](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="f0f0a-163">The following may be used to modify a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax

WsRemoveNode                 // Delete an element or text from a document
```

## <a name="other"></a><span data-ttu-id="f0f0a-164">Outros</span><span class="sxs-lookup"><span data-stu-id="f0f0a-164">Other</span></span>

``` syntax
WsGetNamespaceFromPrefix     // Find a namespace bound to a prefix
WsGetXmlAttribute            // Find an "xml:space" or "xml:lang" attribute in scope
```

 

 





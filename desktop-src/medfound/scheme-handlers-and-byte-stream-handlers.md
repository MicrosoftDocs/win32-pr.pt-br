---
description: Este tópico descreve os detalhes internos de como o resolvedor de origem cria uma origem de mídia.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Manipuladores de esquema e manipuladores de Byte-Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54976f45c7f07e12b6f095297231d306d0644704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812382"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a><span data-ttu-id="68fc5-103">Manipuladores de esquema e manipuladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="68fc5-103">Scheme Handlers and Byte-Stream Handlers</span></span>

<span data-ttu-id="68fc5-104">Este tópico descreve os detalhes internos de como o resolvedor de origem cria uma origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="68fc5-104">This topic describes the internal details of how the source resolver creates a media source.</span></span> <span data-ttu-id="68fc5-105">Leia este tópico se você estiver implementando uma fonte de mídia personalizada para Media Foundation e desejar que a fonte de mídia esteja disponível para aplicativos por meio do resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="68fc5-105">Read this topic if you are implementing a custom media source for Media Foundation, and you want the media source to be available to applications via the source resolver.</span></span>

<span data-ttu-id="68fc5-106">O resolvedor de origem pode criar uma fonte de mídia de uma URL ou de um fluxo de bytes (ou seja, um ponteiro [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) ).</span><span class="sxs-lookup"><span data-stu-id="68fc5-106">The source resolver can create a media source from a URL or from a byte stream (that is, an [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) pointer).</span></span> <span data-ttu-id="68fc5-107">Para fazer isso, ele usa objetos auxiliares chamados de *manipuladores*.</span><span class="sxs-lookup"><span data-stu-id="68fc5-107">To do so, it uses helper objects called *handlers*.</span></span> <span data-ttu-id="68fc5-108">Para URLs, o resolvedor de origem usa *manipuladores de esquema*.</span><span class="sxs-lookup"><span data-stu-id="68fc5-108">For URLs, the source resolver uses *scheme handlers*.</span></span> <span data-ttu-id="68fc5-109">Para fluxos de bytes, ele usa *manipuladores de fluxo de bytes*.</span><span class="sxs-lookup"><span data-stu-id="68fc5-109">For byte streams, it uses *byte-stream handlers*.</span></span>

<span data-ttu-id="68fc5-110">Um manipulador de esquema usa uma URL como entrada e cria uma origem de mídia ou um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="68fc5-110">A scheme handler takes a URL as input and creates either a media source or a byte stream.</span></span> <span data-ttu-id="68fc5-111">Se ele criar um fluxo de bytes, o resolvedor de origem irá passá-lo para um manipulador de fluxo de bytes, que cria a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="68fc5-111">If it creates a byte stream, the source resolver will pass that to a byte-stream handler, which creates the media source.</span></span> <span data-ttu-id="68fc5-112">A imagem a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="68fc5-112">The following image illustrates this process.</span></span>

![diagrama mostrando o processo de resolução de origem](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a><span data-ttu-id="68fc5-114">Manipuladores de esquema</span><span class="sxs-lookup"><span data-stu-id="68fc5-114">Scheme Handlers</span></span>

<span data-ttu-id="68fc5-115">Os manipuladores de esquema são usados quando o aplicativo chama [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) ou seu equivalente assíncrono, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="68fc5-115">Scheme handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) or its asynchronous equivalent, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

<span data-ttu-id="68fc5-116">O resolvedor de origem pesquisa manipuladores de esquema no registro.</span><span class="sxs-lookup"><span data-stu-id="68fc5-116">The source resolver looks up scheme handlers in the registry.</span></span> <span data-ttu-id="68fc5-117">Os manipuladores de esquema são listados por esquema de URL, sob as seguintes chaves:</span><span class="sxs-lookup"><span data-stu-id="68fc5-117">Scheme handlers are listed by URL scheme, under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="68fc5-118">em que *<scheme>* é o esquema de URL que o manipulador foi projetado para analisar.</span><span class="sxs-lookup"><span data-stu-id="68fc5-118">where *<scheme>* is the URL scheme that the handler is designed to parse.</span></span> <span data-ttu-id="68fc5-119">O esquema inclui o caractere ': ' à direita; por exemplo, "http:".</span><span class="sxs-lookup"><span data-stu-id="68fc5-119">The scheme includes the trailing ':' character; for example, "http:".</span></span>

<span data-ttu-id="68fc5-120">Para registrar um novo manipulador de esquema, adicione uma entrada cujo nome seja o CLSID do manipulador de esquema, em formato de cadeia de caracteres canônica: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="68fc5-120">To register a new scheme handler, add an entry whose name is the CLSID of the scheme handler, in canonical string form: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="68fc5-121">O valor da entrada é uma cadeia de caracteres (REG \_ SZ) que contém uma breve descrição do manipulador, como "meu manipulador de esquema".</span><span class="sxs-lookup"><span data-stu-id="68fc5-121">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Scheme Handler."</span></span> <span data-ttu-id="68fc5-122">A parte importante da entrada é o CLSID.</span><span class="sxs-lookup"><span data-stu-id="68fc5-122">The important part of the entry is the CLSID.</span></span> <span data-ttu-id="68fc5-123">O resolvedor de origem cria o manipulador chamando **CoCreateInstance** com esse CLSID.</span><span class="sxs-lookup"><span data-stu-id="68fc5-123">The source resolver creates the handler by calling **CoCreateInstance** with this CLSID.</span></span>

<span data-ttu-id="68fc5-124">Os manipuladores de esquema expõem a interface [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) .</span><span class="sxs-lookup"><span data-stu-id="68fc5-124">Scheme handlers expose the [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) interface.</span></span> <span data-ttu-id="68fc5-125">Se o resolvedor de origem encontrar um manipulador de esquema que corresponda ao esquema de URL, o resolvedor de origem chamará [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passando a URL original.</span><span class="sxs-lookup"><span data-stu-id="68fc5-125">If the source resolver finds a scheme handler that matches the URL scheme, the source resolver calls [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passing in the original URL.</span></span> <span data-ttu-id="68fc5-126">O manipulador de esquema abrirá a URL e tentará analisar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="68fc5-126">The scheme handler will open the URL and attempt to parse the contents.</span></span> <span data-ttu-id="68fc5-127">Nesse ponto, o manipulador de esquema tem duas opções:</span><span class="sxs-lookup"><span data-stu-id="68fc5-127">At that point, the scheme handler has two options:</span></span>

-   <span data-ttu-id="68fc5-128">Crie uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="68fc5-128">Create a media source.</span></span>
-   <span data-ttu-id="68fc5-129">Crie um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="68fc5-129">Create a byte stream.</span></span>

<span data-ttu-id="68fc5-130">Se ele criar uma origem de mídia, o resolvedor de origem retornará a origem de mídia para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68fc5-130">If it creates a media source, the source resolver returns the media source to the application.</span></span> <span data-ttu-id="68fc5-131">Se ele criar um fluxo de bytes, o resolvedor de origem tentará localizar um manipulador de fluxo de bytes apropriado, conforme descrito na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="68fc5-131">If it creates a byte stream, the source resolver attempts to find an appropriate byte-stream handler, as described in the next section.</span></span>

## <a name="byte-stream-handlers"></a><span data-ttu-id="68fc5-132">Manipuladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="68fc5-132">Byte-Stream Handlers</span></span>

<span data-ttu-id="68fc5-133">Os manipuladores de fluxo de bytes são usados quando o aplicativo chama [**IMFSourceResolver:: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) ou seu equivalente assíncrono, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span><span class="sxs-lookup"><span data-stu-id="68fc5-133">Byte-stream handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) or its asynchronous equivalent, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span></span> <span data-ttu-id="68fc5-134">Eles também são usados quando um manipulador de esquema retorna um fluxo de bytes, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="68fc5-134">They are also used when a scheme handler returns a byte stream, as described previously.</span></span>

<span data-ttu-id="68fc5-135">Assim como os manipuladores de esquema, os manipuladores de fluxo de bytes são listados no registro.</span><span class="sxs-lookup"><span data-stu-id="68fc5-135">As with scheme handlers, byte-stream handlers are listed in the registry.</span></span> <span data-ttu-id="68fc5-136">Eles são listados por extensão de nome de arquivo ou tipo MIME (ou ambos), sob as seguintes chaves:</span><span class="sxs-lookup"><span data-stu-id="68fc5-136">They are listed either by file name extension or MIME type (or both), under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="68fc5-137">em que *<ExtensionOrMimeType>* é a extensão de nome de arquivo ou o tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="68fc5-137">where *<ExtensionOrMimeType>* is the file name extension or MIME type.</span></span> <span data-ttu-id="68fc5-138">As extensões de arquivo incluem o caractere '. ' inicial; por exemplo, ". wmv".</span><span class="sxs-lookup"><span data-stu-id="68fc5-138">File extensions include the initial '.' character; for example, ".wmv".</span></span>

<span data-ttu-id="68fc5-139">A extensão de nome de arquivo faz parte da URL, fornecida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68fc5-139">The file name extension is part of the URL, provided by the application.</span></span> <span data-ttu-id="68fc5-140">O tipo MIME pode estar disponível por meio do atributo de [**\_ tipo de \_ conteúdo \_ MF bytes**](mf-bytestream-content-type-attribute.md) no fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="68fc5-140">The MIME type might be available through the [**MF\_BYTESTREAM\_CONTENT\_TYPE**](mf-bytestream-content-type-attribute.md) attribute on the byte stream.</span></span>

<span data-ttu-id="68fc5-141">Para registrar um novo manipulador de fluxo de bytes, adicione uma entrada cujo nome seja o CLSID do manipulador, em formato de cadeia de caracteres canônica.</span><span class="sxs-lookup"><span data-stu-id="68fc5-141">To register a new byte-stream handler, add an entry whose name is the CLSID of the handler, in canonical string form.</span></span> <span data-ttu-id="68fc5-142">O valor da entrada é uma cadeia de caracteres (REG \_ SZ) que contém uma breve descrição do manipulador, como "meu manipulador de Byte-Stream".</span><span class="sxs-lookup"><span data-stu-id="68fc5-142">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Byte-Stream Handler."</span></span> <span data-ttu-id="68fc5-143">O resolvedor de origem chama **CoCreateInstance** para criar o manipulador a partir do CLSID.</span><span class="sxs-lookup"><span data-stu-id="68fc5-143">The source resolver calls **CoCreateInstance** to create the handler from the CLSID.</span></span> <span data-ttu-id="68fc5-144">Você pode registrar o mesmo manipulador em mais de uma extensão ou tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="68fc5-144">You can register the same handler under more than one extension or MIME type.</span></span>

<span data-ttu-id="68fc5-145">Os manipuladores de fluxo de bytes expõem a interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="68fc5-145">Byte-stream handlers expose the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="68fc5-146">Se o resolvedor de origem encontrar um manipulador de fluxo de bytes correspondente, ele chamará [**IMFByteStreamHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="68fc5-146">If the source resolver finds a matching byte-stream handler, it calls [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="68fc5-147">A entrada para esse método é um ponteiro para o fluxo de bytes, além da URL original, se disponível.</span><span class="sxs-lookup"><span data-stu-id="68fc5-147">The input to this method is a pointer to the byte stream, plus the original URL, if available.</span></span> <span data-ttu-id="68fc5-148">O manipulador de fluxo de bytes lê a partir do fluxo de bytes até que ele analise dados suficientes para criar a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="68fc5-148">The byte-stream handler reads from the byte stream until it parses enough data to create the media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68fc5-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68fc5-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68fc5-150">Resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="68fc5-150">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 




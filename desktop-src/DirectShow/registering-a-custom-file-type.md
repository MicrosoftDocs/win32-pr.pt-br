---
description: Este artigo descreve como o Gerenciador de gráfico de filtro localiza um filtro de origem, dado um nome de arquivo.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registrando um tipo de arquivo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758459"
---
# <a name="registering-a-custom-file-type"></a><span data-ttu-id="01c7c-103">Registrando um tipo de arquivo personalizado</span><span class="sxs-lookup"><span data-stu-id="01c7c-103">Registering a Custom File Type</span></span>

<span data-ttu-id="01c7c-104">Este artigo descreve como o Gerenciador de gráfico de filtro localiza um filtro de origem, dado um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="01c7c-104">This article describes how the Filter Graph Manager locates a source filter, given a file name.</span></span> <span data-ttu-id="01c7c-105">Você pode usar esse mecanismo para registrar seus próprios tipos de arquivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="01c7c-105">You can use this mechanism to register your own custom file types.</span></span> <span data-ttu-id="01c7c-106">Depois que o tipo de arquivo for registrado, o DirectShow carregará automaticamente o filtro de origem correto sempre que um aplicativo chamar [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span><span class="sxs-lookup"><span data-stu-id="01c7c-106">Once the file type is registered, DirectShow will automatically load the correct source filter whenever an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

-   [<span data-ttu-id="01c7c-107">Visão geral</span><span class="sxs-lookup"><span data-stu-id="01c7c-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="01c7c-108">Protocolos</span><span class="sxs-lookup"><span data-stu-id="01c7c-108">Protocols</span></span>](#protocols)
-   [<span data-ttu-id="01c7c-109">Extensões de arquivo</span><span class="sxs-lookup"><span data-stu-id="01c7c-109">File Extensions</span></span>](#file-extensions)
-   [<span data-ttu-id="01c7c-110">Verificar bytes</span><span class="sxs-lookup"><span data-stu-id="01c7c-110">Check Bytes</span></span>](#check-bytes)
-   [<span data-ttu-id="01c7c-111">Carregando o filtro de origem</span><span class="sxs-lookup"><span data-stu-id="01c7c-111">Loading the Source Filter</span></span>](#loading-the-source-filter)
-   [<span data-ttu-id="01c7c-112">Tipos de arquivo personalizados no Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="01c7c-112">Custom File Types in Windows Media Player</span></span>](#custom-file-types-in-windows-media-player)
-   [<span data-ttu-id="01c7c-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01c7c-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="01c7c-114">Visão geral</span><span class="sxs-lookup"><span data-stu-id="01c7c-114">Overview</span></span>

<span data-ttu-id="01c7c-115">Para localizar um filtro de origem de um determinado nome de arquivo, o Gerenciador de gráfico de filtro tenta fazer o seguinte, na ordem:</span><span class="sxs-lookup"><span data-stu-id="01c7c-115">To locate a source filter from a given file name, the Filter Graph Manager attempts to do the following, in order:</span></span>

1.  <span data-ttu-id="01c7c-116">Corresponder ao protocolo, se houver.</span><span class="sxs-lookup"><span data-stu-id="01c7c-116">Match the protocol, if any.</span></span>
2.  <span data-ttu-id="01c7c-117">Corresponder à extensão do arquivo.</span><span class="sxs-lookup"><span data-stu-id="01c7c-117">Match the file extension.</span></span>
3.  <span data-ttu-id="01c7c-118">Corresponder padrões de bytes no arquivo, chamado *verificar bytes*.</span><span class="sxs-lookup"><span data-stu-id="01c7c-118">Match patterns of bytes within the file, called *check bytes*.</span></span>

## <a name="protocols"></a><span data-ttu-id="01c7c-119">Protocolos</span><span class="sxs-lookup"><span data-stu-id="01c7c-119">Protocols</span></span>

<span data-ttu-id="01c7c-120">Os nomes de protocolo, como "FTP" ou "http", são registrados no</span><span class="sxs-lookup"><span data-stu-id="01c7c-120">Protocol names such as "ftp" or "http" are registered under the</span></span>

<span data-ttu-id="01c7c-121">**\_raiz de classes hKey \_**</span><span class="sxs-lookup"><span data-stu-id="01c7c-121">**HKEY\_CLASSES\_ROOT**</span></span>

<span data-ttu-id="01c7c-122">, com a seguinte estrutura:</span><span class="sxs-lookup"><span data-stu-id="01c7c-122">key, with the following structure:</span></span>


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



<span data-ttu-id="01c7c-123">Se o nome ou a URL do arquivo contiver dois-pontos (': '), o Gerenciador do grafo de filtro tentará usar a parte antes de ': ' como um nome de protocolo.</span><span class="sxs-lookup"><span data-stu-id="01c7c-123">If the file name or URL contains a colon (':'), the Filter Graph Manager attempts to use the portion before the ':' as a protocol name.</span></span> <span data-ttu-id="01c7c-124">Por exemplo, se o nome for "myprot://myfile.ext", ele pesquisará uma chave do registro chamada **myprot**.</span><span class="sxs-lookup"><span data-stu-id="01c7c-124">For example, if the name is "myprot://myfile.ext", it searches for a registry key named **myprot**.</span></span> <span data-ttu-id="01c7c-125">Se essa chave existir e contiver uma subchave chamada "Extensions", o Gerenciador do grafo de filtro pesquisará nessa subchave para obter as entradas que correspondam à extensão do arquivo.</span><span class="sxs-lookup"><span data-stu-id="01c7c-125">If this key exists and contains a subkey named "Extensions", the Filter Graph Manager searches within that subkey for entries that match the file extension.</span></span> <span data-ttu-id="01c7c-126">O valor da chave deve ser um GUID na forma de cadeia de caracteres; por exemplo, " {00000000-0000-0000-0000-000000000000} ".</span><span class="sxs-lookup"><span data-stu-id="01c7c-126">The value of the key must be a GUID in string form; for example, "{00000000-0000-0000-0000-000000000000}".</span></span> <span data-ttu-id="01c7c-127">Se o Gerenciador do grafo de filtro não puder corresponder a nada na subchave **extensões** , ele procurará uma subchave chamada **filtro de origem**, que também deve ser um GUID no formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="01c7c-127">If the Filter Graph Manager cannot match anything within the **Extensions** subkey, it looks for a subkey named **Source Filter**, which must also be a GUID in string form.</span></span>

<span data-ttu-id="01c7c-128">Se o Gerenciador do grafo de filtro encontrar um GUID correspondente, ele o usará como o CLSID do filtro de origem e tentará carregar o filtro.</span><span class="sxs-lookup"><span data-stu-id="01c7c-128">If the Filter Graph Manager finds a matching GUID, it uses this as the CLSID of the source filter, and attempts to load the filter.</span></span> <span data-ttu-id="01c7c-129">Se não encontrar uma correspondência, ela usará o filtro de [origem do arquivo (URL)](file-source--url--filter.md) , que trata o nome do arquivo como uma URL.</span><span class="sxs-lookup"><span data-stu-id="01c7c-129">If it does not find a match, it uses the [File Source (URL)](file-source--url--filter.md) filter, which treats the file name as a URL.</span></span>

<span data-ttu-id="01c7c-130">Há duas exceções a esse algoritmo:</span><span class="sxs-lookup"><span data-stu-id="01c7c-130">There are two exceptions to this algorithm:</span></span>

-   <span data-ttu-id="01c7c-131">Para excluir letras de driver, as cadeias de caracteres de caractere único não são consideradas protocolos.</span><span class="sxs-lookup"><span data-stu-id="01c7c-131">To exclude driver letters, single-character strings are not considered protocols.</span></span>
-   <span data-ttu-id="01c7c-132">Se a cadeia de caracteres for "file:" ou "file://", ela não será tratada como um protocolo.</span><span class="sxs-lookup"><span data-stu-id="01c7c-132">If the string is "file:" or "file://", it is not treated as a protocol.</span></span>

## <a name="file-extensions"></a><span data-ttu-id="01c7c-133">Extensões de arquivo</span><span class="sxs-lookup"><span data-stu-id="01c7c-133">File Extensions</span></span>

<span data-ttu-id="01c7c-134">Se não houver nenhum protocolo no nome do arquivo, o Gerenciador do grafo de filtro procurará entradas com as **\_ \_ \\ \\ extensões \\ da chave hKey classes do tipo de mídia raiz**.*ext* \\ , em que.*ext* é a extensão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="01c7c-134">If there is no protocol in the file name, the Filter Graph Manager looks in the registry for entries with the key **HKEY\_CLASSES\_ROOT\\Media Type\\Extensions\\**.*ext*\\, where .*ext* is the file extension.</span></span> <span data-ttu-id="01c7c-135">Se essa chave existir, o **filtro de origem** de valor conterá o CLSID do filtro de origem, em forma de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="01c7c-135">If this key exists, the value **Source Filter** contains the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="01c7c-136">Opcionalmente, a chave pode ter valores para **tipo de mídia** e **subtipo**, que fornecem os GUIDs de tipo e subtipo principais.</span><span class="sxs-lookup"><span data-stu-id="01c7c-136">Optionally, the key can have values for **Media Type** and **Subtype**, which give the major type and subtype GUIDs.</span></span>

## <a name="check-bytes"></a><span data-ttu-id="01c7c-137">Verificar bytes</span><span class="sxs-lookup"><span data-stu-id="01c7c-137">Check Bytes</span></span>

<span data-ttu-id="01c7c-138">Alguns tipos de arquivo podem ser identificados por padrões específicos de bits que ocorrem em deslocamentos de byte específicos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="01c7c-138">Some file types can be identified by specific patterns of bits occurring at specific byte offsets in the file.</span></span> <span data-ttu-id="01c7c-139">O Gerenciador de gráfico de filtro procura as chaves no registro com o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="01c7c-139">The Filter Graph Manager looks in the registry for keys with the following form:</span></span>

<span data-ttu-id="01c7c-140">**HKEY \_ \_ \\ MediaType \\ raiz de classes**{ *tipo principal* } \\ { *subtipo* }</span><span class="sxs-lookup"><span data-stu-id="01c7c-140">**HKEY\_CLASSES\_ROOT\\MediaType\\**{ *major type* }\\{ *subtype* }</span></span>

<span data-ttu-id="01c7c-141">onde o *tipo principal* e *SUBtipo* são GUIDs que definem o tipo de mídia para o fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="01c7c-141">where *major type* and *subtype* are GUIDs that define the media type for the byte stream.</span></span> <span data-ttu-id="01c7c-142">Cada chave contém uma ou mais subchaves, geralmente denominadas 1, 2 e assim por diante, que definem os bytes de verificação; e uma subchave chamada **filtro de origem** que fornece o CLSID do filtro de origem, em forma de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="01c7c-142">Each key contains one or more subkeys, usually named 1, 2, and so on, which define the check bytes; and a subkey named **Source Filter** that gives the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="01c7c-143">As subchaves de byte de verificação são cadeias de caracteres que contêm um ou mais quádruplos de números chamados:</span><span class="sxs-lookup"><span data-stu-id="01c7c-143">The check-byte subkeys are strings that contain one or more quads of numbers called:</span></span>

<span data-ttu-id="01c7c-144">*offset*, *CB*, *máscara*, *Val*</span><span class="sxs-lookup"><span data-stu-id="01c7c-144">*offset*, *cb*, *mask*, *val*</span></span>

<span data-ttu-id="01c7c-145">Para corresponder ao arquivo, o Gerenciador do grafo de filtro lê os bytes de CB, a partir do deslocamento de número de byte.</span><span class="sxs-lookup"><span data-stu-id="01c7c-145">To match the file, the Filter Graph Manager reads cb bytes, starting from byte number offset.</span></span> <span data-ttu-id="01c7c-146">Em seguida, ele executa uma e-bit em relação ao valor em Mask.</span><span class="sxs-lookup"><span data-stu-id="01c7c-146">It then performs a bitwise-AND against the value in mask.</span></span> <span data-ttu-id="01c7c-147">Se o resultado for igual a Val, o arquivo será uma correspondência para esse Quad.</span><span class="sxs-lookup"><span data-stu-id="01c7c-147">If the result equals val, the file is a match for that quad.</span></span> <span data-ttu-id="01c7c-148">Os valores Mask e Val são fornecidos em Hex.</span><span class="sxs-lookup"><span data-stu-id="01c7c-148">The values mask and val are given in hex.</span></span> <span data-ttu-id="01c7c-149">Uma entrada em branco para Mask é tratada como uma cadeia de 1s de comprimento de CB.</span><span class="sxs-lookup"><span data-stu-id="01c7c-149">A blank entry for mask is treated as a string of 1s of length cb.</span></span> <span data-ttu-id="01c7c-150">Um valor negativo para deslocamento indica um deslocamento do final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="01c7c-150">A negative value for offset indicates an offset from the end of the file.</span></span> <span data-ttu-id="01c7c-151">Para corresponder à chave, o arquivo deve corresponder a todos os quatro quádruplos em qualquer uma das subchaves.</span><span class="sxs-lookup"><span data-stu-id="01c7c-151">To match the key, the file must match all of the quads in any of the subkeys.</span></span>

<span data-ttu-id="01c7c-152">Por exemplo, suponha que o registro contenha as seguintes chaves em **\\ tipo de mídia de HKCR**:</span><span class="sxs-lookup"><span data-stu-id="01c7c-152">For example, assume the registry contains the following keys under **HKCR\\Media Type**:</span></span>


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



<span data-ttu-id="01c7c-153">A primeira chave corresponde ao fluxo de MEDIATYPE do tipo principal \_ .</span><span class="sxs-lookup"><span data-stu-id="01c7c-153">The first key corresponds to the major type MEDIATYPE\_Stream.</span></span> <span data-ttu-id="01c7c-154">A subchave abaixo corresponde à MIDI de MEDIATYPE de subtipo \_ .</span><span class="sxs-lookup"><span data-stu-id="01c7c-154">The subkey below that corresponds to the subtype MEDIATYPE\_Midi.</span></span> <span data-ttu-id="01c7c-155">O valor da subchave de filtro de origem é CLSID \_ AsyncReader, CLSID do filtro de [origem de arquivo (Async)](file-source--async--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="01c7c-155">The value for the Source Filter subkey is CLSID\_AsyncReader, the CLSID of the [File Source (Async)](file-source--async--filter.md) filter.</span></span>

<span data-ttu-id="01c7c-156">Cada entrada pode ter vários quádruplos; todos eles devem corresponder.</span><span class="sxs-lookup"><span data-stu-id="01c7c-156">Each entry can have multiple quadruples; all of them must match.</span></span> <span data-ttu-id="01c7c-157">No exemplo a seguir, os quatro primeiros bytes do arquivo devem ser 0xAB, 0xCD, 0x12, 0x34; e os últimos 4 bytes do arquivo devem ser 0xAB, 0xAB, 0x00, 0xAB:</span><span class="sxs-lookup"><span data-stu-id="01c7c-157">In the following example, the first 4 bytes of the file must be 0xAB, 0xCD, 0x12, 0x34; and the last 4 bytes of the file must be 0xAB, 0xAB, 0x00, 0xAB:</span></span>


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



<span data-ttu-id="01c7c-158">Além disso, pode haver várias entradas listadas em um único tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="01c7c-158">Also, there can be multiple entries listed under a single media type.</span></span> <span data-ttu-id="01c7c-159">Uma correspondência a qualquer um deles é suficiente.</span><span class="sxs-lookup"><span data-stu-id="01c7c-159">A match to any of them is sufficient.</span></span> <span data-ttu-id="01c7c-160">Esse esquema permite um conjunto de máscaras alternativas; por exemplo, arquivos. wav que podem ou não ter um cabeçalho RIFF.</span><span class="sxs-lookup"><span data-stu-id="01c7c-160">This scheme allows for a set of alternative masks; for instance, .wav files that might or might not have a RIFF header.</span></span>

> [!Note]  
> <span data-ttu-id="01c7c-161">Esse esquema é semelhante ao usado pela função [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) .</span><span class="sxs-lookup"><span data-stu-id="01c7c-161">This scheme is similar to the one used by the [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) function.</span></span>

 

## <a name="loading-the-source-filter"></a><span data-ttu-id="01c7c-162">Carregando o filtro de origem</span><span class="sxs-lookup"><span data-stu-id="01c7c-162">Loading the Source Filter</span></span>

<span data-ttu-id="01c7c-163">Supondo que o Gerenciador do grafo de filtro Localize um filtro de origem correspondente para o arquivo, ele adiciona esse filtro ao grafo, consulta o filtro para a interface [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) e chama [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span><span class="sxs-lookup"><span data-stu-id="01c7c-163">Assuming that the Filter Graph Manager finds a matching source filter for the file, it adds that filter to the graph, queries the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface, and calls [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span></span> <span data-ttu-id="01c7c-164">Os argumentos para o método **Load** são o nome do arquivo e o tipo de mídia, conforme determinado no registro.</span><span class="sxs-lookup"><span data-stu-id="01c7c-164">The arguments to the **Load** method are the file name and the media type, as determined from the registry.</span></span>

<span data-ttu-id="01c7c-165">Se o Gerenciador do grafo de filtro não encontrar nada no registro, o padrão será usar o filtro de origem de arquivo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="01c7c-165">If the Filter Graph Manager cannot find anything from the registry, it defaults to using the Async File Source filter.</span></span> <span data-ttu-id="01c7c-166">Nesse caso, ele define o tipo de mídia para **\_ fluxo de MediaType**, **MEDIASUBTYPE \_ None**.</span><span class="sxs-lookup"><span data-stu-id="01c7c-166">In that case, it sets the media type to **MEDIATYPE\_Stream**, **MEDIASUBTYPE\_None**.</span></span>

## <a name="custom-file-types-in-windows-media-player"></a><span data-ttu-id="01c7c-167">Tipos de arquivo personalizados no Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="01c7c-167">Custom File Types in Windows Media Player</span></span>

<span data-ttu-id="01c7c-168">O Windows Media Player usa um conjunto adicional de entradas de registro.</span><span class="sxs-lookup"><span data-stu-id="01c7c-168">Windows Media Player uses an additional set of registry entries.</span></span> <span data-ttu-id="01c7c-169">Para obter mais informações, consulte [configurações de registro de extensão de nome de arquivo](../wmp/file-name-extension-registry-settings.md) no SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="01c7c-169">For more information, see [File Name Extension Registry Settings](../wmp/file-name-extension-registry-settings.md) in the Windows Media Player SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01c7c-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01c7c-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01c7c-171">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="01c7c-171">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 

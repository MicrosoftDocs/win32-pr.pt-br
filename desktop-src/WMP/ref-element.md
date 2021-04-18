---
title: Elemento REF
description: O elemento REF especifica uma URL para o conteúdo de mídia digital.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Elemento REF do Windows Media Player
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786234"
---
# <a name="ref-element"></a><span data-ttu-id="8beaa-104">Elemento REF</span><span class="sxs-lookup"><span data-stu-id="8beaa-104">REF Element</span></span>

<span data-ttu-id="8beaa-105">O elemento **ref** especifica uma URL para o conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="8beaa-105">The **REF** element specifies a URL for digital media content.</span></span>

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a><span data-ttu-id="8beaa-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8beaa-106">Attributes</span></span>

<span data-ttu-id="8beaa-107">**Href** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="8beaa-107">**HREF** (required)</span></span>

<span data-ttu-id="8beaa-108">URL para qualquer parte do conteúdo de mídia com suporte no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8beaa-108">URL to any piece of media content supported by Windows Media Player.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="8beaa-109">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="8beaa-109">Parent/Child Elements</span></span>



| <span data-ttu-id="8beaa-110">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="8beaa-110">Hierarchy</span></span>       | <span data-ttu-id="8beaa-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="8beaa-111">Elements</span></span>                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8beaa-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8beaa-112">Parent elements</span></span> | <span data-ttu-id="8beaa-113">**INICIAL**</span><span class="sxs-lookup"><span data-stu-id="8beaa-113">**ENTRY**</span></span>                                                                        |
| <span data-ttu-id="8beaa-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8beaa-114">Child elements</span></span>  | <span data-ttu-id="8beaa-115">**duração**, **endmarcador**, **PREVIEWDURATION**, **STARTMARKER**, **StartTime**</span><span class="sxs-lookup"><span data-stu-id="8beaa-115">**DURATION**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **STARTTIME**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8beaa-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8beaa-116">Remarks</span></span>

<span data-ttu-id="8beaa-117">Esse elemento Especifica uma URL para uma parte do conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8beaa-117">This element specifies a URL for a piece of media content.</span></span> <span data-ttu-id="8beaa-118">A URL pode apontar para qualquer tipo de mídia com suporte, usando qualquer protocolo suportado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8beaa-118">The URL can point to any media type supported, using any protocol supported by Windows Media Player.</span></span>

<span data-ttu-id="8beaa-119">Os tipos de mídia com suporte incluem imagens ainda, como imagens. gif e. jpg e arquivos flash com uma extensão de nome de arquivo. swf.</span><span class="sxs-lookup"><span data-stu-id="8beaa-119">The media types supported include still images such as .gif and .jpg images and Flash files with an .swf file name extension.</span></span> <span data-ttu-id="8beaa-120">Esses tipos de mídia são úteis para incluir conteúdo de publicidade em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="8beaa-120">These media types are useful for including advertising content within a playlist.</span></span> <span data-ttu-id="8beaa-121">Com arquivos de imagem e arquivos flash que são executados em um loop, você também deve especificar a quantidade de tempo para exibir o item de mídia, incluindo um elemento **Duration** dentro do elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="8beaa-121">With image files and Flash files that play in a loop, you must also specify the amount of time to display the media item by including a **DURATION** element within the **REF** element.</span></span> <span data-ttu-id="8beaa-122">Se você quiser que uma imagem continue a ser exibida enquanto a próxima entrada na lista de reprodução estiver armazenada em buffer, inclua um elemento **param** dentro do elemento **entry** , defina seu atributo **Name** como ShowWhileBuffering e defina seu atributo **Value** como true.</span><span class="sxs-lookup"><span data-stu-id="8beaa-122">If you want an image to continue displaying while the next entry in the playlist is buffered, include a **PARAM** element within the **ENTRY** element, set its **name** attribute to ShowWhileBuffering, and set its **value** attribute to true.</span></span>

<span data-ttu-id="8beaa-123">Para fazer referência ao conteúdo em um CD ou DVD que permita, os protocolos Wmpcd e wmpdvd são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="8beaa-123">To reference content on a CD or a DVD that allows it, the wmpcd and wmpdvd protocols are provided.</span></span> <span data-ttu-id="8beaa-124">Por exemplo, definir o atributo **href** como "wmpdvd://f/5/3" executará o capítulo 3 do título 5 em um DVD, mas somente se o DVD tiver sido criado para permiti-lo.</span><span class="sxs-lookup"><span data-stu-id="8beaa-124">For example, setting the **HREF** attribute to "wmpdvd://f/5/3" will play chapter 3 of title 5 on a DVD, but only if the DVD has been authored to allow it.</span></span>

<span data-ttu-id="8beaa-125">Os aplicativos que abrirem mídia digital por trás de um firewall terão um desempenho melhor ao abrir os itens de mídia se o endereço for especificado usando o nome DNS (servidor de nomes de domínio) em vez do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="8beaa-125">Applications that open digital media from behind a firewall will have better performance when opening the media items if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="8beaa-126">O uso mais comum desse elemento é para substituição de URL.</span><span class="sxs-lookup"><span data-stu-id="8beaa-126">The most common use of this element is for URL rollover.</span></span> <span data-ttu-id="8beaa-127">Se o Windows Media Player não puder abrir uma parte da mídia definida em um elemento **ref** , ele tentará a URL no próximo elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="8beaa-127">If Windows Media Player is unable to open a piece of media defined in a **REF** element, it tries the URL in the next **REF** element.</span></span> <span data-ttu-id="8beaa-128">Depois que o Windows Media Player abre o conteúdo de mídia de uma URL definida no escopo de um elemento de **entrada** , ele ignora as marcas de **referência** subsequentes dentro desse elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="8beaa-128">Once Windows Media Player opens media content from a URL defined within the scope of one **ENTRY** element, it ignores subsequent **REF** tags within that **ENTRY** element.</span></span> <span data-ttu-id="8beaa-129">Depois que a parte do conteúdo é executada, o Windows Media Player passa para o próximo elemento de **entrada** , se houver.</span><span class="sxs-lookup"><span data-stu-id="8beaa-129">After the piece of content is done playing, Windows Media Player moves on to the next **ENTRY** element, if any.</span></span>

-   <span data-ttu-id="8beaa-130">**Importante** Depois que o Windows Media Player estabelece uma conexão com uma parte de conteúdo referenciada, ele ignora todos os outros elementos **ref** nessa **entrada**, independentemente de a conexão ser encerrada normalmente ou de forma anormal.</span><span class="sxs-lookup"><span data-stu-id="8beaa-130">**Important** Once Windows Media Player establishes a connection to a referenced piece of content, it ignores all other **REF** elements in that **ENTRY**, whether the connection terminates normally or abnormally.</span></span>

<span data-ttu-id="8beaa-131">Se o item de mídia referenciado for um arquivo de imagem, o elemento **Duration** deverá ser usado para especificar o tempo de exibição da imagem.</span><span class="sxs-lookup"><span data-stu-id="8beaa-131">If the media item referenced is an image file, the **DURATION** element must be used to specify the display time for the image.</span></span>

<span data-ttu-id="8beaa-132">**Observação**</span><span class="sxs-lookup"><span data-stu-id="8beaa-132">**Note**</span></span>

<span data-ttu-id="8beaa-133">A tentativa de reproduzir mídia flash que inclui som com o primeiro quadro pode gerar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="8beaa-133">Attempting to play Flash media that includes sound with the first frame may yield unexpected results.</span></span> <span data-ttu-id="8beaa-134">Você deve criar o conteúdo do flash para tocar no som, começando no início do segundo quadro.</span><span class="sxs-lookup"><span data-stu-id="8beaa-134">You should author Flash content to play sound starting no earlier than the second frame.</span></span>

## <a name="examples"></a><span data-ttu-id="8beaa-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8beaa-135">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="8beaa-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8beaa-136">Requirements</span></span>



| <span data-ttu-id="8beaa-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8beaa-137">Requirement</span></span> | <span data-ttu-id="8beaa-138">Valor</span><span class="sxs-lookup"><span data-stu-id="8beaa-138">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8beaa-139">Versão</span><span class="sxs-lookup"><span data-stu-id="8beaa-139">Version</span></span><br/> | <span data-ttu-id="8beaa-140">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8beaa-140">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8beaa-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="8beaa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8beaa-142">**Tipos de arquivos e protocolos com suporte**</span><span class="sxs-lookup"><span data-stu-id="8beaa-142">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> <dt>

[<span data-ttu-id="8beaa-143">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8beaa-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8beaa-144">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8beaa-144">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 






---
title: Protocolo WMPDVD
description: Protocolo WMPDVD
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows Media Player, protocolos
- Modelo de objeto do Windows Media Player, protocolos
- modelo de objeto, protocolos
- Controle ActiveX do Windows Media Player, protocolos para o modelo de objeto
- Controle ActiveX, protocolos para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, protocolos para modelo de objeto
- Windows Media Player Mobile, protocolos para modelo de objeto
- protocolos, modelo de objeto do Windows Media Player
- protocolos, WMPDVD
- Protocolo WMPDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292105"
---
# <a name="wmpdvd-protocol"></a><span data-ttu-id="90939-113">Protocolo WMPDVD</span><span class="sxs-lookup"><span data-stu-id="90939-113">WMPDVD Protocol</span></span>

<span data-ttu-id="90939-114">O protocolo WMPDVD permite que você especifique a mídia de um DVD usando a sintaxe de URL.</span><span class="sxs-lookup"><span data-stu-id="90939-114">The WMPDVD protocol enables you to specify media from a DVD using URL syntax.</span></span> <span data-ttu-id="90939-115">Essa é a forma geral do protocolo:</span><span class="sxs-lookup"><span data-stu-id="90939-115">This is the general form of the protocol:</span></span>


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



<span data-ttu-id="90939-116">O segmento da *unidade* é a letra da unidade de DVD; Ele não inclui os dois-pontos normalmente usados com especificadores de unidade.</span><span class="sxs-lookup"><span data-stu-id="90939-116">The *drive* segment is the letter of the DVD drive; it does not include the colon typically used with drive specifiers.</span></span> <span data-ttu-id="90939-117">Esse segmento é sempre necessário.</span><span class="sxs-lookup"><span data-stu-id="90939-117">This segment is always required.</span></span>

<span data-ttu-id="90939-118">O segmento de *título* é o número do título a ser tocado.</span><span class="sxs-lookup"><span data-stu-id="90939-118">The *title* segment is the number of the title to play.</span></span> <span data-ttu-id="90939-119">Ela não é necessária, a menos que você queira iniciar a reprodução em um título específico ou em um capítulo específico de um título específico.</span><span class="sxs-lookup"><span data-stu-id="90939-119">It is not required unless you want to start playback at a specific title or at a specific chapter of a specific title.</span></span>

<span data-ttu-id="90939-120">O segmento do *capítulo* é o número do capítulo a ser tocado.</span><span class="sxs-lookup"><span data-stu-id="90939-120">The *chapter* segment is the number of the chapter to play.</span></span> <span data-ttu-id="90939-121">Isso não é necessário, a menos que você queira iniciar a reprodução em um capítulo específico de um título específico.</span><span class="sxs-lookup"><span data-stu-id="90939-121">It is not required unless you want to start playback at a specific chapter of a specific title.</span></span>

<span data-ttu-id="90939-122">O argumento contentdir é o caminho para um TS de vídeo \_ . Arquivo IFO, que pode estar no armazenamento local ou em um compartilhamento de rede.</span><span class="sxs-lookup"><span data-stu-id="90939-122">The contentdir argument is the path to a VIDEO\_TS.IFO file, which may be in local storage or on a network share.</span></span> <span data-ttu-id="90939-123">Se você incluir esse segmento, o segmento da *unidade* será ignorado, embora ainda seja necessário.</span><span class="sxs-lookup"><span data-stu-id="90939-123">If you include this segment, then the *drive* segment is ignored although it is still required.</span></span> <span data-ttu-id="90939-124">Se você também incluir o segmento do *título* ou os segmentos do *título* e do *capítulo* , eles serão relativos ao conteúdo do DVD especificado no segmento contentdir, não ao segmento da *unidade* .</span><span class="sxs-lookup"><span data-stu-id="90939-124">If you also include the *title* segment or both the *title* and *chapter* segments then they are relative to the DVD content specified in the contentdir segment, not the *drive* segment.</span></span>

<span data-ttu-id="90939-125">O exemplo a seguir usa o protocolo WMPDVD para reproduzir o DVD desde o início, como se ele estivesse sendo iniciado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="90939-125">The following example uses the WMPDVD protocol to play the DVD from the beginning, as if it were starting automatically.</span></span>


```C++
player.url = "wmpdvd://F";
```



<span data-ttu-id="90939-126">O exemplo a seguir usa o protocolo WMPDVD para reproduzir o DVD do início do título especificado.</span><span class="sxs-lookup"><span data-stu-id="90939-126">The following example uses the WMPDVD protocol to play the DVD from the beginning of the specified title.</span></span>


```C++
player.url = "wmpdvd://F/2";
```



<span data-ttu-id="90939-127">O exemplo a seguir usa o protocolo WMPDVD para reproduzir o DVD do capítulo especificado.</span><span class="sxs-lookup"><span data-stu-id="90939-127">The following example uses the WMPDVD protocol to play the DVD from the specified chapter.</span></span>


```C++
player.url = "wmpdvd://F/2/4";
```



<span data-ttu-id="90939-128">O exemplo a seguir usa o protocolo WMPDVD para reproduzir conteúdo de DVD do armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="90939-128">The following example uses the WMPDVD protocol to play DVD content from local storage.</span></span> <span data-ttu-id="90939-129">A cadeia de caracteres de *caminho* termina com a pasta que contém o vídeo \_ TS. Arquivo IFO; Ele não inclui o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="90939-129">The *path* string ends with the folder that contains the VIDEO\_TS.IFO file; it does not include the file name.</span></span> <span data-ttu-id="90939-130">Neste exemplo, o valor do segmento da *unidade* não tem nenhum efeito, embora seja necessário, e a reprodução começa no capítulo 4 do título 2.</span><span class="sxs-lookup"><span data-stu-id="90939-130">In this example, the value of the *drive* segment has no effect although it is required, and playback begins in chapter 4 of title 2.</span></span>


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



<span data-ttu-id="90939-131">A atribuição de uma cadeia de caracteres WMPDVD à propriedade **URL** requer o Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="90939-131">Assigning a WMPDVD string to the **url** property requires Windows Media Player 9 Series or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90939-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90939-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90939-133">**Tipos de arquivos e protocolos com suporte**</span><span class="sxs-lookup"><span data-stu-id="90939-133">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 





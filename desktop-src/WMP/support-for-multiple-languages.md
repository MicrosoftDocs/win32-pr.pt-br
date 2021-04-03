---
title: Suporte para vários idiomas
description: Suporte para vários idiomas
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Playlists do metarquivo do Windows Media, suporte para vários idiomas
- listas de reprodução de metarquivo, suporte para vários idiomas
- listas de reprodução, suporte para vários idiomas
- Playlists do metarquivo do Windows Media, suporte a vários idiomas
- playlists de metarquivo, suporte a vários idiomas
- playlists, suporte a vários idiomas
- Playlists do metarquivo do Windows Media, suporte a idiomas
- playlists de metarquivo, suporte a idiomas
- playlists, suporte a idiomas
- suporte para vários idiomas
- suporte a vários idiomas.
- suporte de idiomas
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005999"
---
# <a name="support-for-multiple-languages"></a><span data-ttu-id="0d33e-115">Suporte para vários idiomas</span><span class="sxs-lookup"><span data-stu-id="0d33e-115">Support for Multiple Languages</span></span>

<span data-ttu-id="0d33e-116">O Windows Media Player 9 Series ou posterior dá suporte a arquivos de mídia do Windows Media criados usando o conjunto de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="0d33e-116">Windows Media Player 9 Series or later supports Windows Media metafiles created using the Unicode character set.</span></span> <span data-ttu-id="0d33e-117">Isso permite que você inclua metadados multilíngües na sua lista de reprodução de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="0d33e-117">This allows you to include multilingual metadata in your metafile playlist.</span></span> <span data-ttu-id="0d33e-118">As regras a seguir regem o uso de metadados multilíngües em metaarquivos do Windows Media:</span><span class="sxs-lookup"><span data-stu-id="0d33e-118">The following rules govern the use of multilingual metadata in Windows Media metafiles:</span></span>

-   <span data-ttu-id="0d33e-119">Os caracteres devem ser codificados usando o esquema de codificação UTF-8.</span><span class="sxs-lookup"><span data-stu-id="0d33e-119">Characters must be encoded using the UTF-8 encoding scheme.</span></span>
-   <span data-ttu-id="0d33e-120">A lista de reprodução de metarquivo deve incluir o seguinte **parâmetro** no nível de playlist:</span><span class="sxs-lookup"><span data-stu-id="0d33e-120">The metafile playlist must include the following **PARAM** at the playlist level:</span></span>
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   <span data-ttu-id="0d33e-121">Somente o Windows Media Player 9 Series ou posterior dá suporte a essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="0d33e-121">Only Windows Media Player 9 Series or later supports this functionality.</span></span>
-   <span data-ttu-id="0d33e-122">Se a lista de reprodução do metarquivo não for salva com codificação UTF-8 e o elemento **param** correto, ela será analisada usando a página de código padrão de localidade do sistema do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d33e-122">If the metafile playlist is not saved with UTF-8 encoding and the correct **PARAM** element, it will be parsed using the default system locale code page of the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d33e-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d33e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d33e-124">**Elemento PARAM**</span><span class="sxs-lookup"><span data-stu-id="0d33e-124">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="0d33e-125">**Visão geral dos metaarquivos do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0d33e-125">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 





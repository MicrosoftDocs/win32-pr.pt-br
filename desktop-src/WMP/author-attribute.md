---
title: Atributo de autor
description: O atributo autor é o nome de um artista de mídia ou ator associado ao conteúdo.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Atributo de autor Windows Media Player
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760473"
---
# <a name="author-attribute"></a><span data-ttu-id="96f05-104">Atributo de autor</span><span class="sxs-lookup"><span data-stu-id="96f05-104">Author Attribute</span></span>

<span data-ttu-id="96f05-105">O atributo **autor** é o nome de um artista de mídia ou ator associado ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="96f05-105">The **Author** attribute is the name of a media artist or actor associated with the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="96f05-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="96f05-106">Applies To</span></span>

-   [<span data-ttu-id="96f05-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="96f05-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="96f05-108">Playlists de CD</span><span class="sxs-lookup"><span data-stu-id="96f05-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="96f05-109">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="96f05-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="96f05-110">Arquivos de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="96f05-110">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="96f05-111">DVDs</span><span class="sxs-lookup"><span data-stu-id="96f05-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="96f05-112">Media. getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="96f05-112">Media.getItemInfoByType</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="96f05-113">Itens de foto</span><span class="sxs-lookup"><span data-stu-id="96f05-113">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="96f05-114">Playlists</span><span class="sxs-lookup"><span data-stu-id="96f05-114">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="96f05-115">Itens de rádio</span><span class="sxs-lookup"><span data-stu-id="96f05-115">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="96f05-116">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="96f05-116">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="96f05-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="96f05-117">Remarks</span></span>

<span data-ttu-id="96f05-118">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="96f05-118">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="96f05-119">Esse atributo pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="96f05-119">This attribute may have multiple values.</span></span> <span data-ttu-id="96f05-120">Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar a *mídia*. método **getItemInfoByType** , não a *mídia*. método **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="96f05-120">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.**getItemInfo** method.</span></span>

<span data-ttu-id="96f05-121">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMAuthor.</span><span class="sxs-lookup"><span data-stu-id="96f05-121">The Windows Media Format SDK constant for this attribute is g\_wszWMAuthor.</span></span>

<span data-ttu-id="96f05-122">**Ator** e **artista** são aliases para este atributo.</span><span class="sxs-lookup"><span data-stu-id="96f05-122">**Actor** and **Artist** are aliases for this attribute.</span></span>

<span data-ttu-id="96f05-123">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="96f05-123">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="96f05-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96f05-124">Requirements</span></span>



| <span data-ttu-id="96f05-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="96f05-125">Requirement</span></span> | <span data-ttu-id="96f05-126">Valor</span><span class="sxs-lookup"><span data-stu-id="96f05-126">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="96f05-127">Versão</span><span class="sxs-lookup"><span data-stu-id="96f05-127">Version</span></span><br/> | <span data-ttu-id="96f05-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="96f05-128">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96f05-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="96f05-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f05-130">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="96f05-130">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






---
title: Atributo do WM/gênero
description: O atributo WM/gênero é o gênero do conteúdo.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- Atributo do WM/gênero Windows Media Player
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae4a0c6ae27e85fa1ed147a3173c4cc31b20f1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765299"
---
# <a name="wmgenre-attribute"></a><span data-ttu-id="0daf4-104">Atributo do WM/gênero</span><span class="sxs-lookup"><span data-stu-id="0daf4-104">WM/Genre Attribute</span></span>

<span data-ttu-id="0daf4-105">O atributo **WM/gênero** é o gênero do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0daf4-105">The **WM/Genre** attribute is the genre of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0daf4-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="0daf4-106">Applies To</span></span>

-   [<span data-ttu-id="0daf4-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="0daf4-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="0daf4-108">Playlists de CD</span><span class="sxs-lookup"><span data-stu-id="0daf4-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="0daf4-109">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="0daf4-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="0daf4-110">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="0daf4-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="0daf4-111">DVDs</span><span class="sxs-lookup"><span data-stu-id="0daf4-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="0daf4-112">Outros itens</span><span class="sxs-lookup"><span data-stu-id="0daf4-112">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="0daf4-113">Playlists</span><span class="sxs-lookup"><span data-stu-id="0daf4-113">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="0daf4-114">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="0daf4-114">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="0daf4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0daf4-115">Remarks</span></span>

<span data-ttu-id="0daf4-116">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="0daf4-116">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="0daf4-117">Esse atributo pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="0daf4-117">This attribute may have multiple values.</span></span> <span data-ttu-id="0daf4-118">Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar o método **Media. getItemInfoByType** , não o método **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="0daf4-118">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="0daf4-119">**Gênero** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="0daf4-119">**Genre** is an alias for this attribute.</span></span>

<span data-ttu-id="0daf4-120">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMGenre.</span><span class="sxs-lookup"><span data-stu-id="0daf4-120">The Windows Media Format SDK constant for this attribute is g\_wszWMGenre.</span></span>

<span data-ttu-id="0daf4-121">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="0daf4-121">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0daf4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0daf4-122">Requirements</span></span>



| <span data-ttu-id="0daf4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0daf4-123">Requirement</span></span> | <span data-ttu-id="0daf4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0daf4-124">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="0daf4-125">Versão</span><span class="sxs-lookup"><span data-stu-id="0daf4-125">Version</span></span><br/> | <span data-ttu-id="0daf4-126">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="0daf4-126">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0daf4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0daf4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0daf4-128">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="0daf4-128">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="0daf4-129">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="0daf4-129">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 






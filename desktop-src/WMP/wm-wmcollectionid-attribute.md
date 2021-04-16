---
title: Atributo WM/WMCollectionID
description: O atributo WM/WMCollectionID é um GUID que identifica a coleção à qual o item pertence.
ms.assetid: 21fc0a62-d374-4ca3-bbb8-278e0d2497ce
keywords:
- Atributo WM/WMCollectionID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bce21196e1da9583db293dab004812265c85308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105808249"
---
# <a name="wmwmcollectionid-attribute"></a><span data-ttu-id="43783-104">Atributo WM/WMCollectionID</span><span class="sxs-lookup"><span data-stu-id="43783-104">WM/WMCollectionID Attribute</span></span>

<span data-ttu-id="43783-105">O atributo **WM/WMCollectionID** é um GUID que identifica a coleção à qual o item pertence.</span><span class="sxs-lookup"><span data-stu-id="43783-105">The **WM/WMCollectionID** attribute is a GUID identifying the collection to which the item belongs.</span></span>

## <a name="applies-to"></a><span data-ttu-id="43783-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="43783-106">Applies To</span></span>

-   [<span data-ttu-id="43783-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="43783-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="43783-108">Playlists de CD</span><span class="sxs-lookup"><span data-stu-id="43783-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="43783-109">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="43783-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="43783-110">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="43783-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="43783-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="43783-111">Remarks</span></span>

<span data-ttu-id="43783-112">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="43783-112">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="43783-113">**WMCollectionID** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="43783-113">**WMCollectionID** is an alias for this attribute.</span></span>

<span data-ttu-id="43783-114">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMCollectionID.</span><span class="sxs-lookup"><span data-stu-id="43783-114">The Windows Media Format SDK constant for this attribute is g\_wszWMCollectionID.</span></span>

<span data-ttu-id="43783-115">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="43783-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="43783-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43783-116">Requirements</span></span>



| <span data-ttu-id="43783-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="43783-117">Requirement</span></span> | <span data-ttu-id="43783-118">Valor</span><span class="sxs-lookup"><span data-stu-id="43783-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="43783-119">Versão</span><span class="sxs-lookup"><span data-stu-id="43783-119">Version</span></span><br/> | <span data-ttu-id="43783-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="43783-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43783-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="43783-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43783-122">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="43783-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






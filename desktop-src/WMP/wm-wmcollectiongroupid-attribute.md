---
title: Atributo WM/WMCollectionGroupID
description: O atributo WM/WMCollectionGroupID é um GUID que identifica o grupo que contém a coleção à qual o item pertence.
ms.assetid: 5383fb12-fc16-474e-b9a0-c1e69b86a057
keywords:
- Atributo WM/WMCollectionGroupID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681ad7049520ed77de3ebb385e74efcfef66b4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798197"
---
# <a name="wmwmcollectiongroupid-attribute"></a><span data-ttu-id="40cb6-104">Atributo WM/WMCollectionGroupID</span><span class="sxs-lookup"><span data-stu-id="40cb6-104">WM/WMCollectionGroupID Attribute</span></span>

<span data-ttu-id="40cb6-105">O atributo **WM/WMCollectionGroupID** é um GUID que identifica o grupo que contém a coleção à qual o item pertence.</span><span class="sxs-lookup"><span data-stu-id="40cb6-105">The **WM/WMCollectionGroupID** attribute is a GUID identifying the group containing the collection to which the item belongs.</span></span>

## <a name="applies-to"></a><span data-ttu-id="40cb6-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="40cb6-106">Applies To</span></span>

-   [<span data-ttu-id="40cb6-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="40cb6-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="40cb6-108">Playlists de CD</span><span class="sxs-lookup"><span data-stu-id="40cb6-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="40cb6-109">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="40cb6-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="40cb6-110">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="40cb6-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="40cb6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="40cb6-111">Remarks</span></span>

<span data-ttu-id="40cb6-112">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="40cb6-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="40cb6-113">**WMCollectionGroupID** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="40cb6-113">**WMCollectionGroupID** is an alias for this attribute.</span></span>

<span data-ttu-id="40cb6-114">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMCollectionGroupID.</span><span class="sxs-lookup"><span data-stu-id="40cb6-114">The Windows Media Format SDK constant for this attribute is g\_wszWMCollectionGroupID.</span></span>

<span data-ttu-id="40cb6-115">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="40cb6-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="40cb6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40cb6-116">Requirements</span></span>



| <span data-ttu-id="40cb6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="40cb6-117">Requirement</span></span> | <span data-ttu-id="40cb6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="40cb6-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="40cb6-119">Versão</span><span class="sxs-lookup"><span data-stu-id="40cb6-119">Version</span></span><br/> | <span data-ttu-id="40cb6-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="40cb6-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40cb6-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="40cb6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40cb6-122">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="40cb6-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






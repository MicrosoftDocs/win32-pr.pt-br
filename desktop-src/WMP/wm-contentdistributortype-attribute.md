---
title: Atributo WM/ContentDistributorType
description: O atributo WM/ContentDistributorType é o tipo do distribuidor do item.
ms.assetid: 3be711a2-51b0-4b61-8009-f97394207b1c
keywords:
- Atributo WM/ContentDistributorType do Windows Media Player
topic_type:
- apiref
api_name:
- WM/ContentDistributorType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 855deecf09759edb3e0f61c16f8b5d4692171fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793336"
---
# <a name="wmcontentdistributortype-attribute"></a><span data-ttu-id="1deb8-104">Atributo WM/ContentDistributorType</span><span class="sxs-lookup"><span data-stu-id="1deb8-104">WM/ContentDistributorType Attribute</span></span>

<span data-ttu-id="1deb8-105">O atributo **WM/ContentDistributorType** é o tipo do distribuidor do item.</span><span class="sxs-lookup"><span data-stu-id="1deb8-105">The **WM/ContentDistributorType** attribute is the type of the distributor of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1deb8-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="1deb8-106">Applies To</span></span>

-   [<span data-ttu-id="1deb8-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="1deb8-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="1deb8-108">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="1deb8-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="1deb8-109">Playlists</span><span class="sxs-lookup"><span data-stu-id="1deb8-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="1deb8-110">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="1deb8-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="1deb8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1deb8-111">Remarks</span></span>

<span data-ttu-id="1deb8-112">O valor desse atributo será definido como "List" ou "Radio".</span><span class="sxs-lookup"><span data-stu-id="1deb8-112">The value of this attribute will be set to either "List" or "Radio".</span></span> <span data-ttu-id="1deb8-113">Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="1deb8-113">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="1deb8-114">**ContentDistributorType** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="1deb8-114">**ContentDistributorType** is an alias for this attribute.</span></span>

<span data-ttu-id="1deb8-115">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMContentDistributorType.</span><span class="sxs-lookup"><span data-stu-id="1deb8-115">The Windows Media Format SDK constant for this attribute is g\_wszWMContentDistributorType.</span></span>

<span data-ttu-id="1deb8-116">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1deb8-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1deb8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1deb8-117">Requirements</span></span>



| <span data-ttu-id="1deb8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1deb8-118">Requirement</span></span> | <span data-ttu-id="1deb8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1deb8-119">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="1deb8-120">Versão</span><span class="sxs-lookup"><span data-stu-id="1deb8-120">Version</span></span><br/> | <span data-ttu-id="1deb8-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="1deb8-121">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1deb8-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1deb8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1deb8-123">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="1deb8-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






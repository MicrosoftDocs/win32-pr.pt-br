---
title: Atributo WM/MediaClassPrimaryID
description: O atributo WM/MediaClassPrimaryID é um GUID que especifica uma das classes de mídia primárias música, áudio não música, vídeo ou outro.
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- Atributo WM/MediaClassPrimaryID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5107a2c4e04e9424bf0a20a7d4cf7b8edef80492
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797986"
---
# <a name="wmmediaclassprimaryid-attribute"></a><span data-ttu-id="e41ef-104">Atributo WM/MediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="e41ef-104">WM/MediaClassPrimaryID Attribute</span></span>

<span data-ttu-id="e41ef-105">O atributo **WM/MediaClassPrimaryID** é um GUID que especifica uma das classes de mídia primárias: música, áudio não musical, vídeo ou outro.</span><span class="sxs-lookup"><span data-stu-id="e41ef-105">The **WM/MediaClassPrimaryID** attribute is a GUID specifying one of the primary media classes: music, non-music audio, video, or other.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e41ef-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="e41ef-106">Applies To</span></span>

-   [<span data-ttu-id="e41ef-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="e41ef-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="e41ef-108">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="e41ef-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="e41ef-109">Outros itens</span><span class="sxs-lookup"><span data-stu-id="e41ef-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="e41ef-110">Itens de foto</span><span class="sxs-lookup"><span data-stu-id="e41ef-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="e41ef-111">Playlists</span><span class="sxs-lookup"><span data-stu-id="e41ef-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="e41ef-112">Itens de rádio</span><span class="sxs-lookup"><span data-stu-id="e41ef-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="e41ef-113">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="e41ef-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e41ef-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e41ef-114">Remarks</span></span>

<span data-ttu-id="e41ef-115">Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="e41ef-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="e41ef-116">**MediaClassPrimaryID** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="e41ef-116">**MediaClassPrimaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="e41ef-117">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMMediaClassPrimaryID.</span><span class="sxs-lookup"><span data-stu-id="e41ef-117">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassPrimaryID.</span></span>

<span data-ttu-id="e41ef-118">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="e41ef-118">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41ef-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e41ef-119">Requirements</span></span>



| <span data-ttu-id="e41ef-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e41ef-120">Requirement</span></span> | <span data-ttu-id="e41ef-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e41ef-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e41ef-122">Versão</span><span class="sxs-lookup"><span data-stu-id="e41ef-122">Version</span></span><br/> | <span data-ttu-id="e41ef-123">Windows Media Player 9 Series ou posterior (o item de foto tem suporte apenas no Windows Media Player 10 ou posterior)</span><span class="sxs-lookup"><span data-stu-id="e41ef-123">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e41ef-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e41ef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41ef-125">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="e41ef-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






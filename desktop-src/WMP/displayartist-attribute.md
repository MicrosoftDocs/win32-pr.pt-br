---
title: Atributo DisplayArtist
description: O atributo DisplayArtist é o nome do artista que é exibido para um item.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- Atributo DisplayArtist Windows Media Player
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760268"
---
# <a name="displayartist-attribute"></a><span data-ttu-id="01ab6-104">Atributo DisplayArtist</span><span class="sxs-lookup"><span data-stu-id="01ab6-104">DisplayArtist Attribute</span></span>

<span data-ttu-id="01ab6-105">O atributo **DisplayArtist** é o nome do artista que é exibido para um item.</span><span class="sxs-lookup"><span data-stu-id="01ab6-105">The **DisplayArtist** attribute is the name of the artist that is displayed for an item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="01ab6-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="01ab6-106">Applies To</span></span>

-   [<span data-ttu-id="01ab6-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="01ab6-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="01ab6-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="01ab6-108">Remarks</span></span>

<span data-ttu-id="01ab6-109">Em geral, **DisplayArtist** terá o mesmo valor que o atributo **WM/AlbumArtist** quando esse atributo for definido.</span><span class="sxs-lookup"><span data-stu-id="01ab6-109">Generally, **DisplayArtist** will have the same value as the **WM/AlbumArtist** attribute when that attribute is set.</span></span> <span data-ttu-id="01ab6-110">Caso contrário, o valor será o nome do artista associado à primeira faixa no álbum.</span><span class="sxs-lookup"><span data-stu-id="01ab6-110">Otherwise, the value will be the name of the artist that is associated with the first track on the album.</span></span>

<span data-ttu-id="01ab6-111">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="01ab6-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="01ab6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01ab6-112">Requirements</span></span>



| <span data-ttu-id="01ab6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="01ab6-113">Requirement</span></span> | <span data-ttu-id="01ab6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="01ab6-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="01ab6-115">Versão</span><span class="sxs-lookup"><span data-stu-id="01ab6-115">Version</span></span><br/> | <span data-ttu-id="01ab6-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="01ab6-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01ab6-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="01ab6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01ab6-118">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="01ab6-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="01ab6-119">**Atributo WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="01ab6-119">**WM/AlbumArtist Attribute**</span></span>](wm-albumartist-attribute.md)
</dt> </dl>

 

 






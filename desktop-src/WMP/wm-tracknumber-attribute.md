---
title: Atributo WM/TrackNumber
description: O atributo WM/TrackNumber é o número de faixa do item no álbum no qual ele foi originalmente lançado.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- Atributo WM/TrackNumber do Windows Media Player
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788149"
---
# <a name="wmtracknumber-attribute"></a><span data-ttu-id="361eb-104">Atributo WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="361eb-104">WM/TrackNumber Attribute</span></span>

<span data-ttu-id="361eb-105">O atributo **WM/TrackNumber** é o número de faixa do item no álbum no qual ele foi originalmente lançado.</span><span class="sxs-lookup"><span data-stu-id="361eb-105">The **WM/TrackNumber** attribute is the track number of the item on the album on which it was originally released.</span></span>

## <a name="applies-to"></a><span data-ttu-id="361eb-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="361eb-106">Applies To</span></span>

-   [<span data-ttu-id="361eb-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="361eb-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="361eb-108">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="361eb-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="361eb-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="361eb-109">Remarks</span></span>

<span data-ttu-id="361eb-110">Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="361eb-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="361eb-111">Faixas de números para um álbum começam em 1.</span><span class="sxs-lookup"><span data-stu-id="361eb-111">Track numbers for an album start at 1.</span></span>

<span data-ttu-id="361eb-112">**OriginalIndex** e **OriginalIndexLeft** são aliases para este atributo.</span><span class="sxs-lookup"><span data-stu-id="361eb-112">**OriginalIndex** and **OriginalIndexLeft** are aliases for this attribute.</span></span>

<span data-ttu-id="361eb-113">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMTrackNumber.</span><span class="sxs-lookup"><span data-stu-id="361eb-113">The Windows Media Format SDK constant for this attribute is g\_wszWMTrackNumber.</span></span>

<span data-ttu-id="361eb-114">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="361eb-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="361eb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="361eb-115">Requirements</span></span>



| <span data-ttu-id="361eb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="361eb-116">Requirement</span></span> | <span data-ttu-id="361eb-117">Valor</span><span class="sxs-lookup"><span data-stu-id="361eb-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="361eb-118">Versão</span><span class="sxs-lookup"><span data-stu-id="361eb-118">Version</span></span><br/> | <span data-ttu-id="361eb-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="361eb-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="361eb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="361eb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="361eb-121">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="361eb-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






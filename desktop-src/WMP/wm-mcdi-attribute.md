---
title: Atributo WM/MCDI
description: O atributo WM/MCDI é o identificador do CD de música do CD do qual o arquivo ou o controle foi copiado.
ms.assetid: f0bec14d-416c-477f-98df-dece0bf85ea4
keywords:
- Atributo WM/MCDI do Windows Media Player
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec51c306f94e25acb94155c4d87f1f1a8b95866
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773079"
---
# <a name="wmmcdi-attribute"></a><span data-ttu-id="a1c2a-104">Atributo WM/MCDI</span><span class="sxs-lookup"><span data-stu-id="a1c2a-104">WM/MCDI Attribute</span></span>

<span data-ttu-id="a1c2a-105">O atributo **WM/MCDI** é o identificador do CD de música do CD do qual o arquivo ou o controle foi copiado.</span><span class="sxs-lookup"><span data-stu-id="a1c2a-105">The **WM/MCDI** attribute is the music CD identifier of the CD from which the file or track was copied.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a1c2a-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="a1c2a-106">Applies To</span></span>

-   [<span data-ttu-id="a1c2a-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="a1c2a-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="a1c2a-108">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="a1c2a-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="a1c2a-109">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="a1c2a-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="a1c2a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1c2a-110">Remarks</span></span>

<span data-ttu-id="a1c2a-111">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="a1c2a-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="a1c2a-112">**TOC** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="a1c2a-112">**TOC** is an alias for this attribute.</span></span>

<span data-ttu-id="a1c2a-113">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMMCDI.</span><span class="sxs-lookup"><span data-stu-id="a1c2a-113">The Windows Media Format SDK constant for this attribute is g\_wszWMMCDI.</span></span>

<span data-ttu-id="a1c2a-114">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a1c2a-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1c2a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1c2a-115">Requirements</span></span>



| <span data-ttu-id="a1c2a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1c2a-116">Requirement</span></span> | <span data-ttu-id="a1c2a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a1c2a-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="a1c2a-118">Versão</span><span class="sxs-lookup"><span data-stu-id="a1c2a-118">Version</span></span><br/> | <span data-ttu-id="a1c2a-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="a1c2a-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1c2a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1c2a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c2a-121">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="a1c2a-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






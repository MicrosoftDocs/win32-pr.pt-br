---
title: Atributo WM/condutor
description: O atributo WM/condutor é o nome do condutor da música.
ms.assetid: 31c7d310-da6a-4c30-86b0-15defaee1743
keywords:
- Atributo do WM/condutor do Windows Media Player
topic_type:
- apiref
api_name:
- WM/Conductor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1ae08dfee807d130f04dd258c6af81a8d68057
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782557"
---
# <a name="wmconductor-attribute"></a><span data-ttu-id="84b52-104">Atributo WM/condutor</span><span class="sxs-lookup"><span data-stu-id="84b52-104">WM/Conductor Attribute</span></span>

<span data-ttu-id="84b52-105">O atributo **WM/condutor** é o nome do condutor da música.</span><span class="sxs-lookup"><span data-stu-id="84b52-105">The **WM/Conductor** attribute is the name of the conductor of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="84b52-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="84b52-106">Applies To</span></span>

-   [<span data-ttu-id="84b52-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="84b52-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="84b52-108">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="84b52-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="84b52-109">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="84b52-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="84b52-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="84b52-110">Remarks</span></span>

<span data-ttu-id="84b52-111">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="84b52-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="84b52-112">Esse atributo pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="84b52-112">This attribute may have multiple values.</span></span> <span data-ttu-id="84b52-113">Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar o método **Media. getItemInfoByType** , não o método **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="84b52-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="84b52-114">O **condutor** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="84b52-114">**Conductor** is an alias for this attribute.</span></span>

<span data-ttu-id="84b52-115">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMConductor.</span><span class="sxs-lookup"><span data-stu-id="84b52-115">The Windows Media Format SDK constant for this attribute is g\_wszWMConductor.</span></span>

<span data-ttu-id="84b52-116">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="84b52-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="84b52-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84b52-117">Requirements</span></span>



| <span data-ttu-id="84b52-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="84b52-118">Requirement</span></span> | <span data-ttu-id="84b52-119">Valor</span><span class="sxs-lookup"><span data-stu-id="84b52-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="84b52-120">Versão</span><span class="sxs-lookup"><span data-stu-id="84b52-120">Version</span></span><br/> | <span data-ttu-id="84b52-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="84b52-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84b52-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="84b52-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b52-123">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="84b52-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="84b52-124">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="84b52-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 






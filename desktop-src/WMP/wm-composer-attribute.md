---
title: Atributo do WM/Composer
description: O atributo WM/Composer é o nome do compositor da música.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- Atributo do WM/Composer do Windows Media Player
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793337"
---
# <a name="wmcomposer-attribute"></a><span data-ttu-id="f78f6-104">Atributo do WM/Composer</span><span class="sxs-lookup"><span data-stu-id="f78f6-104">WM/Composer Attribute</span></span>

<span data-ttu-id="f78f6-105">O atributo **WM/Composer** é o nome do compositor da música.</span><span class="sxs-lookup"><span data-stu-id="f78f6-105">The **WM/Composer** attribute is the name of the composer of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f78f6-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="f78f6-106">Applies To</span></span>

-   [<span data-ttu-id="f78f6-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="f78f6-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="f78f6-108">Playlists de CD</span><span class="sxs-lookup"><span data-stu-id="f78f6-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="f78f6-109">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="f78f6-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="f78f6-110">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="f78f6-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f78f6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f78f6-111">Remarks</span></span>

<span data-ttu-id="f78f6-112">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="f78f6-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="f78f6-113">Esse atributo pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="f78f6-113">This attribute may have multiple values.</span></span> <span data-ttu-id="f78f6-114">Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar o método **Media. getItemInfoByType** , não o método **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="f78f6-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="f78f6-115">O **Composer** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="f78f6-115">**Composer** is an alias for this attribute.</span></span>

<span data-ttu-id="f78f6-116">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMComposer.</span><span class="sxs-lookup"><span data-stu-id="f78f6-116">The Windows Media Format SDK constant for this attribute is g\_wszWMComposer.</span></span>

<span data-ttu-id="f78f6-117">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f78f6-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f78f6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f78f6-118">Requirements</span></span>



| <span data-ttu-id="f78f6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f78f6-119">Requirement</span></span> | <span data-ttu-id="f78f6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f78f6-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="f78f6-121">Versão</span><span class="sxs-lookup"><span data-stu-id="f78f6-121">Version</span></span><br/> | <span data-ttu-id="f78f6-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f78f6-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f78f6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f78f6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f78f6-124">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="f78f6-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="f78f6-125">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="f78f6-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 






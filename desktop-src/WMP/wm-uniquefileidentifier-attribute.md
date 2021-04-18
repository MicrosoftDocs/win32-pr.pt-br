---
title: Atributo WM/UniqueFileIdentifier
description: O atributo WM/UniqueFileIdentifier é uma cadeia de caracteres que identifica exclusivamente o item.
ms.assetid: 8196fc38-05dc-4c9e-98cb-1e160ce28a9a
keywords:
- Atributo WM/UniqueFileIdentifier do Windows Media Player
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a4297f299f6e7df64088066b3137d844a0c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751566"
---
# <a name="wmuniquefileidentifier-attribute"></a><span data-ttu-id="7372e-104">Atributo WM/UniqueFileIdentifier</span><span class="sxs-lookup"><span data-stu-id="7372e-104">WM/UniqueFileIdentifier Attribute</span></span>

<span data-ttu-id="7372e-105">O atributo **WM/UniqueFileIdentifier** é uma cadeia de caracteres que identifica exclusivamente o item.</span><span class="sxs-lookup"><span data-stu-id="7372e-105">The **WM/UniqueFileIdentifier** attribute is a string that uniquely identifies the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7372e-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="7372e-106">Applies To</span></span>

-   [<span data-ttu-id="7372e-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="7372e-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="7372e-108">Playlists de CD</span><span class="sxs-lookup"><span data-stu-id="7372e-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="7372e-109">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="7372e-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="7372e-110">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="7372e-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="7372e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7372e-111">Remarks</span></span>

<span data-ttu-id="7372e-112">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="7372e-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="7372e-113">**UniqueFileIdentifier** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="7372e-113">**UniqueFileIdentifier** is an alias for this attribute.</span></span>

<span data-ttu-id="7372e-114">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMUniqueFileIdentifier.</span><span class="sxs-lookup"><span data-stu-id="7372e-114">The Windows Media Format SDK constant for this attribute is g\_wszWMUniqueFileIdentifier.</span></span>

<span data-ttu-id="7372e-115">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="7372e-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7372e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7372e-116">Requirements</span></span>



| <span data-ttu-id="7372e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7372e-117">Requirement</span></span> | <span data-ttu-id="7372e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7372e-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="7372e-119">Versão</span><span class="sxs-lookup"><span data-stu-id="7372e-119">Version</span></span><br/> | <span data-ttu-id="7372e-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7372e-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7372e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="7372e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7372e-122">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="7372e-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






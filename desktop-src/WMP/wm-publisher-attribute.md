---
title: Atributo do WM/Publisher
description: O atributo WM/Publisher é o nome da empresa que publicou o conteúdo.
ms.assetid: 5f3aa5de-237e-449c-918e-8750481adc6f
keywords:
- Atributo do WM/Publisher do Windows Media Player
topic_type:
- apiref
api_name:
- WM/Publisher
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00bd0d2ab2b6d886639cffa1df0770dfe329f7f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790240"
---
# <a name="wmpublisher-attribute"></a><span data-ttu-id="555cc-104">Atributo do WM/Publisher</span><span class="sxs-lookup"><span data-stu-id="555cc-104">WM/Publisher Attribute</span></span>

<span data-ttu-id="555cc-105">O atributo **WM/Publisher** é o nome da empresa que publicou o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="555cc-105">The **WM/Publisher** attribute is the name of the company that published the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="555cc-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="555cc-106">Applies To</span></span>

-   [<span data-ttu-id="555cc-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="555cc-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="555cc-108">Playlists de CD</span><span class="sxs-lookup"><span data-stu-id="555cc-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="555cc-109">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="555cc-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="555cc-110">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="555cc-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="555cc-111">DVDs</span><span class="sxs-lookup"><span data-stu-id="555cc-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="555cc-112">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="555cc-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="555cc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="555cc-113">Remarks</span></span>

<span data-ttu-id="555cc-114">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="555cc-114">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="555cc-115">**Label**, **ReleasedBy** e **Studio** são aliases para este atributo.</span><span class="sxs-lookup"><span data-stu-id="555cc-115">**Label**, **ReleasedBy**, and **Studio** are aliases for this attribute.</span></span>

<span data-ttu-id="555cc-116">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMPublisher.</span><span class="sxs-lookup"><span data-stu-id="555cc-116">The Windows Media Format SDK constant for this attribute is g\_wszWMPublisher.</span></span>

<span data-ttu-id="555cc-117">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="555cc-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="555cc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="555cc-118">Requirements</span></span>



| <span data-ttu-id="555cc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="555cc-119">Requirement</span></span> | <span data-ttu-id="555cc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="555cc-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="555cc-121">Versão</span><span class="sxs-lookup"><span data-stu-id="555cc-121">Version</span></span><br/> | <span data-ttu-id="555cc-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="555cc-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="555cc-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="555cc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="555cc-124">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="555cc-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






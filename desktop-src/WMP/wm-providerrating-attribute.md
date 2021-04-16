---
title: Atributo WM/ProviderRating
description: O atributo WM/ProviderRating é a classificação do item atribuído pelo provedor dos valores de atributo.
ms.assetid: a1a76560-a8d9-486a-badc-56d7bf488c10
keywords:
- Atributo WM/ProviderRating do Windows Media Player
topic_type:
- apiref
api_name:
- WM/ProviderRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0f71985d948e59b8c0f98d50445a48263d67cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765346"
---
# <a name="wmproviderrating-attribute"></a><span data-ttu-id="639ec-104">Atributo WM/ProviderRating</span><span class="sxs-lookup"><span data-stu-id="639ec-104">WM/ProviderRating Attribute</span></span>

<span data-ttu-id="639ec-105">O atributo **WM/ProviderRating** é a classificação do item atribuído pelo provedor dos valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="639ec-105">The **WM/ProviderRating** attribute is the rating of the item assigned by the provider of the attribute values.</span></span>

## <a name="applies-to"></a><span data-ttu-id="639ec-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="639ec-106">Applies To</span></span>

-   [<span data-ttu-id="639ec-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="639ec-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="639ec-108">Playlists de CD</span><span class="sxs-lookup"><span data-stu-id="639ec-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="639ec-109">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="639ec-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="639ec-110">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="639ec-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="639ec-111">DVDs</span><span class="sxs-lookup"><span data-stu-id="639ec-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="639ec-112">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="639ec-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="639ec-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="639ec-113">Remarks</span></span>

<span data-ttu-id="639ec-114">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="639ec-114">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="639ec-115">A **classificação** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="639ec-115">**Rating** is an alias for this attribute.</span></span>

<span data-ttu-id="639ec-116">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMProviderRating.</span><span class="sxs-lookup"><span data-stu-id="639ec-116">The Windows Media Format SDK constant for this attribute is g\_wszWMProviderRating.</span></span>

<span data-ttu-id="639ec-117">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="639ec-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="639ec-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="639ec-118">Requirements</span></span>



| <span data-ttu-id="639ec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="639ec-119">Requirement</span></span> | <span data-ttu-id="639ec-120">Valor</span><span class="sxs-lookup"><span data-stu-id="639ec-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="639ec-121">Versão</span><span class="sxs-lookup"><span data-stu-id="639ec-121">Version</span></span><br/> | <span data-ttu-id="639ec-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="639ec-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="639ec-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="639ec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639ec-124">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="639ec-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






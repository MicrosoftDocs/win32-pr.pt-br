---
title: Atributo do WM/provedor
description: O atributo WM/Provider é o nome do provedor dos valores de atributo.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- Atributo do WM/provedor do Windows Media Player
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c2c1c796edf28a567f72708c60c7976f718bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793359"
---
# <a name="wmprovider-attribute"></a><span data-ttu-id="dabe0-104">Atributo do WM/provedor</span><span class="sxs-lookup"><span data-stu-id="dabe0-104">WM/Provider Attribute</span></span>

<span data-ttu-id="dabe0-105">O atributo **WM/Provider** é o nome do provedor dos valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="dabe0-105">The **WM/Provider** attribute is the name of the provider of the attribute values.</span></span>

## <a name="applies-to"></a><span data-ttu-id="dabe0-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="dabe0-106">Applies To</span></span>

-   [<span data-ttu-id="dabe0-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="dabe0-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="dabe0-108">Playlists de CD</span><span class="sxs-lookup"><span data-stu-id="dabe0-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="dabe0-109">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="dabe0-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="dabe0-110">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="dabe0-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="dabe0-111">Itens de rádio</span><span class="sxs-lookup"><span data-stu-id="dabe0-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="dabe0-112">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="dabe0-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="dabe0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="dabe0-113">Remarks</span></span>

<span data-ttu-id="dabe0-114">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="dabe0-114">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="dabe0-115">O **MetadataName** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="dabe0-115">**MetadataSource** is an alias for this attribute.</span></span>

<span data-ttu-id="dabe0-116">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMProvider.</span><span class="sxs-lookup"><span data-stu-id="dabe0-116">The Windows Media Format SDK constant for this attribute is g\_wszWMProvider.</span></span>

<span data-ttu-id="dabe0-117">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="dabe0-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dabe0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dabe0-118">Requirements</span></span>



| <span data-ttu-id="dabe0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dabe0-119">Requirement</span></span> | <span data-ttu-id="dabe0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dabe0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dabe0-121">Versão</span><span class="sxs-lookup"><span data-stu-id="dabe0-121">Version</span></span><br/> | <span data-ttu-id="dabe0-122">Windows Media Player 9 Series ou posterior (o item de foto tem suporte apenas no Windows Media Player 10 ou posterior)</span><span class="sxs-lookup"><span data-stu-id="dabe0-122">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dabe0-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="dabe0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dabe0-124">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="dabe0-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






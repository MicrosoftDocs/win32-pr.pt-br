---
title: Atributo do WM/Provedorstyle
description: O atributo WM/Providerstyle é o estilo do item atribuído pelo provedor dos valores de atributo.
ms.assetid: 43994d6b-0d71-4f2c-834a-47bbcd32b461
keywords:
- Atributo do WM/Provedorstyle Windows Media Player
topic_type:
- apiref
api_name:
- WM/ProviderStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a18af02254e7ce476ffc9c1e427465966cd66c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780332"
---
# <a name="wmproviderstyle-attribute"></a><span data-ttu-id="6c22d-104">Atributo do WM/Provedorstyle</span><span class="sxs-lookup"><span data-stu-id="6c22d-104">WM/ProviderStyle Attribute</span></span>

<span data-ttu-id="6c22d-105">O atributo **WM/providerstyle** é o estilo do item atribuído pelo provedor dos valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="6c22d-105">The **WM/ProviderStyle** attribute is the style of the item assigned by the provider of the attribute values.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6c22d-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="6c22d-106">Applies To</span></span>

-   [<span data-ttu-id="6c22d-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="6c22d-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="6c22d-108">Playlists de CD</span><span class="sxs-lookup"><span data-stu-id="6c22d-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="6c22d-109">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="6c22d-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="6c22d-110">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="6c22d-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="6c22d-111">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="6c22d-111">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6c22d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c22d-112">Remarks</span></span>

<span data-ttu-id="6c22d-113">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="6c22d-113">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="6c22d-114">O **estilo** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="6c22d-114">**Style** is an alias for this attribute.</span></span>

<span data-ttu-id="6c22d-115">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMProviderStyle.</span><span class="sxs-lookup"><span data-stu-id="6c22d-115">The Windows Media Format SDK constant for this attribute is g\_wszWMProviderStyle.</span></span>

<span data-ttu-id="6c22d-116">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6c22d-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c22d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c22d-117">Requirements</span></span>



| <span data-ttu-id="6c22d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c22d-118">Requirement</span></span> | <span data-ttu-id="6c22d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6c22d-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="6c22d-120">Versão</span><span class="sxs-lookup"><span data-stu-id="6c22d-120">Version</span></span><br/> | <span data-ttu-id="6c22d-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="6c22d-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c22d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c22d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c22d-123">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="6c22d-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






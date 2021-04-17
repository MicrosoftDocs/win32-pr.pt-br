---
title: Atributo WM/MediaClassSecondaryID
description: O atributo WM/MediaClassSecondaryID é um GUID que especifica a classe de mídia secundária, que é uma subclasse da classe de mídia primária.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Atributo WM/MediaClassSecondaryID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797985"
---
# <a name="wmmediaclasssecondaryid-attribute"></a><span data-ttu-id="7c0cc-104">Atributo WM/MediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="7c0cc-104">WM/MediaClassSecondaryID Attribute</span></span>

<span data-ttu-id="7c0cc-105">O atributo **WM/MediaClassSecondaryID** é um GUID que especifica a classe de mídia secundária, que é uma subclasse da classe de mídia primária.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-105">The **WM/MediaClassSecondaryID** attribute is a GUID specifying the secondary media class, which is a subclass of the primary media class.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7c0cc-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="7c0cc-106">Applies To</span></span>

-   [<span data-ttu-id="7c0cc-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="7c0cc-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="7c0cc-108">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="7c0cc-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="7c0cc-109">Outros itens</span><span class="sxs-lookup"><span data-stu-id="7c0cc-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="7c0cc-110">Itens de foto</span><span class="sxs-lookup"><span data-stu-id="7c0cc-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="7c0cc-111">Playlists</span><span class="sxs-lookup"><span data-stu-id="7c0cc-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="7c0cc-112">Itens de rádio</span><span class="sxs-lookup"><span data-stu-id="7c0cc-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="7c0cc-113">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="7c0cc-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="7c0cc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c0cc-114">Remarks</span></span>

<span data-ttu-id="7c0cc-115">Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="7c0cc-116">A tabela a seguir lista os GUIDs com suporte e suas descrições.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-116">The following table lists the supported GUIDs and their descriptions.</span></span>



| <span data-ttu-id="7c0cc-117">GUID</span><span class="sxs-lookup"><span data-stu-id="7c0cc-117">GUID</span></span>                                 | <span data-ttu-id="7c0cc-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c0cc-118">Description</span></span>                                    |
|--------------------------------------|------------------------------------------------|
| <span data-ttu-id="7c0cc-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span><span class="sxs-lookup"><span data-stu-id="7c0cc-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span></span> | <span data-ttu-id="7c0cc-120">O objeto de mídia representa uma lista de reprodução estática.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-120">The media object represents a static playlist.</span></span> |
| <span data-ttu-id="7c0cc-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span><span class="sxs-lookup"><span data-stu-id="7c0cc-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span></span> | <span data-ttu-id="7c0cc-122">O objeto de mídia representa uma lista de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-122">The media object represents an auto playlist.</span></span>  |



 

<span data-ttu-id="7c0cc-123">**MediaClassSecondaryID** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-123">**MediaClassSecondaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="7c0cc-124">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMMediaClassSecondaryID.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-124">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassSecondaryID.</span></span>

<span data-ttu-id="7c0cc-125">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="7c0cc-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c0cc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c0cc-126">Requirements</span></span>



| <span data-ttu-id="7c0cc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c0cc-127">Requirement</span></span> | <span data-ttu-id="7c0cc-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7c0cc-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0cc-129">Versão</span><span class="sxs-lookup"><span data-stu-id="7c0cc-129">Version</span></span><br/> | <span data-ttu-id="7c0cc-130">O item de foto tem suporte apenas no Windows Media Player 10 ou posterior. o item de rádio só tem suporte no Windows Media Player 9 Series todos os outros itens têm suporte no Windows Media Player 9 Series e posteriores</span><span class="sxs-lookup"><span data-stu-id="7c0cc-130">The photo item is supported only in Windows Media Player 10 or later The radio item is supported only in Windows Media Player 9 Series All other items are supported in Windows Media Player 9 Series and later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c0cc-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c0cc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0cc-132">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="7c0cc-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






---
title: Objeto de mídia
description: O objeto de mídia fornece uma maneira de especificar ou recuperar propriedades de um item de mídia, usando as propriedades e os métodos a seguir.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Objeto de mídia Windows Media Player
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88eff6ee0a97e63df6a0c073ef18425cbb576e85
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105785011"
---
# <a name="media-object"></a><span data-ttu-id="2cfa2-104">Objeto de mídia</span><span class="sxs-lookup"><span data-stu-id="2cfa2-104">Media Object</span></span>

<span data-ttu-id="2cfa2-105">O objeto de **mídia** fornece uma maneira de especificar ou recuperar propriedades de um item de mídia, usando as propriedades e os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-105">The **Media** object provides a way to specify or retrieve properties of a media item, using the following properties and methods.</span></span>

<span data-ttu-id="2cfa2-106">O objeto de **mídia** dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-106">The **Media** object supports the following properties.</span></span>



| <span data-ttu-id="2cfa2-107">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2cfa2-107">Property</span></span>                                         | <span data-ttu-id="2cfa2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2cfa2-108">Description</span></span>                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cfa2-109">attributeCount</span><span class="sxs-lookup"><span data-stu-id="2cfa2-109">attributeCount</span></span>](media-attributecount.md)       | <span data-ttu-id="2cfa2-110">Recupera o número de atributos que podem ser consultados e/ou definidos para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-110">Retrieves the number of attributes that can be queried and/or set for the media item.</span></span>              |
| [<span data-ttu-id="2cfa2-111">duration</span><span class="sxs-lookup"><span data-stu-id="2cfa2-111">duration</span></span>](media-duration.md)                   | <span data-ttu-id="2cfa2-112">Recupera a duração em segundos do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-112">Retrieves the duration in seconds of the current media item.</span></span>                                       |
| [<span data-ttu-id="2cfa2-113">duraçãostring</span><span class="sxs-lookup"><span data-stu-id="2cfa2-113">durationString</span></span>](media-durationstring.md)       | <span data-ttu-id="2cfa2-114">Recupera um valor de **cadeia de caracteres** que indica a duração do item de mídia atual no formato hh: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-114">Retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span> |
| [<span data-ttu-id="2cfa2-115">error</span><span class="sxs-lookup"><span data-stu-id="2cfa2-115">error</span></span>](media-error.md)                         | <span data-ttu-id="2cfa2-116">Recupera um objeto [ErrorItem](erroritem-object.md) se o item de mídia tiver uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-116">Retrieves an [ErrorItem](erroritem-object.md) object if the media item has an error condition.</span></span>    |
| [<span data-ttu-id="2cfa2-117">imageSourceHeight</span><span class="sxs-lookup"><span data-stu-id="2cfa2-117">imageSourceHeight</span></span>](media-imagesourceheight.md) | <span data-ttu-id="2cfa2-118">Recupera a altura do item de mídia atual em pixels.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-118">Retrieves the height of the current media item in pixels.</span></span>                                          |
| [<span data-ttu-id="2cfa2-119">imageSourceWidth</span><span class="sxs-lookup"><span data-stu-id="2cfa2-119">imageSourceWidth</span></span>](media-imagesourcewidth.md)   | <span data-ttu-id="2cfa2-120">Recupera a largura do item de mídia atual em pixels.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-120">Retrieves the width of the current media item in pixels.</span></span>                                           |
| [<span data-ttu-id="2cfa2-121">markerCount</span><span class="sxs-lookup"><span data-stu-id="2cfa2-121">markerCount</span></span>](media-markercount.md)             | <span data-ttu-id="2cfa2-122">Recupera o número de marcadores no item de mídia.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-122">Retrieves the number of markers in the media item.</span></span>                                                 |
| [<span data-ttu-id="2cfa2-123">name</span><span class="sxs-lookup"><span data-stu-id="2cfa2-123">name</span></span>](media-name.md)                           | <span data-ttu-id="2cfa2-124">Especifica ou recupera o nome do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-124">Specifies or retrieves the name of the media item.</span></span>                                                 |
| [<span data-ttu-id="2cfa2-125">sourceURL</span><span class="sxs-lookup"><span data-stu-id="2cfa2-125">sourceURL</span></span>](media-sourceurl.md)                 | <span data-ttu-id="2cfa2-126">Recupera a URL do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-126">Retrieves the URL of the media item.</span></span>                                                               |



 

<span data-ttu-id="2cfa2-127">O objeto de **mídia** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-127">The **Media** object supports the following methods.</span></span>



| <span data-ttu-id="2cfa2-128">Método</span><span class="sxs-lookup"><span data-stu-id="2cfa2-128">Method</span></span>                                                       | <span data-ttu-id="2cfa2-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="2cfa2-129">Description</span></span>                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cfa2-130">getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="2cfa2-130">getAttributeCountByType</span></span>](media-getattributecountbytype.md) | <span data-ttu-id="2cfa2-131">Recupera o número de atributos associados ao nome do atributo e idioma especificados.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-131">Retrieves the number of attributes associated with the specified attribute name and language.</span></span>            |
| [<span data-ttu-id="2cfa2-132">GetAttributeName</span><span class="sxs-lookup"><span data-stu-id="2cfa2-132">getAttributeName</span></span>](media-getattributename.md)               | <span data-ttu-id="2cfa2-133">Recupera o nome do atributo correspondente ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-133">Retrieves the name of the attribute corresponding to the specified index.</span></span>                                |
| [<span data-ttu-id="2cfa2-134">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="2cfa2-134">getItemInfo</span></span>](media-getiteminfo.md)                         | <span data-ttu-id="2cfa2-135">Recupera o valor do atributo especificado para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-135">Retrieves the value of the specified attribute for the media item.</span></span>                                       |
| [<span data-ttu-id="2cfa2-136">getItemInfoByAtom</span><span class="sxs-lookup"><span data-stu-id="2cfa2-136">getItemInfoByAtom</span></span>](media-getiteminfobyatom.md)             | <span data-ttu-id="2cfa2-137">Recupera o valor do atributo com o número de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-137">Retrieves the value of the attribute with the specified index number.</span></span>                                    |
| [<span data-ttu-id="2cfa2-138">getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="2cfa2-138">getItemInfoByType</span></span>](media-getiteminfobytype.md)             | <span data-ttu-id="2cfa2-139">Recupera o valor do atributo correspondente ao nome do atributo, idioma e índice especificados.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-139">Retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span> |
| [<span data-ttu-id="2cfa2-140">Getmarkname</span><span class="sxs-lookup"><span data-stu-id="2cfa2-140">getMarkerName</span></span>](media-getmarkername.md)                     | <span data-ttu-id="2cfa2-141">Recupera o nome do marcador no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-141">Retrieves the name of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="2cfa2-142">getmarcadortime</span><span class="sxs-lookup"><span data-stu-id="2cfa2-142">getMarkerTime</span></span>](media-getmarkertime.md)                     | <span data-ttu-id="2cfa2-143">Recupera a hora do marcador no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-143">Retrieves the time of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="2cfa2-144">isidêntico</span><span class="sxs-lookup"><span data-stu-id="2cfa2-144">isIdentical</span></span>](media-isidentical.md)                         | <span data-ttu-id="2cfa2-145">Recupera um valor que indica se o objeto fornecido é o mesmo que o atual.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-145">Retrieves a value indicating whether the supplied object is the same as the current one.</span></span>                 |
| [<span data-ttu-id="2cfa2-146">isMemberOf</span><span class="sxs-lookup"><span data-stu-id="2cfa2-146">isMemberOf</span></span>](media-ismemberof.md)                           | <span data-ttu-id="2cfa2-147">Recupera um valor que indica se o item de mídia especificado é um membro da playlist especificada.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-147">Retrieves a value indicating whether the specified media item is a member of the specified playlist.</span></span>     |
| [<span data-ttu-id="2cfa2-148">isReadOnlyItem</span><span class="sxs-lookup"><span data-stu-id="2cfa2-148">isReadOnlyItem</span></span>](media-isreadonlyitem.md)                   | <span data-ttu-id="2cfa2-149">Recupera um valor que indica se os atributos do item de mídia especificado podem ser editados.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-149">Retrieves a value indicating whether the attributes of the specified media item can be edited.</span></span>           |
| [<span data-ttu-id="2cfa2-150">setItemInfo</span><span class="sxs-lookup"><span data-stu-id="2cfa2-150">setItemInfo</span></span>](media-setiteminfo.md)                         | <span data-ttu-id="2cfa2-151">Define o valor do atributo especificado para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-151">Sets the value of the specified attribute for the media item.</span></span>                                            |



 

<span data-ttu-id="2cfa2-152">O objeto de **mídia** é acessado por meio das propriedades e métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-152">The **Media** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="2cfa2-153">Objeto</span><span class="sxs-lookup"><span data-stu-id="2cfa2-153">Object</span></span>                          | <span data-ttu-id="2cfa2-154">Propriedade ou método</span><span class="sxs-lookup"><span data-stu-id="2cfa2-154">Property or method</span></span>                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="2cfa2-155">Controles</span><span class="sxs-lookup"><span data-stu-id="2cfa2-155">Controls</span></span>](controls-object.md) | [<span data-ttu-id="2cfa2-156">currentItem</span><span class="sxs-lookup"><span data-stu-id="2cfa2-156">currentItem</span></span>](controls-currentitem.md)                                  |
| [<span data-ttu-id="2cfa2-157">Jogador</span><span class="sxs-lookup"><span data-stu-id="2cfa2-157">Player</span></span>](player-object.md)     | <span data-ttu-id="2cfa2-158">[currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="2cfa2-158">[currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md)</span></span> |
| [<span data-ttu-id="2cfa2-159">7.1</span><span class="sxs-lookup"><span data-stu-id="2cfa2-159">Playlist</span></span>](playlist-object.md) | [<span data-ttu-id="2cfa2-160">item</span><span class="sxs-lookup"><span data-stu-id="2cfa2-160">item</span></span>](playlist-item.md)                                                |



 

<span data-ttu-id="2cfa2-161">Porque é o meio mais comum de acesso, *Player*. **currentMedia** é usado para fins de ilustração nas seções de sintaxe de referência.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-161">Because it is the most common means of access, *player*.**currentMedia** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="2cfa2-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cfa2-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cfa2-163">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="2cfa2-163">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





---
title: Media. sourceURL
description: A propriedade sourceURL recupera a URL do item de mídia.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media. sourceURL Windows Media Player
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783739"
---
# <a name="mediasourceurl"></a><span data-ttu-id="68449-104">Media. sourceURL</span><span class="sxs-lookup"><span data-stu-id="68449-104">Media.sourceURL</span></span>

<span data-ttu-id="68449-105">A propriedade **sourceURL** recupera a URL do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="68449-105">The **sourceURL** property retrieves the URL of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="68449-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="68449-106">Syntax</span></span>

<span data-ttu-id="68449-107">*Player*. *currentMedia*. sourceURL</span><span class="sxs-lookup"><span data-stu-id="68449-107">*player*.*currentMedia*.sourceURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="68449-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="68449-108">Possible Values</span></span>

<span data-ttu-id="68449-109">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="68449-109">This property is a read-only **String**.</span></span>

## <a name="examples"></a><span data-ttu-id="68449-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="68449-110">Examples</span></span>

<span data-ttu-id="68449-111">O exemplo de JScript a seguir usa *mídia*. **sourceURL** para recuperar a URL do primeiro item de mídia na playlist de exemplo; a URL do item de mídia é atribuída à propriedade **URL** do objeto Player.</span><span class="sxs-lookup"><span data-stu-id="68449-111">The following JScript example uses *Media*.**sourceURL** to retrieve the URL of the first media item in the sample playlist; the URL of the media item is then assigned to the player object **URL** property.</span></span> <span data-ttu-id="68449-112">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="68449-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="68449-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68449-113">Requirements</span></span>



| <span data-ttu-id="68449-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="68449-114">Requirement</span></span> | <span data-ttu-id="68449-115">Valor</span><span class="sxs-lookup"><span data-stu-id="68449-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68449-116">Versão</span><span class="sxs-lookup"><span data-stu-id="68449-116">Version</span></span><br/> | <span data-ttu-id="68449-117">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="68449-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="68449-118">DLL</span><span class="sxs-lookup"><span data-stu-id="68449-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="68449-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68449-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68449-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="68449-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68449-121">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="68449-121">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 






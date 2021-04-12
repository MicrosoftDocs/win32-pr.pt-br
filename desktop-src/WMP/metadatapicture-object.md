---
title: Objeto MetadataPicture
description: O objeto MetadataPicture fornece uma maneira de recuperar os valores do atributo de metadados do WM/Picture. Esse atributo corresponde à arte do álbum contida em um arquivo de mídia digital, não à arte do álbum baixada pela Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Objeto MetadataPicture Windows Media Player
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454269"
---
# <a name="metadatapicture-object"></a><span data-ttu-id="7c29e-105">Objeto MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="7c29e-105">MetadataPicture Object</span></span>

<span data-ttu-id="7c29e-106">O objeto **MetadataPicture** fornece uma maneira de recuperar os valores do atributo de metadados do [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) .</span><span class="sxs-lookup"><span data-stu-id="7c29e-106">The **MetadataPicture** object provides a way to retrieve the values of the [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) metadata attribute.</span></span> <span data-ttu-id="7c29e-107">Esse atributo corresponde à arte do álbum contida em um arquivo de mídia digital, não à arte do álbum baixada pela Internet.</span><span class="sxs-lookup"><span data-stu-id="7c29e-107">This attribute corresponds to album art contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="7c29e-108">O objeto **MetadataPicture** dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="7c29e-108">The **MetadataPicture** object supports the following properties.</span></span>



| <span data-ttu-id="7c29e-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7c29e-109">Property</span></span>                                           | <span data-ttu-id="7c29e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c29e-110">Description</span></span>                                       |
|----------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="7c29e-111">**ndescrição**</span><span class="sxs-lookup"><span data-stu-id="7c29e-111">**description**</span></span>](metadatapicture-description.md) | <span data-ttu-id="7c29e-112">Recupera uma descrição da imagem de metadados.</span><span class="sxs-lookup"><span data-stu-id="7c29e-112">Retrieves a description of the metadata image.</span></span>    |
| [<span data-ttu-id="7c29e-113">**MIME**</span><span class="sxs-lookup"><span data-stu-id="7c29e-113">**mimeType**</span></span>](metadatapicture-mimetype.md)       | <span data-ttu-id="7c29e-114">Recupera o tipo MIME da imagem de metadados.</span><span class="sxs-lookup"><span data-stu-id="7c29e-114">Retrieves the MIME type of the metadata image.</span></span>    |
| [<span data-ttu-id="7c29e-115">**TipoDeFigura**</span><span class="sxs-lookup"><span data-stu-id="7c29e-115">**pictureType**</span></span>](metadatapicture-picturetype.md) | <span data-ttu-id="7c29e-116">Recupera o tipo de imagem da imagem de metadados.</span><span class="sxs-lookup"><span data-stu-id="7c29e-116">Retrieves the picture type of the metadata image.</span></span> |
| [<span data-ttu-id="7c29e-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="7c29e-117">**URL**</span></span>](metadatapicture-url.md)                 | <span data-ttu-id="7c29e-118">Somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="7c29e-118">Internal use only.</span></span>                                |



 

<span data-ttu-id="7c29e-119">O objeto **MetadataPicture** é acessado por meio do método a seguir.</span><span class="sxs-lookup"><span data-stu-id="7c29e-119">The **MetadataPicture** object is accessed through the following method.</span></span>



| <span data-ttu-id="7c29e-120">Objeto</span><span class="sxs-lookup"><span data-stu-id="7c29e-120">Object</span></span>                        | <span data-ttu-id="7c29e-121">Método</span><span class="sxs-lookup"><span data-stu-id="7c29e-121">Method</span></span>                                               |
|-------------------------------|------------------------------------------------------|
| [<span data-ttu-id="7c29e-122">**Mídia**</span><span class="sxs-lookup"><span data-stu-id="7c29e-122">**Media**</span></span>](media-object.md) | [<span data-ttu-id="7c29e-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="7c29e-123">**getItemInfoByType**</span></span>](media-getiteminfobytype.md) |



 

<span data-ttu-id="7c29e-124">Para fins de ilustração, `player.currentMedia.getItemInfoByType(name, language, index)` é usado nas seções de sintaxe de referência.</span><span class="sxs-lookup"><span data-stu-id="7c29e-124">For purposes of illustration, `player.currentMedia.getItemInfoByType(name, language, index)` is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c29e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c29e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c29e-126">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="7c29e-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 
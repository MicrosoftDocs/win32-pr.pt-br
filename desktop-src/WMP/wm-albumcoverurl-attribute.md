---
title: Atributo WM/AlbumCoverURL
description: O atributo WM/AlbumCoverURL é o Uniform Resource Locator (URL) para arte de álbum ou uma imagem em miniatura.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- Atributo WM/AlbumCoverURL do Windows Media Player
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813745"
---
# <a name="wmalbumcoverurl-attribute"></a><span data-ttu-id="43ec4-104">Atributo WM/AlbumCoverURL</span><span class="sxs-lookup"><span data-stu-id="43ec4-104">WM/AlbumCoverURL Attribute</span></span>

<span data-ttu-id="43ec4-105">O atributo **WM/AlbumCoverURL** é o Uniform Resource Locator (URL) para arte de álbum ou uma imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="43ec4-105">The **WM/AlbumCoverURL** attribute is the uniform resource locator (URL) for album art or a thumbnail image.</span></span>

## <a name="applies-to"></a><span data-ttu-id="43ec4-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="43ec4-106">Applies To</span></span>

-   [<span data-ttu-id="43ec4-107">**Itens de áudio**</span><span class="sxs-lookup"><span data-stu-id="43ec4-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="43ec4-108">**Itens de foto**</span><span class="sxs-lookup"><span data-stu-id="43ec4-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="43ec4-109">**Itens de vídeo**</span><span class="sxs-lookup"><span data-stu-id="43ec4-109">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="43ec4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="43ec4-110">Remarks</span></span>

<span data-ttu-id="43ec4-111">Para um item de áudio, esse atributo é a URL da arte do álbum.</span><span class="sxs-lookup"><span data-stu-id="43ec4-111">For an audio item, this attribute is the URL of the album art.</span></span> <span data-ttu-id="43ec4-112">Para um item de foto ou de vídeo, esse atributo é a URL de uma imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="43ec4-112">For a photo or video item, this attribute is the URL of a thumbnail image.</span></span>

<span data-ttu-id="43ec4-113">Este atributo não está disponível para itens de mídia na biblioteca local do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="43ec4-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="43ec4-114">Ele está disponível somente para itens de mídia que pertencem a uma biblioteca remota; ou seja, uma biblioteca que foi disponibilizada por outro usuário na rede doméstica.</span><span class="sxs-lookup"><span data-stu-id="43ec4-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="43ec4-115">Para determinar se uma biblioteca de mídia é remota, chame o [**\_ tipo IWMPLibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="43ec4-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="43ec4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43ec4-116">Requirements</span></span>



| <span data-ttu-id="43ec4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="43ec4-117">Requirement</span></span> | <span data-ttu-id="43ec4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="43ec4-118">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="43ec4-119">Versão</span><span class="sxs-lookup"><span data-stu-id="43ec4-119">Version</span></span><br/> | <span data-ttu-id="43ec4-120">Windows Media Player 12 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="43ec4-120">Windows Media Player 12 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43ec4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="43ec4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ec4-122">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="43ec4-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






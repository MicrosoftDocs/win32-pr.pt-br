---
title: Atributo AlternateSourceURL
description: O atributo AlternateSourceURL é um localizador de recursos uniforme para o item de mídia que serve como uma alternativa para os atributos DLNASourceURI e SourceURL.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Atributo AlternateSourceURL Windows Media Player
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574a355dfa862c4db004fa2df942e464934a38ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810593"
---
# <a name="alternatesourceurl-attribute"></a><span data-ttu-id="f4eaa-104">Atributo AlternateSourceURL</span><span class="sxs-lookup"><span data-stu-id="f4eaa-104">AlternateSourceURL Attribute</span></span>

<span data-ttu-id="f4eaa-105">O atributo **AlternateSourceURL** é um localizador de recursos uniforme para o item de mídia que serve como uma alternativa para os atributos [**DLNASourceURI**](dlnasourceuri-attribute.md) e [**SourceURL**](sourceurl-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="f4eaa-105">The **AlternateSourceURL** attribute is a uniform resource locator for the media item that serves as an alternative to the [**DLNASourceURI**](dlnasourceuri-attribute.md) and [**SourceURL**](sourceurl-attribute.md) attributes.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f4eaa-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="f4eaa-106">Applies To</span></span>

-   [<span data-ttu-id="f4eaa-107">**Itens de áudio**</span><span class="sxs-lookup"><span data-stu-id="f4eaa-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="f4eaa-108">**Itens de foto**</span><span class="sxs-lookup"><span data-stu-id="f4eaa-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="f4eaa-109">**Itens da lista de reprodução**</span><span class="sxs-lookup"><span data-stu-id="f4eaa-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="f4eaa-110">**Itens de vídeo**</span><span class="sxs-lookup"><span data-stu-id="f4eaa-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f4eaa-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4eaa-111">Remarks</span></span>

<span data-ttu-id="f4eaa-112">Este atributo não está disponível para itens de mídia na biblioteca local do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="f4eaa-113">Ele está disponível somente para itens de mídia que pertencem a uma biblioteca remota; ou seja, uma biblioteca que foi disponibilizada por outro usuário na rede doméstica.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="f4eaa-114">Para determinar se uma biblioteca de mídia é remota, chame o [**\_ tipo IWMPLibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="f4eaa-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4eaa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4eaa-115">Requirements</span></span>



| <span data-ttu-id="f4eaa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4eaa-116">Requirement</span></span> | <span data-ttu-id="f4eaa-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f4eaa-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="f4eaa-118">Versão</span><span class="sxs-lookup"><span data-stu-id="f4eaa-118">Version</span></span><br/> | <span data-ttu-id="f4eaa-119">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="f4eaa-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4eaa-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4eaa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4eaa-121">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="f4eaa-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






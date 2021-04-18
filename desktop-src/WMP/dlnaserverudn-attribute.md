---
title: Atributo DLNAServerUDN
description: O atributo DLNAServerUDN é o nome de dispositivo exclusivo do servidor que hospeda o item de mídia.
ms.assetid: 1965731d-1b6e-4d76-a983-fd57c851fcfb
keywords:
- Atributo DLNAServerUDN Windows Media Player
topic_type:
- apiref
api_name:
- DLNAServerUDN Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa121df7a4f312e3cb00519d2ac4f519f844d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810563"
---
# <a name="dlnaserverudn-attribute"></a><span data-ttu-id="64dbb-104">Atributo DLNAServerUDN</span><span class="sxs-lookup"><span data-stu-id="64dbb-104">DLNAServerUDN Attribute</span></span>

<span data-ttu-id="64dbb-105">O atributo **DLNAServerUDN** é o nome de dispositivo exclusivo do servidor que hospeda o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="64dbb-105">The **DLNAServerUDN** attribute is the unique device name of the server that hosts the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="64dbb-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="64dbb-106">Applies To</span></span>

-   [<span data-ttu-id="64dbb-107">**Itens de áudio**</span><span class="sxs-lookup"><span data-stu-id="64dbb-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="64dbb-108">**Itens de foto**</span><span class="sxs-lookup"><span data-stu-id="64dbb-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="64dbb-109">**Itens da lista de reprodução**</span><span class="sxs-lookup"><span data-stu-id="64dbb-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="64dbb-110">**Itens de vídeo**</span><span class="sxs-lookup"><span data-stu-id="64dbb-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="64dbb-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="64dbb-111">Remarks</span></span>

<span data-ttu-id="64dbb-112">Este atributo não está disponível para itens de mídia na biblioteca local do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="64dbb-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="64dbb-113">Ele está disponível somente para itens de mídia que pertencem a uma biblioteca remota; ou seja, uma biblioteca que foi disponibilizada por outro usuário na rede doméstica.</span><span class="sxs-lookup"><span data-stu-id="64dbb-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="64dbb-114">Para determinar se uma biblioteca de mídia é remota, chame o [**\_ tipo IWMPLibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="64dbb-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="64dbb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64dbb-115">Requirements</span></span>



| <span data-ttu-id="64dbb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="64dbb-116">Requirement</span></span> | <span data-ttu-id="64dbb-117">Valor</span><span class="sxs-lookup"><span data-stu-id="64dbb-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="64dbb-118">Versão</span><span class="sxs-lookup"><span data-stu-id="64dbb-118">Version</span></span><br/> | <span data-ttu-id="64dbb-119">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="64dbb-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64dbb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="64dbb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64dbb-121">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="64dbb-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






---
title: Atributo DTCPIPHost
description: O atributo DTCPIPHost é o nome ou o endereço IP do computador ou dispositivo que deve ser contatado para a transmissão digital Proteção de Conteúdo via RIAR (troca de chave autenticada) do DTCP (Internet Protocol) para o item de mídia.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- Atributo DTCPIPHost Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9983cac920f2d11b9040e03af30e10b9c0c3fbcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813170"
---
# <a name="dtcpiphost-attribute"></a><span data-ttu-id="29c33-104">Atributo DTCPIPHost</span><span class="sxs-lookup"><span data-stu-id="29c33-104">DTCPIPHost Attribute</span></span>

<span data-ttu-id="29c33-105">O atributo **DTCPIPHost** é o nome ou o endereço IP do computador ou dispositivo que deve ser contatado para a transmissão digital proteção de conteúdo via RIAR (troca de chave autenticada) do DTCP (Internet Protocol) para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="29c33-105">The **DTCPIPHost** attribute is the name or IP address of the computer or device that must be contacted for the Digital Transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) for the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="29c33-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="29c33-106">Applies To</span></span>

-   [<span data-ttu-id="29c33-107">**Itens de áudio**</span><span class="sxs-lookup"><span data-stu-id="29c33-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="29c33-108">**Itens de foto**</span><span class="sxs-lookup"><span data-stu-id="29c33-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="29c33-109">**Itens da lista de reprodução**</span><span class="sxs-lookup"><span data-stu-id="29c33-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="29c33-110">**Itens de vídeo**</span><span class="sxs-lookup"><span data-stu-id="29c33-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="29c33-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="29c33-111">Remarks</span></span>

<span data-ttu-id="29c33-112">Se esse atributo estiver disponível, o item de mídia será protegido usando DTCP-IP.</span><span class="sxs-lookup"><span data-stu-id="29c33-112">If this attribute is available, the media item is protected using DTCP-IP.</span></span>

<span data-ttu-id="29c33-113">Este atributo não está disponível para itens de mídia na biblioteca local do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="29c33-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="29c33-114">Ele está disponível somente para itens de mídia que pertencem a uma biblioteca remota; ou seja, uma biblioteca que foi disponibilizada por outro usuário na rede doméstica.</span><span class="sxs-lookup"><span data-stu-id="29c33-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="29c33-115">Para determinar se uma biblioteca de mídia é remota, chame o [**\_ tipo IWMPLibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="29c33-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="29c33-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29c33-116">Requirements</span></span>



| <span data-ttu-id="29c33-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="29c33-117">Requirement</span></span> | <span data-ttu-id="29c33-118">Valor</span><span class="sxs-lookup"><span data-stu-id="29c33-118">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="29c33-119">Versão</span><span class="sxs-lookup"><span data-stu-id="29c33-119">Version</span></span><br/> | <span data-ttu-id="29c33-120">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="29c33-120">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29c33-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="29c33-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29c33-122">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="29c33-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






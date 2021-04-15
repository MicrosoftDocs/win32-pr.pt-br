---
title: Atributo DTCPIPPort
description: O atributo DTCPIPPort é o número da porta TCP (protocolo de controle de transmissão) do computador ou dispositivo que deve ser contatado para Proteção de Conteúdo o RIAR (intercâmbio de chaves autenticado) do DTCP (protocolo de Internet) para o item de mídia.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- Atributo DTCPIPPort Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c1c6117425211c0015d218412c8a9ac0971d7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761464"
---
# <a name="dtcpipport-attribute"></a><span data-ttu-id="b9893-104">Atributo DTCPIPPort</span><span class="sxs-lookup"><span data-stu-id="b9893-104">DTCPIPPort Attribute</span></span>

<span data-ttu-id="b9893-105">O atributo **DTCPIPPort** é o número da porta TCP (protocolo de controle de transmissão) do computador ou dispositivo que deve ser contatado para proteção de conteúdo o RIAR (intercâmbio de chaves autenticado) do DTCP (protocolo de Internet) para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="b9893-105">The **DTCPIPPort** attribute is the Transmission Control Protocol (TCP) port number of the computer or device that must be contacted for the Digital Transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) for the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b9893-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="b9893-106">Applies To</span></span>

-   [<span data-ttu-id="b9893-107">**Itens de áudio**</span><span class="sxs-lookup"><span data-stu-id="b9893-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b9893-108">**Itens de foto**</span><span class="sxs-lookup"><span data-stu-id="b9893-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="b9893-109">**Itens da lista de reprodução**</span><span class="sxs-lookup"><span data-stu-id="b9893-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="b9893-110">**Itens de vídeo**</span><span class="sxs-lookup"><span data-stu-id="b9893-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b9893-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9893-111">Remarks</span></span>

<span data-ttu-id="b9893-112">Se esse atributo estiver disponível, o item de mídia será protegido usando DTCP-IP.</span><span class="sxs-lookup"><span data-stu-id="b9893-112">If this attribute is available, the media item is protected using DTCP-IP.</span></span>

<span data-ttu-id="b9893-113">Este atributo não está disponível para itens de mídia na biblioteca local do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="b9893-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="b9893-114">Ele está disponível somente para itens de mídia que pertencem a uma biblioteca remota; ou seja, uma biblioteca que foi disponibilizada por outro usuário na rede doméstica.</span><span class="sxs-lookup"><span data-stu-id="b9893-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="b9893-115">Para determinar se uma biblioteca de mídia é remota, chame o [**\_ tipo IWMPLibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="b9893-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9893-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9893-116">Requirements</span></span>



| <span data-ttu-id="b9893-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9893-117">Requirement</span></span> | <span data-ttu-id="b9893-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b9893-118">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="b9893-119">Versão</span><span class="sxs-lookup"><span data-stu-id="b9893-119">Version</span></span><br/> | <span data-ttu-id="b9893-120">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="b9893-120">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9893-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9893-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9893-122">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="b9893-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






---
title: Atributo DLNASourceURI
description: O atributo DLNASourceURI é o URI (identificador de recurso universal) do item.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- Atributo DLNASourceURI Windows Media Player
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789567"
---
# <a name="dlnasourceuri-attribute"></a><span data-ttu-id="3dbac-104">Atributo DLNASourceURI</span><span class="sxs-lookup"><span data-stu-id="3dbac-104">DLNASourceURI Attribute</span></span>

<span data-ttu-id="3dbac-105">O atributo **DLNASourceURI** é o URI (identificador de recurso universal) do item.</span><span class="sxs-lookup"><span data-stu-id="3dbac-105">The **DLNASourceURI** attribute is the universal resource identifier (URI) of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3dbac-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="3dbac-106">Applies To</span></span>

-   [<span data-ttu-id="3dbac-107">**Itens de áudio**</span><span class="sxs-lookup"><span data-stu-id="3dbac-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="3dbac-108">**Outros itens**</span><span class="sxs-lookup"><span data-stu-id="3dbac-108">**Other Items**</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="3dbac-109">**Itens de foto**</span><span class="sxs-lookup"><span data-stu-id="3dbac-109">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="3dbac-110">**Itens da lista de reprodução**</span><span class="sxs-lookup"><span data-stu-id="3dbac-110">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="3dbac-111">**Itens de vídeo**</span><span class="sxs-lookup"><span data-stu-id="3dbac-111">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="3dbac-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dbac-112">Remarks</span></span>

<span data-ttu-id="3dbac-113">Se o item estiver na biblioteca local do usuário atual, esse atributo, o atributo [**SourceURL**](sourceurl-attribute.md) e o valor retornado por [**IWMPMedia:: get \_ SourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) serão os mesmos.</span><span class="sxs-lookup"><span data-stu-id="3dbac-113">If the item is in the current user's local library, this attribute, the [**SourceURL**](sourceurl-attribute.md) attribute, and the value returned by [**IWMPMedia::get\_sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) are all the same.</span></span>

<span data-ttu-id="3dbac-114">Se o item não estiver na biblioteca local do usuário atual, mas pertencer a uma biblioteca remota, esse atributo será um identificador do formato DLNA-playsingle://*xxx*.</span><span class="sxs-lookup"><span data-stu-id="3dbac-114">If the item is not in the current user's local library, but belongs to a remote library, this attribute is an identifier of the form dlna-playsingle://*xxx*.</span></span>

<span data-ttu-id="3dbac-115">Você pode passar um URI DLNA-playsingle para o método [**IWMPCore3:: newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) para obter uma interface [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) que permite que você exiba os metadados do item de mídia e, potencialmente, edite a classificação por estrelas do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="3dbac-115">You can pass a dlna-playsingle URI to the [**IWMPCore3::newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) method to obtain an [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) interface that enables you to view the media item's metadata and potentially edit the media item's star rating.</span></span> <span data-ttu-id="3dbac-116">Observe, no entanto, que o URI DLNA-playsingle deve ser para um CDS (serviço de diretório de conteúdo) que o Windows Media Player já descobriu.</span><span class="sxs-lookup"><span data-stu-id="3dbac-116">Note, however, that the dlna-playsingle URI must be for a content directory service (CDS) that Windows Media Player has already discovered.</span></span> <span data-ttu-id="3dbac-117">O método **newMedia** não iniciará a descoberta de UPnP e pesquisará o CDs.</span><span class="sxs-lookup"><span data-stu-id="3dbac-117">The **newMedia** method will not initiate UPnP discovery and search for the CDS.</span></span>

<span data-ttu-id="3dbac-118">Você poderá editar a classificação por estrelas de um item de mídia em uma biblioteca remota somente se a biblioteca remota oferecer suporte à operação de edição.</span><span class="sxs-lookup"><span data-stu-id="3dbac-118">You can edit the star rating of a media item in a remote library only if the remote library supports the edit operation.</span></span> <span data-ttu-id="3dbac-119">As bibliotecas remotas hospedadas em um computador que executa o Windows 7 dão suporte à operação de edição.</span><span class="sxs-lookup"><span data-stu-id="3dbac-119">Remote libraries hosted on a computer running Windows 7 support the edit operation.</span></span> <span data-ttu-id="3dbac-120">As bibliotecas remotas hospedadas em um computador que executa um sistema operacional Windows anterior ao Windows 7 não oferecem suporte à operação de edição.</span><span class="sxs-lookup"><span data-stu-id="3dbac-120">Remote libraries hosted on a computer running a Windows operating system earlier than Windows 7 do not support the edit operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dbac-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dbac-121">Requirements</span></span>



| <span data-ttu-id="3dbac-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dbac-122">Requirement</span></span> | <span data-ttu-id="3dbac-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3dbac-123">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="3dbac-124">Versão</span><span class="sxs-lookup"><span data-stu-id="3dbac-124">Version</span></span><br/> | <span data-ttu-id="3dbac-125">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="3dbac-125">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3dbac-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dbac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbac-127">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="3dbac-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






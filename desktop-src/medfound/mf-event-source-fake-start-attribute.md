---
description: Especifica se a topologia de segmento atual está vazia.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: Atributo MF_EVENT_SOURCE_FAKE_START (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae47bbfdedb7535ff46763ad5bc36f552ffe4780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837439"
---
# <a name="mf_event_source_fake_start-attribute"></a><span data-ttu-id="67c1f-103">\_Atributo de \_ \_ Início falso da origem do evento MF \_</span><span class="sxs-lookup"><span data-stu-id="67c1f-103">MF\_EVENT\_SOURCE\_FAKE\_START attribute</span></span>

<span data-ttu-id="67c1f-104">Especifica se a topologia de segmento atual está vazia.</span><span class="sxs-lookup"><span data-stu-id="67c1f-104">Specifies whether the current segment topology is empty.</span></span>

## <a name="data-type"></a><span data-ttu-id="67c1f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="67c1f-105">Data type</span></span>

<span data-ttu-id="67c1f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="67c1f-106">**UINT32**</span></span>

<span data-ttu-id="67c1f-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="67c1f-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67c1f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="67c1f-108">Remarks</span></span>

<span data-ttu-id="67c1f-109">Esse atributo é usado com o evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="67c1f-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="67c1f-110">A origem do sequenciador define esse atributo como **true** se a topologia do segmento atual estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="67c1f-110">The sequencer source sets this attribute to **TRUE** if the current segment topology is empty.</span></span> <span data-ttu-id="67c1f-111">Se esse atributo for **true**, a reprodução ainda não foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="67c1f-111">If this attribute is **TRUE**, playback has not started yet.</span></span> <span data-ttu-id="67c1f-112">O valor padrão desse atributo é **false**.</span><span class="sxs-lookup"><span data-stu-id="67c1f-112">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="67c1f-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="67c1f-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="67c1f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67c1f-114">Requirements</span></span>



| <span data-ttu-id="67c1f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="67c1f-115">Requirement</span></span> | <span data-ttu-id="67c1f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="67c1f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67c1f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67c1f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="67c1f-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67c1f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="67c1f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67c1f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="67c1f-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67c1f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="67c1f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67c1f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="67c1f-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="67c1f-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c1f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="67c1f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c1f-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67c1f-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="67c1f-125">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="67c1f-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="67c1f-126">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="67c1f-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="67c1f-127">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="67c1f-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 





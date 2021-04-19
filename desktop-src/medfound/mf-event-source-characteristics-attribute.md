---
description: Especifica as características atuais da origem da mídia.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: Atributo MF_EVENT_SOURCE_CHARACTERISTICS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c775c0d3471d3d3442e565879ba8b42e07a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755501"
---
# <a name="mf_event_source_characteristics-attribute"></a><span data-ttu-id="e2a49-103">\_Atributo de \_ características de origem do evento MF \_</span><span class="sxs-lookup"><span data-stu-id="e2a49-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="e2a49-104">Especifica as características atuais da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="e2a49-104">Specifies the current characteristics of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="e2a49-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e2a49-105">Data type</span></span>

<span data-ttu-id="e2a49-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e2a49-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e2a49-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2a49-107">Remarks</span></span>

<span data-ttu-id="e2a49-108">O valor desse atributo é um bit a bit **ou** dos sinalizadores da enumeração de [**\_ características do MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="e2a49-108">The value of this attribute is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

<span data-ttu-id="e2a49-109">Esse atributo é usado com o evento [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="e2a49-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="e2a49-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e2a49-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2a49-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2a49-111">Requirements</span></span>



| <span data-ttu-id="e2a49-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2a49-112">Requirement</span></span> | <span data-ttu-id="e2a49-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e2a49-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a49-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2a49-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e2a49-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2a49-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e2a49-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2a49-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e2a49-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2a49-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e2a49-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2a49-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2a49-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2a49-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a49-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2a49-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a49-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2a49-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2a49-122">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="e2a49-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2a49-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e2a49-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e2a49-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="e2a49-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 





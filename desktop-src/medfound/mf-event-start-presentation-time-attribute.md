---
description: A hora de início da apresentação, em unidades de 100 nanossegundos, conforme medida pelo relógio de apresentação.
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: Atributo MF_EVENT_START_PRESENTATION_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf6142ce12a7bf921fd26373ea5d10ab384560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011851"
---
# <a name="mf_event_start_presentation_time-attribute"></a><span data-ttu-id="f6723-103">\_Atributo de \_ hora de início da \_ apresentação do evento MF \_</span><span class="sxs-lookup"><span data-stu-id="f6723-103">MF\_EVENT\_START\_PRESENTATION\_TIME attribute</span></span>

<span data-ttu-id="f6723-104">A hora de início da apresentação, em unidades de 100 nanossegundos, conforme medida pelo relógio de apresentação.</span><span class="sxs-lookup"><span data-stu-id="f6723-104">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>

## <a name="data-type"></a><span data-ttu-id="f6723-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f6723-105">Data type</span></span>

<span data-ttu-id="f6723-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f6723-106">**UINT64**</span></span>

<span data-ttu-id="f6723-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="f6723-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6723-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6723-108">Remarks</span></span>

<span data-ttu-id="f6723-109">Esse atributo é usado com o evento [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) .</span><span class="sxs-lookup"><span data-stu-id="f6723-109">This attribute is used with the [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) event.</span></span>

<span data-ttu-id="f6723-110">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="f6723-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="f6723-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f6723-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6723-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6723-112">Requirements</span></span>



| <span data-ttu-id="f6723-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6723-113">Requirement</span></span> | <span data-ttu-id="f6723-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f6723-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6723-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6723-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f6723-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6723-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f6723-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6723-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f6723-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6723-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f6723-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6723-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6723-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6723-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6723-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6723-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6723-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6723-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6723-123">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="f6723-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6723-124">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="f6723-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="f6723-125">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="f6723-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 





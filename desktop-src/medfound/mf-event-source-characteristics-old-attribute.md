---
description: Especifica as características anteriores da origem da mídia.
ms.assetid: 9779f350-60d5-4129-bada-0c4a58f93e6a
title: Atributo MF_EVENT_SOURCE_CHARACTERISTICS_OLD (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb19505643de064e3aa54abc9e37649ecd97ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755741"
---
# <a name="mf_event_source_characteristics_old-attribute"></a><span data-ttu-id="36594-103">\_Características de origem do evento MF \_ \_ \_ atributo antigo</span><span class="sxs-lookup"><span data-stu-id="36594-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD attribute</span></span>

<span data-ttu-id="36594-104">Especifica as características anteriores da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="36594-104">Specifies the previous characteristics of the media source.</span></span> <span data-ttu-id="36594-105">Os dados de atributo são um bit a bit **ou** dos sinalizadores da enumeração de [**\_ características do MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="36594-105">The attribute data is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="36594-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="36594-106">Data type</span></span>

<span data-ttu-id="36594-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="36594-107">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="36594-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="36594-108">Remarks</span></span>

<span data-ttu-id="36594-109">Esse atributo é usado com o evento [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="36594-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="36594-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="36594-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="36594-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36594-111">Requirements</span></span>



| <span data-ttu-id="36594-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="36594-112">Requirement</span></span> | <span data-ttu-id="36594-113">Valor</span><span class="sxs-lookup"><span data-stu-id="36594-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36594-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36594-114">Minimum supported client</span></span><br/> | <span data-ttu-id="36594-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36594-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="36594-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36594-116">Minimum supported server</span></span><br/> | <span data-ttu-id="36594-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36594-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="36594-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36594-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="36594-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="36594-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36594-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="36594-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36594-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36594-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="36594-122">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="36594-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="36594-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="36594-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="36594-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="36594-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="36594-125">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="36594-125">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 





---
description: Especifica se as topologias têm uma hora de início e de término global.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: Atributo MF_SESSION_GLOBAL_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814496"
---
# <a name="mf_session_global_time-attribute"></a><span data-ttu-id="5b00b-103">\_Atributo de \_ tempo global de sessão MF \_</span><span class="sxs-lookup"><span data-stu-id="5b00b-103">MF\_SESSION\_GLOBAL\_TIME attribute</span></span>

<span data-ttu-id="5b00b-104">Especifica se as topologias têm uma hora de início e de término global.</span><span class="sxs-lookup"><span data-stu-id="5b00b-104">Specifies whether topologies have a global start and stop time.</span></span>

## <a name="data-type"></a><span data-ttu-id="5b00b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5b00b-105">Data type</span></span>

<span data-ttu-id="5b00b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5b00b-106">**UINT32**</span></span>

<span data-ttu-id="5b00b-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="5b00b-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b00b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b00b-108">Remarks</span></span>

<span data-ttu-id="5b00b-109">Você pode definir esse atributo ao criar a mídia sesison usando o parâmetro *pConfiguration* da função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="5b00b-109">You can set this attribute when you create the media sesison by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="5b00b-110">Se esse atributo estiver presente e for diferente de zero, todas as topologias passadas para a sessão de mídia devem ter os atributos [**\_ \_ PROJECTSTART de topologia MF**](mf-topology-projectstart-attribute.md) e [**MF \_ Topology \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="5b00b-110">If this attribute is present and nonzero, then all topologies passed to the Media Session must have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) and [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attributes.</span></span> <span data-ttu-id="5b00b-111">Esses atributos especificam os horários de início e de parada da topologia em relação à apresentação inteira.</span><span class="sxs-lookup"><span data-stu-id="5b00b-111">These attributes specify the start and stop times for the topology relative to the entire presentation.</span></span>

<span data-ttu-id="5b00b-112">Se esse atributo estiver ausente ou **false**, as topologias não deverão ter o atributo [**MF \_ Topology \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) ou [**MF \_ Topology \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="5b00b-112">If this attribute is absent or **FALSE**, the topologies must not have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) or [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attribute.</span></span>

<span data-ttu-id="5b00b-113">Use este atributo para criar sequências de edição.</span><span class="sxs-lookup"><span data-stu-id="5b00b-113">Use this attribute to create editing sequences.</span></span> <span data-ttu-id="5b00b-114">Para obter mais informações, consulte [tempos de apresentação da sequência](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="5b00b-114">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="5b00b-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5b00b-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b00b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b00b-116">Requirements</span></span>



| <span data-ttu-id="5b00b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b00b-117">Requirement</span></span> | <span data-ttu-id="5b00b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5b00b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b00b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b00b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5b00b-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b00b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5b00b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b00b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5b00b-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b00b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5b00b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b00b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b00b-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b00b-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b00b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b00b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b00b-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b00b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5b00b-127">Atributos de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="5b00b-127">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="5b00b-128">Tempos de apresentação da sequência</span><span class="sxs-lookup"><span data-stu-id="5b00b-128">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="5b00b-129">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5b00b-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5b00b-130">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="5b00b-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5b00b-131">**\_PROJECTSTART de topologia MF \_**</span><span class="sxs-lookup"><span data-stu-id="5b00b-131">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> <dt>

[<span data-ttu-id="5b00b-132">**\_PROJECTSTOP de topologia MF \_**</span><span class="sxs-lookup"><span data-stu-id="5b00b-132">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 





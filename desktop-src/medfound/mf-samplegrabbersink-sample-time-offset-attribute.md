---
description: Deslocamento entre o carimbo de data/hora de cada exemplo recebido pelo exemplo de apoio e a hora em que o exemplo de amostra apresenta o exemplo.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: Atributo MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750148"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a><span data-ttu-id="4db3a-103">\_Atributo de \_ deslocamento de tempo de exemplo MF SAMPLEGRABBERSINK \_ \_</span><span class="sxs-lookup"><span data-stu-id="4db3a-103">MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="4db3a-104">Deslocamento entre o carimbo de data/hora de cada exemplo recebido pelo exemplo de apoio e a hora em que o exemplo de amostra apresenta o exemplo.</span><span class="sxs-lookup"><span data-stu-id="4db3a-104">Offset between the time stamp on each sample received by the sample grabber, and the time when the sample grabber presents the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="4db3a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4db3a-105">Data type</span></span>

<span data-ttu-id="4db3a-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4db3a-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="4db3a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4db3a-107">Remarks</span></span>

<span data-ttu-id="4db3a-108">Você pode definir esse atributo no objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) que é retornado pela função [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="4db3a-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object that is returned by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="4db3a-109">Esse atributo habilita a função de retorno de chamada do exemplo para receber amostras anteriores à hora da apresentação.</span><span class="sxs-lookup"><span data-stu-id="4db3a-109">This attribute enables the sample grabber's callback function to receive samples earlier than the presentation time.</span></span>

<span data-ttu-id="4db3a-110">Quando o complemento de exemplo recebe um novo exemplo, ele apresenta a amostra no tempo *t* − *deslocamento*, em que *t* é o carimbo de data/hora no exemplo e *deslocamento* é o valor desse atributo.</span><span class="sxs-lookup"><span data-stu-id="4db3a-110">When the sample grabber receives a new sample, it presents the sample at time *t* − *offset*, where *t* is the time stamp on the sample and *offset* is the value of this attribute.</span></span> <span data-ttu-id="4db3a-111">Se esse atributo não for definido, o valor padrão será zero.</span><span class="sxs-lookup"><span data-stu-id="4db3a-111">If this attribute is not set, the default value is zero.</span></span>

<span data-ttu-id="4db3a-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4db3a-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db3a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4db3a-113">Requirements</span></span>



| <span data-ttu-id="4db3a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4db3a-114">Requirement</span></span> | <span data-ttu-id="4db3a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4db3a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4db3a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4db3a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4db3a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4db3a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4db3a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4db3a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4db3a-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4db3a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4db3a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4db3a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4db3a-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4db3a-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4db3a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4db3a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db3a-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4db3a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4db3a-124">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="4db3a-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="4db3a-125">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="4db3a-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="4db3a-126">**IMFSampleGrabberSinkCallback**</span><span class="sxs-lookup"><span data-stu-id="4db3a-126">**IMFSampleGrabberSinkCallback**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[<span data-ttu-id="4db3a-127">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4db3a-127">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 





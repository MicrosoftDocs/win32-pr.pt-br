---
description: Especifica um número entre 0 e 100 que indica a compensação entre a qualidade de codificação e a velocidade de codificação.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: Atributo MF_TRANSCODE_QUALITYVSSPEED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4d95fab92276e926189c885dad2ecb8f164a97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765607"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a><span data-ttu-id="1febf-103">\_Atributo QUALITYVSSPEED de rescodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="1febf-103">MF\_TRANSCODE\_QUALITYVSSPEED attribute</span></span>

<span data-ttu-id="1febf-104">Especifica um número entre 0 e 100 que indica a compensação entre a qualidade de codificação e a velocidade de codificação.</span><span class="sxs-lookup"><span data-stu-id="1febf-104">Specifies a number between 0 and 100 that indicates the tradeoff between encoding quality and encoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="1febf-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1febf-105">Data type</span></span>

<span data-ttu-id="1febf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1febf-106">**UINT32**</span></span>

<span data-ttu-id="1febf-107">O valor dessa propriedade tem o seguinte intervalo.</span><span class="sxs-lookup"><span data-stu-id="1febf-107">The value of this property has the following range.</span></span>



| <span data-ttu-id="1febf-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1febf-108">Value</span></span>                                                                          | <span data-ttu-id="1febf-109">Significado</span><span class="sxs-lookup"><span data-stu-id="1febf-109">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="1febf-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1febf-110"><dt>0</dt></span></span> </dl>   | <span data-ttu-id="1febf-111">Menor qualidade e codificação mais rápida.</span><span class="sxs-lookup"><span data-stu-id="1febf-111">Lower quality, faster encoding.</span></span><br/>  |
| <dl> <span data-ttu-id="1febf-112"><dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="1febf-112"><dt>100</dt></span></span> </dl> | <span data-ttu-id="1febf-113">Maior qualidade, codificação mais lenta.</span><span class="sxs-lookup"><span data-stu-id="1febf-113">Higher quality, slower encoding.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="1febf-114">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="1febf-114">Get/set</span></span>

<span data-ttu-id="1febf-115">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="1febf-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1febf-116">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="1febf-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="1febf-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1febf-117">Remarks</span></span>

<span data-ttu-id="1febf-118">Esse atributo tem o mesmo valor de GUID que a propriedade [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) definida para [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)e tem a mesma interpretação.</span><span class="sxs-lookup"><span data-stu-id="1febf-118">This attribute has the same GUID value as the [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) property defined for [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi), and has the same interpretation.</span></span>

<span data-ttu-id="1febf-119">O aplicativo pode definir esse atributo no perfil transcodificar antes de criar a topologia de transcodificação para os codecs do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1febf-119">The application can set this attribute on the transcode profile before building the transcode topology for Windows Media codecs.</span></span> <span data-ttu-id="1febf-120">O valor deve estar no intervalo de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="1febf-120">The value must be in the range from 0 to 100.</span></span> <span data-ttu-id="1febf-121">Para fluxo de vídeo, o construtor de topologia transcodificar mapeia um valor para o valor especificado pelo aplicativo e fornece o valor mapeado para a propriedade **MFPKEY \_ COMPLEXITYEX** do codificador.</span><span class="sxs-lookup"><span data-stu-id="1febf-121">For video stream, the transcode topology builder maps a value to the application-specified value and supplies the mapped value to the **MFPKEY\_COMPLEXITYEX** property of the encoder.</span></span> <span data-ttu-id="1febf-122">Valores mais baixos permitem que o codificador use algoritmos de codificação menos complicados.</span><span class="sxs-lookup"><span data-stu-id="1febf-122">Lower values enable the encoder to use less complicated encoding algorithms.</span></span> <span data-ttu-id="1febf-123">O uso de algoritmos mais simples produz uma saída de baixa qualidade, mas o processo de codificação é mais rápido e requer menos capacidade de processamento.</span><span class="sxs-lookup"><span data-stu-id="1febf-123">Using simpler algorithms produces lower-quality output, but the encoding process is faster and requires less processing power.</span></span>

<span data-ttu-id="1febf-124">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1febf-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1febf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1febf-125">Requirements</span></span>



| <span data-ttu-id="1febf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1febf-126">Requirement</span></span> | <span data-ttu-id="1febf-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1febf-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1febf-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1febf-128">Header</span></span><br/> | <dl> <span data-ttu-id="1febf-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1febf-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1febf-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1febf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1febf-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1febf-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1febf-132">API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="1febf-132">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="1febf-133">**IMFTranscodeProfile:: setvideoattributes**</span><span class="sxs-lookup"><span data-stu-id="1febf-133">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 

---
description: Especifica, em IMFTransform, a taxa máxima de processamento de macrobloco, em macroblocos por segundo, que é suportada pelo codificador de hardware.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: Atributo MF_VIDEO_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768400"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a><span data-ttu-id="1bcdc-103">\_Atributo MF máximo de MB de vídeo \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="1bcdc-103">MF\_VIDEO\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="1bcdc-104">Especifica, em [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), a taxa máxima de processamento de macrobloco, em macroblocos por segundo, que é suportada pelo codificador de hardware.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-104">Specifies, on [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), the maximum macroblock processing rate, in macroblocks per second, that is supported by the hardware encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="1bcdc-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1bcdc-105">Data type</span></span>

<span data-ttu-id="1bcdc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1bcdc-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1bcdc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bcdc-107">Remarks</span></span>

<span data-ttu-id="1bcdc-108">Este é um atributo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-108">This is a read-only attribute.</span></span>

<span data-ttu-id="1bcdc-109">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="1bcdc-109">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="1bcdc-110">Esse atributo é afetado pelas seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="1bcdc-110">This attribute is affected by the following properties:</span></span>

-   <span data-ttu-id="1bcdc-111">[MF \_ \_ \_ Nível de vídeo MT](mf-mt-video-level.md) (que é um alias [do \_ \_ \_ nível de MPEG2 MF MT](mf-mt-mpeg2-level-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="1bcdc-111">[MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) (which is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md))</span></span>
-   [<span data-ttu-id="1bcdc-112">CODECAPI \_ AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="1bcdc-112">CODECAPI\_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="1bcdc-113">CODECAPI \_ AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="1bcdc-113">CODECAPI\_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

<span data-ttu-id="1bcdc-114">Se o atributo de [ \_ nível de \_ vídeo \_ MF MT](mf-mt-video-level.md) estiver presente, o codificador deverá retornar a taxa de processamento para a taxa de bits e resolução mais altas com suporte no nível especificado.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-114">If the [MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) attribute is present, the encoder should return the processing rate for the highest bitrate and resolution supported at the specified level.</span></span> <span data-ttu-id="1bcdc-115">Se o \_ atributo de nível de vídeo MF MT \_ \_ não estiver presente, ele deverá usar um nível padrão de 4.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-115">If the MF\_MT\_VIDEO\_LEVEL attribute is not present then it should use a default level of 4.</span></span>

<span data-ttu-id="1bcdc-116">Se a propriedade [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI tiver sido definida, o codificador deverá retornar a taxa de processamento correspondente ao valor definido para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-116">If the [CODECAPI\_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI property has been set, the encoder should return the processing rate corresponding to the value set for this property.</span></span> <span data-ttu-id="1bcdc-117">Se o \_ atributo CODECAPI AVEncCommonQualityVsSpeed não estiver presente, ele deverá usar um valor padrão de 0 que deve ser o modo de processamento mais rápido.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-117">If the CODECAPI\_AVEncCommonQualityVsSpeed attribute is not present, then it should use a default value of 0 which should be the fastest processing mode.</span></span>

<span data-ttu-id="1bcdc-118">Se a propriedade [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI tiver sido definida como um valor válido e com suporte, o codificador deverá retornar a taxa de processamento correspondente ao valor definido para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-118">If the [CODECAPI\_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI property has been set to a valid and supported value, the encoder should return the processing rate corresponding the value set for this property.</span></span> <span data-ttu-id="1bcdc-119">Se o \_ atributo CODECAPI AVEncMPVDefaultBPictureCount não for, ele deverá usar um valor padrão de 0 B quadros.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-119">If the CODECAPI\_AVEncMPVDefaultBPictureCount attribute is not presen,t then it should use a default value of 0 B frames.</span></span>

<span data-ttu-id="1bcdc-120">Somente os 28 bits inferiores devem ser usados por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-120">Only the lower 28 bits should be used by an application.</span></span> <span data-ttu-id="1bcdc-121">Os 4bits superiores são reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-121">The upper 4bits are reserved for future use.</span></span> <span data-ttu-id="1bcdc-122">Os aplicativos devem ignorar os 4 bits superiores e MFTs deve definir os 4 bits superiores como 0.</span><span class="sxs-lookup"><span data-stu-id="1bcdc-122">Applications should ignore the upper 4 bits and MFTs should set the upper 4 bits to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bcdc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bcdc-123">Requirements</span></span>



| <span data-ttu-id="1bcdc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bcdc-124">Requirement</span></span> | <span data-ttu-id="1bcdc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1bcdc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1bcdc-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bcdc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1bcdc-127">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1bcdc-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="1bcdc-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bcdc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1bcdc-129">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="1bcdc-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1bcdc-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bcdc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bcdc-131"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bcdc-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bcdc-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bcdc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bcdc-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1bcdc-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

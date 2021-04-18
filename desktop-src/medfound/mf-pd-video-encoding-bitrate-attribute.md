---
description: Especifica a taxa de bits de codificação de vídeo para a apresentação, em bits por segundo. Este atributo se aplica aos descritores de apresentação.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: Atributo MF_PD_VIDEO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477d0954b4db8fa11c1540153c096e42f6d255b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782762"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a><span data-ttu-id="06ccb-104">\_Atributo de \_ taxa de bits de \_ codificação de vídeo MF PD \_</span><span class="sxs-lookup"><span data-stu-id="06ccb-104">MF\_PD\_VIDEO\_ENCODING\_BITRATE attribute</span></span>

<span data-ttu-id="06ccb-105">Especifica a taxa de bits de codificação de vídeo para a apresentação, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="06ccb-105">Specifies the video encoding bit rate for the presentation, in bits per second.</span></span> <span data-ttu-id="06ccb-106">Este atributo se aplica aos descritores de apresentação.</span><span class="sxs-lookup"><span data-stu-id="06ccb-106">This attribute applies to presentation descriptors.</span></span>

## <a name="data-type"></a><span data-ttu-id="06ccb-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="06ccb-107">Data type</span></span>

<span data-ttu-id="06ccb-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="06ccb-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="06ccb-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="06ccb-109">Remarks</span></span>

<span data-ttu-id="06ccb-110">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="06ccb-110">This attribute is optional.</span></span> <span data-ttu-id="06ccb-111">Alguns formatos têm esquemas de codificação mais complexos que não podem ser resumidos usando esse atributo.</span><span class="sxs-lookup"><span data-stu-id="06ccb-111">Some formats have more complex encoding schemes that cannot be summarized by using this attribute.</span></span> <span data-ttu-id="06ccb-112">Para arquivos ASF (Advanced Systems Format), os seguintes atributos descrevem coletivamente a taxa de bits de codificação:</span><span class="sxs-lookup"><span data-stu-id="06ccb-112">For Advanced Systems Format (ASF) files, the following attributes collectively describe the encoding bit rate:</span></span>

-   [<span data-ttu-id="06ccb-113">**\_taxa de \_ \_ \_ bits máxima de arquivo MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="06ccb-113">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE**</span></span>](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [<span data-ttu-id="06ccb-114">**\_taxa de \_ \_ \_ bits média de \_ dados \_ do MF SD EXTSTRMPROP**</span><span class="sxs-lookup"><span data-stu-id="06ccb-114">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [<span data-ttu-id="06ccb-115">**\_taxa de \_ \_ \_ bits máxima de \_ dados EXTSTRMPROP \_ MF SD**</span><span class="sxs-lookup"><span data-stu-id="06ccb-115">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [<span data-ttu-id="06ccb-116">**\_taxa de \_ \_ bits STREAMBITRATES do ASF SD \_**</span><span class="sxs-lookup"><span data-stu-id="06ccb-116">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)

<span data-ttu-id="06ccb-117">Formatos de terceiros podem usar outros atributos personalizados.</span><span class="sxs-lookup"><span data-stu-id="06ccb-117">Third-party formats might use other custom attributes.</span></span>

<span data-ttu-id="06ccb-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="06ccb-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="06ccb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06ccb-119">Requirements</span></span>



| <span data-ttu-id="06ccb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="06ccb-120">Requirement</span></span> | <span data-ttu-id="06ccb-121">Valor</span><span class="sxs-lookup"><span data-stu-id="06ccb-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06ccb-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06ccb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="06ccb-123">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="06ccb-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="06ccb-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06ccb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="06ccb-125">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="06ccb-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="06ccb-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06ccb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="06ccb-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="06ccb-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06ccb-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="06ccb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06ccb-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06ccb-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="06ccb-130">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="06ccb-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="06ccb-131">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="06ccb-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="06ccb-132">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="06ccb-132">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="06ccb-133">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="06ccb-133">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





---
description: Especifica a taxa de bits de codificação de áudio para a apresentação, em bits por segundo. Este atributo se aplica aos descritores de apresentação.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: Atributo MF_PD_AUDIO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49566ecb225482ef6513e056de8ba11763de603e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170369"
---
# <a name="mf_pd_audio_encoding_bitrate-attribute"></a><span data-ttu-id="23aa0-104">\_Atributo de \_ taxa de bits de \_ codificação de áudio MF PD \_</span><span class="sxs-lookup"><span data-stu-id="23aa0-104">MF\_PD\_AUDIO\_ENCODING\_BITRATE attribute</span></span>

<span data-ttu-id="23aa0-105">Especifica a taxa de bits de codificação de áudio para a apresentação, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="23aa0-105">Specifies the audio encoding bit rate for the presentation, in bits per second.</span></span> <span data-ttu-id="23aa0-106">Este atributo se aplica aos descritores de apresentação.</span><span class="sxs-lookup"><span data-stu-id="23aa0-106">This attribute applies to presentation descriptors.</span></span>

## <a name="data-type"></a><span data-ttu-id="23aa0-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="23aa0-107">Data type</span></span>

<span data-ttu-id="23aa0-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="23aa0-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="23aa0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="23aa0-109">Remarks</span></span>

<span data-ttu-id="23aa0-110">O atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="23aa0-110">The attribute is optional.</span></span> <span data-ttu-id="23aa0-111">Alguns formatos têm esquemas de codificação mais complexos que não podem ser resumidos usando esse atributo.</span><span class="sxs-lookup"><span data-stu-id="23aa0-111">Some formats have more complex encoding schemes that cannot be summarized by using this attribute.</span></span> <span data-ttu-id="23aa0-112">Para arquivos ASF (Advanced Systems Format), os seguintes atributos descrevem coletivamente a taxa de bits de codificação:</span><span class="sxs-lookup"><span data-stu-id="23aa0-112">For Advanced Systems Format (ASF) files, the following attributes collectively describe the encoding bit rate:</span></span>

-   [<span data-ttu-id="23aa0-113">**\_taxa de \_ \_ \_ bits máxima de arquivo MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="23aa0-113">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE**</span></span>](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [<span data-ttu-id="23aa0-114">**\_taxa de \_ \_ \_ bits média de \_ dados \_ do MF SD EXTSTRMPROP**</span><span class="sxs-lookup"><span data-stu-id="23aa0-114">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [<span data-ttu-id="23aa0-115">**\_taxa de \_ \_ \_ bits máxima de \_ dados EXTSTRMPROP \_ MF SD**</span><span class="sxs-lookup"><span data-stu-id="23aa0-115">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [<span data-ttu-id="23aa0-116">**\_taxa de \_ \_ bits STREAMBITRATES do ASF SD \_**</span><span class="sxs-lookup"><span data-stu-id="23aa0-116">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)

<span data-ttu-id="23aa0-117">Formatos de terceiros podem usar outros atributos personalizados.</span><span class="sxs-lookup"><span data-stu-id="23aa0-117">Third-party formats might use other custom attributes.</span></span>

<span data-ttu-id="23aa0-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="23aa0-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="23aa0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23aa0-119">Requirements</span></span>



| <span data-ttu-id="23aa0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="23aa0-120">Requirement</span></span> | <span data-ttu-id="23aa0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="23aa0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23aa0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23aa0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="23aa0-123">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="23aa0-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="23aa0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23aa0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="23aa0-125">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="23aa0-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="23aa0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23aa0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="23aa0-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="23aa0-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23aa0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="23aa0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23aa0-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23aa0-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="23aa0-130">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="23aa0-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="23aa0-131">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="23aa0-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="23aa0-132">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="23aa0-132">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="23aa0-133">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="23aa0-133">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





---
description: Especifica o perfil de codificação de vídeo no tipo de mídia de saída. Este é um alias do \_ atributo de perfil MF mt de \_ MPEG2 \_ .
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: Atributo MF_MT_VIDEO_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812042"
---
# <a name="mf_mt_video_profile-attribute"></a><span data-ttu-id="6ca3a-104">\_Atributo de \_ perfil de vídeo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="6ca3a-104">MF\_MT\_VIDEO\_PROFILE attribute</span></span>

<span data-ttu-id="6ca3a-105">Especifica o perfil de codificação de vídeo no tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="6ca3a-105">Specifies the profile of video encoding on the output media type.</span></span> <span data-ttu-id="6ca3a-106">Este é um alias do atributo de [ \_ \_ \_ perfil MF mt de MPEG2](mf-mt-mpeg2-profile-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6ca3a-106">This is an alias of [MF\_MT\_MPEG2\_PROFILE](mf-mt-mpeg2-profile-attribute.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="6ca3a-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6ca3a-107">Data type</span></span>

<span data-ttu-id="6ca3a-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6ca3a-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6ca3a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ca3a-109">Remarks</span></span>

<span data-ttu-id="6ca3a-110">**Codificadores H. 264:**</span><span class="sxs-lookup"><span data-stu-id="6ca3a-110">**H.264 encoders:**</span></span>

<span data-ttu-id="6ca3a-111">Os perfis com suporte são excedidos para incluir [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) e **eAVEncH264VProfile \_ ConstrainedHigh**.</span><span class="sxs-lookup"><span data-stu-id="6ca3a-111">Supported profiles are exceeded to include [**eAVEncH264VProfile\_ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) and **eAVEncH264VProfile\_ConstrainedHigh**.</span></span>

<span data-ttu-id="6ca3a-112">Os codificadores devem dar suporte a [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) e [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) para esse atributo.</span><span class="sxs-lookup"><span data-stu-id="6ca3a-112">Encoders shall support both [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) and [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) for this attribute.</span></span>

<span data-ttu-id="6ca3a-113">Isso é estático, portanto, os codificadores de vídeo devem ser configurados antes do início do streaming.</span><span class="sxs-lookup"><span data-stu-id="6ca3a-113">This is static, so video encoders must be configured before the streaming starts.</span></span> <span data-ttu-id="6ca3a-114">Se o aplicativo definir um perfil para o qual o codificador não dá suporte, o codificador deverá rejeitar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="6ca3a-114">If the application sets a profile which the encoder does not support, the encoder shall reject the media type.</span></span>

<span data-ttu-id="6ca3a-115">Padrão recomendado: [**perfil \_ principal do eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="6ca3a-115">Recommended default: [**eAVEncH264VProfile\_Main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca3a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ca3a-116">Requirements</span></span>



| <span data-ttu-id="6ca3a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ca3a-117">Requirement</span></span> | <span data-ttu-id="6ca3a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ca3a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca3a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ca3a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca3a-120">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ca3a-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6ca3a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ca3a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca3a-122">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="6ca3a-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6ca3a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ca3a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ca3a-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca3a-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ca3a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ca3a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca3a-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ca3a-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

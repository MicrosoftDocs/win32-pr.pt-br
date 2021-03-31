---
description: Especifica se o mecanismo de captura captura vídeo, mas não áudio.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: Atributo MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921277"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a><span data-ttu-id="394a7-103">\_Mecanismo de captura MF usar o \_ \_ \_ \_ \_ atributo somente dispositivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="394a7-103">MF\_CAPTURE\_ENGINE\_USE\_VIDEO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="394a7-104">Especifica se o mecanismo de captura captura vídeo, mas não áudio.</span><span class="sxs-lookup"><span data-stu-id="394a7-104">Specifies whether the capture engine captures video but not audio.</span></span>

## <a name="data-type"></a><span data-ttu-id="394a7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="394a7-105">Data type</span></span>

<span data-ttu-id="394a7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="394a7-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="394a7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="394a7-107">Remarks</span></span>

<span data-ttu-id="394a7-108">Se esse atributo for **true**, o mecanismo de captura não selecionará nem usará um dispositivo de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="394a7-108">If this attribute is **TRUE**, the capture engine does not select or use an audio capture device.</span></span> <span data-ttu-id="394a7-109">Defina esse atributo como **true** se desejar capturar vídeo sem áudio.</span><span class="sxs-lookup"><span data-stu-id="394a7-109">Set this attribute to **TRUE** if you want to capture video without audio.</span></span> <span data-ttu-id="394a7-110">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="394a7-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="394a7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="394a7-111">Requirements</span></span>



| <span data-ttu-id="394a7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="394a7-112">Requirement</span></span> | <span data-ttu-id="394a7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="394a7-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="394a7-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="394a7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="394a7-115">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="394a7-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="394a7-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="394a7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="394a7-117">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="394a7-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="394a7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="394a7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="394a7-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="394a7-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="394a7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="394a7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="394a7-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="394a7-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="394a7-122">Atributos do mecanismo de captura</span><span class="sxs-lookup"><span data-stu-id="394a7-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="394a7-123">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="394a7-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





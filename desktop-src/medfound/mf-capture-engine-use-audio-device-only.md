---
description: Especifica se o mecanismo de captura captura áudio, mas não vídeo.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: Atributo MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921031"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a><span data-ttu-id="8cda3-103">\_Mecanismo de captura MF usar o \_ \_ \_ \_ \_ atributo somente dispositivo de áudio</span><span class="sxs-lookup"><span data-stu-id="8cda3-103">MF\_CAPTURE\_ENGINE\_USE\_AUDIO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="8cda3-104">Especifica se o mecanismo de captura captura áudio, mas não vídeo.</span><span class="sxs-lookup"><span data-stu-id="8cda3-104">Specifies whether the capture engine captures audio but not video.</span></span>

## <a name="data-type"></a><span data-ttu-id="8cda3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8cda3-105">Data type</span></span>

<span data-ttu-id="8cda3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8cda3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8cda3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cda3-107">Remarks</span></span>

<span data-ttu-id="8cda3-108">Se esse atributo for **true**, o mecanismo de captura não selecionará nem usará um dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8cda3-108">If this attribute is **TRUE**, the capture engine does not select or use a video capture device.</span></span> <span data-ttu-id="8cda3-109">Defina esse atributo como **true** se você quiser capturar áudio sem vídeo.</span><span class="sxs-lookup"><span data-stu-id="8cda3-109">Set this attribute to **TRUE** if you want to capture audio without video.</span></span> <span data-ttu-id="8cda3-110">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="8cda3-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cda3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cda3-111">Requirements</span></span>



| <span data-ttu-id="8cda3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cda3-112">Requirement</span></span> | <span data-ttu-id="8cda3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8cda3-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cda3-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cda3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8cda3-115">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8cda3-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="8cda3-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cda3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8cda3-117">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8cda3-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8cda3-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cda3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cda3-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cda3-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cda3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cda3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cda3-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8cda3-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8cda3-122">Atributos do mecanismo de captura</span><span class="sxs-lookup"><span data-stu-id="8cda3-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="8cda3-123">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="8cda3-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





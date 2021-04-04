---
description: Define o número máximo de amostras processadas que podem ser armazenadas em buffer no caminho de vídeo do coletor de registros.
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: Atributo MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70c3840f449cebb6579b2c1df5f330379ba30655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647388"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a><span data-ttu-id="f0b97-103">\_Mecanismo de captura MF registro do vídeo do \_ \_ \_ coletor \_ \_ máximo \_ processados \_ atributo de amostras</span><span class="sxs-lookup"><span data-stu-id="f0b97-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="f0b97-104">Define o número máximo de amostras processadas que podem ser armazenadas em buffer no caminho de vídeo do coletor de registros.</span><span class="sxs-lookup"><span data-stu-id="f0b97-104">Sets the maximum number of processed samples that can be buffered in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="f0b97-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f0b97-105">Data type</span></span>

<span data-ttu-id="f0b97-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f0b97-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f0b97-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0b97-107">Remarks</span></span>

<span data-ttu-id="f0b97-108">Para configurar esse atributo no mecanismo de captura, adicione-o ao parâmetro *pAttributes* ao chamar [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="f0b97-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="f0b97-109">O valor máximo para esse atributo é 17.</span><span class="sxs-lookup"><span data-stu-id="f0b97-109">The maximum value for this attribute is 17.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b97-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0b97-110">Requirements</span></span>



| <span data-ttu-id="f0b97-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0b97-111">Requirement</span></span> | <span data-ttu-id="f0b97-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f0b97-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b97-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0b97-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f0b97-114">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f0b97-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f0b97-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0b97-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f0b97-116">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f0b97-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f0b97-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0b97-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0b97-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0b97-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0b97-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0b97-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b97-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0b97-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f0b97-121">Atributos do mecanismo de captura</span><span class="sxs-lookup"><span data-stu-id="f0b97-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="f0b97-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="f0b97-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





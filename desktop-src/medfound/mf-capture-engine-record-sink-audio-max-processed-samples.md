---
description: Define o número máximo de amostras processadas que podem ser armazenadas em buffer no caminho de áudio do coletor de registros.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: Atributo MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d1ce4d649c75106545eb2ff39d4f3ea742e6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501940"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a><span data-ttu-id="1a699-103">\_Mecanismo de captura MF registro de áudio do \_ \_ \_ coletor \_ \_ máximo \_ processados \_ atributo de amostras</span><span class="sxs-lookup"><span data-stu-id="1a699-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="1a699-104">Define o número máximo de amostras processadas que podem ser armazenadas em buffer no caminho de áudio do coletor de registros.</span><span class="sxs-lookup"><span data-stu-id="1a699-104">Sets the maximum number of processed samples that can be buffered in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="1a699-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1a699-105">Data type</span></span>

<span data-ttu-id="1a699-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1a699-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1a699-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a699-107">Remarks</span></span>

<span data-ttu-id="1a699-108">Para configurar esse atributo no mecanismo de captura, adicione-o ao parâmetro *pAttributes* ao chamar [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="1a699-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="1a699-109">O valor máximo para esse atributo é 100.</span><span class="sxs-lookup"><span data-stu-id="1a699-109">The maximum value for this attribute is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a699-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a699-110">Requirements</span></span>



| <span data-ttu-id="1a699-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a699-111">Requirement</span></span> | <span data-ttu-id="1a699-112">Valor</span><span class="sxs-lookup"><span data-stu-id="1a699-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a699-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a699-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1a699-114">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1a699-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1a699-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a699-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1a699-116">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1a699-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1a699-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a699-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a699-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a699-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a699-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a699-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a699-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1a699-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1a699-121">Atributos do mecanismo de captura</span><span class="sxs-lookup"><span data-stu-id="1a699-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="1a699-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="1a699-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





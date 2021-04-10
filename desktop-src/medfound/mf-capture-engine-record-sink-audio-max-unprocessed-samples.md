---
description: Define o número máximo de amostras não processadas que podem ser armazenadas em buffer para processamento no caminho de áudio do coletor de registros.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: Atributo MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442e9b5eca3354e87b8e36b55a3c6cb92ec6f131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296565"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a><span data-ttu-id="74b74-103">\_Registro do mecanismo de captura MF máximo do atributo de \_ \_ \_ \_ \_ \_ amostras não processadas do áudio do coletor \_</span><span class="sxs-lookup"><span data-stu-id="74b74-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="74b74-104">Define o número máximo de amostras não processadas que podem ser armazenadas em buffer para processamento no caminho de áudio do coletor de registros.</span><span class="sxs-lookup"><span data-stu-id="74b74-104">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="74b74-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="74b74-105">Data type</span></span>

<span data-ttu-id="74b74-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="74b74-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="74b74-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="74b74-107">Remarks</span></span>

<span data-ttu-id="74b74-108">Para configurar esse atributo no mecanismo de captura, adicione-o ao parâmetro *pAttributes* ao chamar [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="74b74-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="74b74-109">O valor máximo para esse atributo é 100.</span><span class="sxs-lookup"><span data-stu-id="74b74-109">The maximum value for this attribute is 100.</span></span>

<span data-ttu-id="74b74-110">Depois que o registro armazena em buffer o número máximo de amostras não processadas, especificado pelo \_ mecanismo de captura do MF \_ registro de áudio do \_ \_ coletor máximo de amostras não \_ \_ \_ processadas \_ , ele descarta a taxa de quadros soltando amostras.</span><span class="sxs-lookup"><span data-stu-id="74b74-110">Once the record has buffered the maximum number of unprocessed samples, specified by MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES, it drops the frame rate by dropping samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="74b74-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74b74-111">Requirements</span></span>



| <span data-ttu-id="74b74-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="74b74-112">Requirement</span></span> | <span data-ttu-id="74b74-113">Valor</span><span class="sxs-lookup"><span data-stu-id="74b74-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b74-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74b74-114">Minimum supported client</span></span><br/> | <span data-ttu-id="74b74-115">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="74b74-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="74b74-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74b74-116">Minimum supported server</span></span><br/> | <span data-ttu-id="74b74-117">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="74b74-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="74b74-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74b74-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="74b74-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="74b74-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74b74-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="74b74-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b74-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="74b74-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="74b74-122">Atributos do mecanismo de captura</span><span class="sxs-lookup"><span data-stu-id="74b74-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="74b74-123">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="74b74-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





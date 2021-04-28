---
description: MFT_MESSAGE_COMMAND_DRAIN-solicita uma Media Foundation transformação (MFT) para liberar todos os dados armazenados.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907bfbd888b1eccbe7336c0d8f386d3266fd8e9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092744"
---
# <a name="mft_message_command_drain"></a><span data-ttu-id="8217a-103">\_ \_ drenagem de comando de mensagem MFT \_</span><span class="sxs-lookup"><span data-stu-id="8217a-103">MFT\_MESSAGE\_COMMAND\_DRAIN</span></span>

<span data-ttu-id="8217a-104">Solicita uma Media Foundation transformação (MFT) para liberar todos os dados armazenados.</span><span class="sxs-lookup"><span data-stu-id="8217a-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="8217a-105">Parâmetro de mensagem</span><span class="sxs-lookup"><span data-stu-id="8217a-105">Message Parameter</span></span>

<span data-ttu-id="8217a-106">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8217a-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="8217a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8217a-107">Remarks</span></span>

<span data-ttu-id="8217a-108">Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="8217a-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="8217a-109">Depois que essa mensagem é enviada, o fluxo de entrada especificado não aceita a entrada até que o MFT processe todos os dados das chamadas anteriores para [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="8217a-109">After this message is sent, the specified input stream does not accept input until the MFT processes all data from previous calls to [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

<span data-ttu-id="8217a-110">O processo de descarga varia ligeiramente entre MFTs síncronos e MFTs assíncronas:</span><span class="sxs-lookup"><span data-stu-id="8217a-110">The draining process varies slightly between synchronous MFTs and asynchronous MFTs:</span></span>

<span data-ttu-id="8217a-111">**MFTs síncrono**</span><span class="sxs-lookup"><span data-stu-id="8217a-111">**Synchronous MFTs**</span></span>

1.  <span data-ttu-id="8217a-112">Depois que o cliente envia essa mensagem, ele chama [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) em um loop, até que **ProcessOutput** retorne o código de erro **MF \_ E \_ Transform \_ precise de \_ mais \_ entradas**.</span><span class="sxs-lookup"><span data-stu-id="8217a-112">After the client sends this message, it calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in a loop, until **ProcessOutput** returns the error code **MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT**.</span></span>
2.  <span data-ttu-id="8217a-113">Desde que o MFT ainda tenha dados a serem processados, outras chamadas para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) falharão.</span><span class="sxs-lookup"><span data-stu-id="8217a-113">As long as the MFT still has data to process, further calls to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will fail.</span></span> <span data-ttu-id="8217a-114">O MFT continua a produzir saída até que use todos os dados armazenados.</span><span class="sxs-lookup"><span data-stu-id="8217a-114">The MFT continues to produce output until it uses all stored data.</span></span> <span data-ttu-id="8217a-115">O MFT descarta todos os dados que não podem ser processados em um exemplo de saída completa.</span><span class="sxs-lookup"><span data-stu-id="8217a-115">The MFT discards any data that cannot be processed into a complete output sample.</span></span> <span data-ttu-id="8217a-116">(Por exemplo, ele deve remover um quadro de vídeo parcial.)</span><span class="sxs-lookup"><span data-stu-id="8217a-116">(For example, it should drop a partial video frame.)</span></span>

<span data-ttu-id="8217a-117">**MFTs assíncrona**</span><span class="sxs-lookup"><span data-stu-id="8217a-117">**Asynchronous MFTs**</span></span>

1.  <span data-ttu-id="8217a-118">O MFT continua enviando eventos [METransformHaveOutput](metransformhaveoutput.md) até que não haja mais dados a serem processados.</span><span class="sxs-lookup"><span data-stu-id="8217a-118">The MFT continues to send [METransformHaveOutput](metransformhaveoutput.md) events until it has no more data to process.</span></span> <span data-ttu-id="8217a-119">Ele não envia eventos [METransformNeedInput](metransformneedinput.md) durante esse tempo.</span><span class="sxs-lookup"><span data-stu-id="8217a-119">It does not send [METransformNeedInput](metransformneedinput.md) events during this time.</span></span>
2.  <span data-ttu-id="8217a-120">Depois que o MFT envia o último evento [METransformHaveOutput](metransformhaveoutput.md) , ele envia um evento [METransformDrainComplete](metransformdraincomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="8217a-120">After the MFT sends the last [METransformHaveOutput](metransformhaveoutput.md) event, it sends an [METransformDrainComplete](metransformdraincomplete.md) event.</span></span>
3.  <span data-ttu-id="8217a-121">Após a conclusão do descarregamento, o MFT não enviará outro evento [METransformNeedInput](metransformneedinput.md) até receber uma [**mensagem \_ MFT \_ \_ início \_ da mensagem de \_ fluxo**](mft-message-notify-start-of-stream.md) do cliente.</span><span class="sxs-lookup"><span data-stu-id="8217a-121">After draining is complete, the MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

<span data-ttu-id="8217a-122">Depois que o cliente drena o MFT, o cliente pode enviar mais dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="8217a-122">After the client has drained the MFT, the client can send more input data.</span></span> <span data-ttu-id="8217a-123">O primeiro exemplo após a operação de descarga deve ter o atributo de descontinuidade (atributo de descontinuidade [**MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md) ).</span><span class="sxs-lookup"><span data-stu-id="8217a-123">The first sample after the drain operation must have the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute).</span></span>

> [!Note]  
> <span data-ttu-id="8217a-124">As versões anteriores desta documentação afirmaram que o parâmetro de evento *ulParam* é um membro da enumeração de [**\_ \_ \_ tipo de drenagem de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) .</span><span class="sxs-lookup"><span data-stu-id="8217a-124">Earlier versions of this documentation stated that the *ulParam* event parameter is a member of the [**\_MFT\_DRAIN\_TYPE**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) enumeration.</span></span> <span data-ttu-id="8217a-125">Incorreto.</span><span class="sxs-lookup"><span data-stu-id="8217a-125">That is not correct.</span></span> <span data-ttu-id="8217a-126">O *ulParam* contém um identificador de fluxo.</span><span class="sxs-lookup"><span data-stu-id="8217a-126">The *ulParam* contains a stream identifier.</span></span>

 

### <a name="implementation"></a><span data-ttu-id="8217a-127">Implementação</span><span class="sxs-lookup"><span data-stu-id="8217a-127">Implementation</span></span>

<span data-ttu-id="8217a-128">Uma MFT assíncrona sempre deve retornar [METransformDrainComplete](metransformdraincomplete.md) depois que ela for descarregada.</span><span class="sxs-lookup"><span data-stu-id="8217a-128">An asynchronous MFT must always return [METransformDrainComplete](metransformdraincomplete.md) after it has drained.</span></span>

<span data-ttu-id="8217a-129">Um MFT síncrono pode ignorar essa mensagem e retornar S \_ OK se as seguintes condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="8217a-129">A synchronous MFT can ignore this message and return S\_OK if the following conditions are true:</span></span>

-   <span data-ttu-id="8217a-130">O MFT nunca armazena mais de uma amostra de entrada por vez.</span><span class="sxs-lookup"><span data-stu-id="8217a-130">The MFT never stores more than one input sample at a time.</span></span>
-   <span data-ttu-id="8217a-131">Cada amostra de entrada produz um único exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="8217a-131">Each input sample produces a single output sample.</span></span>

<span data-ttu-id="8217a-132">Caso contrário, um MFT síncrono deve implementar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="8217a-132">Otherwise, a synchronous MFT must implement this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8217a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8217a-133">Requirements</span></span>



| <span data-ttu-id="8217a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8217a-134">Requirement</span></span> | <span data-ttu-id="8217a-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8217a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8217a-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8217a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8217a-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8217a-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8217a-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8217a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8217a-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8217a-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8217a-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8217a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8217a-141"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="8217a-141"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8217a-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8217a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8217a-143">**\_tipo de mensagem MFT \_**</span><span class="sxs-lookup"><span data-stu-id="8217a-143">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[<span data-ttu-id="8217a-144">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="8217a-144">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 





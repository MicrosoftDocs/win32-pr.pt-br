---
description: Marca um ponto no fluxo. Essa mensagem se aplica somente a MFTs assíncronas.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765023"
---
# <a name="mft_message_command_marker"></a><span data-ttu-id="63d92-104">\_marcador de \_ comando de mensagem MFT \_</span><span class="sxs-lookup"><span data-stu-id="63d92-104">MFT\_MESSAGE\_COMMAND\_MARKER</span></span>

<span data-ttu-id="63d92-105">Marca um ponto no fluxo.</span><span class="sxs-lookup"><span data-stu-id="63d92-105">Marks a point in the stream.</span></span> <span data-ttu-id="63d92-106">Essa mensagem se aplica somente a [MFTs assíncronas](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="63d92-106">This message applies only to [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="63d92-107">Parâmetro de mensagem</span><span class="sxs-lookup"><span data-stu-id="63d92-107">Message Parameter</span></span>

<span data-ttu-id="63d92-108">Um valor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="63d92-108">An arbitrary value.</span></span> <span data-ttu-id="63d92-109">O MFT retorna o valor para o cliente no evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="63d92-109">The MFT returns the value to the client in the [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="remarks"></a><span data-ttu-id="63d92-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="63d92-110">Remarks</span></span>

<span data-ttu-id="63d92-111">Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="63d92-111">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="63d92-112">O MFT responde a estas mensagens da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="63d92-112">The MFT responds to this messageas follows:</span></span>

1.  <span data-ttu-id="63d92-113">O MFT gera tantas amostras de saída quanto possível dos dados de entrada existentes, enviando um evento [METransformHaveOutput](metransformhaveoutput.md) para cada exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="63d92-113">The MFT generates as many output samples as it can from the existing input data, sending an [METransformHaveOutput](metransformhaveoutput.md) event for each output sample.</span></span>
2.  <span data-ttu-id="63d92-114">Depois que toda a saída é gerada, o MFT envia um evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="63d92-114">After all of the output is generated, the MFT sends an [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="63d92-115">Esse evento deve ser enviado após todos os eventos [METransformHaveOutput](metransformhaveoutput.md) .</span><span class="sxs-lookup"><span data-stu-id="63d92-115">This event must be sent after all of the [METransformHaveOutput](metransformhaveoutput.md) events.</span></span>

<span data-ttu-id="63d92-116">O cliente não é necessário para enviar essa mensagem e deve enviar essa mensagem somente para MFTs assíncronas.</span><span class="sxs-lookup"><span data-stu-id="63d92-116">The client is not required to send this message, and should send this message only to asynchronous MFTs.</span></span> <span data-ttu-id="63d92-117">Um MFT síncrono não enviará um evento [METransformMarker](metransformmarker.md) em resposta a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="63d92-117">A synchronous MFT will not send an [METransformMarker](metransformmarker.md) event in response to this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="63d92-118">Implementação</span><span class="sxs-lookup"><span data-stu-id="63d92-118">Implementation</span></span>

<span data-ttu-id="63d92-119">O MFTs assíncrono deve responder a essa mensagem, conforme descrito.</span><span class="sxs-lookup"><span data-stu-id="63d92-119">Asynchronous MFTs must respond to this message as described.</span></span> <span data-ttu-id="63d92-120">O MFTs síncrono deve ignorar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="63d92-120">Synchronous MFTs should ignore this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d92-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63d92-121">Requirements</span></span>



| <span data-ttu-id="63d92-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="63d92-122">Requirement</span></span> | <span data-ttu-id="63d92-123">Valor</span><span class="sxs-lookup"><span data-stu-id="63d92-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d92-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63d92-124">Minimum supported client</span></span><br/> | <span data-ttu-id="63d92-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="63d92-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="63d92-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63d92-126">Minimum supported server</span></span><br/> | <span data-ttu-id="63d92-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="63d92-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63d92-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63d92-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="63d92-129"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="63d92-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63d92-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="63d92-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d92-131">**\_tipo de mensagem MFT \_**</span><span class="sxs-lookup"><span data-stu-id="63d92-131">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 





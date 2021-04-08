---
description: Notifica uma Media Foundation transformação (MFT) que a primeira amostra está prestes a ser processada.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010669"
---
# <a name="mft_message_notify_start_of_stream"></a><span data-ttu-id="597f1-103">\_ \_ \_ início \_ da notificação de \_ mensagem MFT</span><span class="sxs-lookup"><span data-stu-id="597f1-103">MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM</span></span>

<span data-ttu-id="597f1-104">Notifica uma Media Foundation transformação (MFT) que a primeira amostra está prestes a ser processada.</span><span class="sxs-lookup"><span data-stu-id="597f1-104">Notifies a Media Foundation transform (MFT) that the first sample is about to be processed.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="597f1-105">Parâmetro de mensagem</span><span class="sxs-lookup"><span data-stu-id="597f1-105">Message Parameter</span></span>

<span data-ttu-id="597f1-106">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="597f1-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="597f1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="597f1-107">Remarks</span></span>

<span data-ttu-id="597f1-108">Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="597f1-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="597f1-109">Para MFTs síncronos, é opcional enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="597f1-109">For synchronous MFTs, it is optional to send this message.</span></span>

<span data-ttu-id="597f1-110">Para MFTs assíncronas, o cliente deve enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="597f1-110">For asynchronous MFTs, the client must send this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="597f1-111">Implementação</span><span class="sxs-lookup"><span data-stu-id="597f1-111">Implementation</span></span>

<span data-ttu-id="597f1-112">Um MFT síncrono não é necessário para responder à mensagem.</span><span class="sxs-lookup"><span data-stu-id="597f1-112">A synchronous MFT is not required to respond to the message.</span></span>

<span data-ttu-id="597f1-113">Uma MFT assíncrona deve implementar essa mensagem, conforme descrito em [MFTs assíncrona](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="597f1-113">An asynchronous MFT must implement this message, as described in [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="597f1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="597f1-114">Requirements</span></span>



| <span data-ttu-id="597f1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="597f1-115">Requirement</span></span> | <span data-ttu-id="597f1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="597f1-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="597f1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="597f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="597f1-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="597f1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="597f1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="597f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="597f1-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="597f1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="597f1-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="597f1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="597f1-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="597f1-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="597f1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="597f1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="597f1-124">**\_tipo de mensagem MFT \_**</span><span class="sxs-lookup"><span data-stu-id="597f1-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 





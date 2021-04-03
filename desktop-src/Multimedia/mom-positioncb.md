---
title: Mensagem de MOM_POSITIONCB (mmsystem. h)
description: A mensagem de posição do MOM \_ é enviada quando um evento de retorno de chamada de MEVT \_ F \_ é alcançado no fluxo de saída de Midi.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- Multimídia do Windows de mensagem MOM_POSITIONCB
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645113"
---
# <a name="mom_positioncb-message"></a><span data-ttu-id="b73c9-104">Mensagem do MOM \_ POSITIONCB</span><span class="sxs-lookup"><span data-stu-id="b73c9-104">MOM\_POSITIONCB message</span></span>

<span data-ttu-id="b73c9-105">A mensagem de **\_ posição do MOM** é enviada quando um evento de **retorno de \_ \_ chamada de MEVT F** é alcançado no fluxo de saída de Midi.</span><span class="sxs-lookup"><span data-stu-id="b73c9-105">The **MOM\_POSITION** message is sent when an **MEVT\_F\_CALLBACK** event is reached in the MIDI output stream.</span></span>

## <a name="parameters"></a><span data-ttu-id="b73c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b73c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b73c9-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b73c9-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b73c9-108">Um ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="b73c9-108">A pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b73c9-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b73c9-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b73c9-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="b73c9-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b73c9-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b73c9-111">Return Value</span></span>

<span data-ttu-id="b73c9-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b73c9-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b73c9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b73c9-113">Remarks</span></span>

<span data-ttu-id="b73c9-114">A reprodução do buffer de fluxo continua até mesmo durante a execução da função de chamada de retorno.</span><span class="sxs-lookup"><span data-stu-id="b73c9-114">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="b73c9-115">Todos os eventos após o evento de **\_ retorno de \_ chamada de MEVT F** no buffer serão agendados e enviados no prazo, independentemente de quanto tempo é gasto na função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b73c9-115">Any events after the **MEVT\_F\_CALLBACK** event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="b73c9-116">Se os retornos de chamada de posição estiverem sendo gerados mais rapidamente do que o seu aplicativo pode processá-los, o membro **dwOffset** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) poderá se referir a um evento que seu aplicativo ainda não tenha processado.</span><span class="sxs-lookup"><span data-stu-id="b73c9-116">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b73c9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b73c9-117">Requirements</span></span>



| <span data-ttu-id="b73c9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b73c9-118">Requirement</span></span> | <span data-ttu-id="b73c9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b73c9-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73c9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b73c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b73c9-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b73c9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b73c9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b73c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b73c9-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b73c9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b73c9-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b73c9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b73c9-125"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b73c9-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b73c9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b73c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73c9-127">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="b73c9-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


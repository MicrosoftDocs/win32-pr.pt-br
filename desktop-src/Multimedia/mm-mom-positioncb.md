---
title: Mensagem de MM_MOM_POSITIONCB (mmsystem. h)
description: A \_ mensagem mm Mom \_ POSITIONCB é enviada para uma janela quando um \_ evento de retorno de chamada MEVT F \_ é atingido no fluxo de saída de Midi.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- Multimídia do Windows de mensagem MM_MOM_POSITIONCB
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918052"
---
# <a name="mm_mom_positioncb-message"></a><span data-ttu-id="8095f-104">\_Mensagem mm Mom \_ POSITIONCB</span><span class="sxs-lookup"><span data-stu-id="8095f-104">MM\_MOM\_POSITIONCB message</span></span>

<span data-ttu-id="8095f-105">A mensagem **mm \_ Mom \_ POSITIONCB** é enviada para uma janela quando um evento de retorno de chamada MEVT \_ F \_ é atingido no fluxo de saída de Midi.</span><span class="sxs-lookup"><span data-stu-id="8095f-105">The **MM\_MOM\_POSITIONCB** message is sent to a window when an MEVT\_F\_CALLBACK event is reached in the MIDI output stream.</span></span>


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="8095f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8095f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8095f-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="8095f-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="8095f-108">Ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o evento que causou o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8095f-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies the event that caused the callback.</span></span> <span data-ttu-id="8095f-109">O membro **dwOffset** fornece o deslocamento do evento.</span><span class="sxs-lookup"><span data-stu-id="8095f-109">The **dwOffset** member gives the offset of the event.</span></span>

</dd> <dt>

<span data-ttu-id="8095f-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8095f-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8095f-111">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="8095f-111">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8095f-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8095f-112">Return Value</span></span>

<span data-ttu-id="8095f-113">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8095f-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8095f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8095f-114">Remarks</span></span>

<span data-ttu-id="8095f-115">A reprodução do buffer de fluxo continua até mesmo durante a execução da função de chamada de retorno.</span><span class="sxs-lookup"><span data-stu-id="8095f-115">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="8095f-116">Todos os eventos após o \_ evento de retorno de chamada de MEVT F \_ no buffer serão agendados e enviados no prazo, independentemente de quanto tempo é gasto na função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8095f-116">Any events after the MEVT\_F\_CALLBACK event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="8095f-117">Se os retornos de chamada de posição estiverem sendo gerados mais rapidamente do que o seu aplicativo pode processá-los, o membro **dwOffset** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) poderá se referir a um evento que seu aplicativo ainda não tenha processado.</span><span class="sxs-lookup"><span data-stu-id="8095f-117">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8095f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8095f-118">Requirements</span></span>



| <span data-ttu-id="8095f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8095f-119">Requirement</span></span> | <span data-ttu-id="8095f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8095f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8095f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8095f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8095f-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8095f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8095f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8095f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8095f-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8095f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8095f-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8095f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8095f-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8095f-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8095f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8095f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8095f-128">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="8095f-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


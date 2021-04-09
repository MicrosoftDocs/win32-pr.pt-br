---
title: Mensagem de MM_MIM_MOREDATA (mmsystem. h)
description: A \_ mensagem mm mim \_ MOREDATA é enviada para uma janela de retorno de chamada quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens de dados do mim \_ rápido o suficiente para acompanhar o driver de dispositivo de entrada.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- Multimídia do Windows de mensagem MM_MIM_MOREDATA
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67835a67c957a250fe1ae6d391f5ebd56d5301b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009341"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="59d1a-104">MM \_ mensagem do mim \_ MOREDATA</span><span class="sxs-lookup"><span data-stu-id="59d1a-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="59d1a-105">A mensagem **mm \_ mim \_ MOREDATA** é enviada para uma janela de retorno de chamada quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens de [**\_ dados do mim**](mim-data.md) rápido o suficiente para acompanhar o driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="59d1a-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="59d1a-106">A janela recebe essa mensagem somente quando o aplicativo especifica o \_ status de e/s de Midi \_ na chamada para a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="59d1a-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="59d1a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59d1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59d1a-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="59d1a-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="59d1a-109">Identificador para o dispositivo de entrada MIDI que recebeu a mensagem MIDI.</span><span class="sxs-lookup"><span data-stu-id="59d1a-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="59d1a-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="59d1a-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="59d1a-111">Especifica a mensagem MIDI que foi recebida.</span><span class="sxs-lookup"><span data-stu-id="59d1a-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="59d1a-112">A mensagem é empacotada em um valor de doubleword da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="59d1a-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="59d1a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="59d1a-113">Requirement</span></span> | <span data-ttu-id="59d1a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="59d1a-114">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="59d1a-115">Palavra alta</span><span class="sxs-lookup"><span data-stu-id="59d1a-115">High word</span></span> | <span data-ttu-id="59d1a-116">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="59d1a-116">High-order byte</span></span> | <span data-ttu-id="59d1a-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="59d1a-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="59d1a-118">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="59d1a-118">Low-order byte</span></span>  | <span data-ttu-id="59d1a-119">Contém um segundo byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="59d1a-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="59d1a-120">Palavra inferior</span><span class="sxs-lookup"><span data-stu-id="59d1a-120">Low word</span></span>  | <span data-ttu-id="59d1a-121">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="59d1a-121">High-order byte</span></span> | <span data-ttu-id="59d1a-122">Contém o primeiro byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="59d1a-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="59d1a-123">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="59d1a-123">Low-order byte</span></span>  | <span data-ttu-id="59d1a-124">Contém o status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="59d1a-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="59d1a-125">Os dois bytes de dados MIDI são opcionais, dependendo do byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="59d1a-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59d1a-126">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="59d1a-126">Return Value</span></span>

<span data-ttu-id="59d1a-127">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="59d1a-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59d1a-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="59d1a-128">Remarks</span></span>

<span data-ttu-id="59d1a-129">Se seu aplicativo receber dados de MIDI mais rápido do que pode processá-los, você não deve usar um mecanismo de retorno de chamada de janela.</span><span class="sxs-lookup"><span data-stu-id="59d1a-129">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="59d1a-130">Para maximizar a velocidade, use uma função de retorno de chamada e use a mensagem do [**mim \_ MOREDATA**](mim-moredata.md) em vez de mm \_ MOREDATA do mim \_ .</span><span class="sxs-lookup"><span data-stu-id="59d1a-130">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="59d1a-131">Um aplicativo deve fazer apenas uma quantidade mínima de processamento de \_ mensagens MOREDATA do mim mm \_ .</span><span class="sxs-lookup"><span data-stu-id="59d1a-131">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="59d1a-132">(Em particular, os aplicativos não devem chamar a função [CreateMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante o processamento mm \_ MIM \_ MOREDATA.) Em vez disso, o aplicativo deve posicionar os dados de evento em um buffer e, em seguida, retornar.</span><span class="sxs-lookup"><span data-stu-id="59d1a-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="59d1a-133">Quando um aplicativo recebe uma mensagem de [**\_ \_ dados do mim mm**](mm-mim-data.md) após uma série de mensagens mm do \_ mim \_ MOREDATA, ele se inscreveu em eventos de entrada de Midi e pode chamar com segurança funções com uso intensivo de tempo.</span><span class="sxs-lookup"><span data-stu-id="59d1a-133">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="59d1a-134">As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="59d1a-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="59d1a-135">Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida.</span><span class="sxs-lookup"><span data-stu-id="59d1a-135">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="59d1a-136">Não há carimbo de data/hora disponível com esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="59d1a-136">No time stamp is available with this message.</span></span> <span data-ttu-id="59d1a-137">Para dados de entrada com carimbo de data/hora, você deve usar as mensagens que são enviadas para funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="59d1a-137">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="59d1a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59d1a-138">Requirements</span></span>



| <span data-ttu-id="59d1a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="59d1a-139">Requirement</span></span> | <span data-ttu-id="59d1a-140">Valor</span><span class="sxs-lookup"><span data-stu-id="59d1a-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d1a-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59d1a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="59d1a-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="59d1a-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="59d1a-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59d1a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="59d1a-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="59d1a-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="59d1a-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="59d1a-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="59d1a-146"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59d1a-146"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59d1a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="59d1a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d1a-148">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="59d1a-148">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="59d1a-149">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="59d1a-149">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


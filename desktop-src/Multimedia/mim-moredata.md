---
title: Mensagem de MIM_MOREDATA (mmsystem. h)
description: A mensagem do MIM \_ MOREDATA é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens de dados do mim \_ com rapidez suficiente para acompanhar o driver de dispositivo de entrada.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- Multimídia do Windows de mensagem MIM_MOREDATA
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645257"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="5af6a-104">Mensagem do MIM \_ MOREDATA</span><span class="sxs-lookup"><span data-stu-id="5af6a-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="5af6a-105">A mensagem do **mim \_ MOREDATA** é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens de [**\_ dados do mim**](mim-data.md) com rapidez suficiente para acompanhar o driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="5af6a-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="5af6a-106">A função de retorno de chamada recebe essa mensagem somente quando o aplicativo especifica o \_ status de e/s de Midi \_ na chamada para a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="5af6a-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="5af6a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5af6a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af6a-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="5af6a-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="5af6a-109">Especifica a mensagem MIDI que foi recebida.</span><span class="sxs-lookup"><span data-stu-id="5af6a-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="5af6a-110">A mensagem é empacotada em um valor **DWORD** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5af6a-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="5af6a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5af6a-111">Requirement</span></span> | <span data-ttu-id="5af6a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5af6a-112">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="5af6a-113">Palavra alta</span><span class="sxs-lookup"><span data-stu-id="5af6a-113">High word</span></span> | <span data-ttu-id="5af6a-114">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="5af6a-114">High-order byte</span></span> | <span data-ttu-id="5af6a-115">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5af6a-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="5af6a-116">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="5af6a-116">Low-order byte</span></span>  | <span data-ttu-id="5af6a-117">Contém um segundo byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="5af6a-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="5af6a-118">Palavra inferior</span><span class="sxs-lookup"><span data-stu-id="5af6a-118">Low word</span></span>  | <span data-ttu-id="5af6a-119">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="5af6a-119">High-order byte</span></span> | <span data-ttu-id="5af6a-120">Contém o primeiro byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="5af6a-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="5af6a-121">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="5af6a-121">Low-order byte</span></span>  | <span data-ttu-id="5af6a-122">Contém o status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="5af6a-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="5af6a-123">Os dois bytes de dados MIDI são opcionais, dependendo do byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="5af6a-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="5af6a-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="5af6a-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="5af6a-125">Especifica a hora em que a mensagem foi recebida pelo driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="5af6a-125">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="5af6a-126">O carimbo de data/hora é especificado em milissegundos, começando em 0 quando a função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) foi chamada.</span><span class="sxs-lookup"><span data-stu-id="5af6a-126">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5af6a-127">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5af6a-127">Return Value</span></span>

<span data-ttu-id="5af6a-128">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5af6a-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5af6a-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="5af6a-129">Remarks</span></span>

<span data-ttu-id="5af6a-130">Um aplicativo deve fazer apenas uma quantidade mínima de processamento de \_ mensagens MOREDATA do mim.</span><span class="sxs-lookup"><span data-stu-id="5af6a-130">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="5af6a-131">(Em particular, os aplicativos não devem chamar a função [CreateMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante o processamento do mim \_ MOREDATA.) Em vez disso, o aplicativo deve posicionar os dados de evento em um buffer e, em seguida, retornar.</span><span class="sxs-lookup"><span data-stu-id="5af6a-131">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="5af6a-132">Quando um aplicativo recebe uma mensagem de [**\_ dados do mim**](mim-data.md) após uma série de mensagens do mim \_ MOREDATA, ele se deparou com eventos de entrada de Midi e pode chamar com segurança funções de uso intensivo de tempo.</span><span class="sxs-lookup"><span data-stu-id="5af6a-132">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="5af6a-133">As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="5af6a-133">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="5af6a-134">Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida.</span><span class="sxs-lookup"><span data-stu-id="5af6a-134">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="5af6a-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5af6a-135">Requirements</span></span>



| <span data-ttu-id="5af6a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5af6a-136">Requirement</span></span> | <span data-ttu-id="5af6a-137">Valor</span><span class="sxs-lookup"><span data-stu-id="5af6a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af6a-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5af6a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5af6a-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5af6a-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5af6a-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5af6a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5af6a-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5af6a-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5af6a-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5af6a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5af6a-143"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5af6a-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5af6a-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="5af6a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af6a-145">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="5af6a-145">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="5af6a-146">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="5af6a-146">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


---
title: MIM_MOREDATA mensagem (Mmsystem.h)
description: A mensagem MIM MOREDATA é enviada para uma função de retorno de chamada de entrada MIDI quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens MIM DATA rápido o suficiente para acompanhar o driver de dispositivo de \_ \_ entrada.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA mensagem Multimídia do Windows
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
ms.openlocfilehash: c6342823e13a085b377a3e71f28a0f9ff016681c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119401"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="22759-104">Mensagem MIM \_ MOREDATA</span><span class="sxs-lookup"><span data-stu-id="22759-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="22759-105">A **mensagem MIM \_ MOREDATA** é enviada para uma função de retorno de chamada de entrada MIDI quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens [**MIM \_ DATA**](mim-data.md) rápido o suficiente para acompanhar o driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="22759-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="22759-106">A função de retorno de chamada recebe essa mensagem somente quando o aplicativo especifica o STATUS de E/S MIDI na chamada para a \_ \_ função [**midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)</span><span class="sxs-lookup"><span data-stu-id="22759-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="22759-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22759-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22759-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="22759-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="22759-109">Especifica a mensagem MIDI recebida.</span><span class="sxs-lookup"><span data-stu-id="22759-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="22759-110">A mensagem é empacotada em um **valor DWORD** da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="22759-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="22759-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="22759-111">Requirement</span></span> | <span data-ttu-id="22759-112">Valor</span><span class="sxs-lookup"><span data-stu-id="22759-112">Value</span></span> | <span data-ttu-id="22759-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="22759-113">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="22759-114">Palavra alta</span><span class="sxs-lookup"><span data-stu-id="22759-114">High word</span></span> | <span data-ttu-id="22759-115">Byte de ordem alta</span><span class="sxs-lookup"><span data-stu-id="22759-115">High-order byte</span></span> | <span data-ttu-id="22759-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="22759-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="22759-117">Byte de baixa ordem</span><span class="sxs-lookup"><span data-stu-id="22759-117">Low-order byte</span></span>  | <span data-ttu-id="22759-118">Contém um segundo byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="22759-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="22759-119">Palavra baixa</span><span class="sxs-lookup"><span data-stu-id="22759-119">Low word</span></span>  | <span data-ttu-id="22759-120">Byte de ordem alta</span><span class="sxs-lookup"><span data-stu-id="22759-120">High-order byte</span></span> | <span data-ttu-id="22759-121">Contém o primeiro byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="22759-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="22759-122">Byte de baixa ordem</span><span class="sxs-lookup"><span data-stu-id="22759-122">Low-order byte</span></span>  | <span data-ttu-id="22759-123">Contém o status MIDI.</span><span class="sxs-lookup"><span data-stu-id="22759-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="22759-124">Os dois bytes de dados MIDI são opcionais, dependendo do byte de status MIDI.</span><span class="sxs-lookup"><span data-stu-id="22759-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="22759-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="22759-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="22759-126">Especifica a hora em que a mensagem foi recebida pelo driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="22759-126">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="22759-127">O carimbo de data/hora é especificado em milissegundos, começando em 0 quando a [**função midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) foi chamada.</span><span class="sxs-lookup"><span data-stu-id="22759-127">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22759-128">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="22759-128">Return Value</span></span>

<span data-ttu-id="22759-129">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="22759-129">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22759-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="22759-130">Remarks</span></span>

<span data-ttu-id="22759-131">Um aplicativo deve fazer apenas uma quantidade mínima de processamento de mensagens MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="22759-131">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="22759-132">(Em particular, os aplicativos não devem chamar a [função PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante o processamento do MIM \_ MOREDATA.) Em vez disso, o aplicativo deve colocar os dados do evento em um buffer e, em seguida, retornar.</span><span class="sxs-lookup"><span data-stu-id="22759-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="22759-133">Quando um aplicativo recebe uma mensagem [**MIM \_ DATA**](mim-data.md) após uma série de mensagens MIM MOREDATA, ele foi atualizado com eventos MIDI de entrada e pode chamar funções com uso intensivo \_ de tempo com segurança.</span><span class="sxs-lookup"><span data-stu-id="22759-133">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="22759-134">As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status MIDI.</span><span class="sxs-lookup"><span data-stu-id="22759-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="22759-135">Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida.</span><span class="sxs-lookup"><span data-stu-id="22759-135">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="22759-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22759-136">Requirements</span></span>



| <span data-ttu-id="22759-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="22759-137">Requirement</span></span> | <span data-ttu-id="22759-138">Valor</span><span class="sxs-lookup"><span data-stu-id="22759-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22759-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22759-139">Minimum supported client</span></span><br/> | <span data-ttu-id="22759-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22759-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="22759-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22759-141">Minimum supported server</span></span><br/> | <span data-ttu-id="22759-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22759-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="22759-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="22759-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="22759-144"><dt>Mmsystem.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="22759-144"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22759-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="22759-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22759-146">MIDI (Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="22759-146">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="22759-147">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="22759-147">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


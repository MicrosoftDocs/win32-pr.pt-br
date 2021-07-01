---
title: Mensagem de MIM_DATA (mmsystem. h)
description: A mensagem de dados do MIM \_ é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- Multimídia do Windows de mensagem MIM_DATA
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11d2701d488fe29ae6d0bc0742c32c803b28076
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118401"
---
# <a name="mim_data-message"></a><span data-ttu-id="0c743-104">Mensagem de dados do MIM \_</span><span class="sxs-lookup"><span data-stu-id="0c743-104">MIM\_DATA message</span></span>

<span data-ttu-id="0c743-105">A mensagem de **\_ dados do mim** é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="0c743-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="0c743-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c743-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c743-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="0c743-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="0c743-108">Mensagem MIDI recebida.</span><span class="sxs-lookup"><span data-stu-id="0c743-108">MIDI message that was received.</span></span> <span data-ttu-id="0c743-109">A mensagem é empacotada em um valor de doubleword da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0c743-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="0c743-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c743-110">Requirement</span></span> | <span data-ttu-id="0c743-111">Valor</span><span class="sxs-lookup"><span data-stu-id="0c743-111">Value</span></span> | <span data-ttu-id="0c743-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c743-112">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="0c743-113">Palavra alta</span><span class="sxs-lookup"><span data-stu-id="0c743-113">High word</span></span> | <span data-ttu-id="0c743-114">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="0c743-114">High-order byte</span></span> | <span data-ttu-id="0c743-115">Não usado.</span><span class="sxs-lookup"><span data-stu-id="0c743-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="0c743-116">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="0c743-116">Low-order byte</span></span>  | <span data-ttu-id="0c743-117">Contém um segundo byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="0c743-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="0c743-118">Palavra inferior</span><span class="sxs-lookup"><span data-stu-id="0c743-118">Low word</span></span>  | <span data-ttu-id="0c743-119">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="0c743-119">High-order byte</span></span> | <span data-ttu-id="0c743-120">Contém o primeiro byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="0c743-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="0c743-121">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="0c743-121">Low-order byte</span></span>  | <span data-ttu-id="0c743-122">Contém o status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="0c743-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="0c743-123">Os dois bytes de dados MIDI são opcionais, dependendo do byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="0c743-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="0c743-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="0c743-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="0c743-125">Hora em que a mensagem foi recebida pelo driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="0c743-125">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="0c743-126">O carimbo de data/hora é especificado em milissegundos, começando em zero quando a função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) foi chamada.</span><span class="sxs-lookup"><span data-stu-id="0c743-126">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c743-127">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0c743-127">Return Value</span></span>

<span data-ttu-id="0c743-128">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0c743-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c743-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c743-129">Remarks</span></span>

<span data-ttu-id="0c743-130">As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="0c743-130">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="0c743-131">Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida.</span><span class="sxs-lookup"><span data-stu-id="0c743-131">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c743-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c743-132">Requirements</span></span>



| <span data-ttu-id="0c743-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c743-133">Requirement</span></span> | <span data-ttu-id="0c743-134">Valor</span><span class="sxs-lookup"><span data-stu-id="0c743-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c743-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c743-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0c743-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0c743-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0c743-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c743-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0c743-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0c743-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0c743-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0c743-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c743-140"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c743-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c743-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c743-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c743-142">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="0c743-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="0c743-143">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="0c743-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


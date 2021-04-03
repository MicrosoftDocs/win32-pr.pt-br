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
ms.openlocfilehash: 48f96d2c23e64700a7a923cdd7633dabfcba9d1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824823"
---
# <a name="mim_data-message"></a><span data-ttu-id="e76fa-104">Mensagem de dados do MIM \_</span><span class="sxs-lookup"><span data-stu-id="e76fa-104">MIM\_DATA message</span></span>

<span data-ttu-id="e76fa-105">A mensagem de **\_ dados do mim** é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="e76fa-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="e76fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e76fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e76fa-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="e76fa-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="e76fa-108">Mensagem MIDI recebida.</span><span class="sxs-lookup"><span data-stu-id="e76fa-108">MIDI message that was received.</span></span> <span data-ttu-id="e76fa-109">A mensagem é empacotada em um valor de doubleword da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e76fa-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="e76fa-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e76fa-110">Requirement</span></span> | <span data-ttu-id="e76fa-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e76fa-111">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="e76fa-112">Palavra alta</span><span class="sxs-lookup"><span data-stu-id="e76fa-112">High word</span></span> | <span data-ttu-id="e76fa-113">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="e76fa-113">High-order byte</span></span> | <span data-ttu-id="e76fa-114">Não usado.</span><span class="sxs-lookup"><span data-stu-id="e76fa-114">Not used.</span></span>                                           |
|           | <span data-ttu-id="e76fa-115">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="e76fa-115">Low-order byte</span></span>  | <span data-ttu-id="e76fa-116">Contém um segundo byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="e76fa-116">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="e76fa-117">Palavra inferior</span><span class="sxs-lookup"><span data-stu-id="e76fa-117">Low word</span></span>  | <span data-ttu-id="e76fa-118">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="e76fa-118">High-order byte</span></span> | <span data-ttu-id="e76fa-119">Contém o primeiro byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="e76fa-119">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="e76fa-120">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="e76fa-120">Low-order byte</span></span>  | <span data-ttu-id="e76fa-121">Contém o status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="e76fa-121">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="e76fa-122">Os dois bytes de dados MIDI são opcionais, dependendo do byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="e76fa-122">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="e76fa-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="e76fa-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="e76fa-124">Hora em que a mensagem foi recebida pelo driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e76fa-124">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="e76fa-125">O carimbo de data/hora é especificado em milissegundos, começando em zero quando a função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) foi chamada.</span><span class="sxs-lookup"><span data-stu-id="e76fa-125">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e76fa-126">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e76fa-126">Return Value</span></span>

<span data-ttu-id="e76fa-127">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e76fa-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e76fa-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="e76fa-128">Remarks</span></span>

<span data-ttu-id="e76fa-129">As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="e76fa-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="e76fa-130">Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida.</span><span class="sxs-lookup"><span data-stu-id="e76fa-130">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="e76fa-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e76fa-131">Requirements</span></span>



| <span data-ttu-id="e76fa-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e76fa-132">Requirement</span></span> | <span data-ttu-id="e76fa-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e76fa-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e76fa-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e76fa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e76fa-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e76fa-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e76fa-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e76fa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e76fa-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e76fa-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e76fa-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e76fa-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e76fa-139"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e76fa-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e76fa-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e76fa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76fa-141">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="e76fa-141">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="e76fa-142">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="e76fa-142">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


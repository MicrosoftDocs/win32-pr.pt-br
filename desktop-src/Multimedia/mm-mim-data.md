---
title: Mensagem de MM_MIM_DATA (mmsystem. h)
description: A \_ mensagem de dados do mim mm \_ é enviada para uma janela quando uma mensagem MIDI completa é recebida por um dispositivo de entrada MIDI.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- Multimídia do Windows de mensagem MM_MIM_DATA
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa8c015ba5e08302f7567fe8f474bedca74d3064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008973"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="6f363-104">Mensagem de dados do \_ mim mm \_</span><span class="sxs-lookup"><span data-stu-id="6f363-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="6f363-105">A mensagem de **\_ \_ dados do mim mm** é enviada para uma janela quando uma mensagem MIDI completa é recebida por um dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="6f363-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="6f363-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f363-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f363-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="6f363-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="6f363-108">Identificador para o dispositivo de entrada MIDI que recebeu a mensagem MIDI.</span><span class="sxs-lookup"><span data-stu-id="6f363-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="6f363-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="6f363-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="6f363-110">Mensagem MIDI recebida.</span><span class="sxs-lookup"><span data-stu-id="6f363-110">MIDI message that was received.</span></span> <span data-ttu-id="6f363-111">A mensagem é empacotada em um valor de doubleword da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6f363-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="6f363-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f363-112">Requirement</span></span> | <span data-ttu-id="6f363-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6f363-113">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="6f363-114">Palavra alta</span><span class="sxs-lookup"><span data-stu-id="6f363-114">High word</span></span> | <span data-ttu-id="6f363-115">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="6f363-115">High-order byte</span></span> | <span data-ttu-id="6f363-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="6f363-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="6f363-117">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="6f363-117">Low-order byte</span></span>  | <span data-ttu-id="6f363-118">Contém um segundo byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="6f363-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="6f363-119">Palavra inferior</span><span class="sxs-lookup"><span data-stu-id="6f363-119">Low word</span></span>  | <span data-ttu-id="6f363-120">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="6f363-120">High-order byte</span></span> | <span data-ttu-id="6f363-121">Contém o primeiro byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="6f363-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="6f363-122">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="6f363-122">Low-order byte</span></span>  | <span data-ttu-id="6f363-123">Contém o status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="6f363-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="6f363-124">Os dois bytes de dados MIDI são opcionais, dependendo do byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="6f363-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f363-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6f363-125">Return Value</span></span>

<span data-ttu-id="6f363-126">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6f363-126">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f363-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f363-127">Remarks</span></span>

<span data-ttu-id="6f363-128">As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="6f363-128">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="6f363-129">Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida.</span><span class="sxs-lookup"><span data-stu-id="6f363-129">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="6f363-130">Não há carimbo de data/hora disponível com esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f363-130">No time stamp is available with this message.</span></span> <span data-ttu-id="6f363-131">Para dados de entrada com carimbo de data/hora, você deve usar as mensagens que são enviadas para funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6f363-131">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f363-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f363-132">Requirements</span></span>



| <span data-ttu-id="6f363-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f363-133">Requirement</span></span> | <span data-ttu-id="6f363-134">Valor</span><span class="sxs-lookup"><span data-stu-id="6f363-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f363-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f363-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6f363-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f363-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6f363-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f363-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6f363-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f363-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6f363-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6f363-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f363-140"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f363-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f363-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f363-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f363-142">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="6f363-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="6f363-143">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="6f363-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 






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
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119691"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="f1cd6-104">Mensagem de dados do \_ mim mm \_</span><span class="sxs-lookup"><span data-stu-id="f1cd6-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="f1cd6-105">A mensagem de **\_ \_ dados do mim mm** é enviada para uma janela quando uma mensagem MIDI completa é recebida por um dispositivo de entrada MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="f1cd6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1cd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1cd6-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="f1cd6-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="f1cd6-108">Identificador para o dispositivo de entrada MIDI que recebeu a mensagem MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="f1cd6-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="f1cd6-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="f1cd6-110">Mensagem MIDI recebida.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-110">MIDI message that was received.</span></span> <span data-ttu-id="f1cd6-111">A mensagem é empacotada em um valor de doubleword da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f1cd6-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="f1cd6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1cd6-112">Requirement</span></span> | <span data-ttu-id="f1cd6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f1cd6-113">Value</span></span> | <span data-ttu-id="f1cd6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1cd6-114">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="f1cd6-115">Palavra alta</span><span class="sxs-lookup"><span data-stu-id="f1cd6-115">High word</span></span> | <span data-ttu-id="f1cd6-116">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="f1cd6-116">High-order byte</span></span> | <span data-ttu-id="f1cd6-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="f1cd6-118">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="f1cd6-118">Low-order byte</span></span>  | <span data-ttu-id="f1cd6-119">Contém um segundo byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="f1cd6-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="f1cd6-120">Palavra inferior</span><span class="sxs-lookup"><span data-stu-id="f1cd6-120">Low word</span></span>  | <span data-ttu-id="f1cd6-121">Byte de ordem superior</span><span class="sxs-lookup"><span data-stu-id="f1cd6-121">High-order byte</span></span> | <span data-ttu-id="f1cd6-122">Contém o primeiro byte de dados MIDI (quando necessário).</span><span class="sxs-lookup"><span data-stu-id="f1cd6-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="f1cd6-123">Byte de ordem inferior</span><span class="sxs-lookup"><span data-stu-id="f1cd6-123">Low-order byte</span></span>  | <span data-ttu-id="f1cd6-124">Contém o status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="f1cd6-125">Os dois bytes de dados MIDI são opcionais, dependendo do byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1cd6-126">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f1cd6-126">Return Value</span></span>

<span data-ttu-id="f1cd6-127">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1cd6-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1cd6-128">Remarks</span></span>

<span data-ttu-id="f1cd6-129">As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status de MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="f1cd6-130">Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-130">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="f1cd6-131">Não há carimbo de data/hora disponível com esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-131">No time stamp is available with this message.</span></span> <span data-ttu-id="f1cd6-132">Para dados de entrada com carimbo de data/hora, você deve usar as mensagens que são enviadas para funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="f1cd6-132">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1cd6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1cd6-133">Requirements</span></span>



| <span data-ttu-id="f1cd6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1cd6-134">Requirement</span></span> | <span data-ttu-id="f1cd6-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f1cd6-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1cd6-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1cd6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f1cd6-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f1cd6-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f1cd6-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1cd6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f1cd6-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f1cd6-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f1cd6-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f1cd6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1cd6-141"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1cd6-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1cd6-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1cd6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1cd6-143">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="f1cd6-143">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="f1cd6-144">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="f1cd6-144">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 






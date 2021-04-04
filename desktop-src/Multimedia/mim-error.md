---
title: Mensagem de MIM_ERROR (mmsystem. h)
description: A mensagem de erro do MIM \_ é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem MIDI inválida é recebida.
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- Multimídia do Windows de mensagem MIM_ERROR
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add5b675a557ab25d41e79d99864e090364d384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085245"
---
# <a name="mim_error-message"></a><span data-ttu-id="a68b9-104">Mensagem de erro do MIM \_</span><span class="sxs-lookup"><span data-stu-id="a68b9-104">MIM\_ERROR message</span></span>

<span data-ttu-id="a68b9-105">A mensagem de **\_ erro do mim** é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem MIDI inválida é recebida.</span><span class="sxs-lookup"><span data-stu-id="a68b9-105">The **MIM\_ERROR** message is sent to a MIDI input callback function when an invalid MIDI message is received.</span></span>


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="a68b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a68b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a68b9-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="a68b9-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="a68b9-108">Mensagem MIDI inválida recebida.</span><span class="sxs-lookup"><span data-stu-id="a68b9-108">Invalid MIDI message that was received.</span></span> <span data-ttu-id="a68b9-109">A mensagem é empacotada em um valor doubleword com o primeiro byte da mensagem no byte de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="a68b9-109">The message is packed into a doubleword value with the first byte of the message in the low-order byte.</span></span>

</dd> <dt>

<span data-ttu-id="a68b9-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="a68b9-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="a68b9-111">Hora em que a mensagem foi recebida pelo driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a68b9-111">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="a68b9-112">O carimbo de data/hora é especificado em milissegundos, começando em zero quando a função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) foi chamada.</span><span class="sxs-lookup"><span data-stu-id="a68b9-112">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a68b9-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a68b9-113">Return Value</span></span>

<span data-ttu-id="a68b9-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a68b9-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a68b9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a68b9-115">Requirements</span></span>



| <span data-ttu-id="a68b9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a68b9-116">Requirement</span></span> | <span data-ttu-id="a68b9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a68b9-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a68b9-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a68b9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a68b9-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a68b9-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a68b9-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a68b9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a68b9-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a68b9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a68b9-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a68b9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a68b9-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a68b9-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a68b9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a68b9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a68b9-125">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="a68b9-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="a68b9-126">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="a68b9-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


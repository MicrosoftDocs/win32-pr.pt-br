---
title: Mensagem de MIM_LONGERROR (mmsystem. h)
description: A mensagem do MIM \_ LONGERROR é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem exclusiva de sistema MIDI inválida ou incompleta é recebida.
ms.assetid: 7e3b0716-33c4-449c-a200-e5ba72428dc1
keywords:
- Multimídia do Windows de mensagem MIM_LONGERROR
topic_type:
- apiref
api_name:
- MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631c4fdcd31eef01d691aea80100427d116ae7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454744"
---
# <a name="mim_longerror-message"></a><span data-ttu-id="bfb3d-104">Mensagem do MIM \_ LONGERROR</span><span class="sxs-lookup"><span data-stu-id="bfb3d-104">MIM\_LONGERROR message</span></span>

<span data-ttu-id="bfb3d-105">A mensagem do **mim \_ LONGERROR** é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem exclusiva de sistema MIDI inválida ou incompleta é recebida.</span><span class="sxs-lookup"><span data-stu-id="bfb3d-105">The **MIM\_LONGERROR** message is sent to a MIDI input callback function when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MIM_LONGERROR 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="bfb3d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfb3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfb3d-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="bfb3d-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="bfb3d-108">Ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identificando o buffer que contém a mensagem inválida.</span><span class="sxs-lookup"><span data-stu-id="bfb3d-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="bfb3d-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="bfb3d-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="bfb3d-110">Hora em que os dados foram recebidos pelo driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="bfb3d-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="bfb3d-111">O carimbo de data/hora é especificado em milissegundos, começando em zero quando a função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) foi chamada.</span><span class="sxs-lookup"><span data-stu-id="bfb3d-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfb3d-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bfb3d-112">Return Value</span></span>

<span data-ttu-id="bfb3d-113">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bfb3d-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfb3d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfb3d-114">Remarks</span></span>

<span data-ttu-id="bfb3d-115">O buffer retornado pode não estar cheio.</span><span class="sxs-lookup"><span data-stu-id="bfb3d-115">The returned buffer might not be full.</span></span> <span data-ttu-id="bfb3d-116">Para determinar o número de bytes registrados no buffer retornado, use o membro **dwBytesRecorded** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) especificada por *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="bfb3d-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfb3d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfb3d-117">Requirements</span></span>



| <span data-ttu-id="bfb3d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfb3d-118">Requirement</span></span> | <span data-ttu-id="bfb3d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bfb3d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb3d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfb3d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bfb3d-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bfb3d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bfb3d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfb3d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bfb3d-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bfb3d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bfb3d-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bfb3d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfb3d-125"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfb3d-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfb3d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfb3d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfb3d-127">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="bfb3d-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="bfb3d-128">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="bfb3d-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


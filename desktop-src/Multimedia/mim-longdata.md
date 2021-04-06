---
title: Mensagem de MIM_LONGDATA (mmsystem. h)
description: A mensagem do MIM \_ LONGDATA é enviada para uma função de retorno de chamada de entrada de Midi quando um buffer exclusivo do sistema é preenchido com dados e está sendo retornado para o aplicativo.
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- Multimídia do Windows de mensagem MIM_LONGDATA
topic_type:
- apiref
api_name:
- MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc5f83b1f0468540da18d0d8317dae42cbf33bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086505"
---
# <a name="mim_longdata-message"></a><span data-ttu-id="a6249-104">Mensagem do MIM \_ LONGDATA</span><span class="sxs-lookup"><span data-stu-id="a6249-104">MIM\_LONGDATA message</span></span>

<span data-ttu-id="a6249-105">A mensagem do **mim \_ LONGDATA** é enviada para uma função de retorno de chamada de entrada de Midi quando um buffer exclusivo do sistema é preenchido com dados e está sendo retornado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6249-105">The **MIM\_LONGDATA** message is sent to a MIDI input callback function when a system-exclusive buffer has been filled with data and is being returned to the application.</span></span>


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="a6249-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6249-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6249-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="a6249-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="a6249-108">Ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="a6249-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a6249-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="a6249-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="a6249-110">Hora em que os dados foram recebidos pelo driver de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a6249-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="a6249-111">O carimbo de data/hora é especificado em milissegundos, começando em zero quando a função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) foi chamada.</span><span class="sxs-lookup"><span data-stu-id="a6249-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6249-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a6249-112">Return Value</span></span>

<span data-ttu-id="a6249-113">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a6249-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6249-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6249-114">Remarks</span></span>

<span data-ttu-id="a6249-115">O buffer retornado pode não estar cheio.</span><span class="sxs-lookup"><span data-stu-id="a6249-115">The returned buffer might not be full.</span></span> <span data-ttu-id="a6249-116">Para determinar o número de bytes registrados no buffer retornado, use o membro **dwBytesRecorded** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) especificada por *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="a6249-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6249-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6249-117">Requirements</span></span>



| <span data-ttu-id="a6249-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6249-118">Requirement</span></span> | <span data-ttu-id="a6249-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a6249-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6249-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6249-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a6249-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a6249-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a6249-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6249-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a6249-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a6249-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a6249-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a6249-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6249-125"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6249-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6249-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6249-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6249-127">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="a6249-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="a6249-128">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="a6249-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


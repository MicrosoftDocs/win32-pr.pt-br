---
title: Mensagem de MM_MIM_LONGDATA (mmsystem. h)
description: A \_ mensagem mm mim \_ LONGDATA é enviada para uma janela quando uma mensagem exclusiva do sistema MIDI é recebida ou quando um buffer é preenchido com dados exclusivos do sistema.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- Multimídia do Windows de mensagem MM_MIM_LONGDATA
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf1900ef2e9394b9d8772747eba873f8d607f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086297"
---
# <a name="mm_mim_longdata-message"></a><span data-ttu-id="16c13-104">MM \_ mensagem do mim \_ LONGDATA</span><span class="sxs-lookup"><span data-stu-id="16c13-104">MM\_MIM\_LONGDATA message</span></span>

<span data-ttu-id="16c13-105">A mensagem **mm \_ mim \_ LONGDATA** é enviada para uma janela quando uma mensagem exclusiva do sistema MIDI é recebida ou quando um buffer é preenchido com dados exclusivos do sistema.</span><span class="sxs-lookup"><span data-stu-id="16c13-105">The **MM\_MIM\_LONGDATA** message is sent to a window when either a complete MIDI system-exclusive message is received or when a buffer has been filled with system-exclusive data.</span></span>


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="16c13-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16c13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16c13-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="16c13-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="16c13-108">Identificador para o dispositivo de entrada MIDI que recebeu os dados.</span><span class="sxs-lookup"><span data-stu-id="16c13-108">Handle to the MIDI input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="16c13-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="16c13-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="16c13-110">Ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identificando o buffer.</span><span class="sxs-lookup"><span data-stu-id="16c13-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16c13-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="16c13-111">Return Value</span></span>

<span data-ttu-id="16c13-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="16c13-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16c13-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="16c13-113">Remarks</span></span>

<span data-ttu-id="16c13-114">O buffer retornado pode não estar cheio.</span><span class="sxs-lookup"><span data-stu-id="16c13-114">The returned buffer might not be full.</span></span> <span data-ttu-id="16c13-115">Para determinar o número de bytes registrados no buffer retornado, use o membro **dwBytesRecorded** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) apontada por *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="16c13-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure pointed to by *lpMidiHdr*.</span></span>

<span data-ttu-id="16c13-116">Não há carimbo de data/hora disponível com esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="16c13-116">No time stamp is available with this message.</span></span> <span data-ttu-id="16c13-117">Para dados de entrada com carimbo de data/hora, você deve usar as mensagens que são enviadas para funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="16c13-117">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c13-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16c13-118">Requirements</span></span>



| <span data-ttu-id="16c13-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="16c13-119">Requirement</span></span> | <span data-ttu-id="16c13-120">Valor</span><span class="sxs-lookup"><span data-stu-id="16c13-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16c13-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16c13-121">Minimum supported client</span></span><br/> | <span data-ttu-id="16c13-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="16c13-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="16c13-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16c13-123">Minimum supported server</span></span><br/> | <span data-ttu-id="16c13-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="16c13-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="16c13-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="16c13-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="16c13-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16c13-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16c13-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="16c13-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c13-128">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="16c13-128">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="16c13-129">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="16c13-129">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


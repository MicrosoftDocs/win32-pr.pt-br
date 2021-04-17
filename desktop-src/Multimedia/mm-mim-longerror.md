---
title: Mensagem de MM_MIM_LONGERROR (mmsystem. h)
description: A \_ mensagem mm LONGERROR do mim \_ é enviada para uma janela quando uma mensagem exclusiva de sistema MIDI inválida ou incompleta é recebida.
ms.assetid: 2de4c2f8-2ded-4994-934c-6e72c95637b2
keywords:
- Multimídia do Windows de mensagem MM_MIM_LONGERROR
topic_type:
- apiref
api_name:
- MM_MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e274faca26a90a5cd3b3915a7e8e1ed27bcfd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813140"
---
# <a name="mm_mim_longerror-message"></a><span data-ttu-id="6ae86-104">MM \_ mensagem do mim \_ LONGERROR</span><span class="sxs-lookup"><span data-stu-id="6ae86-104">MM\_MIM\_LONGERROR message</span></span>

<span data-ttu-id="6ae86-105">A **mensagem \_ mm \_ LONGERROR do mim** é enviada para uma janela quando uma mensagem exclusiva de sistema MIDI inválida ou incompleta é recebida.</span><span class="sxs-lookup"><span data-stu-id="6ae86-105">The **MM\_MIM\_LONGERROR** message is sent to a window when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MM_MIM_LONGERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="6ae86-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ae86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae86-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="6ae86-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="6ae86-108">Identificador para o dispositivo de entrada MIDI que recebeu a mensagem inválida.</span><span class="sxs-lookup"><span data-stu-id="6ae86-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="6ae86-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="6ae86-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="6ae86-110">Ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identificando o buffer que contém a mensagem inválida.</span><span class="sxs-lookup"><span data-stu-id="6ae86-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae86-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6ae86-111">Return Value</span></span>

<span data-ttu-id="6ae86-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6ae86-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ae86-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ae86-113">Remarks</span></span>

<span data-ttu-id="6ae86-114">O buffer retornado pode não estar cheio.</span><span class="sxs-lookup"><span data-stu-id="6ae86-114">The returned buffer might not be full.</span></span> <span data-ttu-id="6ae86-115">Para determinar o número de bytes registrados no buffer retornado, use o membro **dwBytesRecorded** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) especificada por *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="6ae86-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae86-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ae86-116">Requirements</span></span>



| <span data-ttu-id="6ae86-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ae86-117">Requirement</span></span> | <span data-ttu-id="6ae86-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ae86-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae86-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ae86-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae86-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ae86-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ae86-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ae86-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae86-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ae86-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6ae86-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6ae86-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ae86-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ae86-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ae86-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ae86-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae86-126">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="6ae86-126">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="6ae86-127">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="6ae86-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 


---
title: Mensagem de MM_MIM_ERROR (mmsystem. h)
description: A mensagem de erro MM do \_ mim \_ é enviada para uma janela quando uma mensagem MIDI inválida é recebida.
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- Multimídia do Windows de mensagem MM_MIM_ERROR
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b45988259601b40a804f9eb8acfbb085bddcda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085240"
---
# <a name="mm_mim_error-message"></a><span data-ttu-id="3d87c-104">Mensagem de erro do \_ mim mm \_</span><span class="sxs-lookup"><span data-stu-id="3d87c-104">MM\_MIM\_ERROR message</span></span>

<span data-ttu-id="3d87c-105">A mensagem de **\_ \_ erro mm do mim** é enviada para uma janela quando uma mensagem MIDI inválida é recebida.</span><span class="sxs-lookup"><span data-stu-id="3d87c-105">The **MM\_MIM\_ERROR** message is sent to a window when an invalid MIDI message is received.</span></span>


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="3d87c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d87c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d87c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="3d87c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="3d87c-108">Identificador para o dispositivo de entrada MIDI que recebeu a mensagem inválida.</span><span class="sxs-lookup"><span data-stu-id="3d87c-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="3d87c-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="3d87c-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="3d87c-110">Mensagem MIDI inválida.</span><span class="sxs-lookup"><span data-stu-id="3d87c-110">Invalid MIDI message.</span></span> <span data-ttu-id="3d87c-111">A mensagem é empacotada em um valor **DWORD** com o primeiro byte da mensagem no byte de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="3d87c-111">The message is packed into a **DWORD** value with the first byte of the message in the low-order byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d87c-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3d87c-112">Return Value</span></span>

<span data-ttu-id="3d87c-113">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3d87c-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d87c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d87c-114">Requirements</span></span>



| <span data-ttu-id="3d87c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d87c-115">Requirement</span></span> | <span data-ttu-id="3d87c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3d87c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d87c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d87c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3d87c-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3d87c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3d87c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d87c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3d87c-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3d87c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3d87c-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3d87c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d87c-122"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d87c-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d87c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d87c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d87c-124">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="3d87c-124">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="3d87c-125">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="3d87c-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 






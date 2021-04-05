---
title: Mensagem de MM_MIM_CLOSE (mmsystem. h)
description: A \_ mensagem de fechamento do mim mm \_ é enviada para uma janela quando um dispositivo de entrada de Midi é fechado.
ms.assetid: 261021aa-4df6-44d8-aad3-5f98b1213459
keywords:
- Multimídia do Windows de mensagem MM_MIM_CLOSE
topic_type:
- apiref
api_name:
- MM_MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ce511365b1faa49faefaf4ed25c5b8befb2288
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918753"
---
# <a name="mm_mim_close-message"></a><span data-ttu-id="b3502-104">Mensagem de fechamento do \_ mim mm \_</span><span class="sxs-lookup"><span data-stu-id="b3502-104">MM\_MIM\_CLOSE message</span></span>

<span data-ttu-id="b3502-105">A mensagem de **\_ \_ fechamento do mim mm** é enviada para uma janela quando um dispositivo de entrada de Midi é fechado.</span><span class="sxs-lookup"><span data-stu-id="b3502-105">The **MM\_MIM\_CLOSE** message is sent to a window when a MIDI input device is closed.</span></span>


```C++
MM_MIM_CLOSE 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b3502-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3502-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3502-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="b3502-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="b3502-108">Identificador para o dispositivo de entrada MIDI que foi fechado.</span><span class="sxs-lookup"><span data-stu-id="b3502-108">Handle to the MIDI input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="b3502-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3502-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b3502-110">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="b3502-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3502-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b3502-111">Return Value</span></span>

<span data-ttu-id="b3502-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b3502-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3502-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3502-113">Remarks</span></span>

<span data-ttu-id="b3502-114">O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="b3502-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3502-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3502-115">Requirements</span></span>



| <span data-ttu-id="b3502-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3502-116">Requirement</span></span> | <span data-ttu-id="b3502-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b3502-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3502-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3502-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b3502-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3502-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b3502-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3502-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b3502-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3502-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b3502-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b3502-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3502-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3502-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3502-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3502-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3502-125">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="b3502-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="b3502-126">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="b3502-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 






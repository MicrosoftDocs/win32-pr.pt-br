---
title: Mensagem de MIM_CLOSE (mmsystem. h)
description: A mensagem de fechamento do MIM \_ é enviada para uma função de retorno de chamada de entrada de Midi quando um dispositivo de entrada MIDI é fechado.
ms.assetid: c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15
keywords:
- Multimídia do Windows de mensagem MIM_CLOSE
topic_type:
- apiref
api_name:
- MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5549d9bef1e802b0b34ab6437b1386519a25d349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499251"
---
# <a name="mim_close-message"></a><span data-ttu-id="330f7-104">Mensagem de fechamento do MIM \_</span><span class="sxs-lookup"><span data-stu-id="330f7-104">MIM\_CLOSE message</span></span>

<span data-ttu-id="330f7-105">A mensagem de **\_ fechamento do mim** é enviada para uma função de retorno de chamada de entrada de Midi quando um dispositivo de entrada MIDI é fechado.</span><span class="sxs-lookup"><span data-stu-id="330f7-105">The **MIM\_CLOSE** message is sent to a MIDI input callback function when a MIDI input device is closed.</span></span>


```C++
MIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="330f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="330f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="330f7-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="330f7-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="330f7-108">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="330f7-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="330f7-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="330f7-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="330f7-110">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="330f7-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="330f7-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="330f7-111">Return Value</span></span>

<span data-ttu-id="330f7-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="330f7-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="330f7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="330f7-113">Remarks</span></span>

<span data-ttu-id="330f7-114">O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="330f7-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="330f7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="330f7-115">Requirements</span></span>



| <span data-ttu-id="330f7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="330f7-116">Requirement</span></span> | <span data-ttu-id="330f7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="330f7-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="330f7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="330f7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="330f7-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="330f7-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="330f7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="330f7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="330f7-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="330f7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="330f7-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="330f7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="330f7-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="330f7-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="330f7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="330f7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="330f7-125">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="330f7-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="330f7-126">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="330f7-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 






---
title: Mensagem de MIM_OPEN (mmsystem. h)
description: A \_ mensagem aberta do mim é enviada para uma função de retorno de chamada de entrada de Midi quando um dispositivo de entrada MIDI é aberto.
ms.assetid: c7a8b856-aedd-457d-8a21-0ec2e9303960
keywords:
- Multimídia do Windows de mensagem MIM_OPEN
topic_type:
- apiref
api_name:
- MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49fcfd05ef7702fbc7bf3108365e49660071ae9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369276"
---
# <a name="mim_open-message"></a><span data-ttu-id="303d7-104">\_Mensagem aberta do mim</span><span class="sxs-lookup"><span data-stu-id="303d7-104">MIM\_OPEN message</span></span>

<span data-ttu-id="303d7-105">A **mensagem \_ aberta do mim** é enviada para uma função de retorno de chamada de entrada de Midi quando um dispositivo de entrada MIDI é aberto.</span><span class="sxs-lookup"><span data-stu-id="303d7-105">The **MIM\_OPEN** message is sent to a MIDI input callback function when a MIDI input device is opened.</span></span>


```C++
MIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="303d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="303d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="303d7-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="303d7-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="303d7-108">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="303d7-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="303d7-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="303d7-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="303d7-110">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="303d7-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="303d7-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="303d7-111">Return Value</span></span>

<span data-ttu-id="303d7-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="303d7-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="303d7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="303d7-113">Requirements</span></span>



| <span data-ttu-id="303d7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="303d7-114">Requirement</span></span> | <span data-ttu-id="303d7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="303d7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="303d7-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="303d7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="303d7-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="303d7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="303d7-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="303d7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="303d7-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="303d7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="303d7-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="303d7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="303d7-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="303d7-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="303d7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="303d7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="303d7-123">MIDI (interface digital de instrumento musical)</span><span class="sxs-lookup"><span data-stu-id="303d7-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="303d7-124">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="303d7-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 






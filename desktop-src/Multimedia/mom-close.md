---
title: Mensagem de MOM_CLOSE (mmsystem. h)
description: A mensagem de fechamento do MOM \_ é enviada para uma função de retorno de chamada de saída de Midi quando um dispositivo de saída de Midi é fechado.
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- Multimídia do Windows de mensagem MOM_CLOSE
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f173daa2fb104305979a72c9a14106175d7d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919067"
---
# <a name="mom_close-message"></a><span data-ttu-id="96d8a-104">Mensagem de fechamento do MOM \_</span><span class="sxs-lookup"><span data-stu-id="96d8a-104">MOM\_CLOSE message</span></span>

<span data-ttu-id="96d8a-105">A mensagem de **\_ fechamento do MOM** é enviada para uma função de retorno de chamada de saída de Midi quando um dispositivo de saída de Midi é fechado.</span><span class="sxs-lookup"><span data-stu-id="96d8a-105">The **MOM\_CLOSE** message is sent to a MIDI output callback function when a MIDI output device is closed.</span></span>


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="96d8a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96d8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d8a-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="96d8a-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="96d8a-108">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="96d8a-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="96d8a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="96d8a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="96d8a-110">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="96d8a-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d8a-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="96d8a-111">Return Value</span></span>

<span data-ttu-id="96d8a-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="96d8a-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96d8a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="96d8a-113">Remarks</span></span>

<span data-ttu-id="96d8a-114">O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="96d8a-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d8a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96d8a-115">Requirements</span></span>



| <span data-ttu-id="96d8a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d8a-116">Requirement</span></span> | <span data-ttu-id="96d8a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="96d8a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d8a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96d8a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="96d8a-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96d8a-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="96d8a-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96d8a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="96d8a-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96d8a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="96d8a-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="96d8a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="96d8a-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96d8a-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96d8a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="96d8a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d8a-125">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="96d8a-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 






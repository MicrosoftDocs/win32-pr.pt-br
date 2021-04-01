---
title: Mensagem de MOM_OPEN (mmsystem. h)
description: A \_ mensagem aberta do MOM é enviada para uma função de retorno de chamada de saída de Midi quando um dispositivo de saída de Midi é aberto.
ms.assetid: f3360482-7d16-419c-b5d1-0dd3a6e3c690
keywords:
- Multimídia do Windows de mensagem MOM_OPEN
topic_type:
- apiref
api_name:
- MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24072aad6bff9ce192460c2c8525da4506f32746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645115"
---
# <a name="mom_open-message"></a><span data-ttu-id="bc6a5-104">\_Mensagem aberta do MOM</span><span class="sxs-lookup"><span data-stu-id="bc6a5-104">MOM\_OPEN message</span></span>

<span data-ttu-id="bc6a5-105">A **mensagem \_ aberta do MOM** é enviada para uma função de retorno de chamada de saída de Midi quando um dispositivo de saída de Midi é aberto.</span><span class="sxs-lookup"><span data-stu-id="bc6a5-105">The **MOM\_OPEN** message is sent to a MIDI output callback function when a MIDI output device is opened.</span></span>


```C++
MOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="bc6a5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc6a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc6a5-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="bc6a5-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="bc6a5-108">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="bc6a5-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="bc6a5-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="bc6a5-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="bc6a5-110">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="bc6a5-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc6a5-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bc6a5-111">Return Value</span></span>

<span data-ttu-id="bc6a5-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bc6a5-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc6a5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc6a5-113">Requirements</span></span>



| <span data-ttu-id="bc6a5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc6a5-114">Requirement</span></span> | <span data-ttu-id="bc6a5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bc6a5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6a5-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc6a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc6a5-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bc6a5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bc6a5-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc6a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc6a5-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bc6a5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bc6a5-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bc6a5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc6a5-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc6a5-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc6a5-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc6a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc6a5-123">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="bc6a5-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 






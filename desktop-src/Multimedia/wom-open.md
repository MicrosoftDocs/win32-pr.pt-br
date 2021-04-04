---
title: Mensagem de WOM_OPEN (mmsystem. h)
description: A \_ mensagem de abertura wom é enviada para uma função de retorno de chamada de saída de áudio de forma de onda quando um dispositivo de saída de wave-áudio é aberto.
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- Multimídia do Windows de mensagem WOM_OPEN
topic_type:
- apiref
api_name:
- WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfca721019b28a5bf039e8c56c75892d85bd5e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085141"
---
# <a name="wom_open-message"></a><span data-ttu-id="0aa2e-104">WOM \_ Abrir mensagem</span><span class="sxs-lookup"><span data-stu-id="0aa2e-104">WOM\_OPEN message</span></span>

<span data-ttu-id="0aa2e-105">A mensagem de **\_ abertura wom** é enviada para uma função de retorno de chamada de saída de áudio de forma de onda quando um dispositivo de saída de wave-áudio é aberto.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-105">The **WOM\_OPEN** message is sent to a waveform-audio output callback function when a waveform-audio output device is opened.</span></span>


```C++
WOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="0aa2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0aa2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa2e-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0aa2e-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0aa2e-108">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0aa2e-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0aa2e-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0aa2e-110">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa2e-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0aa2e-111">Return Value</span></span>

<span data-ttu-id="0aa2e-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa2e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aa2e-113">Requirements</span></span>



| <span data-ttu-id="0aa2e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa2e-114">Requirement</span></span> | <span data-ttu-id="0aa2e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0aa2e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa2e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0aa2e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa2e-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0aa2e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0aa2e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0aa2e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa2e-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0aa2e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0aa2e-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0aa2e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa2e-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa2e-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aa2e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0aa2e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa2e-123">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="0aa2e-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="0aa2e-124">Mensagens de formato de onda</span><span class="sxs-lookup"><span data-stu-id="0aa2e-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 






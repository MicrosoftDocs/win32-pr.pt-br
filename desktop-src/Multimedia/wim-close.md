---
title: Mensagem de WIM_CLOSE (mmsystem. h)
description: A \_ mensagem wim Close é enviada para a função de retorno de chamada de entrada de áudio de forma de onda fornecida quando um dispositivo de entrada de forma de onda-áudio é fechado. O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.
ms.assetid: 3774b8b4-b03b-49e7-b9cd-cf3f194df847
keywords:
- Multimídia do Windows de mensagem WIM_CLOSE
topic_type:
- apiref
api_name:
- WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6028ac6c45aa013138aab227e79d8d210ad70bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455813"
---
# <a name="wim_close-message"></a><span data-ttu-id="47108-105">\_Fechar mensagem wim</span><span class="sxs-lookup"><span data-stu-id="47108-105">WIM\_CLOSE message</span></span>

<span data-ttu-id="47108-106">A mensagem **wim \_ Close** é enviada para a função de retorno de chamada de entrada de áudio de forma de onda fornecida quando um dispositivo de entrada de forma de onda-áudio é fechado.</span><span class="sxs-lookup"><span data-stu-id="47108-106">The **WIM\_CLOSE** message is sent to the given waveform-audio input callback function when a waveform-audio input device is closed.</span></span> <span data-ttu-id="47108-107">O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="47108-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="47108-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47108-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47108-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="47108-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="47108-110">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="47108-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="47108-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="47108-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="47108-112">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="47108-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47108-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="47108-113">Return Value</span></span>

<span data-ttu-id="47108-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="47108-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="47108-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47108-115">Requirements</span></span>



| <span data-ttu-id="47108-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="47108-116">Requirement</span></span> | <span data-ttu-id="47108-117">Valor</span><span class="sxs-lookup"><span data-stu-id="47108-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47108-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47108-118">Minimum supported client</span></span><br/> | <span data-ttu-id="47108-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="47108-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="47108-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47108-120">Minimum supported server</span></span><br/> | <span data-ttu-id="47108-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="47108-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="47108-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="47108-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="47108-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47108-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47108-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="47108-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47108-125">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="47108-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="47108-126">Mensagens de formato de onda</span><span class="sxs-lookup"><span data-stu-id="47108-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 






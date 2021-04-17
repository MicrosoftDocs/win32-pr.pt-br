---
title: Mensagem de WOM_CLOSE (mmsystem. h)
description: A \_ mensagem de fechamento wom é enviada para uma função de retorno de chamada de saída de áudio de forma de onda quando um dispositivo de saída de wave-áudio é fechado. O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- Multimídia do Windows de mensagem WOM_CLOSE
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a802d6eceed018fa0c25591ee9e4b38708e1787e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759625"
---
# <a name="wom_close-message"></a><span data-ttu-id="f9814-105">WOM \_ fechar mensagem</span><span class="sxs-lookup"><span data-stu-id="f9814-105">WOM\_CLOSE message</span></span>

<span data-ttu-id="f9814-106">A mensagem de **\_ fechamento wom** é enviada para uma função de retorno de chamada de saída de áudio de forma de onda quando um dispositivo de saída de wave-áudio é fechado.</span><span class="sxs-lookup"><span data-stu-id="f9814-106">The **WOM\_CLOSE** message is sent to a waveform-audio output callback function when a waveform-audio output device is closed.</span></span> <span data-ttu-id="f9814-107">O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="f9814-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="f9814-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9814-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9814-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f9814-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f9814-110">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f9814-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f9814-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f9814-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f9814-112">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f9814-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9814-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f9814-113">Return Value</span></span>

<span data-ttu-id="f9814-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f9814-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9814-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9814-115">Requirements</span></span>



| <span data-ttu-id="f9814-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9814-116">Requirement</span></span> | <span data-ttu-id="f9814-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f9814-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9814-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9814-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9814-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9814-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f9814-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9814-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9814-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9814-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f9814-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f9814-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9814-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9814-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9814-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9814-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9814-125">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="f9814-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="f9814-126">Mensagens de formato de onda</span><span class="sxs-lookup"><span data-stu-id="f9814-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 






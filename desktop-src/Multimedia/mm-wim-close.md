---
title: Mensagem de MM_WIM_CLOSE (mmsystem. h)
description: A \_ mensagem mm wim \_ Close é enviada para uma janela quando um dispositivo de entrada de forma de onda-áudio é fechado. O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- Multimídia do Windows de mensagem MM_WIM_CLOSE
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d9934ef7045debbcac2f5baf1c2f750d22dad5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008832"
---
# <a name="mm_wim_close-message"></a><span data-ttu-id="c0563-105">MM \_ \_ mensagem de fechamento wim</span><span class="sxs-lookup"><span data-stu-id="c0563-105">MM\_WIM\_CLOSE message</span></span>

<span data-ttu-id="c0563-106">A mensagem **mm \_ wim \_ Close** é enviada para uma janela quando um dispositivo de entrada de forma de onda-áudio é fechado.</span><span class="sxs-lookup"><span data-stu-id="c0563-106">The **MM\_WIM\_CLOSE** message is sent to a window when a waveform-audio input device is closed.</span></span> <span data-ttu-id="c0563-107">O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="c0563-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="c0563-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0563-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0563-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="c0563-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="c0563-110">Identificador para o dispositivo de entrada de wave-áudio que foi fechado.</span><span class="sxs-lookup"><span data-stu-id="c0563-110">Handle to the waveform-audio input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="c0563-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0563-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="c0563-112">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c0563-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0563-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c0563-113">Return Value</span></span>

<span data-ttu-id="c0563-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c0563-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0563-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0563-115">Requirements</span></span>



| <span data-ttu-id="c0563-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0563-116">Requirement</span></span> | <span data-ttu-id="c0563-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c0563-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0563-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0563-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c0563-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c0563-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c0563-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0563-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c0563-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c0563-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c0563-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c0563-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0563-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0563-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0563-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0563-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0563-125">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="c0563-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="c0563-126">Mensagens de formato de onda</span><span class="sxs-lookup"><span data-stu-id="c0563-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 






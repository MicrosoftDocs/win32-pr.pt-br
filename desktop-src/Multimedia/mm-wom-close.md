---
title: Mensagem de MM_WOM_CLOSE (mmsystem. h)
description: A \_ mensagem mm wom \_ fechar é enviada para uma janela quando um dispositivo de saída de wave-áudio é fechado. O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- Multimídia do Windows de mensagem MM_WOM_CLOSE
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dccdae49efc107a513e047282922f3a6de73e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761421"
---
# <a name="mm_wom_close-message"></a><span data-ttu-id="9548f-105">MM \_ wom \_ fechar mensagem</span><span class="sxs-lookup"><span data-stu-id="9548f-105">MM\_WOM\_CLOSE message</span></span>

<span data-ttu-id="9548f-106">A mensagem **mm \_ wom \_ Fechar** é enviada para uma janela quando um dispositivo de saída de wave-áudio é fechado.</span><span class="sxs-lookup"><span data-stu-id="9548f-106">The **MM\_WOM\_CLOSE** message is sent to a window when a waveform-audio output device is closed.</span></span> <span data-ttu-id="9548f-107">O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="9548f-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="9548f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9548f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9548f-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="9548f-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="9548f-110">Identificador para o dispositivo que foi fechado.</span><span class="sxs-lookup"><span data-stu-id="9548f-110">Handle to the device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="9548f-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="9548f-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="9548f-112">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9548f-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9548f-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9548f-113">Return Value</span></span>

<span data-ttu-id="9548f-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9548f-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9548f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9548f-115">Requirements</span></span>



| <span data-ttu-id="9548f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9548f-116">Requirement</span></span> | <span data-ttu-id="9548f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9548f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9548f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9548f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9548f-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9548f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9548f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9548f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9548f-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9548f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9548f-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9548f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9548f-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9548f-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9548f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9548f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9548f-125">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="9548f-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="9548f-126">Mensagens de formato de onda</span><span class="sxs-lookup"><span data-stu-id="9548f-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 






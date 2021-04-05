---
title: Mensagem de MM_WIM_OPEN (mmsystem. h)
description: A \_ mensagem mm wim \_ Open é enviada para uma janela quando um dispositivo de entrada de forma de onda-áudio é aberto.
ms.assetid: 4c646f58-c324-467e-871b-8fc36d5b89bc
keywords:
- Multimídia do Windows de mensagem MM_WIM_OPEN
topic_type:
- apiref
api_name:
- MM_WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff028dcd9dc851d94699ef5cb75707429ba149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009767"
---
# <a name="mm_wim_open-message"></a><span data-ttu-id="760ff-104">MM \_ \_ Abrir mensagem wim</span><span class="sxs-lookup"><span data-stu-id="760ff-104">MM\_WIM\_OPEN message</span></span>

<span data-ttu-id="760ff-105">A mensagem **mm \_ wim \_ Open** é enviada para uma janela quando um dispositivo de entrada de forma de onda-áudio é aberto.</span><span class="sxs-lookup"><span data-stu-id="760ff-105">The **MM\_WIM\_OPEN** message is sent to a window when a waveform-audio input device is opened.</span></span>


```C++
MM_WIM_OPEN 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="760ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="760ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="760ff-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="760ff-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="760ff-108">Identificador para o dispositivo que foi aberto.</span><span class="sxs-lookup"><span data-stu-id="760ff-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="760ff-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="760ff-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="760ff-110">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="760ff-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="760ff-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="760ff-111">Return Value</span></span>

<span data-ttu-id="760ff-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="760ff-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="760ff-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="760ff-113">Requirements</span></span>



| <span data-ttu-id="760ff-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="760ff-114">Requirement</span></span> | <span data-ttu-id="760ff-115">Valor</span><span class="sxs-lookup"><span data-stu-id="760ff-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="760ff-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="760ff-116">Minimum supported client</span></span><br/> | <span data-ttu-id="760ff-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="760ff-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="760ff-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="760ff-118">Minimum supported server</span></span><br/> | <span data-ttu-id="760ff-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="760ff-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="760ff-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="760ff-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="760ff-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="760ff-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="760ff-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="760ff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="760ff-123">Áudio de onda</span><span class="sxs-lookup"><span data-stu-id="760ff-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="760ff-124">Mensagens de formato de onda</span><span class="sxs-lookup"><span data-stu-id="760ff-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 






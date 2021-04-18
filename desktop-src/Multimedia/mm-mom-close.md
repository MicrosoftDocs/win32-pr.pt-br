---
title: Mensagem de MM_MOM_CLOSE (mmsystem. h)
description: A \_ mensagem mm Mom \_ Close é enviada para uma janela quando um dispositivo de saída de Midi é fechado.
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- Multimídia do Windows de mensagem MM_MOM_CLOSE
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454741"
---
# <a name="mm_mom_close-message"></a><span data-ttu-id="61787-104">Mensagem de fechamento do \_ Mom mm \_</span><span class="sxs-lookup"><span data-stu-id="61787-104">MM\_MOM\_CLOSE message</span></span>

<span data-ttu-id="61787-105">A mensagem **mm \_ Mom \_ Close** é enviada para uma janela quando um dispositivo de saída de Midi é fechado.</span><span class="sxs-lookup"><span data-stu-id="61787-105">The **MM\_MOM\_CLOSE** message is sent to a window when a MIDI output device is closed.</span></span>


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="61787-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61787-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61787-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="61787-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="61787-108">Identificador para o dispositivo de saída de MIDI.</span><span class="sxs-lookup"><span data-stu-id="61787-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="61787-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="61787-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="61787-110">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="61787-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61787-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="61787-111">Return Value</span></span>

<span data-ttu-id="61787-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="61787-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61787-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="61787-113">Remarks</span></span>

<span data-ttu-id="61787-114">O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="61787-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="61787-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61787-115">Requirements</span></span>



| <span data-ttu-id="61787-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="61787-116">Requirement</span></span> | <span data-ttu-id="61787-117">Valor</span><span class="sxs-lookup"><span data-stu-id="61787-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61787-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61787-118">Minimum supported client</span></span><br/> | <span data-ttu-id="61787-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="61787-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="61787-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61787-120">Minimum supported server</span></span><br/> | <span data-ttu-id="61787-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="61787-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="61787-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61787-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="61787-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61787-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61787-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="61787-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61787-125">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="61787-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 






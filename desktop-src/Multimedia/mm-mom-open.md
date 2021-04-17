---
title: Mensagem de MM_MOM_OPEN (mmsystem. h)
description: A \_ mensagem de abertura do MOM mm \_ é enviada para uma janela quando um dispositivo de saída de Midi é aberto.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- Multimídia do Windows de mensagem MM_MOM_OPEN
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f676dccf532290ab2153b888c20fad7b19d98d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454600"
---
# <a name="mm_mom_open-message"></a><span data-ttu-id="472d2-104">Mensagem de abertura do \_ Mom mm \_</span><span class="sxs-lookup"><span data-stu-id="472d2-104">MM\_MOM\_OPEN message</span></span>

<span data-ttu-id="472d2-105">A mensagem de **\_ \_ abertura do MOM mm** é enviada para uma janela quando um dispositivo de saída de Midi é aberto.</span><span class="sxs-lookup"><span data-stu-id="472d2-105">The **MM\_MOM\_OPEN** message is sent to a window when a MIDI output device is opened.</span></span>


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="472d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="472d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="472d2-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="472d2-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="472d2-108">Identificador para o dispositivo de saída de MIDI.</span><span class="sxs-lookup"><span data-stu-id="472d2-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="472d2-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="472d2-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="472d2-110">Reservado Não use.</span><span class="sxs-lookup"><span data-stu-id="472d2-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="472d2-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="472d2-111">Return Value</span></span>

<span data-ttu-id="472d2-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="472d2-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="472d2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="472d2-113">Requirements</span></span>



| <span data-ttu-id="472d2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="472d2-114">Requirement</span></span> | <span data-ttu-id="472d2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="472d2-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="472d2-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="472d2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="472d2-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="472d2-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="472d2-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="472d2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="472d2-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="472d2-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="472d2-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="472d2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="472d2-121"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="472d2-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="472d2-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="472d2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472d2-123">Mensagens MIDI</span><span class="sxs-lookup"><span data-stu-id="472d2-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 






---
title: WM_POINTERROUTEDAWAY mensagem
description: Ocorre no processo que recebe a entrada quando a entrada do ponteiro é roteada para outro processo. AddContentWithCrossProcessChaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- Mensagens de entrada e notificações de WM_POINTERROUTEDAWAY mensagem
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009535"
---
# <a name="wm_pointerroutedaway-message"></a><span data-ttu-id="cbf5e-104">WM_POINTERROUTEDAWAY mensagem</span><span class="sxs-lookup"><span data-stu-id="cbf5e-104">WM_POINTERROUTEDAWAY message</span></span>

<span data-ttu-id="cbf5e-105">Ocorre no processo que recebe a entrada quando a entrada do ponteiro é roteada para outro processo.</span><span class="sxs-lookup"><span data-stu-id="cbf5e-105">Occurs on the process receiving input when the pointer input is routed to another process.</span></span>

<span data-ttu-id="cbf5e-106">Enviado quando a entrada do ponteiro faz a transição de um processo para outro no conteúdo configurado para encadeamento de processo cruzado ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span><span class="sxs-lookup"><span data-stu-id="cbf5e-106">Sent when pointer input transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="cbf5e-107">Esta mensagem é enviada para o processo que recebe entrada de ponteiro no momento.</span><span class="sxs-lookup"><span data-stu-id="cbf5e-107">This message is sent to the process currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDAWAY       0x0252
```



## <a name="parameters"></a><span data-ttu-id="cbf5e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbf5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbf5e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cbf5e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf5e-110">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="cbf5e-110">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="cbf5e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cbf5e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf5e-112">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="cbf5e-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbf5e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbf5e-113">Return value</span></span>

<span data-ttu-id="cbf5e-114">NULO</span><span class="sxs-lookup"><span data-stu-id="cbf5e-114">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="cbf5e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbf5e-115">Remarks</span></span>

<span data-ttu-id="cbf5e-116">Essa mensagem não é enviada com uma mensagem [**WM_POINTERUP**](wm-pointerup.md) ou uma mensagem de [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="cbf5e-116">This message is not sent with either a [**WM_POINTERUP**](wm-pointerup.md) message or a [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf5e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbf5e-117">Requirements</span></span>



| <span data-ttu-id="cbf5e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbf5e-118">Requirement</span></span> | <span data-ttu-id="cbf5e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf5e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf5e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbf5e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf5e-121">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cbf5e-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cbf5e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbf5e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf5e-123">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="cbf5e-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cbf5e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbf5e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbf5e-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbf5e-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbf5e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbf5e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf5e-127">Mensagens</span><span class="sxs-lookup"><span data-stu-id="cbf5e-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="cbf5e-128">**WM_POINTERROUTEDTO**</span><span class="sxs-lookup"><span data-stu-id="cbf5e-128">**WM_POINTERROUTEDTO**</span></span>](wm-pointerroutedto.md)
</dt> </dl>

 


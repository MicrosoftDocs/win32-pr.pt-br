---
title: WM_POINTERROUTEDRELEASED mensagem
description: Enviado a todos os processos (configurados para encadeamento de processo cruzado por meio de AddContentWithCrossProcessChaining e não manipulando a entrada de ponteiro), já associados a uma ID de ponteiro específica, quando uma mensagem de WM_POINTERUP é recebida no processo atual.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- Mensagens de entrada e notificações de WM_POINTERROUTEDRELEASED mensagem
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369629"
---
# <a name="wm_pointerroutedreleased-message"></a><span data-ttu-id="180f1-104">WM_POINTERROUTEDRELEASED mensagem</span><span class="sxs-lookup"><span data-stu-id="180f1-104">WM_POINTERROUTEDRELEASED message</span></span>

<span data-ttu-id="180f1-105">Enviado a todos os processos (configurados para encadeamento de processo cruzado por meio de [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) e não manipulando a entrada de ponteiro), já associados a uma ID de ponteiro específica, quando uma mensagem de [**WM_POINTERUP**](wm-pointerup.md) é recebida no processo atual.</span><span class="sxs-lookup"><span data-stu-id="180f1-105">Sent to all processes (configured for cross-process chaining through [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) and not currently handling pointer input) ever associated with a specific pointer ID, when a [**WM_POINTERUP**](wm-pointerup.md) message is received on the current process.</span></span>


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a><span data-ttu-id="180f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="180f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="180f1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="180f1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="180f1-108">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="180f1-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="180f1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="180f1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="180f1-110">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="180f1-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="180f1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="180f1-111">Return value</span></span>

<span data-ttu-id="180f1-112">NULO</span><span class="sxs-lookup"><span data-stu-id="180f1-112">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="180f1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="180f1-113">Requirements</span></span>



| <span data-ttu-id="180f1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="180f1-114">Requirement</span></span> | <span data-ttu-id="180f1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="180f1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="180f1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="180f1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="180f1-117">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="180f1-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="180f1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="180f1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="180f1-119">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="180f1-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="180f1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="180f1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="180f1-121"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="180f1-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="180f1-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="180f1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="180f1-123">Mensagens</span><span class="sxs-lookup"><span data-stu-id="180f1-123">Messages</span></span>](messages.md)
</dt> </dl>

 


---
title: WM_POINTERROUTEDTO mensagem
description: Enviado quando entrada de ponteiro contínua, para uma ID de ponteiro existente, faz a transição de um processo para outro em todo o conteúdo configurado para AddContentWithCrossProcessChaining (encadeamento de processo cruzado).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- Mensagens de entrada e notificações de WM_POINTERROUTEDTO mensagem
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369492"
---
# <a name="wm_pointerroutedto-message"></a><span data-ttu-id="504c5-104">WM_POINTERROUTEDTO mensagem</span><span class="sxs-lookup"><span data-stu-id="504c5-104">WM_POINTERROUTEDTO message</span></span>

<span data-ttu-id="504c5-105">Enviado quando entrada de ponteiro contínua, para uma ID de ponteiro existente, faz a transição de um processo para outro em todo o conteúdo configurado para [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)(encadeamento de processo cruzado).</span><span class="sxs-lookup"><span data-stu-id="504c5-105">Sent when ongoing pointer input, for an existing pointer ID, transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="504c5-106">Esta mensagem é enviada para o processo que não está recebendo entrada de ponteiro no momento.</span><span class="sxs-lookup"><span data-stu-id="504c5-106">This message is sent to the process not currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDTO       0x0251
```



## <a name="parameters"></a><span data-ttu-id="504c5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="504c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="504c5-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="504c5-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="504c5-109">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="504c5-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="504c5-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="504c5-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="504c5-111">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="504c5-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="504c5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="504c5-112">Return value</span></span>

<span data-ttu-id="504c5-113">NULO</span><span class="sxs-lookup"><span data-stu-id="504c5-113">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="504c5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="504c5-114">Remarks</span></span>

<span data-ttu-id="504c5-115">Essa mensagem não é enviada quando uma mensagem de [**WM_POINTERDOWN**](wm-pointerdown.md) é postada para uma nova ID de ponteiro em um processo diferente.</span><span class="sxs-lookup"><span data-stu-id="504c5-115">This message is not sent when a [**WM_POINTERDOWN**](wm-pointerdown.md) message is posted for a new pointer ID on a different process.</span></span>

<span data-ttu-id="504c5-116">Uma mensagem de [**WM_POINTERDOWN**](wm-pointerdown.md) não será enviada se uma mensagem de **WM_POINTERROUTEDTO** for postada primeiro.</span><span class="sxs-lookup"><span data-stu-id="504c5-116">A [**WM_POINTERDOWN**](wm-pointerdown.md) message is not sent if a **WM_POINTERROUTEDTO** message is posted first.</span></span>

## <a name="requirements"></a><span data-ttu-id="504c5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="504c5-117">Requirements</span></span>



| <span data-ttu-id="504c5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="504c5-118">Requirement</span></span> | <span data-ttu-id="504c5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="504c5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="504c5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="504c5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="504c5-121">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="504c5-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="504c5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="504c5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="504c5-123">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="504c5-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="504c5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="504c5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="504c5-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="504c5-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="504c5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="504c5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="504c5-127">Mensagens</span><span class="sxs-lookup"><span data-stu-id="504c5-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="504c5-128">**WM_POINTERROUTEDAWAY**</span><span class="sxs-lookup"><span data-stu-id="504c5-128">**WM_POINTERROUTEDAWAY**</span></span>](wm-pointerroutedaway.md)
</dt> </dl>

 


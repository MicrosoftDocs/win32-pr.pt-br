---
description: Um aplicativo envia a mensagem do WM \_ MDINEXT para uma janela de cliente MDI (interface de vários documentos) para ativar a janela filho seguinte ou anterior.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: Mensagem de WM_MDINEXT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647076"
---
# <a name="wm_mdinext-message"></a><span data-ttu-id="dffa7-103">Mensagem do WM \_ MDINEXT</span><span class="sxs-lookup"><span data-stu-id="dffa7-103">WM\_MDINEXT message</span></span>

<span data-ttu-id="dffa7-104">Um aplicativo envia a mensagem do **WM \_ MDINEXT** para uma janela de cliente MDI (interface de vários documentos) para ativar a janela filho seguinte ou anterior.</span><span class="sxs-lookup"><span data-stu-id="dffa7-104">An application sends the **WM\_MDINEXT** message to a multiple-document interface (MDI) client window to activate the next or previous child window.</span></span>


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a><span data-ttu-id="dffa7-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dffa7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dffa7-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dffa7-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dffa7-107">Um identificador para a janela filho MDI.</span><span class="sxs-lookup"><span data-stu-id="dffa7-107">A handle to the MDI child window.</span></span> <span data-ttu-id="dffa7-108">O sistema ativa a janela filho imediatamente antes ou depois da janela filho especificada, dependendo do valor do parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="dffa7-108">The system activates the child window that is immediately before or after the specified child window, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="dffa7-109">Se o parâmetro *wParam* for **nulo**, o sistema ativará a janela filho imediatamente antes ou depois da janela filho ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="dffa7-109">If the *wParam* parameter is **NULL**, the system activates the child window that is immediately before or after the currently active child window.</span></span>

</dd> <dt>

<span data-ttu-id="dffa7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dffa7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dffa7-111">Se esse parâmetro for zero, o sistema ativará a próxima janela filho MDI e colocará a janela filho identificada pelo parâmetro *wParam* por trás de todas as outras janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="dffa7-111">If this parameter is zero, the system activates the next MDI child window and places the child window identified by the *wParam* parameter behind all other child windows.</span></span> <span data-ttu-id="dffa7-112">Se esse parâmetro for diferente de zero, o sistema ativará a janela filho anterior, colocando-o na frente da janela filho identificada por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="dffa7-112">If this parameter is nonzero, the system activates the previous child window, placing it in front of the child window identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dffa7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dffa7-113">Return value</span></span>

<span data-ttu-id="dffa7-114">Tipo: **zero**</span><span class="sxs-lookup"><span data-stu-id="dffa7-114">Type: **zero**</span></span>

<span data-ttu-id="dffa7-115">O valor de retorno é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="dffa7-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dffa7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="dffa7-116">Remarks</span></span>

<span data-ttu-id="dffa7-117">Se uma janela do cliente MDI receber qualquer mensagem que altere a ativação de suas janelas filhas enquanto a janela filho MDI ativa for maximizada, o sistema restaura a janela filho ativa e maximiza a janela filho ativada recentemente.</span><span class="sxs-lookup"><span data-stu-id="dffa7-117">If an MDI client window receives any message that changes the activation of its child windows while the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="dffa7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dffa7-118">Requirements</span></span>



| <span data-ttu-id="dffa7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dffa7-119">Requirement</span></span> | <span data-ttu-id="dffa7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dffa7-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dffa7-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dffa7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dffa7-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dffa7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dffa7-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dffa7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dffa7-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dffa7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dffa7-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dffa7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dffa7-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dffa7-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dffa7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="dffa7-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="dffa7-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="dffa7-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dffa7-129">**MDIACTIVATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="dffa7-129">**WM\_MDIACTIVATE**</span></span>](wm-mdiactivate.md)
</dt> <dt>

[<span data-ttu-id="dffa7-130">**MDIGETACTIVE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="dffa7-130">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

<span data-ttu-id="dffa7-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="dffa7-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dffa7-132">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="dffa7-132">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





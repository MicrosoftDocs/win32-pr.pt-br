---
description: Um aplicativo envia a mensagem do WM \_ MDIDESTROY para uma janela de cliente MDI (interface de vários documentos) para fechar uma janela filho MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: Mensagem de WM_MDIDESTROY (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647077"
---
# <a name="wm_mdidestroy-message"></a><span data-ttu-id="626fb-103">Mensagem do WM \_ MDIDESTROY</span><span class="sxs-lookup"><span data-stu-id="626fb-103">WM\_MDIDESTROY message</span></span>

<span data-ttu-id="626fb-104">Um aplicativo envia a mensagem do **WM \_ MDIDESTROY** para uma janela de cliente MDI (interface de vários documentos) para fechar uma janela filho MDI.</span><span class="sxs-lookup"><span data-stu-id="626fb-104">An application sends the **WM\_MDIDESTROY** message to a multiple-document interface (MDI) client window to close an MDI child window.</span></span>


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a><span data-ttu-id="626fb-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="626fb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="626fb-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="626fb-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="626fb-107">Um identificador para a janela filho MDI a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="626fb-107">A handle to the MDI child window to be closed.</span></span>

</dd> <dt>

<span data-ttu-id="626fb-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="626fb-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="626fb-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="626fb-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="626fb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="626fb-110">Return value</span></span>

<span data-ttu-id="626fb-111">Tipo: **zero**</span><span class="sxs-lookup"><span data-stu-id="626fb-111">Type: **zero**</span></span>

<span data-ttu-id="626fb-112">Essa mensagem sempre retorna zero.</span><span class="sxs-lookup"><span data-stu-id="626fb-112">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="626fb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="626fb-113">Remarks</span></span>

<span data-ttu-id="626fb-114">Essa mensagem remove o título da janela filho MDI da janela do quadro MDI e desativa a janela filho.</span><span class="sxs-lookup"><span data-stu-id="626fb-114">This message removes the title of the MDI child window from the MDI frame window and deactivates the child window.</span></span> <span data-ttu-id="626fb-115">Um aplicativo deve usar essa mensagem para fechar todas as janelas filhas MDI.</span><span class="sxs-lookup"><span data-stu-id="626fb-115">An application should use this message to close all MDI child windows.</span></span>

<span data-ttu-id="626fb-116">Se uma janela do cliente MDI receber uma mensagem que altera a ativação de suas janelas filhas e a janela filho MDI ativa for maximizada, o sistema restaura a janela filho ativa e maximiza a janela filho ativada recentemente.</span><span class="sxs-lookup"><span data-stu-id="626fb-116">If an MDI client window receives a message that changes the activation of its child windows and the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="626fb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="626fb-117">Requirements</span></span>



| <span data-ttu-id="626fb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="626fb-118">Requirement</span></span> | <span data-ttu-id="626fb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="626fb-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="626fb-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="626fb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="626fb-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="626fb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="626fb-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="626fb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="626fb-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="626fb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="626fb-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="626fb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="626fb-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="626fb-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="626fb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="626fb-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="626fb-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="626fb-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="626fb-128">**MDICREATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="626fb-128">**WM\_MDICREATE**</span></span>](wm-mdicreate.md)
</dt> <dt>

<span data-ttu-id="626fb-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="626fb-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="626fb-130">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="626fb-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





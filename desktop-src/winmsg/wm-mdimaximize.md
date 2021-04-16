---
description: Um aplicativo envia a mensagem do WM \_ MDIMAXIMIZE para uma janela de cliente MDI (interface de vários documentos) para maximizar uma janela filho MDI.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: Mensagem de WM_MDIMAXIMIZE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772713"
---
# <a name="wm_mdimaximize-message"></a><span data-ttu-id="cb476-103">Mensagem do WM \_ MDIMAXIMIZE</span><span class="sxs-lookup"><span data-stu-id="cb476-103">WM\_MDIMAXIMIZE message</span></span>

<span data-ttu-id="cb476-104">Um aplicativo envia a mensagem do **WM \_ MDIMAXIMIZE** para uma janela de cliente MDI (interface de vários documentos) para maximizar uma janela filho MDI.</span><span class="sxs-lookup"><span data-stu-id="cb476-104">An application sends the **WM\_MDIMAXIMIZE** message to a multiple-document interface (MDI) client window to maximize an MDI child window.</span></span> <span data-ttu-id="cb476-105">O sistema redimensiona a janela filho para que sua área cliente preencha a janela do cliente.</span><span class="sxs-lookup"><span data-stu-id="cb476-105">The system resizes the child window to make its client area fill the client window.</span></span> <span data-ttu-id="cb476-106">O sistema coloca o ícone do menu de janela da janela filho na posição mais à direita da barra de menus da janela do quadro e coloca o ícone de restauração da janela filho na posição mais à esquerda.</span><span class="sxs-lookup"><span data-stu-id="cb476-106">The system places the child window's window menu icon in the rightmost position of the frame window's menu bar, and places the child window's restore icon in the leftmost position.</span></span> <span data-ttu-id="cb476-107">O sistema também acrescenta o texto da barra de título da janela filho ao da janela do quadro.</span><span class="sxs-lookup"><span data-stu-id="cb476-107">The system also appends the title bar text of the child window to that of the frame window.</span></span>


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a><span data-ttu-id="cb476-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb476-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb476-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb476-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb476-110">Um identificador para a janela filho MDI a ser maximizado.</span><span class="sxs-lookup"><span data-stu-id="cb476-110">A handle to the MDI child window to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="cb476-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb476-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb476-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="cb476-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb476-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb476-113">Return value</span></span>

<span data-ttu-id="cb476-114">Tipo: **zero**</span><span class="sxs-lookup"><span data-stu-id="cb476-114">Type: **zero**</span></span>

<span data-ttu-id="cb476-115">O valor de retorno é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="cb476-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb476-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb476-116">Remarks</span></span>

<span data-ttu-id="cb476-117">Se uma janela do cliente MDI receber qualquer mensagem que altere a ativação de suas janelas filhas enquanto a janela filho MDI ativa no momento for maximizada, o sistema restaurará a janela filho ativa e maximizará a janela filho ativada recentemente.</span><span class="sxs-lookup"><span data-stu-id="cb476-117">If an MDI client window receives any message that changes the activation of its child windows while the currently active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb476-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb476-118">Requirements</span></span>



| <span data-ttu-id="cb476-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb476-119">Requirement</span></span> | <span data-ttu-id="cb476-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cb476-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb476-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb476-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cb476-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cb476-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cb476-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb476-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cb476-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cb476-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb476-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cb476-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb476-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb476-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb476-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb476-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb476-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cb476-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb476-129">**MDIRESTORE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="cb476-129">**WM\_MDIRESTORE**</span></span>](wm-mdirestore.md)
</dt> <dt>

<span data-ttu-id="cb476-130">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="cb476-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cb476-131">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="cb476-131">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





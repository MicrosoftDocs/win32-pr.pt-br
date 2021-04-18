---
description: Um aplicativo envia a mensagem do WM \_ MDIGETACTIVE para uma janela de cliente de interface de vários documentos (MDI) para recuperar o identificador para a janela filho MDI ativa.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: Mensagem de WM_MDIGETACTIVE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813703"
---
# <a name="wm_mdigetactive-message"></a><span data-ttu-id="ec499-103">Mensagem do WM \_ MDIGETACTIVE</span><span class="sxs-lookup"><span data-stu-id="ec499-103">WM\_MDIGETACTIVE message</span></span>

<span data-ttu-id="ec499-104">Um aplicativo envia a mensagem do **WM \_ MDIGETACTIVE** para uma janela de cliente de interface de vários documentos (MDI) para recuperar o identificador para a janela filho MDI ativa.</span><span class="sxs-lookup"><span data-stu-id="ec499-104">An application sends the **WM\_MDIGETACTIVE** message to a multiple-document interface (MDI) client window to retrieve the handle to the active MDI child window.</span></span>


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a><span data-ttu-id="ec499-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec499-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec499-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec499-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec499-107">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="ec499-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec499-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec499-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec499-109">O estado maximizado.</span><span class="sxs-lookup"><span data-stu-id="ec499-109">The maximized state.</span></span> <span data-ttu-id="ec499-110">Se esse parâmetro não for **nulo**, ele será um ponteiro para um valor que indica o estado maximizado da janela filho MDI.</span><span class="sxs-lookup"><span data-stu-id="ec499-110">If this parameter is not **NULL**, it is a pointer to a value that indicates the maximized state of the MDI child window.</span></span> <span data-ttu-id="ec499-111">Se o valor for **true**, a janela será maximizada; um valor **false** indica que não é.</span><span class="sxs-lookup"><span data-stu-id="ec499-111">If the value is **TRUE**, the window is maximized; a value of **FALSE** indicates that it is not.</span></span> <span data-ttu-id="ec499-112">Se esse parâmetro for **nulo**, o parâmetro será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ec499-112">If this parameter is **NULL**, the parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec499-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec499-113">Return value</span></span>

<span data-ttu-id="ec499-114">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="ec499-114">Type: **HWND**</span></span>

<span data-ttu-id="ec499-115">O valor de retorno é o identificador para a janela filho MDI ativa.</span><span class="sxs-lookup"><span data-stu-id="ec499-115">The return value is the handle to the active MDI child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec499-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec499-116">Requirements</span></span>



| <span data-ttu-id="ec499-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec499-117">Requirement</span></span> | <span data-ttu-id="ec499-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ec499-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec499-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec499-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ec499-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec499-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ec499-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec499-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ec499-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec499-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ec499-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ec499-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec499-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec499-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec499-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec499-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec499-126">Visão geral da interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="ec499-126">Multiple Document Interface Overview</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





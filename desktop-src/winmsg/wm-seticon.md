---
description: Associa um novo ícone grande ou pequeno a uma janela. O sistema exibe o ícone grande na caixa de diálogo ALT + TAB e o ícone pequeno na legenda da janela.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: Mensagem de WM_SETICON (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169528"
---
# <a name="wm_seticon-message"></a><span data-ttu-id="572e9-104">\_Mensagem de SETicon do WM</span><span class="sxs-lookup"><span data-stu-id="572e9-104">WM\_SETICON message</span></span>

<span data-ttu-id="572e9-105">Associa um novo ícone grande ou pequeno a uma janela.</span><span class="sxs-lookup"><span data-stu-id="572e9-105">Associates a new large or small icon with a window.</span></span> <span data-ttu-id="572e9-106">O sistema exibe o ícone grande na caixa de diálogo ALT + TAB e o ícone pequeno na legenda da janela.</span><span class="sxs-lookup"><span data-stu-id="572e9-106">The system displays the large icon in the ALT+TAB dialog box, and the small icon in the window caption.</span></span>


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a><span data-ttu-id="572e9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="572e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="572e9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="572e9-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="572e9-109">O tipo de ícone a ser definido.</span><span class="sxs-lookup"><span data-stu-id="572e9-109">The type of icon to be set.</span></span> <span data-ttu-id="572e9-110">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="572e9-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="572e9-111">Valor</span><span class="sxs-lookup"><span data-stu-id="572e9-111">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="572e9-112">Significado</span><span class="sxs-lookup"><span data-stu-id="572e9-112">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="572e9-113"><dt>**Ícone \_ do BIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="572e9-113"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="572e9-114">Defina o ícone grande para a janela.</span><span class="sxs-lookup"><span data-stu-id="572e9-114">Set the large icon for the window.</span></span><br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="572e9-115"><dt>**Ícone \_ do PEQUENO**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="572e9-115"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="572e9-116">Defina o ícone pequeno para a janela.</span><span class="sxs-lookup"><span data-stu-id="572e9-116">Set the small icon for the window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="572e9-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="572e9-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="572e9-118">Um identificador para o novo ícone grande ou pequeno.</span><span class="sxs-lookup"><span data-stu-id="572e9-118">A handle to the new large or small icon.</span></span> <span data-ttu-id="572e9-119">Se esse parâmetro for **NULL**, o ícone indicado por *wParam* será removido.</span><span class="sxs-lookup"><span data-stu-id="572e9-119">If this parameter is **NULL**, the icon indicated by *wParam* is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="572e9-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="572e9-120">Return value</span></span>

<span data-ttu-id="572e9-121">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="572e9-121">Type: **LRESULT**</span></span>

<span data-ttu-id="572e9-122">O valor de retorno é um identificador para o ícone grande ou pequeno anterior, dependendo do valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="572e9-122">The return value is a handle to the previous large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="572e9-123">Será **nulo** se a janela não tivesse nenhum ícone do tipo indicado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="572e9-123">It is **NULL** if the window previously had no icon of the type indicated by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="572e9-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="572e9-124">Remarks</span></span>

<span data-ttu-id="572e9-125">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna um identificador para o ícone grande ou pequeno anterior associado à janela, dependendo do valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="572e9-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns a handle to the previous large or small icon associated with the window, depending on the value of *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="572e9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="572e9-126">Requirements</span></span>



| <span data-ttu-id="572e9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="572e9-127">Requirement</span></span> | <span data-ttu-id="572e9-128">Valor</span><span class="sxs-lookup"><span data-stu-id="572e9-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="572e9-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="572e9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="572e9-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="572e9-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="572e9-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="572e9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="572e9-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="572e9-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="572e9-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="572e9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="572e9-134"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="572e9-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="572e9-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="572e9-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="572e9-136">**Referência**</span><span class="sxs-lookup"><span data-stu-id="572e9-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="572e9-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="572e9-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="572e9-138">**WM \_ GETicon**</span><span class="sxs-lookup"><span data-stu-id="572e9-138">**WM\_GETICON**</span></span>](wm-geticon.md)
</dt> <dt>

<span data-ttu-id="572e9-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="572e9-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="572e9-140">Windows</span><span class="sxs-lookup"><span data-stu-id="572e9-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 

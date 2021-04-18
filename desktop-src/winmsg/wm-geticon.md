---
description: Enviado a uma janela para recuperar um identificador para o ícone grande ou pequeno associado a uma janela. O sistema exibe o ícone grande na caixa de diálogo ALT + TAB e o ícone pequeno na legenda da janela.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: Mensagem de WM_GETICON (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793241"
---
# <a name="wm_geticon-message"></a><span data-ttu-id="64d44-104">\_Mensagem de GETicon do WM</span><span class="sxs-lookup"><span data-stu-id="64d44-104">WM\_GETICON message</span></span>

<span data-ttu-id="64d44-105">Enviado a uma janela para recuperar um identificador para o ícone grande ou pequeno associado a uma janela.</span><span class="sxs-lookup"><span data-stu-id="64d44-105">Sent to a window to retrieve a handle to the large or small icon associated with a window.</span></span> <span data-ttu-id="64d44-106">O sistema exibe o ícone grande na caixa de diálogo ALT + TAB e o ícone pequeno na legenda da janela.</span><span class="sxs-lookup"><span data-stu-id="64d44-106">The system displays the large icon in the ALT+TAB dialog, and the small icon in the window caption.</span></span>

<span data-ttu-id="64d44-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="64d44-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a><span data-ttu-id="64d44-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64d44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d44-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64d44-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64d44-110">O tipo de ícone que está sendo recuperado.</span><span class="sxs-lookup"><span data-stu-id="64d44-110">The type of icon being retrieved.</span></span> <span data-ttu-id="64d44-111">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="64d44-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="64d44-112">Valor</span><span class="sxs-lookup"><span data-stu-id="64d44-112">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="64d44-113">Significado</span><span class="sxs-lookup"><span data-stu-id="64d44-113">Meaning</span></span>                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="64d44-114"><dt>**Ícone \_ do BIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="64d44-114"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="64d44-115">Recupere o ícone grande para a janela.</span><span class="sxs-lookup"><span data-stu-id="64d44-115">Retrieve the large icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="64d44-116"><dt>**Ícone \_ do PEQUENO**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="64d44-116"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="64d44-117">Recupere o ícone pequeno da janela.</span><span class="sxs-lookup"><span data-stu-id="64d44-117">Retrieve the small icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <span data-ttu-id="64d44-118"><dt>**Ícone \_ do SMALL2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="64d44-118"><dt>**ICON\_SMALL2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="64d44-119">Recupera o ícone pequeno fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="64d44-119">Retrieves the small icon provided by the application.</span></span> <span data-ttu-id="64d44-120">Se o aplicativo não fornecer um, o sistema usará o ícone gerado pelo sistema para essa janela.</span><span class="sxs-lookup"><span data-stu-id="64d44-120">If the application does not provide one, the system uses the system-generated icon for that window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="64d44-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64d44-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64d44-122">O DPI do ícone que está sendo recuperado.</span><span class="sxs-lookup"><span data-stu-id="64d44-122">The DPI of the icon being retrieved.</span></span> <span data-ttu-id="64d44-123">Isso pode ser usado para fornecer ícones diferentes, dependendo do tamanho do ícone.</span><span class="sxs-lookup"><span data-stu-id="64d44-123">This can be used to provide different icons depending on the icon size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d44-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64d44-124">Return value</span></span>

<span data-ttu-id="64d44-125">Tipo: **HICON**</span><span class="sxs-lookup"><span data-stu-id="64d44-125">Type: **HICON**</span></span>

<span data-ttu-id="64d44-126">O valor de retorno é um identificador para o ícone grande ou pequeno, dependendo do valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="64d44-126">The return value is a handle to the large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="64d44-127">Quando um aplicativo recebe essa mensagem, ele pode retornar um identificador para um ícone grande ou pequeno, ou passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="64d44-127">When an application receives this message, it can return a handle to a large or small icon, or pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d44-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="64d44-128">Remarks</span></span>

<span data-ttu-id="64d44-129">Quando um aplicativo recebe essa mensagem, ele pode retornar um identificador para um ícone grande ou pequeno, ou passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="64d44-129">When an application receives this message, it can return a handle to a large or small icon, or pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="64d44-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna um identificador para o ícone grande ou pequeno associado à janela, dependendo do valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="64d44-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns a handle to the large or small icon associated with the window, depending on the value of *wParam*.</span></span>

<span data-ttu-id="64d44-131">Uma janela que não tem nenhum ícone definido explicitamente (com o **WM \_ SetIcon**) usa o ícone para a classe de janela registrada e, nesse caso, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retornará 0 para uma mensagem do **WM \_ GetIcon** .</span><span class="sxs-lookup"><span data-stu-id="64d44-131">A window that has no icon explicitly set (with **WM\_SETICON**) uses the icon for the registered window class, and in this case [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) will return 0 for a **WM\_GETICON** message.</span></span> <span data-ttu-id="64d44-132">Se o envio de uma mensagem do **WM \_ GetIcon** para uma janela retornar 0, tente chamar a função [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) para a janela.</span><span class="sxs-lookup"><span data-stu-id="64d44-132">If sending a **WM\_GETICON** message to a window returns 0, next try calling the [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) function for the window.</span></span> <span data-ttu-id="64d44-133">Se isso retornar 0, tente a função [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) .</span><span class="sxs-lookup"><span data-stu-id="64d44-133">If that returns 0 then try the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d44-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64d44-134">Requirements</span></span>



| <span data-ttu-id="64d44-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="64d44-135">Requirement</span></span> | <span data-ttu-id="64d44-136">Valor</span><span class="sxs-lookup"><span data-stu-id="64d44-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d44-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64d44-137">Minimum supported client</span></span><br/> | <span data-ttu-id="64d44-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="64d44-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="64d44-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64d44-139">Minimum supported server</span></span><br/> | <span data-ttu-id="64d44-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="64d44-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64d44-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="64d44-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="64d44-142"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64d44-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d44-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="64d44-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="64d44-144">**Referência**</span><span class="sxs-lookup"><span data-stu-id="64d44-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="64d44-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="64d44-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="64d44-146">**ÍCONE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="64d44-146">**WM\_SETICON**</span></span>](wm-seticon.md)
</dt> <dt>

<span data-ttu-id="64d44-147">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="64d44-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="64d44-148">Windows</span><span class="sxs-lookup"><span data-stu-id="64d44-148">Windows</span></span>](windows.md)
</dt> </dl>

 

 

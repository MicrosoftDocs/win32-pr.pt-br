---
description: Enviado a uma janela quando sua área não cliente precisa ser alterada para indicar um estado ativo ou inativo.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: Mensagem de WM_NCACTIVATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789914"
---
# <a name="wm_ncactivate-message"></a><span data-ttu-id="54cf4-103">Mensagem do WM \_ NCACTIVATE</span><span class="sxs-lookup"><span data-stu-id="54cf4-103">WM\_NCACTIVATE message</span></span>

<span data-ttu-id="54cf4-104">Enviado a uma janela quando sua área não cliente precisa ser alterada para indicar um estado ativo ou inativo.</span><span class="sxs-lookup"><span data-stu-id="54cf4-104">Sent to a window when its nonclient area needs to be changed to indicate an active or inactive state.</span></span>

<span data-ttu-id="54cf4-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="54cf4-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a><span data-ttu-id="54cf4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54cf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54cf4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54cf4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54cf4-108">Indica quando uma barra de título ou um ícone precisa ser alterado para indicar um estado ativo ou inativo.</span><span class="sxs-lookup"><span data-stu-id="54cf4-108">Indicates when a title bar or icon needs to be changed to indicate an active or inactive state.</span></span> <span data-ttu-id="54cf4-109">Se uma barra de título ou um ícone ativo for ser desenhado, o parâmetro *wParam* será **true**.</span><span class="sxs-lookup"><span data-stu-id="54cf4-109">If an active title bar or icon is to be drawn, the *wParam* parameter is **TRUE**.</span></span> <span data-ttu-id="54cf4-110">Se uma barra de título ou um ícone inativo for ser desenhado, *wParam* será **false**.</span><span class="sxs-lookup"><span data-stu-id="54cf4-110">If an inactive title bar or icon is to be drawn, *wParam* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="54cf4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54cf4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54cf4-112">Quando um [estilo visual](../controls/themes-overview.md) está ativo para esta janela, esse parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="54cf4-112">When a [visual style](../controls/themes-overview.md) is active for this window, this parameter is not used.</span></span>

<span data-ttu-id="54cf4-113">Quando um estilo visual não está ativo para esta janela, esse parâmetro é um identificador para uma região de atualização opcional para a área não cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="54cf4-113">When a visual style is not active for this window, this parameter is a handle to an optional update region for the nonclient area of the window.</span></span> <span data-ttu-id="54cf4-114">Se esse parâmetro for definido como-1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) não repintará a área não cliente para refletir a alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="54cf4-114">If this parameter is set to -1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not repaint the nonclient area to reflect the state change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54cf4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="54cf4-115">Return value</span></span>

<span data-ttu-id="54cf4-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="54cf4-116">Type: **LRESULT**</span></span>

<span data-ttu-id="54cf4-117">Quando o parâmetro *wParam* é **false**, um aplicativo deve retornar **true** para indicar que o sistema deve continuar com o processamento padrão ou deve retornar **false** para impedir a alteração.</span><span class="sxs-lookup"><span data-stu-id="54cf4-117">When the *wParam* parameter is **FALSE**, an application should return **TRUE** to indicate that the system should proceed with the default processing, or it should return **FALSE** to prevent the change.</span></span> <span data-ttu-id="54cf4-118">Quando *wParam* é **true**, o valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="54cf4-118">When *wParam* is **TRUE**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="54cf4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="54cf4-119">Remarks</span></span>

<span data-ttu-id="54cf4-120">O processamento de mensagens relacionadas à área não cliente de uma janela padrão não é recomendado, pois o aplicativo deve ser capaz de desenhar todas as partes necessárias da área não cliente para a janela.</span><span class="sxs-lookup"><span data-stu-id="54cf4-120">Processing messages related to the nonclient area of a standard window is not recommended, because the application must be able to draw all the required parts of the nonclient area for the window.</span></span> <span data-ttu-id="54cf4-121">Se um aplicativo processar essa mensagem, ele deverá retornar **true** para instruir o sistema a concluir a alteração da janela ativa.</span><span class="sxs-lookup"><span data-stu-id="54cf4-121">If an application does process this message, it must return **TRUE** to direct the system to complete the change of active window.</span></span> <span data-ttu-id="54cf4-122">Se a janela for minimizada quando essa mensagem for recebida, o aplicativo deverá passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="54cf4-122">If the window is minimized when this message is received, the application should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="54cf4-123">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) desenha a barra de título ou o título do ícone em suas cores ativas quando o parâmetro *wParam* é **true** e em suas cores inativas quando *wParam* é **false**.</span><span class="sxs-lookup"><span data-stu-id="54cf4-123">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the title bar or icon title in its active colors when the *wParam* parameter is **TRUE** and in its inactive colors when *wParam* is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="54cf4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54cf4-124">Requirements</span></span>



| <span data-ttu-id="54cf4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="54cf4-125">Requirement</span></span> | <span data-ttu-id="54cf4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="54cf4-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54cf4-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54cf4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="54cf4-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="54cf4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="54cf4-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54cf4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="54cf4-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="54cf4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="54cf4-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="54cf4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="54cf4-132"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54cf4-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54cf4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="54cf4-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="54cf4-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="54cf4-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54cf4-135">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="54cf4-135">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="54cf4-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="54cf4-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="54cf4-137">Windows</span><span class="sxs-lookup"><span data-stu-id="54cf4-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 

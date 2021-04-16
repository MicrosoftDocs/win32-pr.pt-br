---
title: Mensagem de WM_VSCROLLCLIPBOARD (WinUser. h)
description: Enviado ao proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no \_ formato OWNERDISPLAY do CF e um evento ocorre na barra de rolagem vertical do Visualizador da área de transferência.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- Troca de dados de mensagem WM_VSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455299"
---
# <a name="wm_vscrollclipboard-message"></a><span data-ttu-id="f5c04-104">Mensagem do WM \_ VSCROLLCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="f5c04-104">WM\_VSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="f5c04-105">Enviado ao proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no formato [**\_ OWNERDISPLAY do CF**](standard-clipboard-formats.md) e um evento ocorre na barra de rolagem vertical do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="f5c04-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's vertical scroll bar.</span></span> <span data-ttu-id="f5c04-106">O proprietário deve rolar a imagem da área de transferência e atualizar os valores da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="f5c04-106">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a><span data-ttu-id="f5c04-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5c04-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c04-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5c04-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c04-109">Um identificador para a janela do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="f5c04-109">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="f5c04-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5c04-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c04-111">A palavra de ordem inferior de *lParam* especifica um evento de barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="f5c04-111">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="f5c04-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f5c04-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f5c04-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f5c04-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="f5c04-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f5c04-114">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="f5c04-115"><dt>**SB \_ INFERIOR**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f5c04-115"><dt>**SB\_BOTTOM**</dt> <dt>7</dt></span></span> </dl>                      | <span data-ttu-id="f5c04-116">Role para o canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="f5c04-116">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="f5c04-117"><dt>**SB \_ Endrolagem**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="f5c04-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="f5c04-118">Finalizar rolagem.</span><span class="sxs-lookup"><span data-stu-id="f5c04-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="f5c04-119"><dt>**SB \_ LINEDOWN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f5c04-119"><dt>**SB\_LINEDOWN**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="f5c04-120">Rolar uma linha para baixo.</span><span class="sxs-lookup"><span data-stu-id="f5c04-120">Scroll one line down.</span></span><br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="f5c04-121"><dt>**SB \_ LINHAr**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5c04-121"><dt>**SB\_LINEUP**</dt> <dt>0</dt></span></span> </dl>                      | <span data-ttu-id="f5c04-122">Rolar uma linha para cima.</span><span class="sxs-lookup"><span data-stu-id="f5c04-122">Scroll one line up.</span></span><br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="f5c04-123"><dt>**SB \_ PAGEDOWN**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f5c04-123"><dt>**SB\_PAGEDOWN**</dt> <dt>3</dt></span></span> </dl>                | <span data-ttu-id="f5c04-124">Rolar uma página para baixo.</span><span class="sxs-lookup"><span data-stu-id="f5c04-124">Scroll one page down.</span></span><br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="f5c04-125"><dt>**SB \_ PAGEUP**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f5c04-125"><dt>**SB\_PAGEUP**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="f5c04-126">Rolar uma página para cima.</span><span class="sxs-lookup"><span data-stu-id="f5c04-126">Scroll one page up.</span></span><br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="f5c04-127"><dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f5c04-127"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="f5c04-128">Role até a posição absoluta.</span><span class="sxs-lookup"><span data-stu-id="f5c04-128">Scroll to absolute position.</span></span> <span data-ttu-id="f5c04-129">A posição atual é especificada pela palavra de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="f5c04-129">The current position is specified by the high-order word.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="f5c04-130"><dt>**SB \_**</dt> <dt>6</dt> principais</span><span class="sxs-lookup"><span data-stu-id="f5c04-130"><dt>**SB\_TOP**</dt> <dt>6</dt></span></span> </dl>                               | <span data-ttu-id="f5c04-131">Role para o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="f5c04-131">Scroll to upper left.</span></span><br/>                                                                  |



 

<span data-ttu-id="f5c04-132">A palavra de ordem superior de *lParam* especifica a posição atual da caixa de rolagem se a palavra de ordem inferior de *lParam* for **SB \_ THUMBPOSITION**; caso contrário, a palavra de ordem superior de *lParam* não será usada.</span><span class="sxs-lookup"><span data-stu-id="f5c04-132">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word of *lParam* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c04-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5c04-133">Return value</span></span>

<span data-ttu-id="f5c04-134">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="f5c04-134">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5c04-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5c04-135">Remarks</span></span>

<span data-ttu-id="f5c04-136">O proprietário da área de transferência pode usar a função [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) para rolar a imagem na janela do Visualizador da área de transferência e invalidar a região apropriada.</span><span class="sxs-lookup"><span data-stu-id="f5c04-136">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c04-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5c04-137">Requirements</span></span>



| <span data-ttu-id="f5c04-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c04-138">Requirement</span></span> | <span data-ttu-id="f5c04-139">Valor</span><span class="sxs-lookup"><span data-stu-id="f5c04-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c04-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5c04-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c04-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f5c04-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f5c04-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5c04-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c04-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f5c04-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f5c04-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f5c04-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5c04-145"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5c04-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c04-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5c04-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5c04-147">**Referência**</span><span class="sxs-lookup"><span data-stu-id="f5c04-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="f5c04-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5c04-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f5c04-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5c04-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f5c04-150">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="f5c04-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f5c04-151">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="f5c04-151">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="f5c04-152">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="f5c04-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="f5c04-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="f5c04-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 


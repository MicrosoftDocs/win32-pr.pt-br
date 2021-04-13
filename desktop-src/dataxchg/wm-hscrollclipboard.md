---
title: Mensagem de WM_HSCROLLCLIPBOARD (WinUser. h)
description: Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- Troca de dados de mensagem WM_HSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455675"
---
# <a name="wm_hscrollclipboard-message"></a><span data-ttu-id="1ec67-104">Mensagem do WM \_ HSCROLLCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="1ec67-104">WM\_HSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="1ec67-105">Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="1ec67-105">Sent to the clipboard owner by a clipboard viewer window.</span></span> <span data-ttu-id="1ec67-106">Isso ocorre quando a área de transferência contém dados no formato [**\_ OWNERDISPLAY do CF**](standard-clipboard-formats.md) e um evento ocorre na barra de rolagem horizontal do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="1ec67-106">This occurs when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's horizontal scroll bar.</span></span> <span data-ttu-id="1ec67-107">O proprietário deve rolar a imagem da área de transferência e atualizar os valores da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="1ec67-107">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a><span data-ttu-id="1ec67-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ec67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec67-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ec67-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec67-110">Um identificador para a janela do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="1ec67-110">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="1ec67-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ec67-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec67-112">A palavra de ordem inferior de *lParam* especifica um evento de barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="1ec67-112">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="1ec67-113">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ec67-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="1ec67-114">A palavra de ordem superior de *lParam* especifica a posição atual da caixa de rolagem se a palavra de ordem inferior de *lParam* for **SB \_ THUMBPOSITION**; caso contrário, a palavra de ordem superior não será usada.</span><span class="sxs-lookup"><span data-stu-id="1ec67-114">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word is not used.</span></span>



| <span data-ttu-id="1ec67-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1ec67-115">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="1ec67-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1ec67-116">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="1ec67-117"><dt>**SB \_ Endrolagem**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="1ec67-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="1ec67-118">Finalizar rolagem.</span><span class="sxs-lookup"><span data-stu-id="1ec67-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="1ec67-119"><dt>**SB \_ ESQUERDA**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1ec67-119"><dt>**SB\_LEFT**</dt> <dt>6</dt></span></span> </dl>                            | <span data-ttu-id="1ec67-120">Role para o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="1ec67-120">Scroll to upper left.</span></span><br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="1ec67-121"><dt>**SB \_ DIREITA**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="1ec67-121"><dt>**SB\_RIGHT**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="1ec67-122">Role para o canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="1ec67-122">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="1ec67-123"><dt>**SB \_ LINELEFT**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1ec67-123"><dt>**SB\_LINELEFT**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="1ec67-124">Rola para a esquerda em uma unidade.</span><span class="sxs-lookup"><span data-stu-id="1ec67-124">Scrolls left by one unit.</span></span><br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="1ec67-125"><dt>**SB \_ LINERIGHT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1ec67-125"><dt>**SB\_LINERIGHT**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="1ec67-126">Rola para a direita em uma unidade.</span><span class="sxs-lookup"><span data-stu-id="1ec67-126">Scrolls right by one unit.</span></span><br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="1ec67-127"><dt>**SB \_ PAGELEFT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1ec67-127"><dt>**SB\_PAGELEFT**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="1ec67-128">Rola para a esquerda pela largura da janela.</span><span class="sxs-lookup"><span data-stu-id="1ec67-128">Scrolls left by the width of the window.</span></span><br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="1ec67-129"><dt>**SB \_ FIXADA**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1ec67-129"><dt>**SB\_PAGERIGHT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="1ec67-130">Rola para a direita pela largura da janela.</span><span class="sxs-lookup"><span data-stu-id="1ec67-130">Scrolls right by the width of the window.</span></span><br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="1ec67-131"><dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1ec67-131"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="1ec67-132">Role até a posição absoluta.</span><span class="sxs-lookup"><span data-stu-id="1ec67-132">Scroll to absolute position.</span></span> <span data-ttu-id="1ec67-133">A posição atual é especificada pela palavra de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="1ec67-133">The current position is specified by the high-order word.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec67-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ec67-134">Return value</span></span>

<span data-ttu-id="1ec67-135">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="1ec67-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec67-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ec67-136">Remarks</span></span>

<span data-ttu-id="1ec67-137">O proprietário da área de transferência pode usar a função [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) para rolar a imagem na janela do Visualizador da área de transferência e invalidar a região apropriada.</span><span class="sxs-lookup"><span data-stu-id="1ec67-137">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec67-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ec67-138">Requirements</span></span>



| <span data-ttu-id="1ec67-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec67-139">Requirement</span></span> | <span data-ttu-id="1ec67-140">Valor</span><span class="sxs-lookup"><span data-stu-id="1ec67-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec67-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ec67-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec67-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ec67-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1ec67-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ec67-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec67-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ec67-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ec67-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1ec67-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ec67-146"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec67-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec67-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ec67-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="1ec67-148">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1ec67-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="1ec67-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ec67-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1ec67-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ec67-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1ec67-151">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="1ec67-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1ec67-152">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="1ec67-152">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="1ec67-153">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="1ec67-153">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="1ec67-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="1ec67-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 


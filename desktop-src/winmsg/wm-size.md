---
Description: Enviado a uma janela após a alteração de seu tamanho.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: Mensagem de WM_SIZE (WinUser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752546"
---
# <a name="wm_size-message"></a><span data-ttu-id="818b2-103">Mensagem de tamanho do WM \_</span><span class="sxs-lookup"><span data-stu-id="818b2-103">WM\_SIZE message</span></span>

<span data-ttu-id="818b2-104">Enviado a uma janela após a alteração de seu tamanho.</span><span class="sxs-lookup"><span data-stu-id="818b2-104">Sent to a window after its size has changed.</span></span>

<span data-ttu-id="818b2-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="818b2-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a><span data-ttu-id="818b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="818b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="818b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="818b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="818b2-108">O tipo de redimensionamento solicitado.</span><span class="sxs-lookup"><span data-stu-id="818b2-108">The type of resizing requested.</span></span> <span data-ttu-id="818b2-109">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="818b2-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="818b2-110">Valor</span><span class="sxs-lookup"><span data-stu-id="818b2-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="818b2-111">Significado</span><span class="sxs-lookup"><span data-stu-id="818b2-111">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <span data-ttu-id="818b2-112"><dt>**Tamanho \_ MAXHIDE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="818b2-112"><dt>**SIZE\_MAXHIDE**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="818b2-113">A mensagem é enviada para todas as janelas pop-up quando alguma outra janela é maximizada.</span><span class="sxs-lookup"><span data-stu-id="818b2-113">Message is sent to all pop-up windows when some other window is maximized.</span></span><br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <span data-ttu-id="818b2-114"><dt>**Tamanho \_ MAXIMIZAdo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="818b2-114"><dt>**SIZE\_MAXIMIZED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="818b2-115">A janela foi maximizada.</span><span class="sxs-lookup"><span data-stu-id="818b2-115">The window has been maximized.</span></span><br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <span data-ttu-id="818b2-116"><dt>**Tamanho \_ MAXSHOW**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="818b2-116"><dt>**SIZE\_MAXSHOW**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="818b2-117">A mensagem é enviada para todas as janelas pop-up quando alguma outra janela é restaurada para seu tamanho anterior.</span><span class="sxs-lookup"><span data-stu-id="818b2-117">Message is sent to all pop-up windows when some other window has been restored to its former size.</span></span><br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <span data-ttu-id="818b2-118"><dt>**Tamanho \_ MINIMIZAdo**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="818b2-118"><dt>**SIZE\_MINIMIZED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="818b2-119">A janela foi minimizada.</span><span class="sxs-lookup"><span data-stu-id="818b2-119">The window has been minimized.</span></span><br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <span data-ttu-id="818b2-120"><dt>**Tamanho \_ RESTAURAdo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="818b2-120"><dt>**SIZE\_RESTORED**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="818b2-121">A janela foi redimensionada, mas nem o valor de **tamanho \_ minimizado** nem de **tamanho \_ maximizado** se aplica.</span><span class="sxs-lookup"><span data-stu-id="818b2-121">The window has been resized, but neither the **SIZE\_MINIMIZED** nor **SIZE\_MAXIMIZED** value applies.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="818b2-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="818b2-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="818b2-123">A palavra de ordem inferior de *lParam* especifica a nova largura da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="818b2-123">The low-order word of *lParam* specifies the new width of the client area.</span></span>

<span data-ttu-id="818b2-124">A palavra de ordem superior do *lParam* especifica a nova altura da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="818b2-124">The high-order word of *lParam* specifies the new height of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="818b2-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="818b2-125">Return value</span></span>

<span data-ttu-id="818b2-126">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="818b2-126">Type: **LRESULT**</span></span>

<span data-ttu-id="818b2-127">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="818b2-127">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="818b2-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="818b2-128">Example</span></span>

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

<span data-ttu-id="818b2-129">Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) no github.</span><span class="sxs-lookup"><span data-stu-id="818b2-129">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="818b2-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="818b2-130">Remarks</span></span>

<span data-ttu-id="818b2-131">Se a função [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) ou [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) for chamada para uma janela filho como resultado da mensagem de **\_ tamanho do WM** , o parâmetro *bRedraw* ou *bRepaint* deverá ser diferente de zero para fazer com que a janela seja repintada.</span><span class="sxs-lookup"><span data-stu-id="818b2-131">If the [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) or [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function is called for a child window as a result of the **WM\_SIZE** message, the *bRedraw* or *bRepaint* parameter should be nonzero to cause the window to be repainted.</span></span>

<span data-ttu-id="818b2-132">Embora a largura e a altura de uma janela sejam valores de 32 bits, o parâmetro *lParam* contém apenas os 16 bits de ordem inferior de cada um.</span><span class="sxs-lookup"><span data-stu-id="818b2-132">Although the width and height of a window are 32-bit values, the *lParam* parameter contains only the low-order 16 bits of each.</span></span>

<span data-ttu-id="818b2-133">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia o **\_ tamanho do WM** e as mensagens de **\_ movimentação do WM** quando processa a mensagem do [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="818b2-133">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="818b2-134">O **\_ tamanho do WM** e as mensagens de **\_ movimentação do WM** não serão enviadas se um aplicativo manipular a mensagem do **WM \_ WINDOWPOSCHANGED** sem chamar **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="818b2-134">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="818b2-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="818b2-135">Requirements</span></span>



| <span data-ttu-id="818b2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="818b2-136">Requirement</span></span> | <span data-ttu-id="818b2-137">Valor</span><span class="sxs-lookup"><span data-stu-id="818b2-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="818b2-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="818b2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="818b2-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="818b2-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="818b2-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="818b2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="818b2-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="818b2-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="818b2-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="818b2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="818b2-143"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="818b2-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="818b2-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="818b2-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="818b2-145">**Referência**</span><span class="sxs-lookup"><span data-stu-id="818b2-145">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="818b2-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="818b2-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="818b2-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="818b2-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="818b2-148">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="818b2-148">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="818b2-149">**WINDOWPOSCHANGED do WM \_**</span><span class="sxs-lookup"><span data-stu-id="818b2-149">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="818b2-150">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="818b2-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="818b2-151">Windows</span><span class="sxs-lookup"><span data-stu-id="818b2-151">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="818b2-152">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="818b2-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="818b2-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="818b2-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

 

---
title: Mensagem de WM_COMMAND (WinUser. h)
description: Enviado quando o usuário seleciona um item de comando em um menu, quando um controle envia uma mensagem de notificação para sua janela pai ou quando um pressionamento de teclas de acelerador é traduzido.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791502"
---
# <a name="wm_command-message"></a><span data-ttu-id="05491-104">Mensagem de comando do WM \_</span><span class="sxs-lookup"><span data-stu-id="05491-104">WM\_COMMAND message</span></span>

<span data-ttu-id="05491-105">Enviado quando o usuário seleciona um item de comando em um menu, quando um controle envia uma mensagem de notificação para sua janela pai ou quando um pressionamento de teclas de acelerador é traduzido.</span><span class="sxs-lookup"><span data-stu-id="05491-105">Sent when the user selects a command item from a menu, when a control sends a notification message to its parent window, or when an accelerator keystroke is translated.</span></span>


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a><span data-ttu-id="05491-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05491-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05491-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05491-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05491-108">Para obter uma descrição desse parâmetro, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="05491-108">For a description of this parameter, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="05491-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05491-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05491-110">Para obter uma descrição desse parâmetro, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="05491-110">For a description of this parameter, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05491-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05491-111">Return value</span></span>

<span data-ttu-id="05491-112">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="05491-112">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="05491-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="05491-113">Example</span></span>

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
<span data-ttu-id="05491-114">Exemplo obtido de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples) no github.</span><span class="sxs-lookup"><span data-stu-id="05491-114">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="05491-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="05491-115">Remarks</span></span>

<span data-ttu-id="05491-116">O uso dos parâmetros *wParam* e *lParam* é resumido aqui.</span><span class="sxs-lookup"><span data-stu-id="05491-116">Use of the *wParam* and *lParam* parameters are summarized here.</span></span>



| <span data-ttu-id="05491-117">Origem da mensagem</span><span class="sxs-lookup"><span data-stu-id="05491-117">Message Source</span></span> | <span data-ttu-id="05491-118">wParam (palavra alta)</span><span class="sxs-lookup"><span data-stu-id="05491-118">wParam (high word)</span></span>                | <span data-ttu-id="05491-119">wParam (palavra inferior)</span><span class="sxs-lookup"><span data-stu-id="05491-119">wParam (low word)</span></span>                | <span data-ttu-id="05491-120">lParam</span><span class="sxs-lookup"><span data-stu-id="05491-120">lParam</span></span>                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| <span data-ttu-id="05491-121">Menu</span><span class="sxs-lookup"><span data-stu-id="05491-121">Menu</span></span>           | <span data-ttu-id="05491-122">0</span><span class="sxs-lookup"><span data-stu-id="05491-122">0</span></span>                                 | <span data-ttu-id="05491-123">Identificador de menu (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="05491-123">Menu identifier (IDM\_\*)</span></span>        | <span data-ttu-id="05491-124">0</span><span class="sxs-lookup"><span data-stu-id="05491-124">0</span></span>                            |
| <span data-ttu-id="05491-125">Acelerador</span><span class="sxs-lookup"><span data-stu-id="05491-125">Accelerator</span></span>    | <span data-ttu-id="05491-126">1</span><span class="sxs-lookup"><span data-stu-id="05491-126">1</span></span>                                 | <span data-ttu-id="05491-127">Identificador do acelerador (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="05491-127">Accelerator identifier (IDM\_\*)</span></span> | <span data-ttu-id="05491-128">0</span><span class="sxs-lookup"><span data-stu-id="05491-128">0</span></span>                            |
| <span data-ttu-id="05491-129">Control</span><span class="sxs-lookup"><span data-stu-id="05491-129">Control</span></span>        | <span data-ttu-id="05491-130">Código de notificação definido pelo controle</span><span class="sxs-lookup"><span data-stu-id="05491-130">Control-defined notification code</span></span> | <span data-ttu-id="05491-131">Identificador de controle</span><span class="sxs-lookup"><span data-stu-id="05491-131">Control identifier</span></span>               | <span data-ttu-id="05491-132">Identificador para a janela de controle</span><span class="sxs-lookup"><span data-stu-id="05491-132">Handle to the control window</span></span> |



 

### <a name="menus"></a><span data-ttu-id="05491-133">Menus</span><span class="sxs-lookup"><span data-stu-id="05491-133">Menus</span></span>

<span data-ttu-id="05491-134">Se um aplicativo habilitar um separador de menus, o sistema enviará uma mensagem de **\_ comando do WM** com a palavra inferior do parâmetro *wParam* definido como zero quando o usuário selecionar o separador.</span><span class="sxs-lookup"><span data-stu-id="05491-134">If an application enables a menu separator, the system sends a **WM\_COMMAND** message with the low-word of the *wParam* parameter set to zero when the user selects the separator.</span></span>

<span data-ttu-id="05491-135">Se um menu for definido com um valor de [**MENUINFO. dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) de **MNS \_ NOTIFYBYPOS**, o [**WM \_ MENUCOMMAND**](wm-menucommand.md) será enviado em vez do **\_ comando do WM**.</span><span class="sxs-lookup"><span data-stu-id="05491-135">If a menu is defined with a [**MENUINFO.dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) value of **MNS\_NOTIFYBYPOS**, [**WM\_MENUCOMMAND**](wm-menucommand.md) is sent instead of **WM\_COMMAND**.</span></span>

### <a name="accelerators"></a><span data-ttu-id="05491-136">Aceleradores</span><span class="sxs-lookup"><span data-stu-id="05491-136">Accelerators</span></span>

<span data-ttu-id="05491-137">Os pressionamentos de teclas do acelerador que selecionam itens no menu janela são convertidos em mensagens do [**WM \_ SYSCOMMAND**](wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="05491-137">Accelerator keystrokes that select items from the window menu are translated into [**WM\_SYSCOMMAND**](wm-syscommand.md) messages.</span></span>

<span data-ttu-id="05491-138">Se ocorrer uma tecla aceleradora que corresponda a um item de menu quando a janela proprietária do menu for minimizada, nenhuma mensagem de **\_ comando do WM** será enviada.</span><span class="sxs-lookup"><span data-stu-id="05491-138">If an accelerator keystroke occurs that corresponds to a menu item when the window that owns the menu is minimized, no **WM\_COMMAND** message is sent.</span></span> <span data-ttu-id="05491-139">No entanto, se ocorrer uma tecla aceleradora que não corresponda a nenhum dos itens no menu da janela ou no menu janela, uma mensagem de **\_ comando do WM** será enviada, mesmo que a janela seja minimizada.</span><span class="sxs-lookup"><span data-stu-id="05491-139">However, if an accelerator keystroke occurs that does not match any of the items in the window's menu or in the window menu, a **WM\_COMMAND** message is sent, even if the window is minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="05491-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05491-140">Requirements</span></span>



| <span data-ttu-id="05491-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="05491-141">Requirement</span></span> | <span data-ttu-id="05491-142">Valor</span><span class="sxs-lookup"><span data-stu-id="05491-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05491-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05491-143">Minimum supported client</span></span><br/> | <span data-ttu-id="05491-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="05491-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="05491-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05491-145">Minimum supported server</span></span><br/> | <span data-ttu-id="05491-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="05491-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05491-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="05491-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="05491-148"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05491-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05491-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="05491-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="05491-150">**Referência**</span><span class="sxs-lookup"><span data-stu-id="05491-150">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="05491-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="05491-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="05491-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="05491-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="05491-153">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="05491-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="05491-154">Menus</span><span class="sxs-lookup"><span data-stu-id="05491-154">Menus</span></span>](menus.md)
</dt> </dl>

 


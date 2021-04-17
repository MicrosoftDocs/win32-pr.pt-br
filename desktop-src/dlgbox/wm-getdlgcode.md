---
title: Mensagem de WM_GETDLGCODE (WinUser. h)
description: Enviado para o procedimento de janela associado a um controle.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- Caixas de diálogo de WM_GETDLGCODE mensagem
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811513"
---
# <a name="wm_getdlgcode-message"></a><span data-ttu-id="99583-104">Mensagem do WM \_ GETDLGCODE</span><span class="sxs-lookup"><span data-stu-id="99583-104">WM\_GETDLGCODE message</span></span>

<span data-ttu-id="99583-105">Enviado para o procedimento de janela associado a um controle.</span><span class="sxs-lookup"><span data-stu-id="99583-105">Sent to the window procedure associated with a control.</span></span> <span data-ttu-id="99583-106">Por padrão, o sistema manipula toda a entrada de teclado para o controle; o sistema interpreta determinados tipos de entrada de teclado como chaves de navegação da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="99583-106">By default, the system handles all keyboard input to the control; the system interprets certain types of keyboard input as dialog box navigation keys.</span></span> <span data-ttu-id="99583-107">Para substituir esse comportamento padrão, o controle pode responder à mensagem do **WM \_ GETDLGCODE** para indicar os tipos de entrada que ele deseja processar.</span><span class="sxs-lookup"><span data-stu-id="99583-107">To override this default behavior, the control can respond to the **WM\_GETDLGCODE** message to indicate the types of input it wants to process itself.</span></span>


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a><span data-ttu-id="99583-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99583-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99583-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99583-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99583-110">A chave virtual, pressionada pelo usuário, que solicitou que o Windows emitisse essa notificação.</span><span class="sxs-lookup"><span data-stu-id="99583-110">The virtual key, pressed by the user, that prompted Windows to issue this notification.</span></span> <span data-ttu-id="99583-111">O manipulador deve lidar seletivamente com essas chaves.</span><span class="sxs-lookup"><span data-stu-id="99583-111">The handler must selectively handle these keys.</span></span> <span data-ttu-id="99583-112">Por exemplo, o manipulador pode aceitar e processar **VK \_ Return** , mas delegar **VK \_ Tab** para a janela do proprietário.</span><span class="sxs-lookup"><span data-stu-id="99583-112">For instance, the handler might accept and process **VK\_RETURN** but delegate **VK\_TAB** to the owner window.</span></span> <span data-ttu-id="99583-113">Para obter uma lista de valores, consulte [**códigos de chave virtual**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="99583-113">For a list of values, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="99583-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99583-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99583-115">Um ponteiro para uma estrutura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) (ou **NULL** se o sistema estiver executando uma consulta).</span><span class="sxs-lookup"><span data-stu-id="99583-115">A pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure (or **NULL** if the system is performing a query).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99583-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99583-116">Return value</span></span>

<span data-ttu-id="99583-117">O valor de retorno é um ou mais dos valores a seguir, indicando qual tipo de entrada o aplicativo processa.</span><span class="sxs-lookup"><span data-stu-id="99583-117">The return value is one or more of the following values, indicating which type of input the application processes.</span></span>



| <span data-ttu-id="99583-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="99583-118">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="99583-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="99583-119">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="99583-120"><dt>**DLGC \_ BOTÃO**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="99583-120"><dt>**DLGC\_BUTTON**</dt> <dt>0x2000</dt></span></span> </dl>          | <span data-ttu-id="99583-121">Button.</span><span class="sxs-lookup"><span data-stu-id="99583-121">Button.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="99583-122"><dt>**DLGC \_ DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="99583-122"><dt>**DLGC\_DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>   | <span data-ttu-id="99583-123">Botão de ação padrão.</span><span class="sxs-lookup"><span data-stu-id="99583-123">Default push button.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="99583-124"><dt>**DLGC \_ HASSETSEL**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="99583-124"><dt>**DLGC\_HASSETSEL**</dt> <dt>0x0008</dt></span></span> </dl>       | <span data-ttu-id="99583-125">[**Em \_ Mensagens SETSEL**](/windows/desktop/Controls/em-setsel) .</span><span class="sxs-lookup"><span data-stu-id="99583-125">[**EM\_SETSEL**](/windows/desktop/Controls/em-setsel) messages.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="99583-126"><dt>**DLGC \_**</dt> <dt>0X0040</dt> do botão de opção</span><span class="sxs-lookup"><span data-stu-id="99583-126"><dt>**DLGC\_RADIOBUTTON**</dt> <dt>0x0040</dt></span></span> </dl>     | <span data-ttu-id="99583-127">Botão de opção.</span><span class="sxs-lookup"><span data-stu-id="99583-127">Radio button.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="99583-128"><dt>**DLGC \_**</dt> <dt>0x0100</dt> estático</span><span class="sxs-lookup"><span data-stu-id="99583-128"><dt>**DLGC\_STATIC**</dt> <dt>0x0100</dt></span></span> </dl>          | <span data-ttu-id="99583-129">Controle estático.</span><span class="sxs-lookup"><span data-stu-id="99583-129">Static control.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="99583-130"><dt>**DLGC \_ UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="99583-130"><dt>**DLGC\_UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="99583-131">Botão de ação não padrão.</span><span class="sxs-lookup"><span data-stu-id="99583-131">Non-default push button.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="99583-132"><dt>**DLGC \_ WANTALLKEYS**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="99583-132"><dt>**DLGC\_WANTALLKEYS**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="99583-133">Todas as entradas de teclado.</span><span class="sxs-lookup"><span data-stu-id="99583-133">All keyboard input.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="99583-134"><dt>**DLGC \_ WANTARROWS**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="99583-134"><dt>**DLGC\_WANTARROWS**</dt> <dt>0x0001</dt></span></span> </dl>      | <span data-ttu-id="99583-135">Teclas de direção.</span><span class="sxs-lookup"><span data-stu-id="99583-135">Direction keys.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="99583-136"><dt>**DLGC \_ WANTCHARS**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="99583-136"><dt>**DLGC\_WANTCHARS**</dt> <dt>0x0080</dt></span></span> </dl>       | <span data-ttu-id="99583-137">[**WM \_ Mensagens CHAR**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="99583-137">[**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="99583-138"><dt>**DLGC \_ WANTMESSAGE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="99583-138"><dt>**DLGC\_WANTMESSAGE**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="99583-139">Todas as entradas de teclado (o aplicativo passa essa mensagem na estrutura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) para o controle).</span><span class="sxs-lookup"><span data-stu-id="99583-139">All keyboard input (the application passes this message in the [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure to the control).</span></span><br/> |
| <dl> <span data-ttu-id="99583-140"><dt>**DLGC \_ WANTTAB**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="99583-140"><dt>**DLGC\_WANTTAB**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="99583-141">Tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="99583-141">TAB key.</span></span><br/>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="99583-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="99583-142">Remarks</span></span>

<span data-ttu-id="99583-143">Embora a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sempre retorne zero em resposta à mensagem do **WM \_ GETDLGCODE** , o procedimento de janela para as classes de controle predefinidas retorna um código apropriado para cada classe.</span><span class="sxs-lookup"><span data-stu-id="99583-143">Although the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function always returns zero in response to the **WM\_GETDLGCODE** message, the window procedure for the predefined control classes return a code appropriate for each class.</span></span>

<span data-ttu-id="99583-144">A mensagem do **WM \_ GETDLGCODE** e os valores retornados são úteis somente com controles de caixa de diálogo definidos pelo usuário ou controles padrão modificados por subclasses.</span><span class="sxs-lookup"><span data-stu-id="99583-144">The **WM\_GETDLGCODE** message and the returned values are useful only with user-defined dialog box controls or standard controls modified by subclassing.</span></span>

## <a name="requirements"></a><span data-ttu-id="99583-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99583-145">Requirements</span></span>



| <span data-ttu-id="99583-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="99583-146">Requirement</span></span> | <span data-ttu-id="99583-147">Valor</span><span class="sxs-lookup"><span data-stu-id="99583-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99583-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99583-148">Minimum supported client</span></span><br/> | <span data-ttu-id="99583-149">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99583-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="99583-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99583-150">Minimum supported server</span></span><br/> | <span data-ttu-id="99583-151">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99583-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99583-152">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99583-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="99583-153"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99583-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99583-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="99583-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="99583-155">**Referência**</span><span class="sxs-lookup"><span data-stu-id="99583-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="99583-156">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="99583-156">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="99583-157">**em \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="99583-157">**EM\_SETSEL**</span></span>](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[<span data-ttu-id="99583-158">**MSG**</span><span class="sxs-lookup"><span data-stu-id="99583-158">**MSG**</span></span>](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[<span data-ttu-id="99583-159">**caractere do WM \_**</span><span class="sxs-lookup"><span data-stu-id="99583-159">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> <dt>

<span data-ttu-id="99583-160">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="99583-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="99583-161">Caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="99583-161">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 


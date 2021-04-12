---
title: Mensagem de WM_VKEYTOITEM (WinUser. h)
description: Enviado por uma caixa de listagem com o \_ estilo de lbs WANTKEYBOARDINPUT para seu proprietário em resposta a uma mensagem do WM \_ KEYDOWN.
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- Controles de WM_VKEYTOITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "104297995"
---
# <a name="wm_vkeytoitem-message"></a><span data-ttu-id="6b4f0-104">Mensagem do WM \_ VKEYTOITEM</span><span class="sxs-lookup"><span data-stu-id="6b4f0-104">WM\_VKEYTOITEM message</span></span>

<span data-ttu-id="6b4f0-105">Enviado por uma caixa de listagem com o estilo de [**lbs \_ WANTKEYBOARDINPUT**](list-box-styles.md) para seu proprietário em resposta a uma mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="6b4f0-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span>


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6b4f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b4f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b4f0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b4f0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b4f0-108">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o código de chave virtual da chave que o usuário pressionou.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the virtual-key code of the key the user pressed.</span></span> <span data-ttu-id="6b4f0-109">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="6b4f0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b4f0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b4f0-111">Identificador para a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b4f0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b4f0-112">Return value</span></span>

<span data-ttu-id="6b4f0-113">O valor de retorno especifica a ação que o aplicativo realizou em resposta à mensagem.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="6b4f0-114">Um valor de retorno de-2 indica que o aplicativo tratou todos os aspectos da seleção do item e não requer nenhuma ação adicional na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-114">A return value of -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="6b4f0-115">(Consulte comentários.) Um valor de retorno de-1 indica que a caixa de listagem deve executar a ação padrão em resposta ao pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-115">(See Remarks.) A return value of -1 indicates that the list box should perform the default action in response to the keystroke.</span></span> <span data-ttu-id="6b4f0-116">Um valor de retorno 0 ou maior especifica o índice de um item na caixa de listagem e indica que a caixa de listagem deve executar a ação padrão para o pressionamento de tecla no item especificado.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-116">A return value of 0 or greater specifies the index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b4f0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b4f0-117">Remarks</span></span>

<span data-ttu-id="6b4f0-118">Um valor de retorno de-2 é válido somente para chaves que não são convertidas em caracteres pelo controle de caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-118">A return value of -2 is valid only for keys that are not translated into characters by the list box control.</span></span> <span data-ttu-id="6b4f0-119">Se a mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) estiver convertida em uma mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) e o aplicativo processar a mensagem do **WM \_ VKEYTOITEM** gerada como resultado do pressionamento da tecla, a caixa de listagem ignorará o valor de retorno e fará o processamento padrão para esse caractere).</span><span class="sxs-lookup"><span data-stu-id="6b4f0-119">If the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message translates to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message and the application processes the **WM\_VKEYTOITEM** message generated as a result of the key press, the list box ignores the return value and does the default processing for that character).</span></span> <span data-ttu-id="6b4f0-120">**WM \_** As mensagens de KEYDOWN geradas por chaves como VK \_ up, VK \_ down, VK \_ Next e VK \_ Previous não são convertidas em mensagens do **WM \_ Char** .</span><span class="sxs-lookup"><span data-stu-id="6b4f0-120">**WM\_KEYDOWN** messages generated by keys such as VK\_UP, VK\_DOWN, VK\_NEXT, and VK\_PREVIOUS are not translated to **WM\_CHAR** messages.</span></span> <span data-ttu-id="6b4f0-121">Nesses casos, o trapping da mensagem **\_ VKEYTOITEM do WM** e o retorno de-2 impede que a caixa de listagem faça o processamento padrão para essa chave.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-121">In such cases, trapping the **WM\_VKEYTOITEM** message and returning -2 prevents the list box from doing the default processing for that key.</span></span>

<span data-ttu-id="6b4f0-122">Para ajustar as chaves que geram uma mensagem char e executar processamento especial, o aplicativo deve criar uma subclasse da caixa de listagem, interceptar as mensagens de [**\_ caracteres**](/windows/desktop/inputdev/wm-char) do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) e do WM e processar as mensagens adequadamente no procedimento de subclasse.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-122">To trap keys that generate a char message and do special processing, the application must subclass the list box, trap both the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) and [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages, and process the messages appropriately in the subclass procedure.</span></span>

<span data-ttu-id="6b4f0-123">Os comentários anteriores se aplicam a caixas de listagem normais que são criadas com o estilo [**lbs \_ WANTKEYBOARDINPUT**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6b4f0-123">The preceding remarks apply to regular list boxes that are created with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style.</span></span> <span data-ttu-id="6b4f0-124">Se a caixa de listagem for desenhada pelo proprietário, o aplicativo deverá processar a mensagem do [**WM \_ CHARTOITEM**](wm-chartoitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6b4f0-124">If the list box is owner-drawn, the application must process the [**WM\_CHARTOITEM**](wm-chartoitem.md) message.</span></span>

<span data-ttu-id="6b4f0-125">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna-1.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="6b4f0-126">Se um procedimento da caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado em um **bool** e retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-126">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="6b4f0-127">O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="6b4f0-127">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b4f0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b4f0-128">Requirements</span></span>



| <span data-ttu-id="6b4f0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b4f0-129">Requirement</span></span> | <span data-ttu-id="6b4f0-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6b4f0-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b4f0-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b4f0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6b4f0-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b4f0-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6b4f0-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b4f0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6b4f0-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b4f0-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b4f0-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b4f0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b4f0-136"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b4f0-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b4f0-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b4f0-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b4f0-138">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6b4f0-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6b4f0-139">**CHARTOITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b4f0-139">**WM\_CHARTOITEM**</span></span>](wm-chartoitem.md)
</dt> <dt>

<span data-ttu-id="6b4f0-140">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="6b4f0-140">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6b4f0-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b4f0-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6b4f0-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b4f0-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6b4f0-143">**o WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="6b4f0-143">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 


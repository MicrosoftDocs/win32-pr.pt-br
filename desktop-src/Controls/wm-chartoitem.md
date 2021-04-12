---
title: Mensagem de WM_CHARTOITEM (WinUser. h)
description: Enviado por uma caixa de listagem com o \_ estilo de lbs WANTKEYBOARDINPUT para seu proprietário em resposta a uma mensagem do WM \_ Char.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- Controles de WM_CHARTOITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104298432"
---
# <a name="wm_chartoitem-message"></a><span data-ttu-id="142eb-104">Mensagem do WM \_ CHARTOITEM</span><span class="sxs-lookup"><span data-stu-id="142eb-104">WM\_CHARTOITEM message</span></span>

<span data-ttu-id="142eb-105">Enviado por uma caixa de listagem com o estilo de [**lbs \_ WANTKEYBOARDINPUT**](list-box-styles.md) para seu proprietário em resposta a uma mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="142eb-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="142eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="142eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="142eb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="142eb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="142eb-108">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o código de caractere da chave que o usuário pressionou.</span><span class="sxs-lookup"><span data-stu-id="142eb-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the character code of the key the user pressed.</span></span> <span data-ttu-id="142eb-109">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="142eb-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="142eb-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="142eb-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="142eb-111">Identificador para a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="142eb-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="142eb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="142eb-112">Return value</span></span>

<span data-ttu-id="142eb-113">O valor de retorno especifica a ação que o aplicativo realizou em resposta à mensagem.</span><span class="sxs-lookup"><span data-stu-id="142eb-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="142eb-114">Um valor de retorno de-1 ou-2 indica que o aplicativo tratou todos os aspectos da seleção do item e não requer nenhuma ação adicional na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="142eb-114">A return value of -1 or -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="142eb-115">Um valor de retorno igual a 0 ou superior especifica o índice de base zero de um item na caixa de listagem e indica que a caixa de listagem deve executar a ação padrão para o pressionamento de tecla no item especificado.</span><span class="sxs-lookup"><span data-stu-id="142eb-115">A return value of 0 or greater specifies the zero-based index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="142eb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="142eb-116">Remarks</span></span>

<span data-ttu-id="142eb-117">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna-1.</span><span class="sxs-lookup"><span data-stu-id="142eb-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="142eb-118">Somente as caixas de listagem desenhadas pelo proprietário que não têm o estilo de [**lb \_ HASSTRINGS**](list-box-styles.md) podem receber essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="142eb-118">Only owner-drawn list boxes that do not have the [**LBS\_HASSTRINGS**](list-box-styles.md) style can receive this message.</span></span>

<span data-ttu-id="142eb-119">Se um procedimento da caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado em um **bool** e retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="142eb-119">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="142eb-120">O valor de *\_ MSGRESULT DWL* definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="142eb-120">The *DWL\_MSGRESULT* value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="142eb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="142eb-121">Requirements</span></span>



| <span data-ttu-id="142eb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="142eb-122">Requirement</span></span> | <span data-ttu-id="142eb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="142eb-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="142eb-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="142eb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="142eb-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="142eb-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="142eb-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="142eb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="142eb-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="142eb-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="142eb-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="142eb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="142eb-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="142eb-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="142eb-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="142eb-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="142eb-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="142eb-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="142eb-132">**VKEYTOITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="142eb-132">**WM\_VKEYTOITEM**</span></span>](wm-vkeytoitem.md)
</dt> <dt>

<span data-ttu-id="142eb-133">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="142eb-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="142eb-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="142eb-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="142eb-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="142eb-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="142eb-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="142eb-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="142eb-137">**caractere do WM \_**</span><span class="sxs-lookup"><span data-stu-id="142eb-137">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 


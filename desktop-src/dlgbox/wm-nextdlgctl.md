---
title: Mensagem de WM_NEXTDLGCTL (WinUser. h)
description: Enviado a um procedimento de caixa de diálogo para definir o foco do teclado para um controle diferente na caixa de diálogo.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- Caixas de diálogo de WM_NEXTDLGCTL mensagem
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499563"
---
# <a name="wm_nextdlgctl-message"></a><span data-ttu-id="584b2-104">Mensagem do WM \_ NEXTDLGCTL</span><span class="sxs-lookup"><span data-stu-id="584b2-104">WM\_NEXTDLGCTL message</span></span>

<span data-ttu-id="584b2-105">Enviado a um procedimento de caixa de diálogo para definir o foco do teclado para um controle diferente na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="584b2-105">Sent to a dialog box procedure to set the keyboard focus to a different control in the dialog box.</span></span>


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a><span data-ttu-id="584b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="584b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="584b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="584b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="584b2-108">Se *lParam* for **true**, esse parâmetro identificará o controle que recebe o foco.</span><span class="sxs-lookup"><span data-stu-id="584b2-108">If *lParam* is **TRUE**, this parameter identifies the control that receives the focus.</span></span> <span data-ttu-id="584b2-109">Se *lParam* for **false**, esse parâmetro indicará se o controle seguinte ou anterior com o estilo **WS \_ TabStop** receberá o foco.</span><span class="sxs-lookup"><span data-stu-id="584b2-109">If *lParam* is **FALSE**, this parameter indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span> <span data-ttu-id="584b2-110">Se *wParam* for zero, o próximo controle receberá o foco; caso contrário, o controle anterior com o estilo **WS \_ TabStop** receberá o foco.</span><span class="sxs-lookup"><span data-stu-id="584b2-110">If *wParam* is zero, the next control receives the focus; otherwise, the previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> <dt>

<span data-ttu-id="584b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="584b2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="584b2-112">A palavra de ordem inferior indica como o sistema usa *wParam*.</span><span class="sxs-lookup"><span data-stu-id="584b2-112">The low-order word indicates how the system uses *wParam*.</span></span> <span data-ttu-id="584b2-113">Se a palavra de ordem inferior for **verdadeira**, *wParam* é um identificador associado ao controle que recebe o foco; caso contrário, *wParam* é um sinalizador que indica se o controle seguinte ou anterior com o estilo **WS \_ TabStop** recebe o foco.</span><span class="sxs-lookup"><span data-stu-id="584b2-113">If the low-order word is **TRUE**, *wParam* is a handle associated with the control that receives the focus; otherwise, *wParam* is a flag that indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="584b2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="584b2-114">Return value</span></span>

<span data-ttu-id="584b2-115">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="584b2-115">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="584b2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="584b2-116">Remarks</span></span>

<span data-ttu-id="584b2-117">Essa mensagem executa operações de gerenciamento de caixa de diálogo adicionais além daquelas executadas pela função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) do **WM \_ NEXTDLGCTL** atualiza a borda de pressão padrão, define o identificador de controle padrão e seleciona automaticamente o texto de um controle de edição (se a janela de destino for um controle de edição).</span><span class="sxs-lookup"><span data-stu-id="584b2-117">This message performs additional dialog box management operations beyond those performed by the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function **WM\_NEXTDLGCTL** updates the default pushbutton border, sets the default control identifier, and automatically selects the text of an edit control (if the target window is an edit control).</span></span>

<span data-ttu-id="584b2-118">Não use a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para enviar uma mensagem do **WM \_ NEXTDLGCTL** se seu aplicativo processar simultaneamente outras mensagens que definirem o foco.</span><span class="sxs-lookup"><span data-stu-id="584b2-118">Do not use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to send a **WM\_NEXTDLGCTL** message if your application will concurrently process other messages that set the focus.</span></span> <span data-ttu-id="584b2-119">Em vez disso, use a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .</span><span class="sxs-lookup"><span data-stu-id="584b2-119">Use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="584b2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="584b2-120">Requirements</span></span>



| <span data-ttu-id="584b2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="584b2-121">Requirement</span></span> | <span data-ttu-id="584b2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="584b2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="584b2-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="584b2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="584b2-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="584b2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="584b2-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="584b2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="584b2-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="584b2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="584b2-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="584b2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="584b2-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="584b2-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="584b2-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="584b2-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="584b2-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="584b2-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="584b2-131">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="584b2-131">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="584b2-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="584b2-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="584b2-133">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="584b2-133">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="584b2-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="584b2-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="584b2-135">Caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="584b2-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 


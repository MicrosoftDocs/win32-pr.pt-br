---
title: Mensagem de WM_DRAWITEM (WinUser. h)
description: Enviado para a janela pai de um botão, caixa de combinação, caixa de listagem ou menu de desenho de proprietário quando um aspecto visual do botão, caixa de combinação, caixa de listagem ou menu foi alterado.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- Controles de WM_DRAWITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644615"
---
# <a name="wm_drawitem-message"></a><span data-ttu-id="a93af-104">Mensagem do WM \_ DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="a93af-104">WM\_DRAWITEM message</span></span>

<span data-ttu-id="a93af-105">Enviado para a janela pai de um botão, caixa de combinação, caixa de listagem ou menu de desenho de proprietário quando um aspecto visual do botão, caixa de combinação, caixa de listagem ou menu foi alterado.</span><span class="sxs-lookup"><span data-stu-id="a93af-105">Sent to the parent window of an owner-drawn button, combo box, list box, or menu when a visual aspect of the button, combo box, list box, or menu has changed.</span></span>

<span data-ttu-id="a93af-106">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a93af-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a93af-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a93af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a93af-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a93af-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a93af-109">Especifica o identificador do controle que enviou a mensagem **de \_ DRAWITEM do WM** .</span><span class="sxs-lookup"><span data-stu-id="a93af-109">Specifies the identifier of the control that sent the **WM\_DRAWITEM** message.</span></span> <span data-ttu-id="a93af-110">Se a mensagem foi enviada por um menu, esse parâmetro será zero.</span><span class="sxs-lookup"><span data-stu-id="a93af-110">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="a93af-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a93af-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a93af-112">Ponteiro para uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contém informações sobre o item a ser desenhado e o tipo de desenho necessário.</span><span class="sxs-lookup"><span data-stu-id="a93af-112">Pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a93af-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a93af-113">Return value</span></span>

<span data-ttu-id="a93af-114">Se um aplicativo processar essa mensagem, ele deverá retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="a93af-114">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a93af-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a93af-115">Remarks</span></span>

<span data-ttu-id="a93af-116">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) desenha o retângulo de foco para um item da caixa de listagem desenhada pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="a93af-116">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the focus rectangle for an owner-drawn list box item.</span></span>

<span data-ttu-id="a93af-117">O membro de *ação* da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) especifica a operação de desenho que um aplicativo deve executar.</span><span class="sxs-lookup"><span data-stu-id="a93af-117">The *itemAction* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="a93af-118">Antes de retornar do processamento dessa mensagem, um aplicativo deve garantir que o contexto do dispositivo identificado pelo membro *HDC* da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) esteja no estado padrão.</span><span class="sxs-lookup"><span data-stu-id="a93af-118">Before returning from processing this message, an application should ensure that the device context identified by the *hDC* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="a93af-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a93af-119">Requirements</span></span>



| <span data-ttu-id="a93af-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a93af-120">Requirement</span></span> | <span data-ttu-id="a93af-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a93af-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a93af-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a93af-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a93af-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a93af-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a93af-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a93af-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a93af-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a93af-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a93af-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a93af-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a93af-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a93af-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a93af-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a93af-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="a93af-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a93af-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a93af-130">**DRAWITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="a93af-130">**DRAWITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

<span data-ttu-id="a93af-131">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="a93af-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a93af-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="a93af-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 


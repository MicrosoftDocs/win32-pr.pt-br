---
title: Mensagem de TCM_SETCURFOCUS (commctrl. h)
description: Define o foco para uma guia especificada em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetCurFocus.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- Controles de TCM_SETCURFOCUS de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918478"
---
# <a name="tcm_setcurfocus-message"></a><span data-ttu-id="d13cc-105">\_Mensagem SETCURFOCUS de TCM</span><span class="sxs-lookup"><span data-stu-id="d13cc-105">TCM\_SETCURFOCUS message</span></span>

<span data-ttu-id="d13cc-106">Define o foco para uma guia especificada em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="d13cc-106">Sets the focus to a specified tab in a tab control.</span></span> <span data-ttu-id="d13cc-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) .</span><span class="sxs-lookup"><span data-stu-id="d13cc-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d13cc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d13cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d13cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d13cc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d13cc-110">Índice da guia que obtém o foco.</span><span class="sxs-lookup"><span data-stu-id="d13cc-110">Index of the tab that gets the focus.</span></span>

</dd> <dt>

<span data-ttu-id="d13cc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d13cc-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d13cc-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d13cc-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d13cc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d13cc-113">Return value</span></span>

<span data-ttu-id="d13cc-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d13cc-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d13cc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d13cc-115">Remarks</span></span>

<span data-ttu-id="d13cc-116">Se o controle guia tiver o estilo de [**\_ botões de TCS**](tab-control-styles.md) (modo de botão), a guia com o foco poderá ser diferente da guia selecionada. Por exemplo, quando uma guia é selecionada, o usuário pode pressionar as teclas de seta para definir o foco para uma guia diferente sem alterar a guia selecionada. No modo de botão, o **TCM \_ SETCURFOCUS** define o foco de entrada para o botão associado à guia especificada, mas não altera a guia selecionada.</span><span class="sxs-lookup"><span data-stu-id="d13cc-116">If the tab control has the [**TCS\_BUTTONS**](tab-control-styles.md) style (button mode), the tab with the focus may be different from the selected tab. For example, when a tab is selected, the user can press the arrow keys to set the focus to a different tab without changing the selected tab. In button mode, **TCM\_SETCURFOCUS** sets the input focus to the button associated with the specified tab, but it does not change the selected tab.</span></span>

<span data-ttu-id="d13cc-117">Se o controle guia não tiver o estilo [**de \_ botões de TCS**](tab-control-styles.md) , alterar o foco também alterará a guia selecionada. Nesse caso, o controle guia envia os códigos de notificação [TCN \_ SELCHANGING](tcn-selchanging.md) e [TCN \_ SELCHANGE](tcn-selchange.md) para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="d13cc-117">If the tab control does not have the [**TCS\_BUTTONS**](tab-control-styles.md) style, changing the focus also changes the selected tab. In this case, the tab control sends the [TCN\_SELCHANGING](tcn-selchanging.md) and [TCN\_SELCHANGE](tcn-selchange.md) notification codes to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d13cc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d13cc-118">Requirements</span></span>



| <span data-ttu-id="d13cc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d13cc-119">Requirement</span></span> | <span data-ttu-id="d13cc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d13cc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d13cc-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d13cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d13cc-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d13cc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d13cc-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d13cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d13cc-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d13cc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d13cc-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d13cc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d13cc-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d13cc-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d13cc-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d13cc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d13cc-128">**\_GETCURFOCUS TCM**</span><span class="sxs-lookup"><span data-stu-id="d13cc-128">**TCM\_GETCURFOCUS**</span></span>](tcm-getcurfocus.md)
</dt> </dl>

 

 






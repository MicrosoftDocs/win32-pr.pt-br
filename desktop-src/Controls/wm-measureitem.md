---
title: Mensagem de WM_MEASUREITEM (WinUser. h)
description: Enviado para a janela do proprietário de uma caixa de combinação, caixa de listagem, controle de exibição de lista ou item de menu quando o controle ou o menu é criado.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- Controles de WM_MEASUREITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824560"
---
# <a name="wm_measureitem-message"></a><span data-ttu-id="f1566-104">Mensagem do WM \_ MEASUREITEM</span><span class="sxs-lookup"><span data-stu-id="f1566-104">WM\_MEASUREITEM message</span></span>

<span data-ttu-id="f1566-105">Enviado para a janela do proprietário de uma caixa de combinação, caixa de listagem, controle de exibição de lista ou item de menu quando o controle ou o menu é criado.</span><span class="sxs-lookup"><span data-stu-id="f1566-105">Sent to the owner window of a combo box, list box, list-view control, or menu item when the control or menu is created.</span></span>

<span data-ttu-id="f1566-106">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f1566-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f1566-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1566-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1566-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1566-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1566-109">Contém o valor do membro **CtlID** da estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) apontada pelo parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f1566-109">Contains the value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="f1566-110">Esse valor identifica o controle que enviou a mensagem de **\_ MEASUREITEM do WM** .</span><span class="sxs-lookup"><span data-stu-id="f1566-110">This value identifies the control that sent the **WM\_MEASUREITEM** message.</span></span> <span data-ttu-id="f1566-111">Se o valor for zero, a mensagem foi enviada por um menu.</span><span class="sxs-lookup"><span data-stu-id="f1566-111">If the value is zero, the message was sent by a menu.</span></span> <span data-ttu-id="f1566-112">Se o valor for diferente de zero, a mensagem foi enviada por uma caixa de combinação ou por uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="f1566-112">If the value is nonzero, the message was sent by a combo box or by a list box.</span></span> <span data-ttu-id="f1566-113">Se o valor for diferente de zero e o valor do membro **ItemId** do **MEASUREITEMSTRUCT** apontado por *lParam* for (UINT) 1, a mensagem foi enviada por um campo de edição de combinação.</span><span class="sxs-lookup"><span data-stu-id="f1566-113">If the value is nonzero, and the value of the **itemID** member of the **MEASUREITEMSTRUCT** pointed to by *lParam* is (UINT)  1, the message was sent by a combo edit field.</span></span>

</dd> <dt>

<span data-ttu-id="f1566-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1566-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1566-115">Ponteiro para uma estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que contém as dimensões do controle ou item de menu desenhado pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="f1566-115">Pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1566-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1566-116">Return value</span></span>

<span data-ttu-id="f1566-117">Se um aplicativo processar essa mensagem, ele deverá retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="f1566-117">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1566-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1566-118">Remarks</span></span>

<span data-ttu-id="f1566-119">Quando a janela do proprietário recebe a mensagem **\_ MEASUREITEM do WM** , o proprietário preenche a estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) apontada pelo parâmetro *lParam* da mensagem e retorna; isso informa o sistema das dimensões do controle.</span><span class="sxs-lookup"><span data-stu-id="f1566-119">When the owner window receives the **WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span> <span data-ttu-id="f1566-120">Se uma caixa de listagem ou caixa de combinação for criada com o estilo [**de \_ OwnerDrawVariable**](combo-box-styles.md) [**lbs \_ OwnerDrawVariable**](list-box-styles.md) ou CBS, essa mensagem será enviada ao proprietário de cada item no controle; caso contrário, essa mensagem será enviada uma vez.</span><span class="sxs-lookup"><span data-stu-id="f1566-120">If a list box or combo box is created with the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, this message is sent to the owner for each item in the control; otherwise, this message is sent once.</span></span>

<span data-ttu-id="f1566-121">O sistema envia a mensagem do **WM \_ MEASUREITEM** para a janela do proprietário de caixas de combinação e caixas de listagem criadas com o estilo OwnerDrawFixed antes de enviar a mensagem [**\_ INITDIALOG do WM**](/windows/desktop/dlgbox/wm-initdialog) .</span><span class="sxs-lookup"><span data-stu-id="f1566-121">The system sends the **WM\_MEASUREITEM** message to the owner window of combo boxes and list boxes created with the OWNERDRAWFIXED style before sending the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="f1566-122">Como resultado, quando o proprietário recebe essa mensagem, o sistema ainda não determinou a altura e a largura da fonte usada no controle; as chamadas de função e os cálculos que exigem esses valores devem ocorrer na função principal do aplicativo ou da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f1566-122">As a result, when the owner receives this message, the system has not yet determined the height and width of the font used in the control; function calls and calculations requiring these values should occur in the main function of the application or library.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1566-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1566-123">Requirements</span></span>



| <span data-ttu-id="f1566-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1566-124">Requirement</span></span> | <span data-ttu-id="f1566-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f1566-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1566-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1566-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f1566-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1566-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f1566-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1566-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f1566-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f1566-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f1566-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1566-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1566-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1566-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1566-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1566-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1566-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="f1566-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f1566-134">**MEASUREITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="f1566-134">**MEASUREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

<span data-ttu-id="f1566-135">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="f1566-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f1566-136">**INITDIALOG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f1566-136">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 


---
title: Mensagem de EM_SETTABSTOPS (WinUser. h)
description: A \_ mensagem em SETtabstops define as paradas de tabulação em um controle de edição de várias linhas.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- Controles de EM_SETTABSTOPS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085733"
---
# <a name="em_settabstops-message"></a><span data-ttu-id="c4e04-104">\_Mensagem em SETtabstops</span><span class="sxs-lookup"><span data-stu-id="c4e04-104">EM\_SETTABSTOPS message</span></span>

<span data-ttu-id="c4e04-105">A mensagem em **\_ SetTabStops** define as paradas de tabulação em um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="c4e04-105">The **EM\_SETTABSTOPS** message sets the tab stops in a multiline edit control.</span></span> <span data-ttu-id="c4e04-106">Quando o texto é copiado para o controle, qualquer caractere de tabulação no texto faz com que o espaço seja gerado até a próxima parada de tabulação.</span><span class="sxs-lookup"><span data-stu-id="c4e04-106">When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop.</span></span>

<span data-ttu-id="c4e04-107">Essa mensagem é processada somente por controles de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="c4e04-107">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="c4e04-108">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="c4e04-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4e04-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4e04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4e04-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4e04-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4e04-111">O número de paradas de tabulação contidas na matriz.</span><span class="sxs-lookup"><span data-stu-id="c4e04-111">The number of tab stops contained in the array.</span></span> <span data-ttu-id="c4e04-112">Se esse parâmetro for zero, o parâmetro *lParam* será ignorado e as tabulações padrão serão definidas a cada unidades de modelo de caixa de diálogo de 32.</span><span class="sxs-lookup"><span data-stu-id="c4e04-112">If this parameter is zero, the *lParam* parameter is ignored and default tab stops are set at every 32 dialog template units.</span></span> <span data-ttu-id="c4e04-113">Se esse parâmetro for 1, as paradas de tabulação serão definidas a cada *n* unidades de modelo de caixa de diálogo, em que *n* é a distância apontada pelo parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c4e04-113">If this parameter is 1, tab stops are set at every *n* dialog template units, where *n* is the distance pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="c4e04-114">Se esse parâmetro for maior que 1, *lParam* será um ponteiro para uma matriz de paradas de tabulação.</span><span class="sxs-lookup"><span data-stu-id="c4e04-114">If this parameter is greater than 1, *lParam* is a pointer to an array of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="c4e04-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4e04-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4e04-116">Um ponteiro para uma matriz de inteiros sem sinal especificando as paradas de tabulação, em unidades de modelo de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c4e04-116">A pointer to an array of unsigned integers specifying the tab stops, in dialog template units.</span></span> <span data-ttu-id="c4e04-117">Se o parâmetro *wParam* for 1, esse parâmetro será um ponteiro para um inteiro não assinado que contém a distância entre todas as paradas de tabulação, em unidades de modelo de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c4e04-117">If the *wParam* parameter is 1, this parameter is a pointer to an unsigned integer containing the distance between all tab stops, in dialog template units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4e04-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4e04-118">Return value</span></span>

<span data-ttu-id="c4e04-119">Se todas as guias estiverem definidas, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="c4e04-119">If all the tabs are set, the return value is **TRUE**.</span></span>

<span data-ttu-id="c4e04-120">Se todas as guias não estiverem definidas, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="c4e04-120">If all the tabs are not set, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4e04-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4e04-121">Remarks</span></span>

<span data-ttu-id="c4e04-122">A mensagem em **\_ SetTabStops** não redesenha automaticamente a janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="c4e04-122">The **EM\_SETTABSTOPS** message does not automatically redraw the edit control window.</span></span> <span data-ttu-id="c4e04-123">Se o aplicativo estiver alterando as paradas de tabulação para o texto já no controle de edição, ele deverá chamar a função [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) para redesenhar a janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="c4e04-123">If the application is changing the tab stops for text already in the edit control, it should call the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function to redraw the edit control window.</span></span>

<span data-ttu-id="c4e04-124">Os valores especificados na matriz estão em unidades de modelo de caixa de diálogo, que são as unidades independentes de dispositivo usadas em modelos de caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c4e04-124">The values specified in the array are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="c4e04-125">Para converter medidas de unidades de modelo de caixa de diálogo em unidades de tela (pixels), use a função [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="c4e04-125">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="c4e04-126">**Edição avançada:** Com suporte no Microsoft Rich Edit 3,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c4e04-126">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="c4e04-127">Um controle de edição rico pode ter o número máximo de paradas de tabulação especificado pelo máximo de \_ paradas de tabulação \_ .</span><span class="sxs-lookup"><span data-stu-id="c4e04-127">A rich edit control can have the maximum number of tab stops specified by MAX\_TAB\_STOPS.</span></span> <span data-ttu-id="c4e04-128">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c4e04-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4e04-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4e04-129">Requirements</span></span>



| <span data-ttu-id="c4e04-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4e04-130">Requirement</span></span> | <span data-ttu-id="c4e04-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c4e04-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e04-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4e04-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c4e04-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4e04-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c4e04-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4e04-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c4e04-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4e04-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4e04-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4e04-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4e04-137"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4e04-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4e04-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4e04-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4e04-139">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="c4e04-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c4e04-140">**InvalidateRect**</span><span class="sxs-lookup"><span data-stu-id="c4e04-140">**InvalidateRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[<span data-ttu-id="c4e04-141">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="c4e04-141">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 


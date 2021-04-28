---
title: Mensagem de EM_SETRECT (WinUser. h)
description: EM_SETRECT mensagem – define o retângulo de formatação de um controle de edição de várias linhas.
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- Controles de EM_SETRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042428a236b8e9a23f03cdcceaf5d76eb977efd8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085964"
---
# <a name="em_setrect-message"></a><span data-ttu-id="fbb88-104">\_Mensagem em SETrect</span><span class="sxs-lookup"><span data-stu-id="fbb88-104">EM\_SETRECT message</span></span>

<span data-ttu-id="fbb88-105">Define o [retângulo de formatação](about-edit-controls.md) de um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="fbb88-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="fbb88-106">O retângulo de formatação é o retângulo limitador no qual o controle desenha o texto.</span><span class="sxs-lookup"><span data-stu-id="fbb88-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="fbb88-107">O retângulo de limitação é independente do tamanho da janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="fbb88-107">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="fbb88-108">Essa mensagem é processada somente por controles de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="fbb88-108">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="fbb88-109">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="fbb88-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fbb88-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbb88-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb88-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbb88-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbb88-112">**Edição avançada 2,0 e posterior:** Indica se *lParam* especifica coordenadas absolutas ou relativas.</span><span class="sxs-lookup"><span data-stu-id="fbb88-112">**Rich Edit 2.0 and later:** Indicates whether *lParam* specifies absolute or relative coordinates.</span></span> <span data-ttu-id="fbb88-113">Um valor de zero indica coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="fbb88-113">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="fbb88-114">Um valor de 1 indica deslocamentos relativos ao retângulo de formatação atual.</span><span class="sxs-lookup"><span data-stu-id="fbb88-114">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="fbb88-115">(Os deslocamentos podem ser positivos ou negativos.)</span><span class="sxs-lookup"><span data-stu-id="fbb88-115">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="fbb88-116">**Editar controles e edição avançada 1,0:** Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fbb88-116">**Edit controls and Rich Edit 1.0:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fbb88-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbb88-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbb88-118">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica as novas dimensões do retângulo.</span><span class="sxs-lookup"><span data-stu-id="fbb88-118">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="fbb88-119">Se esse parâmetro for **NULL**, o retângulo de formatação será definido com seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="fbb88-119">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbb88-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fbb88-120">Return value</span></span>

<span data-ttu-id="fbb88-121">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fbb88-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbb88-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbb88-122">Remarks</span></span>

<span data-ttu-id="fbb88-123">Definir *lParam* como **nulo** não terá efeito se um dispositivo de toque estiver instalado ou se **em \_ SetRect** for enviado de um thread que tenha um gancho instalado (consulte [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span><span class="sxs-lookup"><span data-stu-id="fbb88-123">Setting *lParam* to **NULL** has no effect if a touch device is installed, or if **EM\_SETRECT** is sent from a thread that has a hook installed (see [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)).</span></span> <span data-ttu-id="fbb88-124">Nesses casos, *lParam* deve conter um ponteiro válido para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fbb88-124">In these cases, *lParam* should contain a valid pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span>

<span data-ttu-id="fbb88-125">A mensagem em **\_ SetRect** faz com que o texto do controle de edição seja redesenhado.</span><span class="sxs-lookup"><span data-stu-id="fbb88-125">The **EM\_SETRECT** message causes the text of the edit control to be redrawn.</span></span> <span data-ttu-id="fbb88-126">Para alterar o tamanho do retângulo de formatação sem redesenhar o texto, use a mensagem [**em \_ SETRECTNP**](em-setrectnp.md) .</span><span class="sxs-lookup"><span data-stu-id="fbb88-126">To change the size of the formatting rectangle without redrawing the text, use the [**EM\_SETRECTNP**](em-setrectnp.md) message.</span></span>

<span data-ttu-id="fbb88-127">Quando um controle de edição é criado pela primeira vez, o retângulo de formatação é definido como um tamanho padrão.</span><span class="sxs-lookup"><span data-stu-id="fbb88-127">When an edit control is first created, the formatting rectangle is set to a default size.</span></span> <span data-ttu-id="fbb88-128">Você pode usar a mensagem com **\_ SetRect** para tornar o retângulo de formatação maior ou menor do que a janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="fbb88-128">You can use the **EM\_SETRECT** message to make the formatting rectangle larger or smaller than the edit control window.</span></span>

<span data-ttu-id="fbb88-129">Se o controle de edição não tiver uma barra de rolagem horizontal e o retângulo de formatação for definido como maior que a janela de controle de edição, as linhas de texto que excedem a largura da janela de controle de edição (mas menor que a largura do retângulo de formatação) serão recortadas em vez de encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="fbb88-129">If the edit control does not have a horizontal scroll bar, and the formatting rectangle is set to be larger than the edit control window, lines of text exceeding the width of the edit control window (but smaller than the width of the formatting rectangle) are clipped instead of wrapped.</span></span>

<span data-ttu-id="fbb88-130">Se o controle de edição contiver uma borda, o retângulo de formatação será reduzido pelo tamanho da borda.</span><span class="sxs-lookup"><span data-stu-id="fbb88-130">If the edit control contains a border, the formatting rectangle is reduced by the size of the border.</span></span> <span data-ttu-id="fbb88-131">Se você estiver ajustando o retângulo retornado por uma mensagem em [**\_ GetRect**](em-getrect.md) , deverá remover o tamanho da borda antes de usar o retângulo com a mensagem de **\_ SetRect** .</span><span class="sxs-lookup"><span data-stu-id="fbb88-131">If you are adjusting the rectangle returned by an [**EM\_GETRECT**](em-getrect.md) message, you must remove the size of the border before using the rectangle with the **EM\_SETRECT** message.</span></span>

<span data-ttu-id="fbb88-132">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="fbb88-132">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="fbb88-133">O retângulo de formatação não inclui a barra de seleção, que é uma área desmarcada à esquerda de cada parágrafo.</span><span class="sxs-lookup"><span data-stu-id="fbb88-133">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="fbb88-134">Quando o usuário clica na barra de seleção, a linha correspondente é selecionada.</span><span class="sxs-lookup"><span data-stu-id="fbb88-134">When the user clicks in the selection bar, the corresponding line is selected.</span></span> <span data-ttu-id="fbb88-135">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="fbb88-135">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb88-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbb88-136">Requirements</span></span>



| <span data-ttu-id="fbb88-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbb88-137">Requirement</span></span> | <span data-ttu-id="fbb88-138">Valor</span><span class="sxs-lookup"><span data-stu-id="fbb88-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb88-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbb88-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb88-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbb88-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fbb88-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbb88-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb88-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fbb88-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fbb88-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbb88-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbb88-144"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbb88-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbb88-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fbb88-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="fbb88-146">**Referência**</span><span class="sxs-lookup"><span data-stu-id="fbb88-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fbb88-147">**em \_ GETrect**</span><span class="sxs-lookup"><span data-stu-id="fbb88-147">**EM\_GETRECT**</span></span>](em-getrect.md)
</dt> <dt>

[<span data-ttu-id="fbb88-148">**em \_ SETRECTNP**</span><span class="sxs-lookup"><span data-stu-id="fbb88-148">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="fbb88-149">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="fbb88-149">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="fbb88-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fbb88-150">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 


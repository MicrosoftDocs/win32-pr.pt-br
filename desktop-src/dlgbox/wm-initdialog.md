---
title: Mensagem de WM_INITDIALOG (WinUser. h)
description: Enviado para o procedimento da caixa de diálogo imediatamente antes de uma caixa de diálogo ser exibida. Os procedimentos da caixa de diálogo normalmente usam essa mensagem para inicializar controles e executar qualquer outra tarefa de inicialização que afete a aparência da caixa de diálogo.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- Caixas de diálogo de WM_INITDIALOG mensagem
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769649"
---
# <a name="wm_initdialog-message"></a><span data-ttu-id="7093d-105">Mensagem do WM \_ INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="7093d-105">WM\_INITDIALOG message</span></span>

<span data-ttu-id="7093d-106">Enviado para o procedimento da caixa de diálogo imediatamente antes de uma caixa de diálogo ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7093d-106">Sent to the dialog box procedure immediately before a dialog box is displayed.</span></span> <span data-ttu-id="7093d-107">Os procedimentos da caixa de diálogo normalmente usam essa mensagem para inicializar controles e executar qualquer outra tarefa de inicialização que afete a aparência da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7093d-107">Dialog box procedures typically use this message to initialize controls and carry out any other initialization tasks that affect the appearance of the dialog box.</span></span>


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a><span data-ttu-id="7093d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7093d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7093d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7093d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7093d-110">Um identificador para o controle para receber o foco padrão do teclado.</span><span class="sxs-lookup"><span data-stu-id="7093d-110">A handle to the control to receive the default keyboard focus.</span></span> <span data-ttu-id="7093d-111">O sistema atribuirá o foco padrão do teclado somente se o procedimento da caixa de diálogo retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="7093d-111">The system assigns the default keyboard focus only if the dialog box procedure returns **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="7093d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7093d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7093d-113">Dados de inicialização adicionais.</span><span class="sxs-lookup"><span data-stu-id="7093d-113">Additional initialization data.</span></span> <span data-ttu-id="7093d-114">Esses dados são passados para o sistema como o parâmetro *lParam* em uma chamada para a [**função CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)ou [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) usada para criar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7093d-114">This data is passed to the system as the *lParam* parameter in a call to the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), or [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) function used to create the dialog box.</span></span> <span data-ttu-id="7093d-115">Para folhas de propriedades, esse parâmetro é um ponteiro para a estrutura [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) usada para criar a página.</span><span class="sxs-lookup"><span data-stu-id="7093d-115">For property sheets, this parameter is a pointer to the [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) structure used to create the page.</span></span> <span data-ttu-id="7093d-116">Esse parâmetro será zero se qualquer outra função de criação de caixa de diálogo for usada.</span><span class="sxs-lookup"><span data-stu-id="7093d-116">This parameter is zero if any other dialog box creation function is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7093d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7093d-117">Return value</span></span>

<span data-ttu-id="7093d-118">O procedimento da caixa de diálogo deve retornar **true** para instruir o sistema a definir o foco do teclado para o controle especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="7093d-118">The dialog box procedure should return **TRUE** to direct the system to set the keyboard focus to the control specified by *wParam*.</span></span> <span data-ttu-id="7093d-119">Caso contrário, ele deve retornar **false** para impedir que o sistema defina o foco padrão do teclado.</span><span class="sxs-lookup"><span data-stu-id="7093d-119">Otherwise, it should return **FALSE** to prevent the system from setting the default keyboard focus.</span></span>

<span data-ttu-id="7093d-120">O procedimento da caixa de diálogo deve retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="7093d-120">The dialog box procedure should return the value directly.</span></span> <span data-ttu-id="7093d-121">O valor de **\_ MSGRESULT DWL** definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="7093d-121">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="7093d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7093d-122">Remarks</span></span>

<span data-ttu-id="7093d-123">O controle para receber o foco padrão do teclado é sempre o primeiro controle na caixa de diálogo que está visível, não desabilitado, e que tem o estilo **WS \_ TabStop** .</span><span class="sxs-lookup"><span data-stu-id="7093d-123">The control to receive the default keyboard focus is always the first control in the dialog box that is visible, not disabled, and that has the **WS\_TABSTOP** style.</span></span> <span data-ttu-id="7093d-124">Quando o procedimento da caixa de diálogo retorna **true**, o sistema verifica o controle para garantir que o procedimento não o tenha desabilitado.</span><span class="sxs-lookup"><span data-stu-id="7093d-124">When the dialog box procedure returns **TRUE**, the system checks the control to ensure that the procedure has not disabled it.</span></span> <span data-ttu-id="7093d-125">Se ele tiver sido desabilitado, o sistema definirá o foco do teclado para o próximo controle que está visível, não desabilitado e que tem o **WS \_ TabStop**.</span><span class="sxs-lookup"><span data-stu-id="7093d-125">If it has been disabled, the system sets the keyboard focus to the next control that is visible, not disabled, and has the **WS\_TABSTOP**.</span></span>

<span data-ttu-id="7093d-126">Um aplicativo pode retornar **false** somente se tiver definido o foco do teclado para um dos controles da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7093d-126">An application can return **FALSE** only if it has set the keyboard focus to one of the controls of the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7093d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7093d-127">Requirements</span></span>



| <span data-ttu-id="7093d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7093d-128">Requirement</span></span> | <span data-ttu-id="7093d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7093d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7093d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7093d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7093d-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7093d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7093d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7093d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7093d-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7093d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7093d-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7093d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7093d-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7093d-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7093d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="7093d-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="7093d-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7093d-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7093d-138">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="7093d-138">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="7093d-139">**CreateDialogParam**</span><span class="sxs-lookup"><span data-stu-id="7093d-139">**CreateDialogParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[<span data-ttu-id="7093d-140">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="7093d-140">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="7093d-141">**DialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="7093d-141">**DialogBoxParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[<span data-ttu-id="7093d-142">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="7093d-142">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="7093d-143">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="7093d-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7093d-144">Caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="7093d-144">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="7093d-145">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="7093d-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7093d-146">**PROPSHEETPAGE**</span><span class="sxs-lookup"><span data-stu-id="7093d-146">**PROPSHEETPAGE**</span></span>](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 


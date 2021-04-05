---
description: Define a fonte que um controle deve usar ao desenhar o texto.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: Mensagem de WM_SETFONT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fc334e6b8c937759555c471f00ec56254a629c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921791"
---
# <a name="wm_setfont-message"></a><span data-ttu-id="6115b-103">\_Mensagem de SETfont do WM</span><span class="sxs-lookup"><span data-stu-id="6115b-103">WM\_SETFONT message</span></span>

<span data-ttu-id="6115b-104">Define a fonte que um controle deve usar ao desenhar o texto.</span><span class="sxs-lookup"><span data-stu-id="6115b-104">Sets the font that a control is to use when drawing text.</span></span>


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a><span data-ttu-id="6115b-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6115b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6115b-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6115b-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6115b-107">Um identificador para a fonte (**HFONT**).</span><span class="sxs-lookup"><span data-stu-id="6115b-107">A handle to the font (**HFONT**).</span></span> <span data-ttu-id="6115b-108">Se esse parâmetro for **nulo**, o controle usará a fonte padrão do sistema para desenhar texto.</span><span class="sxs-lookup"><span data-stu-id="6115b-108">If this parameter is **NULL**, the control uses the default system font to draw text.</span></span>

</dd> <dt>

<span data-ttu-id="6115b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6115b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6115b-110">A palavra de ordem inferior de *lParam* especifica se o controle deve ser redesenhado imediatamente após a configuração da fonte.</span><span class="sxs-lookup"><span data-stu-id="6115b-110">The low-order word of *lParam* specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="6115b-111">Se esse parâmetro for **true**, o controle redesenhará a si mesmo.</span><span class="sxs-lookup"><span data-stu-id="6115b-111">If this parameter is **TRUE**, the control redraws itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6115b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6115b-112">Return value</span></span>

<span data-ttu-id="6115b-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6115b-113">Type: **LRESULT**</span></span>

<span data-ttu-id="6115b-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6115b-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6115b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6115b-115">Remarks</span></span>

<span data-ttu-id="6115b-116">A mensagem de **\_ fonte do WM** é aplicada a todos os controles, não apenas às caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6115b-116">The **WM\_SETFONT** message applies to all controls, not just those in dialog boxes.</span></span>

<span data-ttu-id="6115b-117">O melhor momento para o proprietário de um controle de caixa de diálogo definir a fonte do controle é quando ele recebe a [**mensagem \_ INITDIALOG do WM**](../dlgbox/wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="6115b-117">The best time for the owner of a dialog box control to set the font of the control is when it receives the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span> <span data-ttu-id="6115b-118">O aplicativo deve chamar a função [**ExcluirObjeto**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) para excluir a fonte quando ela não for mais necessária; por exemplo, depois de destruir o controle.</span><span class="sxs-lookup"><span data-stu-id="6115b-118">The application should call the [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) function to delete the font when it is no longer needed; for example, after it destroys the control.</span></span>

<span data-ttu-id="6115b-119">O tamanho do controle não é alterado como resultado da recepção desta mensagem.</span><span class="sxs-lookup"><span data-stu-id="6115b-119">The size of the control does not change as a result of receiving this message.</span></span> <span data-ttu-id="6115b-120">Para evitar o recorte de texto que não caiba nos limites do controle, o aplicativo deve corrigir o tamanho da janela de controle antes de definir a fonte.</span><span class="sxs-lookup"><span data-stu-id="6115b-120">To avoid clipping text that does not fit within the boundaries of the control, the application should correct the size of the control window before it sets the font.</span></span>

<span data-ttu-id="6115b-121">Quando uma caixa de diálogo usa o estilo de [ \_ fonte de domínio DS](../dlgbox/about-dialog-boxes.md) para definir o texto em seus controles, o sistema envia a mensagem do **WM \_ SetFont** para o procedimento da caixa de diálogo antes de criar os controles.</span><span class="sxs-lookup"><span data-stu-id="6115b-121">When a dialog box uses the [DS\_SETFONT](../dlgbox/about-dialog-boxes.md) style to set the text in its controls, the system sends the **WM\_SETFONT** message to the dialog box procedure before it creates the controls.</span></span> <span data-ttu-id="6115b-122">Um aplicativo pode criar uma caixa de diálogo que contém o \_ estilo de fonte DS chamando qualquer uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="6115b-122">An application can create a dialog box that contains the DS\_SETFONT style by calling any of the following functions:</span></span>

-   [<span data-ttu-id="6115b-123">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="6115b-123">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [<span data-ttu-id="6115b-124">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="6115b-124">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [<span data-ttu-id="6115b-125">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="6115b-125">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [<span data-ttu-id="6115b-126">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="6115b-126">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a><span data-ttu-id="6115b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6115b-127">Requirements</span></span>



| <span data-ttu-id="6115b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6115b-128">Requirement</span></span> | <span data-ttu-id="6115b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6115b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6115b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6115b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6115b-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6115b-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6115b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6115b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6115b-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6115b-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6115b-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6115b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6115b-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6115b-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6115b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="6115b-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="6115b-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6115b-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6115b-138">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="6115b-138">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="6115b-139">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="6115b-139">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="6115b-140">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="6115b-140">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="6115b-141">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="6115b-141">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="6115b-142">**DLGTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="6115b-142">**DLGTEMPLATE**</span></span>](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[<span data-ttu-id="6115b-143">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="6115b-143">**MAKELPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="6115b-144">**WM \_ GETfont**</span><span class="sxs-lookup"><span data-stu-id="6115b-144">**WM\_GETFONT**</span></span>](wm-getfont.md)
</dt> <dt>

[<span data-ttu-id="6115b-145">**INITDIALOG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6115b-145">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> <dt>

<span data-ttu-id="6115b-146">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6115b-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6115b-147">Windows</span><span class="sxs-lookup"><span data-stu-id="6115b-147">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="6115b-148">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="6115b-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6115b-149">**DeleteObject**</span><span class="sxs-lookup"><span data-stu-id="6115b-149">**DeleteObject**</span></span>](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 

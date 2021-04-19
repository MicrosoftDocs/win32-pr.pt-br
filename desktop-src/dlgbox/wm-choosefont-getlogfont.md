---
title: Mensagem de WM_CHOOSEFONT_GETLOGFONT (Commdlg. h)
description: Um aplicativo envia a \_ \_ mensagem GETLOGFONT do WM ChooseFont para uma caixa de diálogo fonte para recuperar informações sobre as seleções de fontes atuais do usuário.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- Caixas de diálogo de WM_CHOOSEFONT_GETLOGFONT mensagem
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764087"
---
# <a name="wm_choosefont_getlogfont-message"></a><span data-ttu-id="1ef3d-104">Mensagem de GETLOGFONT do WM \_ ChooseFont \_</span><span class="sxs-lookup"><span data-stu-id="1ef3d-104">WM\_CHOOSEFONT\_GETLOGFONT message</span></span>

<span data-ttu-id="1ef3d-105">Um aplicativo envia a **mensagem \_ \_ GETLOGFONT do WM ChooseFont** para uma caixa de diálogo **fonte** para recuperar informações sobre as seleções de fontes atuais do usuário.</span><span class="sxs-lookup"><span data-stu-id="1ef3d-105">An application sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to a **Font** dialog box to retrieve information about the user's current font selections.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a><span data-ttu-id="1ef3d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ef3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef3d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ef3d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ef3d-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="1ef3d-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ef3d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ef3d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ef3d-110">Um ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que recebe informações sobre as seleções de fonte atuais do usuário.</span><span class="sxs-lookup"><span data-stu-id="1ef3d-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the user's current font selections.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef3d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ef3d-111">Return value</span></span>

<span data-ttu-id="1ef3d-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1ef3d-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ef3d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ef3d-113">Remarks</span></span>

<span data-ttu-id="1ef3d-114">A função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) cria uma caixa de diálogo de **fonte** .</span><span class="sxs-lookup"><span data-stu-id="1ef3d-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box.</span></span> <span data-ttu-id="1ef3d-115">Quando o usuário fecha a caixa de diálogo **fonte** , a função **ChooseFont** retorna informações sobre as seleções de fontes do usuário na estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .</span><span class="sxs-lookup"><span data-stu-id="1ef3d-115">When the user closes the **Font** dialog box, the **ChooseFont** function returns information about the user's font selections in the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure.</span></span> <span data-ttu-id="1ef3d-116">O membro **lpLogFont** da estrutura **ChooseFont** é um ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="1ef3d-116">The **lpLogFont** member of the **CHOOSEFONT** structure is a pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

<span data-ttu-id="1ef3d-117">Use a **mensagem \_ \_ GETLOGFONT do WM ChooseFont** para obter informações sobre as seleções de fontes atuais do usuário enquanto a caixa de diálogo **fonte** está aberta.</span><span class="sxs-lookup"><span data-stu-id="1ef3d-117">Use the **WM\_CHOOSEFONT\_GETLOGFONT** message to get information about the user's current font selections while the **Font** dialog box is open.</span></span> <span data-ttu-id="1ef3d-118">Por exemplo, se você habilitar o botão **aplicar** na caixa de diálogo **fonte** , envie a mensagem para obter as informações de fonte a serem aplicadas à seleção de texto atual.</span><span class="sxs-lookup"><span data-stu-id="1ef3d-118">For example, if you enable the **Apply** button in the **Font** dialog box, send the message to get the font information to apply to the current text selection.</span></span>

<span data-ttu-id="1ef3d-119">Normalmente, você habilita um procedimento de gancho [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) para processar mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para o botão **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="1ef3d-119">Typically, you enable a [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure to process [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages for the **Apply** button.</span></span> <span data-ttu-id="1ef3d-120">Quando o usuário clica no botão **aplicar** , o procedimento de gancho envia a mensagem **GETLOGFONT do WM \_ ChooseFont \_** para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1ef3d-120">When the user clicks the **Apply** button, the hook procedure sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef3d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ef3d-121">Requirements</span></span>



| <span data-ttu-id="1ef3d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ef3d-122">Requirement</span></span> | <span data-ttu-id="1ef3d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1ef3d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef3d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ef3d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef3d-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ef3d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1ef3d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ef3d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef3d-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ef3d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ef3d-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1ef3d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ef3d-129"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ef3d-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ef3d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ef3d-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="1ef3d-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1ef3d-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1ef3d-132">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="1ef3d-132">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="1ef3d-133">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="1ef3d-133">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="1ef3d-134">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="1ef3d-134">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="1ef3d-135">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="1ef3d-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> <dt>

<span data-ttu-id="1ef3d-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="1ef3d-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1ef3d-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="1ef3d-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="1ef3d-138">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="1ef3d-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1ef3d-139">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="1ef3d-139">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 


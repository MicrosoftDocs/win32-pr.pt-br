---
title: Mensagem de WM_CHOOSEFONT_SETLOGFONT (Commdlg. h)
description: Um aplicativo envia a \_ mensagem SETLOGFONT do WM ChooseFont \_ para uma caixa de diálogo fonte para definir as informações da fonte lógica atual.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- Caixas de diálogo de WM_CHOOSEFONT_SETLOGFONT mensagem
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644920"
---
# <a name="wm_choosefont_setlogfont-message"></a><span data-ttu-id="6fbb4-104">Mensagem de SETLOGFONT do WM \_ ChooseFont \_</span><span class="sxs-lookup"><span data-stu-id="6fbb4-104">WM\_CHOOSEFONT\_SETLOGFONT message</span></span>

<span data-ttu-id="6fbb4-105">Um aplicativo envia a **mensagem \_ \_ SETLOGFONT do WM ChooseFont** para uma caixa de diálogo **fonte** para definir as informações da fonte lógica atual.</span><span class="sxs-lookup"><span data-stu-id="6fbb4-105">An application sends the **WM\_CHOOSEFONT\_SETLOGFONT** message to a **Font** dialog box to set the current logical font information.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a><span data-ttu-id="6fbb4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fbb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fbb4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6fbb4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fbb4-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6fbb4-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fbb4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fbb4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fbb4-110">Um ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contém informações sobre a fonte lógica atual.</span><span class="sxs-lookup"><span data-stu-id="6fbb4-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the current logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fbb4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fbb4-111">Return value</span></span>

<span data-ttu-id="6fbb4-112">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="6fbb4-112">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fbb4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fbb4-113">Remarks</span></span>

<span data-ttu-id="6fbb4-114">Ao chamar a função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para criar uma caixa de diálogo de **fonte** , você pode usar o membro **lpLogFont** da estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) contendo valores iniciais para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6fbb4-114">When you call the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to create a **Font** dialog box, you can use the **lpLogFont** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure containing initial values for the dialog box.</span></span> <span data-ttu-id="6fbb4-115">Use a **mensagem \_ \_ SETLOGFONT do WM ChooseFont** para especificar uma estrutura **LOGFONT** com valores diferentes, enquanto a caixa de diálogo **fonte** está aberta.</span><span class="sxs-lookup"><span data-stu-id="6fbb4-115">Use the **WM\_CHOOSEFONT\_SETLOGFONT** message to specify a **LOGFONT** structure with different values while the **Font** dialog box is open.</span></span>

<span data-ttu-id="6fbb4-116">Normalmente, você enviaria a mensagem de **\_ \_ SETLOGFONT do WM ChooseFont** de um procedimento de gancho de [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .</span><span class="sxs-lookup"><span data-stu-id="6fbb4-116">Typically, you would send the **WM\_CHOOSEFONT\_SETLOGFONT** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span> <span data-ttu-id="6fbb4-117">O procedimento de gancho também pode enviar as mensagens do [**WM \_ ChooseFont \_ GETLOGFONT**](wm-choosefont-getlogfont.md) e do [**WM \_ ChooseFont \_ SetFlags**](wm-choosefont-setflags.md) .</span><span class="sxs-lookup"><span data-stu-id="6fbb4-117">The hook procedure can also send the [**WM\_CHOOSEFONT\_GETLOGFONT**](wm-choosefont-getlogfont.md) and [**WM\_CHOOSEFONT\_SETFLAGS**](wm-choosefont-setflags.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fbb4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fbb4-118">Requirements</span></span>



| <span data-ttu-id="6fbb4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fbb4-119">Requirement</span></span> | <span data-ttu-id="6fbb4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6fbb4-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbb4-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fbb4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6fbb4-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fbb4-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6fbb4-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fbb4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6fbb4-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fbb4-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6fbb4-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6fbb4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fbb4-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fbb4-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fbb4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fbb4-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="6fbb4-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6fbb4-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6fbb4-129">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="6fbb4-129">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="6fbb4-130">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="6fbb4-130">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="6fbb4-131">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="6fbb4-131">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="6fbb4-132">**GETLOGFONT do WM \_ ChooseFont \_**</span><span class="sxs-lookup"><span data-stu-id="6fbb4-132">**WM\_CHOOSEFONT\_GETLOGFONT**</span></span>](wm-choosefont-getlogfont.md)
</dt> <dt>

[<span data-ttu-id="6fbb4-133">**ChooseFont do WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6fbb4-133">**WM\_CHOOSEFONT\_SETFLAGS**</span></span>](wm-choosefont-setflags.md)
</dt> <dt>

<span data-ttu-id="6fbb4-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6fbb4-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6fbb4-135">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="6fbb4-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="6fbb4-136">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="6fbb4-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6fbb4-137">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="6fbb4-137">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 


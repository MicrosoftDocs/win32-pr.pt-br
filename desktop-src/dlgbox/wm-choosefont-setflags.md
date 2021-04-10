---
title: Mensagem de WM_CHOOSEFONT_SETFLAGS (Commdlg. h)
description: Um aplicativo envia a mensagem do WM \_ ChooseFont \_ SetFlags para uma caixa de diálogo de fonte para definir as opções de exibição para a caixa de diálogo.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- Caixas de diálogo de WM_CHOOSEFONT_SETFLAGS mensagem
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085956"
---
# <a name="wm_choosefont_setflags-message"></a><span data-ttu-id="06c84-104">Mensagem do WM \_ ChooseFont \_ SetFlags</span><span class="sxs-lookup"><span data-stu-id="06c84-104">WM\_CHOOSEFONT\_SETFLAGS message</span></span>

<span data-ttu-id="06c84-105">Um aplicativo envia a mensagem do **WM \_ ChooseFont \_ SetFlags** para uma caixa de diálogo de **fonte** para definir as opções de exibição para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="06c84-105">An application sends the **WM\_CHOOSEFONT\_SETFLAGS** message to a **Font** dialog box to set the display options for the dialog box.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a><span data-ttu-id="06c84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06c84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06c84-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06c84-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="06c84-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06c84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06c84-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06c84-110">Um ponteiro para uma estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) que contém novas configurações no membro **flags** .</span><span class="sxs-lookup"><span data-stu-id="06c84-110">A pointer to a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure that contains new settings in the **Flags** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c84-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06c84-111">Return value</span></span>

<span data-ttu-id="06c84-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="06c84-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06c84-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="06c84-113">Remarks</span></span>

<span data-ttu-id="06c84-114">A função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) cria uma caixa de diálogo de **fonte** e usa uma estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar os valores iniciais para o membro **flags** .</span><span class="sxs-lookup"><span data-stu-id="06c84-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box and uses a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify the initial values for the **Flags** member.</span></span> <span data-ttu-id="06c84-115">Use a mensagem do **WM \_ ChooseFont \_ SetFlags** para especificar valores diferentes para o membro **flags** enquanto a caixa de diálogo **fonte** estiver aberta.</span><span class="sxs-lookup"><span data-stu-id="06c84-115">Use the **WM\_CHOOSEFONT\_SETFLAGS** message to specify different values for the **Flags** member while the **Font** dialog box is open.</span></span>

<span data-ttu-id="06c84-116">Normalmente, você deve enviar a mensagem do **WM \_ ChooseFont \_ SetFlags** de um procedimento de gancho de [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .</span><span class="sxs-lookup"><span data-stu-id="06c84-116">Typically, you should send the **WM\_CHOOSEFONT\_SETFLAGS** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c84-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06c84-117">Requirements</span></span>



| <span data-ttu-id="06c84-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c84-118">Requirement</span></span> | <span data-ttu-id="06c84-119">Valor</span><span class="sxs-lookup"><span data-stu-id="06c84-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c84-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06c84-120">Minimum supported client</span></span><br/> | <span data-ttu-id="06c84-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06c84-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="06c84-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06c84-122">Minimum supported server</span></span><br/> | <span data-ttu-id="06c84-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06c84-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="06c84-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="06c84-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c84-125"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06c84-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c84-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="06c84-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="06c84-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="06c84-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="06c84-128">**CFHookProc**</span><span class="sxs-lookup"><span data-stu-id="06c84-128">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="06c84-129">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="06c84-129">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="06c84-130">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="06c84-130">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

<span data-ttu-id="06c84-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="06c84-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="06c84-132">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="06c84-132">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


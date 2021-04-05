---
title: Mensagem de COLOROKSTRING (Commdlg. h)
description: Uma caixa de diálogo cor envia a mensagem registrada COLOROKSTRING para o procedimento de gancho, CCHookProc, quando o usuário seleciona uma cor e clica no botão OK.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Caixas de diálogo de mensagem COLOROKSTRING
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085545"
---
# <a name="colorokstring-message"></a><span data-ttu-id="c7e83-104">Mensagem COLOROKSTRING</span><span class="sxs-lookup"><span data-stu-id="c7e83-104">COLOROKSTRING message</span></span>

<span data-ttu-id="c7e83-105">Uma caixa de diálogo **cor** envia a mensagem registrada **COLOROKSTRING** para o procedimento de gancho, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), quando o usuário seleciona uma cor e clica no botão **OK** .</span><span class="sxs-lookup"><span data-stu-id="c7e83-105">A **Color** dialog box sends the **COLOROKSTRING** registered message to your hook procedure, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), when the user selects a color and clicks the **OK** button.</span></span> <span data-ttu-id="c7e83-106">O procedimento de gancho pode aceitar a cor e permitir que a caixa de diálogo seja fechada, ou rejeitar a cor e forçar a caixa de diálogo a permanecer aberta.</span><span class="sxs-lookup"><span data-stu-id="c7e83-106">The hook procedure can accept the color and allow the dialog box to close, or reject the color and force the dialog box to remain open.</span></span>


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a><span data-ttu-id="c7e83-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7e83-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e83-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7e83-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7e83-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="c7e83-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7e83-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7e83-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7e83-111">Um ponteiro para uma estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) .</span><span class="sxs-lookup"><span data-stu-id="c7e83-111">A pointer to a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure.</span></span> <span data-ttu-id="c7e83-112">O membro **rgbResult** dessa estrutura contém o valor de cor RGB da cor selecionada.</span><span class="sxs-lookup"><span data-stu-id="c7e83-112">The **rgbResult** member of this structure contains the RGB color value of the selected color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e83-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7e83-113">Return value</span></span>

<span data-ttu-id="c7e83-114">Se o procedimento de gancho retornar zero, a caixa de diálogo **cor** aceitará a cor selecionada e fechará.</span><span class="sxs-lookup"><span data-stu-id="c7e83-114">If the hook procedure returns zero, the **Color** dialog box accepts the selected color and closes.</span></span>

<span data-ttu-id="c7e83-115">Se o procedimento de gancho retornar um valor diferente de zero, a caixa de diálogo **cor** rejeitará a cor selecionada e permanecerá aberta.</span><span class="sxs-lookup"><span data-stu-id="c7e83-115">If the hook procedure returns a nonzero value, the **Color** dialog box rejects the selected color and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e83-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7e83-116">Remarks</span></span>

<span data-ttu-id="c7e83-117">O procedimento de gancho deve especificar a constante **COLOROKSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador da mensagem enviada pela caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7e83-117">The hook procedure must specify the **COLOROKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier of the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e83-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7e83-118">Requirements</span></span>



| <span data-ttu-id="c7e83-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7e83-119">Requirement</span></span> | <span data-ttu-id="c7e83-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c7e83-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e83-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7e83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e83-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7e83-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c7e83-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7e83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e83-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7e83-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7e83-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c7e83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7e83-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7e83-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c7e83-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c7e83-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c7e83-128">**COLOROKSTRINGW** (Unicode) e **COLOROKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c7e83-128">**COLOROKSTRINGW** (Unicode) and **COLOROKSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="c7e83-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7e83-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7e83-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c7e83-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c7e83-131">**CHOOSECOLOR**</span><span class="sxs-lookup"><span data-stu-id="c7e83-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="c7e83-132">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="c7e83-132">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="c7e83-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c7e83-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7e83-134">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="c7e83-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


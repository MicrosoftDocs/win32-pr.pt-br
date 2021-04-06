---
title: Mensagem de HELPMSGSTRING (Commdlg. h)
description: Uma caixa de diálogo comum envia a mensagem registrada HELPMSGSTRING para o procedimento de janela de sua janela do proprietário quando o usuário clica no botão ajuda.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Caixas de diálogo de mensagem HELPMSGSTRING
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3f7a883f50b06c8d142cb83bedf0bfa2920191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086333"
---
# <a name="helpmsgstring-message"></a><span data-ttu-id="c17c6-104">Mensagem HELPMSGSTRING</span><span class="sxs-lookup"><span data-stu-id="c17c6-104">HELPMSGSTRING message</span></span>

<span data-ttu-id="c17c6-105">Uma caixa de diálogo comum envia a mensagem registrada **HELPMSGSTRING** para o procedimento de janela de sua janela do proprietário quando o usuário clica no botão **ajuda** .</span><span class="sxs-lookup"><span data-stu-id="c17c6-105">A common dialog box sends the **HELPMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Help** button.</span></span>


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a><span data-ttu-id="c17c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c17c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c17c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c17c6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c17c6-108">Um identificador para a caixa de diálogo comum.</span><span class="sxs-lookup"><span data-stu-id="c17c6-108">A handle to the common dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="c17c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c17c6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c17c6-110">Um ponteiro para a estrutura de inicialização da caixa de diálogo comum.</span><span class="sxs-lookup"><span data-stu-id="c17c6-110">A pointer to the initialization structure for the common dialog box.</span></span> <span data-ttu-id="c17c6-111">Essa estrutura pode ser uma estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) ou [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .</span><span class="sxs-lookup"><span data-stu-id="c17c6-111">This structure can be a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) or [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c17c6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c17c6-112">Return value</span></span>

<span data-ttu-id="c17c6-113">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="c17c6-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c17c6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c17c6-114">Remarks</span></span>

<span data-ttu-id="c17c6-115">Você deve especificar a constante **HELPMSGSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c17c6-115">You must specify the **HELPMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="c17c6-116">Quando você criar a caixa de diálogo, use o membro **hwndOwner** da estrutura de inicialização para identificar a janela para receber mensagens **HELPMSGSTRING** .</span><span class="sxs-lookup"><span data-stu-id="c17c6-116">When you create the dialog box, use the **hwndOwner** member of the initialization structure to identify the window to receive **HELPMSGSTRING** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="c17c6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c17c6-117">Requirements</span></span>



| <span data-ttu-id="c17c6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c17c6-118">Requirement</span></span> | <span data-ttu-id="c17c6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c17c6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c17c6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c17c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c17c6-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c17c6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c17c6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c17c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c17c6-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c17c6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c17c6-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c17c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c17c6-125"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c17c6-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c17c6-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c17c6-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c17c6-127">**HELPMSGSTRINGW** (Unicode) e **HELPMSGSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c17c6-127">**HELPMSGSTRINGW** (Unicode) and **HELPMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="c17c6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c17c6-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c17c6-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c17c6-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c17c6-130">**ajuda da CDN \_**</span><span class="sxs-lookup"><span data-stu-id="c17c6-130">**CDN\_HELP**</span></span>](cdn-help.md)
</dt> <dt>

[<span data-ttu-id="c17c6-131">**CHOOSECOLOR**</span><span class="sxs-lookup"><span data-stu-id="c17c6-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="c17c6-132">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="c17c6-132">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="c17c6-133">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="c17c6-133">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="c17c6-134">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="c17c6-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="c17c6-135">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="c17c6-135">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[<span data-ttu-id="c17c6-136">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="c17c6-136">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="c17c6-137">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="c17c6-137">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="c17c6-138">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c17c6-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c17c6-139">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="c17c6-139">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


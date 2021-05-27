---
title: Mensagem de SHAREVISTRING (Commdlg. h)
description: Uma caixa de diálogo abrir ou salvar como envia a mensagem registrada SHAREVISTRING para o procedimento de gancho, OFNHookProc, se ocorrer uma violação de compartilhamento para o arquivo selecionado quando o usuário clicar no botão OK.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Caixas de diálogo de mensagem SHAREVISTRING
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043bed9edd08269e4e030482cbd44debea3a3695
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548761"
---
# <a name="sharevistring-message"></a><span data-ttu-id="12260-104">Mensagem SHAREVISTRING</span><span class="sxs-lookup"><span data-stu-id="12260-104">SHAREVISTRING message</span></span>

<span data-ttu-id="12260-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="12260-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="12260-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="12260-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="12260-107">Uma caixa de diálogo **abrir** ou **salvar como** envia a mensagem registrada **SHAREVISTRING** para o procedimento de gancho, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), se ocorrer uma violação de compartilhamento para o arquivo selecionado quando o usuário clicar no botão **OK** .</span><span class="sxs-lookup"><span data-stu-id="12260-107">An **Open** or **Save As** dialog box sends the **SHAREVISTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), if a sharing violation occurs for the selected file when the user clicks the **OK** button.</span></span>


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a><span data-ttu-id="12260-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12260-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12260-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12260-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12260-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="12260-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="12260-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12260-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12260-112">Um ponteiro para uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="12260-112">A pointer to a [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="12260-113">O membro **lpstrFile** dessa estrutura contém o nome do arquivo que causou a violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="12260-113">The **lpstrFile** member of this structure contains the file name that caused the sharing violation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12260-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12260-114">Return value</span></span>

<span data-ttu-id="12260-115">O procedimento de gancho deve retornar um dos valores a seguir para indicar como a caixa de diálogo deve tratar a violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="12260-115">The hook procedure must return one of the following values to indicate how the dialog box should handle the sharing violation.</span></span>



| <span data-ttu-id="12260-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="12260-116">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="12260-117">Description</span><span class="sxs-lookup"><span data-stu-id="12260-117">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12260-118"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="12260-118"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="12260-119">Aceitar o nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="12260-119">Accept the file name</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="12260-120"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="12260-120"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="12260-121">Rejeite o nome do arquivo, mas não avise o usuário.</span><span class="sxs-lookup"><span data-stu-id="12260-121">Reject the file name but do not warn the user.</span></span> <span data-ttu-id="12260-122">O aplicativo é responsável por exibir uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="12260-122">The application is responsible for displaying a warning message.</span></span><br/> |
| <dl> <span data-ttu-id="12260-123"><dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="12260-123"><dt>**OFN\_SHAREWARN**</dt> <dt>0</dt></span></span> </dl>        | <span data-ttu-id="12260-124">Rejeite o nome do arquivo e exibe uma mensagem de aviso (o mesmo resultado que se não houvesse nenhum procedimento de gancho).</span><span class="sxs-lookup"><span data-stu-id="12260-124">Reject the file name and displays a warning message (the same result as if there were no hook procedure).</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="12260-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="12260-125">Remarks</span></span>

<span data-ttu-id="12260-126">O procedimento de gancho deve especificar a constante **SHAREVISTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="12260-126">The hook procedure must specify the **SHAREVISTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="12260-127">A caixa de diálogo enviará a mensagem registrada **SHAREVISTRING** somente se você não tiver especificado o sinalizador **OFN \_ SHAREAWARE** no membro **flags** da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quando criou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="12260-127">The dialog box sends the **SHAREVISTRING** registered message only if you did not specify the **OFN\_SHAREAWARE** flag in the **Flags** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure when you created the dialog.</span></span>

<span data-ttu-id="12260-128">Se o procedimento de gancho retornar um valor indefinido, a caixa de diálogo responderá como se **OFN \_ SHAREWARN** tivesse sido retornado.</span><span class="sxs-lookup"><span data-stu-id="12260-128">If the hook procedure returns an undefined value, the dialog box responds as if **OFN\_SHAREWARN** was returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="12260-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12260-129">Requirements</span></span>



| <span data-ttu-id="12260-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="12260-130">Requirement</span></span> | <span data-ttu-id="12260-131">Valor</span><span class="sxs-lookup"><span data-stu-id="12260-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12260-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12260-132">Minimum supported client</span></span><br/> | <span data-ttu-id="12260-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="12260-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="12260-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12260-134">Minimum supported server</span></span><br/> | <span data-ttu-id="12260-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="12260-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="12260-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="12260-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="12260-137"><dt>Commdlg.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="12260-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="12260-138">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="12260-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="12260-139">**SHAREVISTRINGW** (Unicode) e **SHAREVISTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="12260-139">**SHAREVISTRINGW** (Unicode) and **SHAREVISTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="12260-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="12260-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="12260-141">**Referência**</span><span class="sxs-lookup"><span data-stu-id="12260-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="12260-142">**COMPARTILHAMENTO \_ DE CDNVIOLATION**</span><span class="sxs-lookup"><span data-stu-id="12260-142">**CDN\_SHAREVIOLATION**</span></span>](cdn-shareviolation.md)
</dt> <dt>

[<span data-ttu-id="12260-143">**Openfilename**</span><span class="sxs-lookup"><span data-stu-id="12260-143">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="12260-144">**Registerwindowmessage**</span><span class="sxs-lookup"><span data-stu-id="12260-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="12260-145">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="12260-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="12260-146">Biblioteca de caixas de diálogo comuns</span><span class="sxs-lookup"><span data-stu-id="12260-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>


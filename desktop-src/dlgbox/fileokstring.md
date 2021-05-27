---
title: Mensagem FILEOKSTRING (Commdlg.h)
description: Uma caixa de diálogo Abrir ou Salvar como envia a mensagem registrada FILEOKSTRING para o procedimento de gancho, OFNHookProc, quando o usuário especifica um nome de arquivo e clica no botão OK.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Caixas de diálogo da mensagem FILEOKSTRING
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24dd07faecc66bc50c408eab36bcbd8c93c460ef
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549211"
---
# <a name="fileokstring-message"></a><span data-ttu-id="7d68b-104">Mensagem FILEOKSTRING</span><span class="sxs-lookup"><span data-stu-id="7d68b-104">FILEOKSTRING message</span></span>

<span data-ttu-id="7d68b-105">\[Começando com o Windows Vista, as **caixas** de **diálogo** Abrir e Salvar como comuns foram superadas pela caixa de diálogo Item [Comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="7d68b-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="7d68b-106">Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]</span><span class="sxs-lookup"><span data-stu-id="7d68b-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="7d68b-107">Uma **caixa** de diálogo Abrir ou Salvar **como** envia a mensagem registrada **FILEOKSTRING** para o procedimento de [*gancho, OFNHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)quando o usuário especifica um nome de arquivo e clica no **botão OK.**</span><span class="sxs-lookup"><span data-stu-id="7d68b-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="7d68b-108">O procedimento de gancho pode aceitar o nome do arquivo e permitir que a caixa de diálogo feche ou rejeite o nome do arquivo e force a caixa de diálogo a permanecer aberta.</span><span class="sxs-lookup"><span data-stu-id="7d68b-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="7d68b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d68b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d68b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d68b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d68b-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="7d68b-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d68b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d68b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d68b-113">Um ponteiro para uma [**estrutura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)</span><span class="sxs-lookup"><span data-stu-id="7d68b-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="7d68b-114">O **membro lpstrFile** dessa estrutura contém a unidade, o caminho e o nome do arquivo especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7d68b-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d68b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d68b-115">Return value</span></span>

<span data-ttu-id="7d68b-116">Se o procedimento de gancho retornar zero, a caixa de diálogo **Abrir** ou Salvar **como** aceitará o nome de arquivo especificado e fechará.</span><span class="sxs-lookup"><span data-stu-id="7d68b-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="7d68b-117">Se o procedimento de gancho retornar  um valor diferente de zero, a caixa de diálogo Abrir ou Salvar **como** rejeitará o nome de arquivo especificado e permanecerá aberta.</span><span class="sxs-lookup"><span data-stu-id="7d68b-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d68b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d68b-118">Remarks</span></span>

<span data-ttu-id="7d68b-119">O procedimento de gancho deve especificar a constante **FILEOKSTRING** em uma chamada para a [**função RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador da mensagem enviada pela caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7d68b-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d68b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d68b-120">Requirements</span></span>



| <span data-ttu-id="7d68b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d68b-121">Requirement</span></span> | <span data-ttu-id="7d68b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7d68b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d68b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d68b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7d68b-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d68b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7d68b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d68b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7d68b-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7d68b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7d68b-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7d68b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d68b-128"><dt>Commdlg.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d68b-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7d68b-129">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7d68b-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7d68b-130">**FILEOKSTRINGW** (Unicode) e **FILEOKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7d68b-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="7d68b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d68b-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d68b-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7d68b-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7d68b-133">**CDN \_ FILEOK**</span><span class="sxs-lookup"><span data-stu-id="7d68b-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="7d68b-134">**Openfilename**</span><span class="sxs-lookup"><span data-stu-id="7d68b-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="7d68b-135">**Registerwindowmessage**</span><span class="sxs-lookup"><span data-stu-id="7d68b-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="7d68b-136">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="7d68b-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7d68b-137">Biblioteca de caixas de diálogo comuns</span><span class="sxs-lookup"><span data-stu-id="7d68b-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>


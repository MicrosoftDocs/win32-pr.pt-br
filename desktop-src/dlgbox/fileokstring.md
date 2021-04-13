---
title: Mensagem de FILEOKSTRING (Commdlg. h)
description: Uma caixa de diálogo abrir ou salvar como envia a mensagem registrada FILEOKSTRING para o procedimento de gancho, OFNHookProc, quando o usuário especifica um nome de arquivo e clica no botão OK.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Caixas de diálogo de mensagem FILEOKSTRING
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
ms.openlocfilehash: 61208ddebc63f1186c2947416e451231f0bea24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455901"
---
# <a name="fileokstring-message"></a><span data-ttu-id="069a0-104">Mensagem FILEOKSTRING</span><span class="sxs-lookup"><span data-stu-id="069a0-104">FILEOKSTRING message</span></span>

<span data-ttu-id="069a0-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="069a0-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="069a0-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="069a0-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="069a0-107">Uma caixa de diálogo **abrir** ou **salvar como** envia a mensagem registrada **FILEOKSTRING** para o procedimento de gancho, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), quando o usuário especifica um nome de arquivo e clica no botão **OK** .</span><span class="sxs-lookup"><span data-stu-id="069a0-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="069a0-108">O procedimento de gancho pode aceitar o nome do arquivo e permitir que a caixa de diálogo seja fechada ou rejeitar o nome do arquivo e forçar a caixa de diálogo a permanecer aberta.</span><span class="sxs-lookup"><span data-stu-id="069a0-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="069a0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="069a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="069a0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="069a0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="069a0-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="069a0-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="069a0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="069a0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="069a0-113">Um ponteiro para uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="069a0-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="069a0-114">O membro **lpstrFile** dessa estrutura contém a unidade, o caminho e o nome de arquivo especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="069a0-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="069a0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="069a0-115">Return value</span></span>

<span data-ttu-id="069a0-116">Se o procedimento de gancho retornar zero, a caixa de diálogo **abrir** ou **salvar como** aceitará o nome de arquivo especificado e fechará.</span><span class="sxs-lookup"><span data-stu-id="069a0-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="069a0-117">Se o procedimento de gancho retornar um valor diferente de zero, a caixa de diálogo **abrir** ou **salvar como** rejeitará o nome de arquivo especificado e permanecerá aberto.</span><span class="sxs-lookup"><span data-stu-id="069a0-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="069a0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="069a0-118">Remarks</span></span>

<span data-ttu-id="069a0-119">O procedimento de gancho deve especificar a constante **FILEOKSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="069a0-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="069a0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="069a0-120">Requirements</span></span>



| <span data-ttu-id="069a0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="069a0-121">Requirement</span></span> | <span data-ttu-id="069a0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="069a0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="069a0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="069a0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="069a0-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="069a0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="069a0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="069a0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="069a0-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="069a0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="069a0-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="069a0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="069a0-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="069a0-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="069a0-129">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="069a0-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="069a0-130">**FILEOKSTRINGW** (Unicode) e **FILEOKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="069a0-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="069a0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="069a0-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="069a0-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="069a0-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="069a0-133">**\_FILEOK CDN**</span><span class="sxs-lookup"><span data-stu-id="069a0-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="069a0-134">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="069a0-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="069a0-135">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="069a0-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="069a0-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="069a0-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="069a0-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="069a0-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


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
ms.openlocfilehash: a6fddbb3460f15e1efb946b9bd17f1c85fd031a8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590783"
---
# <a name="fileokstring-message"></a><span data-ttu-id="611f5-104">Mensagem FILEOKSTRING</span><span class="sxs-lookup"><span data-stu-id="611f5-104">FILEOKSTRING message</span></span>

<span data-ttu-id="611f5-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="611f5-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="611f5-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="611f5-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="611f5-107">Uma caixa de diálogo **abrir** ou **salvar como** envia a mensagem registrada **FILEOKSTRING** para o procedimento de gancho, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), quando o usuário especifica um nome de arquivo e clica no botão **OK** .</span><span class="sxs-lookup"><span data-stu-id="611f5-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="611f5-108">O procedimento de gancho pode aceitar o nome do arquivo e permitir que a caixa de diálogo seja fechada ou rejeitar o nome do arquivo e forçar a caixa de diálogo a permanecer aberta.</span><span class="sxs-lookup"><span data-stu-id="611f5-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="611f5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="611f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="611f5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="611f5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="611f5-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="611f5-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="611f5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="611f5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="611f5-113">Um ponteiro para uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="611f5-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="611f5-114">O membro **lpstrFile** dessa estrutura contém a unidade, o caminho e o nome de arquivo especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="611f5-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="611f5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="611f5-115">Return value</span></span>

<span data-ttu-id="611f5-116">Se o procedimento de gancho retornar zero, a caixa de diálogo **abrir** ou **salvar como** aceitará o nome de arquivo especificado e fechará.</span><span class="sxs-lookup"><span data-stu-id="611f5-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="611f5-117">Se o procedimento de gancho retornar um valor diferente de zero, a caixa de diálogo **abrir** ou **salvar como** rejeitará o nome de arquivo especificado e permanecerá aberto.</span><span class="sxs-lookup"><span data-stu-id="611f5-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="611f5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="611f5-118">Remarks</span></span>

<span data-ttu-id="611f5-119">O procedimento de gancho deve especificar a constante **FILEOKSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="611f5-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="611f5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="611f5-120">Requirements</span></span>



| <span data-ttu-id="611f5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="611f5-121">Requirement</span></span> | <span data-ttu-id="611f5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="611f5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611f5-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="611f5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="611f5-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="611f5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="611f5-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="611f5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="611f5-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="611f5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="611f5-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="611f5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="611f5-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="611f5-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="611f5-129">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="611f5-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="611f5-130">**FILEOKSTRINGW** (Unicode) e **FILEOKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="611f5-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="611f5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="611f5-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="611f5-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="611f5-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="611f5-133">**\_FILEOK CDN**</span><span class="sxs-lookup"><span data-stu-id="611f5-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="611f5-134">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="611f5-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="611f5-135">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="611f5-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="611f5-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="611f5-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="611f5-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="611f5-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


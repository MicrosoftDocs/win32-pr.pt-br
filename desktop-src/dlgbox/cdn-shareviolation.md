---
title: CDN_SHAREVIOLATION código de notificação (Commdlg. h)
description: Enviado por uma caixa de diálogo abrir no estilo do Explorer ou salvar como quando o usuário clica no botão OK e ocorre uma violação de compartilhamento de rede para o arquivo selecionado.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- Caixas de diálogo CDN_SHAREVIOLATION código de notificação
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e79d9c48d3e80d14d83de07c03f7db119ea8e78
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590693"
---
# <a name="cdn_shareviolation-notification-code"></a><span data-ttu-id="1bac8-104">Código de notificação da CDN \_ SHAREVIOLATION</span><span class="sxs-lookup"><span data-stu-id="1bac8-104">CDN\_SHAREVIOLATION notification code</span></span>

<span data-ttu-id="1bac8-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="1bac8-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="1bac8-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="1bac8-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="1bac8-107">Enviado por uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** quando o usuário clica no botão **OK** e ocorre uma violação de compartilhamento de rede para o arquivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="1bac8-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **OK** button and a network sharing violation occurs for the selected file.</span></span>

<span data-ttu-id="1bac8-108">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1bac8-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="1bac8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bac8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bac8-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1bac8-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bac8-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="1bac8-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bac8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1bac8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bac8-113">Um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="1bac8-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="1bac8-114">O membro **pszFile** dessa estrutura é um ponteiro para o nome do arquivo que tinha a violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1bac8-114">The **pszFile** member of this structure is a pointer to the name of the file that had the sharing violation.</span></span> <span data-ttu-id="1bac8-115">A estrutura **OFNOTIFY** contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação **CDN \_ SHAREVIOLATION** .</span><span class="sxs-lookup"><span data-stu-id="1bac8-115">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SHAREVIOLATION** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bac8-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1bac8-116">Return value</span></span>

<span data-ttu-id="1bac8-117">O valor de retorno indica como a caixa de diálogo deve tratar a violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1bac8-117">The return value indicates how the dialog box should handle the sharing violation.</span></span>

<span data-ttu-id="1bac8-118">Se o procedimento de gancho retornar zero, a caixa de diálogo exibirá a mensagem de aviso padrão para uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1bac8-118">If the hook procedure returns zero, the dialog box displays the standard warning message for a sharing violation.</span></span>

<span data-ttu-id="1bac8-119">Para evitar a exibição da mensagem de aviso padrão, retorne um valor diferente de zero do procedimento de gancho e chame a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para definir um dos seguintes valores de **DWL \_ MSGRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1bac8-119">To prevent the display of the standard warning message, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set one of the following **DWL\_MSGRESULT** values.</span></span>



| <span data-ttu-id="1bac8-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1bac8-120">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="1bac8-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bac8-121">Description</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1bac8-122"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1bac8-122"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="1bac8-123">Faz com que a caixa de diálogo retorne o nome do arquivo sem avisar o usuário sobre a violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1bac8-123">Causes the dialog box to return the file name without warning the user about the sharing violation.</span></span><br/>  |
| <dl> <span data-ttu-id="1bac8-124"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1bac8-124"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="1bac8-125">Faz com que a caixa de diálogo rejeite o nome do arquivo sem avisar o usuário sobre a violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1bac8-125">Causes the dialog box to reject the file name without warning the user about the sharing violation.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="1bac8-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bac8-126">Remarks</span></span>

<span data-ttu-id="1bac8-127">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o valor do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="1bac8-127">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="1bac8-128">O sistema enviará essa notificação somente se o valor de **\_ SHAREAWARE OFN** não tiver sido especificado quando a caixa de diálogo foi criada.</span><span class="sxs-lookup"><span data-stu-id="1bac8-128">The system sends this notification only if the **OFN\_SHAREAWARE** value was not specified when the dialog box was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bac8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bac8-129">Requirements</span></span>



| <span data-ttu-id="1bac8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bac8-130">Requirement</span></span> | <span data-ttu-id="1bac8-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1bac8-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bac8-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bac8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1bac8-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1bac8-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1bac8-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bac8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1bac8-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1bac8-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1bac8-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1bac8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bac8-137"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bac8-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bac8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bac8-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="1bac8-139">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1bac8-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1bac8-140">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="1bac8-140">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="1bac8-141">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="1bac8-141">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="1bac8-142">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="1bac8-142">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="1bac8-143">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="1bac8-143">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="1bac8-144">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="1bac8-144">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="1bac8-145">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="1bac8-145">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="1bac8-146">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="1bac8-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1bac8-147">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="1bac8-147">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


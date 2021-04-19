---
title: CDN_FOLDERCHANGE código de notificação (Commdlg. h)
description: Enviado por uma caixa de diálogo abrir no estilo do Explorer ou salvar como quando uma nova pasta é aberta.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- Caixas de diálogo CDN_FOLDERCHANGE código de notificação
topic_type:
- apiref
api_name:
- CDN_FOLDERCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39075bddbd191f60a9f9bcbad745e213fe9a978
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590863"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="d09a3-104">Código de notificação da CDN \_ FOLDERCHANGE</span><span class="sxs-lookup"><span data-stu-id="d09a3-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="d09a3-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="d09a3-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="d09a3-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="d09a3-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="d09a3-107">Enviado por uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** quando uma nova pasta é aberta.</span><span class="sxs-lookup"><span data-stu-id="d09a3-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="d09a3-108">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d09a3-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="d09a3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d09a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d09a3-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d09a3-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d09a3-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="d09a3-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d09a3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d09a3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d09a3-113">Um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="d09a3-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="d09a3-114">A estrutura **OFNOTIFY** contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação **CDN \_ FOLDERCHANGE** .</span><span class="sxs-lookup"><span data-stu-id="d09a3-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d09a3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d09a3-115">Return value</span></span>

<span data-ttu-id="d09a3-116">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="d09a3-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="d09a3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d09a3-117">Remarks</span></span>

<span data-ttu-id="d09a3-118">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o valor do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="d09a3-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="d09a3-119">Para obter o caminho da pasta aberta recentemente, o procedimento de gancho pode enviar a mensagem [**CDM \_ GetFolderPath**](cdm-getfolderpath.md) para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d09a3-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="d09a3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d09a3-120">Requirements</span></span>



| <span data-ttu-id="d09a3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d09a3-121">Requirement</span></span> | <span data-ttu-id="d09a3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d09a3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d09a3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d09a3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d09a3-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d09a3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d09a3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d09a3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d09a3-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d09a3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d09a3-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d09a3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d09a3-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d09a3-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09a3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d09a3-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d09a3-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d09a3-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d09a3-131">**CDM \_ GETfolderpath**</span><span class="sxs-lookup"><span data-stu-id="d09a3-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="d09a3-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="d09a3-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="d09a3-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="d09a3-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="d09a3-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="d09a3-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="d09a3-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="d09a3-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="d09a3-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="d09a3-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d09a3-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="d09a3-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


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
ms.openlocfilehash: 4c93bd37afa44e7fc5ca81d928974f56bf80d1b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085644"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="4331e-104">Código de notificação da CDN \_ FOLDERCHANGE</span><span class="sxs-lookup"><span data-stu-id="4331e-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="4331e-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4331e-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="4331e-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="4331e-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="4331e-107">Enviado por uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** quando uma nova pasta é aberta.</span><span class="sxs-lookup"><span data-stu-id="4331e-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="4331e-108">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4331e-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="4331e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4331e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4331e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4331e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4331e-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="4331e-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4331e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4331e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4331e-113">Um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="4331e-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="4331e-114">A estrutura **OFNOTIFY** contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação **CDN \_ FOLDERCHANGE** .</span><span class="sxs-lookup"><span data-stu-id="4331e-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4331e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4331e-115">Return value</span></span>

<span data-ttu-id="4331e-116">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="4331e-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="4331e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4331e-117">Remarks</span></span>

<span data-ttu-id="4331e-118">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o valor do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="4331e-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="4331e-119">Para obter o caminho da pasta aberta recentemente, o procedimento de gancho pode enviar a mensagem [**CDM \_ GetFolderPath**](cdm-getfolderpath.md) para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4331e-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="4331e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4331e-120">Requirements</span></span>



| <span data-ttu-id="4331e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4331e-121">Requirement</span></span> | <span data-ttu-id="4331e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4331e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4331e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4331e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4331e-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4331e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4331e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4331e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4331e-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4331e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4331e-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4331e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4331e-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4331e-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4331e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4331e-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="4331e-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4331e-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4331e-131">**CDM \_ GETfolderpath**</span><span class="sxs-lookup"><span data-stu-id="4331e-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="4331e-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="4331e-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="4331e-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="4331e-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="4331e-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="4331e-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="4331e-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="4331e-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="4331e-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="4331e-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4331e-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="4331e-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


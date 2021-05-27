---
title: CDN_HELP código de notificação (Commdlg. h)
description: Enviado por uma caixa de diálogo abrir no estilo do Explorer ou salvar como quando o usuário clica no botão ajuda.
ms.assetid: 18ee86b2-3446-4de4-a47a-2e44e677f4f7
keywords:
- Caixas de diálogo CDN_HELP código de notificação
topic_type:
- apiref
api_name:
- CDN_HELP
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abd3519bdc877eca24304b1104a12d51b2dfe4f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550061"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="538f2-104">Código de notificação da ajuda da CDN \_</span><span class="sxs-lookup"><span data-stu-id="538f2-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="538f2-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="538f2-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="538f2-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="538f2-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="538f2-107">Enviado por uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** quando o usuário clica no botão **ajuda** .</span><span class="sxs-lookup"><span data-stu-id="538f2-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="538f2-108">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="538f2-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="538f2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="538f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="538f2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="538f2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="538f2-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="538f2-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="538f2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="538f2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="538f2-113">Um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="538f2-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="538f2-114">A estrutura **OFNOTIFY** contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação da **\_ ajuda da CDN** .</span><span class="sxs-lookup"><span data-stu-id="538f2-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="538f2-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="538f2-115">Return value</span></span>

<span data-ttu-id="538f2-116">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="538f2-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="538f2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="538f2-117">Remarks</span></span>

<span data-ttu-id="538f2-118">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o valor do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="538f2-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="538f2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="538f2-119">Requirements</span></span>



| <span data-ttu-id="538f2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="538f2-120">Requirement</span></span> | <span data-ttu-id="538f2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="538f2-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="538f2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="538f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="538f2-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="538f2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="538f2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="538f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="538f2-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="538f2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="538f2-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="538f2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="538f2-127"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="538f2-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="538f2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="538f2-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="538f2-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="538f2-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="538f2-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="538f2-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="538f2-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="538f2-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="538f2-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="538f2-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="538f2-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="538f2-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="538f2-134">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="538f2-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="538f2-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="538f2-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="538f2-136">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="538f2-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>


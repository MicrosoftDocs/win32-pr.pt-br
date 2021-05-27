---
title: CDN_FOLDERCHANGE de notificação (Commdlg.h)
description: Enviado por uma caixa de diálogo Abrir ou Salvar como no estilo Explorer quando uma nova pasta é aberta.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- CDN_FOLDERCHANGE de diálogo de código de notificação
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
ms.openlocfilehash: 318aa2ffe4ddd47bcb1472f412f85ab785c5049e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550071"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="48929-104">Código de \_ notificação CDN FOLDERCHANGE</span><span class="sxs-lookup"><span data-stu-id="48929-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="48929-105">\[Começando com o Windows Vista, as **caixas** de **diálogo** Abrir e Salvar como comuns foram superadas pela caixa de diálogo Item [Comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="48929-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="48929-106">Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]</span><span class="sxs-lookup"><span data-stu-id="48929-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="48929-107">Enviado por uma caixa de diálogo **Abrir** ou Salvar **como** no estilo Explorer quando uma nova pasta é aberta.</span><span class="sxs-lookup"><span data-stu-id="48929-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="48929-108">O [*procedimento de gancho OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="48929-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="48929-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48929-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48929-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48929-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48929-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="48929-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="48929-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48929-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48929-113">Um ponteiro para uma [**estrutura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="48929-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="48929-114">A **estrutura OFNOTIFY** contém uma [**estrutura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cujo** membro de código indica a mensagem de notificação **CDN \_ FOLDERCHANGE.**</span><span class="sxs-lookup"><span data-stu-id="48929-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48929-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48929-115">Return value</span></span>

<span data-ttu-id="48929-116">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="48929-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="48929-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="48929-117">Remarks</span></span>

<span data-ttu-id="48929-118">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="48929-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="48929-119">Para obter o caminho da pasta recém-aberta, o procedimento de gancho pode enviar a mensagem [**\_ GETFOLDERPATH**](cdm-getfolderpath.md) do CDM para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="48929-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="48929-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48929-120">Requirements</span></span>



| <span data-ttu-id="48929-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="48929-121">Requirement</span></span> | <span data-ttu-id="48929-122">Valor</span><span class="sxs-lookup"><span data-stu-id="48929-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48929-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48929-123">Minimum supported client</span></span><br/> | <span data-ttu-id="48929-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="48929-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="48929-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48929-125">Minimum supported server</span></span><br/> | <span data-ttu-id="48929-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="48929-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48929-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="48929-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="48929-128"><dt>Commdlg.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="48929-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48929-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="48929-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="48929-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="48929-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="48929-131">**GETFOLDERPATH do CDM \_**</span><span class="sxs-lookup"><span data-stu-id="48929-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="48929-132">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="48929-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="48929-133">**Getsavefilename**</span><span class="sxs-lookup"><span data-stu-id="48929-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="48929-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="48929-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="48929-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="48929-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="48929-136">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="48929-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="48929-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="48929-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>


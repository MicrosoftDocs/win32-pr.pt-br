---
title: CDN_INITDONE de notificação (Commdlg.h)
description: Enviado por uma caixa de diálogo Abrir ou Salvar como no estilo Explorer quando o sistema terminar de organizar os controles na caixa de diálogo. O sistema move os controles padrão para dar espaço aos controles da caixa de diálogo filho.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- CDN_INITDONE caixa de diálogo de código de notificação
topic_type:
- apiref
api_name:
- CDN_INITDONE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6594c161d57a5d0772679477ee9bce2cda28ba12
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549831"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="f23f4-105">Código de \_ notificação DE CDN INITDONE</span><span class="sxs-lookup"><span data-stu-id="f23f4-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="f23f4-106">\[Começando com o Windows Vista, as **caixas** de **diálogo** Abrir e Salvar como comuns foram superadas pela caixa de diálogo Item [Comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="f23f4-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="f23f4-107">Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]</span><span class="sxs-lookup"><span data-stu-id="f23f4-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="f23f4-108">Enviado por uma caixa de diálogo **Abrir** ou Salvar **como** no estilo Explorer quando o sistema terminar de organizar os controles na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f23f4-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="f23f4-109">O sistema move os controles padrão para dar espaço aos controles da caixa de diálogo filho.</span><span class="sxs-lookup"><span data-stu-id="f23f4-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="f23f4-110">O [*procedimento de gancho OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="f23f4-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="f23f4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f23f4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f23f4-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f23f4-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f23f4-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="f23f4-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f23f4-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f23f4-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f23f4-115">Um ponteiro para uma [**estrutura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="f23f4-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="f23f4-116">A **estrutura OFNOTIFY** contém uma [**estrutura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cujo** membro de código indica a mensagem **de \_ notificação CDN INITDONE.**</span><span class="sxs-lookup"><span data-stu-id="f23f4-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f23f4-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f23f4-117">Return value</span></span>

<span data-ttu-id="f23f4-118">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f23f4-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f23f4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f23f4-119">Remarks</span></span>

<span data-ttu-id="f23f4-120">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="f23f4-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23f4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f23f4-121">Requirements</span></span>



| <span data-ttu-id="f23f4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f23f4-122">Requirement</span></span> | <span data-ttu-id="f23f4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f23f4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f23f4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f23f4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f23f4-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f23f4-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f23f4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f23f4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f23f4-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f23f4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f23f4-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f23f4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f23f4-129"><dt>Commdlg.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f23f4-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23f4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f23f4-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="f23f4-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="f23f4-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f23f4-132">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="f23f4-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="f23f4-133">**Getsavefilename**</span><span class="sxs-lookup"><span data-stu-id="f23f4-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="f23f4-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="f23f4-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="f23f4-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="f23f4-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="f23f4-136">**Openfilename**</span><span class="sxs-lookup"><span data-stu-id="f23f4-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="f23f4-137">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="f23f4-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f23f4-138">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="f23f4-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>


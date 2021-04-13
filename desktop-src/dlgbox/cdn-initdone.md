---
title: CDN_INITDONE código de notificação (Commdlg. h)
description: Enviado por uma caixa de diálogo abrir no estilo do Explorer ou salvar como quando o sistema tiver terminado de organizar os controles na caixa de diálogo. O sistema move os controles padrão para liberar espaço para os controles da caixa de diálogo filho.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- Caixas de diálogo CDN_INITDONE código de notificação
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
ms.openlocfilehash: 9e6d51f1c34a0a399775e1786356aae4fc6526fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369611"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="b5656-105">Código de notificação da CDN \_ INITDONE</span><span class="sxs-lookup"><span data-stu-id="b5656-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="b5656-106">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5656-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="b5656-107">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="b5656-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="b5656-108">Enviado por uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** quando o sistema tiver terminado de organizar os controles na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b5656-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="b5656-109">O sistema move os controles padrão para liberar espaço para os controles da caixa de diálogo filho.</span><span class="sxs-lookup"><span data-stu-id="b5656-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="b5656-110">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b5656-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="b5656-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5656-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5656-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5656-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5656-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="b5656-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5656-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5656-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5656-115">Um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="b5656-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="b5656-116">A estrutura **OFNOTIFY** contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação **CDN \_ INITDONE** .</span><span class="sxs-lookup"><span data-stu-id="b5656-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5656-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5656-117">Return value</span></span>

<span data-ttu-id="b5656-118">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="b5656-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5656-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5656-119">Remarks</span></span>

<span data-ttu-id="b5656-120">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o valor do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="b5656-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5656-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5656-121">Requirements</span></span>



| <span data-ttu-id="b5656-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5656-122">Requirement</span></span> | <span data-ttu-id="b5656-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b5656-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5656-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5656-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b5656-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b5656-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b5656-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5656-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b5656-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b5656-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5656-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b5656-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5656-129"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5656-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5656-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5656-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="b5656-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b5656-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b5656-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="b5656-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="b5656-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="b5656-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="b5656-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="b5656-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="b5656-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="b5656-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="b5656-136">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="b5656-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="b5656-137">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b5656-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b5656-138">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="b5656-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


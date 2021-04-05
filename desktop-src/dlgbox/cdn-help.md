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
ms.openlocfilehash: c73b690b1ac522a985ae121413804c4385e0f2cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086101"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="8ef00-104">Código de notificação da ajuda da CDN \_</span><span class="sxs-lookup"><span data-stu-id="8ef00-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="8ef00-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ef00-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="8ef00-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="8ef00-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="8ef00-107">Enviado por uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** quando o usuário clica no botão **ajuda** .</span><span class="sxs-lookup"><span data-stu-id="8ef00-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="8ef00-108">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8ef00-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="8ef00-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ef00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ef00-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ef00-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef00-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="8ef00-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef00-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ef00-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef00-113">Um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="8ef00-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="8ef00-114">A estrutura **OFNOTIFY** contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação da **\_ ajuda da CDN** .</span><span class="sxs-lookup"><span data-stu-id="8ef00-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ef00-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ef00-115">Return value</span></span>

<span data-ttu-id="8ef00-116">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8ef00-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ef00-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ef00-117">Remarks</span></span>

<span data-ttu-id="8ef00-118">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o valor do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="8ef00-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ef00-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ef00-119">Requirements</span></span>



| <span data-ttu-id="8ef00-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ef00-120">Requirement</span></span> | <span data-ttu-id="8ef00-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8ef00-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef00-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ef00-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8ef00-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8ef00-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8ef00-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ef00-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8ef00-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8ef00-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8ef00-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8ef00-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ef00-127"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ef00-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ef00-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ef00-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ef00-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8ef00-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8ef00-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="8ef00-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="8ef00-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="8ef00-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="8ef00-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="8ef00-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="8ef00-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="8ef00-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="8ef00-134">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="8ef00-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="8ef00-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="8ef00-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8ef00-136">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="8ef00-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


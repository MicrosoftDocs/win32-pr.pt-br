---
title: CDN_FILEOK código de notificação (Commdlg. h)
description: Enviado por uma caixa de diálogo abrir no estilo do Explorer ou salvar como quando o usuário especifica um nome de arquivo e clica no botão OK.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- Caixas de diálogo CDN_FILEOK código de notificação
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759020"
---
# <a name="cdn_fileok-notification-code"></a><span data-ttu-id="15bdd-104">Código de notificação da CDN \_ FILEOK</span><span class="sxs-lookup"><span data-stu-id="15bdd-104">CDN\_FILEOK notification code</span></span>

<span data-ttu-id="15bdd-105">Enviado por uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** quando o usuário especifica um nome de arquivo e clica no botão **OK** .</span><span class="sxs-lookup"><span data-stu-id="15bdd-105">Sent by an Explorer-style **Open** or **Save As** dialog box when the user specifies a file name and clicks the **OK** button.</span></span>

<span data-ttu-id="15bdd-106">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="15bdd-106">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="15bdd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15bdd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15bdd-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15bdd-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15bdd-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="15bdd-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="15bdd-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15bdd-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15bdd-111">Um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="15bdd-111">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="15bdd-112">A estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação **CDN \_ FILEOK** .</span><span class="sxs-lookup"><span data-stu-id="15bdd-112">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FILEOK** notification message.</span></span>

<span data-ttu-id="15bdd-113">A estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) também contém um ponteiro para uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) cujo membro **lpstrFile** especifica o endereço do nome de arquivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="15bdd-113">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **lpstrFile** member specifies the address of the selected file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15bdd-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15bdd-114">Return value</span></span>

<span data-ttu-id="15bdd-115">Se o procedimento de gancho retornar zero, a caixa de diálogo aceitará o nome de arquivo especificado e fechará.</span><span class="sxs-lookup"><span data-stu-id="15bdd-115">If the hook procedure returns zero, the dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="15bdd-116">Para rejeitar o nome de arquivo especificado e forçar a caixa de diálogo a permanecer aberta, retorne um valor diferente de zero do procedimento de gancho e chame a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para definir um valor de **\_ MSGRESULT de DWL** diferente.</span><span class="sxs-lookup"><span data-stu-id="15bdd-116">To reject the specified file name and force the dialog box to remain open, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set a nonzero **DWL\_MSGRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15bdd-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="15bdd-117">Remarks</span></span>

<span data-ttu-id="15bdd-118">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o valor do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="15bdd-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="15bdd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15bdd-119">Requirements</span></span>



| <span data-ttu-id="15bdd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="15bdd-120">Requirement</span></span> | <span data-ttu-id="15bdd-121">Valor</span><span class="sxs-lookup"><span data-stu-id="15bdd-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15bdd-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15bdd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="15bdd-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15bdd-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="15bdd-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15bdd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="15bdd-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15bdd-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15bdd-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="15bdd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="15bdd-127"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15bdd-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15bdd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="15bdd-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="15bdd-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="15bdd-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="15bdd-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="15bdd-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="15bdd-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="15bdd-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="15bdd-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="15bdd-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="15bdd-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="15bdd-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="15bdd-134">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="15bdd-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="15bdd-135">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="15bdd-135">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="15bdd-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="15bdd-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="15bdd-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="15bdd-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="15bdd-138">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="15bdd-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="15bdd-139">**notificação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="15bdd-139">**WM\_NOTIFY**</span></span>](../controls/wm-notify.md)
</dt> </dl>

 


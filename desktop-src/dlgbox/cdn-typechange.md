---
title: CDN_TYPECHANGE código de notificação (Commdlg. h)
description: Enviado por uma caixa de diálogo abrir no estilo do Explorer ou salvar como quando o usuário seleciona um novo tipo de arquivo na caixa de combinação tipos de arquivo.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- Caixas de diálogo CDN_TYPECHANGE código de notificação
topic_type:
- apiref
api_name:
- CDN_TYPECHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64226c1ac15cb6b55c6c2e2de7264d726e6f3a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455132"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="8b674-104">Código de notificação da CDN \_ TYPECHANGE</span><span class="sxs-lookup"><span data-stu-id="8b674-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="8b674-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b674-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="8b674-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="8b674-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="8b674-107">Enviado por uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** quando o usuário seleciona um novo tipo de arquivo na caixa de combinação tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8b674-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="8b674-108">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8b674-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="8b674-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b674-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b674-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b674-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b674-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="8b674-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b674-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b674-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b674-113">Um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="8b674-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="8b674-114">A estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação **CDN \_ TYPECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="8b674-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="8b674-115">A estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) também contém um ponteiro para uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) cujo membro **nFilterIndex** indica o índice baseado em um do filtro de tipo de arquivo selecionado recentemente.</span><span class="sxs-lookup"><span data-stu-id="8b674-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b674-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b674-116">Return value</span></span>

<span data-ttu-id="8b674-117">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="8b674-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b674-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b674-118">Remarks</span></span>

<span data-ttu-id="8b674-119">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o valor do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="8b674-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b674-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b674-120">Requirements</span></span>



| <span data-ttu-id="8b674-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b674-121">Requirement</span></span> | <span data-ttu-id="8b674-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8b674-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b674-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b674-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8b674-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8b674-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8b674-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b674-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8b674-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8b674-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8b674-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8b674-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b674-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b674-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b674-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b674-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b674-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8b674-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8b674-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="8b674-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="8b674-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="8b674-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="8b674-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="8b674-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="8b674-134">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="8b674-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="8b674-135">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="8b674-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="8b674-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="8b674-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8b674-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="8b674-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


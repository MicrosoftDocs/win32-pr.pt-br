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
ms.openlocfilehash: 180a16c32fb6e83ea0b17e38b42ce8c729f7685a
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590803"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="4d9e5-104">Código de notificação da CDN \_ TYPECHANGE</span><span class="sxs-lookup"><span data-stu-id="4d9e5-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="4d9e5-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="4d9e5-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="4d9e5-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="4d9e5-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="4d9e5-107">Enviado por uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** quando o usuário seleciona um novo tipo de arquivo na caixa de combinação tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4d9e5-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="4d9e5-108">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4d9e5-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="4d9e5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d9e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d9e5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d9e5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d9e5-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="4d9e5-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4d9e5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d9e5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d9e5-113">Um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="4d9e5-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="4d9e5-114">A estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação **CDN \_ TYPECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="4d9e5-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="4d9e5-115">A estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) também contém um ponteiro para uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) cujo membro **nFilterIndex** indica o índice baseado em um do filtro de tipo de arquivo selecionado recentemente.</span><span class="sxs-lookup"><span data-stu-id="4d9e5-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d9e5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d9e5-116">Return value</span></span>

<span data-ttu-id="4d9e5-117">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="4d9e5-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d9e5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d9e5-118">Remarks</span></span>

<span data-ttu-id="4d9e5-119">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o valor do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="4d9e5-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d9e5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d9e5-120">Requirements</span></span>



| <span data-ttu-id="4d9e5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d9e5-121">Requirement</span></span> | <span data-ttu-id="4d9e5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4d9e5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d9e5-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d9e5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4d9e5-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4d9e5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4d9e5-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d9e5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4d9e5-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4d9e5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4d9e5-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4d9e5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d9e5-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d9e5-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d9e5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d9e5-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="4d9e5-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4d9e5-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4d9e5-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="4d9e5-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="4d9e5-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="4d9e5-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="4d9e5-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="4d9e5-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="4d9e5-134">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="4d9e5-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="4d9e5-135">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="4d9e5-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="4d9e5-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="4d9e5-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4d9e5-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="4d9e5-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


---
title: CDN_TYPECHANGE de notificação (Commdlg.h)
description: Enviado por uma caixa de diálogo Abrir ou Salvar como no estilo Explorer quando o usuário seleciona um novo tipo de arquivo na caixa de combinação tipos de arquivo.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- CDN_TYPECHANGE caixa de diálogo de código de notificação
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
ms.openlocfilehash: 3922dd71b70ace579fa4b5f2318776779afdfa4e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548861"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="b76af-104">Código de \_ notificação TYPECHANGE da CDN</span><span class="sxs-lookup"><span data-stu-id="b76af-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="b76af-105">\[Começando com o Windows Vista, as **caixas** de **diálogo** Abrir e Salvar como comuns foram superadas pela caixa de diálogo Item [Comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="b76af-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="b76af-106">Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]</span><span class="sxs-lookup"><span data-stu-id="b76af-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="b76af-107">Enviado por uma caixa de diálogo **Abrir** ou Salvar **como** no estilo Explorer quando o usuário seleciona um novo tipo de arquivo na caixa de combinação tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b76af-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="b76af-108">O [*procedimento de gancho OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="b76af-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="b76af-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b76af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b76af-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b76af-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b76af-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="b76af-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b76af-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b76af-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b76af-113">Um ponteiro para uma [**estrutura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="b76af-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="b76af-114">A [**estrutura OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cujo** membro de código indica a mensagem de notificação **\_ TYPECHANGE da CDN.**</span><span class="sxs-lookup"><span data-stu-id="b76af-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="b76af-115">A [**estrutura OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) também contém um ponteiro para uma estrutura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) cujo membro **nFilterIndex** indica o índice baseado em um do filtro de tipo de arquivo recém-selecionado.</span><span class="sxs-lookup"><span data-stu-id="b76af-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b76af-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b76af-116">Return value</span></span>

<span data-ttu-id="b76af-117">Essa mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b76af-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b76af-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b76af-118">Remarks</span></span>

<span data-ttu-id="b76af-119">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="b76af-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b76af-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b76af-120">Requirements</span></span>



| <span data-ttu-id="b76af-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b76af-121">Requirement</span></span> | <span data-ttu-id="b76af-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b76af-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b76af-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b76af-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b76af-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b76af-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b76af-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b76af-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b76af-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b76af-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b76af-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b76af-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b76af-128"><dt>Commdlg.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b76af-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b76af-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b76af-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="b76af-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b76af-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b76af-131">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="b76af-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="b76af-132">**Getsavefilename**</span><span class="sxs-lookup"><span data-stu-id="b76af-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="b76af-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="b76af-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="b76af-134">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="b76af-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="b76af-135">**Openfilename**</span><span class="sxs-lookup"><span data-stu-id="b76af-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="b76af-136">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="b76af-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b76af-137">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="b76af-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>


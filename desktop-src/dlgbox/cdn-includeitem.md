---
title: CDN_INCLUDEITEM código de notificação (Commdlg. h)
description: Enviado por uma caixa de diálogo abrir ou salvar como para determinar se a caixa de diálogo deve exibir um item na lista de itens de uma pasta do Shell.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- Caixas de diálogo CDN_INCLUDEITEM código de notificação
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a91c61e4a7c2786e67ed28e2c62e5963762659c
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590773"
---
# <a name="cdn_includeitem-notification-code"></a><span data-ttu-id="f6c20-104">Código de notificação da CDN \_ INCLUDEITEM</span><span class="sxs-lookup"><span data-stu-id="f6c20-104">CDN\_INCLUDEITEM notification code</span></span>

<span data-ttu-id="f6c20-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="f6c20-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="f6c20-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="f6c20-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="f6c20-107">Enviado por uma caixa de diálogo **abrir** ou **salvar como** para determinar se a caixa de diálogo deve exibir um item na lista de itens de uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="f6c20-107">Sent by an **Open** or **Save As** dialog box to determine whether the dialog box should display an item in a shell folder's item list.</span></span> <span data-ttu-id="f6c20-108">Quando o usuário abre uma pasta, a caixa de diálogo envia uma notificação **\_ INCLUDEITEM de CDN** para cada item na pasta.</span><span class="sxs-lookup"><span data-stu-id="f6c20-108">When the user opens a folder, the dialog box sends a **CDN\_INCLUDEITEM** notification for each item in the folder.</span></span> <span data-ttu-id="f6c20-109">A caixa de diálogo enviará essa notificação somente se o sinalizador **OFN \_ ENABLEINCLUDENOTIFY** tiver sido definido quando a caixa de diálogo foi criada.</span><span class="sxs-lookup"><span data-stu-id="f6c20-109">The dialog box sends this notification only if the **OFN\_ENABLEINCLUDENOTIFY** flag was set when the dialog box was created.</span></span>

<span data-ttu-id="f6c20-110">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f6c20-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a><span data-ttu-id="f6c20-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6c20-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6c20-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6c20-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c20-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="f6c20-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f6c20-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6c20-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6c20-115">Um ponteiro para uma estrutura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) .</span><span class="sxs-lookup"><span data-stu-id="f6c20-115">A pointer to an [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure.</span></span>

<span data-ttu-id="f6c20-116">A estrutura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação **CDN \_ INCLUDEITEM** .</span><span class="sxs-lookup"><span data-stu-id="f6c20-116">The [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INCLUDEITEM** notification message.</span></span>

<span data-ttu-id="f6c20-117">O membro **PSF** da estrutura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) é um ponteiro para uma interface para a pasta cujos itens estão sendo enumerados.</span><span class="sxs-lookup"><span data-stu-id="f6c20-117">The **psf** member of the [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure is a pointer to an interface for the folder whose items are being enumerated.</span></span> <span data-ttu-id="f6c20-118">O membro **PIDL** é um ponteiro para uma lista de identificadores de item que identifica o item relativo à pasta.</span><span class="sxs-lookup"><span data-stu-id="f6c20-118">The **pidl** member is a pointer to an item identifier list that identifies the item relative to the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6c20-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6c20-119">Return value</span></span>

<span data-ttu-id="f6c20-120">Se o procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) retornar zero, a caixa de diálogo excluirá o item da lista de itens.</span><span class="sxs-lookup"><span data-stu-id="f6c20-120">If the [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure returns zero, the dialog box excludes the item from the list of items.</span></span>

<span data-ttu-id="f6c20-121">Para incluir o item, retorne um valor diferente de zero do procedimento de gancho.</span><span class="sxs-lookup"><span data-stu-id="f6c20-121">To include the item, return a nonzero value from the hook procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6c20-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6c20-122">Remarks</span></span>

<span data-ttu-id="f6c20-123">A caixa de diálogo sempre inclui itens que têm os atributos **SFGAO \_ FileSystem** e **SFGAO \_ FILESYSANCESTOR** , independentemente do valor retornado pela **CDN \_ INCLUDEITEM**.</span><span class="sxs-lookup"><span data-stu-id="f6c20-123">The dialog box always includes items that have both the **SFGAO\_FILESYSTEM** and **SFGAO\_FILESYSANCESTOR** attributes, regardless of the value returned by **CDN\_INCLUDEITEM**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c20-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6c20-124">Requirements</span></span>



| <span data-ttu-id="f6c20-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6c20-125">Requirement</span></span> | <span data-ttu-id="f6c20-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f6c20-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c20-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6c20-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c20-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6c20-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f6c20-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6c20-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c20-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6c20-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f6c20-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f6c20-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6c20-132"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6c20-132"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6c20-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6c20-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6c20-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="f6c20-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f6c20-135">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="f6c20-135">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="f6c20-136">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="f6c20-136">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="f6c20-137">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="f6c20-137">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="f6c20-138">**OFNOTIFYEX**</span><span class="sxs-lookup"><span data-stu-id="f6c20-138">**OFNOTIFYEX**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

<span data-ttu-id="f6c20-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="f6c20-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f6c20-140">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="f6c20-140">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


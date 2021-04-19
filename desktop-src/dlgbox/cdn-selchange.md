---
title: CDN_SELCHANGE código de notificação (Commdlg. h)
description: Enviado por uma caixa de diálogo abrir no estilo do Explorer ou salvar como quando a seleção é alterada na caixa de listagem que exibe o conteúdo da pasta ou do diretório aberto no momento.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- Caixas de diálogo CDN_SELCHANGE código de notificação
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a5c7aed47d02fb7c7fcf2232b144e7a99e7c46
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590749"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="a511c-104">Código de notificação da CDN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="a511c-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="a511c-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="a511c-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="a511c-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="a511c-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="a511c-107">Enviado por uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** quando a seleção é alterada na caixa de listagem que exibe o conteúdo da pasta ou do diretório aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="a511c-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="a511c-108">Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a511c-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="a511c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a511c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a511c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a511c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a511c-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="a511c-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a511c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a511c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a511c-113">Um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="a511c-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="a511c-114">A estrutura **OFNOTIFY** contém uma estrutura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação **CDN \_ SELCHANGE** .</span><span class="sxs-lookup"><span data-stu-id="a511c-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a511c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a511c-115">Return value</span></span>

<span data-ttu-id="a511c-116">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="a511c-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a511c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a511c-117">Remarks</span></span>

<span data-ttu-id="a511c-118">O sistema enviará essa notificação somente se a caixa de diálogo tiver sido criada usando o valor do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="a511c-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="a511c-119">Para obter o nome do arquivo ou da pasta recentemente selecionada, o procedimento de gancho pode enviar a mensagem [**CDM \_ GetFilePath**](cdm-getfilepath.md) ou [**CDM \_ getspec**](cdm-getspec.md) para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a511c-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="a511c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a511c-120">Requirements</span></span>



| <span data-ttu-id="a511c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a511c-121">Requirement</span></span> | <span data-ttu-id="a511c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a511c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a511c-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a511c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a511c-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a511c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a511c-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a511c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a511c-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a511c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a511c-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a511c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a511c-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a511c-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a511c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a511c-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="a511c-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a511c-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a511c-131">**CDM \_ GETfilepath**</span><span class="sxs-lookup"><span data-stu-id="a511c-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="a511c-132">**CDM \_ GETspec**</span><span class="sxs-lookup"><span data-stu-id="a511c-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="a511c-133">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="a511c-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="a511c-134">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="a511c-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="a511c-135">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="a511c-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="a511c-136">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="a511c-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="a511c-137">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a511c-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a511c-138">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="a511c-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


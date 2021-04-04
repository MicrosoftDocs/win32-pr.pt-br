---
title: EN_CLIPFORMAT código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que ocorreu uma colagem com um formato de área de transferência específico. Um controle de edição rico sem janela envia essa notificação usando o método ITextHost TxNotify.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918275"
---
# <a name="en_clipformat-notification-code"></a><span data-ttu-id="02d95-105">\_Código de notificação en CLIPFORMAT</span><span class="sxs-lookup"><span data-stu-id="02d95-105">EN\_CLIPFORMAT notification code</span></span>

<span data-ttu-id="02d95-106">Notifica uma janela pai do controle de edição rico que ocorreu uma colagem com um formato de área de transferência específico.</span><span class="sxs-lookup"><span data-stu-id="02d95-106">Notifies a rich edit control's parent window that a paste occurred with a particular clipboard format.</span></span> <span data-ttu-id="02d95-107">Um controle de edição rico sem janela envia essa notificação usando o método [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .</span><span class="sxs-lookup"><span data-stu-id="02d95-107">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span>


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="02d95-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02d95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02d95-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02d95-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02d95-110">A ID da janela recuperada chamando a função [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) com o \_ valor da ID GWL.</span><span class="sxs-lookup"><span data-stu-id="02d95-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="02d95-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02d95-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02d95-112">Um ponteiro para uma estrutura [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) que contém informações sobre o formato da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="02d95-112">A pointer to a [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) structure that contains information about the clipboard format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02d95-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02d95-113">Return value</span></span>

<span data-ttu-id="02d95-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="02d95-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="02d95-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="02d95-115">Remarks</span></span>

<span data-ttu-id="02d95-116">Para receber \_ códigos de notificação do en CLIPFORMAT, especifique [**enm \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="02d95-116">To receive EN\_CLIPFORMAT notification codes, specify [**ENM\_CLIPFORMAT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="02d95-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02d95-117">Requirements</span></span>



| <span data-ttu-id="02d95-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="02d95-118">Requirement</span></span> | <span data-ttu-id="02d95-119">Valor</span><span class="sxs-lookup"><span data-stu-id="02d95-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02d95-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02d95-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02d95-121">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="02d95-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="02d95-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02d95-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02d95-123">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="02d95-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02d95-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02d95-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="02d95-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="02d95-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02d95-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="02d95-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d95-127">**CLIPBOARDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="02d95-127">**CLIPBOARDFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 


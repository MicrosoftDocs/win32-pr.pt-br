---
title: Mensagem de WM_CLIPBOARDUPDATE (WinUser. h)
description: Enviado quando o conteúdo da área de transferência foi alterado.
ms.assetid: 1508aa22-9cf0-40a2-8cb0-ce7c8671df2c
keywords:
- Troca de dados de mensagem WM_CLIPBOARDUPDATE
topic_type:
- apiref
api_name:
- WM_CLIPBOARDUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303110f0d094cfed336a9f92006b3720a0ccc83b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085691"
---
# <a name="wm_clipboardupdate-message"></a><span data-ttu-id="c1691-104">Mensagem do WM \_ CLIPBOARDUPDATE</span><span class="sxs-lookup"><span data-stu-id="c1691-104">WM\_CLIPBOARDUPDATE message</span></span>

<span data-ttu-id="c1691-105">Enviado quando o conteúdo da área de transferência foi alterado.</span><span class="sxs-lookup"><span data-stu-id="c1691-105">Sent when the contents of the clipboard have changed.</span></span>


```C++
#define WM_CLIPBOARDUPDATE              0x031D
```



## <a name="parameters"></a><span data-ttu-id="c1691-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1691-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1691-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1691-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1691-108">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c1691-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1691-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1691-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1691-110">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c1691-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1691-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1691-111">Return value</span></span>

<span data-ttu-id="c1691-112">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="c1691-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1691-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1691-113">Remarks</span></span>

<span data-ttu-id="c1691-114">Para registrar uma janela para receber essa mensagem, use a função [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="c1691-114">To register a window to receive this message, use the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1691-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1691-115">Requirements</span></span>



| <span data-ttu-id="c1691-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1691-116">Requirement</span></span> | <span data-ttu-id="c1691-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c1691-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1691-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1691-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c1691-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1691-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c1691-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1691-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c1691-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1691-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1691-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1691-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1691-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1691-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1691-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1691-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1691-125">**AddClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="c1691-125">**AddClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="c1691-126">**RemoveClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="c1691-126">**RemoveClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="c1691-127">**GetClipboardSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="c1691-127">**GetClipboardSequenceNumber**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
</dt> </dl>

 

 






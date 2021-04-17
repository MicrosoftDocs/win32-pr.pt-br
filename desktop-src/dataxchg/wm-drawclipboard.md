---
title: Mensagem de WM_DRAWCLIPBOARD (WinUser. h)
description: Enviado para a primeira janela na cadeia do Visualizador da área de transferência quando o conteúdo da área de transferência é alterado. Isso permite que uma janela do Visualizador da área de transferência exiba o novo conteúdo da área de transferência. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- Troca de dados de mensagem WM_DRAWCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811774"
---
# <a name="wm_drawclipboard-message"></a><span data-ttu-id="ecd5a-106">Mensagem do WM \_ DRAWCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="ecd5a-106">WM\_DRAWCLIPBOARD message</span></span>

<span data-ttu-id="ecd5a-107">Enviado para a primeira janela na cadeia do Visualizador da área de transferência quando o conteúdo da área de transferência é alterado.</span><span class="sxs-lookup"><span data-stu-id="ecd5a-107">Sent to the first window in the clipboard viewer chain when the content of the clipboard changes.</span></span> <span data-ttu-id="ecd5a-108">Isso permite que uma janela do Visualizador da área de transferência exiba o novo conteúdo da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ecd5a-108">This enables a clipboard viewer window to display the new content of the clipboard.</span></span>

<span data-ttu-id="ecd5a-109">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ecd5a-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a><span data-ttu-id="ecd5a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecd5a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecd5a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecd5a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecd5a-112">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ecd5a-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ecd5a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecd5a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecd5a-114">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ecd5a-114">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecd5a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecd5a-115">Remarks</span></span>

<span data-ttu-id="ecd5a-116">Somente as janelas do Visualizador da área de transferência recebem essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="ecd5a-116">Only clipboard viewer windows receive this message.</span></span> <span data-ttu-id="ecd5a-117">Essas são as janelas que foram adicionadas à cadeia do Visualizador da área de transferência usando a função [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="ecd5a-117">These are windows that have been added to the clipboard viewer chain by using the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="ecd5a-118">Cada janela que recebe a **mensagem \_ DRAWCLIPBOARD do WM** deve chamar a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para passar a mensagem para a próxima janela na cadeia do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ecd5a-118">Each window that receives the **WM\_DRAWCLIPBOARD** message must call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message on to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="ecd5a-119">O identificador para a próxima janela na cadeia é retornado por [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)e pode ser alterado em resposta a uma mensagem do [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd5a-119">The handle to the next window in the chain is returned by [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer), and may change in response to a [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd5a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecd5a-120">Requirements</span></span>



| <span data-ttu-id="ecd5a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecd5a-121">Requirement</span></span> | <span data-ttu-id="ecd5a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ecd5a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd5a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecd5a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ecd5a-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ecd5a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ecd5a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecd5a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ecd5a-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ecd5a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ecd5a-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ecd5a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecd5a-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecd5a-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecd5a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecd5a-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ecd5a-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ecd5a-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="ecd5a-132">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-132">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="ecd5a-133">**CHANGECBCHAIN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-133">**WM\_CHANGECBCHAIN**</span></span>](wm-changecbchain.md)
</dt> <dt>

<span data-ttu-id="ecd5a-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ecd5a-135">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="ecd5a-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


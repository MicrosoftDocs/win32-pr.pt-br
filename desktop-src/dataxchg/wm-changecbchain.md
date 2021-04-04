---
title: Mensagem de WM_CHANGECBCHAIN (WinUser. h)
description: Enviado para a primeira janela na cadeia do Visualizador da área de transferência quando uma janela está sendo removida da cadeia. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- Troca de dados de mensagem WM_CHANGECBCHAIN
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085692"
---
# <a name="wm_changecbchain-message"></a><span data-ttu-id="000ae-105">Mensagem do WM \_ CHANGECBCHAIN</span><span class="sxs-lookup"><span data-stu-id="000ae-105">WM\_CHANGECBCHAIN message</span></span>

<span data-ttu-id="000ae-106">Enviado para a primeira janela na cadeia do Visualizador da área de transferência quando uma janela está sendo removida da cadeia.</span><span class="sxs-lookup"><span data-stu-id="000ae-106">Sent to the first window in the clipboard viewer chain when a window is being removed from the chain.</span></span>

<span data-ttu-id="000ae-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="000ae-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a><span data-ttu-id="000ae-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="000ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="000ae-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="000ae-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="000ae-110">Um identificador para a janela que está sendo removida da cadeia do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="000ae-110">A handle to the window being removed from the clipboard viewer chain.</span></span>

</dd> <dt>

<span data-ttu-id="000ae-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="000ae-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="000ae-112">Um identificador para a próxima janela na cadeia após a janela que está sendo removida.</span><span class="sxs-lookup"><span data-stu-id="000ae-112">A handle to the next window in the chain following the window being removed.</span></span> <span data-ttu-id="000ae-113">Esse parâmetro será **nulo** se a janela que está sendo removida for a última janela na cadeia.</span><span class="sxs-lookup"><span data-stu-id="000ae-113">This parameter is **NULL** if the window being removed is the last window in the chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="000ae-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="000ae-114">Return value</span></span>

<span data-ttu-id="000ae-115">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="000ae-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="000ae-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="000ae-116">Remarks</span></span>

<span data-ttu-id="000ae-117">Cada janela do Visualizador da área de transferência salva o identificador na próxima janela da cadeia do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="000ae-117">Each clipboard viewer window saves the handle to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="000ae-118">Inicialmente, esse identificador é o valor de retorno da função [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="000ae-118">Initially, this handle is the return value of the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="000ae-119">Quando uma janela do Visualizador da área de transferência recebe a mensagem **\_ CHANGECBCHAIN do WM** , ela deve chamar a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para passar a mensagem para a próxima janela na cadeia, a menos que a janela seguinte esteja sendo removida.</span><span class="sxs-lookup"><span data-stu-id="000ae-119">When a clipboard viewer window receives the **WM\_CHANGECBCHAIN** message, it should call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message to the next window in the chain, unless the next window is the window being removed.</span></span> <span data-ttu-id="000ae-120">Nesse caso, o Visualizador da área de transferência deve salvar o identificador especificado pelo parâmetro *lParam* como a próxima janela na cadeia.</span><span class="sxs-lookup"><span data-stu-id="000ae-120">In this case, the clipboard viewer should save the handle specified by the *lParam* parameter as the next window in the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="000ae-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="000ae-121">Requirements</span></span>



| <span data-ttu-id="000ae-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="000ae-122">Requirement</span></span> | <span data-ttu-id="000ae-123">Valor</span><span class="sxs-lookup"><span data-stu-id="000ae-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="000ae-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="000ae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="000ae-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="000ae-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="000ae-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="000ae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="000ae-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="000ae-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="000ae-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="000ae-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="000ae-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="000ae-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="000ae-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="000ae-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="000ae-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="000ae-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="000ae-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="000ae-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="000ae-133">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="000ae-133">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

<span data-ttu-id="000ae-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="000ae-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="000ae-135">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="000ae-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


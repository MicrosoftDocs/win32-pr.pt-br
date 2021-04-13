---
title: Mensagem de WM_RENDERALLFORMATS (WinUser. h)
description: Enviado para o proprietário da área de transferência antes de ser destruído, se o proprietário da área de transferência tiver atrasado o processamento de um ou mais formatos de área de transferência.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- Troca de dados de mensagem WM_RENDERALLFORMATS
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499633"
---
# <a name="wm_renderallformats-message"></a><span data-ttu-id="a9835-104">Mensagem do WM \_ RENDERALLFORMATS</span><span class="sxs-lookup"><span data-stu-id="a9835-104">WM\_RENDERALLFORMATS message</span></span>

<span data-ttu-id="a9835-105">Enviado para o proprietário da área de transferência antes de ser destruído, se o proprietário da área de transferência tiver atrasado o processamento de um ou mais formatos de área de transferência.</span><span class="sxs-lookup"><span data-stu-id="a9835-105">Sent to the clipboard owner before it is destroyed, if the clipboard owner has delayed rendering one or more clipboard formats.</span></span> <span data-ttu-id="a9835-106">Para que o conteúdo da área de transferência permaneça disponível para outros aplicativos, o proprietário da área de transferência deve renderizar dados em todos os formatos que são capazes de gerar e colocar os dados na área de transferência chamando a função [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="a9835-106">For the content of the clipboard to remain available to other applications, the clipboard owner must render data in all the formats it is capable of generating, and place the data on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>

<span data-ttu-id="a9835-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a9835-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a><span data-ttu-id="a9835-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9835-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9835-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9835-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9835-110">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a9835-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a9835-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9835-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9835-112">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a9835-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9835-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9835-113">Return value</span></span>

<span data-ttu-id="a9835-114">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="a9835-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9835-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9835-115">Remarks</span></span>

<span data-ttu-id="a9835-116">Ao responder a uma mensagem do **WM \_ RENDERALLFORMATS** , o aplicativo deve chamar a função [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) e, em seguida, verificar se ela ainda é o proprietário da área de transferência chamando a função [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) antes de chamar [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span><span class="sxs-lookup"><span data-stu-id="a9835-116">When responding to a **WM\_RENDERALLFORMATS** message, the application must call the [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) function and then check that it is still the clipboard owner by calling the [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span>

<span data-ttu-id="a9835-117">O aplicativo precisa verificar se ele ainda é o proprietário da área de transferência depois de abrir a área de transferência porque depois de receber a mensagem **\_ RENDERALLFORMATS do WM** , mas antes de abrir a área de transferência, outro aplicativo pode ter aberto e assumido a propriedade da área de transferência e os dados desse aplicativo não devem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="a9835-117">The application needs to check that it is still the clipboard owner after opening the clipboard because after it receives the **WM\_RENDERALLFORMATS** message, but before it opens the clipboard, another application may have opened and taken ownership of the clipboard, and that application's data should not be overwritten.</span></span>

<span data-ttu-id="a9835-118">Na maioria dos casos, o aplicativo não deve chamar a função [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) antes de chamar [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), pois isso apagará os formatos da área de transferência que o aplicativo já tenha processado.</span><span class="sxs-lookup"><span data-stu-id="a9835-118">In most cases, the application should not call the [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), since doing so will erase the clipboard formats that the application has already rendered.</span></span>

<span data-ttu-id="a9835-119">Quando o aplicativo retorna, o sistema remove todos os formatos não renderizados da lista de formatos de área de transferência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a9835-119">When the application returns, the system removes any unrendered formats from the list of available clipboard formats.</span></span> <span data-ttu-id="a9835-120">Para obter informações sobre a renderização atrasada, consulte [processamento atrasado](clipboard-operations.md#delayed-rendering).</span><span class="sxs-lookup"><span data-stu-id="a9835-120">For information about delayed rendering, see [Delayed Rendering](clipboard-operations.md#delayed-rendering).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9835-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9835-121">Requirements</span></span>



| <span data-ttu-id="a9835-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9835-122">Requirement</span></span> | <span data-ttu-id="a9835-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a9835-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9835-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9835-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9835-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a9835-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a9835-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9835-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9835-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a9835-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9835-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a9835-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9835-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9835-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9835-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9835-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9835-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a9835-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a9835-132">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="a9835-132">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[<span data-ttu-id="a9835-133">**OpenClipboard**</span><span class="sxs-lookup"><span data-stu-id="a9835-133">**OpenClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[<span data-ttu-id="a9835-134">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="a9835-134">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="a9835-135">**RENDERFORMAT do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a9835-135">**WM\_RENDERFORMAT**</span></span>](wm-renderformat.md)
</dt> <dt>

<span data-ttu-id="a9835-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a9835-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a9835-137">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="a9835-137">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


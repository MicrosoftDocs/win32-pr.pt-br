---
title: Mensagem de WM_SIZECLIPBOARD (WinUser. h)
description: Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no formato de OWNERDISPLAY do CF \_ e o tamanho do cliente do Visualizador de áreas de transferência é alterado.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- Troca de dados de mensagem WM_SIZECLIPBOARD
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644740"
---
# <a name="wm_sizeclipboard-message"></a><span data-ttu-id="470d6-104">Mensagem do WM \_ SIZECLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="470d6-104">WM\_SIZECLIPBOARD message</span></span>

<span data-ttu-id="470d6-105">Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no formato de [**\_ OWNERDISPLAY do CF**](standard-clipboard-formats.md) e o tamanho do cliente do Visualizador de áreas de transferência é alterado.</span><span class="sxs-lookup"><span data-stu-id="470d6-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area has changed size.</span></span>


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a><span data-ttu-id="470d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="470d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="470d6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="470d6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="470d6-108">Um identificador para a janela do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="470d6-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="470d6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="470d6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="470d6-110">Um identificador para um objeto de memória global que contém uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="470d6-110">A handle to a global memory object that contains a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="470d6-111">A estrutura especifica as novas dimensões da área do cliente do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="470d6-111">The structure specifies the new dimensions of the clipboard viewer's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="470d6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="470d6-112">Return value</span></span>

<span data-ttu-id="470d6-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="470d6-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="470d6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="470d6-114">Remarks</span></span>

<span data-ttu-id="470d6-115">Quando a janela do Visualizador da área de transferência está prestes a ser destruída ou redimensionada, uma mensagem do **WM \_ SIZECLIPBOARD** é enviada com um retângulo nulo (0, 0, 0, 0) como o novo tamanho.</span><span class="sxs-lookup"><span data-stu-id="470d6-115">When the clipboard viewer window is about to be destroyed or resized, a **WM\_SIZECLIPBOARD** message is sent with a null rectangle (0, 0, 0, 0) as the new size.</span></span> <span data-ttu-id="470d6-116">Isso permite que o proprietário da área de transferência libere seus recursos de exibição.</span><span class="sxs-lookup"><span data-stu-id="470d6-116">This permits the clipboard owner to free its display resources.</span></span>

<span data-ttu-id="470d6-117">O proprietário da área de transferência deve usar a função [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) para bloquear o objeto de memória que contém [**Rect**](/previous-versions//dd162897(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="470d6-117">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory object that contains [**RECT**](/previous-versions//dd162897(v=vs.85)).</span></span> <span data-ttu-id="470d6-118">Antes de retornar, o proprietário da área de transferência deve desbloquear o objeto usando a função [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .</span><span class="sxs-lookup"><span data-stu-id="470d6-118">Before returning, the clipboard owner must unlock the object by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="470d6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="470d6-119">Requirements</span></span>



| <span data-ttu-id="470d6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="470d6-120">Requirement</span></span> | <span data-ttu-id="470d6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="470d6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="470d6-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="470d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="470d6-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="470d6-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="470d6-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="470d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="470d6-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="470d6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="470d6-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="470d6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="470d6-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="470d6-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="470d6-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="470d6-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="470d6-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="470d6-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="470d6-130">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="470d6-130">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 


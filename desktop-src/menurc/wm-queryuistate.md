---
title: Mensagem de WM_QUERYUISTATE (WinUser. h)
description: Um aplicativo envia a mensagem do WM \_ QUERYUISTATE para recuperar o estado da interface do usuário para uma janela.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763871"
---
# <a name="wm_queryuistate-message"></a><span data-ttu-id="7e784-104">Mensagem do WM \_ QUERYUISTATE</span><span class="sxs-lookup"><span data-stu-id="7e784-104">WM\_QUERYUISTATE message</span></span>

<span data-ttu-id="7e784-105">Um aplicativo envia a mensagem do **WM \_ QUERYUISTATE** para recuperar o estado da interface do usuário para uma janela.</span><span class="sxs-lookup"><span data-stu-id="7e784-105">An application sends the **WM\_QUERYUISTATE** message to retrieve the UI state for a window.</span></span>


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a><span data-ttu-id="7e784-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e784-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e784-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e784-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e784-108">Esse parâmetro não é usado e deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="7e784-108">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="7e784-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e784-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e784-110">Esse parâmetro não é usado e deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="7e784-110">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e784-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e784-111">Return value</span></span>

<span data-ttu-id="7e784-112">O valor de retorno será **nulo** se os indicadores de foco e os aceleradores de teclado estiverem visíveis.</span><span class="sxs-lookup"><span data-stu-id="7e784-112">The return value is **NULL** if the focus indicators and the keyboard accelerators are visible.</span></span> <span data-ttu-id="7e784-113">Caso contrário, o valor de retorno poderá ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7e784-113">Otherwise, the return value can be one or more of the following values.</span></span>



| <span data-ttu-id="7e784-114">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7e784-114">Return code/value</span></span>                                                                                                                                       | <span data-ttu-id="7e784-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e784-115">Description</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e784-116"><dt>**UISF \_ ATIVO**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="7e784-116"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>    | <span data-ttu-id="7e784-117">Um controle deve ser desenhado no estilo usado para controles ativos.</span><span class="sxs-lookup"><span data-stu-id="7e784-117">A control should be drawn in the style used for active controls.</span></span><br/> |
| <dl> <span data-ttu-id="7e784-118"><dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL</span><span class="sxs-lookup"><span data-stu-id="7e784-118"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="7e784-119">Os aceleradores de teclado estão ocultos.</span><span class="sxs-lookup"><span data-stu-id="7e784-119">Keyboard accelerators are hidden.</span></span><br/>                                |
| <dl> <span data-ttu-id="7e784-120"><dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="7e784-120"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="7e784-121">Os indicadores de foco estão ocultos.</span><span class="sxs-lookup"><span data-stu-id="7e784-121">Focus indicators are hidden.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="7e784-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e784-122">Requirements</span></span>



| <span data-ttu-id="7e784-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e784-123">Requirement</span></span> | <span data-ttu-id="7e784-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7e784-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e784-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e784-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7e784-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7e784-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7e784-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e784-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7e784-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7e784-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7e784-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7e784-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e784-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e784-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e784-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e784-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e784-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7e784-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7e784-133">**CHANGEUISTATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7e784-133">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="7e784-134">**UPDATEUISTATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7e784-134">**WM\_UPDATEUISTATE**</span></span>](wm-updateuistate.md)
</dt> <dt>

<span data-ttu-id="7e784-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="7e784-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7e784-136">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="7e784-136">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

 






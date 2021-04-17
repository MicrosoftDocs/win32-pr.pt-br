---
description: Enviado a uma janela que o usuário está movendo. Ao processar essa mensagem, um aplicativo pode monitorar a posição do retângulo de arrastar e, se necessário, alterar sua posição.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: Mensagem de WM_MOVING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770047"
---
# <a name="wm_moving-message"></a><span data-ttu-id="bd302-104">Mensagem de movimentação do WM \_</span><span class="sxs-lookup"><span data-stu-id="bd302-104">WM\_MOVING message</span></span>

<span data-ttu-id="bd302-105">Enviado a uma janela que o usuário está movendo.</span><span class="sxs-lookup"><span data-stu-id="bd302-105">Sent to a window that the user is moving.</span></span> <span data-ttu-id="bd302-106">Ao processar essa mensagem, um aplicativo pode monitorar a posição do retângulo de arrastar e, se necessário, alterar sua posição.</span><span class="sxs-lookup"><span data-stu-id="bd302-106">By processing this message, an application can monitor the position of the drag rectangle and, if needed, change its position.</span></span>

<span data-ttu-id="bd302-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bd302-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a><span data-ttu-id="bd302-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd302-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd302-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd302-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd302-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="bd302-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bd302-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd302-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd302-112">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) com a posição atual da janela, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="bd302-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the current position of the window, in screen coordinates.</span></span> <span data-ttu-id="bd302-113">Para alterar a posição do retângulo de arrastar, um aplicativo deve alterar os membros dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="bd302-113">To change the position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd302-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd302-114">Return value</span></span>

<span data-ttu-id="bd302-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="bd302-115">Type: **LRESULT**</span></span>

<span data-ttu-id="bd302-116">Um aplicativo deve retornar **true** se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="bd302-116">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd302-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd302-117">Requirements</span></span>



| <span data-ttu-id="bd302-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd302-118">Requirement</span></span> | <span data-ttu-id="bd302-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bd302-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd302-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd302-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bd302-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bd302-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bd302-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd302-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bd302-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bd302-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bd302-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bd302-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd302-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd302-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd302-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd302-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd302-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bd302-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bd302-128">**movimentação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="bd302-128">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="bd302-129">**\_dimensionamento do WM**</span><span class="sxs-lookup"><span data-stu-id="bd302-129">**WM\_SIZING**</span></span>](wm-sizing.md)
</dt> <dt>

<span data-ttu-id="bd302-130">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="bd302-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bd302-131">Windows</span><span class="sxs-lookup"><span data-stu-id="bd302-131">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="bd302-132">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="bd302-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="bd302-133">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd302-133">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 

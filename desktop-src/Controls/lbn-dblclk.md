---
title: Código de notificação LBN_DBLCLK (WinUser. h)
description: Notifica o aplicativo de que o usuário clicou duas vezes em um item em uma caixa de listagem. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: 487282cb-833a-4123-987e-6a417fbd09d4
keywords:
- LBN_DBLCLK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a60623aafb287f2006d9e27da49d0df34c05b05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645027"
---
# <a name="lbn_dblclk-notification-code"></a><span data-ttu-id="6a9e6-105">Código de notificação do LBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="6a9e6-105">LBN\_DBLCLK notification code</span></span>

<span data-ttu-id="6a9e6-106">Notifica o aplicativo de que o usuário clicou duas vezes em um item em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="6a9e6-106">Notifies the application that the user has double-clicked an item in a list box.</span></span> <span data-ttu-id="6a9e6-107">A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="6a9e6-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6a9e6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a9e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a9e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a9e6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a9e6-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="6a9e6-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="6a9e6-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a9e6-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6a9e6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a9e6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a9e6-113">Identificador para a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="6a9e6-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a9e6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a9e6-114">Remarks</span></span>

<span data-ttu-id="6a9e6-115">Este código de notificação é enviado somente por uma caixa de listagem que tem o estilo de [**\_ notificação L BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6a9e6-115">This notification code is sent only by a list box that has the L [**BS\_NOTIFY**](button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a9e6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a9e6-116">Requirements</span></span>



| <span data-ttu-id="6a9e6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a9e6-117">Requirement</span></span> | <span data-ttu-id="6a9e6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6a9e6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9e6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a9e6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6a9e6-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a9e6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6a9e6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a9e6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6a9e6-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a9e6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6a9e6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a9e6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a9e6-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a9e6-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a9e6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a9e6-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a9e6-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6a9e6-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6a9e6-127">LBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="6a9e6-127">LBN\_SELCHANGE</span></span>](lbn-selchange.md)
</dt> <dt>

<span data-ttu-id="6a9e6-128">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="6a9e6-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6a9e6-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9e6-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6a9e6-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9e6-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6a9e6-131">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6a9e6-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


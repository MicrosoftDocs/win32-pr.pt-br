---
title: Código de notificação CBN_DBLCLK (WinUser. h)
description: Enviado quando o usuário clica duas vezes em uma cadeia de caracteres na caixa de listagem de uma caixa de combinação. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- CBN_DBLCLK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841c68079572e1740f074034c1a8097ba6a86253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756237"
---
# <a name="cbn_dblclk-notification-code"></a><span data-ttu-id="1fc14-105">Código de notificação do CBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="1fc14-105">CBN\_DBLCLK notification code</span></span>

<span data-ttu-id="1fc14-106">Enviado quando o usuário clica duas vezes em uma cadeia de caracteres na caixa de listagem de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="1fc14-106">Sent when the user double-clicks a string in the list box of a combo box.</span></span> <span data-ttu-id="1fc14-107">A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="1fc14-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1fc14-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fc14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc14-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1fc14-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fc14-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="1fc14-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="1fc14-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="1fc14-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="1fc14-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fc14-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fc14-113">Identificador para a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="1fc14-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fc14-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fc14-114">Remarks</span></span>

<span data-ttu-id="1fc14-115">Esse código de notificação ocorre apenas para uma caixa de combinação com o estilo [**\_ simples do CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc14-115">This notification code occurs only for a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="1fc14-116">Em uma caixa de combinação com o estilo de [**\_ lista suspensa CBS**](combo-box-styles.md) ou [**CBS \_**](combo-box-styles.md) , um clique duplo não pode ocorrer porque um único clique fecha a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="1fc14-116">In a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, a double-click cannot occur because a single click closes the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc14-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc14-117">Requirements</span></span>



| <span data-ttu-id="1fc14-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc14-118">Requirement</span></span> | <span data-ttu-id="1fc14-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1fc14-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc14-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fc14-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc14-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1fc14-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1fc14-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fc14-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc14-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1fc14-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1fc14-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fc14-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fc14-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fc14-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fc14-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fc14-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="1fc14-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1fc14-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1fc14-128">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="1fc14-128">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="1fc14-129">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="1fc14-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="1fc14-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1fc14-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1fc14-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1fc14-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1fc14-132">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="1fc14-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


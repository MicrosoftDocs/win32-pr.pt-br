---
title: Código de notificação LBN_ERRSPACE (WinUser. h)
description: Notifica o aplicativo que a caixa de listagem não pode alocar memória suficiente para atender a uma solicitação específica. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: ff716ad0-cbd8-4ac3-bcaf-d5be81355eaa
keywords:
- LBN_ERRSPACE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d324b17a83e38a9b3592be71720486910e88689d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163608"
---
# <a name="lbn_errspace-notification-code"></a><span data-ttu-id="a1387-105">Código de notificação do LBN \_ ERRSPACE</span><span class="sxs-lookup"><span data-stu-id="a1387-105">LBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="a1387-106">Notifica o aplicativo que a caixa de listagem não pode alocar memória suficiente para atender a uma solicitação específica.</span><span class="sxs-lookup"><span data-stu-id="a1387-106">Notifies the application that the list box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="a1387-107">A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="a1387-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a1387-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1387-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1387-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1387-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1387-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="a1387-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="a1387-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="a1387-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="a1387-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1387-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1387-113">Identificador para a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="a1387-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1387-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1387-114">Requirements</span></span>



| <span data-ttu-id="a1387-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1387-115">Requirement</span></span> | <span data-ttu-id="a1387-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a1387-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1387-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1387-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a1387-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1387-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a1387-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1387-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a1387-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a1387-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a1387-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1387-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1387-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1387-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1387-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1387-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1387-124">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="a1387-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="a1387-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a1387-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a1387-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a1387-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a1387-127">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a1387-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


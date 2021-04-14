---
description: Um aplicativo envia a mensagem do WM \_ MDIICONARRANGE para uma janela de cliente de interface de vários documentos (MDI) para organizar todas as janelas filho MDI minimizadas. Ele não afeta as janelas filhas que não são minimizadas.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: Mensagem de WM_MDIICONARRANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461068"
---
# <a name="wm_mdiiconarrange-message"></a><span data-ttu-id="734e4-104">Mensagem do WM \_ MDIICONARRANGE</span><span class="sxs-lookup"><span data-stu-id="734e4-104">WM\_MDIICONARRANGE message</span></span>

<span data-ttu-id="734e4-105">Um aplicativo envia a mensagem do **WM \_ MDIICONARRANGE** para uma janela de cliente de interface de vários documentos (MDI) para organizar todas as janelas filho MDI minimizadas.</span><span class="sxs-lookup"><span data-stu-id="734e4-105">An application sends the **WM\_MDIICONARRANGE** message to a multiple-document interface (MDI) client window to arrange all minimized MDI child windows.</span></span> <span data-ttu-id="734e4-106">Ele não afeta as janelas filhas que não são minimizadas.</span><span class="sxs-lookup"><span data-stu-id="734e4-106">It does not affect child windows that are not minimized.</span></span>


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a><span data-ttu-id="734e4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="734e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="734e4-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="734e4-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="734e4-109">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="734e4-109">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="734e4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="734e4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="734e4-111">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="734e4-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="734e4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="734e4-112">Requirements</span></span>



| <span data-ttu-id="734e4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="734e4-113">Requirement</span></span> | <span data-ttu-id="734e4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="734e4-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="734e4-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="734e4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="734e4-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="734e4-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="734e4-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="734e4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="734e4-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="734e4-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="734e4-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="734e4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="734e4-120"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="734e4-120"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="734e4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="734e4-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="734e4-122">**Referência**</span><span class="sxs-lookup"><span data-stu-id="734e4-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="734e4-123">**MDICASCADE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="734e4-123">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="734e4-124">**MDITILE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="734e4-124">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="734e4-125">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="734e4-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="734e4-126">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="734e4-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





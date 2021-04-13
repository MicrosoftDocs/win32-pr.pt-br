---
title: Mensagem de WM_UNINITMENUPOPUP (WinUser. h)
description: Enviado quando um menu suspenso ou submenu foi destruído.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499834"
---
# <a name="wm_uninitmenupopup-message"></a><span data-ttu-id="fe782-104">Mensagem do WM \_ UNINITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="fe782-104">WM\_UNINITMENUPOPUP message</span></span>

<span data-ttu-id="fe782-105">Enviado quando um menu suspenso ou submenu foi destruído.</span><span class="sxs-lookup"><span data-stu-id="fe782-105">Sent when a drop-down menu or submenu has been destroyed.</span></span>


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a><span data-ttu-id="fe782-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe782-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe782-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe782-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe782-108">Um identificador para o menu</span><span class="sxs-lookup"><span data-stu-id="fe782-108">A handle to the menu</span></span>

</dd> <dt>

<span data-ttu-id="fe782-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe782-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe782-110">A palavra de ordem superior identifica o menu que foi destruído.</span><span class="sxs-lookup"><span data-stu-id="fe782-110">The high-order word identifies the menu that was destroyed.</span></span> <span data-ttu-id="fe782-111">Atualmente, esse parâmetro só pode ser **MF \_ SYSMENU** (o menu janela).</span><span class="sxs-lookup"><span data-stu-id="fe782-111">Currently, this parameter can only be **MF\_SYSMENU** (the window menu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe782-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe782-112">Remarks</span></span>

<span data-ttu-id="fe782-113">Se um aplicativo receber uma mensagem do [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) , ele receberá uma mensagem do **WM \_ UNINITMENUPOPUP** .</span><span class="sxs-lookup"><span data-stu-id="fe782-113">If an application receives a [**WM\_INITMENUPOPUP**](wm-initmenupopup.md) message, it will receive a **WM\_UNINITMENUPOPUP** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe782-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe782-114">Requirements</span></span>



| <span data-ttu-id="fe782-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe782-115">Requirement</span></span> | <span data-ttu-id="fe782-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fe782-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe782-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe782-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fe782-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fe782-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fe782-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe782-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fe782-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fe782-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe782-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fe782-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe782-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe782-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe782-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe782-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe782-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="fe782-124">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="fe782-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe782-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fe782-126">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="fe782-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fe782-127">Menus</span><span class="sxs-lookup"><span data-stu-id="fe782-127">Menus</span></span>](menus.md)
</dt> </dl>

 


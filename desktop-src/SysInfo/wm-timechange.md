---
description: Uma mensagem que é enviada sempre que há uma alteração na hora do sistema.
ms.assetid: 94b5b6f7-04bb-4e0a-848b-e2b31ffc2938
title: Mensagem de WM_TIMECHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d43bb5cd4284813c45ab074a93a9cd9699883aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749431"
---
# <a name="wm_timechange-message"></a><span data-ttu-id="076ef-103">\_Mensagem de TIMEchange do WM</span><span class="sxs-lookup"><span data-stu-id="076ef-103">WM\_TIMECHANGE message</span></span>

<span data-ttu-id="076ef-104">Uma mensagem que é enviada sempre que há uma alteração na hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="076ef-104">A message that is sent whenever there is a change in the system time.</span></span>

<span data-ttu-id="076ef-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="076ef-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // message identifier
  WPARAM wParam,   // not used; must be zero
  LPARAM lParam    // not used; must be zero
);
```



## <a name="parameters"></a><span data-ttu-id="076ef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="076ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="076ef-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="076ef-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="076ef-108">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="076ef-108">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="076ef-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="076ef-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="076ef-110">**WM \_ Identificador de timechange** .</span><span class="sxs-lookup"><span data-stu-id="076ef-110">**WM\_TIMECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="076ef-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="076ef-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="076ef-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="076ef-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="076ef-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="076ef-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="076ef-114">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="076ef-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="076ef-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="076ef-115">Return value</span></span>

<span data-ttu-id="076ef-116">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="076ef-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="076ef-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="076ef-117">Remarks</span></span>

<span data-ttu-id="076ef-118">Um aplicativo não deve transmitir essa mensagem, pois o sistema transmitirá essa mensagem quando o aplicativo alterar a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="076ef-118">An application should not broadcast this message, because the system will broadcast this message when the application changes the system time.</span></span>

## <a name="requirements"></a><span data-ttu-id="076ef-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="076ef-119">Requirements</span></span>



| <span data-ttu-id="076ef-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="076ef-120">Requirement</span></span> | <span data-ttu-id="076ef-121">Valor</span><span class="sxs-lookup"><span data-stu-id="076ef-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="076ef-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="076ef-122">Minimum supported client</span></span><br/> | <span data-ttu-id="076ef-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="076ef-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="076ef-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="076ef-124">Minimum supported server</span></span><br/> | <span data-ttu-id="076ef-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="076ef-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="076ef-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="076ef-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="076ef-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="076ef-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="076ef-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="076ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="076ef-129">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="076ef-129">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 


---
description: Enviado por um aplicativo de treinamento baseado em computador (CBT) para separar mensagens de entrada de usuário de outras mensagens enviadas por meio do \_ procedimento JOURNALPLAYBACK do qu.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: Mensagem de WM_QUEUESYNC (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751530"
---
# <a name="wm_queuesync-message"></a><span data-ttu-id="24f75-103">Mensagem do WM \_ QUEUESYNC</span><span class="sxs-lookup"><span data-stu-id="24f75-103">WM\_QUEUESYNC message</span></span>

<span data-ttu-id="24f75-104">Enviado por um aplicativo de treinamento baseado em computador (CBT) para separar mensagens de entrada de usuário de outras mensagens enviadas por meio do procedimento [**\_ JOURNALPLAYBACK do qu**](about-hooks.md) .</span><span class="sxs-lookup"><span data-stu-id="24f75-104">Sent by a computer-based training (CBT) application to separate user-input messages from other messages sent through the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure.</span></span>


```C++
#define WM_QUEUESYNC                    0x0023
```



## <a name="parameters"></a><span data-ttu-id="24f75-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24f75-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f75-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24f75-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24f75-107">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="24f75-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="24f75-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24f75-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24f75-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="24f75-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f75-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24f75-110">Return value</span></span>

<span data-ttu-id="24f75-111">Tipo: **void**</span><span class="sxs-lookup"><span data-stu-id="24f75-111">Type: **void**</span></span>

<span data-ttu-id="24f75-112">Um aplicativo CBT deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="24f75-112">A CBT application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="24f75-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="24f75-113">Remarks</span></span>

<span data-ttu-id="24f75-114">Sempre que um aplicativo CBT usa o procedimento [**qu \_ JOURNALPLAYBACK**](about-hooks.md) , a primeira e a última mensagem são o **WM \_ QUEUESYNC**.</span><span class="sxs-lookup"><span data-stu-id="24f75-114">Whenever a CBT application uses the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure, the first and last messages are **WM\_QUEUESYNC**.</span></span> <span data-ttu-id="24f75-115">Isso permite que o aplicativo CBT intercepte e examine as mensagens iniciadas pelo usuário sem fazer isso para os eventos que ele envia.</span><span class="sxs-lookup"><span data-stu-id="24f75-115">This allows the CBT application to intercept and examine user-initiated messages without doing so for events that it sends.</span></span>

<span data-ttu-id="24f75-116">Se um aplicativo especificar um identificador de janela **nulo** , a mensagem será postada na fila de mensagens da janela ativa.</span><span class="sxs-lookup"><span data-stu-id="24f75-116">If an application specifies a **NULL** window handle, the message is posted to the message queue of the active window.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f75-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24f75-117">Requirements</span></span>



| <span data-ttu-id="24f75-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24f75-118">Requirement</span></span> | <span data-ttu-id="24f75-119">Valor</span><span class="sxs-lookup"><span data-stu-id="24f75-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24f75-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24f75-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24f75-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="24f75-121">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="24f75-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24f75-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24f75-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="24f75-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24f75-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="24f75-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="24f75-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24f75-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24f75-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="24f75-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="24f75-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="24f75-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="24f75-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24f75-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="24f75-129">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="24f75-129">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="24f75-130">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="24f75-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="24f75-131">Ganchos</span><span class="sxs-lookup"><span data-stu-id="24f75-131">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 

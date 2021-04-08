---
title: Mensagem de WM_GESTURENOTIFY (WinUser. h)
description: Oferece a oportunidade de definir a configuração do gesto.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY a mensagem Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085839"
---
# <a name="wm_gesturenotify-message"></a><span data-ttu-id="b696d-104">Mensagem do WM \_ GESTURENOTIFY</span><span class="sxs-lookup"><span data-stu-id="b696d-104">WM\_GESTURENOTIFY message</span></span>

<span data-ttu-id="b696d-105">Oferece a oportunidade de definir a configuração do gesto.</span><span class="sxs-lookup"><span data-stu-id="b696d-105">Gives you a chance to set the gesture configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="b696d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b696d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b696d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b696d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b696d-108">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="b696d-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="b696d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b696d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b696d-110">Um ponteiro para um [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span><span class="sxs-lookup"><span data-stu-id="b696d-110">A pointer to a [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b696d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b696d-111">Return value</span></span>

<span data-ttu-id="b696d-112">Um valor deve ser retornado de [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="b696d-112">A value should be returned from [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="b696d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b696d-113">Remarks</span></span>

<span data-ttu-id="b696d-114">Quando a **mensagem \_ GESTURENOTIFY do WM** é recebida, o aplicativo pode usar [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) para especificar os gestos a serem recebidos.</span><span class="sxs-lookup"><span data-stu-id="b696d-114">When the **WM\_GESTURENOTIFY** message is received, the application can use [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) to specify the gestures to receive.</span></span> <span data-ttu-id="b696d-115">Essa mensagem deve sempre ser consumida usando a função [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="b696d-115">This message should always be bubbled up using the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

> [!Note]  
> <span data-ttu-id="b696d-116">Manipular a mensagem do **WM \_ GESTURENOTIFY** alterará a configuração do gesto para o tempo de vida da janela, não apenas para o próximo gesto.</span><span class="sxs-lookup"><span data-stu-id="b696d-116">Handling the **WM\_GESTURENOTIFY** message will change the gesture configuration for the lifetime of the Window, not just for the next gesture.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b696d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b696d-117">Examples</span></span>

<span data-ttu-id="b696d-118">O exemplo a seguir mostra como habilitar todos os gestos.</span><span class="sxs-lookup"><span data-stu-id="b696d-118">The following example shows how to enable all gestures.</span></span> <span data-ttu-id="b696d-119">Para obter mais exemplos, consulte [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span><span class="sxs-lookup"><span data-stu-id="b696d-119">For more examples, see [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span></span>


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a><span data-ttu-id="b696d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b696d-120">Requirements</span></span>



| <span data-ttu-id="b696d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b696d-121">Requirement</span></span> | <span data-ttu-id="b696d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b696d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b696d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b696d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b696d-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b696d-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="b696d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b696d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b696d-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="b696d-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="b696d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b696d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b696d-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b696d-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b696d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b696d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b696d-130">Notificações</span><span class="sxs-lookup"><span data-stu-id="b696d-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b696d-131">Guia de programação de gestos do Windows Touch</span><span class="sxs-lookup"><span data-stu-id="b696d-131">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="b696d-132">**GESTURENOTIFYSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="b696d-132">**GESTURENOTIFYSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[<span data-ttu-id="b696d-133">**SetGestureConfig**</span><span class="sxs-lookup"><span data-stu-id="b696d-133">**SetGestureConfig**</span></span>](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 


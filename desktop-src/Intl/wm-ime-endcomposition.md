---
description: Enviado a um aplicativo quando o IME termina a composição. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: Mensagem de WM_IME_ENDCOMPOSITION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ca9d1560810b22ae0d36010d2371e75b83a81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296375"
---
# <a name="wm_ime_endcomposition-message"></a><span data-ttu-id="138c2-104">\_Mensagem de composição de endime do WM \_</span><span class="sxs-lookup"><span data-stu-id="138c2-104">WM\_IME\_ENDCOMPOSITION message</span></span>

<span data-ttu-id="138c2-105">Enviado a um aplicativo quando o IME termina a composição.</span><span class="sxs-lookup"><span data-stu-id="138c2-105">Sent to an application when the IME ends composition.</span></span> <span data-ttu-id="138c2-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="138c2-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
  WPARAM wParam,      
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="138c2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="138c2-107">Parameters</span></span>

<span data-ttu-id="138c2-108">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="138c2-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="138c2-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="138c2-109">Return value</span></span>

<span data-ttu-id="138c2-110">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="138c2-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="138c2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="138c2-111">Remarks</span></span>

<span data-ttu-id="138c2-112">Um aplicativo deve processar essa mensagem se exibir os próprios caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="138c2-112">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="138c2-113">Se o aplicativo tiver criado uma janela IME, ele deverá passar essa mensagem para essa janela.</span><span class="sxs-lookup"><span data-stu-id="138c2-113">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="138c2-114">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  processa essa mensagem passando-a para a janela padrão do IME.</span><span class="sxs-lookup"><span data-stu-id="138c2-114">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="138c2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="138c2-115">Requirements</span></span>



| <span data-ttu-id="138c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="138c2-116">Requirement</span></span> | <span data-ttu-id="138c2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="138c2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="138c2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="138c2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="138c2-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="138c2-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="138c2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="138c2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="138c2-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="138c2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="138c2-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="138c2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="138c2-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="138c2-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="138c2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="138c2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="138c2-125">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="138c2-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="138c2-126">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="138c2-126">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 

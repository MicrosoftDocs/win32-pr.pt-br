---
description: Enviado para a janela afetada na extremidade superior após a alteração do idioma de entrada de um aplicativo. Você deve fazer qualquer configuração específica do aplicativo e passar a mensagem para a função DefWindowProc, que passa a mensagem para todas as janelas filho de primeiro nível.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Mensagem de WM_INPUTLANGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090277"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="ac983-104">Mensagem do WM \_ INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="ac983-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="ac983-105">Enviado para a janela afetada na extremidade superior após a alteração do idioma de entrada de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac983-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="ac983-106">Você deve fazer qualquer configuração específica do aplicativo e passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , que passa a mensagem para todas as janelas filho de primeiro nível.</span><span class="sxs-lookup"><span data-stu-id="ac983-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="ac983-107">Essas janelas filhas podem passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que ela passe a mensagem para suas janelas filhas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ac983-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="ac983-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ac983-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a><span data-ttu-id="ac983-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac983-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac983-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac983-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac983-111">O conjunto de caracteres da nova localidade.</span><span class="sxs-lookup"><span data-stu-id="ac983-111">The character set of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="ac983-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac983-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac983-113">O identificador de localidade de entrada.</span><span class="sxs-lookup"><span data-stu-id="ac983-113">The input locale identifier.</span></span> <span data-ttu-id="ac983-114">Para obter mais informações, consulte [idiomas, localidades e layouts de teclado](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="ac983-114">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac983-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac983-115">Return value</span></span>

<span data-ttu-id="ac983-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ac983-116">Type: **LRESULT**</span></span>

<span data-ttu-id="ac983-117">Um aplicativo deve retornar diferente de zero se processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="ac983-117">An application should return nonzero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac983-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac983-118">Requirements</span></span>



| <span data-ttu-id="ac983-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac983-119">Requirement</span></span> | <span data-ttu-id="ac983-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ac983-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac983-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac983-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ac983-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ac983-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ac983-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac983-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ac983-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ac983-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ac983-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ac983-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac983-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac983-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac983-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac983-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ac983-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ac983-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ac983-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ac983-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="ac983-130">**INPUTLANGCHANGEREQUEST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ac983-130">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)
</dt> <dt>

<span data-ttu-id="ac983-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ac983-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ac983-132">Windows</span><span class="sxs-lookup"><span data-stu-id="ac983-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 

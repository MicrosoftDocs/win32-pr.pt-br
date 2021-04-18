---
title: WM_POINTERACTIVATE mensagem
description: Enviado a uma janela inativa quando um ponteiro principal gera uma WM_POINTERDOWN sobre a janela.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- Mensagens de entrada e notificações de WM_POINTERACTIVATE mensagem
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105816046"
---
# <a name="wm_pointeractivate-message"></a><span data-ttu-id="c7aed-104">WM_POINTERACTIVATE mensagem</span><span class="sxs-lookup"><span data-stu-id="c7aed-104">WM_POINTERACTIVATE message</span></span>

<span data-ttu-id="c7aed-105">Enviado a uma janela inativa quando um ponteiro principal gera uma [**WM_POINTERDOWN**](wm-pointerdown.md) sobre a janela.</span><span class="sxs-lookup"><span data-stu-id="c7aed-105">Sent to an inactive window when a primary pointer generates a [**WM_POINTERDOWN**](wm-pointerdown.md) over the window.</span></span> <span data-ttu-id="c7aed-106">Desde que a mensagem permaneça sem tratamento, ela viaja para a cadeia de janelas pai até atingir a janela de nível superior.</span><span class="sxs-lookup"><span data-stu-id="c7aed-106">As long as the message remains unhandled, it travels up the parent window chain until it is reaches the top-level window.</span></span> <span data-ttu-id="c7aed-107">Os aplicativos podem responder a essa mensagem para especificar se desejam ser ativados.</span><span class="sxs-lookup"><span data-stu-id="c7aed-107">Applications can respond to this message to specify whether they wish to be activated.</span></span>

<span data-ttu-id="c7aed-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c7aed-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a><span data-ttu-id="c7aed-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7aed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7aed-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7aed-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7aed-111">Contém o identificador de ponteiro e informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="c7aed-111">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="c7aed-112">Use as macros a seguir para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="c7aed-112">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="c7aed-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de ponteiro</span><span class="sxs-lookup"><span data-stu-id="c7aed-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="c7aed-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valor de teste de sucesso retornado pelo processamento da mensagem de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="c7aed-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="c7aed-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7aed-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7aed-116">Contém o identificador para a janela de nível superior da janela que está sendo ativada.</span><span class="sxs-lookup"><span data-stu-id="c7aed-116">Contains the handle to the top-level window of the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7aed-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7aed-117">Return value</span></span>

<span data-ttu-id="c7aed-118">Se um aplicativo processar essa mensagem, ele deverá retornar um dos valores descritos na seção comentários.</span><span class="sxs-lookup"><span data-stu-id="c7aed-118">If an application processes this message, it should return one of the values described in the Remarks section.</span></span>

<span data-ttu-id="c7aed-119">Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="c7aed-119">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7aed-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7aed-120">Remarks</span></span>

<span data-ttu-id="c7aed-121">Um aplicativo pode manipular essa mensagem e retornar um dos seguintes valores para determinar como o sistema processa a ativação e a entrada de ativação:</span><span class="sxs-lookup"><span data-stu-id="c7aed-121">An application can handle this message and return one of the following values to determine how the system processes the activation and the activating input:</span></span>

-   <span data-ttu-id="c7aed-122">PA_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="c7aed-122">PA_ACTIVATE</span></span>
-   <span data-ttu-id="c7aed-123">PA_NOACTIVATE</span><span class="sxs-lookup"><span data-stu-id="c7aed-123">PA_NOACTIVATE</span></span>

<span data-ttu-id="c7aed-124">É importante observar que, quando o usuário está interagindo com o sistema com vários ponteiros simultâneos, a oportunidade de ativação que a **WM_POINTERACTIVATE** mensagem representa está disponível para aplicativos somente para o primeiro desses ponteiros.</span><span class="sxs-lookup"><span data-stu-id="c7aed-124">It is important to note that, when the user is interacting with the system with multiple simultaneous pointers, the activation opportunity that the **WM_POINTERACTIVATE** message represents is available to applications only for the first of those pointers.</span></span> <span data-ttu-id="c7aed-125">Os aplicativos devem, portanto, estar cientes de que eles ainda podem receber entradas de ponteiros enquanto estiverem inativos.</span><span class="sxs-lookup"><span data-stu-id="c7aed-125">Applications should, therefore, be aware that they may still receive input from pointers while they are inactive.</span></span>

<span data-ttu-id="c7aed-126">Se o aplicativo não tratar essa mensagem, o [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passará a mensagem para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="c7aed-126">If the application does not handle this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passes the message to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7aed-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7aed-127">Requirements</span></span>



| <span data-ttu-id="c7aed-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7aed-128">Requirement</span></span> | <span data-ttu-id="c7aed-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c7aed-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7aed-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7aed-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c7aed-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c7aed-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="c7aed-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7aed-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c7aed-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c7aed-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7aed-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7aed-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7aed-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7aed-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7aed-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7aed-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7aed-137">Mensagens</span><span class="sxs-lookup"><span data-stu-id="c7aed-137">Messages</span></span>](messages.md)
</dt> </dl>

 


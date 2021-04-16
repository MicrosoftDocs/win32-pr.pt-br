---
description: Notifica um aplicativo quando um IME selecionado precisa de informações sobre a janela de composição. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação do IME do WM \_ com parâmetros definidos, conforme mostrado abaixo.
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: IMR_COMPOSITIONWINDOW código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752271"
---
# <a name="imr_compositionwindow-notification-code"></a><span data-ttu-id="0d827-104">Código de notificação do IMR \_ COMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="0d827-104">IMR\_COMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="0d827-105">Notifica um aplicativo quando um IME selecionado precisa de informações sobre a janela de composição.</span><span class="sxs-lookup"><span data-stu-id="0d827-105">Notifies an application when a selected IME needs information about the composition window.</span></span> <span data-ttu-id="0d827-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação do IME do WM**](wm-ime-request.md) com parâmetros definidos, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="0d827-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="0d827-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d827-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d827-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d827-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="0d827-109">Defina como IMR \_ COMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="0d827-109">Set to IMR\_COMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="0d827-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d827-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="0d827-111">Ponteiro para um buffer que contém uma estrutura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .</span><span class="sxs-lookup"><span data-stu-id="0d827-111">Pointer to a buffer containing a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d827-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0d827-112">Return Value</span></span>

<span data-ttu-id="0d827-113">Retorna um valor diferente de zero se o aplicativo preenche a estrutura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .</span><span class="sxs-lookup"><span data-stu-id="0d827-113">Returns a nonzero value if the application fills in the [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span> <span data-ttu-id="0d827-114">Caso contrário, o comando retornará 0.</span><span class="sxs-lookup"><span data-stu-id="0d827-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d827-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d827-115">Remarks</span></span>

<span data-ttu-id="0d827-116">Esse comando pode ser enviado pelo IME para uma janela que limpou o \_ sinalizador SHOWUICOMPOSITIONWINDOW da ISC no manipulador de mensagens [**\_ \_ SetContext do WM IME**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="0d827-116">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d827-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d827-117">Requirements</span></span>



| <span data-ttu-id="0d827-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d827-118">Requirement</span></span> | <span data-ttu-id="0d827-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0d827-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d827-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d827-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d827-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0d827-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0d827-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d827-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d827-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0d827-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0d827-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0d827-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d827-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d827-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d827-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d827-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d827-127">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="0d827-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="0d827-128">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="0d827-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="0d827-129">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="0d827-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="0d827-130">**\_solicitação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0d827-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="0d827-131">**SetContext IME do WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0d827-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 





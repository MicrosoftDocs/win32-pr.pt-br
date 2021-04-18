---
description: Notfies um aplicativo quando um IME selecionado precisa de informações sobre a janela candidata. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: IMR_CANDIDATEWINDOW código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758973"
---
# <a name="imr_candidatewindow-notification-code"></a><span data-ttu-id="24b10-104">Código de notificação do IMR \_ CANDIDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="24b10-104">IMR\_CANDIDATEWINDOW notification code</span></span>

<span data-ttu-id="24b10-105">Notfies um aplicativo quando um IME selecionado precisa de informações sobre a janela candidata.</span><span class="sxs-lookup"><span data-stu-id="24b10-105">Notfies an application when a selected IME needs information about the candidate window.</span></span> <span data-ttu-id="24b10-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação IME do WM**](wm-ime-request.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="24b10-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a><span data-ttu-id="24b10-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24b10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24b10-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="24b10-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="24b10-109">Defina como IMR \_ CANDIDATEWINDOW.</span><span class="sxs-lookup"><span data-stu-id="24b10-109">Set to IMR\_CANDIDATEWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="24b10-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="24b10-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="24b10-111">Ponteiro para um buffer que contém uma estrutura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) .</span><span class="sxs-lookup"><span data-stu-id="24b10-111">Pointer to a buffer containing a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="24b10-112">Seu membro **dwIndex** contém o índice para a janela candidata referenciada.</span><span class="sxs-lookup"><span data-stu-id="24b10-112">Its **dwIndex** member contains the index to the candidate window referenced.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24b10-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="24b10-113">Return Value</span></span>

<span data-ttu-id="24b10-114">Retorna um valor diferente de zero se o aplicativo preenche a estrutura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) .</span><span class="sxs-lookup"><span data-stu-id="24b10-114">Returns a nonzero value if the application fills in the [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="24b10-115">Caso contrário, o comando retornará 0.</span><span class="sxs-lookup"><span data-stu-id="24b10-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="24b10-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="24b10-116">Remarks</span></span>

<span data-ttu-id="24b10-117">Esse comando pode ser enviado pelo IME para uma janela que limpou o \_ sinalizador SHOWUICANDIDATEWINDOW da ISC no manipulador de mensagens [**\_ \_ SetContext do WM IME**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="24b10-117">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICANDIDATEWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="24b10-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24b10-118">Requirements</span></span>



| <span data-ttu-id="24b10-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b10-119">Requirement</span></span> | <span data-ttu-id="24b10-120">Valor</span><span class="sxs-lookup"><span data-stu-id="24b10-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b10-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24b10-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24b10-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="24b10-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="24b10-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24b10-123">Minimum supported server</span></span><br/> | <span data-ttu-id="24b10-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="24b10-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="24b10-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="24b10-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="24b10-126"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24b10-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b10-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="24b10-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b10-128">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="24b10-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="24b10-129">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="24b10-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="24b10-130">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="24b10-130">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="24b10-131">**\_solicitação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="24b10-131">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="24b10-132">**SetContext IME do WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="24b10-132">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 





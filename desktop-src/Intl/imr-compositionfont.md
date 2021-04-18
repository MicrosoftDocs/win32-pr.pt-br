---
description: Notifica um aplicativo quando um IME selecionado precisa de informações sobre a fonte usada pela janela de composição. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação do IME do WM \_ com parâmetros, conforme mostrado abaixo.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: IMR_COMPOSITIONFONT código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758791"
---
# <a name="imr_compositionfont-notification-code"></a><span data-ttu-id="3e9e9-104">Código de notificação do IMR \_ COMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="3e9e9-104">IMR\_COMPOSITIONFONT notification code</span></span>

<span data-ttu-id="3e9e9-105">Notifica um aplicativo quando um IME selecionado precisa de informações sobre a fonte usada pela janela de composição.</span><span class="sxs-lookup"><span data-stu-id="3e9e9-105">Notifies an application when a selected IME needs information about the font used by the composition window.</span></span> <span data-ttu-id="3e9e9-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação do IME do WM**](wm-ime-request.md) com parâmetros, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="3e9e9-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="3e9e9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e9e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e9e9-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e9e9-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="3e9e9-109">Defina como IMR \_ COMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="3e9e9-109">Set to IMR\_COMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="3e9e9-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e9e9-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3e9e9-111">Ponteiro para um buffer que contém uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="3e9e9-111">Pointer to a buffer containing a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="3e9e9-112">O aplicativo preenche os valores para a janela de composição atual.</span><span class="sxs-lookup"><span data-stu-id="3e9e9-112">The application fills in the values for the current composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e9e9-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3e9e9-113">Return Value</span></span>

<span data-ttu-id="3e9e9-114">Retorna um valor diferente de zero se o aplicativo preenche a estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="3e9e9-114">Returns a nonzero value if the application fills in the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="3e9e9-115">Caso contrário, o comando retornará 0.</span><span class="sxs-lookup"><span data-stu-id="3e9e9-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e9e9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e9e9-116">Remarks</span></span>

<span data-ttu-id="3e9e9-117">Esse comando pode ser enviado pelo IME para uma janela que desmarcou o \_ sinalizador SHOWUICOMPOSITIONWINDOW da ISC no manipulador de mensagens [**\_ \_ SetContext do WM IME**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="3e9e9-117">This command can be sent by the IME to a window that cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e9e9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e9e9-118">Requirements</span></span>



| <span data-ttu-id="3e9e9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e9e9-119">Requirement</span></span> | <span data-ttu-id="3e9e9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3e9e9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9e9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e9e9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3e9e9-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3e9e9-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3e9e9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e9e9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3e9e9-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3e9e9-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3e9e9-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3e9e9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e9e9-126"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e9-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e9e9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e9e9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9e9-128">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="3e9e9-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="3e9e9-129">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="3e9e9-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="3e9e9-130">**\_solicitação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3e9e9-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="3e9e9-131">**SetContext IME do WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e9e9-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 

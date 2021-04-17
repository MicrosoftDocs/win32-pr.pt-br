---
description: Notifica um aplicativo quando o IME selecionado precisa de informações sobre as coordenadas de um caractere na cadeia de caracteres de composição. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: IMR_QUERYCHARPOSITION código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759390"
---
# <a name="imr_querycharposition-notification-code"></a><span data-ttu-id="28333-104">Código de notificação do IMR \_ QUERYCHARPOSITION</span><span class="sxs-lookup"><span data-stu-id="28333-104">IMR\_QUERYCHARPOSITION notification code</span></span>

<span data-ttu-id="28333-105">Notifica um aplicativo quando o IME selecionado precisa de informações sobre as coordenadas de um caractere na cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="28333-105">Notifies an application when the selected IME needs information about the coordinates of a character in the composition string.</span></span> <span data-ttu-id="28333-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação IME do WM**](wm-ime-request.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="28333-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a><span data-ttu-id="28333-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28333-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28333-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="28333-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="28333-109">Defina como IMR \_ QUERYCHARPOSITION.</span><span class="sxs-lookup"><span data-stu-id="28333-109">Set to IMR\_QUERYCHARPOSITION.</span></span>

</dd> <dt>

<span data-ttu-id="28333-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="28333-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="28333-111">Ponteiro para uma estrutura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) que contém a posição do caractere na janela de composição.</span><span class="sxs-lookup"><span data-stu-id="28333-111">Pointer to an [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure that contains the position of the character in the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28333-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="28333-112">Return Value</span></span>

<span data-ttu-id="28333-113">Retorna um valor diferente de zero se o aplicativo preenche a estrutura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) .</span><span class="sxs-lookup"><span data-stu-id="28333-113">Returns a nonzero value if the application fills the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="28333-114">Caso contrário, o comando retornará 0.</span><span class="sxs-lookup"><span data-stu-id="28333-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="28333-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="28333-115">Remarks</span></span>

<span data-ttu-id="28333-116">Um aplicativo que desenha a própria cadeia de caracteres de composição, em vez de depender do IME, é responsável por preencher todos os membros da estrutura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) .</span><span class="sxs-lookup"><span data-stu-id="28333-116">An application that draws the composition string itself, instead of relying on the IME, is responsible for filling in all the members of the [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) structure.</span></span> <span data-ttu-id="28333-117">Caso contrário, o aplicativo deve passar o comando para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) se ele tiver sua própria janela de interface do usuário do IME.</span><span class="sxs-lookup"><span data-stu-id="28333-117">Otherwise, the application should pass the command to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) if it has its own IME user interface window.</span></span>

## <a name="requirements"></a><span data-ttu-id="28333-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28333-118">Requirements</span></span>



| <span data-ttu-id="28333-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="28333-119">Requirement</span></span> | <span data-ttu-id="28333-120">Valor</span><span class="sxs-lookup"><span data-stu-id="28333-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28333-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28333-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28333-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28333-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="28333-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28333-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28333-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28333-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="28333-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="28333-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="28333-126"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28333-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28333-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="28333-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28333-128">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="28333-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="28333-129">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="28333-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="28333-130">**IMECHARPOSITION**</span><span class="sxs-lookup"><span data-stu-id="28333-130">**IMECHARPOSITION**</span></span>](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[<span data-ttu-id="28333-131">**ImmIsUIMessage**</span><span class="sxs-lookup"><span data-stu-id="28333-131">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[<span data-ttu-id="28333-132">**\_solicitação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="28333-132">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 

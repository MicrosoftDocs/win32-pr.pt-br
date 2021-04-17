---
description: Instrui uma janela do IME para definir o estilo da janela de composição. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: Comando IMC_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789792"
---
# <a name="imc_setcompositionwindow-command"></a><span data-ttu-id="96833-104">\_Comando SETCOMPOSITIONWINDOW do IMC</span><span class="sxs-lookup"><span data-stu-id="96833-104">IMC\_SETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="96833-105">Instrui uma janela do IME para definir o estilo da janela de composição.</span><span class="sxs-lookup"><span data-stu-id="96833-105">Instructs an IME window to set the style of the composition window.</span></span> <span data-ttu-id="96833-106">Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="96833-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="96833-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96833-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96833-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="96833-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="96833-109">Defina como IMC \_ SETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="96833-109">Set to IMC\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="96833-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="96833-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="96833-111">Ponteiro para uma estrutura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) que contém as informações de estilo.</span><span class="sxs-lookup"><span data-stu-id="96833-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the style information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96833-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="96833-112">Return Value</span></span>

<span data-ttu-id="96833-113">Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="96833-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="96833-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="96833-114">Remarks</span></span>

<span data-ttu-id="96833-115">Esse comando define o estilo no contexto de entrada atual, e o estilo é aplicado posteriormente a cada janela do IME que recebe esse contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="96833-115">This command sets the style in the current input context, and the style is subsequently applied to each IME window that receives that input context.</span></span>

<span data-ttu-id="96833-116">Por padrão, a janela IME tem o \_ estilo de ponto CFS.</span><span class="sxs-lookup"><span data-stu-id="96833-116">By default, the IME window has the CFS\_POINT style.</span></span> <span data-ttu-id="96833-117">Com esse estilo, a janela do IME usa a posição atual do cursor e a área do cliente do Windows quando ele abre qualquer janela de composição.</span><span class="sxs-lookup"><span data-stu-id="96833-117">With this style, the IME window uses the current caret position and window client area when it opens any composition window.</span></span>

## <a name="requirements"></a><span data-ttu-id="96833-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96833-118">Requirements</span></span>



| <span data-ttu-id="96833-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="96833-119">Requirement</span></span> | <span data-ttu-id="96833-120">Valor</span><span class="sxs-lookup"><span data-stu-id="96833-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96833-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96833-121">Minimum supported client</span></span><br/> | <span data-ttu-id="96833-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96833-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="96833-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96833-123">Minimum supported server</span></span><br/> | <span data-ttu-id="96833-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96833-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="96833-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="96833-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="96833-126"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96833-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96833-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="96833-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96833-128">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="96833-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="96833-129">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="96833-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="96833-130">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="96833-130">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="96833-131">**\_controle IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="96833-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 





---
description: Instrui uma janela do IME para especificar a fonte lógica a ser usada para exibir os caracteres intermediários na janela de composição. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: Comando IMC_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb84c9e05ab19206064988a71b0ffc39b21a44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827291"
---
# <a name="imc_setcompositionfont-command"></a><span data-ttu-id="c569e-104">\_Comando SETCOMPOSITIONFONT do IMC</span><span class="sxs-lookup"><span data-stu-id="c569e-104">IMC\_SETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="c569e-105">Instrui uma janela do IME para especificar a fonte lógica a ser usada para exibir os caracteres intermediários na janela de composição.</span><span class="sxs-lookup"><span data-stu-id="c569e-105">Instructs an IME window to specify the logical font to use for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="c569e-106">Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="c569e-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="c569e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c569e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c569e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="c569e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="c569e-109">Defina como IMC \_ SETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="c569e-109">Set to IMC\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="c569e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="c569e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="c569e-111">Ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contém informações sobre a fonte lógica.</span><span class="sxs-lookup"><span data-stu-id="c569e-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c569e-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c569e-112">Return Value</span></span>

<span data-ttu-id="c569e-113">Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c569e-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c569e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c569e-114">Remarks</span></span>

<span data-ttu-id="c569e-115">Ao processar esse comando, a janela do IME altera a fonte selecionada atualmente no contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="c569e-115">When processing this command, the IME window changes the current selected font in the input context.</span></span>

## <a name="requirements"></a><span data-ttu-id="c569e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c569e-116">Requirements</span></span>



| <span data-ttu-id="c569e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c569e-117">Requirement</span></span> | <span data-ttu-id="c569e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c569e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c569e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c569e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c569e-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c569e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c569e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c569e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c569e-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c569e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c569e-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c569e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c569e-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c569e-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c569e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c569e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c569e-126">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="c569e-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="c569e-127">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="c569e-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="c569e-128">**\_controle IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c569e-128">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 

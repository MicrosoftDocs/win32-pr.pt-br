---
description: Instrui uma janela do IME para obter a posição da janela de composição. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: d2c60974-a602-4a42-8a45-870ee39df001
title: Comando IMC_GETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32b8f4414311d0727f622a1b552428cd31b0716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647360"
---
# <a name="imc_getcompositionwindow-command"></a><span data-ttu-id="8abb0-104">\_Comando GETCOMPOSITIONWINDOW do IMC</span><span class="sxs-lookup"><span data-stu-id="8abb0-104">IMC\_GETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="8abb0-105">Instrui uma janela do IME para obter a posição da janela de composição.</span><span class="sxs-lookup"><span data-stu-id="8abb0-105">Instructs an IME window to get the position of the composition window.</span></span> <span data-ttu-id="8abb0-106">Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="8abb0-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="8abb0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8abb0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8abb0-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="8abb0-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="8abb0-109">Defina como IMC \_ GETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="8abb0-109">Set to IMC\_GETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="8abb0-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8abb0-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8abb0-111">Ponteiro para uma estrutura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) que contém a posição da janela de composição.</span><span class="sxs-lookup"><span data-stu-id="8abb0-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the position of the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8abb0-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8abb0-112">Return Value</span></span>

<span data-ttu-id="8abb0-113">Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8abb0-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8abb0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8abb0-114">Remarks</span></span>

<span data-ttu-id="8abb0-115">Como o IME pode ajustar a posição de uma janela de composição, um aplicativo usa esse comando para obter a posição real para decidir se a janela deve ser reposicionada.</span><span class="sxs-lookup"><span data-stu-id="8abb0-115">Because the IME might adjust the position of a composition window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="8abb0-116">A posição recuperada está em coordenadas de janela em relação à janela que tem o foco de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="8abb0-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="8abb0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8abb0-117">Requirements</span></span>



| <span data-ttu-id="8abb0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8abb0-118">Requirement</span></span> | <span data-ttu-id="8abb0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8abb0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8abb0-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8abb0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8abb0-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8abb0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8abb0-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8abb0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8abb0-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8abb0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8abb0-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8abb0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8abb0-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8abb0-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8abb0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8abb0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8abb0-127">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="8abb0-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="8abb0-128">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="8abb0-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="8abb0-129">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="8abb0-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> </dl>

 

 





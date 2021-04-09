---
description: Instrui uma janela do IME para recuperar a fonte lógica usada para exibir os caracteres intermediários na janela de composição. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: Comando IMC_GETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164639"
---
# <a name="imc_getcompositionfont-command"></a><span data-ttu-id="3328f-104">\_Comando GETCOMPOSITIONFONT do IMC</span><span class="sxs-lookup"><span data-stu-id="3328f-104">IMC\_GETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="3328f-105">Instrui uma janela do IME para recuperar a fonte lógica usada para exibir os caracteres intermediários na janela de composição.</span><span class="sxs-lookup"><span data-stu-id="3328f-105">Instructs an IME window to retrieve the logical font used for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="3328f-106">Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="3328f-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="3328f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3328f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3328f-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="3328f-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="3328f-109">Defina como IMC \_ GETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="3328f-109">Set to IMC\_GETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="3328f-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3328f-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3328f-111">Ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que recebe informações sobre a fonte lógica.</span><span class="sxs-lookup"><span data-stu-id="3328f-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3328f-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3328f-112">Return Value</span></span>

<span data-ttu-id="3328f-113">Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3328f-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3328f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3328f-114">Requirements</span></span>



| <span data-ttu-id="3328f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3328f-115">Requirement</span></span> | <span data-ttu-id="3328f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3328f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3328f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3328f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3328f-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3328f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3328f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3328f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3328f-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3328f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3328f-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3328f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3328f-122"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3328f-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3328f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3328f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3328f-124">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="3328f-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="3328f-125">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="3328f-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 

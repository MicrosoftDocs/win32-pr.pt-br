---
description: Instrui a janela do IME para ocultar a janela de status. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: Comando IMC_CLOSESTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207f04d53f269318f87ed11038cbd6817d5e607e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837511"
---
# <a name="imc_closestatuswindow-command"></a><span data-ttu-id="dad5a-104">\_Comando CLOSESTATUSWINDOW do IMC</span><span class="sxs-lookup"><span data-stu-id="dad5a-104">IMC\_CLOSESTATUSWINDOW command</span></span>

<span data-ttu-id="dad5a-105">Instrui a janela do IME para ocultar a janela de status.</span><span class="sxs-lookup"><span data-stu-id="dad5a-105">Instructs the IME window to hide the status window.</span></span> <span data-ttu-id="dad5a-106">Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="dad5a-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="dad5a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dad5a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dad5a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="dad5a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="dad5a-109">Defina como IMC \_ CLOSESTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="dad5a-109">Set to IMC\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="dad5a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="dad5a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="dad5a-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="dad5a-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dad5a-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="dad5a-112">Return Value</span></span>

<span data-ttu-id="dad5a-113">Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="dad5a-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dad5a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dad5a-114">Remarks</span></span>

<span data-ttu-id="dad5a-115">Quando a janela de status do IME já estiver oculta, esse comando não fará nada.</span><span class="sxs-lookup"><span data-stu-id="dad5a-115">When the IME status window is already hidden, this command does nothing.</span></span> <span data-ttu-id="dad5a-116">Embora um aplicativo possa enviar esse comando para a janela do IME, o aplicativo não recebe o comando [IMN \_ CLOSESTATUSWINDOW](imn-closestatuswindow.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="dad5a-116">Although an application can send this command to the IME window, the application does not receive the corresponding [IMN\_CLOSESTATUSWINDOW](imn-closestatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad5a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dad5a-117">Requirements</span></span>



| <span data-ttu-id="dad5a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dad5a-118">Requirement</span></span> | <span data-ttu-id="dad5a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="dad5a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dad5a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dad5a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dad5a-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dad5a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dad5a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dad5a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dad5a-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dad5a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dad5a-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dad5a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dad5a-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dad5a-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dad5a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="dad5a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad5a-127">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="dad5a-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="dad5a-128">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="dad5a-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 





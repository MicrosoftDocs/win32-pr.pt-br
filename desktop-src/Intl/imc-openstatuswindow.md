---
description: Instrui a janela do IME para mostrar a janela de status. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: Comando IMC_OPENSTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd0b5e19ef6a026459eedb050e9ac9587b5ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827292"
---
# <a name="imc_openstatuswindow-command"></a><span data-ttu-id="3e181-104">\_Comando OPENSTATUSWINDOW do IMC</span><span class="sxs-lookup"><span data-stu-id="3e181-104">IMC\_OPENSTATUSWINDOW command</span></span>

<span data-ttu-id="3e181-105">Instrui a janela do IME para mostrar a janela de status.</span><span class="sxs-lookup"><span data-stu-id="3e181-105">Instructs the IME window to show the status window.</span></span> <span data-ttu-id="3e181-106">Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="3e181-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="3e181-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e181-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e181-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e181-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="3e181-109">Defina como IMC \_ OPENSTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="3e181-109">Set to IMC\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="3e181-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e181-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3e181-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="3e181-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e181-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3e181-112">Return Value</span></span>

<span data-ttu-id="3e181-113">Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3e181-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e181-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e181-114">Remarks</span></span>

<span data-ttu-id="3e181-115">Esse comando será ignorado se o sistema operacional não estiver no modo de exibição de status do IME.</span><span class="sxs-lookup"><span data-stu-id="3e181-115">This command is ignored if the operating system is not in the show IME status mode.</span></span> <span data-ttu-id="3e181-116">O usuário pode definir ou desmarcar o modo de exibição de status do IME na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="3e181-116">The user can set or clear the show IME status mode from the task bar.</span></span>

<span data-ttu-id="3e181-117">Se a janela de status já for mostrada, esse comando não fará nada.</span><span class="sxs-lookup"><span data-stu-id="3e181-117">If the status window is already shown, this command does nothing.</span></span> <span data-ttu-id="3e181-118">Embora o aplicativo possa enviar esse comando para a janela do IME, o aplicativo não recebe o comando [**IMN \_ OPENSTATUSWINDOW**](imn-openstatuswindow.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="3e181-118">Although the application can send this command to the IME window, the application does not receive the corresponding [**IMN\_OPENSTATUSWINDOW**](imn-openstatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e181-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e181-119">Requirements</span></span>



| <span data-ttu-id="3e181-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e181-120">Requirement</span></span> | <span data-ttu-id="3e181-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3e181-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e181-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e181-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3e181-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3e181-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3e181-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e181-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3e181-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3e181-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3e181-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3e181-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e181-127"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e181-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e181-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e181-129">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="3e181-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="3e181-130">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="3e181-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="3e181-131">**\_controle IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3e181-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 





---
description: Instrui uma janela do IME para obter a posição da janela de status. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: Comando IMC_GETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd17c5787d9ef8c787e62a556afa2f136bd65c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787095"
---
# <a name="imc_getstatuswindowpos-command"></a><span data-ttu-id="e7855-104">\_Comando GETSTATUSWINDOWPOS do IMC</span><span class="sxs-lookup"><span data-stu-id="e7855-104">IMC\_GETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="e7855-105">Instrui uma janela do IME para obter a posição da janela de status.</span><span class="sxs-lookup"><span data-stu-id="e7855-105">Instructs an IME window to get the position of the status window.</span></span> <span data-ttu-id="e7855-106">Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="e7855-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="e7855-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7855-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7855-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7855-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="e7855-109">Defina como IMC \_ GETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="e7855-109">Set to IMC\_GETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="e7855-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7855-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e7855-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="e7855-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7855-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e7855-112">Return Value</span></span>

<span data-ttu-id="e7855-113">Retorna uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém a coordenada x e a coordenada y da posição da janela de status em coordenadas de tela, em relação ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="e7855-113">Returns a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the status window position in screen coordinates, relative to the upper left corner of the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7855-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7855-114">Requirements</span></span>



| <span data-ttu-id="e7855-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7855-115">Requirement</span></span> | <span data-ttu-id="e7855-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e7855-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7855-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7855-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7855-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7855-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e7855-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7855-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7855-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7855-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e7855-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e7855-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7855-122"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7855-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7855-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7855-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7855-124">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e7855-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e7855-125">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e7855-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="e7855-126">**\_controle IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e7855-126">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 

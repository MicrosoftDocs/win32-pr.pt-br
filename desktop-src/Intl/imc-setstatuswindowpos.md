---
description: Instrui uma janela do IME para definir a posição da janela de status. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: Comando IMC_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010565"
---
# <a name="imc_setstatuswindowpos-command"></a><span data-ttu-id="42125-104">\_Comando SETSTATUSWINDOWPOS do IMC</span><span class="sxs-lookup"><span data-stu-id="42125-104">IMC\_SETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="42125-105">Instrui uma janela do IME para definir a posição da janela de status.</span><span class="sxs-lookup"><span data-stu-id="42125-105">Instructs an IME window to set the position of the status window.</span></span> <span data-ttu-id="42125-106">Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="42125-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="42125-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42125-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42125-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="42125-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="42125-109">Defina como IMC \_ SETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="42125-109">Set to IMC\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="42125-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="42125-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="42125-111">Ponteiro para uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém a coordenada x e a coordenada y da posição da janela de status.</span><span class="sxs-lookup"><span data-stu-id="42125-111">Pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the position of the status window.</span></span> <span data-ttu-id="42125-112">As coordenadas são em coordenadas de tela, em relação ao canto superior esquerdo da exibição.</span><span class="sxs-lookup"><span data-stu-id="42125-112">The coordinates are in screen coordinates, relative to the upper left corner of the display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42125-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="42125-113">Return Value</span></span>

<span data-ttu-id="42125-114">Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="42125-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="42125-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42125-115">Requirements</span></span>



| <span data-ttu-id="42125-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="42125-116">Requirement</span></span> | <span data-ttu-id="42125-117">Valor</span><span class="sxs-lookup"><span data-stu-id="42125-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42125-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42125-118">Minimum supported client</span></span><br/> | <span data-ttu-id="42125-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="42125-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="42125-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42125-120">Minimum supported server</span></span><br/> | <span data-ttu-id="42125-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="42125-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="42125-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="42125-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="42125-123"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42125-123"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42125-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="42125-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42125-125">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="42125-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="42125-126">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="42125-126">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="42125-127">**\_controle IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="42125-127">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 

---
description: Instrui uma janela do IME para obter a posição da janela candidata. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: Comando IMC_GETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb5cd143bf45f9bdb37be4cbe3078a483f53db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749813"
---
# <a name="imc_getcandidatepos-command"></a><span data-ttu-id="96153-104">\_Comando GETCANDIDATEPOS do IMC</span><span class="sxs-lookup"><span data-stu-id="96153-104">IMC\_GETCANDIDATEPOS command</span></span>

<span data-ttu-id="96153-105">Instrui uma janela do IME para obter a posição da janela candidata.</span><span class="sxs-lookup"><span data-stu-id="96153-105">Instructs an IME window to get the position of the candidate window.</span></span> <span data-ttu-id="96153-106">Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="96153-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="96153-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96153-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96153-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="96153-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="96153-109">Defina como IMC \_ GETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="96153-109">Set to IMC\_GETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="96153-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="96153-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="96153-111">Ponteiro para uma estrutura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) que contém a posição da janela candidata.</span><span class="sxs-lookup"><span data-stu-id="96153-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the position of the candidate window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96153-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="96153-112">Return Value</span></span>

<span data-ttu-id="96153-113">Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="96153-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="96153-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="96153-114">Remarks</span></span>

<span data-ttu-id="96153-115">Como o IME pode ajustar a posição de uma janela candidata, um aplicativo usa esse comando para obter a posição real para decidir se a janela deve ser reposicionada.</span><span class="sxs-lookup"><span data-stu-id="96153-115">Because the IME might adjust the position of a candidate window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="96153-116">A posição recuperada está em coordenadas de janela em relação à janela que tem o foco de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="96153-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="96153-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96153-117">Requirements</span></span>



| <span data-ttu-id="96153-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="96153-118">Requirement</span></span> | <span data-ttu-id="96153-119">Valor</span><span class="sxs-lookup"><span data-stu-id="96153-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96153-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96153-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96153-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96153-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="96153-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96153-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96153-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96153-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="96153-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="96153-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="96153-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96153-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96153-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="96153-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96153-127">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="96153-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="96153-128">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="96153-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="96153-129">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="96153-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 





---
description: Notifica um aplicativo quando o processamento de candidato foi concluído e o IME está prestes a mover a janela candidata. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: IMN_SETCANDIDATEPOS código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03171a76ce94572d2425f8e75f1cbe45b7efe4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747357"
---
# <a name="imn_setcandidatepos-notification-code"></a><span data-ttu-id="906c9-104">Código de notificação do IMN \_ SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="906c9-104">IMN\_SETCANDIDATEPOS notification code</span></span>

<span data-ttu-id="906c9-105">Notifica um aplicativo quando o processamento de candidato foi concluído e o IME está prestes a mover a janela candidata.</span><span class="sxs-lookup"><span data-stu-id="906c9-105">Notifies an application when candidate processing has finished and the IME is about to move the candidate window.</span></span> <span data-ttu-id="906c9-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="906c9-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="906c9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="906c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="906c9-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="906c9-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="906c9-109">Defina como IMN \_ SETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="906c9-109">Set to IMN\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="906c9-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="906c9-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="906c9-111">Sinalizador de lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="906c9-111">Candidate list flag.</span></span> <span data-ttu-id="906c9-112">Cada bit corresponde a uma lista de candidatos: bit 0 à primeira lista, bit 1 até o segundo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="906c9-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="906c9-113">Se um bit especificado for 1, a janela candidata correspondente estará prestes a ser movida.</span><span class="sxs-lookup"><span data-stu-id="906c9-113">If a specified bit is 1, the corresponding candidate window is about to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="906c9-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="906c9-114">Return Value</span></span>

<span data-ttu-id="906c9-115">Este comando não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="906c9-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="906c9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="906c9-116">Remarks</span></span>

<span data-ttu-id="906c9-117">Um aplicativo deve processar esse comando se ele exibir a própria janela candidata.</span><span class="sxs-lookup"><span data-stu-id="906c9-117">An application should process this command if it displays the candidate window itself.</span></span>

<span data-ttu-id="906c9-118">A janela do IME move a janela candidata ao processar esse comando.</span><span class="sxs-lookup"><span data-stu-id="906c9-118">The IME window moves the candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="906c9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="906c9-119">Requirements</span></span>



| <span data-ttu-id="906c9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="906c9-120">Requirement</span></span> | <span data-ttu-id="906c9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="906c9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="906c9-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="906c9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="906c9-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="906c9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="906c9-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="906c9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="906c9-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="906c9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="906c9-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="906c9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="906c9-127"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="906c9-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="906c9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="906c9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="906c9-129">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="906c9-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="906c9-130">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="906c9-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="906c9-131">**\_notificação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="906c9-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 





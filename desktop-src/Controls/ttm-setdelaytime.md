---
title: Mensagem de TTM_SETDELAYTIME (commctrl. h)
description: Define as durações inicial, pop-up e Reexibir para um controle ToolTip.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- Controles de TTM_SETDELAYTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918464"
---
# <a name="ttm_setdelaytime-message"></a><span data-ttu-id="7c06b-104">TTM de \_ mensagens</span><span class="sxs-lookup"><span data-stu-id="7c06b-104">TTM\_SETDELAYTIME message</span></span>

<span data-ttu-id="7c06b-105">Define as durações inicial, pop-up e Reexibir para um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="7c06b-105">Sets the initial, pop-up, and reshow durations for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c06b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c06b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c06b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c06b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c06b-108">Sinalizador que especifica qual valor de tempo definir.</span><span class="sxs-lookup"><span data-stu-id="7c06b-108">Flag that specifies which time value to set.</span></span> <span data-ttu-id="7c06b-109">Esse parâmetro pode ser um dos valores a seguir</span><span class="sxs-lookup"><span data-stu-id="7c06b-109">This parameter can be one of the following values</span></span>



| <span data-ttu-id="7c06b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7c06b-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="7c06b-111">Significado</span><span class="sxs-lookup"><span data-stu-id="7c06b-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="7c06b-112"><dt>**TTDT \_ AUTOPOP**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06b-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl>       | <span data-ttu-id="7c06b-113">Defina a quantidade de tempo que uma janela de dica de ferramenta permanecerá visível se o ponteiro for estático dentro do retângulo delimitador de uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="7c06b-113">Set the amount of time a tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span> <span data-ttu-id="7c06b-114">Para retornar o tempo de atraso Autopop ao valor padrão, defina *lParam* como-1.</span><span class="sxs-lookup"><span data-stu-id="7c06b-114">To return the autopop delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="7c06b-115"><dt>**TTDT \_ inicial**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06b-115"><dt>**TTDT\_INITIAL**</dt></span></span> </dl>       | <span data-ttu-id="7c06b-116">Defina a quantidade de tempo que um ponteiro deve permanecer fixo dentro do retângulo delimitador de uma ferramenta antes que a janela de dica de ferramentas seja exibida.</span><span class="sxs-lookup"><span data-stu-id="7c06b-116">Set the amount of time a pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span> <span data-ttu-id="7c06b-117">Para retornar o tempo de atraso inicial para seu valor padrão, defina *lParam* como-1.</span><span class="sxs-lookup"><span data-stu-id="7c06b-117">To return the initial delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="7c06b-118"><dt>**remostrar TTDT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06b-118"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>          | <span data-ttu-id="7c06b-119">Defina a quantidade de tempo que leva para que janelas de dica de ferramenta subsequentes apareçam à medida que o ponteiro se move de uma das ferramentas para outra.</span><span class="sxs-lookup"><span data-stu-id="7c06b-119">Set the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span> <span data-ttu-id="7c06b-120">Para retornar o tempo de atraso de reexibição para seu valor padrão, defina *lParam* como-1.</span><span class="sxs-lookup"><span data-stu-id="7c06b-120">To return the reshow delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <span data-ttu-id="7c06b-121"><dt>**TTDT \_ automático**</dt></span><span class="sxs-lookup"><span data-stu-id="7c06b-121"><dt>**TTDT\_AUTOMATIC**</dt></span></span> </dl> | <span data-ttu-id="7c06b-122">Defina todos os três tempos de atraso para as proporções padrão.</span><span class="sxs-lookup"><span data-stu-id="7c06b-122">Set all three delay times to default proportions.</span></span> <span data-ttu-id="7c06b-123">A hora de Autopop será dez vezes a hora inicial e o tempo de reapresentação será de uma quinta a hora inicial.</span><span class="sxs-lookup"><span data-stu-id="7c06b-123">The autopop time will be ten times the initial time and the reshow time will be one fifth the initial time.</span></span> <span data-ttu-id="7c06b-124">Se esse sinalizador estiver definido, use um valor positivo de *lParam* para especificar a hora inicial, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="7c06b-124">If this flag is set, use a positive value of *lParam* to specify the initial time, in milliseconds.</span></span> <span data-ttu-id="7c06b-125">Defina *lParam* como um valor negativo para retornar todos os três tempos de atraso para seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="7c06b-125">Set *lParam* to a negative value to return all three delay times to their default values.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7c06b-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c06b-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c06b-127">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o tempo de atraso, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="7c06b-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the delay time, in milliseconds.</span></span> <span data-ttu-id="7c06b-128">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7c06b-128">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c06b-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c06b-129">Return value</span></span>

<span data-ttu-id="7c06b-130">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="7c06b-130">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c06b-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c06b-131">Remarks</span></span>

<span data-ttu-id="7c06b-132">Os tempos de atraso padrão se baseiam no tempo de clique duplo.</span><span class="sxs-lookup"><span data-stu-id="7c06b-132">The default delay times are based on the double-click time.</span></span> <span data-ttu-id="7c06b-133">Para o tempo de clique duplo padrão de 500 MS, os tempos de atraso inicial, Autopop e reshow são 500 milhões, 5000ms e 100 ms, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7c06b-133">For the default double-click time of 500 ms, the initial, autopop, and reshow delay times are 500ms, 5000ms, and 100ms respectively.</span></span> <span data-ttu-id="7c06b-134">O fragmento de código a seguir usa a função [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) para determinar os três tempos de atraso para qualquer sistema.</span><span class="sxs-lookup"><span data-stu-id="7c06b-134">The following code fragment uses the [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) function to determine the three delay times for any system.</span></span>


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a><span data-ttu-id="7c06b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c06b-135">Requirements</span></span>



| <span data-ttu-id="7c06b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c06b-136">Requirement</span></span> | <span data-ttu-id="7c06b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="7c06b-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c06b-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c06b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7c06b-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c06b-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c06b-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c06b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7c06b-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c06b-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c06b-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c06b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c06b-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c06b-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c06b-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c06b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c06b-145">**TTM \_ GETdelaytime**</span><span class="sxs-lookup"><span data-stu-id="7c06b-145">**TTM\_GETDELAYTIME**</span></span>](ttm-getdelaytime.md)
</dt> </dl>

 


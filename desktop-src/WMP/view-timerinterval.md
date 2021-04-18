---
title: VIEW. IntervaloDoCronômetro
description: O atributo IntervaloDoCronômetro especifica ou recupera o intervalo, em milissegundos, no qual o temporizador dispara eventos para o manipulador de eventos OnTimer.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- VIEW. IntervaloDoCronômetro Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780361"
---
# <a name="viewtimerinterval"></a><span data-ttu-id="2ecb6-104">VIEW. IntervaloDoCronômetro</span><span class="sxs-lookup"><span data-stu-id="2ecb6-104">VIEW.timerInterval</span></span>

<span data-ttu-id="2ecb6-105">O atributo **IntervaloDoCronômetro** especifica ou recupera o intervalo, em milissegundos, no qual o temporizador dispara eventos para o manipulador de eventos **OnTimer** .</span><span class="sxs-lookup"><span data-stu-id="2ecb6-105">The **timerInterval** attribute specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span>

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a><span data-ttu-id="2ecb6-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="2ecb6-106">Possible Values</span></span>

<span data-ttu-id="2ecb6-107">Esse atributo é um **número** de leitura/gravação (**longo**) com um valor padrão de 1000.</span><span class="sxs-lookup"><span data-stu-id="2ecb6-107">This attribute is a read/write **Number** (**long**) with a default value of 1000.</span></span>



| <span data-ttu-id="2ecb6-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2ecb6-108">Value</span></span>        | <span data-ttu-id="2ecb6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ecb6-109">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="2ecb6-110">0</span><span class="sxs-lookup"><span data-stu-id="2ecb6-110">0</span></span>            | <span data-ttu-id="2ecb6-111">O evento de timer não é acionado.</span><span class="sxs-lookup"><span data-stu-id="2ecb6-111">The timer event does not fire.</span></span> |
| <span data-ttu-id="2ecb6-112">50 e acima</span><span class="sxs-lookup"><span data-stu-id="2ecb6-112">50 and above</span></span> | <span data-ttu-id="2ecb6-113">O intervalo em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="2ecb6-113">The interval in milliseconds.</span></span>  |



 

<span data-ttu-id="2ecb6-114">Qualquer valor abaixo de 50 (incluindo números negativos, mas não incluindo zero) gera um erro e o valor anterior é mantido.</span><span class="sxs-lookup"><span data-stu-id="2ecb6-114">Any value below 50 (including negative numbers, but not including zero) generates an error and the previous value is maintained.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ecb6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ecb6-115">Remarks</span></span>

<span data-ttu-id="2ecb6-116">Isso não será acionado automaticamente se nenhum manipulador de eventos **OnTimer** for implementado.</span><span class="sxs-lookup"><span data-stu-id="2ecb6-116">This will not fire automatically if no **ontimer** event handler is implemented.</span></span> <span data-ttu-id="2ecb6-117">Portanto, não há degradação de desempenho, embora o valor padrão seja diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="2ecb6-117">Thus there is no performance degradation even though the default value is nonzero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ecb6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ecb6-118">Requirements</span></span>



| <span data-ttu-id="2ecb6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ecb6-119">Requirement</span></span> | <span data-ttu-id="2ecb6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2ecb6-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2ecb6-121">Versão</span><span class="sxs-lookup"><span data-stu-id="2ecb6-121">Version</span></span><br/> | <span data-ttu-id="2ecb6-122">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="2ecb6-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ecb6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ecb6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ecb6-124">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="2ecb6-124">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="2ecb6-125">**Exibir. OnTimer**</span><span class="sxs-lookup"><span data-stu-id="2ecb6-125">**VIEW.ontimer**</span></span>](view-ontimer.md)
</dt> </dl>

 

 






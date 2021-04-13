---
description: O método setatrasartime define o tempo de atraso para a dica de ferramenta associada ao objeto MSWebDVD.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456341"
---
# <a name="setdelaytime"></a><span data-ttu-id="f375a-103">SetDelayTime</span><span class="sxs-lookup"><span data-stu-id="f375a-103">SetDelayTime</span></span>

> [!Note]  
> <span data-ttu-id="f375a-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f375a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f375a-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f375a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f375a-106">O `SetDelayTime` método define o tempo de atraso para a dica de ferramenta associada ao objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="f375a-106">The `SetDelayTime` method sets the delay time for the ToolTip associated with the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a><span data-ttu-id="f375a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f375a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f375a-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span><span class="sxs-lookup"><span data-stu-id="f375a-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span></span>
</dt> <dd>

<span data-ttu-id="f375a-109">Especifica o tipo de atraso como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="f375a-109">Specifies the type of delay as an Integer.</span></span>



| <span data-ttu-id="f375a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f375a-110">Value</span></span> | <span data-ttu-id="f375a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f375a-111">Description</span></span>                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f375a-112">-1</span><span class="sxs-lookup"><span data-stu-id="f375a-112">-1</span></span>    | <span data-ttu-id="f375a-113">Para redefinir o tempo de atraso Autopop para o valor padrão, defina *iNewVal* como-1.</span><span class="sxs-lookup"><span data-stu-id="f375a-113">To reset the autopop delay time to its default value, set *iNewVal* to -1.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="f375a-114">0</span><span class="sxs-lookup"><span data-stu-id="f375a-114">0</span></span>     | <span data-ttu-id="f375a-115">Defina o período de tempo que uma janela de dica de ferramenta permanecerá visível se o ponteiro for estático dentro do retângulo delimitador de uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="f375a-115">Set the length of time a ToolTip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span>                                                                                                                         |
| <span data-ttu-id="f375a-116">1</span><span class="sxs-lookup"><span data-stu-id="f375a-116">1</span></span>     | <span data-ttu-id="f375a-117">Defina o período de tempo que um ponteiro deve permanecer fixo dentro do retângulo delimitador de uma ferramenta antes que a janela de dica de ferramentas seja exibida.</span><span class="sxs-lookup"><span data-stu-id="f375a-117">Set the length of time a pointer must remain stationary within a tool's bounding rectangle before the ToolTip window appears.</span></span>                                                                                                                    |
| <span data-ttu-id="f375a-118">2</span><span class="sxs-lookup"><span data-stu-id="f375a-118">2</span></span>     | <span data-ttu-id="f375a-119">Defina o período de tempo que leva para que janelas de dica de ferramenta subsequentes apareçam quando o ponteiro se mover de uma das ferramentas para outra.</span><span class="sxs-lookup"><span data-stu-id="f375a-119">Set the length of time it takes for subsequent ToolTip windows to appear as the pointer moves from one tool to another.</span></span>                                                                                                                          |
| <span data-ttu-id="f375a-120">3</span><span class="sxs-lookup"><span data-stu-id="f375a-120">3</span></span>     | <span data-ttu-id="f375a-121">Defina todos os tempos de atraso para as proporções padrão.</span><span class="sxs-lookup"><span data-stu-id="f375a-121">Set all delay times to default proportions.</span></span> <span data-ttu-id="f375a-122">A hora de Autopop é dez vezes a hora inicial e o tempo de reapresentação é um quinto da hora inicial.</span><span class="sxs-lookup"><span data-stu-id="f375a-122">The autopop time is ten times the initial time and the reshow time is one-fifth the initial time.</span></span> <span data-ttu-id="f375a-123">Se esse sinalizador estiver definido, use um valor positivo de iNewVal para especificar a hora inicial, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="f375a-123">If this flag is set, use a positive value of iNewVal to specify the initial time, in milliseconds.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f375a-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span><span class="sxs-lookup"><span data-stu-id="f375a-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span></span>
</dt> <dd>

<span data-ttu-id="f375a-125">Especifica o atraso, em milissegundos, como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="f375a-125">Specifies the delay, in milliseconds, as an Integer.</span></span>



| <span data-ttu-id="f375a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f375a-126">Value</span></span>                    | <span data-ttu-id="f375a-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="f375a-127">Description</span></span>                                                   |
|--------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f375a-128">-1</span><span class="sxs-lookup"><span data-stu-id="f375a-128">-1</span></span>                       | <span data-ttu-id="f375a-129">Define o atraso especificado em *iDelayType* para seu valor padrão</span><span class="sxs-lookup"><span data-stu-id="f375a-129">Sets the delay specified in *iDelayType* to its default value</span></span> |
| <span data-ttu-id="f375a-130">qualquer outro valor negativo</span><span class="sxs-lookup"><span data-stu-id="f375a-130">any other negative value</span></span> | <span data-ttu-id="f375a-131">Define todos os tipos de atraso para o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="f375a-131">Sets all delay types to their default value.</span></span>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f375a-132">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f375a-132">Return Value</span></span>

<span data-ttu-id="f375a-133">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f375a-133">No return value.</span></span>

 

 




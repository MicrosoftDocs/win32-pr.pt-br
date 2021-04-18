---
title: Valor de enumeração D1115 inválido
description: Valor de enumeração D1115 inválido
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- O valor de enumeração D1115 não é válido Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105752369"
---
# <a name="d1115-enumeration-value-not-valid"></a><span data-ttu-id="0c667-104">D1115: valor de enumeração inválido</span><span class="sxs-lookup"><span data-stu-id="0c667-104">D1115: Enumeration Value Not Valid</span></span>

<span data-ttu-id="0c667-105">O parâmetro de parâmetro \[  \] com \[ *valor* \] de valor para *interface*::*Method* não é um valor de enumeração válido.</span><span class="sxs-lookup"><span data-stu-id="0c667-105">The parameter \[*parameter*\] with value \[*value*\] for *interface*::*method* is not a valid enumeration value.</span></span>

## <a name="placeholders"></a><span data-ttu-id="0c667-106">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="0c667-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="0c667-107"><span id="parameter"></span><span id="PARAMETER"></span>*meter*</span><span class="sxs-lookup"><span data-stu-id="0c667-107"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="0c667-108">O nome do parâmetro que recebeu o tipo inesperado.</span><span class="sxs-lookup"><span data-stu-id="0c667-108">The name of the parameter that received the unexpected type.</span></span>

</dd> <dt>

<span data-ttu-id="0c667-109"><span id="value"></span><span id="VALUE"></span>*valor*</span><span class="sxs-lookup"><span data-stu-id="0c667-109"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="0c667-110">O valor de enumeração inválido.</span><span class="sxs-lookup"><span data-stu-id="0c667-110">The invalid enumeration value.</span></span>

</dd> <dt>

<span data-ttu-id="0c667-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="0c667-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="0c667-112">O nome da interface à qual o *método* pertence.</span><span class="sxs-lookup"><span data-stu-id="0c667-112">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="0c667-113"><span id="method"></span><span id="METHOD"></span>*forma*</span><span class="sxs-lookup"><span data-stu-id="0c667-113"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="0c667-114">O nome do método que recebeu o valor de enumeração inválido.</span><span class="sxs-lookup"><span data-stu-id="0c667-114">The name of the method that received the invalid enumeration value.</span></span>

</dd> </dl> 




 

## <a name="examples"></a><span data-ttu-id="0c667-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c667-115">Examples</span></span>

<span data-ttu-id="0c667-116">O exemplo a seguir especifica um valor de enumeração de [**\_ tipo de \_ destino \_ de renderização d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) de 30, que está fora do intervalo esperado.</span><span class="sxs-lookup"><span data-stu-id="0c667-116">The following example specifies a [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) enumeration value of 30, which is outside the expected range.</span></span>


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



<span data-ttu-id="0c667-117">Este exemplo produz a seguinte mensagem de depuração:</span><span class="sxs-lookup"><span data-stu-id="0c667-117">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a><span data-ttu-id="0c667-118">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="0c667-118">Possible Causes</span></span>

<span data-ttu-id="0c667-119">Um parâmetro usou um valor de enumeração inválido.</span><span class="sxs-lookup"><span data-stu-id="0c667-119">A parameter used an invalid enumeration value.</span></span>

## <a name="fixes"></a><span data-ttu-id="0c667-120">Correções</span><span class="sxs-lookup"><span data-stu-id="0c667-120">Fixes</span></span>

<span data-ttu-id="0c667-121">Use um valor de enumeração válido.</span><span class="sxs-lookup"><span data-stu-id="0c667-121">Use a valid enumeration value.</span></span>

> [!Note]  
> <span data-ttu-id="0c667-122">A camada de depuração atualmente verifica apenas os valores individuais de enumeração; Ele não verifica se uma combinação bit-de-bits é válida.</span><span class="sxs-lookup"><span data-stu-id="0c667-122">The debug layer currently checks only the individual enumeration values; it does not check whether a bitwise combination is valid.</span></span>

 

 

 

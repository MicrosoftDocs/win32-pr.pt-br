---
title: D1114 de ponteiro nulo não opcional
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: 'O parâmetro do método interface:: não é opcional. Um ponteiro nulo foi passado. Isso fará com que o Direct2D falhe.'
keywords:
- D1114 Direct2D nula de ponteiro não opcional
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105751946"
---
# <a name="d1114-non-optional-pointer-null"></a><span data-ttu-id="24b7f-106">D1114: ponteiro não opcional nulo</span><span class="sxs-lookup"><span data-stu-id="24b7f-106">D1114: Non Optional Pointer NULL</span></span>

<span data-ttu-id="24b7f-107">O \[ *parâmetro* \] de parâmetro para o *método* *interface*:: não é opcional.</span><span class="sxs-lookup"><span data-stu-id="24b7f-107">The parameter \[*parameter*\] for *interface*::*method* is not optional.</span></span> <span data-ttu-id="24b7f-108">Um ponteiro **nulo** foi passado.</span><span class="sxs-lookup"><span data-stu-id="24b7f-108">A **NULL** pointer was passed.</span></span> <span data-ttu-id="24b7f-109">Isso fará com que o Direct2D falhe.</span><span class="sxs-lookup"><span data-stu-id="24b7f-109">This will cause Direct2D to crash.</span></span>

### <a name="placeholders"></a><span data-ttu-id="24b7f-110">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="24b7f-110">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="24b7f-111"><span id="parameter"></span><span id="PARAMETER"></span>*meter*</span><span class="sxs-lookup"><span data-stu-id="24b7f-111"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="24b7f-112">O nome do parâmetro que contém o ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="24b7f-112">The name of the parameter that contains the **NULL** pointer.</span></span>

</dd> <dt>

<span data-ttu-id="24b7f-113"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="24b7f-113"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="24b7f-114">O nome da interface à qual o *método* pertence.</span><span class="sxs-lookup"><span data-stu-id="24b7f-114">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="24b7f-115"><span id="method"></span><span id="METHOD"></span>*forma*</span><span class="sxs-lookup"><span data-stu-id="24b7f-115"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="24b7f-116">O nome do método que recebeu o parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="24b7f-116">The name of the method that received the invalid parameter.</span></span>

</dd> </dl> 




 

### <a name="examples"></a><span data-ttu-id="24b7f-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="24b7f-117">Examples</span></span>

<span data-ttu-id="24b7f-118">O exemplo a seguir mostra que o método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) recebe um ponteiro nulo para o parâmetro *Geometry* não opcional.</span><span class="sxs-lookup"><span data-stu-id="24b7f-118">The following example shows that the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method receives a NULL pointer for the non-optional *geometry* parameter.</span></span>


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



<span data-ttu-id="24b7f-119">Este exemplo produz a seguinte mensagem de depuração:</span><span class="sxs-lookup"><span data-stu-id="24b7f-119">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a><span data-ttu-id="24b7f-120">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="24b7f-120">Possible Causes</span></span>

<span data-ttu-id="24b7f-121">Um ponteiro nulo foi passado para um parâmetro não opcional.</span><span class="sxs-lookup"><span data-stu-id="24b7f-121">A NULL pointer was passed for a non-optional parameter.</span></span>

## <a name="fixes"></a><span data-ttu-id="24b7f-122">Correções</span><span class="sxs-lookup"><span data-stu-id="24b7f-122">Fixes</span></span>

<span data-ttu-id="24b7f-123">Certifique-se de que um parâmetro não opcional não tenha um ponteiro nulo.</span><span class="sxs-lookup"><span data-stu-id="24b7f-123">Ensure that a non-optional parameter does not have a NULL pointer.</span></span>

 

 

---
title: O recurso D1106 é do tipo incorreto
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: O recurso fornecido não é de um tipo esperado.
keywords:
- O recurso D1106 está errado no tipo Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105747673"
---
# <a name="d1106-resource-is-wrong-type"></a><span data-ttu-id="f73c4-104">D1106: tipo de recurso incorreto</span><span class="sxs-lookup"><span data-stu-id="f73c4-104">D1106: Resource Is Wrong Type</span></span>

<span data-ttu-id="f73c4-105">O recurso de recurso fornecido \[  \] não é de um tipo esperado.</span><span class="sxs-lookup"><span data-stu-id="f73c4-105">The given resource \[*resource*\] is not of an expected type.</span></span>

## <a name="placeholders"></a><span data-ttu-id="f73c4-106">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="f73c4-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="f73c4-107"><span id="resource"></span><span id="RESOURCE"></span>*Kit*</span><span class="sxs-lookup"><span data-stu-id="f73c4-107"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="f73c4-108">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="f73c4-108">The address of the resource.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="f73c4-109">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="f73c4-109">Possible Causes</span></span>

<span data-ttu-id="f73c4-110">Uma interface foi convertida de forma inadequada e usada como parâmetro para um método ou função.</span><span class="sxs-lookup"><span data-stu-id="f73c4-110">An interface was improperly cast and used as a parameter for a method or function.</span></span>

## <a name="examples"></a><span data-ttu-id="f73c4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f73c4-111">Examples</span></span>

<span data-ttu-id="f73c4-112">O exemplo a seguir passa um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) quando um [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) é esperado.</span><span class="sxs-lookup"><span data-stu-id="f73c4-112">The following example passes an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) when an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) is expected.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



<span data-ttu-id="f73c4-113">Este exemplo produz a seguinte mensagem de depuração:</span><span class="sxs-lookup"><span data-stu-id="f73c4-113">This example produces the following debug message:</span></span>

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a><span data-ttu-id="f73c4-114">Correções</span><span class="sxs-lookup"><span data-stu-id="f73c4-114">Fixes</span></span>

<span data-ttu-id="f73c4-115">Use o tipo exigido pelo método.</span><span class="sxs-lookup"><span data-stu-id="f73c4-115">Use the type required by the method.</span></span>

 

 

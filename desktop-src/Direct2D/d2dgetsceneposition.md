---
title: Função D2DGetScenePosition (D2d1effecthelpers. h)
description: Retorna o valor da posição da cena de entrada \_ . Disponível somente quando D2D \_ requer \_ que \_ a posição da cena seja declarada no arquivo de origem.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- Direct2D da função D2DGetScenePosition
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756405"
---
# <a name="d2dgetsceneposition-function"></a><span data-ttu-id="dfc7c-105">Função D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="dfc7c-105">D2DGetScenePosition function</span></span>

<span data-ttu-id="dfc7c-106">Retorna o valor da posição da cena de entrada \_ .</span><span class="sxs-lookup"><span data-stu-id="dfc7c-106">Returns the value of the input SCENE\_POSITION.</span></span> <span data-ttu-id="dfc7c-107">Disponível somente quando D2D \_ requer \_ que \_ a posição da cena seja declarada no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="dfc7c-107">Only available when D2D\_REQUIRES\_SCENE\_POSITION is declared in the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc7c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfc7c-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a><span data-ttu-id="dfc7c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfc7c-109">Parameters</span></span>

<span data-ttu-id="dfc7c-110">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dfc7c-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfc7c-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dfc7c-111">Return value</span></span>

<span data-ttu-id="dfc7c-112">A função retorna um **FLOAT4** no formato posição da cena \_ .</span><span class="sxs-lookup"><span data-stu-id="dfc7c-112">The function returns a **float4** in the format SCENE\_POSITION.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfc7c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfc7c-113">Remarks</span></span>

<span data-ttu-id="dfc7c-114">O exemplo a seguir mostra o uso da função na geração de um padrão de dissolução.</span><span class="sxs-lookup"><span data-stu-id="dfc7c-114">The following example shows the use of the function in generating a dissolve pattern.</span></span>

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
}  
```

## <a name="requirements"></a><span data-ttu-id="dfc7c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfc7c-115">Requirements</span></span>



| <span data-ttu-id="dfc7c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfc7c-116">Requirement</span></span> | <span data-ttu-id="dfc7c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dfc7c-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfc7c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfc7c-118">Header</span></span><br/> | <dl> <span data-ttu-id="dfc7c-119"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="dfc7c-119"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="dfc7c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="dfc7c-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="dfc7c-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfc7c-121"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="dfc7c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfc7c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc7c-123">Vinculação de Sombreador de Efeito</span><span class="sxs-lookup"><span data-stu-id="dfc7c-123">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="dfc7c-124">Auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="dfc7c-124">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 






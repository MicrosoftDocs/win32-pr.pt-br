---
title: Função D2DSampleInputAtPosition (D2d1effecthelpers. h)
description: A entrada de exemplos N é uma posição de cena absoluta, em vez de uma posição relativa à entrada. Disponível somente para entradas complexas.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- Direct2D da função D2DSampleInputAtPosition
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759512"
---
# <a name="d2dsampleinputatposition-function"></a><span data-ttu-id="c5ed9-105">Função D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="c5ed9-105">D2DSampleInputAtPosition function</span></span>

<span data-ttu-id="c5ed9-106">A entrada de exemplos N é uma posição de cena absoluta, em vez de uma posição relativa à entrada.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-106">Samples input N at an absolute scene position, rather than an input-relative position.</span></span> <span data-ttu-id="c5ed9-107">Disponível somente para entradas complexas.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ed9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5ed9-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="c5ed9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5ed9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ed9-110">*N* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c5ed9-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ed9-111">O número de entrada.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="c5ed9-112">*UV* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5ed9-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ed9-113">A posição UV.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ed9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5ed9-114">Return value</span></span>

<span data-ttu-id="c5ed9-115">A função retorna um **FLOAT4**, no formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ed9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5ed9-116">Remarks</span></span>

<span data-ttu-id="c5ed9-117">O exemplo a seguir mostra a função usada em um encapsulamento circular.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-117">The following example shows the function used in a circular wrap.</span></span>

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
}
```

## <a name="requirements"></a><span data-ttu-id="c5ed9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5ed9-118">Requirements</span></span>



| <span data-ttu-id="c5ed9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ed9-119">Requirement</span></span> | <span data-ttu-id="c5ed9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c5ed9-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ed9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5ed9-121">Header</span></span><br/> | <dl> <span data-ttu-id="c5ed9-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="c5ed9-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="c5ed9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c5ed9-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="c5ed9-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5ed9-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="c5ed9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5ed9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ed9-126">Vinculação de Sombreador de Efeito</span><span class="sxs-lookup"><span data-stu-id="c5ed9-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="c5ed9-127">Auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="c5ed9-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 






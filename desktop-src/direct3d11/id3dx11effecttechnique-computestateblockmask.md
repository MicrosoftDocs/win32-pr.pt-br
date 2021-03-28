---
title: Método ID3DX11EffectTechnique ComputeStateBlockMask (D3dx11effect. h)
description: Compute uma máscara de bloco de estado para permitir/impedir alterações de estado.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- Método ComputeStateBlockMask Direct3D 11
- Método ComputeStateBlockMask Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, método ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d15a159c15f35d530559b4ad6d84dd815e5964a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172947"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a><span data-ttu-id="9b357-106">Método ID3DX11EffectTechnique:: ComputeStateBlockMask</span><span class="sxs-lookup"><span data-stu-id="9b357-106">ID3DX11EffectTechnique::ComputeStateBlockMask method</span></span>

<span data-ttu-id="9b357-107">Compute uma máscara de bloco de estado para permitir/impedir alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="9b357-107">Compute a state-block mask to allow/prevent state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b357-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b357-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="9b357-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b357-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b357-110">*pStateBlockMask*</span><span class="sxs-lookup"><span data-stu-id="9b357-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="9b357-111">Tipo: **[ **\_ máscara de \_ bloco \_ de estado D3DX11**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b357-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="9b357-112">Um ponteiro para uma máscara de bloco de estado ( [**consulte \_ \_ \_ máscara de bloco de estado D3DX11**](d3dx11-state-block-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="9b357-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b357-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b357-113">Return value</span></span>

<span data-ttu-id="9b357-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b357-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b357-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9b357-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b357-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b357-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9b357-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="9b357-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9b357-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="9b357-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9b357-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9b357-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b357-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b357-120">Requirements</span></span>



| <span data-ttu-id="9b357-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b357-121">Requirement</span></span> | <span data-ttu-id="9b357-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9b357-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b357-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b357-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9b357-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b357-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9b357-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b357-125">Library</span></span><br/> | <dl> <span data-ttu-id="9b357-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="9b357-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b357-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b357-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b357-128">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="9b357-128">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

 






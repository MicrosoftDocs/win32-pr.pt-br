---
title: Método ID3DX11EffectPass ComputeStateBlockMask (D3dx11effect. h)
description: Gere uma máscara para permitir/impedir alterações de estado.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Método ComputeStateBlockMask Direct3D 11
- Método ComputeStateBlockMask Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, método ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc5cb32ce9e9644d7d5b62868bfa99f150cc94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968636"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a><span data-ttu-id="92a34-106">Método ID3DX11EffectPass:: ComputeStateBlockMask</span><span class="sxs-lookup"><span data-stu-id="92a34-106">ID3DX11EffectPass::ComputeStateBlockMask method</span></span>

<span data-ttu-id="92a34-107">Gere uma máscara para permitir/impedir alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="92a34-107">Generate a mask for allowing/preventing state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a34-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92a34-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="92a34-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92a34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a34-110">*pStateBlockMask*</span><span class="sxs-lookup"><span data-stu-id="92a34-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="92a34-111">Tipo: **[ **\_ máscara de \_ bloco \_ de estado D3DX11**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="92a34-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="92a34-112">Um ponteiro para uma máscara de bloco de estado ( [**consulte \_ \_ \_ máscara de bloco de estado D3DX11**](d3dx11-state-block-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="92a34-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a34-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92a34-113">Return value</span></span>

<span data-ttu-id="92a34-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92a34-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92a34-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="92a34-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92a34-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="92a34-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="92a34-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="92a34-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="92a34-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="92a34-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="92a34-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="92a34-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92a34-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92a34-120">Requirements</span></span>



| <span data-ttu-id="92a34-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="92a34-121">Requirement</span></span> | <span data-ttu-id="92a34-122">Valor</span><span class="sxs-lookup"><span data-stu-id="92a34-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a34-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92a34-123">Header</span></span><br/>  | <dl> <span data-ttu-id="92a34-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="92a34-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="92a34-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92a34-125">Library</span></span><br/> | <dl> <span data-ttu-id="92a34-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="92a34-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92a34-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="92a34-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a34-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="92a34-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 






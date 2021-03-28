---
title: Método GetDesc de ID3DX11EffectVariable (D3dx11effect. h)
description: Obtenha uma descrição.
ms.assetid: bf6339d7-8eb0-44da-893e-c805309a3cd3
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc do Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625b9d72b3ff4afe1880b48125d244da1f68844
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989417"
---
# <a name="id3dx11effectvariablegetdesc-method"></a><span data-ttu-id="a740a-106">Método ID3DX11EffectVariable:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="a740a-106">ID3DX11EffectVariable::GetDesc method</span></span>

<span data-ttu-id="a740a-107">Obtenha uma descrição.</span><span class="sxs-lookup"><span data-stu-id="a740a-107">Get a description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a740a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a740a-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_VARIABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a740a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a740a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a740a-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="a740a-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="a740a-111">Tipo: **[ **\_ variável de efeito D3DX11 \_ \_ desc**](d3dx11-effect-variable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a740a-111">Type: **[**D3DX11\_EFFECT\_VARIABLE\_DESC**](d3dx11-effect-variable-desc.md)\***</span></span>

<span data-ttu-id="a740a-112">Um ponteiro para uma descrição de variável de efeito (consulte a [**\_ variável de efeito D3DX11 \_ \_ desc**](d3dx11-effect-variable-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="a740a-112">A pointer to an effect-variable description (see [**D3DX11\_EFFECT\_VARIABLE\_DESC**](d3dx11-effect-variable-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a740a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a740a-113">Return value</span></span>

<span data-ttu-id="a740a-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a740a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a740a-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a740a-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a740a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a740a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a740a-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="a740a-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a740a-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="a740a-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a740a-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a740a-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a740a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a740a-120">Requirements</span></span>



| <span data-ttu-id="a740a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a740a-121">Requirement</span></span> | <span data-ttu-id="a740a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a740a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a740a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a740a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a740a-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a740a-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a740a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a740a-125">Library</span></span><br/> | <dl> <span data-ttu-id="a740a-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="a740a-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a740a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a740a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a740a-128">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="a740a-128">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 






---
title: Método GetDesc de ID3DX11EffectPass (D3dx11effect. h)
description: Obtenha uma descrição de Pass.
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc do Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a85a8c08faa100ecb3987a1a1421613d9c448b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298698"
---
# <a name="id3dx11effectpassgetdesc-method"></a><span data-ttu-id="bbd72-106">Método ID3DX11EffectPass:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="bbd72-106">ID3DX11EffectPass::GetDesc method</span></span>

<span data-ttu-id="bbd72-107">Obtenha uma descrição de Pass.</span><span class="sxs-lookup"><span data-stu-id="bbd72-107">Get a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd72-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbd72-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="bbd72-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbd72-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbd72-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="bbd72-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="bbd72-111">Tipo: **[ **D3DX11 \_ Pass \_ desc**](d3dx11-pass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbd72-111">Type: **[**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)\***</span></span>

<span data-ttu-id="bbd72-112">Um ponteiro para uma descrição de passagem (consulte [**D3DX11 \_ Pass \_ desc**](d3dx11-pass-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="bbd72-112">A pointer to a pass description (see [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbd72-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bbd72-113">Return value</span></span>

<span data-ttu-id="bbd72-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bbd72-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bbd72-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bbd72-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bbd72-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbd72-116">Remarks</span></span>

<span data-ttu-id="bbd72-117">Uma passagem é um bloco de código que define o estado de renderização e os sombreadores (que, por sua vez, define buffers constantes, amostras e texturas).</span><span class="sxs-lookup"><span data-stu-id="bbd72-117">A pass is a block of code that sets render state and shaders (which in turn sets constant buffers, samplers and textures).</span></span> <span data-ttu-id="bbd72-118">Uma técnica de efeito contém um ou mais passos.</span><span class="sxs-lookup"><span data-stu-id="bbd72-118">An effect technique contains one or more passes.</span></span>

> [!Note]  
> <span data-ttu-id="bbd72-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="bbd72-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bbd72-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="bbd72-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bbd72-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bbd72-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bbd72-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbd72-122">Requirements</span></span>



| <span data-ttu-id="bbd72-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbd72-123">Requirement</span></span> | <span data-ttu-id="bbd72-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bbd72-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd72-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bbd72-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bbd72-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbd72-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bbd72-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bbd72-127">Library</span></span><br/> | <dl> <span data-ttu-id="bbd72-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd72-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd72-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbd72-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd72-130">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="bbd72-130">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 






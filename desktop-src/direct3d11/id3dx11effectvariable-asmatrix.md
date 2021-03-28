---
title: Método asmatrix ID3DX11EffectVariable (D3dx11effect. h)
description: Obter uma variável de matriz.
ms.assetid: 5d2baf65-ab0d-44df-bc6f-6ffae16cbb01
keywords:
- Método asmatrix Direct3D 11
- Método asmatrix Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método asmatrix
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c26acd38124a976b53ea950f54e929e717d56555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989429"
---
# <a name="id3dx11effectvariableasmatrix-method"></a><span data-ttu-id="cbccf-106">Método ID3DX11EffectVariable:: asmatrix</span><span class="sxs-lookup"><span data-stu-id="cbccf-106">ID3DX11EffectVariable::AsMatrix method</span></span>

<span data-ttu-id="cbccf-107">Obter uma variável de matriz.</span><span class="sxs-lookup"><span data-stu-id="cbccf-107">Get a matrix variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbccf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbccf-108">Syntax</span></span>


```C++
ID3DX11EffectMatrixVariable* AsMatrix();
```



## <a name="parameters"></a><span data-ttu-id="cbccf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbccf-109">Parameters</span></span>

<span data-ttu-id="cbccf-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cbccf-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbccf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbccf-111">Return value</span></span>

<span data-ttu-id="cbccf-112">Tipo: **[ **ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="cbccf-112">Type: **[**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)\***</span></span>

<span data-ttu-id="cbccf-113">Um ponteiro para uma variável de matriz.</span><span class="sxs-lookup"><span data-stu-id="cbccf-113">A pointer to a matrix variable.</span></span> <span data-ttu-id="cbccf-114">Consulte [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md).</span><span class="sxs-lookup"><span data-stu-id="cbccf-114">See [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cbccf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbccf-115">Remarks</span></span>

<span data-ttu-id="cbccf-116">Asmatrix retorna uma versão da variável de efeito que foi especializada em uma variável de matriz.</span><span class="sxs-lookup"><span data-stu-id="cbccf-116">AsMatrix returns a version of the effect variable that has been specialized to a matrix variable.</span></span> <span data-ttu-id="cbccf-117">De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados de matriz.</span><span class="sxs-lookup"><span data-stu-id="cbccf-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain matrix data.</span></span>

<span data-ttu-id="cbccf-118">Os aplicativos podem testar a validade do objeto retornado chamando [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="cbccf-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="cbccf-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="cbccf-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cbccf-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="cbccf-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cbccf-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cbccf-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cbccf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbccf-122">Requirements</span></span>



| <span data-ttu-id="cbccf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbccf-123">Requirement</span></span> | <span data-ttu-id="cbccf-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cbccf-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbccf-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbccf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cbccf-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbccf-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cbccf-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cbccf-127">Library</span></span><br/> | <dl> <span data-ttu-id="cbccf-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="cbccf-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbccf-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbccf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbccf-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="cbccf-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 






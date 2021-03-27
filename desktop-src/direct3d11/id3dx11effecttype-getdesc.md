---
title: Método GetDesc de ID3DX11EffectType (D3dx11effect. h)
description: Obter uma descrição do tipo de efeito.
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc do Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1ee52e4c6628c00b0155e5bd3081b6c4fd8c46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989406"
---
# <a name="id3dx11effecttypegetdesc-method"></a><span data-ttu-id="86ce6-106">Método ID3DX11EffectType:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="86ce6-106">ID3DX11EffectType::GetDesc method</span></span>

<span data-ttu-id="86ce6-107">Obter uma descrição do tipo de efeito.</span><span class="sxs-lookup"><span data-stu-id="86ce6-107">Get an effect-type description.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ce6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86ce6-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="86ce6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86ce6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86ce6-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="86ce6-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="86ce6-111">Tipo: **[ **\_ tipo de efeito D3DX11 \_ \_ desc**](d3dx11-effect-type-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="86ce6-111">Type: **[**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md)\***</span></span>

<span data-ttu-id="86ce6-112">Um ponteiro para uma descrição de tipo de efeito.</span><span class="sxs-lookup"><span data-stu-id="86ce6-112">A pointer to an effect-type description.</span></span> <span data-ttu-id="86ce6-113">Consulte [**o \_ tipo de efeito D3DX11 \_ \_ desc**](d3dx11-effect-type-desc.md).</span><span class="sxs-lookup"><span data-stu-id="86ce6-113">See [**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86ce6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86ce6-114">Return value</span></span>

<span data-ttu-id="86ce6-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86ce6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86ce6-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="86ce6-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="86ce6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="86ce6-117">Remarks</span></span>

<span data-ttu-id="86ce6-118">A descrição da variável de efeito contém dados sobre o nome, as anotações, a semântica, os sinalizadores e o deslocamento do buffer do tipo de efeito.</span><span class="sxs-lookup"><span data-stu-id="86ce6-118">The effect-variable description contains data about the name, annotations, semantic, flags and buffer offset of the effect type.</span></span>

> [!Note]  
> <span data-ttu-id="86ce6-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="86ce6-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="86ce6-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="86ce6-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="86ce6-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="86ce6-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86ce6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86ce6-122">Requirements</span></span>



| <span data-ttu-id="86ce6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="86ce6-123">Requirement</span></span> | <span data-ttu-id="86ce6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="86ce6-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86ce6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86ce6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="86ce6-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="86ce6-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="86ce6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86ce6-127">Library</span></span><br/> | <dl> <span data-ttu-id="86ce6-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="86ce6-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ce6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="86ce6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ce6-130">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="86ce6-130">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

 






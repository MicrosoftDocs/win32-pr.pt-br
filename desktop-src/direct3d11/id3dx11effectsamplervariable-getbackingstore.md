---
title: Método ID3DX11EffectSamplerVariable GetBackingStore (D3dx11effect. h)
description: Obtenha um ponteiro para uma variável que contém o estado de amostra.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11, interface ID3DX11EffectSamplerVariable
- Interface ID3DX11EffectSamplerVariable Direct3D 11, método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f2d6ac3035d1dd2fd3aee8950135d7b4481862
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298722"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a><span data-ttu-id="9140f-106">Método ID3DX11EffectSamplerVariable:: GetBackingStore</span><span class="sxs-lookup"><span data-stu-id="9140f-106">ID3DX11EffectSamplerVariable::GetBackingStore method</span></span>

<span data-ttu-id="9140f-107">Obtenha um ponteiro para uma variável que contém o estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="9140f-107">Get a pointer to a variable that contains sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9140f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9140f-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="9140f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9140f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9140f-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="9140f-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="9140f-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9140f-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9140f-112">Indexe em uma matriz de descrições de amostras.</span><span class="sxs-lookup"><span data-stu-id="9140f-112">Index into an array of sampler descriptions.</span></span> <span data-ttu-id="9140f-113">Se houver apenas uma variável de amostra no efeito, use 0.</span><span class="sxs-lookup"><span data-stu-id="9140f-113">If there is only one sampler variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="9140f-114">*pSamplerDesc*</span><span class="sxs-lookup"><span data-stu-id="9140f-114">*pSamplerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="9140f-115">Tipo: **[ **D3D11 \_ amostra \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span><span class="sxs-lookup"><span data-stu-id="9140f-115">Type: **[**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span></span>

<span data-ttu-id="9140f-116">Um ponteiro para uma descrição de amostra (consulte o [**D3D11 de \_ amostra \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span><span class="sxs-lookup"><span data-stu-id="9140f-116">A pointer to a sampler description (see [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9140f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9140f-117">Return value</span></span>

<span data-ttu-id="9140f-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9140f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9140f-119">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9140f-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9140f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9140f-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9140f-121">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="9140f-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9140f-122">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="9140f-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9140f-123">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9140f-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9140f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9140f-124">Requirements</span></span>



| <span data-ttu-id="9140f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9140f-125">Requirement</span></span> | <span data-ttu-id="9140f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9140f-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9140f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9140f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9140f-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9140f-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9140f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9140f-129">Library</span></span><br/> | <dl> <span data-ttu-id="9140f-130"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="9140f-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9140f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9140f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9140f-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="9140f-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 


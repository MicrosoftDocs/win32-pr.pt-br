---
title: Método ID3DX11EffectShaderResourceVariable GetResourceArray (D3dx11effect. h)
description: Obtenha uma matriz de recursos de sombreador.
ms.assetid: 7540183d-dabb-46c2-8df1-6d4734b77f25
keywords:
- Método GetResourceArray Direct3D 11
- Método GetResourceArray Direct3D 11, interface ID3DX11EffectShaderResourceVariable
- Interface ID3DX11EffectShaderResourceVariable Direct3D 11, método GetResourceArray
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResourceArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0091d81b7e157aecb8315e1def380800c8155c60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930764"
---
# <a name="id3dx11effectshaderresourcevariablegetresourcearray-method"></a><span data-ttu-id="3c319-106">Método ID3DX11EffectShaderResourceVariable:: GetResourceArray</span><span class="sxs-lookup"><span data-stu-id="3c319-106">ID3DX11EffectShaderResourceVariable::GetResourceArray method</span></span>

<span data-ttu-id="3c319-107">Obtenha uma matriz de recursos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3c319-107">Get an array of shader resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c319-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c319-108">Syntax</span></span>


```C++
HRESULT GetResourceArray(
   ID3D11ShaderResourceView **ppResources,
   UINT                     Offset,
   UINT                     Count
);
```



## <a name="parameters"></a><span data-ttu-id="3c319-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c319-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c319-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="3c319-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="3c319-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="3c319-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="3c319-112">O endereço de uma matriz de interfaces Shader-Resource-View.</span><span class="sxs-lookup"><span data-stu-id="3c319-112">The address of an array of shader-resource-view interfaces.</span></span> <span data-ttu-id="3c319-113">Consulte [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="3c319-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="3c319-114">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="3c319-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3c319-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c319-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c319-116">O índice de matriz com base em zero para obter a primeira interface.</span><span class="sxs-lookup"><span data-stu-id="3c319-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="3c319-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="3c319-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3c319-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c319-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c319-119">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="3c319-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c319-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c319-120">Return value</span></span>

<span data-ttu-id="3c319-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c319-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c319-122">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3c319-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c319-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c319-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3c319-124">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="3c319-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3c319-125">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="3c319-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3c319-126">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3c319-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c319-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c319-127">Requirements</span></span>



| <span data-ttu-id="3c319-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c319-128">Requirement</span></span> | <span data-ttu-id="3c319-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3c319-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c319-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c319-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3c319-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c319-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3c319-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c319-132">Library</span></span><br/> | <dl> <span data-ttu-id="3c319-133"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="3c319-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c319-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c319-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c319-135">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="3c319-135">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 


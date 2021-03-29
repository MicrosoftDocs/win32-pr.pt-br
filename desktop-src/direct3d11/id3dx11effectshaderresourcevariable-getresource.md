---
title: Método getResource ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Obter um recurso de sombreador.
ms.assetid: 7c56aba0-ce60-4b50-9c1a-802bf1d73c6b
keywords:
- Método getResource Direct3D 11
- Método getResource Direct3D 11, interface ID3DX11EffectShaderResourceVariable
- Interface ID3DX11EffectShaderResourceVariable Direct3D 11, método getResource
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea841ae63646958603396d5b65305c242961942
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172933"
---
# <a name="id3dx11effectshaderresourcevariablegetresource-method"></a><span data-ttu-id="fb27f-106">Método ID3DX11EffectShaderResourceVariable:: getResource</span><span class="sxs-lookup"><span data-stu-id="fb27f-106">ID3DX11EffectShaderResourceVariable::GetResource method</span></span>

<span data-ttu-id="fb27f-107">Obter um recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fb27f-107">Get a shader resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb27f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb27f-108">Syntax</span></span>


```C++
HRESULT GetResource(
   ID3D11ShaderResourceView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="fb27f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb27f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb27f-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="fb27f-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="fb27f-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="fb27f-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="fb27f-112">O endereço de um ponteiro para uma interface de exibição de recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fb27f-112">The address of a pointer to a shader-resource-view interface.</span></span> <span data-ttu-id="fb27f-113">Consulte [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="fb27f-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb27f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb27f-114">Return value</span></span>

<span data-ttu-id="fb27f-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb27f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb27f-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fb27f-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb27f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb27f-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fb27f-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="fb27f-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fb27f-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="fb27f-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fb27f-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fb27f-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb27f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb27f-121">Requirements</span></span>



| <span data-ttu-id="fb27f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb27f-122">Requirement</span></span> | <span data-ttu-id="fb27f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fb27f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb27f-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb27f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fb27f-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb27f-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fb27f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb27f-126">Library</span></span><br/> | <dl> <span data-ttu-id="fb27f-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="fb27f-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb27f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb27f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb27f-129">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="fb27f-129">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 






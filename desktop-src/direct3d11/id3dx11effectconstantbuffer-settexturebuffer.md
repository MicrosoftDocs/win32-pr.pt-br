---
title: Método ID3DX11EffectConstantBuffer SetTextureBuffer (D3dx11effect. h)
description: Defina um buffer de textura.
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- Método SetTextureBuffer Direct3D 11
- Método SetTextureBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, método SetTextureBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736ec4c5f0125dfc37925d67875cf97c5441117c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968568"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a><span data-ttu-id="64513-106">Método ID3DX11EffectConstantBuffer:: SetTextureBuffer</span><span class="sxs-lookup"><span data-stu-id="64513-106">ID3DX11EffectConstantBuffer::SetTextureBuffer method</span></span>

<span data-ttu-id="64513-107">Defina um buffer de textura.</span><span class="sxs-lookup"><span data-stu-id="64513-107">Set a texture-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="64513-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64513-108">Syntax</span></span>


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="64513-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64513-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64513-110">*pTextureBuffer*</span><span class="sxs-lookup"><span data-stu-id="64513-110">*pTextureBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="64513-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="64513-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span></span>

<span data-ttu-id="64513-112">Um ponteiro para uma interface Shader-Resource-View para acessar um buffer de textura.</span><span class="sxs-lookup"><span data-stu-id="64513-112">A pointer to a shader-resource-view interface for accessing a texture buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64513-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64513-113">Return value</span></span>

<span data-ttu-id="64513-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64513-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64513-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="64513-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="64513-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="64513-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="64513-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="64513-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="64513-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="64513-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="64513-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="64513-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64513-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64513-120">Requirements</span></span>



| <span data-ttu-id="64513-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="64513-121">Requirement</span></span> | <span data-ttu-id="64513-122">Valor</span><span class="sxs-lookup"><span data-stu-id="64513-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64513-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64513-123">Header</span></span><br/>  | <dl> <span data-ttu-id="64513-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="64513-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="64513-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="64513-125">Library</span></span><br/> | <dl> <span data-ttu-id="64513-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="64513-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64513-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="64513-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64513-128">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="64513-128">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 






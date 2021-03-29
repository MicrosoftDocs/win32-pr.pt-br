---
title: Método ID3DX11EffectConstantBuffer GetTextureBuffer (D3dx11effect. h)
description: Obter um buffer de textura.
ms.assetid: 8d09e67c-358e-49ee-8ca4-e1f548b52c3a
keywords:
- Método GetTextureBuffer Direct3D 11
- Método GetTextureBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, método GetTextureBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03000338c725e71096e57715a49a70b4347b358
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968673"
---
# <a name="id3dx11effectconstantbuffergettexturebuffer-method"></a><span data-ttu-id="fa4a2-106">Método ID3DX11EffectConstantBuffer:: GetTextureBuffer</span><span class="sxs-lookup"><span data-stu-id="fa4a2-106">ID3DX11EffectConstantBuffer::GetTextureBuffer method</span></span>

<span data-ttu-id="fa4a2-107">Obter um buffer de textura.</span><span class="sxs-lookup"><span data-stu-id="fa4a2-107">Get a texture-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4a2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa4a2-108">Syntax</span></span>


```C++
HRESULT GetTextureBuffer(
   ID3D11ShaderResourceView **ppTextureBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="fa4a2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa4a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa4a2-110">*ppTextureBuffer*</span><span class="sxs-lookup"><span data-stu-id="fa4a2-110">*ppTextureBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="fa4a2-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="fa4a2-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="fa4a2-112">O endereço de um ponteiro para uma interface de exibição de recurso de sombreador para acessar um buffer de textura.</span><span class="sxs-lookup"><span data-stu-id="fa4a2-112">The address of a pointer to a shader-resource-view interface for accessing a texture buffer.</span></span> <span data-ttu-id="fa4a2-113">Consulte [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="fa4a2-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa4a2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa4a2-114">Return value</span></span>

<span data-ttu-id="fa4a2-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa4a2-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa4a2-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fa4a2-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fa4a2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa4a2-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa4a2-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="fa4a2-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fa4a2-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="fa4a2-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fa4a2-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fa4a2-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa4a2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa4a2-121">Requirements</span></span>



| <span data-ttu-id="fa4a2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa4a2-122">Requirement</span></span> | <span data-ttu-id="fa4a2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fa4a2-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa4a2-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa4a2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fa4a2-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa4a2-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fa4a2-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa4a2-126">Library</span></span><br/> | <dl> <span data-ttu-id="fa4a2-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="fa4a2-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa4a2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa4a2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa4a2-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="fa4a2-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 






---
title: Método ID3DX11EffectVariable AsConstantBuffer (D3dx11effect. h)
description: Obter um buffer de constantes. | Método ID3DX11EffectVariable AsConstantBuffer (D3dx11effect. h)
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- Método AsConstantBuffer Direct3D 11
- Método AsConstantBuffer Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método AsConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4caca60216df0c04a773da22150dbc6f7be717
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989310"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a><span data-ttu-id="9b351-107">Método ID3DX11EffectVariable:: AsConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="9b351-107">ID3DX11EffectVariable::AsConstantBuffer method</span></span>

<span data-ttu-id="9b351-108">Obter um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="9b351-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b351-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b351-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="9b351-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b351-110">Parameters</span></span>

<span data-ttu-id="9b351-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9b351-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b351-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b351-112">Return value</span></span>

<span data-ttu-id="9b351-113">Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b351-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="9b351-114">Um ponteiro para um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="9b351-114">A pointer to a constant buffer.</span></span> <span data-ttu-id="9b351-115">Consulte [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9b351-115">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b351-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b351-116">Remarks</span></span>

<span data-ttu-id="9b351-117">AsConstantBuffer retorna uma versão da variável de efeito que foi especializada em um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="9b351-117">AsConstantBuffer returns a version of the effect variable that has been specialized to a constant buffer.</span></span> <span data-ttu-id="9b351-118">De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados de buffer constante.</span><span class="sxs-lookup"><span data-stu-id="9b351-118">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain constant buffer data.</span></span>

<span data-ttu-id="9b351-119">Os aplicativos podem testar a validade do objeto retornado chamando [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="9b351-119">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="9b351-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="9b351-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9b351-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="9b351-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9b351-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9b351-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b351-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b351-123">Requirements</span></span>



| <span data-ttu-id="9b351-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b351-124">Requirement</span></span> | <span data-ttu-id="9b351-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9b351-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b351-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b351-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9b351-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b351-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9b351-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b351-128">Library</span></span><br/> | <dl> <span data-ttu-id="9b351-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="9b351-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b351-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b351-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b351-131">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="9b351-131">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 






---
title: Método ID3DX11EffectVariable GetParentConstantBuffer (D3dx11effect. h)
description: Obter um buffer de constantes. | Método ID3DX11EffectVariable GetParentConstantBuffer (D3dx11effect. h)
ms.assetid: 43b46b05-951e-4c52-8bc7-4bb5f657ea78
keywords:
- Método GetParentConstantBuffer Direct3D 11
- Método GetParentConstantBuffer Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetParentConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetParentConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa424b91b72dca5539fd0f96a1380e86d1f23f58
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989408"
---
# <a name="id3dx11effectvariablegetparentconstantbuffer-method"></a><span data-ttu-id="37f39-107">Método ID3DX11EffectVariable:: GetParentConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="37f39-107">ID3DX11EffectVariable::GetParentConstantBuffer method</span></span>

<span data-ttu-id="37f39-108">Obter um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="37f39-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="37f39-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37f39-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetParentConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="37f39-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37f39-110">Parameters</span></span>

<span data-ttu-id="37f39-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="37f39-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37f39-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37f39-112">Return value</span></span>

<span data-ttu-id="37f39-113">Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="37f39-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="37f39-114">Um ponteiro para um [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="37f39-114">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="37f39-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="37f39-115">Remarks</span></span>

<span data-ttu-id="37f39-116">Variáveis de efeito são de leitura ou gravação para um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="37f39-116">Effect variables are read-from or written-to a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="37f39-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="37f39-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="37f39-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="37f39-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="37f39-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="37f39-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="37f39-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37f39-120">Requirements</span></span>



| <span data-ttu-id="37f39-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="37f39-121">Requirement</span></span> | <span data-ttu-id="37f39-122">Valor</span><span class="sxs-lookup"><span data-stu-id="37f39-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37f39-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37f39-123">Header</span></span><br/>  | <dl> <span data-ttu-id="37f39-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="37f39-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="37f39-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37f39-125">Library</span></span><br/> | <dl> <span data-ttu-id="37f39-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="37f39-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37f39-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="37f39-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f39-128">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="37f39-128">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 






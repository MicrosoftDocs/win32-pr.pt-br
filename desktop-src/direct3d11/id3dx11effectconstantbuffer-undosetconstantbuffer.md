---
title: Método ID3DX11EffectConstantBuffer UndoSetConstantBuffer (D3dx11effect. h)
description: Reverte um buffer de constante definido anteriormente.
ms.assetid: 6c5e1256-3a92-4bfe-8614-f09d627bc3db
keywords:
- Método UndoSetConstantBuffer Direct3D 11
- Método UndoSetConstantBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, método UndoSetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c95a26f1ea92d5bfe1975e3fe4dc1961046e5535
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104371002"
---
# <a name="id3dx11effectconstantbufferundosetconstantbuffer-method"></a><span data-ttu-id="292fb-106">Método ID3DX11EffectConstantBuffer:: UndoSetConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="292fb-106">ID3DX11EffectConstantBuffer::UndoSetConstantBuffer method</span></span>

<span data-ttu-id="292fb-107">Reverte um buffer de constante definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="292fb-107">Reverts a previously set constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="292fb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="292fb-108">Syntax</span></span>


```C++
HRESULT UndoSetConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="292fb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="292fb-109">Parameters</span></span>

<span data-ttu-id="292fb-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="292fb-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="292fb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="292fb-111">Return value</span></span>

<span data-ttu-id="292fb-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="292fb-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="292fb-113">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="292fb-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="292fb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="292fb-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="292fb-115">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="292fb-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="292fb-116">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="292fb-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="292fb-117">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="292fb-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="292fb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="292fb-118">Requirements</span></span>



| <span data-ttu-id="292fb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="292fb-119">Requirement</span></span> | <span data-ttu-id="292fb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="292fb-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="292fb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="292fb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="292fb-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="292fb-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="292fb-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="292fb-123">Library</span></span><br/> | <dl> <span data-ttu-id="292fb-124"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="292fb-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="292fb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="292fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="292fb-126">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="292fb-126">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 






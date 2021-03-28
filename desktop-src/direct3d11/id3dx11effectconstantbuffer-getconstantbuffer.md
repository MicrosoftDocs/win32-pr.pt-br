---
title: Método ID3DX11EffectConstantBuffer GetConstantBuffer (D3dx11effect. h)
description: Obtenha um buffer constante.
ms.assetid: 857b3dc2-41ae-4a52-904a-9ca8f0afeb9e
keywords:
- Método GetConstantBuffer Direct3D 11
- Método GetConstantBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, método GetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041ca2fea028cb86d0959313bae73c320e6e5a36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012181"
---
# <a name="id3dx11effectconstantbuffergetconstantbuffer-method"></a><span data-ttu-id="943ac-106">Método ID3DX11EffectConstantBuffer:: GetConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="943ac-106">ID3DX11EffectConstantBuffer::GetConstantBuffer method</span></span>

<span data-ttu-id="943ac-107">Obtenha um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="943ac-107">Get a constant-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="943ac-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="943ac-108">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
   ID3D11Buffer **ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="943ac-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="943ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="943ac-110">*ppConstantBuffer*</span><span class="sxs-lookup"><span data-stu-id="943ac-110">*ppConstantBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="943ac-111">Tipo: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="943ac-111">Type: **[**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span></span>

<span data-ttu-id="943ac-112">O endereço de um ponteiro para uma interface de buffer constante.</span><span class="sxs-lookup"><span data-stu-id="943ac-112">The address of a pointer to a constant-buffer interface.</span></span> <span data-ttu-id="943ac-113">Consulte [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span><span class="sxs-lookup"><span data-stu-id="943ac-113">See [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="943ac-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="943ac-114">Return value</span></span>

<span data-ttu-id="943ac-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="943ac-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="943ac-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="943ac-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="943ac-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="943ac-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="943ac-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="943ac-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="943ac-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="943ac-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="943ac-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="943ac-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="943ac-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="943ac-121">Requirements</span></span>



| <span data-ttu-id="943ac-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="943ac-122">Requirement</span></span> | <span data-ttu-id="943ac-123">Valor</span><span class="sxs-lookup"><span data-stu-id="943ac-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="943ac-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="943ac-124">Header</span></span><br/>  | <dl> <span data-ttu-id="943ac-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="943ac-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="943ac-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="943ac-126">Library</span></span><br/> | <dl> <span data-ttu-id="943ac-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="943ac-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="943ac-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="943ac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943ac-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="943ac-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 






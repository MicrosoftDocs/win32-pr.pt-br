---
title: Método ID3DX11EffectConstantBuffer SetConstantBuffer (D3dx11effect. h)
description: Definir um buffer de constantes.
ms.assetid: 288e029a-e69a-4f58-be3f-8f9900c0e1dd
keywords:
- Método SetConstantBuffer Direct3D 11
- Método SetConstantBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, método SetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12249d9830ced43c3a56a2c8cf51942e66f6494e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173159"
---
# <a name="id3dx11effectconstantbuffersetconstantbuffer-method"></a><span data-ttu-id="e8686-106">Método ID3DX11EffectConstantBuffer:: SetConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="e8686-106">ID3DX11EffectConstantBuffer::SetConstantBuffer method</span></span>

<span data-ttu-id="e8686-107">Definir um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="e8686-107">Set a constant-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8686-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8686-108">Syntax</span></span>


```C++
HRESULT SetConstantBuffer(
   ID3D11Buffer *pConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="e8686-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8686-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8686-110">*pConstantBuffer*</span><span class="sxs-lookup"><span data-stu-id="e8686-110">*pConstantBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="e8686-111">Tipo: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\***</span><span class="sxs-lookup"><span data-stu-id="e8686-111">Type: **[**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\***</span></span>

<span data-ttu-id="e8686-112">Um ponteiro para uma interface de buffer constante.</span><span class="sxs-lookup"><span data-stu-id="e8686-112">A pointer to a constant-buffer interface.</span></span> <span data-ttu-id="e8686-113">Consulte [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span><span class="sxs-lookup"><span data-stu-id="e8686-113">See [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8686-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8686-114">Return value</span></span>

<span data-ttu-id="e8686-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8686-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8686-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e8686-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8686-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8686-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8686-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="e8686-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e8686-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="e8686-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e8686-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e8686-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8686-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8686-121">Requirements</span></span>



| <span data-ttu-id="e8686-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8686-122">Requirement</span></span> | <span data-ttu-id="e8686-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e8686-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8686-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8686-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e8686-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8686-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e8686-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8686-126">Library</span></span><br/> | <dl> <span data-ttu-id="e8686-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="e8686-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8686-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8686-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8686-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="e8686-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 






---
title: Método GetDesc de ID3DX11Effect (D3dx11effect. h)
description: Obtenha uma descrição de efeito.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc do Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587cde43ec2d9136bab5884691c99321d1492835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989377"
---
# <a name="id3dx11effectgetdesc-method"></a><span data-ttu-id="090de-106">Método ID3DX11Effect:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="090de-106">ID3DX11Effect::GetDesc method</span></span>

<span data-ttu-id="090de-107">Obtenha uma descrição de efeito.</span><span class="sxs-lookup"><span data-stu-id="090de-107">Get an effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="090de-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="090de-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="090de-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="090de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090de-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="090de-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="090de-111">Tipo: **[ **D3DX11 \_ efeito \_ desc**](d3dx11-effect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="090de-111">Type: **[**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)\***</span></span>

<span data-ttu-id="090de-112">Um ponteiro para uma descrição de efeito (consulte o [**\_ efeito \_ desc de D3DX11**](d3dx11-effect-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="090de-112">A pointer to an effect description (see [**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090de-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="090de-113">Return value</span></span>

<span data-ttu-id="090de-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="090de-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="090de-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="090de-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="090de-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="090de-116">Remarks</span></span>

<span data-ttu-id="090de-117">Uma descrição de efeito contém informações básicas sobre um efeito, como as técnicas que ele contém e os recursos de buffer constantes necessários.</span><span class="sxs-lookup"><span data-stu-id="090de-117">An effect description contains basic information about an effect such as the techniques it contains and the constant buffer resources it requires.</span></span>

> [!Note]  
> <span data-ttu-id="090de-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="090de-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="090de-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="090de-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="090de-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="090de-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="090de-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="090de-121">Requirements</span></span>



| <span data-ttu-id="090de-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="090de-122">Requirement</span></span> | <span data-ttu-id="090de-123">Valor</span><span class="sxs-lookup"><span data-stu-id="090de-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="090de-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="090de-124">Header</span></span><br/>  | <dl> <span data-ttu-id="090de-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="090de-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="090de-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="090de-126">Library</span></span><br/> | <dl> <span data-ttu-id="090de-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="090de-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="090de-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="090de-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090de-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="090de-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 






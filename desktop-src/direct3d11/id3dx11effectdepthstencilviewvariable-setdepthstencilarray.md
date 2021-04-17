---
title: Método ID3DX11EffectDepthStencilViewVariable SetDepthStencilArray (D3dx11effect. h)
description: Defina uma matriz de recursos de exibição de estêncil de profundidade.
ms.assetid: 7a00ca3e-fb07-4185-a361-36228f72dcea
keywords:
- Método SetDepthStencilArray Direct3D 11
- Método SetDepthStencilArray Direct3D 11, interface ID3DX11EffectDepthStencilViewVariable
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, método SetDepthStencilArray
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329f91fff70d78c51475b799a08dec1c6d34a157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968615"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencilarray-method"></a><span data-ttu-id="ad2bf-106">Método ID3DX11EffectDepthStencilViewVariable:: SetDepthStencilArray</span><span class="sxs-lookup"><span data-stu-id="ad2bf-106">ID3DX11EffectDepthStencilViewVariable::SetDepthStencilArray method</span></span>

<span data-ttu-id="ad2bf-107">Defina uma matriz de recursos de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="ad2bf-107">Set an array of depth-stencil-view resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad2bf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad2bf-108">Syntax</span></span>


```C++
HRESULT SetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="ad2bf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad2bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad2bf-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="ad2bf-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="ad2bf-111">Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="ad2bf-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="ad2bf-112">Um ponteiro para uma matriz de interfaces de exibição de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="ad2bf-112">A pointer to an array of depth-stencil-view interfaces.</span></span> <span data-ttu-id="ad2bf-113">Consulte [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="ad2bf-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> <dt>

<span data-ttu-id="ad2bf-114">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="ad2bf-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="ad2bf-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ad2bf-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ad2bf-116">O índice de matriz com base em zero para definir a primeira interface.</span><span class="sxs-lookup"><span data-stu-id="ad2bf-116">The zero-based array index to set the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="ad2bf-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="ad2bf-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="ad2bf-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ad2bf-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ad2bf-119">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="ad2bf-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad2bf-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad2bf-120">Return value</span></span>

<span data-ttu-id="ad2bf-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad2bf-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad2bf-122">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ad2bf-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad2bf-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad2bf-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ad2bf-124">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="ad2bf-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ad2bf-125">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="ad2bf-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ad2bf-126">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ad2bf-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad2bf-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad2bf-127">Requirements</span></span>



| <span data-ttu-id="ad2bf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad2bf-128">Requirement</span></span> | <span data-ttu-id="ad2bf-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ad2bf-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad2bf-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad2bf-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ad2bf-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad2bf-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ad2bf-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad2bf-132">Library</span></span><br/> | <dl> <span data-ttu-id="ad2bf-133"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="ad2bf-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad2bf-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad2bf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad2bf-135">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="ad2bf-135">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 


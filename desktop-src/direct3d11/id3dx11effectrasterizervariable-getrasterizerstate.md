---
title: Método ID3DX11EffectRasterizerVariable GetRasterizerState (D3dx11effect. h)
description: Obter um ponteiro para uma interface do rasterizador.
ms.assetid: 4b8515e0-b79a-4572-9142-07c50a8839b8
keywords:
- Método GetRasterizerState Direct3D 11
- Método GetRasterizerState Direct3D 11, interface ID3DX11EffectRasterizerVariable
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, método GetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972140a8f74a3e5a6728429faddacc253aaa6c9d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968710"
---
# <a name="id3dx11effectrasterizervariablegetrasterizerstate-method"></a><span data-ttu-id="92477-106">Método ID3DX11EffectRasterizerVariable:: GetRasterizerState</span><span class="sxs-lookup"><span data-stu-id="92477-106">ID3DX11EffectRasterizerVariable::GetRasterizerState method</span></span>

<span data-ttu-id="92477-107">Obter um ponteiro para uma interface do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="92477-107">Get a pointer to a rasterizer interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="92477-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92477-108">Syntax</span></span>


```C++
HRESULT GetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState **ppRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="92477-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92477-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92477-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="92477-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="92477-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="92477-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="92477-112">Indexe em uma matriz de interfaces do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="92477-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="92477-113">Se houver apenas uma interface do rasterizador, use 0.</span><span class="sxs-lookup"><span data-stu-id="92477-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="92477-114">*ppRasterizerState*</span><span class="sxs-lookup"><span data-stu-id="92477-114">*ppRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="92477-115">Tipo: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="92477-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span></span>

<span data-ttu-id="92477-116">O endereço de um ponteiro para uma interface do rasterizador (consulte [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span><span class="sxs-lookup"><span data-stu-id="92477-116">The address of a pointer to a rasterizer interface (see [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92477-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92477-117">Return value</span></span>

<span data-ttu-id="92477-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92477-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92477-119">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="92477-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92477-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="92477-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="92477-121">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="92477-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="92477-122">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="92477-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="92477-123">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="92477-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92477-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92477-124">Requirements</span></span>



| <span data-ttu-id="92477-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="92477-125">Requirement</span></span> | <span data-ttu-id="92477-126">Valor</span><span class="sxs-lookup"><span data-stu-id="92477-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92477-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92477-127">Header</span></span><br/>  | <dl> <span data-ttu-id="92477-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="92477-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="92477-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92477-129">Library</span></span><br/> | <dl> <span data-ttu-id="92477-130"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="92477-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92477-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="92477-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92477-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="92477-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 


---
title: Método ID3DX11EffectRasterizerVariable GetBackingStore (D3dx11effect. h)
description: Obtenha um ponteiro para uma variável que contém o estado rasteriser.
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11, interface ID3DX11EffectRasterizerVariable
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1941ba93b69f1d07eeebaa6c1f0c9323f5c0a49e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012152"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a><span data-ttu-id="ef6d4-106">Método ID3DX11EffectRasterizerVariable:: GetBackingStore</span><span class="sxs-lookup"><span data-stu-id="ef6d4-106">ID3DX11EffectRasterizerVariable::GetBackingStore method</span></span>

<span data-ttu-id="ef6d4-107">Obtenha um ponteiro para uma variável que contém o estado rasteriser.</span><span class="sxs-lookup"><span data-stu-id="ef6d4-107">Get a pointer to a variable that contains rasteriser state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef6d4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef6d4-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ef6d4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef6d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef6d4-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="ef6d4-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="ef6d4-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ef6d4-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ef6d4-112">Indexe em uma matriz de descrições de rasteriser.</span><span class="sxs-lookup"><span data-stu-id="ef6d4-112">Index into an array of rasteriser-state descriptions.</span></span> <span data-ttu-id="ef6d4-113">Se houver apenas uma variável rasteriser no efeito, use 0.</span><span class="sxs-lookup"><span data-stu-id="ef6d4-113">If there is only one rasteriser variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="ef6d4-114">*pRasterizerDesc*</span><span class="sxs-lookup"><span data-stu-id="ef6d4-114">*pRasterizerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="ef6d4-115">Tipo: **[ **D3D11 do \_ rasterizador \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***</span><span class="sxs-lookup"><span data-stu-id="ef6d4-115">Type: **[**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***</span></span>

<span data-ttu-id="ef6d4-116">Um ponteiro para uma descrição de rasteriser (consulte [**D3D11 \_ rasterizador \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).</span><span class="sxs-lookup"><span data-stu-id="ef6d4-116">A pointer to a rasteriser-state description (see [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef6d4-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef6d4-117">Return value</span></span>

<span data-ttu-id="ef6d4-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef6d4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef6d4-119">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ef6d4-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef6d4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef6d4-120">Remarks</span></span>

<span data-ttu-id="ef6d4-121">As variáveis de efeito são salvas na memória no repositório de backup; Quando uma técnica é aplicada, os valores no repositório de backup são copiados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef6d4-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="ef6d4-122">O backup de dados do repositório pode ser usado para recriar a variável quando necessário.</span><span class="sxs-lookup"><span data-stu-id="ef6d4-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="ef6d4-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="ef6d4-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ef6d4-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="ef6d4-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ef6d4-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ef6d4-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef6d4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef6d4-126">Requirements</span></span>



| <span data-ttu-id="ef6d4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef6d4-127">Requirement</span></span> | <span data-ttu-id="ef6d4-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ef6d4-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6d4-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef6d4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ef6d4-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef6d4-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ef6d4-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef6d4-131">Library</span></span><br/> | <dl> <span data-ttu-id="ef6d4-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="ef6d4-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef6d4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef6d4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef6d4-134">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="ef6d4-134">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 


---
title: Método ID3DX11EffectTechnique GetPassByIndex (D3dx11effect. h)
description: Obter uma passagem por índice.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Método GetPassByIndex Direct3D 11
- Método GetPassByIndex Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, método GetPassByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6af222298cc3d00ad87e5037f9de20139e4fc40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930711"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a><span data-ttu-id="daac4-106">Método ID3DX11EffectTechnique:: GetPassByIndex</span><span class="sxs-lookup"><span data-stu-id="daac4-106">ID3DX11EffectTechnique::GetPassByIndex method</span></span>

<span data-ttu-id="daac4-107">Obter uma passagem por índice.</span><span class="sxs-lookup"><span data-stu-id="daac4-107">Get a pass by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="daac4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="daac4-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="daac4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="daac4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daac4-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="daac4-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="daac4-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="daac4-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="daac4-112">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="daac4-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daac4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="daac4-113">Return value</span></span>

<span data-ttu-id="daac4-114">Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="daac4-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="daac4-115">Um ponteiro para um [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="daac4-115">A pointer to a [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="daac4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="daac4-116">Remarks</span></span>

<span data-ttu-id="daac4-117">Uma técnica contém uma ou mais passagens; Obtenha uma passagem usando um nome ou um índice.</span><span class="sxs-lookup"><span data-stu-id="daac4-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="daac4-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="daac4-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="daac4-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="daac4-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="daac4-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="daac4-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="daac4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daac4-121">Requirements</span></span>



| <span data-ttu-id="daac4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="daac4-122">Requirement</span></span> | <span data-ttu-id="daac4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="daac4-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daac4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="daac4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="daac4-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="daac4-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="daac4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="daac4-126">Library</span></span><br/> | <dl> <span data-ttu-id="daac4-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="daac4-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daac4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="daac4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daac4-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="daac4-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 


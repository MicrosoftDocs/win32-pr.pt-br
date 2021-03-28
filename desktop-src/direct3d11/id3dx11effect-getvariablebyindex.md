---
title: Método ID3DX11Effect GetVariableByIndex (D3dx11effect. h)
description: Obter uma variável por índice.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Método GetVariableByIndex Direct3D 11
- Método GetVariableByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetVariableByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989371"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a><span data-ttu-id="57b83-106">Método ID3DX11Effect:: GetVariableByIndex</span><span class="sxs-lookup"><span data-stu-id="57b83-106">ID3DX11Effect::GetVariableByIndex method</span></span>

<span data-ttu-id="57b83-107">Obter uma variável por índice.</span><span class="sxs-lookup"><span data-stu-id="57b83-107">Get a variable by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="57b83-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57b83-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="57b83-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57b83-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b83-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="57b83-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="57b83-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="57b83-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="57b83-112">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="57b83-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b83-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57b83-113">Return value</span></span>

<span data-ttu-id="57b83-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="57b83-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="57b83-115">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="57b83-115">A pointer to a [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="57b83-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="57b83-116">Remarks</span></span>

<span data-ttu-id="57b83-117">Um efeito pode conter uma ou mais variáveis.</span><span class="sxs-lookup"><span data-stu-id="57b83-117">An effect may contain one or more variables.</span></span> <span data-ttu-id="57b83-118">Variáveis fora de uma técnica são consideradas globais para todos os efeitos, aquelas localizadas dentro de uma técnica são locais para essa técnica.</span><span class="sxs-lookup"><span data-stu-id="57b83-118">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="57b83-119">Você pode acessar qualquer variável de efeito local não estática usando seu nome ou com um índice.</span><span class="sxs-lookup"><span data-stu-id="57b83-119">You can access any local non-static effect variable using its name or with an index.</span></span>

<span data-ttu-id="57b83-120">O método retornará um ponteiro para uma [**interface variável de efeito**](id3dx11effectvariable.md) se uma variável não for encontrada; Você pode chamar [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) para verificar se o índice existe ou não.</span><span class="sxs-lookup"><span data-stu-id="57b83-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the index exists.</span></span>

> [!Note]  
> <span data-ttu-id="57b83-121">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="57b83-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="57b83-122">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="57b83-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="57b83-123">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="57b83-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57b83-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57b83-124">Requirements</span></span>



| <span data-ttu-id="57b83-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="57b83-125">Requirement</span></span> | <span data-ttu-id="57b83-126">Valor</span><span class="sxs-lookup"><span data-stu-id="57b83-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57b83-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57b83-127">Header</span></span><br/>  | <dl> <span data-ttu-id="57b83-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="57b83-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="57b83-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57b83-129">Library</span></span><br/> | <dl> <span data-ttu-id="57b83-130"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="57b83-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57b83-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="57b83-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b83-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="57b83-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


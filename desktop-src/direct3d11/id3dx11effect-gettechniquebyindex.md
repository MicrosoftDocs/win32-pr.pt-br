---
title: Método ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
description: Obtenha uma técnica por índice. | Método ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: ee9c0cc3-0ca1-42e8-bd37-5878fd56cff1
keywords:
- Método GetTechniqueByIndex Direct3D 11
- Método GetTechniqueByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d3be5ec403fb25ab3a49792ed77fd4d96bf571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930698"
---
# <a name="id3dx11effectgettechniquebyindex-method"></a><span data-ttu-id="3f903-107">Método ID3DX11Effect:: GetTechniqueByIndex</span><span class="sxs-lookup"><span data-stu-id="3f903-107">ID3DX11Effect::GetTechniqueByIndex method</span></span>

<span data-ttu-id="3f903-108">Obtenha uma técnica por índice.</span><span class="sxs-lookup"><span data-stu-id="3f903-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f903-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f903-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="3f903-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f903-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f903-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="3f903-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="3f903-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f903-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3f903-113">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="3f903-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f903-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f903-114">Return value</span></span>

<span data-ttu-id="3f903-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f903-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="3f903-116">Um ponteiro para um [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="3f903-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f903-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f903-117">Remarks</span></span>

<span data-ttu-id="3f903-118">Um efeito contém uma ou mais técnicas; cada técnica contém uma ou mais passagens.</span><span class="sxs-lookup"><span data-stu-id="3f903-118">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="3f903-119">Você pode acessar uma técnica usando seu nome ou com um índice.</span><span class="sxs-lookup"><span data-stu-id="3f903-119">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="3f903-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="3f903-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3f903-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="3f903-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3f903-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3f903-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f903-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f903-123">Requirements</span></span>



| <span data-ttu-id="3f903-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f903-124">Requirement</span></span> | <span data-ttu-id="3f903-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3f903-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f903-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f903-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3f903-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f903-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3f903-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f903-128">Library</span></span><br/> | <dl> <span data-ttu-id="3f903-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="3f903-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f903-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f903-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f903-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="3f903-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


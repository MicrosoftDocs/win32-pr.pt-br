---
title: Método ID3DX11EffectTechnique GetPassByName (D3dx11effect. h)
description: Obter uma passagem por nome.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Método GetPassByName Direct3D 11
- Método GetPassByName Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, método GetPassByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bbe9b954efff12e458ee6172665118a7b8ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989328"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a><span data-ttu-id="eaaa1-106">Método ID3DX11EffectTechnique:: GetPassByName</span><span class="sxs-lookup"><span data-stu-id="eaaa1-106">ID3DX11EffectTechnique::GetPassByName method</span></span>

<span data-ttu-id="eaaa1-107">Obter uma passagem por nome.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-107">Get a pass by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaaa1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eaaa1-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="eaaa1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eaaa1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaaa1-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="eaaa1-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="eaaa1-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaaa1-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eaaa1-112">O nome da passagem.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-112">The name of the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaaa1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eaaa1-113">Return value</span></span>

<span data-ttu-id="eaaa1-114">Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="eaaa1-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="eaaa1-115">Um ponteiro para um [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="eaaa1-115">A pointer to an [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eaaa1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="eaaa1-116">Remarks</span></span>

<span data-ttu-id="eaaa1-117">Uma técnica contém uma ou mais passagens; Obtenha uma passagem usando um nome ou um índice.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="eaaa1-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="eaaa1-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="eaaa1-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="eaaa1-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="eaaa1-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eaaa1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaaa1-121">Requirements</span></span>



| <span data-ttu-id="eaaa1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaaa1-122">Requirement</span></span> | <span data-ttu-id="eaaa1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="eaaa1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaaa1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eaaa1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="eaaa1-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaaa1-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="eaaa1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eaaa1-126">Library</span></span><br/> | <dl> <span data-ttu-id="eaaa1-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="eaaa1-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaaa1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="eaaa1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaaa1-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="eaaa1-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 


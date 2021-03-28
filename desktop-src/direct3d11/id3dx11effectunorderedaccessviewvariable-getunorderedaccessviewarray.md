---
title: Método ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessViewArray (D3dx11effect. h)
description: Obter uma matriz de exibições de acesso não ordenado.
ms.assetid: 38f838bb-cdcb-43c2-8b98-a188f479e93d
keywords:
- Método GetUnorderedAccessViewArray Direct3D 11
- Método GetUnorderedAccessViewArray Direct3D 11, interface ID3DX11EffectUnorderedAccessViewVariable
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, método GetUnorderedAccessViewArray
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c264b5652287676d0792027f4f0ea8921bdb92f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173077"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessviewarray-method"></a><span data-ttu-id="77793-106">Método ID3DX11EffectUnorderedAccessViewVariable:: GetUnorderedAccessViewArray</span><span class="sxs-lookup"><span data-stu-id="77793-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="77793-107">Obter uma matriz de exibições de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="77793-107">Get an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="77793-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77793-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="77793-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77793-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77793-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="77793-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="77793-111">Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="77793-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="77793-112">Ponteiro para um ponteiro [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) que será definido para a matriz UAV no retorno.</span><span class="sxs-lookup"><span data-stu-id="77793-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set to the UAV array on return.</span></span>

</dd> <dt>

<span data-ttu-id="77793-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="77793-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="77793-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77793-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77793-115">Índice da primeira interface.</span><span class="sxs-lookup"><span data-stu-id="77793-115">Index of the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="77793-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="77793-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="77793-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77793-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77793-118">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="77793-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77793-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77793-119">Return value</span></span>

<span data-ttu-id="77793-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77793-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77793-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="77793-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="77793-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="77793-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="77793-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="77793-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="77793-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="77793-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="77793-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="77793-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="77793-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77793-126">Requirements</span></span>



| <span data-ttu-id="77793-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="77793-127">Requirement</span></span> | <span data-ttu-id="77793-128">Valor</span><span class="sxs-lookup"><span data-stu-id="77793-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77793-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77793-129">Header</span></span><br/>  | <dl> <span data-ttu-id="77793-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="77793-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="77793-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77793-131">Library</span></span><br/> | <dl> <span data-ttu-id="77793-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="77793-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77793-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="77793-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77793-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="77793-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 


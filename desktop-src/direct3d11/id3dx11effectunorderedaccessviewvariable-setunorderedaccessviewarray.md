---
title: Método ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessViewArray (D3dx11effect. h)
description: Defina uma matriz de modos de exibição de acesso não ordenado.
ms.assetid: 12d0da06-990a-42b2-9566-cc5136f48781
keywords:
- Método SetUnorderedAccessViewArray Direct3D 11
- Método SetUnorderedAccessViewArray Direct3D 11, interface ID3DX11EffectUnorderedAccessViewVariable
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, método SetUnorderedAccessViewArray
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053856f294906cf56acf1f38ca90663ebcc34051
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989280"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessviewarray-method"></a><span data-ttu-id="bede3-106">Método ID3DX11EffectUnorderedAccessViewVariable:: SetUnorderedAccessViewArray</span><span class="sxs-lookup"><span data-stu-id="bede3-106">ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="bede3-107">Defina uma matriz de modos de exibição de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="bede3-107">Set an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="bede3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bede3-108">Syntax</span></span>


```C++
HRESULT SetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="bede3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bede3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bede3-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="bede3-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="bede3-111">Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="bede3-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="bede3-112">Uma matriz de ponteiros [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) .</span><span class="sxs-lookup"><span data-stu-id="bede3-112">An array of [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="bede3-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="bede3-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="bede3-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bede3-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bede3-115">Índice da primeira exibição de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="bede3-115">Index of the first unordered-access-view.</span></span>

</dd> <dt>

<span data-ttu-id="bede3-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="bede3-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="bede3-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bede3-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bede3-118">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="bede3-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bede3-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bede3-119">Return value</span></span>

<span data-ttu-id="bede3-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bede3-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bede3-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bede3-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bede3-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="bede3-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bede3-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="bede3-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bede3-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="bede3-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bede3-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bede3-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bede3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bede3-126">Requirements</span></span>



| <span data-ttu-id="bede3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bede3-127">Requirement</span></span> | <span data-ttu-id="bede3-128">Valor</span><span class="sxs-lookup"><span data-stu-id="bede3-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bede3-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bede3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bede3-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bede3-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bede3-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bede3-131">Library</span></span><br/> | <dl> <span data-ttu-id="bede3-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="bede3-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bede3-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="bede3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bede3-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="bede3-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 


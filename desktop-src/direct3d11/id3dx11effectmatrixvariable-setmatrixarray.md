---
title: Método ID3DX11EffectMatrixVariable SetMatrixArray (D3dx11effect. h)
description: Defina uma matriz de matrizes de ponto flutuante.
ms.assetid: c90d621c-7500-49c3-ab40-2d0630fc4bec
keywords:
- Método SetMatrixArray Direct3D 11
- Método SetMatrixArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, método SetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffe0f6a81e0086a9afd6da9e464f09ae577dab2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968638"
---
# <a name="id3dx11effectmatrixvariablesetmatrixarray-method"></a><span data-ttu-id="e9aa0-106">Método ID3DX11EffectMatrixVariable:: SetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="e9aa0-106">ID3DX11EffectMatrixVariable::SetMatrixArray method</span></span>

<span data-ttu-id="e9aa0-107">Defina uma matriz de matrizes de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-107">Set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9aa0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9aa0-108">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="e9aa0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9aa0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9aa0-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="e9aa0-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="e9aa0-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="e9aa0-111">Type: **float\***</span></span>

<span data-ttu-id="e9aa0-112">Um ponteiro para a primeira matriz.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-112">A pointer to the first matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e9aa0-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="e9aa0-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="e9aa0-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9aa0-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9aa0-115">O número de elementos de matriz a serem ignorados do início da matriz.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-115">The number of matrix elements to skip from the start of the array.</span></span>

</dd> <dt>

<span data-ttu-id="e9aa0-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="e9aa0-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="e9aa0-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9aa0-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9aa0-118">O número de elementos a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-118">The number of elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9aa0-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9aa0-119">Return value</span></span>

<span data-ttu-id="e9aa0-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9aa0-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9aa0-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e9aa0-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9aa0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9aa0-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e9aa0-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e9aa0-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="e9aa0-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e9aa0-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e9aa0-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9aa0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9aa0-126">Requirements</span></span>



| <span data-ttu-id="e9aa0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9aa0-127">Requirement</span></span> | <span data-ttu-id="e9aa0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e9aa0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9aa0-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9aa0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e9aa0-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9aa0-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e9aa0-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9aa0-131">Library</span></span><br/> | <dl> <span data-ttu-id="e9aa0-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="e9aa0-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9aa0-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9aa0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9aa0-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="e9aa0-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 


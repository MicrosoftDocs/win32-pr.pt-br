---
title: Método ID3DX11EffectMatrixVariable SetMatrixTransposeArray (D3dx11effect. h)
description: Transpor e definir uma matriz de matrizes de ponto flutuante.
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- Método SetMatrixTransposeArray Direct3D 11
- Método SetMatrixTransposeArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, método SetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f70676b76658b5732c1a2ee15858f83694272b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930706"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a><span data-ttu-id="8a02a-106">Método ID3DX11EffectMatrixVariable:: SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="8a02a-106">ID3DX11EffectMatrixVariable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="8a02a-107">Transpor e definir uma matriz de matrizes de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="8a02a-107">Transpose and set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a02a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a02a-108">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="8a02a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a02a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a02a-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="8a02a-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="8a02a-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="8a02a-111">Type: **float\***</span></span>

<span data-ttu-id="8a02a-112">Um ponteiro para uma matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="8a02a-112">A pointer to an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="8a02a-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="8a02a-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="8a02a-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a02a-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a02a-115">O deslocamento (em número de matrizes) entre o início da matriz e a primeira matriz a ser definida.</span><span class="sxs-lookup"><span data-stu-id="8a02a-115">The offset (in number of matrices) between the start of the array and the first matrix to set.</span></span>

</dd> <dt>

<span data-ttu-id="8a02a-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="8a02a-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="8a02a-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a02a-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a02a-118">O número de matrizes na matriz a ser definido.</span><span class="sxs-lookup"><span data-stu-id="8a02a-118">The number of matrices in the array to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a02a-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a02a-119">Return value</span></span>

<span data-ttu-id="8a02a-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a02a-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a02a-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8a02a-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a02a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a02a-122">Remarks</span></span>

<span data-ttu-id="8a02a-123">A transposição de uma matriz reorganizará a ordem dos dados da ordem da coluna de linha para a ordem da linha de coluna (ou vice-versa).</span><span class="sxs-lookup"><span data-stu-id="8a02a-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="8a02a-124">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="8a02a-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8a02a-125">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="8a02a-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8a02a-126">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8a02a-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8a02a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a02a-127">Requirements</span></span>



| <span data-ttu-id="8a02a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a02a-128">Requirement</span></span> | <span data-ttu-id="8a02a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8a02a-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a02a-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a02a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8a02a-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a02a-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8a02a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a02a-132">Library</span></span><br/> | <dl> <span data-ttu-id="8a02a-133"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="8a02a-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a02a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a02a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a02a-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="8a02a-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 


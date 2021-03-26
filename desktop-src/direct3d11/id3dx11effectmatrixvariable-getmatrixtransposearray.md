---
title: Método ID3DX11EffectMatrixVariable GetMatrixTransposeArray (D3dx11effect. h)
description: Transpor e obter uma matriz de matrizes de ponto flutuante.
ms.assetid: cfcdbda0-b321-4e94-8d09-bb9d7ddfb4a5
keywords:
- Método GetMatrixTransposeArray Direct3D 11
- Método GetMatrixTransposeArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, método GetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d0a43e69ccf88c15d8296c024535dec42b3f31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968602"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtransposearray-method"></a><span data-ttu-id="5cfdb-106">Método ID3DX11EffectMatrixVariable:: GetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="5cfdb-106">ID3DX11EffectMatrixVariable::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="5cfdb-107">Transpor e obter uma matriz de matrizes de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="5cfdb-107">Transpose and get an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cfdb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cfdb-108">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="5cfdb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cfdb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cfdb-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="5cfdb-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="5cfdb-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="5cfdb-111">Type: **float\***</span></span>

<span data-ttu-id="5cfdb-112">Um ponteiro para o primeiro elemento de uma matriz das matrizes tranposed.</span><span class="sxs-lookup"><span data-stu-id="5cfdb-112">A pointer to the first element of an array of tranposed matrices.</span></span>

</dd> <dt>

<span data-ttu-id="5cfdb-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="5cfdb-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="5cfdb-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5cfdb-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5cfdb-115">O deslocamento (em número de matrizes) entre o início da matriz e a primeira matriz a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="5cfdb-115">The offset (in number of matrices) between the start of the array and the first matrix to get.</span></span>

</dd> <dt>

<span data-ttu-id="5cfdb-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="5cfdb-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="5cfdb-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5cfdb-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5cfdb-118">O número de matrizes na matriz a serem obtidas.</span><span class="sxs-lookup"><span data-stu-id="5cfdb-118">The number of matrices in the array to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cfdb-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5cfdb-119">Return value</span></span>

<span data-ttu-id="5cfdb-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5cfdb-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5cfdb-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5cfdb-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5cfdb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cfdb-122">Remarks</span></span>

<span data-ttu-id="5cfdb-123">A transposição de uma matriz reorganizará a ordem dos dados da ordem da coluna de linha para a ordem da linha de coluna (ou vice-versa).</span><span class="sxs-lookup"><span data-stu-id="5cfdb-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="5cfdb-124">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="5cfdb-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5cfdb-125">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="5cfdb-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5cfdb-126">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5cfdb-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5cfdb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cfdb-127">Requirements</span></span>



| <span data-ttu-id="5cfdb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cfdb-128">Requirement</span></span> | <span data-ttu-id="5cfdb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5cfdb-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cfdb-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5cfdb-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5cfdb-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cfdb-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5cfdb-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5cfdb-132">Library</span></span><br/> | <dl> <span data-ttu-id="5cfdb-133"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="5cfdb-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cfdb-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cfdb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cfdb-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="5cfdb-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 


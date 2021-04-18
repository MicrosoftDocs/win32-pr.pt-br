---
title: Método ID3DX11EffectMatrixVariable SetMatrixTranspose (D3dx11effect. h)
description: Transpor e definir uma matriz de ponto flutuante.
ms.assetid: 228546c9-0141-4e17-bc8f-bff7201825d7
keywords:
- Método SetMatrixTranspose Direct3D 11
- Método SetMatrixTranspose Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, método SetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daf77b6e2e9578dcbc6c9cfe80f57b149097c32
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968601"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtranspose-method"></a><span data-ttu-id="acc41-106">Método ID3DX11EffectMatrixVariable:: SetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="acc41-106">ID3DX11EffectMatrixVariable::SetMatrixTranspose method</span></span>

<span data-ttu-id="acc41-107">Transpor e definir uma matriz de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="acc41-107">Transpose and set a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc41-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acc41-108">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="acc41-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acc41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc41-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="acc41-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="acc41-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="acc41-111">Type: **float\***</span></span>

<span data-ttu-id="acc41-112">Um ponteiro para o primeiro elemento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="acc41-112">A pointer to the first element of a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acc41-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="acc41-113">Return value</span></span>

<span data-ttu-id="acc41-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="acc41-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="acc41-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="acc41-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="acc41-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="acc41-116">Remarks</span></span>

<span data-ttu-id="acc41-117">A transposição de uma matriz reorganizará a ordem dos dados da ordem da coluna de linha para a ordem da linha de coluna (ou vice-versa).</span><span class="sxs-lookup"><span data-stu-id="acc41-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="acc41-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="acc41-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="acc41-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="acc41-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="acc41-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="acc41-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="acc41-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acc41-121">Requirements</span></span>



| <span data-ttu-id="acc41-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="acc41-122">Requirement</span></span> | <span data-ttu-id="acc41-123">Valor</span><span class="sxs-lookup"><span data-stu-id="acc41-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acc41-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="acc41-124">Header</span></span><br/>  | <dl> <span data-ttu-id="acc41-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="acc41-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="acc41-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="acc41-126">Library</span></span><br/> | <dl> <span data-ttu-id="acc41-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="acc41-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acc41-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="acc41-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc41-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="acc41-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 






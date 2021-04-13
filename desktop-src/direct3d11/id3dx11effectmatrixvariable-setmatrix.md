---
title: Método setmatrix ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Defina uma matriz de ponto flutuante.
ms.assetid: 91c69bc0-c8c6-4232-8c70-801ac8ddbcda
keywords:
- Método setmatrix Direct3D 11
- Método setmatrix Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, método setmatrix
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af7b64e7391461efc47b6f65ca676b870174347
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968639"
---
# <a name="id3dx11effectmatrixvariablesetmatrix-method"></a><span data-ttu-id="84416-106">Método ID3DX11EffectMatrixVariable:: setmatrix</span><span class="sxs-lookup"><span data-stu-id="84416-106">ID3DX11EffectMatrixVariable::SetMatrix method</span></span>

<span data-ttu-id="84416-107">Defina uma matriz de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="84416-107">Set a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="84416-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84416-108">Syntax</span></span>


```C++
HRESULT SetMatrix(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="84416-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84416-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84416-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="84416-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="84416-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="84416-111">Type: **float\***</span></span>

<span data-ttu-id="84416-112">Um ponteiro para o primeiro elemento na matriz.</span><span class="sxs-lookup"><span data-stu-id="84416-112">A pointer to the first element in the matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84416-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84416-113">Return value</span></span>

<span data-ttu-id="84416-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="84416-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="84416-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="84416-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="84416-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="84416-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="84416-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="84416-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="84416-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="84416-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="84416-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="84416-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="84416-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84416-120">Requirements</span></span>



| <span data-ttu-id="84416-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="84416-121">Requirement</span></span> | <span data-ttu-id="84416-122">Valor</span><span class="sxs-lookup"><span data-stu-id="84416-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84416-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84416-123">Header</span></span><br/>  | <dl> <span data-ttu-id="84416-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="84416-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="84416-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84416-125">Library</span></span><br/> | <dl> <span data-ttu-id="84416-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="84416-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84416-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="84416-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84416-128">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="84416-128">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 






---
title: Método getmatrix ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Obter uma matriz.
ms.assetid: 1d0b20f2-6e43-414d-a161-65ce13bef1e0
keywords:
- Método getmatrix Direct3D 11
- Método getmatrix Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, método getmatrix
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14c2f196c4072d7f81a75045fe4703bf51ea338
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012127"
---
# <a name="id3dx11effectmatrixvariablegetmatrix-method"></a><span data-ttu-id="d1681-106">Método ID3DX11EffectMatrixVariable:: getmatrix</span><span class="sxs-lookup"><span data-stu-id="d1681-106">ID3DX11EffectMatrixVariable::GetMatrix method</span></span>

<span data-ttu-id="d1681-107">Obter uma matriz.</span><span class="sxs-lookup"><span data-stu-id="d1681-107">Get a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1681-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1681-108">Syntax</span></span>


```C++
HRESULT GetMatrix(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="d1681-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1681-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1681-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="d1681-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="d1681-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="d1681-111">Type: **float\***</span></span>

<span data-ttu-id="d1681-112">Um ponteiro para o primeiro elemento em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="d1681-112">A pointer to the first element in a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1681-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1681-113">Return value</span></span>

<span data-ttu-id="d1681-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1681-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1681-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d1681-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d1681-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1681-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d1681-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="d1681-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d1681-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="d1681-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d1681-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d1681-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d1681-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1681-120">Requirements</span></span>



| <span data-ttu-id="d1681-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1681-121">Requirement</span></span> | <span data-ttu-id="d1681-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d1681-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1681-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1681-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d1681-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1681-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d1681-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1681-125">Library</span></span><br/> | <dl> <span data-ttu-id="d1681-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="d1681-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1681-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1681-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1681-128">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="d1681-128">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 






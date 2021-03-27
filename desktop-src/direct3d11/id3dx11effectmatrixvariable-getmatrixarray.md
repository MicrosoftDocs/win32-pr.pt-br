---
title: Método ID3DX11EffectMatrixVariable GetMatrixArray (D3dx11effect. h)
description: Obtenha uma matriz de matrizes.
ms.assetid: a7598687-a11c-41ad-9fb6-2c16d12f5edc
keywords:
- Método GetMatrixArray Direct3D 11
- Método GetMatrixArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, método GetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a339bf6918868473966b6d79bcbe6b6aa3eaa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930658"
---
# <a name="id3dx11effectmatrixvariablegetmatrixarray-method"></a><span data-ttu-id="f8202-106">Método ID3DX11EffectMatrixVariable:: GetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="f8202-106">ID3DX11EffectMatrixVariable::GetMatrixArray method</span></span>

<span data-ttu-id="f8202-107">Obtenha uma matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="f8202-107">Get an array of matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8202-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8202-108">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="f8202-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8202-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8202-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="f8202-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="f8202-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="f8202-111">Type: **float\***</span></span>

<span data-ttu-id="f8202-112">Um ponteiro para o primeiro elemento da primeira matriz em uma matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="f8202-112">A pointer to the first element of the first matrix in an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="f8202-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="f8202-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="f8202-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8202-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8202-115">O deslocamento (em número de matrizes) entre o início da matriz e a primeira matriz retornados.</span><span class="sxs-lookup"><span data-stu-id="f8202-115">The offset (in number of matrices) between the start of the array and the first matrix returned.</span></span>

</dd> <dt>

<span data-ttu-id="f8202-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="f8202-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="f8202-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8202-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8202-118">O número de matrizes na matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="f8202-118">The number of matrices in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8202-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8202-119">Return value</span></span>

<span data-ttu-id="f8202-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8202-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8202-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f8202-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8202-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8202-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8202-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="f8202-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f8202-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="f8202-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f8202-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f8202-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8202-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8202-126">Requirements</span></span>



| <span data-ttu-id="f8202-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8202-127">Requirement</span></span> | <span data-ttu-id="f8202-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f8202-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8202-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8202-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f8202-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8202-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f8202-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8202-131">Library</span></span><br/> | <dl> <span data-ttu-id="f8202-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="f8202-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8202-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8202-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8202-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="f8202-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 


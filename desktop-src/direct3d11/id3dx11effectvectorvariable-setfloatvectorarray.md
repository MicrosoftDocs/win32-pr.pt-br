---
title: Método ID3DX11EffectVectorVariable SetFloatVectorArray (D3dx11effect. h)
description: Defina uma matriz de vetores de quatro componentes que contêm dados de ponto flutuante.
ms.assetid: f07edf0f-8a90-41bf-ae03-5a62a19e57e2
keywords:
- Método SetFloatVectorArray Direct3D 11
- Método SetFloatVectorArray Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, método SetFloatVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f8f731dd90251848095f899bdc141bbc1d6748
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968646"
---
# <a name="id3dx11effectvectorvariablesetfloatvectorarray-method"></a><span data-ttu-id="10eb6-106">Método ID3DX11EffectVectorVariable:: SetFloatVectorArray</span><span class="sxs-lookup"><span data-stu-id="10eb6-106">ID3DX11EffectVectorVariable::SetFloatVectorArray method</span></span>

<span data-ttu-id="10eb6-107">Defina uma matriz de vetores de quatro componentes que contêm dados de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="10eb6-107">Set an array of four-component vectors that contain floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="10eb6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10eb6-108">Syntax</span></span>


```C++
HRESULT SetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="10eb6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10eb6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10eb6-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="10eb6-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="10eb6-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="10eb6-111">Type: **float\***</span></span>

<span data-ttu-id="10eb6-112">Um ponteiro para o início dos dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="10eb6-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="10eb6-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="10eb6-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="10eb6-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="10eb6-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="10eb6-115">Deve ser definido como 0; Isso é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="10eb6-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="10eb6-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="10eb6-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="10eb6-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="10eb6-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="10eb6-118">O número de elementos da matriz a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="10eb6-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10eb6-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10eb6-119">Return value</span></span>

<span data-ttu-id="10eb6-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="10eb6-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="10eb6-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="10eb6-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="10eb6-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="10eb6-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="10eb6-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="10eb6-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="10eb6-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="10eb6-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="10eb6-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="10eb6-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="10eb6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10eb6-126">Requirements</span></span>



| <span data-ttu-id="10eb6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="10eb6-127">Requirement</span></span> | <span data-ttu-id="10eb6-128">Valor</span><span class="sxs-lookup"><span data-stu-id="10eb6-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10eb6-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10eb6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="10eb6-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="10eb6-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="10eb6-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10eb6-131">Library</span></span><br/> | <dl> <span data-ttu-id="10eb6-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="10eb6-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10eb6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="10eb6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10eb6-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="10eb6-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 


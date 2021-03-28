---
title: Método ID3DX11EffectVectorVariable SetIntVectorArray (D3dx11effect. h)
description: Defina uma matriz de vetores de quatro componentes que contenham dados inteiros.
ms.assetid: c9e522d7-5545-4b91-b6b3-6fad9a151cb0
keywords:
- Método SetIntVectorArray Direct3D 11
- Método SetIntVectorArray Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, método SetIntVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetIntVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7a450245c589feb41f7078120833cedc01c91d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930690"
---
# <a name="id3dx11effectvectorvariablesetintvectorarray-method"></a><span data-ttu-id="f2e80-106">Método ID3DX11EffectVectorVariable:: SetIntVectorArray</span><span class="sxs-lookup"><span data-stu-id="f2e80-106">ID3DX11EffectVectorVariable::SetIntVectorArray method</span></span>

<span data-ttu-id="f2e80-107">Defina uma matriz de vetores de quatro componentes que contenham dados inteiros.</span><span class="sxs-lookup"><span data-stu-id="f2e80-107">Set an array of four-component vectors that contain integer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e80-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2e80-108">Syntax</span></span>


```C++
HRESULT SetIntVectorArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="f2e80-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2e80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e80-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="f2e80-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e80-111">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="f2e80-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="f2e80-112">Um ponteiro para o início dos dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="f2e80-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="f2e80-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="f2e80-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e80-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f2e80-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f2e80-115">Deve ser definido como 0; Isso é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f2e80-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="f2e80-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="f2e80-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e80-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f2e80-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f2e80-118">O número de elementos da matriz a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="f2e80-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e80-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2e80-119">Return value</span></span>

<span data-ttu-id="f2e80-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2e80-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2e80-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f2e80-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2e80-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2e80-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f2e80-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="f2e80-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f2e80-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="f2e80-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f2e80-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f2e80-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2e80-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2e80-126">Requirements</span></span>



| <span data-ttu-id="f2e80-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e80-127">Requirement</span></span> | <span data-ttu-id="f2e80-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f2e80-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e80-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2e80-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f2e80-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2e80-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f2e80-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2e80-131">Library</span></span><br/> | <dl> <span data-ttu-id="f2e80-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="f2e80-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e80-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2e80-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e80-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="f2e80-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 


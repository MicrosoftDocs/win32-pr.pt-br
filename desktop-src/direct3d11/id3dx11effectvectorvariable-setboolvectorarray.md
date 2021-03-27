---
title: Método ID3DX11EffectVectorVariable SetBoolVectorArray (D3dx11effect. h)
description: Defina uma matriz de vetores de quatro componentes que contenham dados boolianos.
ms.assetid: 063735de-093c-4891-9a5c-fe1622da283b
keywords:
- Método SetBoolVectorArray Direct3D 11
- Método SetBoolVectorArray Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, método SetBoolVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetBoolVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ce1f34783390c4bcef55df81ba6c9a2215486cb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298743"
---
# <a name="id3dx11effectvectorvariablesetboolvectorarray-method"></a><span data-ttu-id="b265d-106">Método ID3DX11EffectVectorVariable:: SetBoolVectorArray</span><span class="sxs-lookup"><span data-stu-id="b265d-106">ID3DX11EffectVectorVariable::SetBoolVectorArray method</span></span>

<span data-ttu-id="b265d-107">Defina uma matriz de vetores de quatro componentes que contenham dados boolianos.</span><span class="sxs-lookup"><span data-stu-id="b265d-107">Set an array of four-component vectors that contain boolean data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b265d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b265d-108">Syntax</span></span>


```C++
HRESULT SetBoolVectorArray(
   BOOL *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="b265d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b265d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b265d-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="b265d-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="b265d-111">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="b265d-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="b265d-112">Um ponteiro para o início dos dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="b265d-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="b265d-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="b265d-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="b265d-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b265d-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b265d-115">Deve ser definido como 0; Isso é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b265d-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="b265d-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="b265d-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="b265d-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b265d-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b265d-118">O número de elementos da matriz a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="b265d-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b265d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b265d-119">Return value</span></span>

<span data-ttu-id="b265d-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b265d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b265d-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b265d-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b265d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b265d-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b265d-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="b265d-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b265d-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="b265d-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b265d-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b265d-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b265d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b265d-126">Requirements</span></span>



| <span data-ttu-id="b265d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b265d-127">Requirement</span></span> | <span data-ttu-id="b265d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b265d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b265d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b265d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b265d-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b265d-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b265d-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b265d-131">Library</span></span><br/> | <dl> <span data-ttu-id="b265d-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="b265d-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b265d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b265d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b265d-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="b265d-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 


---
title: Método ID3DX11EffectScalarVariable GetFloatArray (D3dx11effect. h)
description: Obter uma matriz de variáveis de ponto flutuante.
ms.assetid: e5e0dbee-47f5-46ed-89a0-01782345498f
keywords:
- Método GetFloatArray Direct3D 11
- Método GetFloatArray Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, método GetFloatArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloatArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc760b7b7b57172becee0b9df9765be4d097f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968683"
---
# <a name="id3dx11effectscalarvariablegetfloatarray-method"></a><span data-ttu-id="9c80c-106">Método ID3DX11EffectScalarVariable:: GetFloatArray</span><span class="sxs-lookup"><span data-stu-id="9c80c-106">ID3DX11EffectScalarVariable::GetFloatArray method</span></span>

<span data-ttu-id="9c80c-107">Obter uma matriz de variáveis de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="9c80c-107">Get an array of floating-point variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c80c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c80c-108">Syntax</span></span>


```C++
HRESULT GetFloatArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="9c80c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c80c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c80c-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="9c80c-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="9c80c-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="9c80c-111">Type: **float\***</span></span>

<span data-ttu-id="9c80c-112">Um ponteiro para o início dos dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="9c80c-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="9c80c-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="9c80c-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="9c80c-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9c80c-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9c80c-115">Deve ser definido como 0; Isso é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="9c80c-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="9c80c-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="9c80c-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="9c80c-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9c80c-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9c80c-118">O número de elementos da matriz a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="9c80c-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c80c-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c80c-119">Return value</span></span>

<span data-ttu-id="9c80c-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9c80c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9c80c-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9c80c-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c80c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c80c-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9c80c-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="9c80c-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9c80c-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="9c80c-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9c80c-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9c80c-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c80c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c80c-126">Requirements</span></span>



| <span data-ttu-id="9c80c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c80c-127">Requirement</span></span> | <span data-ttu-id="9c80c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9c80c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c80c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c80c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9c80c-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c80c-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9c80c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c80c-131">Library</span></span><br/> | <dl> <span data-ttu-id="9c80c-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="9c80c-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c80c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c80c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c80c-134">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="9c80c-134">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 


---
title: Método ID3DX11EffectStringVariable GetStringArray (D3dx11effect. h)
description: Obter uma matriz de cadeias de caracteres.
ms.assetid: 2cc45b2f-1851-49d2-8844-3e249c48f327
keywords:
- Método GetStringArray Direct3D 11
- Método GetStringArray Direct3D 11, interface ID3DX11EffectStringVariable
- Interface ID3DX11EffectStringVariable Direct3D 11, método GetStringArray
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetStringArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2050ebd7c9ae3735385a379e6ef7bdff0e1cfd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968561"
---
# <a name="id3dx11effectstringvariablegetstringarray-method"></a><span data-ttu-id="30b39-106">Método ID3DX11EffectStringVariable:: GetStringArray</span><span class="sxs-lookup"><span data-stu-id="30b39-106">ID3DX11EffectStringVariable::GetStringArray method</span></span>

<span data-ttu-id="30b39-107">Obter uma matriz de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="30b39-107">Get an array of strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b39-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30b39-108">Syntax</span></span>


```C++
HRESULT GetStringArray(
   LPCSTR *ppStrings,
   UINT   Offset,
   UINT   Count
);
```



## <a name="parameters"></a><span data-ttu-id="30b39-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30b39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30b39-110">*ppStrings*</span><span class="sxs-lookup"><span data-stu-id="30b39-110">*ppStrings*</span></span> 
</dt> <dd>

<span data-ttu-id="30b39-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="30b39-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="30b39-112">Um ponteiro para a primeira cadeia de caracteres na matriz.</span><span class="sxs-lookup"><span data-stu-id="30b39-112">A pointer to the first string in the array.</span></span>

</dd> <dt>

<span data-ttu-id="30b39-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="30b39-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="30b39-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30b39-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="30b39-115">O deslocamento (em número de cadeias de caracteres) entre o início da matriz e a primeira cadeia de caracteres a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="30b39-115">The offset (in number of strings) between the start of the array and the first string to get.</span></span>

</dd> <dt>

<span data-ttu-id="30b39-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="30b39-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="30b39-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30b39-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="30b39-118">O número de cadeias de caracteres na matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="30b39-118">The number of strings in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30b39-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30b39-119">Return value</span></span>

<span data-ttu-id="30b39-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30b39-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30b39-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="30b39-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30b39-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="30b39-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30b39-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="30b39-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="30b39-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="30b39-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="30b39-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="30b39-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30b39-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30b39-126">Requirements</span></span>



| <span data-ttu-id="30b39-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="30b39-127">Requirement</span></span> | <span data-ttu-id="30b39-128">Valor</span><span class="sxs-lookup"><span data-stu-id="30b39-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b39-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30b39-129">Header</span></span><br/>  | <dl> <span data-ttu-id="30b39-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="30b39-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="30b39-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30b39-131">Library</span></span><br/> | <dl> <span data-ttu-id="30b39-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="30b39-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b39-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="30b39-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b39-134">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="30b39-134">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 


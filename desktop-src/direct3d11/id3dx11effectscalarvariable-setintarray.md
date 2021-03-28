---
title: Método ID3DX11EffectScalarVariable SetIntArray (D3dx11effect. h)
description: Defina uma matriz de variáveis de inteiro.
ms.assetid: 27efb643-0762-4cd7-84ad-f82b2bb1584a
keywords:
- Método SetIntArray Direct3D 11
- Método SetIntArray Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, método SetIntArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetIntArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142a1686b9dde8f6a2c8f41d521ac085bd403ec0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968566"
---
# <a name="id3dx11effectscalarvariablesetintarray-method"></a><span data-ttu-id="cba05-106">Método ID3DX11EffectScalarVariable:: SetIntArray</span><span class="sxs-lookup"><span data-stu-id="cba05-106">ID3DX11EffectScalarVariable::SetIntArray method</span></span>

<span data-ttu-id="cba05-107">Defina uma matriz de variáveis de inteiro.</span><span class="sxs-lookup"><span data-stu-id="cba05-107">Set an array of integer variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba05-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cba05-108">Syntax</span></span>


```C++
HRESULT SetIntArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="cba05-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cba05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cba05-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="cba05-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="cba05-111">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="cba05-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cba05-112">Um ponteiro para o início dos dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="cba05-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="cba05-113">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="cba05-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="cba05-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cba05-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cba05-115">Deve ser definido como 0; Isso é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="cba05-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="cba05-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="cba05-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="cba05-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cba05-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cba05-118">O número de elementos da matriz a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="cba05-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cba05-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cba05-119">Return value</span></span>

<span data-ttu-id="cba05-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cba05-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cba05-121">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cba05-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cba05-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="cba05-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cba05-123">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="cba05-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cba05-124">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="cba05-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cba05-125">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cba05-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cba05-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cba05-126">Requirements</span></span>



| <span data-ttu-id="cba05-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cba05-127">Requirement</span></span> | <span data-ttu-id="cba05-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cba05-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cba05-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cba05-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cba05-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cba05-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cba05-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cba05-131">Library</span></span><br/> | <dl> <span data-ttu-id="cba05-132"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="cba05-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba05-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="cba05-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba05-134">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="cba05-134">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 


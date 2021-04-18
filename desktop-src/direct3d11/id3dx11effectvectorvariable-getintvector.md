---
title: Método ID3DX11EffectVectorVariable GetIntVector (D3dx11effect. h)
description: Obtenha um vetor de quatro componentes que contém dados inteiros.
ms.assetid: 27c75cfb-7c6f-43f4-9489-186006a60203
keywords:
- Método GetIntVector Direct3D 11
- Método GetIntVector Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, método GetIntVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e661ecce642cae4cf94a1bc35f92dc1afad16a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506513"
---
# <a name="id3dx11effectvectorvariablegetintvector-method"></a><span data-ttu-id="f8931-106">Método ID3DX11EffectVectorVariable:: GetIntVector</span><span class="sxs-lookup"><span data-stu-id="f8931-106">ID3DX11EffectVectorVariable::GetIntVector method</span></span>

<span data-ttu-id="f8931-107">Obtenha um vetor de quatro componentes que contém dados inteiros.</span><span class="sxs-lookup"><span data-stu-id="f8931-107">Get a four-component vector that contains integer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8931-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8931-108">Syntax</span></span>


```C++
HRESULT GetIntVector(
   int *pData
);
```



## <a name="parameters"></a><span data-ttu-id="f8931-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8931-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8931-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="f8931-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="f8931-111">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="f8931-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="f8931-112">Um ponteiro para o primeiro componente.</span><span class="sxs-lookup"><span data-stu-id="f8931-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8931-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8931-113">Return value</span></span>

<span data-ttu-id="f8931-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8931-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8931-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f8931-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8931-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8931-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8931-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="f8931-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f8931-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="f8931-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f8931-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f8931-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8931-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8931-120">Requirements</span></span>



| <span data-ttu-id="f8931-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8931-121">Requirement</span></span> | <span data-ttu-id="f8931-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f8931-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8931-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8931-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f8931-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8931-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f8931-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8931-125">Library</span></span><br/> | <dl> <span data-ttu-id="f8931-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="f8931-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8931-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8931-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8931-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="f8931-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 


---
title: Método ID3DX11EffectVectorVariable GetBoolVector (D3dx11effect. h)
description: Obtenha um vetor de quatro componentes que contém dados boolianos.
ms.assetid: ecaf5705-d13b-4d61-9766-d2ff183af789
keywords:
- Método GetBoolVector Direct3D 11
- Método GetBoolVector Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, método GetBoolVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetBoolVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a24563bd7c685579115e3b10309fb0a1c158c2e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968649"
---
# <a name="id3dx11effectvectorvariablegetboolvector-method"></a><span data-ttu-id="c1fcb-106">Método ID3DX11EffectVectorVariable:: GetBoolVector</span><span class="sxs-lookup"><span data-stu-id="c1fcb-106">ID3DX11EffectVectorVariable::GetBoolVector method</span></span>

<span data-ttu-id="c1fcb-107">Obtenha um vetor de quatro componentes que contém dados boolianos.</span><span class="sxs-lookup"><span data-stu-id="c1fcb-107">Get a four-component vector that contains boolean data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1fcb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1fcb-108">Syntax</span></span>


```C++
HRESULT GetBoolVector(
   BOOL *pData
);
```



## <a name="parameters"></a><span data-ttu-id="c1fcb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1fcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1fcb-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="c1fcb-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="c1fcb-111">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="c1fcb-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="c1fcb-112">Um ponteiro para o primeiro componente.</span><span class="sxs-lookup"><span data-stu-id="c1fcb-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1fcb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1fcb-113">Return value</span></span>

<span data-ttu-id="c1fcb-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1fcb-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c1fcb-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c1fcb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1fcb-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c1fcb-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="c1fcb-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c1fcb-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="c1fcb-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c1fcb-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c1fcb-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1fcb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1fcb-120">Requirements</span></span>



| <span data-ttu-id="c1fcb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1fcb-121">Requirement</span></span> | <span data-ttu-id="c1fcb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c1fcb-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fcb-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1fcb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c1fcb-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1fcb-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c1fcb-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1fcb-125">Library</span></span><br/> | <dl> <span data-ttu-id="c1fcb-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="c1fcb-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1fcb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1fcb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1fcb-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="c1fcb-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 


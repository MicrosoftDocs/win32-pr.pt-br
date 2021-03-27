---
title: Método ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessView (D3dx11effect. h)
description: Obtenha um modo de exibição de acesso não ordenado.
ms.assetid: 46f61c4f-b3ee-4058-99b9-a43ca6944fb2
keywords:
- Método GetUnorderedAccessView Direct3D 11
- Método GetUnorderedAccessView Direct3D 11, interface ID3DX11EffectUnorderedAccessViewVariable
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, método GetUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7743d15c2380ff4e38bdcae1d38bbd8905cbccda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989392"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessview-method"></a><span data-ttu-id="26ac4-106">Método ID3DX11EffectUnorderedAccessViewVariable:: GetUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="26ac4-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessView method</span></span>

<span data-ttu-id="26ac4-107">Obtenha um modo de exibição de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="26ac4-107">Get an unordered-access-view.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ac4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26ac4-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessView(
   ID3D11UnorderedAccessView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="26ac4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26ac4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26ac4-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="26ac4-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="26ac4-111">Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="26ac4-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="26ac4-112">Ponteiro para um ponteiro [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) que será definido no retorno.</span><span class="sxs-lookup"><span data-stu-id="26ac4-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26ac4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26ac4-113">Return value</span></span>

<span data-ttu-id="26ac4-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26ac4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26ac4-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="26ac4-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26ac4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="26ac4-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="26ac4-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="26ac4-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="26ac4-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="26ac4-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="26ac4-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="26ac4-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26ac4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26ac4-120">Requirements</span></span>



| <span data-ttu-id="26ac4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="26ac4-121">Requirement</span></span> | <span data-ttu-id="26ac4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="26ac4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26ac4-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26ac4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="26ac4-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="26ac4-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="26ac4-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26ac4-125">Library</span></span><br/> | <dl> <span data-ttu-id="26ac4-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="26ac4-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ac4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="26ac4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ac4-128">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="26ac4-128">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 






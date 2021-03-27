---
title: Método GetDesc de ID3DX11EffectGroup (D3dx11effect. h)
description: Obtém uma descrição do grupo.
ms.assetid: 04bb707a-be21-43d1-8d9d-5a84d29fda74
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc do Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c32d44e215a6c89a7d71e899d9839509cbe39417
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930682"
---
# <a name="id3dx11effectgroupgetdesc-method"></a><span data-ttu-id="b9e53-106">Método ID3DX11EffectGroup:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="b9e53-106">ID3DX11EffectGroup::GetDesc method</span></span>

<span data-ttu-id="b9e53-107">Obtém uma descrição do grupo.</span><span class="sxs-lookup"><span data-stu-id="b9e53-107">Gets a group description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e53-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9e53-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_GROUP_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="b9e53-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9e53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e53-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="b9e53-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="b9e53-111">Tipo: **[ **D3DX11 do \_ grupo de \_ Descrição**](d3dx11-group-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9e53-111">Type: **[**D3DX11\_GROUP\_DESC**](d3dx11-group-desc.md)\***</span></span>

<span data-ttu-id="b9e53-112">Um ponteiro para uma [**estrutura \_ \_ desc de grupo D3DX11**](d3dx11-group-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="b9e53-112">A pointer to a [**D3DX11\_GROUP\_DESC**](d3dx11-group-desc.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9e53-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9e53-113">Return value</span></span>

<span data-ttu-id="b9e53-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b9e53-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b9e53-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b9e53-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9e53-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9e53-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b9e53-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="b9e53-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b9e53-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="b9e53-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b9e53-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b9e53-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b9e53-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9e53-120">Requirements</span></span>



| <span data-ttu-id="b9e53-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9e53-121">Requirement</span></span> | <span data-ttu-id="b9e53-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b9e53-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e53-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9e53-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b9e53-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e53-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b9e53-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9e53-125">Library</span></span><br/> | <dl> <span data-ttu-id="b9e53-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="b9e53-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9e53-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9e53-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e53-128">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="b9e53-128">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

 






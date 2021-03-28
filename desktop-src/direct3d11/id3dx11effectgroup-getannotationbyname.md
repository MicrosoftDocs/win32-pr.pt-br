---
title: Método ID3DX11EffectGroup GetAnnotationByName (D3dx11effect. h)
description: Obter uma anotação por nome. | Método ID3DX11EffectGroup GetAnnotationByName (D3dx11effect. h)
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1880983785fcfea8a4cda4aa09c8baec2cfebf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989324"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a><span data-ttu-id="27677-107">Método ID3DX11EffectGroup:: GetAnnotationByName</span><span class="sxs-lookup"><span data-stu-id="27677-107">ID3DX11EffectGroup::GetAnnotationByName method</span></span>

<span data-ttu-id="27677-108">Obter uma anotação por nome.</span><span class="sxs-lookup"><span data-stu-id="27677-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="27677-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27677-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="27677-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27677-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27677-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="27677-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="27677-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="27677-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="27677-113">O nome da anotação.</span><span class="sxs-lookup"><span data-stu-id="27677-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27677-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27677-114">Return value</span></span>

<span data-ttu-id="27677-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="27677-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="27677-116">Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="27677-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="27677-117">Observe que, se a anotação não for encontrada, o **ID3DX11EffectVariable** retornado estará vazio.</span><span class="sxs-lookup"><span data-stu-id="27677-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="27677-118">O método [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) deve ser chamado para determinar se a anotação foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="27677-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="27677-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="27677-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="27677-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="27677-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="27677-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="27677-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="27677-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="27677-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27677-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27677-123">Requirements</span></span>



| <span data-ttu-id="27677-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="27677-124">Requirement</span></span> | <span data-ttu-id="27677-125">Valor</span><span class="sxs-lookup"><span data-stu-id="27677-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27677-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27677-126">Header</span></span><br/>  | <dl> <span data-ttu-id="27677-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="27677-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="27677-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27677-128">Library</span></span><br/> | <dl> <span data-ttu-id="27677-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="27677-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27677-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="27677-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27677-131">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="27677-131">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 


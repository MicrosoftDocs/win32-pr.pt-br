---
title: Método ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
description: Obtenha uma técnica por nome. | Método ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- Método GetTechniqueByName Direct3D 11
- Método GetTechniqueByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26b6067352d4ca898cc1fc970524040d407bda1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968654"
---
# <a name="id3dx11effectgettechniquebyname-method"></a><span data-ttu-id="462a6-107">Método ID3DX11Effect:: GetTechniqueByName</span><span class="sxs-lookup"><span data-stu-id="462a6-107">ID3DX11Effect::GetTechniqueByName method</span></span>

<span data-ttu-id="462a6-108">Obtenha uma técnica por nome.</span><span class="sxs-lookup"><span data-stu-id="462a6-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="462a6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="462a6-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="462a6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="462a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="462a6-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="462a6-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="462a6-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="462a6-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="462a6-113">O nome da técnica.</span><span class="sxs-lookup"><span data-stu-id="462a6-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="462a6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="462a6-114">Return value</span></span>

<span data-ttu-id="462a6-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="462a6-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="462a6-116">Um ponteiro para um [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="462a6-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span> <span data-ttu-id="462a6-117">Se uma técnica com o nome apropriado não for encontrada, uma técnica inválida será retornada.</span><span class="sxs-lookup"><span data-stu-id="462a6-117">If a technique with the appropriate name is not found an invalid technique is returned.</span></span> <span data-ttu-id="462a6-118">[**ID3DX11EffectTechnique:: IsValid**](id3dx11effecttechnique-isvalid.md) deve ser chamado na técnica retornada para determinar se ele é válido.</span><span class="sxs-lookup"><span data-stu-id="462a6-118">[**ID3DX11EffectTechnique::IsValid**](id3dx11effecttechnique-isvalid.md) should be called on the returned technique to determine whether it is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="462a6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="462a6-119">Remarks</span></span>

<span data-ttu-id="462a6-120">Um efeito contém uma ou mais técnicas; cada técnica contém uma ou mais passagens.</span><span class="sxs-lookup"><span data-stu-id="462a6-120">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="462a6-121">Você pode acessar uma técnica usando seu nome ou com um índice.</span><span class="sxs-lookup"><span data-stu-id="462a6-121">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="462a6-122">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="462a6-122">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="462a6-123">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="462a6-123">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="462a6-124">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="462a6-124">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="462a6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="462a6-125">Requirements</span></span>



| <span data-ttu-id="462a6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="462a6-126">Requirement</span></span> | <span data-ttu-id="462a6-127">Valor</span><span class="sxs-lookup"><span data-stu-id="462a6-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462a6-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="462a6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="462a6-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="462a6-129"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="462a6-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="462a6-130">Library</span></span><br/> | <dl> <span data-ttu-id="462a6-131"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="462a6-131"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="462a6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="462a6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="462a6-133">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="462a6-133">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


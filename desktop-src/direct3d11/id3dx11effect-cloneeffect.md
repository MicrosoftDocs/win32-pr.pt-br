---
title: Método ID3DX11Effect CloneEffect (D3dx11effect. h)
description: Cria uma cópia de uma interface de efeito.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Método CloneEffect Direct3D 11
- Método CloneEffect Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método CloneEffect
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968704"
---
# <a name="id3dx11effectcloneeffect-method"></a><span data-ttu-id="9a67d-106">Método ID3DX11Effect:: CloneEffect</span><span class="sxs-lookup"><span data-stu-id="9a67d-106">ID3DX11Effect::CloneEffect method</span></span>

<span data-ttu-id="9a67d-107">Cria uma cópia de uma interface de efeito.</span><span class="sxs-lookup"><span data-stu-id="9a67d-107">Creates a copy of an effect interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a67d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a67d-108">Syntax</span></span>


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a><span data-ttu-id="9a67d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a67d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a67d-110">*Sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="9a67d-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="9a67d-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a67d-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a67d-112">Sinalizadores que afetam a criação do efeito clonado.</span><span class="sxs-lookup"><span data-stu-id="9a67d-112">Flags affecting the creation of the cloned effect.</span></span> <span data-ttu-id="9a67d-113">Pode ser 0 ou um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a67d-113">Can be 0 or one of the following values.</span></span>



| <span data-ttu-id="9a67d-114">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="9a67d-114">Flag</span></span>                                    | <span data-ttu-id="9a67d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a67d-115">Description</span></span>                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a67d-116">D3DX11 \_ de \_ clonagem de efeito de clone não \_ \_ único</span><span class="sxs-lookup"><span data-stu-id="9a67d-116">D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE</span></span> | <span data-ttu-id="9a67d-117">Ignorar todos os qualificadores "únicos" em cbuffers.</span><span class="sxs-lookup"><span data-stu-id="9a67d-117">Ignore all "single" qualifiers on cbuffers.</span></span> <span data-ttu-id="9a67d-118">Todos os cbuffers terão seus próprios [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s criados no efeito clonado.</span><span class="sxs-lookup"><span data-stu-id="9a67d-118">All cbuffers will have their own [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s created in the cloned effect.</span></span> |



 

</dd> <dt>

<span data-ttu-id="9a67d-119">*ppClonedEffect*</span><span class="sxs-lookup"><span data-stu-id="9a67d-119">*ppClonedEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="9a67d-120">Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9a67d-120">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="9a67d-121">Ponteiro para um ponteiro [**ID3DX11Effect**](id3dx11effect.md) que será definido como a cópia do efeito.</span><span class="sxs-lookup"><span data-stu-id="9a67d-121">Pointer to an [**ID3DX11Effect**](id3dx11effect.md) pointer that will be set to the copy of the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a67d-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a67d-122">Return value</span></span>

<span data-ttu-id="9a67d-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a67d-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a67d-124">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9a67d-124">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a67d-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a67d-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9a67d-126">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="9a67d-126">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9a67d-127">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="9a67d-127">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9a67d-128">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9a67d-128">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a67d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a67d-129">Requirements</span></span>



| <span data-ttu-id="9a67d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a67d-130">Requirement</span></span> | <span data-ttu-id="9a67d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9a67d-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a67d-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a67d-132">Header</span></span><br/>  | <dl> <span data-ttu-id="9a67d-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a67d-133"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9a67d-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a67d-134">Library</span></span><br/> | <dl> <span data-ttu-id="9a67d-135"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="9a67d-135"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a67d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a67d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a67d-137">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="9a67d-137">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


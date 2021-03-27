---
title: Interface ID3DX11EffectStringVariable (D3dx11effect. h)
description: Uma interface de variável de cadeia de caracteres acessa uma variável de cadeia de caracteres.
ms.assetid: 8304d7cc-de30-41fe-af12-e11bf7ae32ce
keywords:
- Interface ID3DX11EffectStringVariable Direct3D 11
- Interface ID3DX11EffectStringVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45eb5e0825bd8487396ed850c9d79665e5f1044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989274"
---
# <a name="id3dx11effectstringvariable-interface"></a><span data-ttu-id="3fa6a-105">Interface ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="3fa6a-105">ID3DX11EffectStringVariable interface</span></span>

<span data-ttu-id="3fa6a-106">Uma interface de variável de cadeia de caracteres acessa uma variável de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3fa6a-106">A string-variable interface accesses a string variable.</span></span>

## <a name="members"></a><span data-ttu-id="3fa6a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3fa6a-107">Members</span></span>

<span data-ttu-id="3fa6a-108">A interface **ID3DX11EffectStringVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="3fa6a-108">The **ID3DX11EffectStringVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="3fa6a-109">**ID3DX11EffectStringVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3fa6a-109">**ID3DX11EffectStringVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="3fa6a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3fa6a-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3fa6a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3fa6a-111">Methods</span></span>

<span data-ttu-id="3fa6a-112">A interface **ID3DX11EffectStringVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3fa6a-112">The **ID3DX11EffectStringVariable** interface has these methods.</span></span>



| <span data-ttu-id="3fa6a-113">Método</span><span class="sxs-lookup"><span data-stu-id="3fa6a-113">Method</span></span>                                                               | <span data-ttu-id="3fa6a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fa6a-114">Description</span></span>                         |
|:---------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="3fa6a-115">**GetString**</span><span class="sxs-lookup"><span data-stu-id="3fa6a-115">**GetString**</span></span>](id3dx11effectstringvariable-getstring.md)           | <span data-ttu-id="3fa6a-116">Obter a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3fa6a-116">Get the string.</span></span><br/>          |
| [<span data-ttu-id="3fa6a-117">**GetStringArray**</span><span class="sxs-lookup"><span data-stu-id="3fa6a-117">**GetStringArray**</span></span>](id3dx11effectstringvariable-getstringarray.md) | <span data-ttu-id="3fa6a-118">Obter uma matriz de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3fa6a-118">Get an array of strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3fa6a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fa6a-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3fa6a-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="3fa6a-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3fa6a-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="3fa6a-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3fa6a-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3fa6a-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3fa6a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fa6a-123">Requirements</span></span>



| <span data-ttu-id="3fa6a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fa6a-124">Requirement</span></span> | <span data-ttu-id="3fa6a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3fa6a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa6a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fa6a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3fa6a-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fa6a-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3fa6a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fa6a-128">Library</span></span><br/> | <dl> <span data-ttu-id="3fa6a-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="3fa6a-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fa6a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fa6a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa6a-131">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="3fa6a-131">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="3fa6a-132">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="3fa6a-132">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3fa6a-133">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="3fa6a-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






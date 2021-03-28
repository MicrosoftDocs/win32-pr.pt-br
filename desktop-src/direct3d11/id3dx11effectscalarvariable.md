---
title: Interface ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Uma interface de variável escalar de efeito acessa valores escalares.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- Interface ID3DX11EffectScalarVariable Direct3D 11
- Interface ID3DX11EffectScalarVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d07f0d14ce37f9c84c20564189e1b8475e69887
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172934"
---
# <a name="id3dx11effectscalarvariable-interface"></a><span data-ttu-id="18ad6-105">Interface ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="18ad6-105">ID3DX11EffectScalarVariable interface</span></span>

<span data-ttu-id="18ad6-106">Uma interface de variável escalar de efeito acessa valores escalares.</span><span class="sxs-lookup"><span data-stu-id="18ad6-106">An effect-scalar-variable interface accesses scalar values.</span></span>

## <a name="members"></a><span data-ttu-id="18ad6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="18ad6-107">Members</span></span>

<span data-ttu-id="18ad6-108">A interface **ID3DX11EffectScalarVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="18ad6-108">The **ID3DX11EffectScalarVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="18ad6-109">**ID3DX11EffectScalarVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="18ad6-109">**ID3DX11EffectScalarVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="18ad6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="18ad6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="18ad6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="18ad6-111">Methods</span></span>

<span data-ttu-id="18ad6-112">A interface **ID3DX11EffectScalarVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="18ad6-112">The **ID3DX11EffectScalarVariable** interface has these methods.</span></span>



| <span data-ttu-id="18ad6-113">Método</span><span class="sxs-lookup"><span data-stu-id="18ad6-113">Method</span></span>                                                             | <span data-ttu-id="18ad6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="18ad6-114">Description</span></span>                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="18ad6-115">**Getbool**</span><span class="sxs-lookup"><span data-stu-id="18ad6-115">**GetBool**</span></span>](id3dx11effectscalarvariable-getbool.md)             | <span data-ttu-id="18ad6-116">Obter uma variável booliana.</span><span class="sxs-lookup"><span data-stu-id="18ad6-116">Get a boolean variable.</span></span><br/>                   |
| [<span data-ttu-id="18ad6-117">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="18ad6-117">**GetBoolArray**</span></span>](id3dx11effectscalarvariable-getboolarray.md)   | <span data-ttu-id="18ad6-118">Obter uma matriz de variáveis booleanas.</span><span class="sxs-lookup"><span data-stu-id="18ad6-118">Get an array of boolean variables.</span></span><br/>        |
| [<span data-ttu-id="18ad6-119">**GetFloat**</span><span class="sxs-lookup"><span data-stu-id="18ad6-119">**GetFloat**</span></span>](id3dx11effectscalarvariable-getfloat.md)           | <span data-ttu-id="18ad6-120">Obter uma variável de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="18ad6-120">Get a floating-point variable.</span></span><br/>            |
| [<span data-ttu-id="18ad6-121">**GetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="18ad6-121">**GetFloatArray**</span></span>](id3dx11effectscalarvariable-getfloatarray.md) | <span data-ttu-id="18ad6-122">Obter uma matriz de variáveis de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="18ad6-122">Get an array of floating-point variables.</span></span><br/> |
| [<span data-ttu-id="18ad6-123">**GetInt**</span><span class="sxs-lookup"><span data-stu-id="18ad6-123">**GetInt**</span></span>](id3dx11effectscalarvariable-getint.md)               | <span data-ttu-id="18ad6-124">Obter uma variável de inteiro.</span><span class="sxs-lookup"><span data-stu-id="18ad6-124">Get an integer variable.</span></span><br/>                  |
| [<span data-ttu-id="18ad6-125">**GetIntArray**</span><span class="sxs-lookup"><span data-stu-id="18ad6-125">**GetIntArray**</span></span>](id3dx11effectscalarvariable-getintarray.md)     | <span data-ttu-id="18ad6-126">Obter uma matriz de variáveis de inteiro.</span><span class="sxs-lookup"><span data-stu-id="18ad6-126">Get an array of integer variables.</span></span><br/>        |
| [<span data-ttu-id="18ad6-127">**Setbool**</span><span class="sxs-lookup"><span data-stu-id="18ad6-127">**SetBool**</span></span>](id3dx11effectscalarvariable-setbool.md)             | <span data-ttu-id="18ad6-128">Defina uma variável booliana.</span><span class="sxs-lookup"><span data-stu-id="18ad6-128">Set a boolean variable.</span></span><br/>                   |
| [<span data-ttu-id="18ad6-129">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="18ad6-129">**SetBoolArray**</span></span>](id3dx11effectscalarvariable-setboolarray.md)   | <span data-ttu-id="18ad6-130">Defina uma matriz de variáveis boolianas.</span><span class="sxs-lookup"><span data-stu-id="18ad6-130">Set an array of boolean variables.</span></span><br/>        |
| [<span data-ttu-id="18ad6-131">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="18ad6-131">**SetFloat**</span></span>](id3dx11effectscalarvariable-setfloat.md)           | <span data-ttu-id="18ad6-132">Defina uma variável de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="18ad6-132">Set a floating-point variable.</span></span><br/>            |
| [<span data-ttu-id="18ad6-133">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="18ad6-133">**SetFloatArray**</span></span>](id3dx11effectscalarvariable-setfloatarray.md) | <span data-ttu-id="18ad6-134">Defina uma matriz de variáveis de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="18ad6-134">Set an array of floating-point variables.</span></span><br/> |
| [<span data-ttu-id="18ad6-135">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="18ad6-135">**SetInt**</span></span>](id3dx11effectscalarvariable-setint.md)               | <span data-ttu-id="18ad6-136">Defina uma variável de inteiro.</span><span class="sxs-lookup"><span data-stu-id="18ad6-136">Set an integer variable.</span></span><br/>                  |
| [<span data-ttu-id="18ad6-137">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="18ad6-137">**SetIntArray**</span></span>](id3dx11effectscalarvariable-setintarray.md)     | <span data-ttu-id="18ad6-138">Defina uma matriz de variáveis de inteiro.</span><span class="sxs-lookup"><span data-stu-id="18ad6-138">Set an array of integer variables.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="18ad6-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="18ad6-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="18ad6-140">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="18ad6-140">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="18ad6-141">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="18ad6-141">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="18ad6-142">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="18ad6-142">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18ad6-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18ad6-143">Requirements</span></span>



| <span data-ttu-id="18ad6-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="18ad6-144">Requirement</span></span> | <span data-ttu-id="18ad6-145">Valor</span><span class="sxs-lookup"><span data-stu-id="18ad6-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ad6-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18ad6-146">Header</span></span><br/>  | <dl> <span data-ttu-id="18ad6-147"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ad6-147"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="18ad6-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18ad6-148">Library</span></span><br/> | <dl> <span data-ttu-id="18ad6-149"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="18ad6-149"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ad6-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="18ad6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ad6-151">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="18ad6-151">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="18ad6-152">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="18ad6-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="18ad6-153">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="18ad6-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






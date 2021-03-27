---
title: dcl_resource (sm4-ASM)
description: '\_recurso DCL (sm4-ASM)'
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638892"
---
# <a name="dcl_resource-sm4---asm"></a><span data-ttu-id="4adb6-103">\_recurso DCL (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4adb6-103">dcl\_resource (sm4 - asm)</span></span>

<span data-ttu-id="4adb6-104">Declara um recurso de entrada de sombreador não multiamostrado.</span><span class="sxs-lookup"><span data-stu-id="4adb6-104">Declares a non-multisampled shader-input resource.</span></span>



| <span data-ttu-id="4adb6-105">\_recurso DCL *TN*, *ResourceType*, *ReturnType (s)*</span><span class="sxs-lookup"><span data-stu-id="4adb6-105">dcl\_resource *tN*, *resourceType*, *returnType(s)*</span></span> |
|-----------------------------------------------------|



 

<span data-ttu-id="4adb6-106">Declara um recurso de entrada de sombreador com uma amostra.</span><span class="sxs-lookup"><span data-stu-id="4adb6-106">Declares a multisampled shader-input resource.</span></span>



| <span data-ttu-id="4adb6-107">\_recurso DCL *TN*, *tamanho do ResourceType \[ \] NN*, *ReturnType (s)*</span><span class="sxs-lookup"><span data-stu-id="4adb6-107">dcl\_resource *tN*, *resourceType\[size\]NN*, *returnType(s)*</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="4adb6-108">Item</span><span class="sxs-lookup"><span data-stu-id="4adb6-108">Item</span></span>                                                                                                                                                     | <span data-ttu-id="4adb6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4adb6-109">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4adb6-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span><span class="sxs-lookup"><span data-stu-id="4adb6-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span></span><br/>                                                                           | <span data-ttu-id="4adb6-111">\[no \] registro de textura, onde *N* é um inteiro que denota o número do registro.</span><span class="sxs-lookup"><span data-stu-id="4adb6-111">\[in\] The texture register, where *N* is an integer that denotes the register number.</span></span><br/>                                                                                                                                                                        |
| <span data-ttu-id="4adb6-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span><span class="sxs-lookup"><span data-stu-id="4adb6-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span></span><br/>                                   | <span data-ttu-id="4adb6-113">\[em \] qualquer tipo de objeto listado na página de [objeto de textura](dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4adb6-113">\[in\] Any object type listed in the [texture-object](dx-graphics-hlsl-to-type.md) page.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="4adb6-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*tamanho de resourceType \[ \] nn*</span><span class="sxs-lookup"><span data-stu-id="4adb6-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType\[size\]NN*</span></span><br/> | <span data-ttu-id="4adb6-115">\[em \] um tipo de objeto Texture2D ou Texture2DArray (consulte a página [Texture-Object](dx-graphics-hlsl-to-type.md) ); *size* é um inteiro opcional que denota o número de elementos na matriz; *NN* é um inteiro que denota o número de multiamostras.</span><span class="sxs-lookup"><span data-stu-id="4adb6-115">\[in\] A Texture2D or a Texture2DArray object type (see the [texture-object](dx-graphics-hlsl-to-type.md) page); *size* is an optional integer that denotes the number of elements in the array; *NN* is an integer that denotes the number of multisamples.</span></span><br/> |
| <span data-ttu-id="4adb6-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*</span><span class="sxs-lookup"><span data-stu-id="4adb6-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType(s)*</span></span><br/>                               | <span data-ttu-id="4adb6-117">\[no \] tipo de retorno por componente, que é um dos seguintes: UNORM, SNORM, Santo, uint ou float.</span><span class="sxs-lookup"><span data-stu-id="4adb6-117">\[in\] Per-component return type which is one of the following: UNORM, SNORM, SINT, UINT, or FLOAT.</span></span> <span data-ttu-id="4adb6-118">O número de tipos de retorno pode ser de até 1 (se todos os componentes forem do mesmo tipo), mas puder ser de até quatro.</span><span class="sxs-lookup"><span data-stu-id="4adb6-118">The number of return types can be as few as 1 (if all components are the same type), but can be as many as four.</span></span><br/>                                          |



 

<span data-ttu-id="4adb6-119">Um recurso é acessado no HLSL usando [Load](dx-graphics-hlsl-to-load.md); uma textura sem amostra também pode ser acessada usando qualquer um dos métodos de exemplo de [objeto de textura](dx-graphics-hlsl-to-type.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="4adb6-119">A resource is accessed in HLSL using [load](dx-graphics-hlsl-to-load.md); a non-multisampled texture can also be accessed using any of the HLSL [texture object](dx-graphics-hlsl-to-type.md) sample methods.</span></span>

<span data-ttu-id="4adb6-120">Se um recurso estiver associado a um estágio do sombreador, o formato de recurso será validado em relação ao tipo de retorno.</span><span class="sxs-lookup"><span data-stu-id="4adb6-120">If a resource is bound to a shader stage, the resource format will be validated against the return type.</span></span>

<span data-ttu-id="4adb6-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4adb6-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4adb6-122">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="4adb6-122">Vertex Shader</span></span> | <span data-ttu-id="4adb6-123">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="4adb6-123">Geometry Shader</span></span> | <span data-ttu-id="4adb6-124">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4adb6-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4adb6-125">x</span><span class="sxs-lookup"><span data-stu-id="4adb6-125">x</span></span>             | <span data-ttu-id="4adb6-126">x</span><span class="sxs-lookup"><span data-stu-id="4adb6-126">x</span></span>               | <span data-ttu-id="4adb6-127">x</span><span class="sxs-lookup"><span data-stu-id="4adb6-127">x</span></span>            |



 

<span data-ttu-id="4adb6-128">Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="4adb6-128">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="4adb6-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4adb6-129">Example</span></span>

<span data-ttu-id="4adb6-130">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="4adb6-130">Here is an example.</span></span>


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a><span data-ttu-id="4adb6-131">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4adb6-131">Minimum Shader Model</span></span>

<span data-ttu-id="4adb6-132">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4adb6-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4adb6-133">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4adb6-133">Shader Model</span></span>                                              | <span data-ttu-id="4adb6-134">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4adb6-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4adb6-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4adb6-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4adb6-136">sim</span><span class="sxs-lookup"><span data-stu-id="4adb6-136">yes</span></span>       |
| [<span data-ttu-id="4adb6-137">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="4adb6-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4adb6-138">sim</span><span class="sxs-lookup"><span data-stu-id="4adb6-138">yes</span></span>       |
| [<span data-ttu-id="4adb6-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4adb6-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4adb6-140">sim</span><span class="sxs-lookup"><span data-stu-id="4adb6-140">yes</span></span>       |
| [<span data-ttu-id="4adb6-141">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4adb6-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4adb6-142">não</span><span class="sxs-lookup"><span data-stu-id="4adb6-142">no</span></span>        |
| [<span data-ttu-id="4adb6-143">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4adb6-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4adb6-144">não</span><span class="sxs-lookup"><span data-stu-id="4adb6-144">no</span></span>        |
| [<span data-ttu-id="4adb6-145">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4adb6-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4adb6-146">não</span><span class="sxs-lookup"><span data-stu-id="4adb6-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4adb6-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4adb6-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4adb6-148">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4adb6-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






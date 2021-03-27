---
title: Tipo de Sombreador
description: A sintaxe para declarar uma variável de sombreador em um efeito mudou de Direct3D 9 para Direct3D 10.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- Tipo de sombreador HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967210"
---
# <a name="shader-type"></a><span data-ttu-id="fe39a-104">Tipo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="fe39a-104">Shader Type</span></span>

<span data-ttu-id="fe39a-105">A sintaxe para declarar uma variável de sombreador em um efeito mudou de Direct3D 9 para Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="fe39a-105">The syntax for declaring a shader variable in an effect changed from Direct3D 9 to Direct3D 10.</span></span>

## <a name="shader-type-for-direct3d-10"></a><span data-ttu-id="fe39a-106">Tipo de sombreador para Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="fe39a-106">Shader Type for Direct3D 10</span></span>

<span data-ttu-id="fe39a-107">Declare uma variável de sombreador dentro de uma passagem de efeito (no Direct3D 10) usando a sintaxe do tipo de sombreador:</span><span class="sxs-lookup"><span data-stu-id="fe39a-107">Declare a shader variable within an effect pass (in Direct3D 10) using the shader type syntax:</span></span>



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe39a-108">**SetPixelShader** Compile ( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile ( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile ( **ShaderTarget, ShaderFunction** );</span><span class="sxs-lookup"><span data-stu-id="fe39a-108">**SetPixelShader** Compile( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile( **ShaderTarget, ShaderFunction** );</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="fe39a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe39a-109">Parameters</span></span>



| <span data-ttu-id="fe39a-110">Item</span><span class="sxs-lookup"><span data-stu-id="fe39a-110">Item</span></span>                                                                                                                             | <span data-ttu-id="fe39a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe39a-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe39a-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span><span class="sxs-lookup"><span data-stu-id="fe39a-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span></span><br/>         | <span data-ttu-id="fe39a-113">A chamada à API do Direct3D que cria o objeto Shader.</span><span class="sxs-lookup"><span data-stu-id="fe39a-113">The Direct3D API call that creates the shader object.</span></span> <span data-ttu-id="fe39a-114">Pode ser: **SetPixelShader** ou **SetGeometryShader** ou **SetVertexShader**.</span><span class="sxs-lookup"><span data-stu-id="fe39a-114">Can be either: **SetPixelShader** or **SetGeometryShader** or **SetVertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="fe39a-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span><span class="sxs-lookup"><span data-stu-id="fe39a-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>         | <span data-ttu-id="fe39a-116">O modelo do sombreador a ser compilado.</span><span class="sxs-lookup"><span data-stu-id="fe39a-116">The shader model to compile against.</span></span> <span data-ttu-id="fe39a-117">Isso é válido para qualquer destino, incluindo todos os destinos do Direct3D 9 mais os destinos do [modelo do sombreador 4](dx-graphics-hlsl-sm4.md) : vs \_ 4 \_ 0, GS \_ 4 \_ 0 e PS \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="fe39a-117">This is valid for any target including all Direct3D 9 targets plus the [shader model 4](dx-graphics-hlsl-sm4.md) targets: vs\_4\_0, gs\_4\_0, and ps\_4\_0.</span></span><br/>                                                                                                                                                                                                                                          |
| <span data-ttu-id="fe39a-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="fe39a-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span></span><br/> | <span data-ttu-id="fe39a-119">Uma cadeia de caracteres ASCII que contém o nome da função de ponto de entrada do sombreador; Essa é a função que começa a execução quando o sombreador é invocado.</span><span class="sxs-lookup"><span data-stu-id="fe39a-119">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="fe39a-120">O (...) representa os argumentos do sombreador; Esses são os mesmos argumentos passados para a API de criação do sombreador: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) ou [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) ou [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="fe39a-120">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) or [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) or [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="fe39a-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fe39a-121">Example</span></span>

<span data-ttu-id="fe39a-122">Aqui está um exemplo que cria um sombreador de vértice e um objeto de sombreador de pixel, compilados para um modelo de sombreador específico.</span><span class="sxs-lookup"><span data-stu-id="fe39a-122">Here is an example that creates a vertex shader and pixel shader object, compiled for a particular shader model.</span></span> <span data-ttu-id="fe39a-123">No exemplo do Direct3D 10, não há um sombreador Geometry, portanto, o ponteiro está definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fe39a-123">In the Direct3D 10 example, there is no geometry shader, so the pointer is set to **NULL**.</span></span>


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a><span data-ttu-id="fe39a-124">Tipo de sombreador para Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="fe39a-124">Shader Type for Direct3D 9</span></span>

<span data-ttu-id="fe39a-125">Declare uma variável de sombreador dentro de uma passagem de efeito (para Direct3D 9) usando a sintaxe de tipo de sombreador:</span><span class="sxs-lookup"><span data-stu-id="fe39a-125">Declare a shader variable within an effect pass (for Direct3D 9) using the shader type syntax:</span></span>



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe39a-126">**PixelShader** = compilar **ShaderTarget ShaderFunction (...); VertexShader** = compilar **ShaderTarget ShaderFunction (...);**</span><span class="sxs-lookup"><span data-stu-id="fe39a-126">**PixelShader** = compile **ShaderTarget ShaderFunction(...);VertexShader** = compile **ShaderTarget ShaderFunction(...);**</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="fe39a-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe39a-127">Parameters</span></span>



| <span data-ttu-id="fe39a-128">Item</span><span class="sxs-lookup"><span data-stu-id="fe39a-128">Item</span></span>                                                                                                                                                 | <span data-ttu-id="fe39a-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe39a-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe39a-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span><span class="sxs-lookup"><span data-stu-id="fe39a-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span></span><br/>                                         | <span data-ttu-id="fe39a-131">Uma variável de sombreador, que representa o sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="fe39a-131">A shader variable, which represents the compiled shader.</span></span> <span data-ttu-id="fe39a-132">Pode ser: **PixelShader** ou **VertexShader**.</span><span class="sxs-lookup"><span data-stu-id="fe39a-132">Can be either: **PixelShader** or **VertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="fe39a-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span><span class="sxs-lookup"><span data-stu-id="fe39a-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>                             | <span data-ttu-id="fe39a-134">O [modelo do sombreador](dx-graphics-hlsl-models.md) a ser compilado; depende do tipo de variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fe39a-134">The [shader model](dx-graphics-hlsl-models.md) to compile against; depends on the type of shader variable.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="fe39a-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span><span class="sxs-lookup"><span data-stu-id="fe39a-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span></span><br/> | <span data-ttu-id="fe39a-136">Uma cadeia de caracteres ASCII que contém o nome da função de ponto de entrada do sombreador; Essa é a função que começa a execução quando o sombreador é invocado.</span><span class="sxs-lookup"><span data-stu-id="fe39a-136">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="fe39a-137">O (...) representa os argumentos do sombreador; Esses são os mesmos argumentos passados para a API de criação do sombreador: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) ou [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span><span class="sxs-lookup"><span data-stu-id="fe39a-137">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) or [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="fe39a-138">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fe39a-138">Example</span></span>

<span data-ttu-id="fe39a-139">Aqui está um exemplo de um sombreador de vértice e objeto de sombreador de pixel, compilado para um modelo de sombreador específico.</span><span class="sxs-lookup"><span data-stu-id="fe39a-139">Here is an example of a vertex shader and pixel shader object, compiled for a particular shader model.</span></span>


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a><span data-ttu-id="fe39a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe39a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe39a-141">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe39a-141">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 


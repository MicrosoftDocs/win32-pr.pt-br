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
# <a name="shader-type"></a>Tipo de Sombreador

A sintaxe para declarar uma variável de sombreador em um efeito mudou de Direct3D 9 para Direct3D 10.

## <a name="shader-type-for-direct3d-10"></a>Tipo de sombreador para Direct3D 10

Declare uma variável de sombreador dentro de uma passagem de efeito (no Direct3D 10) usando a sintaxe do tipo de sombreador:



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SetPixelShader** Compile ( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile ( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile ( **ShaderTarget, ShaderFunction** ); |



 

### <a name="parameters"></a>Parâmetros



| Item                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**<br/>         | A chamada à API do Direct3D que cria o objeto Shader. Pode ser: **SetPixelShader** ou **SetGeometryShader** ou **SetVertexShader**.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>         | O modelo do sombreador a ser compilado. Isso é válido para qualquer destino, incluindo todos os destinos do Direct3D 9 mais os destinos do [modelo do sombreador 4](dx-graphics-hlsl-sm4.md) : vs \_ 4 \_ 0, GS \_ 4 \_ 0 e PS \_ 4 \_ 0.<br/>                                                                                                                                                                                                                                          |
| <span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**<br/> | Uma cadeia de caracteres ASCII que contém o nome da função de ponto de entrada do sombreador; Essa é a função que começa a execução quando o sombreador é invocado. O (...) representa os argumentos do sombreador; Esses são os mesmos argumentos passados para a API de criação do sombreador: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) ou [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) ou [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).<br/> |



 

### <a name="example"></a>Exemplo

Aqui está um exemplo que cria um sombreador de vértice e um objeto de sombreador de pixel, compilados para um modelo de sombreador específico. No exemplo do Direct3D 10, não há um sombreador Geometry, portanto, o ponteiro está definido como **NULL**.


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



## <a name="shader-type-for-direct3d-9"></a>Tipo de sombreador para Direct3D 9

Declare uma variável de sombreador dentro de uma passagem de efeito (para Direct3D 9) usando a sintaxe de tipo de sombreador:



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| **PixelShader** = compilar **ShaderTarget ShaderFunction (...); VertexShader** = compilar **ShaderTarget ShaderFunction (...);** |



 

### <a name="parameters"></a>Parâmetros



| Item                                                                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**<br/>                                         | Uma variável de sombreador, que representa o sombreador compilado. Pode ser: **PixelShader** ou **VertexShader**.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>                             | O [modelo do sombreador](dx-graphics-hlsl-models.md) a ser compilado; depende do tipo de variável de sombreador.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**<br/> | Uma cadeia de caracteres ASCII que contém o nome da função de ponto de entrada do sombreador; Essa é a função que começa a execução quando o sombreador é invocado. O (...) representa os argumentos do sombreador; Esses são os mesmos argumentos passados para a API de criação do sombreador: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) ou [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).<br/> |



 

### <a name="example"></a>Exemplo

Aqui está um exemplo de um sombreador de vértice e objeto de sombreador de pixel, compilado para um modelo de sombreador específico.


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



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 


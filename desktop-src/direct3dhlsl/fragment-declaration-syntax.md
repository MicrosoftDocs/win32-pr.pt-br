---
title: Sintaxe de declaração de fragmento (Direct3D 9 HLSL)
description: Cada função de HLSL (linguagem de sombreamento de alto nível) da Microsoft pode ser convertida em um fragmento de sombreador com a adição de uma declaração de fragmento.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c9090caec35bfc5e46d7024bf6de44d865d4ad6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998303"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a>Sintaxe de declaração de fragmento (Direct3D 9 HLSL)

Cada função de HLSL (linguagem de sombreamento de alto nível) da Microsoft pode ser convertida em um fragmento de sombreador com a adição de uma declaração de fragmento.

## <a name="syntax"></a>Sintaxe


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



em que:



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fragmentKeyword   | Palavra-chave required. Pixelfragment ou vertexfragment.                                                                                                                                                                                             |
| Fragmentoname      | Uma cadeia de texto ASCII que especifica o nome do fragmento compilado.                                                                                                                                                                                       |
| Compilar \_ fragmento | Palavra-chave required.                                                                                                                                                                                                                                     |
| shaderProfile     | O modelo do sombreador a ser compilado. Qualquer perfil de sombreador de vértice válido (consulte [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) ou perfil de sombreador de pixel (consulte [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)). |
| FunctionName ()    | O nome da função de sombreador, seguido por parênteses.                                                                                                                                                                                                    |



 

Os parâmetros de fragmento compartilhados são marcados pela adição de um prefixo ' r \_ ' à sua semântica.


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



Neste exemplo, a semântica do r \_ PosWorld e do NormalWorld do r \_ identificam que esses dois parâmetros são parâmetros compartilhados entre outros fragmentos.

> [!Note]  
> O fragmento linker foi uma tecnologia Microsoft Direct3D 9 no D3DX 9. O vinculador de fragmento era uma ferramenta (Flink.exe), uma API do D3DX 9 e um aprimoramento de HLSL. O fragmento linker foi descartado a partir da versão do SDK do DirectX de agosto de 2009. O vinculador de fragmento nunca se aplica ao Microsoft Direct3D 10, Microsoft Direct3D 10,1 ou Microsoft Direct3D 11.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 

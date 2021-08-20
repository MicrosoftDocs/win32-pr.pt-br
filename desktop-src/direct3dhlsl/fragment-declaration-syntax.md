---
title: Sintaxe de declaração de fragmento (Direct3D 9 HLSL)
description: Cada função HLSL (Microsoft High Level Shader Language) pode ser convertida em um fragmento de sombreador com a adição de uma declaração de fragmento.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d0b9772a03efb13ba4cd4e928140e38a02f14ef2cff1fc37993bdd917b337095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089896"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a>Sintaxe de declaração de fragmento (Direct3D 9 HLSL)

Cada função HLSL (Microsoft High Level Shader Language) pode ser convertida em um fragmento de sombreador com a adição de uma declaração de fragmento.

## <a name="syntax"></a>Syntax


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



em que:



| Valor                  | Descrição                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fragmentKeyword   | Palavra-chave necessária. Pixelfragment ou vertexfragment.                                                                                                                                                                                             |
| FragmentName      | Uma cadeia de caracteres de texto ASCII que especifica o nome do fragmento compilado.                                                                                                                                                                                       |
| compilar \_ fragmento | Palavra-chave necessária.                                                                                                                                                                                                                                     |
| shaderProfile     | O modelo de sombreador no qual compilar. Qualquer perfil de sombreador de vértice válido (consulte [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) ou perfil de sombreador de pixel (consulte [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)). |
| FunctionName()    | O nome da função do sombreador, seguido por parênteses.                                                                                                                                                                                                    |



 

Os parâmetros de fragmento compartilhado são marcados adicionando um \_ prefixo 'r' à sua semântica.


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



Neste exemplo, a semântica r PosWorld e r NormalWorld identificam que esses dois parâmetros são \_ \_ parâmetros compartilhados entre outros fragmentos.

> [!Note]  
> O fragment linker era uma tecnologia do Microsoft Direct3D 9 no D3DX 9. O fragment linker era uma ferramenta (Flink.exe), uma API D3DX 9 e um aprimoramento de HLSL. O linker de fragmento foi descartado a partir da versão do SDK do DirectX de agosto de 2009. O linker de fragmento nunca se aplicou ao Microsoft Direct3D 10, ao Microsoft Direct3D 10.1 ou ao Microsoft Direct3D 11.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 

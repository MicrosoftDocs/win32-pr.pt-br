---
title: Interfaces e classes
description: O vínculo de sombreador dinâmico usa interfaces e classes HLSL (linguagem de sombreamento de alto nível) que são sintaticamente semelhantes às suas contrapartes do C++.
ms.assetid: 124a358d-30ab-4efe-88ed-1ff277d17b25
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71410caf7d80cb9dbcd0165c753d75cc8f5cbe00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366449"
---
# <a name="interfaces-and-classes"></a>Interfaces e classes

O vínculo de sombreador dinâmico usa interfaces e classes HLSL (linguagem de sombreamento de alto nível) que são sintaticamente semelhantes às suas contrapartes do C++. Isso permite que os sombreadores façam referência a instâncias de interface abstratas em tempo de compilação e deixem a resolução dessas instâncias para classes concretas para o aplicativo em tempo de execução.

As seções a seguir detalham como configurar um sombreador para usar interfaces e classes e como inicializar instâncias de interface no código do aplicativo.

-   [Declarando interfaces](#declaring-interfaces)
-   [Classes declaradoras](#declaring-classes)
-   [Declarações de instância de interface em um sombreador](#interface-instance-declarations-in-a-shader)
-   [Declarações de instância de classe em um sombreador](#class-instance-declarations-in-a-shader)
-   [Inicializando instâncias de interface em um aplicativo](#initializing-interface-instances-in-an-application)
-   [Tópicos relacionados](#related-topics)

## <a name="declaring-interfaces"></a>Declarando interfaces

Uma interface funciona de maneira semelhante a uma classe base abstrata em C++. Uma interface é declarada em um sombreador usando a palavra-chave interface e contém apenas declarações de método. Os métodos declarados em uma interface serão todos métodos virtuais em todas as classes derivadas da interface. Classes derivadas devem implementar todos os métodos declarados em uma interface. Observe que as interfaces são a única maneira de declarar métodos virtuais, não há nenhuma palavra-chave virtual como em C++ e as classes Connot declaram métodos virtuais.

O código de sombreador de exemplo a seguir declara duas interfaces.


```
interface iBaseLight
{
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};       

interface iBaseMaterial
{
   float3 GetAmbientColor(float2 vTexcoord);
   
   float3 GetDiffuseColor(float2 vTexcoord);

   int GetSpecularPower();

};
      
```



## <a name="declaring-classes"></a>Declarando Classes

Uma classe se comporta de forma semelhante às classes em C++. Uma classe é declarada com a palavra-chave class e pode conter variáveis e métodos de membro. Uma classe pode herdar de zero ou uma classe e zero ou mais interfaces. As classes devem implementar ou herdar implementações para todas as interfaces em sua cadeia de herança ou a classe não pode ser instanciada.

O código de sombreador de exemplo a seguir ilustra a derivação de uma classe de uma interface e de outra classe.


```
class cAmbientLight : iBaseLight
{
   float3            m_vLightColor;     
   bool     m_bEnable;
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};

class cHemiAmbientLight : cAmbientLight
{
   float4   m_vGroundColor;
   float4   m_vDirUp;
   float3 IlluminateAmbient(float3 vNormal);
};        
      
```



## <a name="interface-instance-declarations-in-a-shader"></a>Declarações de instância de interface em um sombreador

Uma instância de interface age como um espaço reservado para instâncias de classe que fornecem uma implementação dos métodos da interface. O uso de uma instância de uma interface permite que o código do sombreador chame um método sem saber qual implementação desse método será invocada. O código do sombreador declara uma ou mais instâncias para cada interface que ela define. Essas instâncias são usadas no código de sombreador de maneira semelhante aos ponteiros de classe base do C++.

O código de sombreador de exemplo a seguir ilustra a declaração de várias instâncias de interface e o uso deles no código do sombreador.


```
// Declare interface instances
iBaseLight     g_abstractAmbientLighting;
iBaseLight     g_abstractDirectLighting;
iBaseMaterial  g_abstractMaterial;

struct PS_INPUT
{
    float4 vPosition : SV_POSITION;
    float3 vNormal   : NORMAL;
    float2 vTexcoord : TEXCOORD0;
};

float4 PSMain( PS_INPUT Input ) : SV_TARGET
{ 
    float3 Ambient = (float3)0.0f;       
    Ambient = g_abstractMaterial.GetAmbientColor( Input.vTexcoord ) *         
        g_abstractAmbientLighting.IlluminateAmbient( Input.vNormal );

    float3 Diffuse = (float3)0.0f;  
    Diffuse += g_abstractMaterial.GetDiffuseColor( Input.vTexcoord ) * 
        g_abstractDirectLighting.IlluminateDiffuse( Input.vNormal );

    float3 Specular = (float3)0.0f;   
    Specular += g_abstractDirectLighting.IlluminateSpecular( Input.vNormal, 
        g_abstractMaterial.GetSpecularPower() );
     
    float3 Lighting = saturate( Ambient + Diffuse + Specular );
     
    return float4(Lighting,1.0f); 
}
```



## <a name="class-instance-declarations-in-a-shader"></a>Declarações de instância de classe em um sombreador

Cada classe que será usada no lugar de uma instância de interface deve ser declarada como uma variável em um buffer de constante ou criada pelo aplicativo em tempo de execução usando o método [**ID3D11ClassLinkage:: CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) . As instâncias de interface serão apontadas em instâncias de classe no código do aplicativo. As instâncias de classe podem ser referenciadas no código de sombreador como qualquer outra variável, mas uma classe derivada de uma interface normalmente será usada apenas com uma instância de interface e não será referenciada pelo código de sombreador diretamente.

O código de sombreador de exemplo a seguir ilustra a declaração de várias instâncias de classe.


```
cbuffer cbPerFrame : register( b0 )
{
   cAmbientLight     g_ambientLight;
   cHemiAmbientLight g_hemiAmbientLight;
   cDirectionalLight g_directionalLight;
   cEnvironmentLight g_environmentLight;
   float4            g_vEyeDir;   
};        
      
```



## <a name="initializing-interface-instances-in-an-application"></a>Inicializando instâncias de interface em um aplicativo

As instâncias de interface são inicializadas no código do aplicativo passando uma matriz de vínculo dinâmico que contém atribuições de interface para um dos métodos [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) setshadr.

Para criar uma matriz de vinculação dinâmica, use as etapas a seguir

1.  Crie um objeto de vinculação de classe usando [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  Crie o sombreador que usará a vinculação de classe dinâmica, passando o objeto de vinculação de classe como um parâmetro para a função CREATE do sombreador.
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  Crie um objeto [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) usando a função [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  Use o objeto de reflexo do sombreador para obter o número de instâncias de interface no sombreador usando o método [**ID3D11ShaderReflection:: GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) .
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  Crie uma matriz grande o suficiente para manter o número de instâncias de interface no sombreador.
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  Determine o índice na matriz que corresponde a cada instância de interface usando [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) e [**ID3D11ShaderReflectionVariable:: GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  Obtenha uma instância de classe para cada objeto de classe derivado de uma interface no sombreador usando [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  Defina instâncias de interface para instâncias de classe definindo a entrada correspondente na matriz de vinculação dinâmica.
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  Passe a matriz de vinculação dinâmica como um parâmetro para uma chamada setshadr.
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

[Vinculação dinâmica](overviews-direct3d-11-hlsl-dynamic-linking.md)
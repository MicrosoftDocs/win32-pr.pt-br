---
title: Definir estado de efeito (Direct3D 11)
description: Algumas constantes de efeito só precisam ser inicializadas.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df65e164c2df01f78ae9ea9ab83a547b977335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498624"
---
# <a name="set-effect-state-direct3d-11"></a>Definir estado de efeito (Direct3D 11)

Algumas constantes de efeito só precisam ser inicializadas. Depois de inicializado, o estado de efeito é definido como o dispositivo para todo o loop de processamento. Outras variáveis precisam ser atualizadas sempre que o loop de renderização é chamado. O código básico para definir variáveis de efeito é mostrado abaixo, para cada um dos tipos de variáveis.

Um efeito encapsula todo o estado de renderização necessário para fazer uma passagem de renderização. Em termos da API, há três tipos de estado encapsulados em um efeito.

-   [Estado de constante](#constant-state)
-   [Estado do sombreador](#shader-state)
-   [Estado de textura](#texture-state)

## <a name="constant-state"></a>Estado de constante

Primeiro, declare variáveis em um efeito usando tipos de dados HLSL.


```
//--------------------------------------------------------------------------------------
// Global variables
//--------------------------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
```



Em segundo lugar, declare variáveis no aplicativo que podem ser definidas pelo aplicativo e, em seguida, atualizará as variáveis de efeito.


```
           
    D3DXMATRIX  mWorldViewProjection;
    D3DXVECTOR3 vLightDir[MAX_LIGHTS];
    D3DXVECTOR4 vLightDiffuse[MAX_LIGHTS];
    D3DXMATRIX  mWorld;
    D3DXMATRIX  mView;
    D3DXMATRIX  mProj;

    // Get the projection and view matrix from the camera class
    mWorld = g_mCenterMesh * *g_Camera.GetWorldMatrix();
    mProj = *g_Camera.GetProjMatrix();
    mView = *g_Camera.GetViewMatrix();

    
OnD3D11CreateDevice()
{
  ...
    g_pLightDir = g_pEffect11->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect11->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect11->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect11->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect11->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect11->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect11->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect11->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



Em terceiro lugar, use os métodos Update para definir o valor das variáveis no aplicativo nas variáveis de efeito.


```
           
OnD3D11FrameRender()
{
    ...
    g_pLightDir->SetRawValue( vLightDir, 0, sizeof(D3DXVECTOR3)*MAX_LIGHTS );
    g_pLightDiffuse->SetFloatVectorArray( (float*)vLightDiffuse, 0, MAX_LIGHTS );
    g_pmWorldViewProjection->SetMatrix( (float*)&mWorldViewProjection );
    g_pmWorld->SetMatrix( (float*)&mWorld );
    g_pfTime->SetFloat( (float)fTime );
    g_pnNumLights->SetInt( g_nNumActiveLights );
}
```



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a>Duas maneiras de obter o estado em uma variável de efeito

Há duas maneiras de obter o estado contido em uma variável de efeito. Dado um efeito que foi carregado na memória.

Uma maneira é obter o estado de amostra de um [**ID3DX11EffectVariable**](id3dx11effectvariable.md) que foi convertido como uma interface de amostra.


```
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid() )
        hr = (l_pD3D11EffectVariable->GetBackingStore( 0, 
            &sampler_desc );
}
```



A outra maneira é obter o estado de amostra de um [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).


```
ID3D11SamplerState* l_ppSamplerState = NULL;
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid )
    {
        hr = l_pD3D11EffectVariable->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a>Estado do sombreador

O estado do sombreador é declarado e atribuído em uma técnica de efeito, em uma passagem.


```
VertexShader vsRenderScene = CompileShader( vs_4_0, RenderSceneVS( 1, true, true );  
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( vsRenderScene );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



Isso funcionará da mesma forma que se você não estivesse usando um efeito. Há três chamadas, uma para cada tipo de sombreador (vértice, geometria e pixel). O primeiro, SetVertexShader, chama [**ID3D11DeviceContext:: VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader). CompileShader é uma função de efeito especial que usa o perfil do sombreador (vs \_ 4 \_ 0) e o nome da função de sombreador de vértice (RenderVS). Em outras palavras, cada uma dessas chamadas CompileShader compila sua função de sombreador associada e retorna um ponteiro para o sombreador compilado.

Observe que nem todo o estado do sombreador deve ser definido. Essa passagem não inclui nenhuma chamada SetHullShader ou SetDomainShader, o que significa que os envoltória associados no momento e os sombreadores de domínio ficarão inalterados.

## <a name="texture-state"></a>Estado de textura

O estado de textura é um pouco mais complexo do que definir uma variável, porque os dados de textura não são simplesmente lidos como uma variável, ele é amostrado de uma textura. Portanto, você deve definir a variável de textura (assim como uma variável normal, exceto que ela usa um tipo de textura) e você deve definir as condições de amostragem. Aqui está um exemplo de uma declaração de variável de textura e a declaração de estado de amostragem correspondente.


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



Aqui está um exemplo de como definir uma textura de um aplicativo. Neste exemplo, a textura é armazenada nos dados de malha, que foi carregado quando o efeito foi criado.

A primeira etapa é obter um ponteiro para a textura do efeito (da malha).


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



A segunda etapa é especificar uma exibição para acessar a textura. A exibição define uma maneira geral de acessar os dados do recurso de textura.


```
   
OnD3D11FrameRender()
{
  ID3D11ShaderResourceView* pDiffuseRV = NULL;

  ...
  pDiffuseRV = g_Mesh11.GetMaterial(pSubset->MaterialID)->pDiffuseRV11;
  g_ptxDiffuse->SetResource( pDiffuseRV );
  ...
}   
```



Da perspectiva do aplicativo, as exibições de acesso não ordenado são tratadas de forma semelhante às exibições de recursos do sombreador. No entanto, no sombreador de pixel de efeito e nas funções de sombreador de computação, os dados de exibição de acesso não ordenados são lidos de/gravados diretamente. Você não pode obter uma amostra de uma exibição de acesso não ordenada.

Para obter mais informações sobre como exibir recursos, consulte [recursos](overviews-direct3d-11-resources.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um efeito (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 





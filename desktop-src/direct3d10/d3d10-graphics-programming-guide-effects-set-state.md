---
description: Algumas constantes de efeito só precisam ser inicializadas. Consulte o código básico para definir variáveis de efeito no Direct3D 10.
ms.assetid: 743261a8-fdd8-492e-be8a-4faeb9b6f986
title: Definir estado de efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df7133276b6392abca8d75eed16de896fb58f84
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404719"
---
# <a name="set-effect-state-direct3d-10"></a><span data-ttu-id="a0e41-104">Definir estado de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a0e41-104">Set Effect State (Direct3D 10)</span></span>

<span data-ttu-id="a0e41-105">Algumas constantes de efeito só precisam ser inicializadas.</span><span class="sxs-lookup"><span data-stu-id="a0e41-105">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="a0e41-106">Depois de inicializado, o estado de efeito é definido como o dispositivo para todo o loop de processamento.</span><span class="sxs-lookup"><span data-stu-id="a0e41-106">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="a0e41-107">Outras variáveis precisam ser atualizadas sempre que o loop de renderização é chamado.</span><span class="sxs-lookup"><span data-stu-id="a0e41-107">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="a0e41-108">O código básico para definir variáveis de efeito é mostrado abaixo, para cada um dos tipos de variáveis.</span><span class="sxs-lookup"><span data-stu-id="a0e41-108">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="a0e41-109">Um efeito encapsula todo o estado de renderização necessário para fazer uma passagem de renderização.</span><span class="sxs-lookup"><span data-stu-id="a0e41-109">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="a0e41-110">Em termos da API, há três tipos de estado encapsulados em um efeito.</span><span class="sxs-lookup"><span data-stu-id="a0e41-110">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="a0e41-111">Estado de constante</span><span class="sxs-lookup"><span data-stu-id="a0e41-111">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="a0e41-112">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="a0e41-112">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="a0e41-113">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="a0e41-113">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="a0e41-114">Estado de constante</span><span class="sxs-lookup"><span data-stu-id="a0e41-114">Constant State</span></span>

<span data-ttu-id="a0e41-115">Primeiro, declare variáveis em um efeito usando tipos de dados HLSL.</span><span class="sxs-lookup"><span data-stu-id="a0e41-115">First, declare variables in an effect using HLSL data types.</span></span>


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



<span data-ttu-id="a0e41-116">Em segundo lugar, declare variáveis no aplicativo que podem ser definidas pelo aplicativo e, em seguida, atualizará as variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="a0e41-116">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


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

    
OnD3D10CreateDevice()
{
  ...
    g_pLightDir = g_pEffect10->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect10->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect10->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect10->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect10->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect10->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect10->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect10->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



<span data-ttu-id="a0e41-117">Em terceiro lugar, use os métodos Update para definir o valor das variáveis no aplicativo nas variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="a0e41-117">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


```
           
OnD3D10FrameRender()
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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="a0e41-118">Duas maneiras de obter o estado em uma variável de efeito</span><span class="sxs-lookup"><span data-stu-id="a0e41-118">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="a0e41-119">Há duas maneiras de obter o estado contido em uma variável de efeito.</span><span class="sxs-lookup"><span data-stu-id="a0e41-119">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="a0e41-120">Dado um efeito que foi carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="a0e41-120">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="a0e41-121">Uma delas é obter o estado de amostra de uma [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) que foi convertida como uma interface de amostra.</span><span class="sxs-lookup"><span data-stu-id="a0e41-121">One way is to get the sampler state from an [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) that has been cast as a sampler interface.</span></span>


```
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
        hr = (l_pD3D10EffectVariable->AsSampler())->GetBackingStore( 0, 
            &sampler_desc );
}
```



<span data-ttu-id="a0e41-122">A outra maneira é obter o estado de amostra de uma [**interface ID3D10SamplerState**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span><span class="sxs-lookup"><span data-stu-id="a0e41-122">The other way is to get the sampler state from an [**ID3D10SamplerState Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span></span>


```
ID3D10SamplerState* l_ppSamplerState = NULL;
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
    {
        hr = (l_pD3D10EffectVariable->AsSampler())->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a><span data-ttu-id="a0e41-123">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="a0e41-123">Shader State</span></span>

<span data-ttu-id="a0e41-124">O estado do sombreador é declarado e atribuído em uma técnica de efeito, em uma passagem.</span><span class="sxs-lookup"><span data-stu-id="a0e41-124">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



<span data-ttu-id="a0e41-125">Isso funcionará da mesma forma que se você não estivesse usando um efeito.</span><span class="sxs-lookup"><span data-stu-id="a0e41-125">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="a0e41-126">Há três chamadas, uma para cada tipo de sombreador (vértice, geometria e pixel).</span><span class="sxs-lookup"><span data-stu-id="a0e41-126">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="a0e41-127">O primeiro, SetVertexShader, chama [**ID3D10Device:: VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span><span class="sxs-lookup"><span data-stu-id="a0e41-127">The first one, SetVertexShader, calls [**ID3D10Device::VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span></span> <span data-ttu-id="a0e41-128">CompileShader é uma função de efeito especial que usa o perfil do sombreador (vs \_ 4 \_ 0) e o nome da função de sombreador de vértice (RenderVS).</span><span class="sxs-lookup"><span data-stu-id="a0e41-128">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="a0e41-129">Em outras palavras, cada uma dessas chamadas SetXXXShader compila sua função de sombreador associada e retorna um ponteiro para o sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="a0e41-129">In other words, each of these SetXXXShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

## <a name="texture-state"></a><span data-ttu-id="a0e41-130">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="a0e41-130">Texture State</span></span>

<span data-ttu-id="a0e41-131">O estado de textura é um pouco mais complexo do que definir uma variável, porque os dados de textura não são simplesmente lidos como uma variável, ele é amostrado de uma textura.</span><span class="sxs-lookup"><span data-stu-id="a0e41-131">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="a0e41-132">Portanto, você deve definir a variável de textura (assim como uma variável normal, exceto que ela usa um tipo de textura) e você deve definir as condições de amostragem.</span><span class="sxs-lookup"><span data-stu-id="a0e41-132">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="a0e41-133">Aqui está um exemplo de uma declaração de variável de textura e a declaração de estado de amostragem correspondente.</span><span class="sxs-lookup"><span data-stu-id="a0e41-133">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="a0e41-134">Aqui está um exemplo de como definir uma textura de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a0e41-134">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="a0e41-135">Neste exemplo, a textura é armazenada nos dados de malha, que foi carregado quando o efeito foi criado.</span><span class="sxs-lookup"><span data-stu-id="a0e41-135">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="a0e41-136">A primeira etapa é obter um ponteiro para a textura do efeito (da malha).</span><span class="sxs-lookup"><span data-stu-id="a0e41-136">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D10EffectShaderResourceVariable* g_ptxDiffuse = NULL;

    // Obtain variables
    g_ptxDiffuse = g_pEffect10->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="a0e41-137">A segunda etapa é especificar uma exibição para acessar a textura.</span><span class="sxs-lookup"><span data-stu-id="a0e41-137">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="a0e41-138">A exibição define uma maneira geral de acessar os dados do recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="a0e41-138">The view defines a general way to access the data from the texture resource.</span></span>


```
   
OnD3D10FrameRender()
{
  ID3D10ShaderResourceView* pDiffuseRV = NULL;

   ...
   pDiffuseRV = g_Mesh10.GetMaterial(pSubset->MaterialID)->pDiffuseRV10;
   g_ptxDiffuse->SetResource( pDiffuseRV );
   ...
}   
```



<span data-ttu-id="a0e41-139">Para obter mais informações sobre como exibir recursos, consulte [modos de exibição de textura (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="a0e41-139">For more information about viewing resources, see [Texture Views (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0e41-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0e41-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0e41-141">Renderizando um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a0e41-141">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




---
title: Definir estado de efeito (Direct3D 11)
description: Algumas constantes de efeito só precisam ser inicializadas. Consulte o código básico para definir variáveis de efeito no Direct3D 12.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c64f9e642e867e9398722d4590a4c2ce9193b4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407659"
---
# <a name="set-effect-state-direct3d-11"></a><span data-ttu-id="ac885-104">Definir estado de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="ac885-104">Set Effect State (Direct3D 11)</span></span>

<span data-ttu-id="ac885-105">Algumas constantes de efeito só precisam ser inicializadas.</span><span class="sxs-lookup"><span data-stu-id="ac885-105">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="ac885-106">Depois de inicializado, o estado de efeito é definido como o dispositivo para todo o loop de renderização.</span><span class="sxs-lookup"><span data-stu-id="ac885-106">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="ac885-107">Outras variáveis precisam ser atualizadas sempre que o loop de renderização é chamado.</span><span class="sxs-lookup"><span data-stu-id="ac885-107">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="ac885-108">O código básico para definir variáveis de efeito é mostrado abaixo, para cada um dos tipos de variáveis.</span><span class="sxs-lookup"><span data-stu-id="ac885-108">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="ac885-109">Um efeito encapsula todo o estado de renderização necessário para fazer uma passagem de renderização.</span><span class="sxs-lookup"><span data-stu-id="ac885-109">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="ac885-110">Em termos da API, há três tipos de estado encapsulados em um efeito.</span><span class="sxs-lookup"><span data-stu-id="ac885-110">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="ac885-111">Estado constante</span><span class="sxs-lookup"><span data-stu-id="ac885-111">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="ac885-112">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="ac885-112">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="ac885-113">Estado da textura</span><span class="sxs-lookup"><span data-stu-id="ac885-113">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="ac885-114">Estado constante</span><span class="sxs-lookup"><span data-stu-id="ac885-114">Constant State</span></span>

<span data-ttu-id="ac885-115">Primeiro, declare variáveis em um efeito usando tipos de dados HLSL.</span><span class="sxs-lookup"><span data-stu-id="ac885-115">First, declare variables in an effect using HLSL data types.</span></span>


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



<span data-ttu-id="ac885-116">Em segundo lugar, declare variáveis no aplicativo que podem ser definidas pelo aplicativo e, em seguida, atualizará as variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="ac885-116">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


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



<span data-ttu-id="ac885-117">Em terceiro lugar, use os métodos de atualização para definir o valor das variáveis no aplicativo nas variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="ac885-117">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="ac885-118">Duas maneiras de obter o estado em uma variável de efeito</span><span class="sxs-lookup"><span data-stu-id="ac885-118">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="ac885-119">Há duas maneiras de obter o estado contido em uma variável de efeito.</span><span class="sxs-lookup"><span data-stu-id="ac885-119">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="ac885-120">Dado um efeito que foi carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="ac885-120">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="ac885-121">Uma maneira é obter o estado do amostrador de [**um ID3DX11EffectVariable**](id3dx11effectvariable.md) que foi lançado como uma interface de exemplo.</span><span class="sxs-lookup"><span data-stu-id="ac885-121">One way is to get the sampler state from an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) that has been cast as a sampler interface.</span></span>


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



<span data-ttu-id="ac885-122">A outra maneira é obter o estado do amostrador de [**um ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span><span class="sxs-lookup"><span data-stu-id="ac885-122">The other way is to get the sampler state from an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span></span>


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



## <a name="shader-state"></a><span data-ttu-id="ac885-123">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="ac885-123">Shader State</span></span>

<span data-ttu-id="ac885-124">O estado do sombreador é declarado e atribuído em uma técnica de efeito, dentro de uma passagem.</span><span class="sxs-lookup"><span data-stu-id="ac885-124">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


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



<span data-ttu-id="ac885-125">Isso funcionará da forma como funcionaria se você não estivesse usando um efeito.</span><span class="sxs-lookup"><span data-stu-id="ac885-125">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="ac885-126">Há três chamadas, uma para cada tipo de sombreador (vértice, geometria e pixel).</span><span class="sxs-lookup"><span data-stu-id="ac885-126">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="ac885-127">O primeiro, SetVertexShader, chama [**ID3D11DeviceContext::VSSetShader.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader)</span><span class="sxs-lookup"><span data-stu-id="ac885-127">The first one, SetVertexShader, calls [**ID3D11DeviceContext::VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader).</span></span> <span data-ttu-id="ac885-128">CompileShader é uma função de efeito especial que aceita o perfil do sombreador (vs 4 0) e o nome da função de sombreador de \_ vértice \_ (RenderVS).</span><span class="sxs-lookup"><span data-stu-id="ac885-128">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="ac885-129">Em outras palavras, cada uma dessas chamadas CompileShader compila sua função de sombreador associada e retorna um ponteiro para o sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="ac885-129">In other words, each of these CompileShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

<span data-ttu-id="ac885-130">Observe que nem todo o estado do sombreador deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="ac885-130">Note that not all shader state must be set.</span></span> <span data-ttu-id="ac885-131">Essa passagem não inclui nenhuma chamada SetHullShader ou SetDomainShader, o que significa que os sombreadores de chassi e domínio atualmente vinculados permanecerão inalterados.</span><span class="sxs-lookup"><span data-stu-id="ac885-131">This pass does not include any SetHullShader or SetDomainShader calls, meaning that the currently bound hull and domain shaders will be unchanged.</span></span>

## <a name="texture-state"></a><span data-ttu-id="ac885-132">Estado da textura</span><span class="sxs-lookup"><span data-stu-id="ac885-132">Texture State</span></span>

<span data-ttu-id="ac885-133">O estado de textura é um pouco mais complexo do que definir uma variável, pois os dados de textura não são simplesmente lidos como uma variável, são amostrados de uma textura.</span><span class="sxs-lookup"><span data-stu-id="ac885-133">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="ac885-134">Portanto, você deve definir a variável de textura (assim como uma variável normal, exceto que ela usa um tipo de textura) e definir as condições de amostragem.</span><span class="sxs-lookup"><span data-stu-id="ac885-134">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="ac885-135">Aqui está um exemplo de uma declaração de variável de textura e a declaração de estado de amostragem correspondente.</span><span class="sxs-lookup"><span data-stu-id="ac885-135">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="ac885-136">Aqui está um exemplo de como definir uma textura de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac885-136">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="ac885-137">Neste exemplo, a textura é armazenada nos dados da malha, que foram carregados quando o efeito foi criado.</span><span class="sxs-lookup"><span data-stu-id="ac885-137">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="ac885-138">A primeira etapa é obter um ponteiro para a textura do efeito (da malha).</span><span class="sxs-lookup"><span data-stu-id="ac885-138">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="ac885-139">A segunda etapa é especificar uma exibição para acessar a textura.</span><span class="sxs-lookup"><span data-stu-id="ac885-139">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="ac885-140">A exibição define uma maneira geral de acessar os dados do recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="ac885-140">The view defines a general way to access the data from the texture resource.</span></span>


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



<span data-ttu-id="ac885-141">Da perspectiva do aplicativo, as exibições de acesso não organizado são tratadas da mesma forma que as exibições de recurso do sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac885-141">From the application perspective, unordered access views are handled similarly to shader resource views.</span></span> <span data-ttu-id="ac885-142">No entanto, no efeito sombreador de pixel e funções de sombreador de computação, os dados de exibição de acesso não organizados são lidos/gravados diretamente.</span><span class="sxs-lookup"><span data-stu-id="ac885-142">However, in the effect pixel shader and compute shader functions, unordered access view data is read from/written to directly.</span></span> <span data-ttu-id="ac885-143">Não é possível amostrar de uma exibição de acesso não organizado.</span><span class="sxs-lookup"><span data-stu-id="ac885-143">You cannot sample from an unordered access view.</span></span>

<span data-ttu-id="ac885-144">Para obter mais informações sobre como exibir recursos, consulte [Recursos](overviews-direct3d-11-resources.md).</span><span class="sxs-lookup"><span data-stu-id="ac885-144">For more information about viewing resources, see [Resources](overviews-direct3d-11-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac885-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac885-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac885-146">Renderizar um efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="ac885-146">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 





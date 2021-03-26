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
# <a name="set-effect-state-direct3d-11"></a><span data-ttu-id="f97fc-103">Definir estado de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="f97fc-103">Set Effect State (Direct3D 11)</span></span>

<span data-ttu-id="f97fc-104">Algumas constantes de efeito só precisam ser inicializadas.</span><span class="sxs-lookup"><span data-stu-id="f97fc-104">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="f97fc-105">Depois de inicializado, o estado de efeito é definido como o dispositivo para todo o loop de processamento.</span><span class="sxs-lookup"><span data-stu-id="f97fc-105">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="f97fc-106">Outras variáveis precisam ser atualizadas sempre que o loop de renderização é chamado.</span><span class="sxs-lookup"><span data-stu-id="f97fc-106">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="f97fc-107">O código básico para definir variáveis de efeito é mostrado abaixo, para cada um dos tipos de variáveis.</span><span class="sxs-lookup"><span data-stu-id="f97fc-107">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="f97fc-108">Um efeito encapsula todo o estado de renderização necessário para fazer uma passagem de renderização.</span><span class="sxs-lookup"><span data-stu-id="f97fc-108">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="f97fc-109">Em termos da API, há três tipos de estado encapsulados em um efeito.</span><span class="sxs-lookup"><span data-stu-id="f97fc-109">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="f97fc-110">Estado de constante</span><span class="sxs-lookup"><span data-stu-id="f97fc-110">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="f97fc-111">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="f97fc-111">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="f97fc-112">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="f97fc-112">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="f97fc-113">Estado de constante</span><span class="sxs-lookup"><span data-stu-id="f97fc-113">Constant State</span></span>

<span data-ttu-id="f97fc-114">Primeiro, declare variáveis em um efeito usando tipos de dados HLSL.</span><span class="sxs-lookup"><span data-stu-id="f97fc-114">First, declare variables in an effect using HLSL data types.</span></span>


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



<span data-ttu-id="f97fc-115">Em segundo lugar, declare variáveis no aplicativo que podem ser definidas pelo aplicativo e, em seguida, atualizará as variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="f97fc-115">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


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



<span data-ttu-id="f97fc-116">Em terceiro lugar, use os métodos Update para definir o valor das variáveis no aplicativo nas variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="f97fc-116">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="f97fc-117">Duas maneiras de obter o estado em uma variável de efeito</span><span class="sxs-lookup"><span data-stu-id="f97fc-117">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="f97fc-118">Há duas maneiras de obter o estado contido em uma variável de efeito.</span><span class="sxs-lookup"><span data-stu-id="f97fc-118">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="f97fc-119">Dado um efeito que foi carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="f97fc-119">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="f97fc-120">Uma maneira é obter o estado de amostra de um [**ID3DX11EffectVariable**](id3dx11effectvariable.md) que foi convertido como uma interface de amostra.</span><span class="sxs-lookup"><span data-stu-id="f97fc-120">One way is to get the sampler state from an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) that has been cast as a sampler interface.</span></span>


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



<span data-ttu-id="f97fc-121">A outra maneira é obter o estado de amostra de um [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span><span class="sxs-lookup"><span data-stu-id="f97fc-121">The other way is to get the sampler state from an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span></span>


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



## <a name="shader-state"></a><span data-ttu-id="f97fc-122">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="f97fc-122">Shader State</span></span>

<span data-ttu-id="f97fc-123">O estado do sombreador é declarado e atribuído em uma técnica de efeito, em uma passagem.</span><span class="sxs-lookup"><span data-stu-id="f97fc-123">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


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



<span data-ttu-id="f97fc-124">Isso funcionará da mesma forma que se você não estivesse usando um efeito.</span><span class="sxs-lookup"><span data-stu-id="f97fc-124">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="f97fc-125">Há três chamadas, uma para cada tipo de sombreador (vértice, geometria e pixel).</span><span class="sxs-lookup"><span data-stu-id="f97fc-125">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="f97fc-126">O primeiro, SetVertexShader, chama [**ID3D11DeviceContext:: VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader).</span><span class="sxs-lookup"><span data-stu-id="f97fc-126">The first one, SetVertexShader, calls [**ID3D11DeviceContext::VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader).</span></span> <span data-ttu-id="f97fc-127">CompileShader é uma função de efeito especial que usa o perfil do sombreador (vs \_ 4 \_ 0) e o nome da função de sombreador de vértice (RenderVS).</span><span class="sxs-lookup"><span data-stu-id="f97fc-127">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="f97fc-128">Em outras palavras, cada uma dessas chamadas CompileShader compila sua função de sombreador associada e retorna um ponteiro para o sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="f97fc-128">In other words, each of these CompileShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

<span data-ttu-id="f97fc-129">Observe que nem todo o estado do sombreador deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="f97fc-129">Note that not all shader state must be set.</span></span> <span data-ttu-id="f97fc-130">Essa passagem não inclui nenhuma chamada SetHullShader ou SetDomainShader, o que significa que os envoltória associados no momento e os sombreadores de domínio ficarão inalterados.</span><span class="sxs-lookup"><span data-stu-id="f97fc-130">This pass does not include any SetHullShader or SetDomainShader calls, meaning that the currently bound hull and domain shaders will be unchanged.</span></span>

## <a name="texture-state"></a><span data-ttu-id="f97fc-131">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="f97fc-131">Texture State</span></span>

<span data-ttu-id="f97fc-132">O estado de textura é um pouco mais complexo do que definir uma variável, porque os dados de textura não são simplesmente lidos como uma variável, ele é amostrado de uma textura.</span><span class="sxs-lookup"><span data-stu-id="f97fc-132">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="f97fc-133">Portanto, você deve definir a variável de textura (assim como uma variável normal, exceto que ela usa um tipo de textura) e você deve definir as condições de amostragem.</span><span class="sxs-lookup"><span data-stu-id="f97fc-133">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="f97fc-134">Aqui está um exemplo de uma declaração de variável de textura e a declaração de estado de amostragem correspondente.</span><span class="sxs-lookup"><span data-stu-id="f97fc-134">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="f97fc-135">Aqui está um exemplo de como definir uma textura de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f97fc-135">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="f97fc-136">Neste exemplo, a textura é armazenada nos dados de malha, que foi carregado quando o efeito foi criado.</span><span class="sxs-lookup"><span data-stu-id="f97fc-136">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="f97fc-137">A primeira etapa é obter um ponteiro para a textura do efeito (da malha).</span><span class="sxs-lookup"><span data-stu-id="f97fc-137">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="f97fc-138">A segunda etapa é especificar uma exibição para acessar a textura.</span><span class="sxs-lookup"><span data-stu-id="f97fc-138">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="f97fc-139">A exibição define uma maneira geral de acessar os dados do recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="f97fc-139">The view defines a general way to access the data from the texture resource.</span></span>


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



<span data-ttu-id="f97fc-140">Da perspectiva do aplicativo, as exibições de acesso não ordenado são tratadas de forma semelhante às exibições de recursos do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f97fc-140">From the application perspective, unordered access views are handled similarly to shader resource views.</span></span> <span data-ttu-id="f97fc-141">No entanto, no sombreador de pixel de efeito e nas funções de sombreador de computação, os dados de exibição de acesso não ordenados são lidos de/gravados diretamente.</span><span class="sxs-lookup"><span data-stu-id="f97fc-141">However, in the effect pixel shader and compute shader functions, unordered access view data is read from/written to directly.</span></span> <span data-ttu-id="f97fc-142">Você não pode obter uma amostra de uma exibição de acesso não ordenada.</span><span class="sxs-lookup"><span data-stu-id="f97fc-142">You cannot sample from an unordered access view.</span></span>

<span data-ttu-id="f97fc-143">Para obter mais informações sobre como exibir recursos, consulte [recursos](overviews-direct3d-11-resources.md).</span><span class="sxs-lookup"><span data-stu-id="f97fc-143">For more information about viewing resources, see [Resources](overviews-direct3d-11-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f97fc-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f97fc-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f97fc-145">Renderizando um efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="f97fc-145">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 





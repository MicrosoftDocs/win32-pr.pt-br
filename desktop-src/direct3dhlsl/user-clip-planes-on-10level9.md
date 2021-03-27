---
title: Planos de corte do usuário no hardware de nível de recurso 9
description: A partir do Windows 8, a linguagem de sombreamento de alto nível (HLSL) da Microsoft oferece suporte a uma sintaxe que você pode usar com a API do Microsoft Direct3D 11 para especificar os planos de clipes de usuário no nível de recurso 9 \_ x e superior.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294205"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a><span data-ttu-id="89b1a-103">Planos de corte do usuário no hardware de nível de recurso 9</span><span class="sxs-lookup"><span data-stu-id="89b1a-103">User clip planes on feature level 9 hardware</span></span>

<span data-ttu-id="89b1a-104">A partir do Windows 8, a linguagem de sombreamento de alto nível (HLSL) da Microsoft oferece suporte a uma sintaxe que você pode usar com a API do Microsoft Direct3D 11 para especificar os planos de clipes de usuário no [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e superior.</span><span class="sxs-lookup"><span data-stu-id="89b1a-104">Starting with Windows 8, Microsoft High Level Shader Language (HLSL) supports a syntax that you can use with the Microsoft Direct3D 11 API to specify user clip planes on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="89b1a-105">Você pode usar essa sintaxe de recorte de clipes para escrever um sombreador e, em seguida, usar esse objeto Shader com a API do Direct3D 11 para ser executado em todos os níveis de recurso do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="89b1a-105">You can use this clip-planes syntax to write a shader, and then use that shader object with the Direct3D 11 API to run on all Direct3D feature levels.</span></span>

-   [<span data-ttu-id="89b1a-106">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="89b1a-106">Background</span></span>](#background-reading)
-   [<span data-ttu-id="89b1a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89b1a-107">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="89b1a-108">Criando planos de corte no espaço de clipes no nível de recurso 9 e superior</span><span class="sxs-lookup"><span data-stu-id="89b1a-108">Creating clip planes in clip space on feature level 9 and higher</span></span>](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [<span data-ttu-id="89b1a-109">Leitura em segundo plano</span><span class="sxs-lookup"><span data-stu-id="89b1a-109">Background reading</span></span>](#background-reading)
    -   [<span data-ttu-id="89b1a-110">níveis de recursos do 10Level9</span><span class="sxs-lookup"><span data-stu-id="89b1a-110">10Level9 feature levels</span></span>](#10level9-feature-levels)
    -   [<span data-ttu-id="89b1a-111">Matemática do plano de clipe</span><span class="sxs-lookup"><span data-stu-id="89b1a-111">Clip plane math</span></span>](#clip-plane-math)
    -   [<span data-ttu-id="89b1a-112">Recorte no espaço de exibição</span><span class="sxs-lookup"><span data-stu-id="89b1a-112">Clipping in view space</span></span>](#clipping-in-view-space)
    -   [<span data-ttu-id="89b1a-113">Matriz de projeção</span><span class="sxs-lookup"><span data-stu-id="89b1a-113">Projection matrix</span></span>](#projection-matrix)
    -   [<span data-ttu-id="89b1a-114">Plano de clipe de espaço de clipe</span><span class="sxs-lookup"><span data-stu-id="89b1a-114">Clip space clip plane</span></span>](#clip-space-clip-plane)
-   [<span data-ttu-id="89b1a-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89b1a-115">Related topics</span></span>](#related-topics)

## <a name="background"></a><span data-ttu-id="89b1a-116">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="89b1a-116">Background</span></span>

<span data-ttu-id="89b1a-117">Você pode acessar os planos de clipes do usuário na API do Microsoft Direct3D 9 por meio dos métodos [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) e [**IDirect3DDevice9:: GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) .</span><span class="sxs-lookup"><span data-stu-id="89b1a-117">You can access user clip planes in the Microsoft Direct3D 9 API via [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) and [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) methods.</span></span> <span data-ttu-id="89b1a-118">No Microsoft Direct3D 10 e posterior, você pode acessar os planos de clipes do usuário por meio da semântica de [ \_ ClipDistance de VA](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="89b1a-118">In Microsoft Direct3D 10 and later, you can access user clip planes through the [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="89b1a-119">Mas, antes do Windows 8, \_ o ClipDistance da VA não estava disponível para hardware de [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x nas APIs do Direct3D 10 ou do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="89b1a-119">But before Windows 8, SV\_ClipDistance was not available for [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x hardware in the Direct3D 10 or Direct3D 11 APIs.</span></span> <span data-ttu-id="89b1a-120">Portanto, antes do Windows 8, a única maneira de acessar os planos de clipes de usuário com \_ o hardware de nível de recurso 9 x foi por meio da API do Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="89b1a-120">So, before Windows 8, the only way to access user clip planes with feature level 9\_x hardware was through the Direct3D 9 API.</span></span> <span data-ttu-id="89b1a-121">Os aplicativos da Windows Store do Direct3D não podem usar a API do Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="89b1a-121">Direct3D Windows Store apps can't use the Direct3D 9 API.</span></span> <span data-ttu-id="89b1a-122">Aqui, descrevemos a sintaxe que você pode usar para acessar os planos de clipes do usuário por meio da API do Direct3D 11 no nível de recurso 9 \_ x e superior.</span><span class="sxs-lookup"><span data-stu-id="89b1a-122">Here we describe the syntax that you can use to access user clip planes through the Direct3D 11 API on feature level 9\_x and higher.</span></span>

<span data-ttu-id="89b1a-123">Os aplicativos usam os planos de corte para definir um conjunto de planos invisíveis no mundo 3D que cortam (jogam) todos os primitivos desenhados.</span><span class="sxs-lookup"><span data-stu-id="89b1a-123">Apps use clip planes to define a set of invisible planes within the 3D world that clip (throw away) all drawn primitives.</span></span> <span data-ttu-id="89b1a-124">O Windows não desenhará nenhum pixel que esteja no lado negativo dos planos de corte.</span><span class="sxs-lookup"><span data-stu-id="89b1a-124">Windows won't draw any pixel that is on the negative side of any clip planes.</span></span> <span data-ttu-id="89b1a-125">Os aplicativos podem usar os planos de corte para renderizar os reflexos do planar.</span><span class="sxs-lookup"><span data-stu-id="89b1a-125">Apps can then use clip planes to render planar reflections.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b1a-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="89b1a-126">Syntax</span></span>

<span data-ttu-id="89b1a-127">Use essa sintaxe para declarar os planos de corte como atributos de função em uma [declaração de função](dx-graphics-hlsl-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="89b1a-127">Use this syntax to declare clip planes as function attributes in a [function declaration](dx-graphics-hlsl-function-syntax.md).</span></span> <span data-ttu-id="89b1a-128">Por exemplo, aqui, usamos a sintaxe em um fragmento de sombreador de vértice:</span><span class="sxs-lookup"><span data-stu-id="89b1a-128">For example, here we use the syntax on a vertex shader fragment:</span></span>

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

<span data-ttu-id="89b1a-129">Este exemplo para um fragmento de sombreador de vértice denota dois planos de corte.</span><span class="sxs-lookup"><span data-stu-id="89b1a-129">This example for a vertex shader fragment denotes two clip planes.</span></span> <span data-ttu-id="89b1a-130">Ele mostra que você precisa colocar o novo atributo **clipplanes** entre colchetes imediatamente antes do valor de retorno do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="89b1a-130">It shows that you need to place the new **clipplanes** attribute within square brackets immediately before the return value of the vertex shader.</span></span> <span data-ttu-id="89b1a-131">Entre parênteses após o atributo **clipplanes** , você fornece uma lista de até seis constantes **FLOAT4** que definem os coeficientes de plano para cada plano ativo.</span><span class="sxs-lookup"><span data-stu-id="89b1a-131">Within parentheses after the **clipplanes** attribute, you provide a list of up to 6 **float4** constants that define the plane coefficients for each active clip plane.</span></span> <span data-ttu-id="89b1a-132">O exemplo também mostra que você precisa fazer os coeficientes de cada plano residir em um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="89b1a-132">The example also shows that you need to make the coefficients of each plane reside in a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="89b1a-133">Não há nenhuma sintaxe disponível para desabilitar um plano de corte dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="89b1a-133">There is no syntax available to disable a clip plane dynamically.</span></span> <span data-ttu-id="89b1a-134">Você deve recompilar um sombreador diferente do mesmo sem um atributo **clipplanes** ou seu aplicativo pode definir os coeficientes em seu buffer constante como zero para que o plano não afete mais nenhuma geometria.</span><span class="sxs-lookup"><span data-stu-id="89b1a-134">You must either recompile an otherwise identical shader with no **clipplanes** attribute, or your app can set the coefficients in your constant buffer to zero so that the plane no longer affects any geometry.</span></span>

 

<span data-ttu-id="89b1a-135">Essa sintaxe está disponível para qualquer destino de sombreador de vértice 4,0 ou posterior, que inclui vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1 e vs \_ 4 \_ 0 \_ nível \_ 9 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="89b1a-135">This syntax is available for any 4.0 or later vertex shader target, which includes vs\_4\_0\_level\_9\_1 and vs\_4\_0\_level\_9\_3.</span></span>

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a><span data-ttu-id="89b1a-136">Criando planos de corte no espaço de clipes no nível de recurso 9 e superior</span><span class="sxs-lookup"><span data-stu-id="89b1a-136">Creating clip planes in clip space on feature level 9 and higher</span></span>

<span data-ttu-id="89b1a-137">Aqui, mostramos como criar planos de corte no espaço de clipes no [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e superior.</span><span class="sxs-lookup"><span data-stu-id="89b1a-137">Here we show how to create clip planes in clip space on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

### <a name="background-reading"></a><span data-ttu-id="89b1a-138">Leitura em segundo plano</span><span class="sxs-lookup"><span data-stu-id="89b1a-138">Background reading</span></span>

<span data-ttu-id="89b1a-139">"Introdução à programação de jogos 3D com DirectX 10", de Frank D. Luna, explica o plano de fundo de matemática de gráficos (capítulos 1, 2 e 3) de que você precisa, e os vários espaços e transformações de espaço que ocorrem no sombreador de vértice (seções 5,6 e 5,8).</span><span class="sxs-lookup"><span data-stu-id="89b1a-139">"Introduction to 3D Game Programming with DirectX 10" by Frank D. Luna explains the graphics math background (chapters 1, 2 and 3) you need, and the various spaces and space transformations that occur in the vertex shader (sections 5.6 and 5.8).</span></span>

### <a name="10level9-feature-levels"></a><span data-ttu-id="89b1a-140">níveis de recursos do 10Level9</span><span class="sxs-lookup"><span data-stu-id="89b1a-140">10Level9 feature levels</span></span>

<span data-ttu-id="89b1a-141">No Direct3D 10 e posterior, você pode recortar qualquer espaço que faça sentido, geralmente no espaço do mundo ou no espaço de exibição.</span><span class="sxs-lookup"><span data-stu-id="89b1a-141">In Direct3D 10 and later, you can clip in any space that makes sense, often in world space or view space.</span></span> <span data-ttu-id="89b1a-142">Mas o Direct3D 9 usa o espaço de clipe, que é o espaço de projeção de divisão de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="89b1a-142">But Direct3D 9 uses clip space, which is pre perspective divide projection space.</span></span> <span data-ttu-id="89b1a-143">Os vetores estão no espaço de clipe quando o sombreador de vértice os passa para os estágios que seguem no [pipeline de gráficos](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span><span class="sxs-lookup"><span data-stu-id="89b1a-143">Vectors are in clip space when the vertex shader passes them to stages that follow in the [graphics pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span></span>

<span data-ttu-id="89b1a-144">Ao escrever um aplicativo da Windows Store, você deve usar os níveis de recurso do 10Level9 ([nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x) para que o aplicativo possa ser executado em um hardware de nível de recurso 9 \_ x e superior.</span><span class="sxs-lookup"><span data-stu-id="89b1a-144">When you write a Windows Store app, you must use 10Level9 feature levels ([feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x) so the app can run on feature level 9\_x and higher hardware.</span></span> <span data-ttu-id="89b1a-145">Como seu aplicativo dá suporte ao nível de recurso 9 \_ x e superior, você também deve usar a capacidade comum de aplicar os planos de corte no espaço do clipe.</span><span class="sxs-lookup"><span data-stu-id="89b1a-145">Because your app supports feature level 9\_x and higher, you must also use the common capability of applying clip planes in clip space.</span></span>

<span data-ttu-id="89b1a-146">Quando você compila um sombreador de vértice com vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1 ou posterior, esse sombreador de vértice pode usar o atributo **clipplanes** .</span><span class="sxs-lookup"><span data-stu-id="89b1a-146">When you compile a vertex shader with vs\_4\_0\_level\_9\_1 or later, that vertex shader can use the **clipplanes** attribute.</span></span> <span data-ttu-id="89b1a-147">Um objeto Direct3D 10 ou posterior tem um produto de ponto do vértice emitido que contém cada uma das constantes globais **FLOAT4** especificadas no atributo.</span><span class="sxs-lookup"><span data-stu-id="89b1a-147">A Direct3D 10 or later object has a dot product of the emitted vertex that contains each of the **float4** global constants specified in the attribute.</span></span> <span data-ttu-id="89b1a-148">O objeto Direct3D 9 tem metadados suficientes para fazer com que o tempo de execução do 10Level9 emita as chamadas apropriadas para [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span><span class="sxs-lookup"><span data-stu-id="89b1a-148">The Direct3D 9 object has enough meta data to cause the 10Level9 runtime to issue the appropriate calls to [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span></span>

### <a name="clip-plane-math"></a><span data-ttu-id="89b1a-149">Matemática do plano de clipe</span><span class="sxs-lookup"><span data-stu-id="89b1a-149">Clip plane math</span></span>

<span data-ttu-id="89b1a-150">Um plano de recorte é definido por um vetor com 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="89b1a-150">A clip plane is defined by a vector with 4 components.</span></span> <span data-ttu-id="89b1a-151">Os três primeiros componentes definem um vetor x, y, z que emana da origem no espaço que desejamos cortar.</span><span class="sxs-lookup"><span data-stu-id="89b1a-151">The first three components define an x, y, z vector that emanates from the origin in the space we want to clip.</span></span> <span data-ttu-id="89b1a-152">Esse vetor implica em um plano, perpendicular ao vetor e executado por meio da origem.</span><span class="sxs-lookup"><span data-stu-id="89b1a-152">This vector implies a plane, perpendicular to the vector and running through the origin.</span></span> <span data-ttu-id="89b1a-153">O Windows mantém todos os pixels no lado do vetor do plano e corta todos os pixels por trás do plano.</span><span class="sxs-lookup"><span data-stu-id="89b1a-153">Windows keeps all pixels on the vector side of the plane and clips all pixels behind the plane.</span></span> <span data-ttu-id="89b1a-154">O componente w em diante empurra o plano de volta e faz com que o Windows recorte menos (um negativo w faz com que o Windows recorte mais) ao longo da linha de vetor.</span><span class="sxs-lookup"><span data-stu-id="89b1a-154">The forth w component pushes the plane back and causes Windows to clip less (a negative w causes Windows to clip more) along the vector line.</span></span> <span data-ttu-id="89b1a-155">Se os componentes x, y, z comporem um vetor de unidade (normalizado), w enviará por push as unidades do plano w de volta.</span><span class="sxs-lookup"><span data-stu-id="89b1a-155">If the x, y, z components compose a unit (normalized) vector, w pushes the plane w units back.</span></span>

<span data-ttu-id="89b1a-156">A matemática que a GPU (unidade de processamento gráfico) executa para determinar o recorte é um produto de ponto simples entre o vetor de vértice (x, y, z, 1) e o vetor de plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="89b1a-156">The math that the graphics processing unit (GPU) performs to determine clipping is a simple dot product between the vertex vector (x, y, z, 1) and the clipping plane vector.</span></span> <span data-ttu-id="89b1a-157">Essa operação matemática cria um comprimento de projeção no vetor do plano de corte.</span><span class="sxs-lookup"><span data-stu-id="89b1a-157">This math operation creates a projection length on the clip plane vector.</span></span> <span data-ttu-id="89b1a-158">Um produto de ponto negativo mostra o vértice a ser exibido no lado recortado do plano.</span><span class="sxs-lookup"><span data-stu-id="89b1a-158">A negative dot product shows the vertex to be on the clipped side of the plane.</span></span>

### <a name="clipping-in-view-space"></a><span data-ttu-id="89b1a-159">Recorte no espaço de exibição</span><span class="sxs-lookup"><span data-stu-id="89b1a-159">Clipping in view space</span></span>

<span data-ttu-id="89b1a-160">Aqui está nosso vértice no espaço de exibição:</span><span class="sxs-lookup"><span data-stu-id="89b1a-160">Here is our vertex in view space:</span></span>

![vértice no espaço de exibição](images/vertex-clip.png)

<span data-ttu-id="89b1a-162">Aqui está o nosso plano no espaço de exibição:</span><span class="sxs-lookup"><span data-stu-id="89b1a-162">Here is our clip plane in view space:</span></span>

![recorte de plano no espaço de exibição](images/clip-plane-view.png)

<span data-ttu-id="89b1a-164">Este é o produto de ponto do vértice e do plano de recorte no espaço de exibição:</span><span class="sxs-lookup"><span data-stu-id="89b1a-164">Here is the dot product of vertex and clip plane in view space:</span></span>

<span data-ttu-id="89b1a-165">ClipDistance = **v** · **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="89b1a-165">ClipDistance = **v** · **C** = *v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub></span></span>

<span data-ttu-id="89b1a-166">Esta operação matemática funciona para um objeto Direct3D 10 ou posterior, mas não funcionará para um objeto Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="89b1a-166">This math operation works for a Direct3D 10 or later object but won't work for a Direct3D 9 object.</span></span> <span data-ttu-id="89b1a-167">Para o Direct3D 9, devemos primeiro obter nossa transformação de projeção no espaço do clipe.</span><span class="sxs-lookup"><span data-stu-id="89b1a-167">For Direct3D 9, we must first get through our projection transform into clip space.</span></span>

### <a name="projection-matrix"></a><span data-ttu-id="89b1a-168">Matriz de projeção</span><span class="sxs-lookup"><span data-stu-id="89b1a-168">Projection matrix</span></span>

<span data-ttu-id="89b1a-169">Uma matriz de projeção transforma um vértice do espaço de exibição (onde a origem é o olho do visualizador, + x está à direita, + y está ativo e + z é diretamente à frente) no espaço do clipe.</span><span class="sxs-lookup"><span data-stu-id="89b1a-169">A projection matrix transforms a vertex from view space (where the origin is the viewer's eye, +x is to the right, +y is up, and +z is straight ahead) into clip space.</span></span> <span data-ttu-id="89b1a-170">A matriz de projeção lê o vértice para recorte de hardware e o [estágio de rasterização](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span><span class="sxs-lookup"><span data-stu-id="89b1a-170">The projection matrix readies the vertex for hardware clipping and the [rasterization stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span></span> <span data-ttu-id="89b1a-171">Aqui está uma matriz de perspectiva padrão (outras projeções exigem matemática diferente):</span><span class="sxs-lookup"><span data-stu-id="89b1a-171">Here is a standard perspective matrix (other projections require different math):</span></span>

<dl> <span data-ttu-id="89b1a-172">   taxa de r de largura/altura da janela</span><span class="sxs-lookup"><span data-stu-id="89b1a-172">*r*  ratio of window width/height</span></span>  
<span data-ttu-id="89b1a-173">ângulo de exibição de *α*  </span><span class="sxs-lookup"><span data-stu-id="89b1a-173">*α*  viewing angle</span></span>  
<span data-ttu-id="89b1a-174">*f*   distância do visualizador até o plano distante</span><span class="sxs-lookup"><span data-stu-id="89b1a-174">*f*  distance from the viewer to the far plane</span></span>  
<span data-ttu-id="89b1a-175">*n*   distância do visualizador até o plano próximo</span><span class="sxs-lookup"><span data-stu-id="89b1a-175">*n*  distance from the viewer to the near plane</span></span>
</dl><span data-ttu-id="89b1a-176">![matriz de projeção](images/projection-matrix.png)</span><span class="sxs-lookup"><span data-stu-id="89b1a-176">![projection matrix](images/projection-matrix.png)</span></span>

<span data-ttu-id="89b1a-177">A próxima matriz é uma versão simplificada da matriz anterior.</span><span class="sxs-lookup"><span data-stu-id="89b1a-177">The next matrix is a simplified version of the previous matrix.</span></span> <span data-ttu-id="89b1a-178">Mostramos a matriz simplificada para que possamos usá-la posteriormente na operação de multiplicação de matriz.</span><span class="sxs-lookup"><span data-stu-id="89b1a-178">We show the matrix simplified so we can use it later in the matrix multiply operation.</span></span>

![matriz de projeção simplificada](images/projection-matrix2.png)

<span data-ttu-id="89b1a-180">Agora, transformamos nosso vértice de espaço de exibição em espaço de clipe com uma multiplicação de matriz:</span><span class="sxs-lookup"><span data-stu-id="89b1a-180">Now we transform our view space vertex into clip space with a matrix multiply:</span></span>

![multiplicação de matriz](images/matrix-multiply.png)

<span data-ttu-id="89b1a-182">Em nossa operação de multiplicação de matriz, nossos componentes x e y são apenas ligeiramente ajustados, mas nossos componentes z e w são bastante desconfigurados.</span><span class="sxs-lookup"><span data-stu-id="89b1a-182">In our matrix multiply operation, our x and y components are only slightly adjusted, but our z and w components are quite mangled.</span></span> <span data-ttu-id="89b1a-183">Nosso plano de corte não nos dará mais o que desejamos.</span><span class="sxs-lookup"><span data-stu-id="89b1a-183">Our clip plane won't give us what we want any more.</span></span>

### <a name="clip-space-clip-plane"></a><span data-ttu-id="89b1a-184">Plano de clipe de espaço de clipe</span><span class="sxs-lookup"><span data-stu-id="89b1a-184">Clip space clip plane</span></span>

<span data-ttu-id="89b1a-185">Aqui, queremos criar um plano de clipe de espaço de clipe cujo produto de ponto com nosso vértice de espaço de clipe nos dê o mesmo valor que o **v · C** na seção [recorte na exibição de espaço](#clipping-in-view-space) .</span><span class="sxs-lookup"><span data-stu-id="89b1a-185">Here we want to create a clip space clip plane whose dot product with our clip space vertex gives us the same value as **v · C** in the [Clipping in view space](#clipping-in-view-space) section.</span></span>

![plano de recorte](images/clip-space-clip-plane.png)

<span data-ttu-id="89b1a-187">**v** · **C**  =  **v P** · **C**<sub>P</sub></span><span class="sxs-lookup"><span data-stu-id="89b1a-187">**v** · **C** = **v P** · **C**<sub>P</sub></span></span>

<span data-ttu-id="89b1a-188">*v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *P* ₓ *C*<sub>P ₓ</sub>  + *v*<sub>y</sub>*P*<sub>y</sub>*c*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*C*<sub>P <sub>z</sub></sub>  +  *BC*<sub>p <sub>z</sub></sub>  +  *v*<sub>z</sub>*c*<sub>p <sub>w</sub></sub></span><span class="sxs-lookup"><span data-stu-id="89b1a-188">*v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub> = *v* ₓ *P* ₓ *C*<sub>Pₓ</sub> +*v*<sub>y</sub>*P*<sub>y</sub>*C*<sub>P <sub>y</sub></sub> + *v*<sub>z</sub>*A*<sub>y</sub>*C*<sub>P <sub>z</sub></sub> + *BC*<sub>P <sub>z</sub></sub> + *v*<sub>z</sub>*C*<sub>P<sub>w</sub></sub></span></span>

<span data-ttu-id="89b1a-189">Agora, podemos dividir a operação matemática anterior por componente de vértice em quatro equações separadas:</span><span class="sxs-lookup"><span data-stu-id="89b1a-189">Now we can break the preceding math operation up by vertex component into four separate equations:</span></span>

![componente de vértice x do produto do clip plano](images/clip-space-clip-plane-equ1.png)

![componente de vértice y do produto do clip plano](images/clip-space-clip-plane-equ2.png)

![componente de vértice w do produto do clip plano](images/clip-space-clip-plane-equ3.png)

![componente de vértice z do produto do clip plano](images/clip-space-clip-plane-equ4.png)

<span data-ttu-id="89b1a-194">Nosso plano de espaço de exibição e nossa matriz de projeção derivam e nos fornecem nosso plano de clipes de espaço de clipe.</span><span class="sxs-lookup"><span data-stu-id="89b1a-194">Our view space clip plane and our projection matrix derive and give us our clip space clip plane.</span></span>

![plano de clipe de espaço de clipe](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a><span data-ttu-id="89b1a-196">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89b1a-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89b1a-197">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="89b1a-197">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="89b1a-198">Sintaxe de declaração da função</span><span class="sxs-lookup"><span data-stu-id="89b1a-198">Function Declaration Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 
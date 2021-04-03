---
title: 10 perguntas frequentes sobre o Direct3D
description: Este artigo contém algumas das perguntas frequentes sobre o Direct3D 10 a partir do ponto de vista de um desenvolvedor que está portando um aplicativo existente do Direct3D 9 (D3D9) para o Direct3D 10 (D3D10).
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084672"
---
# <a name="direct3d-10-frequently-asked-questions"></a><span data-ttu-id="c8415-103">10 perguntas frequentes sobre o Direct3D</span><span class="sxs-lookup"><span data-stu-id="c8415-103">Direct3D 10 Frequently Asked Questions</span></span>

<span data-ttu-id="c8415-104">Este artigo contém algumas das perguntas frequentes sobre o Direct3D 10 a partir do ponto de vista de um desenvolvedor que está portando um aplicativo existente do Direct3D 9 (D3D9) para o Direct3D 10 (D3D10).</span><span class="sxs-lookup"><span data-stu-id="c8415-104">This article contains some of the frequently asked questions surrounding Direct3D 10 from the point of view of a developer who is porting an existing application from Direct3D 9 (D3D9) to Direct3D 10 (D3D10).</span></span>

-   [<span data-ttu-id="c8415-105">Buffers de constantes</span><span class="sxs-lookup"><span data-stu-id="c8415-105">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="c8415-106">State</span><span class="sxs-lookup"><span data-stu-id="c8415-106">State</span></span>](#state)
-   [<span data-ttu-id="c8415-107">Formatos</span><span class="sxs-lookup"><span data-stu-id="c8415-107">Formats</span></span>](#formats)
-   [<span data-ttu-id="c8415-108">Vinculação de sombreador</span><span class="sxs-lookup"><span data-stu-id="c8415-108">Shader Linkage</span></span>](#shader-linkage)
-   [<span data-ttu-id="c8415-109">Chamar chamadas</span><span class="sxs-lookup"><span data-stu-id="c8415-109">Draw Calls</span></span>](#draw-calls)
-   [<span data-ttu-id="c8415-110">Recursos</span><span class="sxs-lookup"><span data-stu-id="c8415-110">Resources</span></span>](#resources)
-   [<span data-ttu-id="c8415-111">Profundidade como textura</span><span class="sxs-lookup"><span data-stu-id="c8415-111">Depth as Texture</span></span>](#depth-as-texture)
-   [<span data-ttu-id="c8415-112">MSAA</span><span class="sxs-lookup"><span data-stu-id="c8415-112">MSAA</span></span>](#msaa)
-   [<span data-ttu-id="c8415-113">Falhas</span><span class="sxs-lookup"><span data-stu-id="c8415-113">Crashes</span></span>](#crashes)
-   [<span data-ttu-id="c8415-114">Renderização de predicado</span><span class="sxs-lookup"><span data-stu-id="c8415-114">Predicated Rendering</span></span>](#predicated-rendering)
-   [<span data-ttu-id="c8415-115">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c8415-115">Geometry Shader</span></span>](#geometry-shader)
-   [<span data-ttu-id="c8415-116">HLSL</span><span class="sxs-lookup"><span data-stu-id="c8415-116">HLSL</span></span>](#hlsl)

## <a name="constant-buffers"></a><span data-ttu-id="c8415-117">Buffers de constantes</span><span class="sxs-lookup"><span data-stu-id="c8415-117">Constant Buffers</span></span>

<dl> <dt>

<span data-ttu-id="c8415-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>Qual é a melhor maneira de atualizar os buffers de constantes?</span><span class="sxs-lookup"><span data-stu-id="c8415-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>What is the best way to update constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="c8415-119">UpdateSubresource e MAP com descarte devem ter aproximadamente a mesma velocidade.</span><span class="sxs-lookup"><span data-stu-id="c8415-119">UpdateSubresource and Map with Discard should be about the same speed.</span></span> <span data-ttu-id="c8415-120">Escolha entre elas, dependendo de qual delas copia a quantidade mínima de memória.</span><span class="sxs-lookup"><span data-stu-id="c8415-120">Choose between them depending on which one copies the least amount of memory.</span></span> <span data-ttu-id="c8415-121">Se você já tiver seus dados armazenados na memória em um bloco contíguo, use UpdateSubresource.</span><span class="sxs-lookup"><span data-stu-id="c8415-121">If you already have your data stored in memory in one contiguous block, use UpdateSubresource.</span></span> <span data-ttu-id="c8415-122">Se você precisar acumular dados de outros locais, use mapear com descartar.</span><span class="sxs-lookup"><span data-stu-id="c8415-122">If you need to accumulate data from other places, use Map with Discard.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>Qual é a pior maneira de organizar os buffers de constantes?</span><span class="sxs-lookup"><span data-stu-id="c8415-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>What is the worst way to organize constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="c8415-124">O pior desempenho é realizado ao colocar todas as constantes para um sombreador específico em um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="c8415-124">The worst performance is realized by putting all constants for a particular shader into one constant buffer.</span></span> <span data-ttu-id="c8415-125">Embora isso geralmente seja a maneira mais fácil de portar de D3D9 para D3D10, ele pode prejudicar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="c8415-125">While this often is the easiest way to port from D3D9 to D3D10, it can cripple performance.</span></span> <span data-ttu-id="c8415-126">Por exemplo, considere um cenário que usa o seguinte buffer de constantes:</span><span class="sxs-lookup"><span data-stu-id="c8415-126">For example, consider a scenario that uses the following constant buffer:</span></span>

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

<span data-ttu-id="c8415-127">O buffer é de 6560 bytes.</span><span class="sxs-lookup"><span data-stu-id="c8415-127">The buffer is 6560 bytes.</span></span> <span data-ttu-id="c8415-128">Suponha que haja um aplicativo com 1000 objetos a serem processados, 100 dos quais são malhas com revestimento e 900 das que são malhas estáticas.</span><span class="sxs-lookup"><span data-stu-id="c8415-128">Assume there is an application with 1000 objects to be rendered, 100 of which are skinned meshes, and 900 of which are static meshes.</span></span> <span data-ttu-id="c8415-129">Além disso, suponha que esse aplicativo esteja usando o mapeamento de sombra com uma fonte de luz.</span><span class="sxs-lookup"><span data-stu-id="c8415-129">Also, assume that this application is using shadow mapping with one light source.</span></span> <span data-ttu-id="c8415-130">Isso significa que há duas passagens, uma para o mapa de profundidade renderizado da luz e outra para a passagem de renderização de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="c8415-130">This means there are two passes, one for the depth map rendered from the light, and one for the forward rendering pass.</span></span> <span data-ttu-id="c8415-131">Isso resulta em chamadas de empate de 2000.</span><span class="sxs-lookup"><span data-stu-id="c8415-131">This results in 2000 draw calls.</span></span> <span data-ttu-id="c8415-132">Embora cada chamada de desenho não precise atualizar todas as partes do buffer de constantes, todo o buffer de constante ainda é atualizado e enviado para o cartão.</span><span class="sxs-lookup"><span data-stu-id="c8415-132">Although each draw call does not NEED to update every part of the constant buffer, the entire constant buffer still is updated and sent to the card.</span></span> <span data-ttu-id="c8415-133">Isso resulta na atualização de 13 MB de dados a cada quadro (o 2000 Draw chama o tempo de 6560 KB).</span><span class="sxs-lookup"><span data-stu-id="c8415-133">This results in the update of 13 MB of data every frame (2000 draw calls times 6560 KB).</span></span>

</dd> <dt>

<span data-ttu-id="c8415-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>Qual é a melhor maneira de organizar meus buffers de constantes?</span><span class="sxs-lookup"><span data-stu-id="c8415-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>What is the best way to organize my constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="c8415-135">A melhor maneira é organizar buffers constantes por frequência de atualização.</span><span class="sxs-lookup"><span data-stu-id="c8415-135">The best way is to organize constant buffers by frequency of update.</span></span> <span data-ttu-id="c8415-136">As constantes que são atualizadas em frequências semelhantes devem estar no mesmo buffer.</span><span class="sxs-lookup"><span data-stu-id="c8415-136">Constants that are updated at similar frequencies should be in the same buffer.</span></span> <span data-ttu-id="c8415-137">Por exemplo, considere o cenário apresentado em "Qual é a pior maneira de organizar buffers de constantes?", mas com um layout de constante melhor:</span><span class="sxs-lookup"><span data-stu-id="c8415-137">For example, consider the scenario presented under, "What is the worst way to organize constant buffers?," but with a better constant layout:</span></span>

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

<span data-ttu-id="c8415-138">Os buffers de constantes são divididos por sua frequência de atualização, mas isso só é metade da solução.</span><span class="sxs-lookup"><span data-stu-id="c8415-138">Constant buffers are split by their update frequency, but this only is half of the solution.</span></span> <span data-ttu-id="c8415-139">O aplicativo precisa atualizar os buffers de constantes corretamente para tirar total proveito da divisão.</span><span class="sxs-lookup"><span data-stu-id="c8415-139">The application needs to update the constant buffers correctly in order to take full advantage of the split.</span></span> <span data-ttu-id="c8415-140">Vamos pressupor a mesma cena acima: 900 malhas estáticas, 100 malhas com revestimento, uma passagem leve e uma passagem de avanço.</span><span class="sxs-lookup"><span data-stu-id="c8415-140">We will assume the same scene as above: 900 static meshes, 100 skinned meshes, one light pass, and one forward pass.</span></span> <span data-ttu-id="c8415-141">Também presumiremos que alguns buffers de constante por objeto serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="c8415-141">We also will assume that some constant buffers per-object will be stored.</span></span> <span data-ttu-id="c8415-142">Isso significa que cada objeto conterá um VSPerSkinnedCB ou um VSPerStaticCB, dependendo se ele é ou não docapado ou estático.</span><span class="sxs-lookup"><span data-stu-id="c8415-142">This means that each object will contain either a VSPerSkinnedCB or a VSPerStaticCB, depending on whether or not it is skinned or static.</span></span> <span data-ttu-id="c8415-143">Fazemos isso para evitar o dobro da quantidade de matrizes enviadas por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8415-143">We do this in order to avoid doubling the amount of matrices sent through the pipeline.</span></span>

<span data-ttu-id="c8415-144">Dividimos o quadro em três fases.</span><span class="sxs-lookup"><span data-stu-id="c8415-144">We split the frame into three phases.</span></span> <span data-ttu-id="c8415-145">A primeira fase é o início do quadro e não envolve nenhuma renderização, apenas atualizações constantes.</span><span class="sxs-lookup"><span data-stu-id="c8415-145">The first phase is the beginning of the frame and involves no rendering, just constant updates.</span></span>

<dl> <dt>

<span data-ttu-id="c8415-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Iniciar quadro**</span><span class="sxs-lookup"><span data-stu-id="c8415-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Begin Frame**</span></span>
</dt> <dd>

-   <span data-ttu-id="c8415-147">Atualizar VSGlobalPerFrameCB para o tempo do aplicativo (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="c8415-147">Update VSGlobalPerFrameCB for application time (4 bytes)</span></span>
-   <span data-ttu-id="c8415-148">Atualizar a 100 VSPerSkinnedCB para os objetos 100 com revestimento (640000 bytes)</span><span class="sxs-lookup"><span data-stu-id="c8415-148">Update 100 VSPerSkinnedCB for the 100 skinned objects (640000 bytes)</span></span>
-   <span data-ttu-id="c8415-149">Atualizar VSPerStaticCB para objetos estáticos 900 (57600 bytes)</span><span class="sxs-lookup"><span data-stu-id="c8415-149">Update VSPerStaticCB for 900 static objects (57600 bytes)</span></span>

<span data-ttu-id="c8415-150">A seguir está a passagem do mapa de sombra.</span><span class="sxs-lookup"><span data-stu-id="c8415-150">Next is the shadow map pass.</span></span> <span data-ttu-id="c8415-151">Observe que o único buffer constante que realmente atualiza é VSPerPassCB.</span><span class="sxs-lookup"><span data-stu-id="c8415-151">Notice that the only constant buffer that actually updates is VSPerPassCB.</span></span> <span data-ttu-id="c8415-152">Todos os outros buffers de constantes foram atualizados durante a fase de início do quadro.</span><span class="sxs-lookup"><span data-stu-id="c8415-152">All other constant buffers were updated during the begin frame pass.</span></span> <span data-ttu-id="c8415-153">Embora ainda precisemos associar esses buffers de constantes, a quantidade de informações passadas para a placa de vídeo é mínima, porque os buffers já foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="c8415-153">While we still need to bind these constant buffers, the amount of information passed to the video card is minimal, because the buffers already have been updated.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Passagem de sombra**</span><span class="sxs-lookup"><span data-stu-id="c8415-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Shadow Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="c8415-155">Atualizar VSPerPassCB (72 bytes)</span><span class="sxs-lookup"><span data-stu-id="c8415-155">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="c8415-156">Empates 100 malhas com revestimento (100 associações, sem atualizações)</span><span class="sxs-lookup"><span data-stu-id="c8415-156">Draw 100 skinned meshes (100 binds, no updates)</span></span>
-   <span data-ttu-id="c8415-157">Desenhe malhas estáticas 900 (100 associações, sem atualizações)</span><span class="sxs-lookup"><span data-stu-id="c8415-157">Draw 900 static meshes (100 binds, no updates)</span></span>

<span data-ttu-id="c8415-158">Da mesma forma, a passagem de renderização de encaminhamento só precisa atualizar dados por material, pois ela não foi armazenada por malha.</span><span class="sxs-lookup"><span data-stu-id="c8415-158">Similarly, the forward rendering pass only needs to update per-material data, because it was not stored per-mesh.</span></span> <span data-ttu-id="c8415-159">Se presumirmos que há 500 materiais em uso na cena:</span><span class="sxs-lookup"><span data-stu-id="c8415-159">If we assume that there are 500 materials in use in the scene:</span></span>

</dd> <dt>

<span data-ttu-id="c8415-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Passagem de encaminhamento**</span><span class="sxs-lookup"><span data-stu-id="c8415-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Forward Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="c8415-161">Atualizar VSPerPassCB (72 bytes)</span><span class="sxs-lookup"><span data-stu-id="c8415-161">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="c8415-162">Atualização 500 VSPerMaterialCBs (10000 bytes)</span><span class="sxs-lookup"><span data-stu-id="c8415-162">Update 500 VSPerMaterialCBs (10000 bytes)</span></span>

<span data-ttu-id="c8415-163">Isso resulta em um total de apenas 707 KB.</span><span class="sxs-lookup"><span data-stu-id="c8415-163">This results in a total of just 707 KB.</span></span> <span data-ttu-id="c8415-164">Embora esse seja um cenário muito forçado, ele ilustra a quantidade de sobrecarga de atualização constante que pode ser reduzida por meio da classificação de constantes por frequência de atualização.</span><span class="sxs-lookup"><span data-stu-id="c8415-164">Although this is a very contrived scenario, it illustrates just how much constant update overhead can be reduced by sorting constants by frequency of update.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c8415-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>E se eu não tiver espaço suficiente para armazenar buffers de constantes individuais para minhas malhas, material e assim por diante?</span><span class="sxs-lookup"><span data-stu-id="c8415-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>What if I do not have enough space to store individual constant buffers for my meshes, material, and so on?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-166">Você sempre pode usar um sistema em camadas de buffers de constantes.</span><span class="sxs-lookup"><span data-stu-id="c8415-166">You always can use a tiered system of constant buffers.</span></span> <span data-ttu-id="c8415-167">Crie buffers de constante de tamanho variável (16 bytes, 32 bytes, 64 bytes e assim por diante) até o maior tamanho de buffer constante necessário.</span><span class="sxs-lookup"><span data-stu-id="c8415-167">Create variable-sized constant buffers (16 bytes, 32 bytes, 64 bytes, and so on) up to the largest constant buffer size needed.</span></span> <span data-ttu-id="c8415-168">Quando for o momento de associar um buffer constante a um sombreador, selecione o menor buffer de constante que pode conter os dados necessários para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="c8415-168">When it is time to bind a constant buffer to a shader, select the smallest constant buffer that can hold the data needed by the shader.</span></span> <span data-ttu-id="c8415-169">Embora essa abordagem seja um pouco menos eficiente, ela é uma boa etapa intermediária.</span><span class="sxs-lookup"><span data-stu-id="c8415-169">Although this approach is slightly less efficient, it is a good intermediate step.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Estou compartilhando buffers de constantes entre diferentes sombreadores.</span><span class="sxs-lookup"><span data-stu-id="c8415-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>I am sharing constant buffers between different shaders.</span></span> <span data-ttu-id="c8415-171">Um sombreador pode usar todas as constantes, mas outra pode usar algumas das constantes.</span><span class="sxs-lookup"><span data-stu-id="c8415-171">One shader may use all of the constants, but another may use some of the constants.</span></span> <span data-ttu-id="c8415-172">Qual é a melhor maneira de atualizá-los?</span><span class="sxs-lookup"><span data-stu-id="c8415-172">What is the best way to update these?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-173">Uma abordagem é dividir ainda mais o buffer constante.</span><span class="sxs-lookup"><span data-stu-id="c8415-173">One approach is to split the constant buffer even further.</span></span> <span data-ttu-id="c8415-174">No entanto, há um ponto em que muitos buffers de constante estão associados.</span><span class="sxs-lookup"><span data-stu-id="c8415-174">However, there comes a point at which too many constant buffers are bound.</span></span> <span data-ttu-id="c8415-175">Nesse caso, mova as constantes que provavelmente não serão usadas por vários sombreadores no final do buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="c8415-175">In this case, move the constants that are likely to be unused by several shaders to the end of the constant buffer.</span></span> <span data-ttu-id="c8415-176">Ao obter os dados de variável do sombreador, use o \_ sinalizador d3d10 SVF \_ used da \_ variável de sombreador d3d10 \_ \_ desc para determinar se a variável é usada.</span><span class="sxs-lookup"><span data-stu-id="c8415-176">When getting the variable data from the shader, use the D3D10\_SVF\_USED flag from the D3D10\_SHADER\_VARIABLE\_DESC to determine if the variable is used.</span></span> <span data-ttu-id="c8415-177">Ao colocar variáveis não utilizadas no final do buffer de constantes, você pode associar um buffer menor ao sombreador que não usa essas variáveis, poupando assim o custo de atualização.</span><span class="sxs-lookup"><span data-stu-id="c8415-177">By placing unused variables at the end of the constant buffer, you can bind a smaller buffer to the shader that does not use these variables, thus saving the update cost.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>Quanto posso melhorar minha taxa de quadros se eu carregar apenas os Bones do meu caractere uma vez por quadro, em vez de uma vez por passagem/desenho?</span><span class="sxs-lookup"><span data-stu-id="c8415-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>How much can I improve my frame rate if I only upload my character's bones once per frame instead of once per pass/draw?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-179">Você pode melhorar a taxa de quadros entre 8% e 50 por cento, dependendo da quantidade de dados redundantes.</span><span class="sxs-lookup"><span data-stu-id="c8415-179">You can improve frame rate between 8 percent and 50 percent depending on the amount of redundant data.</span></span> <span data-ttu-id="c8415-180">No pior caso, o desempenho não será reduzido.</span><span class="sxs-lookup"><span data-stu-id="c8415-180">In the worst case, performance will not be reduced.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>Quantos buffers de constantes devo associar ao mesmo tempo?</span><span class="sxs-lookup"><span data-stu-id="c8415-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>How many constant buffers should I have bound at once?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-182">Associe o número mínimo de buffers de constante que é necessário para obter todos os dados no sombreador.</span><span class="sxs-lookup"><span data-stu-id="c8415-182">Bind the minimum number of constant buffers it takes to get all of your data into the shader.</span></span> <span data-ttu-id="c8415-183">Em um cenário realista, cinco é o número recomendado de buffers de constantes a serem usados.</span><span class="sxs-lookup"><span data-stu-id="c8415-183">In a realistic scenario, five is the recommended number of constant buffers to use.</span></span> <span data-ttu-id="c8415-184">O compartilhamento de buffers de constantes entre sombreadores (ligando o mesmo CB para o VS e PS) também pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="c8415-184">Sharing constant buffers between shaders (binding the same CB to the VS and PS) also can improve performance.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Há um custo para ligar buffers constantes sem usá-los?</span><span class="sxs-lookup"><span data-stu-id="c8415-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Is there a cost for binding constant buffers without using them?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-186">Sim, se você não for realmente usar o buffer, não chame VSSetConsantBuffer ou PSSetConstantBuffer.</span><span class="sxs-lookup"><span data-stu-id="c8415-186">Yes, if you are not actually going to use the buffer, then do not call VSSetConsantBuffer or PSSetConstantBuffer.</span></span> <span data-ttu-id="c8415-187">Essa sobrecarga extra da API pode ser somada ao longo de várias chamadas de desenho.</span><span class="sxs-lookup"><span data-stu-id="c8415-187">This extra API overhead can add up over the course of multiple draw calls.</span></span>

</dd> </dl>

## <a name="state"></a><span data-ttu-id="c8415-188">Estado</span><span class="sxs-lookup"><span data-stu-id="c8415-188">State</span></span>

<dl> <dt>

<span data-ttu-id="c8415-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>Qual é a melhor maneira de gerenciar o estado no D3D10?</span><span class="sxs-lookup"><span data-stu-id="c8415-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>What is the best way to manage state in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-190">A melhor solução é conhecer todo o seu estado de antecedência e criar os objetos de estado antecipadamente.</span><span class="sxs-lookup"><span data-stu-id="c8415-190">The best solution is to know all of your state up front and to create the state objects up front.</span></span> <span data-ttu-id="c8415-191">Isso significa que, no momento do processamento, a associação de estado é a única operação que precisa acontecer.</span><span class="sxs-lookup"><span data-stu-id="c8415-191">This means that at render time, state binding is the only operation that needs to happen.</span></span> <span data-ttu-id="c8415-192">D3D10 também filtra duplicatas.</span><span class="sxs-lookup"><span data-stu-id="c8415-192">D3D10 also filter outs duplicates.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Meu jogo carregou dinamicamente ou tem conteúdo gerado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c8415-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>My game has dynamically loaded or has user-generated content.</span></span> <span data-ttu-id="c8415-194">Não consigo carregar todos os meus objetos de estado antecipadamente.</span><span class="sxs-lookup"><span data-stu-id="c8415-194">I cannot load all of my state objects up front.</span></span> <span data-ttu-id="c8415-195">O que devo fazer?</span><span class="sxs-lookup"><span data-stu-id="c8415-195">What should I do?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-196">Há duas soluções aqui.</span><span class="sxs-lookup"><span data-stu-id="c8415-196">There are two solutions here.</span></span> <span data-ttu-id="c8415-197">A primeira é apenas criar objetos de estado imediatamente e permitir que o D3D10 filtre duplicatas.</span><span class="sxs-lookup"><span data-stu-id="c8415-197">The first is to just create state objects on the fly and to let D3D10 filter out duplicates.</span></span> <span data-ttu-id="c8415-198">No entanto, isso não é recomendado para cenários com muitas alterações de objeto de estado por quadro.</span><span class="sxs-lookup"><span data-stu-id="c8415-198">This, however, is not recommended for scenarios with many state object changes per frame.</span></span> <span data-ttu-id="c8415-199">Uma solução melhor é fazer o hash dos objetos de estado por conta própria e criar um objeto de estado somente se um que se ajuste aos requisitos não for encontrado na tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c8415-199">A better solution is to hash the state objects yourself and to create a state object only if one that fits the requirements is not found in the hash table.</span></span> <span data-ttu-id="c8415-200">O raciocínio por trás do uso de uma tabela de hash personalizada é que um aplicativo pode selecionar um hash rápido com base no cenário de uso específico para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8415-200">The reasoning behind using a custom hash table is that an application can select a fast hash based upon the usage scenario particular to that application.</span></span> <span data-ttu-id="c8415-201">Por exemplo, se um aplicativo altera apenas o rendertargetwritemask no Blendstate e mantém todos os outros valores iguais, o aplicativo pode gerar um hash do rendertargetwritemask em vez de toda a estrutura.</span><span class="sxs-lookup"><span data-stu-id="c8415-201">For example, if an application only changes the rendertargetwritemask in the BlendState and keeps all other values the same, the application can generate a hash from the rendertargetwritemask instead of the entire structure.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>O estado AlphaTest não existe mais.</span><span class="sxs-lookup"><span data-stu-id="c8415-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>AlphaTest state is gone.</span></span> <span data-ttu-id="c8415-203">Onde foi?</span><span class="sxs-lookup"><span data-stu-id="c8415-203">Where did it go?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-204">AlphaTest agora deve ser o desempenho no sombreador.</span><span class="sxs-lookup"><span data-stu-id="c8415-204">AlphaTest now should be performance in the shader.</span></span> <span data-ttu-id="c8415-205">Consulte o exemplo de FixedFuncEMU.</span><span class="sxs-lookup"><span data-stu-id="c8415-205">See the FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>O que aconteceu com os planos de clipes do usuário?</span><span class="sxs-lookup"><span data-stu-id="c8415-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>What happened to user clip planes?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-207">Os planos de clipes do usuário foram movidos para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="c8415-207">User clip planes have moved into the shader.</span></span> <span data-ttu-id="c8415-208">Há duas maneiras de lidar com isso.</span><span class="sxs-lookup"><span data-stu-id="c8415-208">There are two ways to handle this.</span></span> <span data-ttu-id="c8415-209">A primeira é a saída de \_ ClipDistance de VA do sombreador de vértice ou do sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="c8415-209">The first is to output SV\_ClipDistance from the vertex shader or the geometry shader.</span></span> <span data-ttu-id="c8415-210">A outra opção é usar o descarte no sombreador de pixel com base em um valor passado pelo sombreador de vértice ou pelo sombreador Geometry.</span><span class="sxs-lookup"><span data-stu-id="c8415-210">The other option is to use discard in the pixel shader based upon some value passed down by the vertex shader or the geometry shader.</span></span> <span data-ttu-id="c8415-211">Experimente ambos para ver qual é mais rápido para seu cenário específico.</span><span class="sxs-lookup"><span data-stu-id="c8415-211">Experiment with both to see which is faster for your particular scenario.</span></span> <span data-ttu-id="c8415-212">O uso de \_ ClipDistance de VA pode fazer com que o hardware use uma rotina de recorte baseada em geometria que pode fazer com que as chamadas de empate de limite de geometria sejam executadas mais lentamente.</span><span class="sxs-lookup"><span data-stu-id="c8415-212">Using SV\_ClipDistance could cause the hardware to use a geometry-based clipping routine that may cause geometry bound draw calls to run slower.</span></span> <span data-ttu-id="c8415-213">Da mesma forma, o uso de descarte desloca o trabalho para o sombreador de pixel, o que pode fazer com que as chamadas de empate com limite de pixel sejam executadas mais lentamente.</span><span class="sxs-lookup"><span data-stu-id="c8415-213">Likewise, using discard shifts the work to the pixel shader, which may cause pixel-bound draw calls to run slower.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Desmarcações não respeitam nenhuma configuração de estado, como minhas configurações de Rect de tesoura no estado do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="c8415-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Clears do not respect any state settings, such as my scissor rect settings in my Rasterizer State.</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-215">As desmarcações foram separadas do estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8415-215">Clears have been separated from the pipeline state.</span></span> <span data-ttu-id="c8415-216">Para obter o comportamento do estilo D3D9, emular limpas desenhando um quatro de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="c8415-216">In order to get D3D9-style behavior, emulate clears by drawing a full-screen quad.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Defini meus Estados de volta para o padrão para tentar diagnosticar um erro de renderização.</span><span class="sxs-lookup"><span data-stu-id="c8415-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>I set my states back to default to try and diagnose a rendering error.</span></span> <span data-ttu-id="c8415-218">Agora, minha tela mostra apenas preto, embora eu saiba que estou desenhando objetos na tela.</span><span class="sxs-lookup"><span data-stu-id="c8415-218">Now my screen just shows black, although I know I am drawing objects onto the screen.</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-219">Ao definir o estado de volta para valores padrão (NULL), verifique se SampleMask na chamada para OMSetBlendState nunca é zero.</span><span class="sxs-lookup"><span data-stu-id="c8415-219">When setting state back to default values (NULL), ensure that the SampleMask in the call to OMSetBlendState is never zero.</span></span> <span data-ttu-id="c8415-220">Se SampleMask for definido como zero, então todos os exemplos serão logicamente e com zero.</span><span class="sxs-lookup"><span data-stu-id="c8415-220">If SampleMask is set to zero, then all samples will logically AND with zero.</span></span> <span data-ttu-id="c8415-221">Nesse cenário, nenhum exemplo passará no teste de mistura.</span><span class="sxs-lookup"><span data-stu-id="c8415-221">In this scenario, no samples will pass the blend test.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Para onde o estado do D3DSAMP \_ SRGBTEXTURE é usado?</span><span class="sxs-lookup"><span data-stu-id="c8415-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Where did the D3DSAMP\_SRGBTEXTURE state go?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-223">O SRGB foi removido como parte do estado de amostra e agora está vinculado ao formato de textura.</span><span class="sxs-lookup"><span data-stu-id="c8415-223">SRGB was removed as part of the sampler state and now is tied to the texture format.</span></span> <span data-ttu-id="c8415-224">A associação de uma textura SRGB resultará na mesma amostragem que você obteria se tiver especificado D3DSAMP \_ SRGBTEXTURE no Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c8415-224">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> </dl>

## <a name="formats"></a><span data-ttu-id="c8415-225">Formatos</span><span class="sxs-lookup"><span data-stu-id="c8415-225">Formats</span></span>

<dl> <dt>

<span data-ttu-id="c8415-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Qual formato D3D9 corresponde ao formato D3D10?</span><span class="sxs-lookup"><span data-stu-id="c8415-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Which D3D9 format corresponds to which D3D10 format?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-227">Para obter informações, consulte [considerações do Direct3D 9 para o Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span><span class="sxs-lookup"><span data-stu-id="c8415-227">For info, see [Direct3D 9 to Direct3D 10 Considerations](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span></span>

</dd> <dt>

<span data-ttu-id="c8415-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>O que aconteceu com os formatos de textura A8R8G8B8?</span><span class="sxs-lookup"><span data-stu-id="c8415-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>What happened to A8R8G8B8 texture formats?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-229">Eles foram preteridos no D3D10.</span><span class="sxs-lookup"><span data-stu-id="c8415-229">They have been deprecated in D3D10.</span></span> <span data-ttu-id="c8415-230">Você pode recriar suas texturas como R8G8B8A8, ou pode swizzle-las na carga ou pode swizzle no sombreador.</span><span class="sxs-lookup"><span data-stu-id="c8415-230">You can re-source your textures as R8G8B8A8, or you can swizzle on load, or you can swizzle in the shader.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>Como fazer usar texturas palettized?</span><span class="sxs-lookup"><span data-stu-id="c8415-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>How do I use palettized textures?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-232">Coloque a paleta de cores em uma textura ou em um buffer de constantes e associe-a ao pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8415-232">Place your color palette in a texture or a constant buffer and bind it to the pipeline.</span></span> <span data-ttu-id="c8415-233">No sombreador de pixel, faça uma pesquisa indireta usando o índice em sua textura palettized.</span><span class="sxs-lookup"><span data-stu-id="c8415-233">In the pixel shader do an indirect lookup using the index in your palettized texture.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>Quais são esses novos formatos SRGB?</span><span class="sxs-lookup"><span data-stu-id="c8415-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>What are these new SRGB formats?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-235">O SRGB foi removido como parte do estado de amostra e agora está vinculado ao formato de textura.</span><span class="sxs-lookup"><span data-stu-id="c8415-235">SRGB was removed as part of the sampler state and is now tied to the texture format.</span></span> <span data-ttu-id="c8415-236">A associação de uma textura SRGB resultará na mesma amostragem que você obteria se tiver especificado D3DSAMP \_ SRGBTEXTURE no Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c8415-236">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Onde os fãs do triângulo vão?</span><span class="sxs-lookup"><span data-stu-id="c8415-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Where did triangle fans go?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-238">Os fãs do triângulo foram preteridos no D3D10.</span><span class="sxs-lookup"><span data-stu-id="c8415-238">Triangle fans have been deprecated in D3D10.</span></span> <span data-ttu-id="c8415-239">Os fãs do triângulo precisarão ser convertidos no pipeline de conteúdo ou no carregamento.</span><span class="sxs-lookup"><span data-stu-id="c8415-239">Triangle fans will need to be converted either in the content pipeline or on load.</span></span>

</dd> </dl>

## <a name="shader-linkage"></a><span data-ttu-id="c8415-240">Vinculação de sombreador</span><span class="sxs-lookup"><span data-stu-id="c8415-240">Shader Linkage</span></span>

<dl> <dt>

<span data-ttu-id="c8415-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Meus sombreadores do Direct3D 9 são bem compilados no modelo do sombreador 4,0, mas quando os vinculo ao pipeline, obtenho erros de vinculação aparecendo na saída de depuração com o tempo de execução de depuração.</span><span class="sxs-lookup"><span data-stu-id="c8415-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>My Direct3D 9 shaders compile fine to Shader Model 4.0, but when I bind them to the pipeline, I get linkage errors showing up in the debug output with the debug runtime.</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-242">O vínculo do sombreador é muito mais estrito em D3D10.</span><span class="sxs-lookup"><span data-stu-id="c8415-242">Shader linkage is much stricter in D3D10.</span></span> <span data-ttu-id="c8415-243">Os elementos em um estágio subsequente devem ser lidos na ordem em que são gerados do estágio anterior.</span><span class="sxs-lookup"><span data-stu-id="c8415-243">Elements in a subsequent stage must be read in the order they are output from the previous stage.</span></span> <span data-ttu-id="c8415-244">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c8415-244">For example:</span></span>

<span data-ttu-id="c8415-245">Saídas de um sombreador de vértice:</span><span class="sxs-lookup"><span data-stu-id="c8415-245">A vertex shader outputs:</span></span>

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="c8415-246">Um sombreador de pixel lê em:</span><span class="sxs-lookup"><span data-stu-id="c8415-246">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="c8415-247">Embora a posição não seja necessária no sombreador de pixel, isso causará um erro de vinculação, pois a posição está sendo saída do sombreador de vértice, mas não lida pelo sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="c8415-247">Although the position is not needed in the pixel shader, this will cause a linkage error, because position is being output from the vertex shader, but not read by the pixel shader.</span></span> <span data-ttu-id="c8415-248">A versão mais correta ficaria assim:</span><span class="sxs-lookup"><span data-stu-id="c8415-248">The more correct version would look like this:</span></span>

<span data-ttu-id="c8415-249">Saídas de um sombreador de vértice:</span><span class="sxs-lookup"><span data-stu-id="c8415-249">A vertex shader outputs:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

<span data-ttu-id="c8415-250">Um sombreador de pixel lê em:</span><span class="sxs-lookup"><span data-stu-id="c8415-250">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="c8415-251">Nesse caso, o sombreador de vértice está gerando as mesmas informações, mas agora o sombreador de pixel está lendo as coisas na saída do pedido.</span><span class="sxs-lookup"><span data-stu-id="c8415-251">In this case, the vertex shader is outputting the same information, but now the pixel shader is reading things in the order output.</span></span> <span data-ttu-id="c8415-252">Como o sombreador de pixel não está lendo nada após Tex, não precisamos se preocupar que o VS está gerando mais informações do que o PS está lendo.</span><span class="sxs-lookup"><span data-stu-id="c8415-252">Because the pixel shader is not reading anything after Tex, we do not have to worry that the VS is outputting more information than the PS is reading.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>Preciso de uma assinatura de sombreador para criar um layout de entrada, mas eu carregou minhas malhas e Crio layouts antes de criar sombreadores.</span><span class="sxs-lookup"><span data-stu-id="c8415-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>I need a shader signature in order to create an Input Layout, but I load my meshes and create layouts before creating shaders.</span></span> <span data-ttu-id="c8415-254">O que devo fazer?</span><span class="sxs-lookup"><span data-stu-id="c8415-254">What do I do?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-255">Uma solução é mudar os sombreadores de pedido e de carga antes de carregar malhas.</span><span class="sxs-lookup"><span data-stu-id="c8415-255">One solution is to switch the order and load shaders before loading meshes.</span></span> <span data-ttu-id="c8415-256">No entanto, isso é muito mais fácil, dito do que fazer.</span><span class="sxs-lookup"><span data-stu-id="c8415-256">However, this is much easier said than done.</span></span> <span data-ttu-id="c8415-257">Você sempre pode criar os layouts de entrada sob demanda quando necessário pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8415-257">You always can create the Input Layouts on demand when needed by the application.</span></span> <span data-ttu-id="c8415-258">Você precisará manter uma versão da assinatura do sombreador.</span><span class="sxs-lookup"><span data-stu-id="c8415-258">You will have to keep a version of the shader signature around.</span></span> <span data-ttu-id="c8415-259">Você deve criar um hash com base no layout do sombreador e do buffer e apenas criar o layout de entrada se um que corresponda ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="c8415-259">You should create a hash based off of the shader and buffer layout, and only create the Input Layout if one that matches does not exist already.</span></span>

</dd> </dl>

## <a name="draw-calls"></a><span data-ttu-id="c8415-260">Chamar chamadas</span><span class="sxs-lookup"><span data-stu-id="c8415-260">Draw Calls</span></span>

<dl> <dt>

<span data-ttu-id="c8415-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>Qual é o meu limite para chamadas de desenho para D3D10 alcançar 60 Hz?</span><span class="sxs-lookup"><span data-stu-id="c8415-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>What is my limit on draw calls for D3D10 to reach 60 Hz?</span></span> <span data-ttu-id="c8415-262">30 Hz?</span><span class="sxs-lookup"><span data-stu-id="c8415-262">30 Hz?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-263">O Direct3D 9 tinha uma limitação no número de chamadas de desenho devido ao custo de CPU por chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="c8415-263">Direct3D 9 had a limitation on the number of draw calls because of the CPU cost per draw call.</span></span> <span data-ttu-id="c8415-264">No Direct3D 10, o custo de cada chamada de desenho foi reduzido.</span><span class="sxs-lookup"><span data-stu-id="c8415-264">On Direct3D 10, the cost of each draw call has been reduced.</span></span> <span data-ttu-id="c8415-265">No entanto, não há mais uma correlação definitiva entre as chamadas de desenho e as taxas de quadros.</span><span class="sxs-lookup"><span data-stu-id="c8415-265">However, there is no longer a definite correlation between draw calls and frame rates.</span></span> <span data-ttu-id="c8415-266">Como as chamadas Draw geralmente exigem muitas chamadas de suporte (atualizações de buffer de constantes, associações de textura, configuração de estado e assim por diante), o impacto da taxa de quadros da API agora é mais dependente do uso geral da API em vez de simplesmente desenhar contagens de chamadas.</span><span class="sxs-lookup"><span data-stu-id="c8415-266">Because draw calls often require many support calls ( constant buffer updates, texture bindings, state setting, and so on) the frame rate impact of the API is now more dependent on the overall API usage as opposed to simply draw call counts.</span></span>

</dd> </dl>

## <a name="resources"></a><span data-ttu-id="c8415-267">Recursos</span><span class="sxs-lookup"><span data-stu-id="c8415-267">Resources</span></span>

<dl> <dt>

<span data-ttu-id="c8415-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>Que tipo de uso de recursos devo usar para as operações?</span><span class="sxs-lookup"><span data-stu-id="c8415-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>What resource usage type should I use for what operations?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-269">Use a seguinte folha de consulta:</span><span class="sxs-lookup"><span data-stu-id="c8415-269">Use the following cheat-sheet:</span></span>

-   <span data-ttu-id="c8415-270">A CPU atualiza o recurso mais de uma vez por quadro: D3D10 \_ uso \_ dinâmico</span><span class="sxs-lookup"><span data-stu-id="c8415-270">The CPU updates the resource more than once per frame: D3D10\_USAGE\_DYNAMIC</span></span>
-   <span data-ttu-id="c8415-271">A CPU atualiza o recurso menos de uma vez por quadro: \_ padrão de uso d3d10 \_</span><span class="sxs-lookup"><span data-stu-id="c8415-271">The CPU updates the resource less than once per frame: D3D10\_USAGE\_DEFAULT</span></span>
-   <span data-ttu-id="c8415-272">A CPU não atualiza o recurso: D3D10 \_ uso \_ imutável</span><span class="sxs-lookup"><span data-stu-id="c8415-272">The CPU does not update the resource: D3D10\_USAGE\_IMMUTABLE</span></span>
-   <span data-ttu-id="c8415-273">A CPU precisa ler o recurso: preparo de \_ uso de d3d10 \_</span><span class="sxs-lookup"><span data-stu-id="c8415-273">The CPU needs to read the resource: D3D10\_USAGE\_STAGING</span></span>

<span data-ttu-id="c8415-274">Como os buffers de constante sempre devem ser atualizados com frequência, eles não estão em conformidade com a "folha de dicas".</span><span class="sxs-lookup"><span data-stu-id="c8415-274">Because constant buffers are always meant to be update frequently, they do not conform to the "cheat-sheet."</span></span> <span data-ttu-id="c8415-275">Para os tipos de recursos a serem usados para buffers de constantes, consulte a seção [buffers de constantes](#constant-buffers) .</span><span class="sxs-lookup"><span data-stu-id="c8415-275">For which resource types to use for constant buffers, see the [Constant Buffers](#constant-buffers) section.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>O que aconteceu com DrawPrimitiveUP e DrawIndexedPrimitiveUP?</span><span class="sxs-lookup"><span data-stu-id="c8415-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>What happened to DrawPrimitiveUP and DrawIndexedPrimitiveUP?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-277">Eles ficaram em D3D10.</span><span class="sxs-lookup"><span data-stu-id="c8415-277">They are gone in D3D10.</span></span> <span data-ttu-id="c8415-278">Para geometria dinâmica, use um \_ buffer dinâmico de uso d3d10 grande \_ .</span><span class="sxs-lookup"><span data-stu-id="c8415-278">For dynamic geometry use a large D3D10\_USAGE\_DYNAMIC buffer.</span></span> <span data-ttu-id="c8415-279">No início do quadro, mapeie-o com o D3D10 \_ map \_ Write \_ Discard.</span><span class="sxs-lookup"><span data-stu-id="c8415-279">At the beginning of the frame, map it with D3D10\_MAP\_WRITE\_DISCARD.</span></span> <span data-ttu-id="c8415-280">Para cada chamada de desenho subsequente, avance o ponteiro de gravação após a posição dos vértices desenhados anteriormente e mapeie o buffer com D3D10 \_ map \_ Write \_ sem \_ substituição.</span><span class="sxs-lookup"><span data-stu-id="c8415-280">For each subsequent draw call advance the write pointer past the position of the previously drawn vertices and map the buffer with D3D10\_MAP\_WRITE\_NO\_OVERWRITE.</span></span> <span data-ttu-id="c8415-281">Se você estiver próximo do final do buffer antes do final do quadro, empacote o ponteiro de gravação em volta ao início e ao mapa com \_ descarte de gravação do mapa de d3d10 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c8415-281">If you near the end of the buffer before the end of the frame, wrap the write pointer around to the beginning and map with D3D10\_MAP\_WRITE\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Posso escrever índices de 16 bits e índices de 32 bits no mesmo buffer de geometria dinâmica?</span><span class="sxs-lookup"><span data-stu-id="c8415-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Can I write 16-bit indices and 32-bit indices into the same dynamic geometry buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-283">Sim, você pode, mas isso pode incorrer em uma penalidade de desempenho em determinado hardware.</span><span class="sxs-lookup"><span data-stu-id="c8415-283">Yes, you can, but this can incur a performance penalty on certain hardware.</span></span> <span data-ttu-id="c8415-284">É mais seguro criar buffers separados para dados de índice dinâmico de 16 bits e dados de índice de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c8415-284">It is a safer to create separate buffers for dynamic 16-bit index data and 32-bit index data.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Como fazer ler dados de volta da GPU para a CPU?</span><span class="sxs-lookup"><span data-stu-id="c8415-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>How do I read data back from the GPU to the CPU?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-286">Você deve usar um recurso de preparo.</span><span class="sxs-lookup"><span data-stu-id="c8415-286">You must use a staging resource.</span></span> <span data-ttu-id="c8415-287">Copie os dados do recurso de GPU para o recurso de preparo usando CopyResource.</span><span class="sxs-lookup"><span data-stu-id="c8415-287">Copy the data from the GPU resource to the staging resource using CopyResource.</span></span> <span data-ttu-id="c8415-288">Mapeie o recurso de preparo para ler os dados.</span><span class="sxs-lookup"><span data-stu-id="c8415-288">Map the staging resource to read the data.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>Meu aplicativo era dependente da funcionalidade de StretchRect.</span><span class="sxs-lookup"><span data-stu-id="c8415-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>My application was dependent on StretchRect functionality.</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-290">Como esse era essencialmente um wrapper para a funcionalidade básica do Direct3D, ele foi removido da API.</span><span class="sxs-lookup"><span data-stu-id="c8415-290">Because this was essentially a wrapper for basic Direct3D functionality, it was removed from the API.</span></span> <span data-ttu-id="c8415-291">Algumas das funcionalidades StretchRect foram movidas para D3DX10LoadTextureFromTexture.</span><span class="sxs-lookup"><span data-stu-id="c8415-291">Some of the StretchRect functionality was moved into D3DX10LoadTextureFromTexture.</span></span> <span data-ttu-id="c8415-292">Para conversões de formato e cópia de texturas, D3DX10LoadTextureFromTexture pode fazer o trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8415-292">For format conversions and copying textures, D3DX10LoadTextureFromTexture may do the job.</span></span> <span data-ttu-id="c8415-293">No entanto, as operações como a conversão de um tamanho para outra provavelmente exigirão um processamento para a operação de textura no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8415-293">However, operations such as converting from one size to another likely will require a render to texture operation in the application.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>Não há deslocamentos ou tamanhos em chamadas de mapa para recursos.</span><span class="sxs-lookup"><span data-stu-id="c8415-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>There are no offsets or sizes on Map calls for resources.</span></span> <span data-ttu-id="c8415-295">Eles estavam lá em chamadas de bloqueio no Direct3D 9; Por que eles mudaram?</span><span class="sxs-lookup"><span data-stu-id="c8415-295">These were there on Lock calls on Direct3D 9; why did they change?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-296">Os deslocamentos e tamanhos nas chamadas de bloqueio no Direct3D 9 eram basicamente uma desordem na API e, muitas vezes, ignorados pelo driver.</span><span class="sxs-lookup"><span data-stu-id="c8415-296">The offsets and sizes on Lock calls on Direct3D 9 were basically API clutter and often ignored by the driver.</span></span> <span data-ttu-id="c8415-297">Os deslocamentos devem ser calculados em vez do aplicativo do ponteiro retornado na chamada de mapa.</span><span class="sxs-lookup"><span data-stu-id="c8415-297">Offsets should be calculated instead by the application from the pointer returned in the Map call.</span></span>

</dd> </dl>

## <a name="depth-as-texture"></a><span data-ttu-id="c8415-298">Profundidade como textura</span><span class="sxs-lookup"><span data-stu-id="c8415-298">Depth as Texture</span></span>

<dl> <dt>

<span data-ttu-id="c8415-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Que é mais rápido?</span><span class="sxs-lookup"><span data-stu-id="c8415-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Which is faster?</span></span> <span data-ttu-id="c8415-300">Usar profundidade como uma textura ou uma profundidade de escrita em alfa e lendo isso?</span><span class="sxs-lookup"><span data-stu-id="c8415-300">Using depth as a texture or writing depth to alpha and reading that?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-301">Isso é específico de aplicativo e hardware.</span><span class="sxs-lookup"><span data-stu-id="c8415-301">This is application and hardware specific.</span></span> <span data-ttu-id="c8415-302">Use aquele que salvar a maior largura de banda.</span><span class="sxs-lookup"><span data-stu-id="c8415-302">Use whichever one saves the most bandwidth.</span></span> <span data-ttu-id="c8415-303">Se você já estiver usando vários destinos de renderização e tiver um canal extra, a criação de profundidade do sombreador pode ser uma solução melhor.</span><span class="sxs-lookup"><span data-stu-id="c8415-303">If you already are using multiple render targets and have an extra channel, then writing depth from the shader may be a better solution.</span></span> <span data-ttu-id="c8415-304">Além disso, escrever profundidade para alfa ou outro destino de renderização permite que você escreva valores de profundidade linear que podem acelerar os cálculos que precisam acessar o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="c8415-304">Also, writing depth to alpha or another render target allows you to write linear depth values that may speed up calculations that need to access the depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Posso ter uma textura ligada como entrada e associada como uma textura de estêncil de profundidade, desde que eu desabilite gravações de profundidade?</span><span class="sxs-lookup"><span data-stu-id="c8415-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Can I have a texture bound as an input AND bound as a depth-stencil texture as long as I disable depth writes?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-306">Não está em D3D10.</span><span class="sxs-lookup"><span data-stu-id="c8415-306">Not in D3D10.</span></span>

</dd> </dl>

## <a name="msaa"></a><span data-ttu-id="c8415-307">MSAA</span><span class="sxs-lookup"><span data-stu-id="c8415-307">MSAA</span></span>

<dl> <dt>

<span data-ttu-id="c8415-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Posso resolver uma textura de estêncil de profundidade de MSAA?</span><span class="sxs-lookup"><span data-stu-id="c8415-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Can I resolve an MSAA depth-stencil texture?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-309">Não está em D3D10.</span><span class="sxs-lookup"><span data-stu-id="c8415-309">Not in D3D10.</span></span> <span data-ttu-id="c8415-310">No entanto, você pode exemplificar exemplos individuais da textura MSAA.</span><span class="sxs-lookup"><span data-stu-id="c8415-310">However, you can sample individual samples from the MSAA texture.</span></span> <span data-ttu-id="c8415-311">Consulte a seção [HLSL](#hlsl) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="c8415-311">See the [HLSL](#hlsl) section for details.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Por que meu aplicativo falha assim que eu habilito o MSAA?</span><span class="sxs-lookup"><span data-stu-id="c8415-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Why does my application crash as soon as I enable MSAA?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-313">Verifique se você está habilitando uma contagem de exemplo de MSAA e um número de qualidade que, na verdade, são enumerados pelo driver.</span><span class="sxs-lookup"><span data-stu-id="c8415-313">Ensure you are enabling an MSAA sample count and quality number that actually are enumerated by the driver.</span></span>

</dd> </dl>

## <a name="crashes"></a><span data-ttu-id="c8415-314">Falhas</span><span class="sxs-lookup"><span data-stu-id="c8415-314">Crashes</span></span>

<dl> <dt>

<span data-ttu-id="c8415-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>Meu aplicativo falha no D3D10 ou no driver e eu não sei por quê.</span><span class="sxs-lookup"><span data-stu-id="c8415-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>My application crashes in D3D10 or in the driver and I do not know why.</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-316">A primeira etapa é habilitar o tempo de execução de depuração ([**d3d10 criar sinalizador de \_ \_ \_ depuração de dispositivo**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) passado para [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="c8415-316">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="c8415-317">Isso vai expor os erros mais comuns como saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="c8415-317">This will expose the most common errors as debug output.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>O PIX falha ao tentar usar meu aplicativo com ele.</span><span class="sxs-lookup"><span data-stu-id="c8415-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX crashes when I try to use my application with it.</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-319">A primeira etapa é habilitar o tempo de execução de depuração ([**d3d10 criar sinalizador de \_ \_ \_ depuração de dispositivo**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) passado para [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="c8415-319">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="c8415-320">O PIX tem uma probabilidade muito maior de falhar se a saída de depuração não estiver limpa.</span><span class="sxs-lookup"><span data-stu-id="c8415-320">PIX has a much higher probability of crashing if the debug output is not clean.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Meu jogo fica sem espaço de endereço virtual no vista de 32 bits em D3D10.</span><span class="sxs-lookup"><span data-stu-id="c8415-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>My game runs out of virtual address space on 32-bit Vista under D3D10.</span></span> <span data-ttu-id="c8415-322">Ele não tem problemas no D3D9.</span><span class="sxs-lookup"><span data-stu-id="c8415-322">It does not have problems on D3D9.</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-323">Houve alguns problemas com o D3D10 e o espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="c8415-323">There were some issues with D3D10 and virtual address space.</span></span> <span data-ttu-id="c8415-324">Isso foi corrigido em [KB940105](https://support.microsoft.com/kb/940105).</span><span class="sxs-lookup"><span data-stu-id="c8415-324">This has been fixed in [KB940105](https://support.microsoft.com/kb/940105).</span></span> <span data-ttu-id="c8415-325">Se isso não corrigir o problema, verifique se você não está criando mais recursos que podem ser mapeados (bloqueados) em D3D10 do que você estava criando no D3D9.</span><span class="sxs-lookup"><span data-stu-id="c8415-325">If that does not fix your problem, ensure you are not creating more resources that can be mapped (locked) in D3D10 than you were creating in D3D9.</span></span> <span data-ttu-id="c8415-326">Além disso, pense em portar para 64 bits, já que isso se tornará mais predominante no futuro.</span><span class="sxs-lookup"><span data-stu-id="c8415-326">Also think about porting to 64-bit since this will become more prevalent in the future.</span></span>

</dd> </dl>

## <a name="predicated-rendering"></a><span data-ttu-id="c8415-327">Renderização de predicado</span><span class="sxs-lookup"><span data-stu-id="c8415-327">Predicated Rendering</span></span>

<dl> <dt>

<span data-ttu-id="c8415-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>Usei renderização predicado (com base nos resultados da consulta oclusão).</span><span class="sxs-lookup"><span data-stu-id="c8415-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>I used Predicated rendering (based on occlusion query results).</span></span> <span data-ttu-id="c8415-329">Por que meu aplicativo ainda é a mesma velocidade?</span><span class="sxs-lookup"><span data-stu-id="c8415-329">Why is my app still the same speed?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-330">Primeiro, verifique se a renderização que você gostaria de ignorar é, na verdade, o afunilamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8415-330">First, ensure that the rendering you would like to skip is actually the application bottleneck.</span></span> <span data-ttu-id="c8415-331">Se não for o afunilamento, ignorar a renderização não ajudará a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="c8415-331">If it is not the bottleneck, then skipping the rendering will not help frame rate.</span></span>

<span data-ttu-id="c8415-332">Em segundo lugar, certifique-se de que o tempo suficiente tenha passado entre o problema da consulta e a renderização que você deseja predicado.</span><span class="sxs-lookup"><span data-stu-id="c8415-332">Second, make sure that enough time has passed between the issue of the query and rendering that you wish to predicate.</span></span> <span data-ttu-id="c8415-333">Se a consulta não tiver sido concluída no momento em que a chamada de renderização atingir a GPU, a renderização ocorrerá de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="c8415-333">If the query has not finished by the time the render call hits the GPU, the rendering will occur anyway.</span></span>

<span data-ttu-id="c8415-334">Terceiro, predicação apenas ignora determinadas chamadas.</span><span class="sxs-lookup"><span data-stu-id="c8415-334">Third, predication only skips certain calls.</span></span> <span data-ttu-id="c8415-335">As chamadas que são ignoradas são desenhar, limpar, copiar, atualizar, ResolveSubresource e GenerateMips.</span><span class="sxs-lookup"><span data-stu-id="c8415-335">The calls that are skipped are Draw, Clear, Copy, Update, ResolveSubresource and GenerateMips.</span></span> <span data-ttu-id="c8415-336">Configurações de estado, instalação de IA, mapear e criar chamadas não respeitam predicação.</span><span class="sxs-lookup"><span data-stu-id="c8415-336">State setting, IA setup, Map, and Create calls do not respect predication.</span></span> <span data-ttu-id="c8415-337">Se houver muitas chamadas de configuração de estado em relação à chamada de desenho a ser preparada, esses Estados ainda serão definidos.</span><span class="sxs-lookup"><span data-stu-id="c8415-337">If there are a lot of state setting calls around the draw call to be predicated, these states still will be set.</span></span>

</dd> </dl>

## <a name="geometry-shader"></a><span data-ttu-id="c8415-338">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c8415-338">Geometry Shader</span></span>

<dl> <dt>

<span data-ttu-id="c8415-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Devo usar o sombreador Geometry para incluí meu (inserir algo aqui)?</span><span class="sxs-lookup"><span data-stu-id="c8415-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Should I use the geometry shader to tessellate my (insert anything here)?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-340">Não.</span><span class="sxs-lookup"><span data-stu-id="c8415-340">No.</span></span> <span data-ttu-id="c8415-341">O sombreador de geometria não deve ser usado para mosaico.</span><span class="sxs-lookup"><span data-stu-id="c8415-341">The geometry shader should NOT be used for tessellation.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Posso usar o sombreador Geometry para criar geometria?</span><span class="sxs-lookup"><span data-stu-id="c8415-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Can I use the geometry shader to create geometry?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-343">Sim, em cenários muito limitados.</span><span class="sxs-lookup"><span data-stu-id="c8415-343">Yes, in very limited scenarios.</span></span> <span data-ttu-id="c8415-344">O sombreador de geometria nas partes D3D10 (2008) atuais não está equipado para lidar com muita expansão.</span><span class="sxs-lookup"><span data-stu-id="c8415-344">The geometry shader in current D3D10 (2008) parts is not equipped to handle much expansion.</span></span> <span data-ttu-id="c8415-345">Isso pode ser alterado no futuro.</span><span class="sxs-lookup"><span data-stu-id="c8415-345">This may change in the future.</span></span> <span data-ttu-id="c8415-346">Os fornecedores de placas de vídeo podem ter um caminho especial para uma a quatro expansões devido a um hardware de ponto-Sprite existente.</span><span class="sxs-lookup"><span data-stu-id="c8415-346">Video card vendors may have a special path for one to four expansions because of existing point-sprite hardware.</span></span> <span data-ttu-id="c8415-347">Qualquer outra expansão teria de ser muito limitada.</span><span class="sxs-lookup"><span data-stu-id="c8415-347">Any other expansion would have to be very limited.</span></span> <span data-ttu-id="c8415-348">Os exemplos de ParticlesGS e PipesGS atingem altas taxas de quadros apenas com a expansão limitada.</span><span class="sxs-lookup"><span data-stu-id="c8415-348">The ParticlesGS and PipesGS samples achieve high frame rates by only doing limited expansion.</span></span> <span data-ttu-id="c8415-349">Apenas alguns pontos são expandidos por quadro.</span><span class="sxs-lookup"><span data-stu-id="c8415-349">Only a few points are expanded per frame.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>Para que devo usar o sombreador Geometry?</span><span class="sxs-lookup"><span data-stu-id="c8415-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>What should I use the geometry shader for?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-351">Qualquer coisa que exija operações em um primitivo inteiro, como detecção de silhueta, coordenadas barycentric e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c8415-351">Anything that requires operations on an entire primitive such as silhouette detection, barycentric coordinates, and so on.</span></span> <span data-ttu-id="c8415-352">Use-o também para selecionar a qual fatia de uma matriz de destino de renderização enviar primitivos.</span><span class="sxs-lookup"><span data-stu-id="c8415-352">Also use it to select which slice of a render target array to send primitives to.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Posso gerar quantidades variáveis de geometria a partir do sombreador Geometry?</span><span class="sxs-lookup"><span data-stu-id="c8415-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Can I output variable amounts of geometry from the geometry shader?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-354">Sim, mas isso pode causar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="c8415-354">Yes, but this can cause performance issues.</span></span> <span data-ttu-id="c8415-355">Veja o exemplo de saída de 1 ponto para uma invocação e 4 pontos para outro.</span><span class="sxs-lookup"><span data-stu-id="c8415-355">Take the example of outputting 1 point for one invocation and 4 points for another.</span></span> <span data-ttu-id="c8415-356">Ao se ajustar nas diretrizes de expansão, isso pode fazer com que os threads do sombreador de geometria sejam executados em série.</span><span class="sxs-lookup"><span data-stu-id="c8415-356">While fitting within the expansion guidelines, this can cause the geometry shader threads to run serially.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>Como o D3D10 sabe como gerar índices de adjacência para minha malha?</span><span class="sxs-lookup"><span data-stu-id="c8415-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>How does D3D10 know how to generate adjacency indices for my mesh?</span></span> <span data-ttu-id="c8415-358">Ou, por que o D3D10 não é renderizado corretamente quando eu especificar que o sombreador Geometry precisa de informações de adjacência.</span><span class="sxs-lookup"><span data-stu-id="c8415-358">Or, why does D3D10 not render correctly when I specify that the geometry shader needs adjacency information.</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-359">As informações de adjacência não são criadas por D3D10, mas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8415-359">The adjacency information is not created by D3D10, but by the application.</span></span> <span data-ttu-id="c8415-360">Os índices de adjacência são gerados pelo aplicativo e devem conter seis índices por primitivo; dos seis, os índices numerados ímpares são os vértices adjacentes da borda.</span><span class="sxs-lookup"><span data-stu-id="c8415-360">Adjacency indices are generated by the application and must contain six indices per primitive; of the six, the odd numbered indices are the edge adjacent vertices.</span></span> <span data-ttu-id="c8415-361">ID3DX10Mesh:: GenerateAdjacencyAndPointsReps pode ser usado para gerar esses dados.</span><span class="sxs-lookup"><span data-stu-id="c8415-361">ID3DX10Mesh::GenerateAdjacencyAndPointsReps can be used to generate this data.</span></span>

</dd> </dl>

## <a name="hlsl"></a><span data-ttu-id="c8415-362">HLSL</span><span class="sxs-lookup"><span data-stu-id="c8415-362">HLSL</span></span>

<dl> <dt>

<span data-ttu-id="c8415-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Há instruções de inteiro e bit-de-processo lentas?</span><span class="sxs-lookup"><span data-stu-id="c8415-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Are integer and bitwise instructions slow?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-364">Eles podem ser.</span><span class="sxs-lookup"><span data-stu-id="c8415-364">They can be.</span></span> <span data-ttu-id="c8415-365">Vários cartões D3D10 podem ser capazes de emitir operações de inteiros em um subconjunto das unidades de ALU disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c8415-365">Various D3D10 cards may be able only to issue integer operations on a subset of the available ALU units.</span></span> <span data-ttu-id="c8415-366">Isso é altamente dependente do hardware.</span><span class="sxs-lookup"><span data-stu-id="c8415-366">This is highly dependent on the hardware.</span></span> <span data-ttu-id="c8415-367">Consulte seu fornecedor de hardware individual para obter recomendações sobre como tratar operações de inteiros nesse hardware específico.</span><span class="sxs-lookup"><span data-stu-id="c8415-367">See your individual hardware vendor for recommendations on how to address integer operations on that particular hardware.</span></span> <span data-ttu-id="c8415-368">Além disso, tenha muito cuidado com as conversões entre os tipos.</span><span class="sxs-lookup"><span data-stu-id="c8415-368">Also, be very careful of casts between types.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>O que aconteceu com o VPOS?</span><span class="sxs-lookup"><span data-stu-id="c8415-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>What happened to VPOS?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-370">Se você declarar uma entrada para o sombreador de pixel como posição da VA \_ , obterá o mesmo comportamento que declará-la como VPOS.</span><span class="sxs-lookup"><span data-stu-id="c8415-370">If you declare an input to your pixel shader as SV\_POSITION, you will get the same behavior as declaring it as VPOS.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Como fazer um exemplo de textura de MSAA?</span><span class="sxs-lookup"><span data-stu-id="c8415-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>How do I sample an MSAA texture?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-372">No sombreador, declare sua textura como Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="c8415-372">In your shader, declare your texture as Texture2DMS.</span></span> <span data-ttu-id="c8415-373">Em seguida, você pode buscar exemplos individuais usando os métodos de exemplo fora do objeto Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="c8415-373">You then can fetch individual samples using the Sample methods off of the Texture2DMS object.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Como fazer dizer se uma variável de sombreador em um buffer de constantes realmente é usada?</span><span class="sxs-lookup"><span data-stu-id="c8415-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>How do I tell if a shader variable in a constant buffer actually is used?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-375">Examine a \_ estrutura desc de variável do sombreador d3d10 refletida \_ \_ para essa variável.</span><span class="sxs-lookup"><span data-stu-id="c8415-375">Look at the reflected D3D10\_SHADER\_VARIABLE\_DESC struct for that variable.</span></span> <span data-ttu-id="c8415-376">uFlags deve ter o sinalizador de D3D10 \_ SVF \_ usado.</span><span class="sxs-lookup"><span data-stu-id="c8415-376">uFlags should have the D3D10\_SVF\_USED flag set.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Como fazer dizer se uma variável de sombreador em um buffer constante realmente está usando FX10?</span><span class="sxs-lookup"><span data-stu-id="c8415-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>How do I tell if a shader variable in a constant buffer actually is using FX10?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-378">Atualmente, isso não é possível usando FX10.</span><span class="sxs-lookup"><span data-stu-id="c8415-378">This currently is not possible using FX10.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>Não tenho controle sobre os buffers de constantes que o FX10 cria.</span><span class="sxs-lookup"><span data-stu-id="c8415-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>I have no control over constant buffers that FX10 creates.</span></span> <span data-ttu-id="c8415-380">Como eles são criados e atualizados?</span><span class="sxs-lookup"><span data-stu-id="c8415-380">How are they created and updated?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-381">Todos os buffers de constante gerenciados por FX10 são criados como \_ recursos padrão de uso de d3d10 \_ e atualizados usando UpdateSubresource.</span><span class="sxs-lookup"><span data-stu-id="c8415-381">All FX10-managed constant buffers are created as D3D10\_USAGE\_DEFAULT resources and are updated using UpdateSubresource.</span></span> <span data-ttu-id="c8415-382">Como o FX10 mantém um repositório de backup de todos os dados constantes, UpdateSubresource é a melhor abordagem para atualizá-los.</span><span class="sxs-lookup"><span data-stu-id="c8415-382">Because FX10 keeps a backing store of all constant data, UpdateSubresource is the best approach for updating these.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Como fazer emular o pipeline de função fixa usando sombreadores?</span><span class="sxs-lookup"><span data-stu-id="c8415-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>How do I emulate the fixed function pipeline using shaders?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-384">Consulte o exemplo de FixedFuncEMU.</span><span class="sxs-lookup"><span data-stu-id="c8415-384">See FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Devo usar o novo \[ relance \] , \[ loop \] , \[ ramificação \] , e assim por diante, dicas de compilador?</span><span class="sxs-lookup"><span data-stu-id="c8415-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Should I use the new \[unroll\], \[loop\], \[branch\], and so on, compiler hints?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-386">Em geral, não.</span><span class="sxs-lookup"><span data-stu-id="c8415-386">In general, no.</span></span> <span data-ttu-id="c8415-387">O compilador geralmente tentará as duas formas e escolherá a mais rápida.</span><span class="sxs-lookup"><span data-stu-id="c8415-387">The compiler will often try both ways and choose the fastest one.</span></span> <span data-ttu-id="c8415-388">Em alguns casos, pode ser necessário usar \[ unroll \] , por exemplo, quando uma busca de textura dentro de um loop precisa de acesso a um gradiente.</span><span class="sxs-lookup"><span data-stu-id="c8415-388">In some cases, it may be necessary to use \[unroll\], for example, when a texture fetch inside a loop needs access to a gradient.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>A precisão parcial faz alguma diferença no D3D10?</span><span class="sxs-lookup"><span data-stu-id="c8415-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Does partial precision make any difference on D3D10?</span></span> <span data-ttu-id="c8415-390">Posso especificar a precisão parcial em meu D3D9 HLSL, mas não em meu D3D10 HLSL.</span><span class="sxs-lookup"><span data-stu-id="c8415-390">I can specify partial precision in my D3D9 HLSL, but not in my D3D10 HLSL.</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-391">Todas as operações de D3D10 são especificadas para serem executadas com precisão de ponto flutuante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c8415-391">All D3D10 operations are specified to run at 32-bit floating point precision.</span></span> <span data-ttu-id="c8415-392">Portanto, a precisão parcial não deve fazer nenhuma diferença no D3D10.</span><span class="sxs-lookup"><span data-stu-id="c8415-392">Therefore, partial precision should not make any difference in D3D10.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>No D3D9, eu poderia fazer a filtragem de sombra do PCF de HW ligando um buffer de profundidade como uma textura e usando instruções regulares de HLSL de tex2d.</span><span class="sxs-lookup"><span data-stu-id="c8415-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In D3D9, I could do HW PCF shadow filtering by binding a depth buffer as a texture and using regular tex2d hlsl instructions.</span></span> <span data-ttu-id="c8415-394">Como fazer fazer isso no D3D10?</span><span class="sxs-lookup"><span data-stu-id="c8415-394">How do I do this on D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-395">Você precisa usar um estado de amostra de comparação e usar instruções de SampleCmp.</span><span class="sxs-lookup"><span data-stu-id="c8415-395">You have to use a comparison sampler state and use SampleCmp instructions.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>Como essa palavra-chave Register funciona no D3D10?</span><span class="sxs-lookup"><span data-stu-id="c8415-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>How does this register keyword work in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-397">A palavra-chave register em D3D10 agora se aplica a qual slot um recurso específico está associado.</span><span class="sxs-lookup"><span data-stu-id="c8415-397">The register keyword in D3D10 now applies to which slot a particular resource is bound to.</span></span> <span data-ttu-id="c8415-398">Nesse caso, o recurso pode ser um buffer (constante ou, caso contrário), textura ou amostra.</span><span class="sxs-lookup"><span data-stu-id="c8415-398">In this case, the resource can be a Buffer (constant or otherwise), Texture, or Sampler.</span></span>

-   <span data-ttu-id="c8415-399">Para buffers de constantes, use a sintaxe: Register (bilhão), em que N é o slot de entrada (0-15)</span><span class="sxs-lookup"><span data-stu-id="c8415-399">For constant buffers, use the syntax: register(bN), where N is the input slot (0-15)</span></span>
-   <span data-ttu-id="c8415-400">Para texturas, use a sintaxe: Register (tN), em que N é o slot de entrada (0-127)</span><span class="sxs-lookup"><span data-stu-id="c8415-400">For textures, use the syntax: register(tN), where N is the input slot (0-127)</span></span>
-   <span data-ttu-id="c8415-401">Para os exemplos, use a sintaxe: Register (sN), em que N é o slot de entrada (0-127)</span><span class="sxs-lookup"><span data-stu-id="c8415-401">For samplers, use the syntax: register(sN), where N is the input slot (0-127)</span></span>

</dd> <dt>

<span data-ttu-id="c8415-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Como fazer Coloque uma variável dentro de um buffer de constantes se o registro for usado apenas para especificar onde associar o buffer inteiro?</span><span class="sxs-lookup"><span data-stu-id="c8415-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>How do I place a variable inside a constant buffer if register is just used to specify where to bind the entire buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="c8415-403">Use a palavra-chave packoffset.</span><span class="sxs-lookup"><span data-stu-id="c8415-403">Use the packoffset keyword.</span></span> <span data-ttu-id="c8415-404">O argumento para packoffset está na forma de c \[ 0-4095 \] . \[ x, y, z, w \] .</span><span class="sxs-lookup"><span data-stu-id="c8415-404">The argument to packoffset is in the form of c\[0-4095\].\[x,y,z,w\].</span></span> <span data-ttu-id="c8415-405">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c8415-405">For example:</span></span>

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

<span data-ttu-id="c8415-406">Nesse buffer de constante, IWaste2Floats é colocado no terceiro float (12 bytes) no buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="c8415-406">In this constant buffer, IWaste2Floats is placed at the third float (12th byte) in the constant buffer.</span></span> <span data-ttu-id="c8415-407">IWasteMore é colocado no 13 FLOAT4 ou 52nd float no buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="c8415-407">IWasteMore is placed at the 13th float4 or 52nd float in the constant buffer.</span></span>

</dd> </dl>

 

 
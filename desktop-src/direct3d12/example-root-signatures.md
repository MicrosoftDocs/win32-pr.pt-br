---
title: Exemplo de assinaturas raiz
description: A seção a seguir mostra as assinaturas raiz que variam em complexidade de vazia para completamente completa.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104021"
---
# <a name="example-root-signatures"></a><span data-ttu-id="02b84-103">Exemplo de assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="02b84-103">Example Root Signatures</span></span>

<span data-ttu-id="02b84-104">A seção a seguir mostra as assinaturas raiz que variam em complexidade de vazia para completamente completa.</span><span class="sxs-lookup"><span data-stu-id="02b84-104">The following section shows root signatures varying in complexity from empty to completely full.</span></span>

-   [<span data-ttu-id="02b84-105">Uma assinatura raiz vazia</span><span class="sxs-lookup"><span data-stu-id="02b84-105">An empty root signature</span></span>](#an-empty-root-signature)
-   [<span data-ttu-id="02b84-106">Uma constante</span><span class="sxs-lookup"><span data-stu-id="02b84-106">One constant</span></span>](#one-constant)
-   [<span data-ttu-id="02b84-107">Adicionando uma exibição de buffer de constante raiz</span><span class="sxs-lookup"><span data-stu-id="02b84-107">Adding a root Constant Buffer View</span></span>](#adding-a-root-constant-buffer-view)
-   [<span data-ttu-id="02b84-108">Tabelas de descritores de associação</span><span class="sxs-lookup"><span data-stu-id="02b84-108">Binding descriptor tables</span></span>](#binding-descriptor-tables)
-   [<span data-ttu-id="02b84-109">Uma assinatura de raiz mais complexa</span><span class="sxs-lookup"><span data-stu-id="02b84-109">A more complex root signature</span></span>](#a-more-complex-root-signature)
-   [<span data-ttu-id="02b84-110">Exibições de recurso do sombreador de streaming</span><span class="sxs-lookup"><span data-stu-id="02b84-110">Streaming Shader Resource Views</span></span>](#streaming-shader-resource-views)
-   [<span data-ttu-id="02b84-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02b84-111">Related topics</span></span>](#related-topics)

## <a name="an-empty-root-signature"></a><span data-ttu-id="02b84-112">Uma assinatura raiz vazia</span><span class="sxs-lookup"><span data-stu-id="02b84-112">An empty root signature</span></span>

![uma assinatura raiz vazia não tem associações](images/root-tables-0.png)

<span data-ttu-id="02b84-114">Uma assinatura raiz vazia é improvável de ser útil, mas pode ser usada em uma passagem de renderização trivial com o uso apenas do assembler de entrada e do vértice mínimo e dos sombreadores de pixel que não acessam nenhum descritor.</span><span class="sxs-lookup"><span data-stu-id="02b84-114">An empty root signature is unlikely to be useful, but could be used in a trivial rendering pass with use of only the input assembler, and minimal vertex and pixel shaders that do not access any descriptors.</span></span> <span data-ttu-id="02b84-115">Além disso, os estágios de estágio de mesclagem, destino de renderização e estêncil de profundidade estão disponíveis, mesmo com uma assinatura de raiz vazia.</span><span class="sxs-lookup"><span data-stu-id="02b84-115">Also the blend stage, render target and depth-stencil stages are available, even with an empty root signature.</span></span>

## <a name="one-constant"></a><span data-ttu-id="02b84-116">Uma constante</span><span class="sxs-lookup"><span data-stu-id="02b84-116">One constant</span></span>

![uma única constante raiz](images/root-tables-constant.png)

<span data-ttu-id="02b84-118">O slot de associação de API é onde o argumento raiz para esse parâmetro será associado no momento do registro da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="02b84-118">The API bind slot is where the root argument for this parameter will be bound at command list record time.</span></span> <span data-ttu-id="02b84-119">O número de Slots de ligação de API é implícito, com base na ordem dos parâmetros na assinatura raiz (o primeiro é sempre zero).</span><span class="sxs-lookup"><span data-stu-id="02b84-119">The number of the API bind slots is implicit, based on the order of the parameters in the root signature (the first is always zero).</span></span> <span data-ttu-id="02b84-120">O slot de ligação do HLSL é onde o sombreador verá que o parâmetro raiz aparece.</span><span class="sxs-lookup"><span data-stu-id="02b84-120">The HLSL bind slot is where the shader will see the root parameter show up.</span></span> <span data-ttu-id="02b84-121">O tipo ("UINT" no exemplo acima) não é conhecido pelo hardware, mas é apenas um comentário na imagem, o hardware simplesmente verá o único DWORD como o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="02b84-121">The type ("uint" in the above example) is not known to the hardware but is just a comment in the image, the hardware will simply see the single DWORD as the contents.</span></span>

<span data-ttu-id="02b84-122">Para associar uma constante no tempo de registro da lista de comandos, um comando semelhante ao seguinte seria usado:</span><span class="sxs-lookup"><span data-stu-id="02b84-122">To bind a constant at command-list record time, a command similar to the following would be used:</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a><span data-ttu-id="02b84-123">Adicionando uma exibição de buffer de constante raiz</span><span class="sxs-lookup"><span data-stu-id="02b84-123">Adding a root Constant Buffer View</span></span>

![Adiciona uma exibição de buffer constante à assinatura raiz](images/root-tables-cbv.png)

<span data-ttu-id="02b84-125">Este exemplo mostra duas constantes raiz e uma CBV (exibição de buffer constante) de raiz que custa dois slots DWORD.</span><span class="sxs-lookup"><span data-stu-id="02b84-125">This example shows two root constants, and a root Constant Buffer View (CBV) that costs two DWORD slots.</span></span>

<span data-ttu-id="02b84-126">Para associar uma exibição de buffer constante, use um comando como o seguinte.</span><span class="sxs-lookup"><span data-stu-id="02b84-126">To bind a constant buffer view use a command such as the following.</span></span> <span data-ttu-id="02b84-127">Observe que o primeiro parâmetro (2) é o slot mostrado na imagem.</span><span class="sxs-lookup"><span data-stu-id="02b84-127">Note the first parameter (2) is the slot shown in the image.</span></span> <span data-ttu-id="02b84-128">Normalmente, uma matriz de constantes será configurada e disponibilizada para os sombreadores em B0 como um CBV.</span><span class="sxs-lookup"><span data-stu-id="02b84-128">Typically an array of constants will be set up and then made available to the shaders at b0 as a CBV.</span></span>

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a><span data-ttu-id="02b84-129">Tabelas de descritores de associação</span><span class="sxs-lookup"><span data-stu-id="02b84-129">Binding descriptor tables</span></span>

![Adiciona tabelas de descritor à assinatura raiz](images/root-tables-2.png)

<span data-ttu-id="02b84-131">Este exemplo mostra o uso de duas tabelas de descritor; um declarando uma tabela de cinco descritores que estarão disponíveis no momento da execução em um \_ \_ heap de descritor cbv SRV UAV e outro declarando uma tabela de dois descritores que serão exibidos no momento da execução em um heap de descritor de amostra.</span><span class="sxs-lookup"><span data-stu-id="02b84-131">This example shows the use of two descriptor tables; one declaring a table of five descriptors that will be available at execution time in a CBV\_SRV\_UAV descriptor heap, and another declaring a table of two descriptors that will show up at execution time in a sampler descriptor heap.</span></span>

<span data-ttu-id="02b84-132">Para associar tabelas de descritor ao gravar uma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="02b84-132">To bind descriptor tables when recording a command list.</span></span>

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

<span data-ttu-id="02b84-133">Outro recurso da assinatura raiz é a constante raiz FLOAT4 que tem quatro DWORDs de tamanho.</span><span class="sxs-lookup"><span data-stu-id="02b84-133">Another feature of the root signature is the float4 root constant that is four DWORDS in size.</span></span> <span data-ttu-id="02b84-134">O comando a seguir associa apenas os dois DWORDs intermediários dos quatro.</span><span class="sxs-lookup"><span data-stu-id="02b84-134">The following command binds just the middle two DWORDS of the four.</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a><span data-ttu-id="02b84-135">Uma assinatura de raiz mais complexa</span><span class="sxs-lookup"><span data-stu-id="02b84-135">A more complex root signature</span></span>

![uma assinatura de raiz complexa com muitos elementos](images/root-tables-3.png)

<span data-ttu-id="02b84-137">Este exemplo mostra uma assinatura raiz densa com a maioria dos tipos de entradas.</span><span class="sxs-lookup"><span data-stu-id="02b84-137">This example shows a dense root signature with most types of entries.</span></span> <span data-ttu-id="02b84-138">Duas das tabelas de descritores (nos slots 3 e 6) incluem matrizes de tamanho não associado.</span><span class="sxs-lookup"><span data-stu-id="02b84-138">Two of the descriptor tables (at slots 3 and 6) include unbounded size arrays.</span></span> <span data-ttu-id="02b84-139">A carga aqui está no aplicativo apenas para tocar descritores válidos em um heap.</span><span class="sxs-lookup"><span data-stu-id="02b84-139">The burden here is on the application to only touch valid descriptors in a heap.</span></span> <span data-ttu-id="02b84-140">Matrizes não associadas, ou muito grandes, exigem a camada de hardware 2 + do suporte de associação de recursos.</span><span class="sxs-lookup"><span data-stu-id="02b84-140">Unbounded, or very large arrays, require hardware tier 2+ of resource binding support.</span></span>

<span data-ttu-id="02b84-141">Há dois exemplos estáticos (vinculados sem a necessidade de Slots de assinatura raiz).</span><span class="sxs-lookup"><span data-stu-id="02b84-141">There are two static samplers (bound without requiring root signature slots).</span></span>

<span data-ttu-id="02b84-142">No slot 9, UAV U4 e UAV U5 são declarados no mesmo deslocamento da tabela de descritores.</span><span class="sxs-lookup"><span data-stu-id="02b84-142">At slot 9, UAV u4 and UAV u5 are declared at the same descriptor table offset.</span></span> <span data-ttu-id="02b84-143">Esse é o uso de um descritor com alias, um descritor na memória aparecerá como U4 e U5 nos sombreadores HLSL.</span><span class="sxs-lookup"><span data-stu-id="02b84-143">This is use of an aliased descriptor, one descriptor in memory will show up as both u4 and u5 in the HLSL shaders.</span></span> <span data-ttu-id="02b84-144">Nesse caso, o sombreador deve ser compilado com a \_ opção d3d10 do sombreador de \_ recursos \_ pode ser \_ alias ou a `/res_may_alias` opção or em FXC.</span><span class="sxs-lookup"><span data-stu-id="02b84-144">In this case the shader must be compiled with the D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, or the or `/res_may_alias` option in FXC.</span></span> <span data-ttu-id="02b84-145">Os descritores com alias permitem a vinculação de uma descrição a vários pontos de ligação, sem a necessidade de fazer nenhuma alteração nos sombreadores.</span><span class="sxs-lookup"><span data-stu-id="02b84-145">Aliased descriptors enable one descriptor to be bound to multiple bind points, without having to make any changes to the shaders.</span></span>

## <a name="streaming-shader-resource-views"></a><span data-ttu-id="02b84-146">Exibições de recurso do sombreador de streaming</span><span class="sxs-lookup"><span data-stu-id="02b84-146">Streaming Shader Resource Views</span></span>

![exibições de recurso do sombreador de streaming nesta assinatura raiz](images/root-tables-4.png)

<span data-ttu-id="02b84-148">Essa assinatura raiz ilustra um cenário em que todos os SRVs são transmitidos e estão fora de uma matriz grande.</span><span class="sxs-lookup"><span data-stu-id="02b84-148">This root signature illustrates a scenario where all SRVs are streamed in and out of one large array.</span></span> <span data-ttu-id="02b84-149">No momento da execução, uma tabela de descritores pode ser definida uma vez quando a assinatura raiz é definida.</span><span class="sxs-lookup"><span data-stu-id="02b84-149">At execution time, a descriptor table can be set once when the root signature is set.</span></span> <span data-ttu-id="02b84-150">Em seguida, todas as leituras de textura são feitas pela indexação na matriz por meio de constantes alimentadas por meio dos primeiros argumentos raiz.</span><span class="sxs-lookup"><span data-stu-id="02b84-150">Then all texture reads are done by indexing into the array via constants fed via the first few root arguments.</span></span> <span data-ttu-id="02b84-151">Apenas um único heap de descritor é necessário e só é atualizado conforme as texturas são transmitidas ou não de Slots de descritor livres.</span><span class="sxs-lookup"><span data-stu-id="02b84-151">Only a single descriptor heap is needed, and is only updated as textures are streamed in or out of free descriptor slots.</span></span>

<span data-ttu-id="02b84-152">Os deslocamentos do descritor no heap grande são identificados por sombreadores usando as constantes nas exibições do buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="02b84-152">The descriptor offsets in the large heap are identified by shaders using the constants in the Constant Buffer Views.</span></span> <span data-ttu-id="02b84-153">Por exemplo, se um sombreador receber uma ID de material, ele poderá indexar uma matriz grande usando a constante para acessar o descritor necessário (que faz referência à textura necessária).</span><span class="sxs-lookup"><span data-stu-id="02b84-153">For example, if a shader is given a material ID, it can index into the one large array using the constant to access the required descriptor (which references the required texture).</span></span>

<span data-ttu-id="02b84-154">Este cenário requer hardware com associação de recursos tier2 +.</span><span class="sxs-lookup"><span data-stu-id="02b84-154">This scenario requires hardware with resource binding tier2+.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02b84-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02b84-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02b84-156">Camadas de hardware de associação de recursos</span><span class="sxs-lookup"><span data-stu-id="02b84-156">Resource Binding Hardware Tiers</span></span>](hardware-support.md)
</dt> <dt>

[<span data-ttu-id="02b84-157">Associação de recursos em HLSL</span><span class="sxs-lookup"><span data-stu-id="02b84-157">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="02b84-158">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="02b84-158">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





---
title: numthreads
description: Define o número de threads a serem executados em um único grupo de threads quando um sombreador de computação é expedido (consulte expedição ID3D11DeviceContext).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366650"
---
# <a name="numthreads"></a><span data-ttu-id="acc70-103">numthreads</span><span class="sxs-lookup"><span data-stu-id="acc70-103">numthreads</span></span>

<span data-ttu-id="acc70-104">Define o número de threads a serem executados em um único grupo de threads quando um sombreador de computação é expedido (consulte [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span><span class="sxs-lookup"><span data-stu-id="acc70-104">Defines the number of threads to be executed in a single thread group when a compute shader is dispatched (see [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span></span>


```
numthreads(X, Y, Z)    
```



<span data-ttu-id="acc70-105">Os valores X, Y e Z indicam o tamanho do grupo de threads em uma direção específica e o total de X \* Y \* Z fornece o número de threads no grupo.</span><span class="sxs-lookup"><span data-stu-id="acc70-105">The X, Y and Z values indicate the size of the thread group in a particular direction and the total of X\*Y\*Z gives the number of threads in the group.</span></span> <span data-ttu-id="acc70-106">A capacidade de especificar o tamanho do grupo de threads em três dimensões permite que threads individuais sejam acessados de uma maneira que as estruturas de dados 2D e 3D logicamente.</span><span class="sxs-lookup"><span data-stu-id="acc70-106">The ability to specify the size of the thread group across three dimensions allows individual threads to be accessed in a manner that logically 2D and 3D data structures.</span></span>

<span data-ttu-id="acc70-107">Por exemplo, se um sombreador de computação estiver fazendo a adição de matriz 4x4, então numthreads poderá ser definido como numthreads (4, 4, 1) e a indexação nos threads individuais corresponderá automaticamente às entradas de matriz.</span><span class="sxs-lookup"><span data-stu-id="acc70-107">For example, if a compute shader is doing 4x4 matrix addition then numthreads could be set to numthreads(4,4,1) and the indexing in the individual threads would automatically match the matrix entries.</span></span> <span data-ttu-id="acc70-108">O sombreador de computação também poderia declarar um grupo de threads com o mesmo número de threads (16) usando numthreads (16, 1, 1), no entanto, ele teria que calcular a entrada da matriz atual com base no número do thread atual.</span><span class="sxs-lookup"><span data-stu-id="acc70-108">The compute shader could also declare a thread group with the same number of threads (16) using numthreads(16,1,1), however it would then have to calculate the current matrix entry based on the current thread number.</span></span>

<span data-ttu-id="acc70-109">Os valores de parâmetro permitidos para **numthreads** dependem da versão do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="acc70-109">The allowable parameter values for **numthreads** depends on the compute shader version.</span></span>



| <span data-ttu-id="acc70-110">Sombreador de computação</span><span class="sxs-lookup"><span data-stu-id="acc70-110">Compute Shader</span></span> | <span data-ttu-id="acc70-111">Z máximo</span><span class="sxs-lookup"><span data-stu-id="acc70-111">Maximum Z</span></span> | <span data-ttu-id="acc70-112">Máximo de threads (X \* Y \* Z)</span><span class="sxs-lookup"><span data-stu-id="acc70-112">Maximum Threads (X\*Y\*Z)</span></span> |
|----------------|-----------|---------------------------|
| <span data-ttu-id="acc70-113">cs \_ 4 \_ x</span><span class="sxs-lookup"><span data-stu-id="acc70-113">cs\_4\_x</span></span>       | <span data-ttu-id="acc70-114">1</span><span class="sxs-lookup"><span data-stu-id="acc70-114">1</span></span>         | <span data-ttu-id="acc70-115">768</span><span class="sxs-lookup"><span data-stu-id="acc70-115">768</span></span>                       |
| <span data-ttu-id="acc70-116">cs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="acc70-116">cs\_5\_0</span></span>       | <span data-ttu-id="acc70-117">64</span><span class="sxs-lookup"><span data-stu-id="acc70-117">64</span></span>        | <span data-ttu-id="acc70-118">1024</span><span class="sxs-lookup"><span data-stu-id="acc70-118">1024</span></span>                      |



 

<span data-ttu-id="acc70-119">A ilustração a seguir mostra a relação entre os parâmetros passados para [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), expedição (5, 3, 2), os valores especificados no atributo numthreads, numthreads (10, 8, 3) e valores que serão passados para o sombreador de computação para os valores de sistema relacionados ao thread ([VA \_ GroupIndex](sv-groupindex.md),[VA \_ DispatchThreadID](sv-dispatchthreadid.md),[VA \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupId](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="acc70-119">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the numthreads attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

<span data-ttu-id="acc70-121">Esse atributo tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="acc70-121">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="acc70-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="acc70-122">Vertex</span></span> | <span data-ttu-id="acc70-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="acc70-123">Hull</span></span> | <span data-ttu-id="acc70-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="acc70-124">Domain</span></span> | <span data-ttu-id="acc70-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="acc70-125">Geometry</span></span> | <span data-ttu-id="acc70-126">16x16</span><span class="sxs-lookup"><span data-stu-id="acc70-126">Pixel</span></span> | <span data-ttu-id="acc70-127">Computação</span><span class="sxs-lookup"><span data-stu-id="acc70-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="acc70-128">x</span><span class="sxs-lookup"><span data-stu-id="acc70-128">x</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="acc70-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="acc70-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acc70-130">Atributos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="acc70-130">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="acc70-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="acc70-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
---
title: Novos tipos de recursos
description: Vários novos tipos de recursos foram adicionados no Direct3D 11.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Buffer de endereço de byte (visão geral)
- Buffer de leitura/gravação (visão geral)
- Buffer estruturado (visão geral)
- Buffer de acesso não ordenado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366349"
---
# <a name="new-resource-types"></a><span data-ttu-id="771cf-107">Novos tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="771cf-107">New Resource Types</span></span>

<span data-ttu-id="771cf-108">Vários novos tipos de recursos foram adicionados no Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="771cf-108">Several new resource types have been added in Direct3D 11.</span></span>

-   [<span data-ttu-id="771cf-109">Buffers de leitura/gravação e texturas</span><span class="sxs-lookup"><span data-stu-id="771cf-109">Read/Write Buffers and Textures</span></span>](#readwrite-buffers-and-textures)
-   [<span data-ttu-id="771cf-110">Buffer estruturado</span><span class="sxs-lookup"><span data-stu-id="771cf-110">Structured Buffer</span></span>](#structured-buffer)
-   [<span data-ttu-id="771cf-111">Buffer de endereço de byte</span><span class="sxs-lookup"><span data-stu-id="771cf-111">Byte Address Buffer</span></span>](#byte-address-buffer)
-   [<span data-ttu-id="771cf-112">Buffer ou textura de acesso não ordenado</span><span class="sxs-lookup"><span data-stu-id="771cf-112">Unordered Access Buffer or Texture</span></span>](#unordered-access-buffer-or-texture)
    -   [<span data-ttu-id="771cf-113">Acrescentar e consumir buffer</span><span class="sxs-lookup"><span data-stu-id="771cf-113">Append and Consume Buffer</span></span>](#append-and-consume-buffer)
-   [<span data-ttu-id="771cf-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="771cf-114">Related topics</span></span>](#related-topics)

## <a name="readwrite-buffers-and-textures"></a><span data-ttu-id="771cf-115">Buffers de leitura/gravação e texturas</span><span class="sxs-lookup"><span data-stu-id="771cf-115">Read/Write Buffers and Textures</span></span>

<span data-ttu-id="771cf-116">Os recursos do Shader Model 4 são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="771cf-116">Shader model 4 resources are read only.</span></span> <span data-ttu-id="771cf-117">O Shader Model 5 implementa um novo conjunto correspondente de recursos de leitura/gravação:</span><span class="sxs-lookup"><span data-stu-id="771cf-117">Shader model 5 implements a new corresponding set of read/write resources:</span></span>

-   [<span data-ttu-id="771cf-118">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="771cf-118">RWBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   <span data-ttu-id="771cf-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span><span class="sxs-lookup"><span data-stu-id="771cf-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span></span>
-   <span data-ttu-id="771cf-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span><span class="sxs-lookup"><span data-stu-id="771cf-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span></span>
-   [<span data-ttu-id="771cf-121">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="771cf-121">RWTexture3D</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

<span data-ttu-id="771cf-122">Esses recursos exigem uma variável de recurso para acessar a memória (por meio de indexação), pois não há métodos para acessar a memória diretamente.</span><span class="sxs-lookup"><span data-stu-id="771cf-122">These resources require a resource variable to access memory (through indexing) as there are no methods for accessing memory directly.</span></span> <span data-ttu-id="771cf-123">Uma variável de recurso pode ser usada nos lados esquerdo e direito de uma equação; Se usado no lado direito, o tipo de modelo deve ser um componente único (float, int ou uint).</span><span class="sxs-lookup"><span data-stu-id="771cf-123">A resource variable can be used on the left and right sides of an equation; if used on the right side, the template type must be single component (float, int, or uint).</span></span>

## <a name="structured-buffer"></a><span data-ttu-id="771cf-124">Buffer estruturado</span><span class="sxs-lookup"><span data-stu-id="771cf-124">Structured Buffer</span></span>

<span data-ttu-id="771cf-125">Um buffer estruturado é um buffer que contém elementos de tamanhos iguais.</span><span class="sxs-lookup"><span data-stu-id="771cf-125">A structured buffer is a buffer that contains elements of equal sizes.</span></span> <span data-ttu-id="771cf-126">Use uma estrutura com um ou mais tipos de membro para definir um elemento.</span><span class="sxs-lookup"><span data-stu-id="771cf-126">Use a structure with one or more member types to define an element.</span></span> <span data-ttu-id="771cf-127">Aqui está uma estrutura com três membros.</span><span class="sxs-lookup"><span data-stu-id="771cf-127">Here is a structure with three members.</span></span>


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



<span data-ttu-id="771cf-128">Use esta estrutura para declarar um buffer estruturado como este:</span><span class="sxs-lookup"><span data-stu-id="771cf-128">Use this structure to declare a structured buffer like this:</span></span>


```
StructuredBuffer<MyStruct> mySB;
```



<span data-ttu-id="771cf-129">Além da indexação, um buffer estruturado dá suporte ao acesso a um único membro como este:</span><span class="sxs-lookup"><span data-stu-id="771cf-129">In addition to indexing, a structured buffer supports accessing a single member like this:</span></span>


```
float4 myColor = mySb[27].Color;
```



<span data-ttu-id="771cf-130">Use os seguintes tipos de objeto para acessar um buffer estruturado:</span><span class="sxs-lookup"><span data-stu-id="771cf-130">Use the following object types to access a structured buffer:</span></span>

-   <span data-ttu-id="771cf-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) é um buffer estruturado somente leitura.</span><span class="sxs-lookup"><span data-stu-id="771cf-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) is a read only structured buffer.</span></span>
-   <span data-ttu-id="771cf-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) é um buffer estruturado de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="771cf-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) is a read/write structured buffer.</span></span>

<span data-ttu-id="771cf-133">[Funções atômicas](direct3d-11-advanced-stages-cs-atomic-functions.md) que implementam operações interbloqueadas são permitidas em elementos int e uint em um **RWStructuredBuffer**.</span><span class="sxs-lookup"><span data-stu-id="771cf-133">[Atomic functions](direct3d-11-advanced-stages-cs-atomic-functions.md) which implement interlocked operations are allowed on int and uint elements in an **RWStructuredBuffer**.</span></span>

## <a name="byte-address-buffer"></a><span data-ttu-id="771cf-134">Buffer de endereço de byte</span><span class="sxs-lookup"><span data-stu-id="771cf-134">Byte Address Buffer</span></span>

<span data-ttu-id="771cf-135">Um buffer de endereço de byte é um buffer cujo conteúdo é endereçável por um deslocamento de byte.</span><span class="sxs-lookup"><span data-stu-id="771cf-135">A byte address buffer is a buffer whose contents are addressable by a byte offset.</span></span> <span data-ttu-id="771cf-136">Normalmente, o conteúdo de um [buffer](overviews-direct3d-11-resources-buffers-intro.md) é indexado por elemento usando um stride para cada elemento e o número do elemento (N), conforme fornecido por S \* N.</span><span class="sxs-lookup"><span data-stu-id="771cf-136">Normally, the contents of a [buffer](overviews-direct3d-11-resources-buffers-intro.md) are indexed per element using a stride for each element (S) and the element number (N) as given by S\*N.</span></span> <span data-ttu-id="771cf-137">Um buffer de endereço de byte, que também pode ser chamado de buffer bruto, usa um deslocamento de valor de byte do início do buffer para acessar dados.</span><span class="sxs-lookup"><span data-stu-id="771cf-137">A byte address buffer, which can also be called a raw buffer, uses a byte value offset from the beginning of the buffer to access data.</span></span> <span data-ttu-id="771cf-138">O valor de byte deve ser um múltiplo de quatro para que seja alinhado em DWORD.</span><span class="sxs-lookup"><span data-stu-id="771cf-138">The byte value must be a multiple of four so that it is DWORD aligned.</span></span> <span data-ttu-id="771cf-139">Se qualquer outro valor for fornecido, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="771cf-139">If any other value is provided, behavior is undefined.</span></span>

<span data-ttu-id="771cf-140">O modelo de sombreador 5 apresenta objetos para acessar um [buffer de endereço de byte somente leitura](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) , bem como um [buffer de endereço de byte de leitura/gravação](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span><span class="sxs-lookup"><span data-stu-id="771cf-140">Shader model 5 introduces objects for accessing a [read-only byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) as well as a [read-write byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span></span> <span data-ttu-id="771cf-141">O conteúdo de um buffer de endereço de byte é projetado para ser um inteiro sem sinal de 32 bits; Se o valor no buffer não for realmente um inteiro sem sinal, use uma função como [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) para lê-lo.</span><span class="sxs-lookup"><span data-stu-id="771cf-141">The contents of a byte address buffer is designed to be a 32-bit unsigned integer; if the value in the buffer is not really an unsigned integer, use a function such as [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) to read it.</span></span>

## <a name="unordered-access-buffer-or-texture"></a><span data-ttu-id="771cf-142">Buffer ou textura de acesso não ordenado</span><span class="sxs-lookup"><span data-stu-id="771cf-142">Unordered Access Buffer or Texture</span></span>

<span data-ttu-id="771cf-143">Um recurso de acesso não ordenado (que inclui buffers, texturas e matrizes de textura-sem várias amostras) permite o acesso de leitura/gravação não ordenado de forma temporal de vários threads.</span><span class="sxs-lookup"><span data-stu-id="771cf-143">An unordered access resource (which includes buffers, textures, and texture arrays - without multisampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="771cf-144">Isso significa que esse tipo de recurso pode ser lido/gravado simultaneamente por vários threads sem gerar conflitos de memória por meio do uso de [funções atômicas](direct3d-11-advanced-stages-cs-atomic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="771cf-144">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts through the use of [Atomic Functions](direct3d-11-advanced-stages-cs-atomic-functions.md).</span></span>

<span data-ttu-id="771cf-145">Crie uma textura ou um buffer de acesso não ordenado chamando uma função como [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ou [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e passando o sinalizador de **\_ \_ \_ acesso de vínculo não ordenado de D3D11** da enumeração de [**\_ \_ sinalizador de associação D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="771cf-145">Create an unordered access buffer or texture by calling a function such as [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) or [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and passing in the **D3D11\_BIND\_UNORDERED\_ACCESS** flag from the [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) enumeration.</span></span>

<span data-ttu-id="771cf-146">Os recursos de acesso não ordenados só podem ser associados a sombreadores de pixel e sombreadores de computação.</span><span class="sxs-lookup"><span data-stu-id="771cf-146">Unordered access resources can only be bound to pixel shaders and compute shaders.</span></span> <span data-ttu-id="771cf-147">Durante a execução, sombreadores de pixel ou sombreadores de computação executados em paralelo têm os mesmos recursos de acesso não ordenados associados.</span><span class="sxs-lookup"><span data-stu-id="771cf-147">During execution, pixel shaders or compute shaders running in parallel have the same unordered access resources bound.</span></span>

### <a name="append-and-consume-buffer"></a><span data-ttu-id="771cf-148">Acrescentar e consumir buffer</span><span class="sxs-lookup"><span data-stu-id="771cf-148">Append and Consume Buffer</span></span>

<span data-ttu-id="771cf-149">Um buffer de acréscimo e consumo é um tipo especial de recurso não ordenado que dá suporte à adição e à remoção de valores do final de um buffer semelhante ao modo como uma pilha funciona.</span><span class="sxs-lookup"><span data-stu-id="771cf-149">An append and consume buffer is a special type of an unordered resource that supports adding and removing values from the end of a buffer similar to the way a stack works.</span></span>

<span data-ttu-id="771cf-150">Um buffer de acréscimo e consumo deve ser um buffer estruturado:</span><span class="sxs-lookup"><span data-stu-id="771cf-150">An append and consume buffer must be a structured buffer:</span></span>

-   [<span data-ttu-id="771cf-151">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="771cf-151">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="771cf-152">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="771cf-152">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

<span data-ttu-id="771cf-153">Use esses recursos por meio de seus métodos, esses recursos não usam variáveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="771cf-153">Use these resources through their methods, these resources do not use resource variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="771cf-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="771cf-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="771cf-155">Visão geral do sombreador de computação</span><span class="sxs-lookup"><span data-stu-id="771cf-155">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 
---
title: Acessando recursos
description: Há várias maneiras de acessar os recursos.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988687"
---
# <a name="accessing-resources"></a><span data-ttu-id="7e8ba-103">Acessando recursos</span><span class="sxs-lookup"><span data-stu-id="7e8ba-103">Accessing Resources</span></span>

<span data-ttu-id="7e8ba-104">Há várias maneiras de acessar os [recursos](overviews-direct3d-11-resources-types.md).</span><span class="sxs-lookup"><span data-stu-id="7e8ba-104">There are several ways to access [resources](overviews-direct3d-11-resources-types.md).</span></span> <span data-ttu-id="7e8ba-105">Independentemente, as garantias de Direct3D retornarão zero para qualquer recurso que seja acessado fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="7e8ba-105">Regardless, Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

-   [<span data-ttu-id="7e8ba-106">Acesso por deslocamento de byte</span><span class="sxs-lookup"><span data-stu-id="7e8ba-106">Access By Byte Offset</span></span>](#access-by-byte-offset)
-   [<span data-ttu-id="7e8ba-107">Acesso por índice</span><span class="sxs-lookup"><span data-stu-id="7e8ba-107">Access By Index</span></span>](#access-by-index)
-   [<span data-ttu-id="7e8ba-108">Acesso por método MIPS</span><span class="sxs-lookup"><span data-stu-id="7e8ba-108">Access By Mips Method</span></span>](#access-by-mips-method)
-   [<span data-ttu-id="7e8ba-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e8ba-109">Related topics</span></span>](#related-topics)

## <a name="access-by-byte-offset"></a><span data-ttu-id="7e8ba-110">Acesso por deslocamento de byte</span><span class="sxs-lookup"><span data-stu-id="7e8ba-110">Access By Byte Offset</span></span>

<span data-ttu-id="7e8ba-111">Dois novos tipos de buffer podem ser acessados usando um deslocamento de byte:</span><span class="sxs-lookup"><span data-stu-id="7e8ba-111">Two new buffer types can be accessed using a byte offset:</span></span>

-   <span data-ttu-id="7e8ba-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) é um buffer somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7e8ba-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) is a read-only buffer.</span></span>
-   <span data-ttu-id="7e8ba-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) é um buffer de leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="7e8ba-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) is a read or write buffer.</span></span>

## <a name="access-by-index"></a><span data-ttu-id="7e8ba-114">Acesso por índice</span><span class="sxs-lookup"><span data-stu-id="7e8ba-114">Access By Index</span></span>

<span data-ttu-id="7e8ba-115">Os tipos de recursos podem usar um índice para fazer referência a um local específico no recurso.</span><span class="sxs-lookup"><span data-stu-id="7e8ba-115">Resource types can use an index to reference a specific location in the resource.</span></span> <span data-ttu-id="7e8ba-116">Considere este exemplo:</span><span class="sxs-lookup"><span data-stu-id="7e8ba-116">Consider this example:</span></span>


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



<span data-ttu-id="7e8ba-117">Este exemplo atribui os 4 valores float que são armazenados no Texel localizado na posição *pos* no recurso de textura 2D *MyTexture* para a variável *myvar* .</span><span class="sxs-lookup"><span data-stu-id="7e8ba-117">This example assigns the 4 float values that are stored at the texel located at the *pos* position in the *myTexture* 2D texture resource to the *myVar* variable.</span></span>

> [!Note]  
> <span data-ttu-id="7e8ba-118">O padrão para acessar uma textura dessa maneira é o nível de mipmap zero (o nível mais detalhado).</span><span class="sxs-lookup"><span data-stu-id="7e8ba-118">The default for accessing a texture in this way is mipmap level zero (the most detailed level).</span></span>

 

> [!Note]  
> <span data-ttu-id="7e8ba-119">A linha "FLOAT4 myVar = MyTexture \[ pos \] ;" é equivalente a "FLOAT4 myvar = mytextura. Load (uint3 (POS, 0));".</span><span class="sxs-lookup"><span data-stu-id="7e8ba-119">The "float4 myVar = myTexture\[pos\];" line is equivalent to "float4 myVar = myTexture.Load(uint3(pos,0));".</span></span> <span data-ttu-id="7e8ba-120">O acesso por índice é um novo aprimoramento de sintaxe de HLSL.</span><span class="sxs-lookup"><span data-stu-id="7e8ba-120">Access by index is a new HLSL syntax enhancement.</span></span>

 

> [!Note]  
> <span data-ttu-id="7e8ba-121">O compilador na versão de junho de 2010 do SDK do DirectX e posterior permite que você Indexe todos os tipos de recursos, exceto os [buffers de endereço de byte](direct3d-11-advanced-stages-cs-resources.md).</span><span class="sxs-lookup"><span data-stu-id="7e8ba-121">The compiler in the June 2010 version of the DirectX SDK and later lets you index all resource types except for [byte address buffers](direct3d-11-advanced-stages-cs-resources.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="7e8ba-122">O compilador de junho de 2010 e posterior permite que você declare variáveis de recurso locais.</span><span class="sxs-lookup"><span data-stu-id="7e8ba-122">The June 2010 compiler and later lets you declare local resource variables.</span></span> <span data-ttu-id="7e8ba-123">Você pode atribuir recursos definidos globalmente (como *MyTexture*) a essas variáveis e usá-las da mesma maneira que suas contrapartes globais.</span><span class="sxs-lookup"><span data-stu-id="7e8ba-123">You can assign globally defined resources (like *myTexture*) to these variables and use them the same way as their global counterparts.</span></span>

 

## <a name="access-by-mips-method"></a><span data-ttu-id="7e8ba-124">Acesso por método MIPS</span><span class="sxs-lookup"><span data-stu-id="7e8ba-124">Access By Mips Method</span></span>

<span data-ttu-id="7e8ba-125">Os objetos de textura têm um método **MIPS** (por exemplo, [**Texture2D. MIPS**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), que pode ser usado para especificar o nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="7e8ba-125">Texture objects have a **mips** method (for example, [**Texture2D.mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), which you can use to specify the mipmap level.</span></span> <span data-ttu-id="7e8ba-126">Este exemplo lê a cor armazenada em (7, 16) no mipmap nível 2 em uma textura 2D:</span><span class="sxs-lookup"><span data-stu-id="7e8ba-126">This example reads the color stored at (7,16) on mipmap level 2 in a 2D texture:</span></span>


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



<span data-ttu-id="7e8ba-127">Esse é um aprimoramento do compilador de junho de 2010 e posterior.</span><span class="sxs-lookup"><span data-stu-id="7e8ba-127">This is an enhancement from the June 2010 compiler and later.</span></span> <span data-ttu-id="7e8ba-128">A expressão "MyTexture. MIPS \[ 2 \] \[ uint2 (x, y) \] " é equivalente a "mytextura. Load (uint3 (x, y, 2))".</span><span class="sxs-lookup"><span data-stu-id="7e8ba-128">The "myTexture.mips\[2\]\[uint2(x,y)\]" expression is equivalent to "myTexture.Load(uint3(x,y,2))".</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e8ba-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e8ba-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e8ba-130">Visão geral do sombreador de computação</span><span class="sxs-lookup"><span data-stu-id="7e8ba-130">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 
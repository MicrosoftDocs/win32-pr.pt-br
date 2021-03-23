---
title: Usando constantes diretamente na assinatura raiz
description: Os aplicativos podem definir constantes raiz na assinatura raiz, cada uma como um conjunto de valores de 32 bits. Eles aparecem na HLSL (linguagem de sombreamento de alto nível) como um buffer constante. Observe que os buffers de constante por motivos históricos são exibidos como conjuntos de valores de 4x32 bits.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103949"
---
# <a name="using-constants-directly-in-the-root-signature"></a><span data-ttu-id="7472c-105">Usando constantes diretamente na assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="7472c-105">Using Constants Directly in the Root Signature</span></span>

<span data-ttu-id="7472c-106">Os aplicativos podem definir constantes raiz na assinatura raiz, cada uma como um conjunto de valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7472c-106">Applications can define root constants in the root signature, each as a set of 32-bit values.</span></span> <span data-ttu-id="7472c-107">Eles aparecem na HLSL (linguagem de sombreamento de alto nível) como um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="7472c-107">They appear in High Level Shading Language (HLSL) as a constant buffer.</span></span> <span data-ttu-id="7472c-108">Observe que os buffers de constante por motivos históricos são exibidos como conjuntos de valores de 4x32 bits.</span><span class="sxs-lookup"><span data-stu-id="7472c-108">Note that constant buffers for historical reasons are viewed as sets of 4x32-bit values.</span></span>

<span data-ttu-id="7472c-109">Cada conjunto de constantes de usuário é tratado como uma matriz escalar de valores de 32 bits, indexáveis e somente leitura dinamicamente do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7472c-109">Each set of user constants is treated as a scalar array of 32 -bit values, dynamically indexable and read-only from the shader.</span></span> <span data-ttu-id="7472c-110">A indexação fora dos limites que indexa um determinado conjunto de constantes raiz produz resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="7472c-110">Out of bounds indexing a given set of root constants produces undefined results.</span></span> <span data-ttu-id="7472c-111">No HLSL, as definições de estrutura de dados podem ser fornecidas para que as constantes do usuário forneçam tipos.</span><span class="sxs-lookup"><span data-stu-id="7472c-111">In HLSL, data structure definitions can be provided for the user constants to give them types.</span></span> <span data-ttu-id="7472c-112">Por exemplo, se a assinatura raiz definir um conjunto de 4 constantes raiz, HLSL poderá sobrepor a estrutura a seguir.</span><span class="sxs-lookup"><span data-stu-id="7472c-112">For example, if the root signature defines a set of 4 root constants, HLSL can overlay the following structure on them.</span></span>

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

<span data-ttu-id="7472c-113">As matrizes não são permitidas em buffers constantes que são mapeados para constantes raiz, pois não há suporte para a indexação dinâmica no espaço de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="7472c-113">Arrays are not permitted in constant buffers that get mapped onto root constants since dynamic indexing in the root signature space is not supported.</span></span> <span data-ttu-id="7472c-114">Por exemplo, é inválido ter uma entrada no buffer de constantes como `float myArray[2];` .</span><span class="sxs-lookup"><span data-stu-id="7472c-114">For example, it is invalid to have an entry in the constant buffer like `float myArray[2];`.</span></span> <span data-ttu-id="7472c-115">Um buffer de constantes que é mapeado para constantes raiz não pode ser uma matriz; Portanto, é inválido mapear para `cbuffer myCBArray[2]` constantes raiz.</span><span class="sxs-lookup"><span data-stu-id="7472c-115">A constant buffer that is mapped to root constants cannot itself be an array; therefore, it is invalid to map `cbuffer myCBArray[2]` into root constants.</span></span>

<span data-ttu-id="7472c-116">As constantes podem ser parcialmente definidas.</span><span class="sxs-lookup"><span data-stu-id="7472c-116">Constants can be partially set.</span></span> <span data-ttu-id="7472c-117">Por exemplo, se a assinatura raiz definir valores de 4 32 bits em *RootTableBindSlot* 2, qualquer subconjunto das quatro constantes poderá ser definido de cada vez (os outros permanecem inalterados).</span><span class="sxs-lookup"><span data-stu-id="7472c-117">For example, if the root signature defines four 32-bit values at *RootTableBindSlot* 2, then any subset of the four constants can be set at a time (the others remain unchanged).</span></span> <span data-ttu-id="7472c-118">Isso pode ser útil em pacotes que herdam o estado da assinatura raiz e podem alterá-lo parcialmente.</span><span class="sxs-lookup"><span data-stu-id="7472c-118">This can be useful in bundles that inherit root signature state and can partially change it.</span></span>

<span data-ttu-id="7472c-119">Ao definir constantes, tenha cuidado com o layout de buffer constante esperado pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="7472c-119">When setting constants be careful of the constant buffer layout expected by the shader.</span></span> <span data-ttu-id="7472c-120">É possível que as constantes sejam preenchidas em `vec4` limites, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="7472c-120">It is possible that constants are padded to `vec4` boundaries, for example.</span></span> <span data-ttu-id="7472c-121">Para verificar o layout esperado, verifique as informações de reflexo do sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="7472c-121">To verify the layout expected, check the reflection information from the HLSL shader.</span></span>

<span data-ttu-id="7472c-122">As APIs a seguir (da interface [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) são para definir constantes diretamente na assinatura raiz:</span><span class="sxs-lookup"><span data-stu-id="7472c-122">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting constants directly on the root signature:</span></span>

-   [<span data-ttu-id="7472c-123">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="7472c-123">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [<span data-ttu-id="7472c-124">**SetGraphicsRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="7472c-124">**SetGraphicsRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [<span data-ttu-id="7472c-125">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="7472c-125">**SetComputeRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="7472c-126">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="7472c-126">**SetComputeRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

<span data-ttu-id="7472c-127">Além disso, consulte a estrutura de [**\_ \_ constantes raiz do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="7472c-127">Also, refer to the [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7472c-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7472c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7472c-129">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="7472c-129">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





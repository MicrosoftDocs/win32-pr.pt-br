---
description: No Direct3D 10, os recursos de textura são acessados com uma exibição, que é um mecanismo para a interpretação de hardware de um recurso na memória.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Exibições de textura (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83dd83b1a3896637ce73505de00027ea9dfadac4
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335580"
---
# <a name="texture-views-direct3d-10"></a><span data-ttu-id="251e9-103">Exibições de textura (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="251e9-103">Texture Views (Direct3D 10)</span></span>

<span data-ttu-id="251e9-104">No Direct3D 10, os recursos de textura são acessados com uma exibição, que é um mecanismo para a interpretação de hardware de um recurso na memória.</span><span class="sxs-lookup"><span data-stu-id="251e9-104">In Direct3D 10, texture resources are accessed with a view, which is a mechanism for hardware interpretation of a resource in memory.</span></span> <span data-ttu-id="251e9-105">Um modo de exibição permite que um estágio de pipeline específico acesse somente os [sub-recursos](d3d10-graphics-programming-guide-resources-types.md) de que precisa, na representação desejada pelo app.</span><span class="sxs-lookup"><span data-stu-id="251e9-105">A view allows a particular pipeline stage to access only the [subresources](d3d10-graphics-programming-guide-resources-types.md) it needs, in the representation desired by the application.</span></span>

<span data-ttu-id="251e9-106">Uma exibição dá suporte à noção de um recurso sem tipo.</span><span class="sxs-lookup"><span data-stu-id="251e9-106">A view supports the notion of a type-less resource.</span></span> <span data-ttu-id="251e9-107">Um recurso sem tipo é um recurso criado com um tamanho específico, mas não um tipo de dados específico.</span><span class="sxs-lookup"><span data-stu-id="251e9-107">A type-less resource is a resource created with a specific size but not a specific data type.</span></span> <span data-ttu-id="251e9-108">Os dados são interpretados dinamicamente quando são associados ao pipeline.</span><span class="sxs-lookup"><span data-stu-id="251e9-108">The data is interpreted dynamically when it is bound to the pipeline.</span></span>

<span data-ttu-id="251e9-109">A ilustração a seguir mostra um exemplo de associação de uma matriz de texturas 2D a 6 texturas como um recurso sombreador, criando uma exibição de recurso sombreador para isso.</span><span class="sxs-lookup"><span data-stu-id="251e9-109">The following illustration shows an example of binding a 2D texture array with 6 textures as a shader resource by creating a shader resource view for it.</span></span> <span data-ttu-id="251e9-110">Em seguida, o recurso é tratado como uma matriz de texturas.</span><span class="sxs-lookup"><span data-stu-id="251e9-110">The resource is then addressed as an array of textures.</span></span> <span data-ttu-id="251e9-111">(Observação: um sub-recurso não pode ser associado como entrada e saída ao pipeline simultaneamente.)</span><span class="sxs-lookup"><span data-stu-id="251e9-111">(Note: a subresource cannot be bound as both input and output to the pipeline simultaneously.)</span></span>

![ilustração de uma matriz com seis texturas](images/d3d10-cube-texture-faces.png)

<span data-ttu-id="251e9-113">Ao usar uma matriz de texturas 2D como destino de renderização, o recurso pode ser exibido como uma matriz de texturas 2D (6 neste exemplo) com níveis de mipmap (3 neste exemplo).</span><span class="sxs-lookup"><span data-stu-id="251e9-113">When using a 2D texture array as a render target, the resource can be viewed as an array of 2D textures (6 in this example) with mipmap levels (3 in this example).</span></span>

<span data-ttu-id="251e9-114">Crie um objeto de exibição para um destino de renderização chamando CreateRenderTargetView.</span><span class="sxs-lookup"><span data-stu-id="251e9-114">Create a view object for a render target by calling CreateRenderTargetView.</span></span> <span data-ttu-id="251e9-115">Em seguida, chame OMSetRenderTargets para definir a exibição do destino de renderização para o pipeline.</span><span class="sxs-lookup"><span data-stu-id="251e9-115">Then call OMSetRenderTargets to set the render target view to the pipeline.</span></span> <span data-ttu-id="251e9-116">Renderize os destinos de renderização chamando Draw e usando RenderTargetArrayIndex para indexar à textura adequada na matriz.</span><span class="sxs-lookup"><span data-stu-id="251e9-116">Render into the render targets by calling Draw and using the RenderTargetArrayIndex to index into the proper texture in the array.</span></span> <span data-ttu-id="251e9-117">Você pode usar um sub-recurso (uma combinação de nível de mipmap e índice de matriz) para associar a qualquer matriz de sub-recursos.</span><span class="sxs-lookup"><span data-stu-id="251e9-117">You can use a subresource (a mipmap level, array index combination) to bind to any array of subresources.</span></span> <span data-ttu-id="251e9-118">Você pode associar o segundo nível de mipmap e só atualizar esse nível de mipmap específico se quiser, como na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="251e9-118">So you could bind to the second mipmap level and only update this particular mipmap level if you wanted, as in the following illustration.</span></span>

![ilustração de associação somente ao segundo nível de mipmap de uma matriz de texturas](images/d3d10-cube-texture-faces-subresource.png)



<span data-ttu-id="251e9-120">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="251e9-120">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="251e9-121">No Direct3D 10, você não associa mais um recurso diretamente ao pipeline, cria uma exibição de um recurso e, em seguida, define a exibição para o pipeline.</span><span class="sxs-lookup"><span data-stu-id="251e9-121">In Direct3D 10, you no longer bind a resource directly to the pipeline, you create a view of a resource, and then set the view to the pipeline.</span></span> <span data-ttu-id="251e9-122">Isso permite que a validação e o mapeamento no tempo de execução e o driver ocorram na criação da exibição, minimizando a verificação de tipo no momento da associação.</span><span class="sxs-lookup"><span data-stu-id="251e9-122">This allows validation and mapping in the runtime and driver to occur at view creation, minimizing type checking at bind-time.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="251e9-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="251e9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="251e9-124">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="251e9-124">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 





---
title: Clonando um efeito
description: A clonagem de um efeito cria uma segunda cópia praticamente idêntica do efeito.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636303"
---
# <a name="cloning-an-effect"></a><span data-ttu-id="6302f-103">Clonando um efeito</span><span class="sxs-lookup"><span data-stu-id="6302f-103">Cloning an Effect</span></span>

<span data-ttu-id="6302f-104">A clonagem de um efeito cria uma segunda cópia praticamente idêntica do efeito.</span><span class="sxs-lookup"><span data-stu-id="6302f-104">Cloning an effect creates a second, almost identical copy of the effect.</span></span> <span data-ttu-id="6302f-105">Consulte o único qualificador a seguir para obter uma explicação de por que não é exato.</span><span class="sxs-lookup"><span data-stu-id="6302f-105">See the following single qualifier for an explanation of why it is not exact.</span></span> <span data-ttu-id="6302f-106">Uma segunda cópia de um efeito é útil quando um deseja usar a estrutura de efeitos em vários threads, pois o tempo de execução do efeito não é thread-safe para manter o alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="6302f-106">A second copy of an effect is useful when one wants to use the effects framework on multiple threads, since the effect runtime is not thread safe to maintain high performance.</span></span>

<span data-ttu-id="6302f-107">Como os contextos de dispositivo também são não-seguros, threads diferentes devem passar contextos de dispositivo diferentes para o método ID3DX11EffectPass:: apply.</span><span class="sxs-lookup"><span data-stu-id="6302f-107">Since device contexts are also non-thread-safe, different threads should pass different device contexts to the ID3DX11EffectPass::Apply method.</span></span>

<span data-ttu-id="6302f-108">Um efeito pode ser clonado com a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="6302f-108">An effect can be cloned with the following syntax:</span></span>


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



<span data-ttu-id="6302f-109">No exemplo acima, a cópia clonada encapsulará o mesmo estado que o efeito original, independentemente de qual estado o efeito original está.</span><span class="sxs-lookup"><span data-stu-id="6302f-109">In the above example, the cloned copy will encapsulate the same state as the original effect, regardless of what state the original effect is in.</span></span> <span data-ttu-id="6302f-110">Especialmente:</span><span class="sxs-lookup"><span data-stu-id="6302f-110">In particular:</span></span>

1.  <span data-ttu-id="6302f-111">Se pEffect for otimizado, o efeito de pCloned será otimizado</span><span class="sxs-lookup"><span data-stu-id="6302f-111">If pEffect is optimized, pCloned Effect is optimized</span></span>
2.  <span data-ttu-id="6302f-112">Se pEffect tiver algumas variáveis gerenciadas pelo usuário, o efeito de pCloned terá as mesmas variáveis gerenciadas pelo usuário (consulte a descrição única abaixo)</span><span class="sxs-lookup"><span data-stu-id="6302f-112">If pEffect has some user-managed variables, pCloned Effect will have the same user-managed variables (see the single description below)</span></span>
3.  <span data-ttu-id="6302f-113">Todas as atualizações de variáveis pendentes (até que uma chamada de aplicação atualiza o estado do dispositivo) em pEffect estarão pendentes em pClonedEffect</span><span class="sxs-lookup"><span data-stu-id="6302f-113">Any pending variable updates (until an Apply call updates device state) in pEffect will be pending in pClonedEffect</span></span>

<span data-ttu-id="6302f-114">Os seguintes objetos de dispositivo do Direct3D 11 são imutáveis ou nunca são atualizados pela estrutura de efeitos, portanto, o efeito clonado apontará para os mesmos objetos que o efeito original:</span><span class="sxs-lookup"><span data-stu-id="6302f-114">The following Direct3D 11 device objects are immutable or never updated by the effects framework, so the cloned effect will point to the same objects as the original effect:</span></span>

1.  <span data-ttu-id="6302f-115">Objetos de bloco de estado (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span><span class="sxs-lookup"><span data-stu-id="6302f-115">State block objects (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span></span>
2.  <span data-ttu-id="6302f-116">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="6302f-116">Shaders</span></span>
3.  <span data-ttu-id="6302f-117">Instâncias de classe</span><span class="sxs-lookup"><span data-stu-id="6302f-117">Class instances</span></span>
4.  <span data-ttu-id="6302f-118">Texturas (não incluindo buffers de textura)</span><span class="sxs-lookup"><span data-stu-id="6302f-118">Textures (not including texture buffers)</span></span>
5.  <span data-ttu-id="6302f-119">Exibições de acesso não ordenado</span><span class="sxs-lookup"><span data-stu-id="6302f-119">Unordered access views</span></span>

<span data-ttu-id="6302f-120">Os seguintes objetos de dispositivo do Direct3D 11 são imutáveis e modificados pelo tempo de execução de efeito (a menos que seja gerenciado pelo usuário ou único em um efeito clonado); novas cópias desses objetos são criadas quando não único:</span><span class="sxs-lookup"><span data-stu-id="6302f-120">The following Direct3D 11 device objects are both immutable and modified by the effect runtime (unless user-managed or single in a cloned effect); new copies of these objects are created when non-single:</span></span>

1.  <span data-ttu-id="6302f-121">Buffers de constantes</span><span class="sxs-lookup"><span data-stu-id="6302f-121">Constant buffers</span></span>
2.  <span data-ttu-id="6302f-122">Buffers de textura</span><span class="sxs-lookup"><span data-stu-id="6302f-122">Texture Buffers</span></span>

## <a name="single-constant-buffers-and-texture-buffers"></a><span data-ttu-id="6302f-123">Buffers de única constante e buffers de textura</span><span class="sxs-lookup"><span data-stu-id="6302f-123">Single Constant Buffers and Texture Buffers</span></span>

<span data-ttu-id="6302f-124">Observe que essa discussão se aplica a buffers de constante e texturas, mas os buffers de constante são assumidos para facilitar a leitura.</span><span class="sxs-lookup"><span data-stu-id="6302f-124">Note that this discussion applies to both constant buffers and textures, but constant buffers are assumed for ease of reading.</span></span>

<span data-ttu-id="6302f-125">Pode haver casos em que um buffer de constante é atualizado apenas por um thread, mas o estado do dispositivo definido por efeitos clonados usará esses dados.</span><span class="sxs-lookup"><span data-stu-id="6302f-125">There may be cases where a constant buffer is only updated by one thread, but device state set by cloned effects will use this data.</span></span> <span data-ttu-id="6302f-126">Por exemplo, o efeito principal pode atualizar o mundo e exibir matrizes que são referenciadas de sombreadores em efeitos clonados que não alteram o mundo e exibem matrizes.</span><span class="sxs-lookup"><span data-stu-id="6302f-126">For example, the main effect may update the world and view matrices which are referenced from shaders in cloned effects which do not change the world and view matrices.</span></span> <span data-ttu-id="6302f-127">Nesses casos, os efeitos clonados precisam fazer referência ao buffer de constantes atual em vez de recriar um.</span><span class="sxs-lookup"><span data-stu-id="6302f-127">In these cases, the cloned effects need to reference the current constant buffer instead of recreating one.</span></span>

<span data-ttu-id="6302f-128">Há duas maneiras de atingir esse resultado desejado:</span><span class="sxs-lookup"><span data-stu-id="6302f-128">There are two ways to achieve this desired result:</span></span>

1.  <span data-ttu-id="6302f-129">Use ID3DX11EffectConstantBuffer:: SetConstantBuffer no efeito clonado para torná-lo gerenciado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="6302f-129">Use ID3DX11EffectConstantBuffer::SetConstantBuffer on the cloned effect to make it user-managed</span></span>
2.  <span data-ttu-id="6302f-130">Marcar o buffer de constantes como "único" no código HLSL, forçando o tempo de execução de efeito a tratar é como gerenciado pelo usuário após a clonagem</span><span class="sxs-lookup"><span data-stu-id="6302f-130">Mark the constant buffer as "single" in the HLSL code, forcing the effect runtime to treat is as user-managed after cloning</span></span>

<span data-ttu-id="6302f-131">Há duas diferenças entre os dois métodos acima.</span><span class="sxs-lookup"><span data-stu-id="6302f-131">There are two differences between the two methods above.</span></span> <span data-ttu-id="6302f-132">Primeiro, no método 1, um novo ID3D11Buffer será criado e o usuário antes de SetConstantBuffer é chamado.</span><span class="sxs-lookup"><span data-stu-id="6302f-132">First, in method 1, a new ID3D11Buffer will be created and user before SetConstantBuffer is called.</span></span> <span data-ttu-id="6302f-133">Além disso, depois de chamar UndoSetConstantBuffer no efeito clonado, a variável no método 1will aponta para o buffer recém-criado (que os efeitos serão atualizados quando aplicados), enquanto a variável no método 2 continuará a apontar para o buffer original (não atualizá-lo na aplicação).</span><span class="sxs-lookup"><span data-stu-id="6302f-133">Also, after calling UndoSetConstantBuffer in the cloned effect, the variable in method 1will point to the newly-created buffer (which effects will update on Apply) while the variable in method 2 will continue to point to the original buffer (not updating it on Apply).</span></span>

<span data-ttu-id="6302f-134">Consulte o exemplo a seguir em HLSL:</span><span class="sxs-lookup"><span data-stu-id="6302f-134">See the following example in HLSL:</span></span>


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



<span data-ttu-id="6302f-135">Durante a clonagem, o efeito clonado criará um novo ID3D11Buffer para objectdata e preencherá seu conteúdo em aplicar, mas fará referência ao ID3D11Buffer original de ViewData.</span><span class="sxs-lookup"><span data-stu-id="6302f-135">While cloning, the cloned effect will create a new ID3D11Buffer for ObjectData, and fill its contents on Apply, but reference the original ID3D11Buffer for ViewData.</span></span> <span data-ttu-id="6302f-136">O único qualificador pode ser ignorado no processo de clonagem definindo o sinalizador de D3DX11 de \_ clonagem de efeito de \_ clone não \_ \_ único.</span><span class="sxs-lookup"><span data-stu-id="6302f-136">The single qualifier can be ignored in the cloning process by setting the D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6302f-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6302f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6302f-138">Efeitos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6302f-138">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 





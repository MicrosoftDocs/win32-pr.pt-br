---
description: Os cartões de multicabeçalho são aqueles que têm um buffer de quadro comum e acelerador, conversores de digital-to-Analog independentes (DACs) e monitoramento de saídas.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456519"
---
# <a name="multihead-direct3d-9"></a><span data-ttu-id="c67bc-103">Multihead (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c67bc-103">Multihead (Direct3D 9)</span></span>

<span data-ttu-id="c67bc-104">Os cartões de multicabeçalho são aqueles que têm um buffer de quadro comum e acelerador, conversores de digital-to-Analog independentes (DACs) e monitoramento de saídas.</span><span class="sxs-lookup"><span data-stu-id="c67bc-104">Multihead cards are those that have a common frame buffer and accelerator, independent digital-to-analog converters (DACs), and monitor outputs.</span></span> <span data-ttu-id="c67bc-105">Esses dispositivos podem oferecer suporte a vários monitores muito mais utilizáveis do que um número semelhante de adaptadores de vídeo heterogêneos.</span><span class="sxs-lookup"><span data-stu-id="c67bc-105">Such devices can offer much more usable multiple monitor support than a similar number of heterogeneous display adapters.</span></span>

<span data-ttu-id="c67bc-106">Os cartões de vários cabeçotes são expostos na API como um único dispositivo de nível de API que pode gerar várias cadeias de troca de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="c67bc-106">Multihead cards are exposed in the API as a single API-level device that can drive several full-screen swap chains.</span></span> <span data-ttu-id="c67bc-107">Consequentemente, todos os recursos são compartilhados com todos os cabeçotes, e cada cabeçalho tem exatamente os mesmos recursos.</span><span class="sxs-lookup"><span data-stu-id="c67bc-107">Consequently, all resources are shared with all the heads, and each head has exactly the same capabilities.</span></span> <span data-ttu-id="c67bc-108">Cada cabeçalho pode ser definido para modos de exibição independentes.</span><span class="sxs-lookup"><span data-stu-id="c67bc-108">Each head can be set to independent display modes.</span></span> <span data-ttu-id="c67bc-109">Você pode usar chamadas separadas para [**IDirect3DSwapChain9::P reenviada**](/windows/desktop/api) para atualizar cada cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="c67bc-109">You can use separate calls to [**IDirect3DSwapChain9::Present**](/windows/desktop/api) to refresh each head.</span></span> <span data-ttu-id="c67bc-110">Você também pode usar uma chamada para [**IDirect3DDevice9::P reenviada**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para atualizar cada cabeçalho sequencialmente.</span><span class="sxs-lookup"><span data-stu-id="c67bc-110">You can also use one call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) to refresh each head sequentially.</span></span>

> [!Note]  
> <span data-ttu-id="c67bc-111">A atualização de cada cabeçalho não ocorre simultaneamente com uma única chamada para [**IDirect3DDevice9::P reenviada**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="c67bc-111">The refresh of each head does not occur simultaneously with a single call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="c67bc-112">As estatísticas presentes no Direct3D 9Ex podem usar a estrutura [**D3DPRESENTSTATS**](d3dpresentstats.md) para manter as atualizações para cada cabeçalho perto umas das outras para limitar os efeitos de divisão em vários cabeçotes de adaptadores.</span><span class="sxs-lookup"><span data-stu-id="c67bc-112">Present statistics in Direct3D 9Ex can use the [**D3DPRESENTSTATS**](d3dpresentstats.md) structure to keep the refreshes to each head close to each other to limit tearing effects across multiple heads of adapters.</span></span> <span data-ttu-id="c67bc-113">Para obter informações sobre a sincronização de quadros de aplicativos de modelo do Direct3D 9Ex flip, consulte [melhorias do Direct3d 9EX](../direct3darticles/direct3d-9ex-improvements.md).</span><span class="sxs-lookup"><span data-stu-id="c67bc-113">For information about synchronizing frames of Direct3D 9Ex flip model applications, see [Direct3D 9Ex Improvements](../direct3darticles/direct3d-9ex-improvements.md).</span></span>

 

<span data-ttu-id="c67bc-114">Cada cadeia de permuta para um dispositivo de multicabeçalho deve ser tela inteira.</span><span class="sxs-lookup"><span data-stu-id="c67bc-114">Each swap chain for a multihead device must be full screen.</span></span> <span data-ttu-id="c67bc-115">Quando um dispositivo entra no modo de multitítulo, ele deve permanecer em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="c67bc-115">When a device has entered multihead mode, it must remain full screen.</span></span> <span data-ttu-id="c67bc-116">A transição de volta para o modo de janela requer a destruição do dispositivo (exceto para a operação normal ALT + TAB-to-Minimize).</span><span class="sxs-lookup"><span data-stu-id="c67bc-116">The transition back to windowed mode requires the destruction of the device (except for the normal ALT+TAB-to-minimize operation).</span></span>

<span data-ttu-id="c67bc-117">O método antigo de dividir a memória de vídeo entre os cabeçotes e tratar cada cabeça como um acelerador totalmente independente ainda será um cenário de uso comum.</span><span class="sxs-lookup"><span data-stu-id="c67bc-117">The old method of dividing video memory between the heads and treating each head as a fully independent accelerator will still be a common usage scenario.</span></span> <span data-ttu-id="c67bc-118">Essa proposta não substitui esse mecanismo, a menos que o aplicativo tenha sido especificamente codificado para funcionar no modo de multicabeçalho do Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c67bc-118">This proposal does not replace that mechanism unless the application has been specifically coded to function in the Direct3D 9 multihead mode.</span></span>

<span data-ttu-id="c67bc-119">Os drivers recebem conhecimento adequado para alternar entre os dois modos de operação.</span><span class="sxs-lookup"><span data-stu-id="c67bc-119">Drivers are given adequate knowledge to switch between the two modes of operation.</span></span>

<span data-ttu-id="c67bc-120">Um cabeçalho será chamado de cabeçalho mestre e todos os outros cabeçotes no mesmo cartão serão chamados de cabeçalhos subordinados.</span><span class="sxs-lookup"><span data-stu-id="c67bc-120">One head will be called the master head, and all other heads on the same card be called subordinate heads.</span></span> <span data-ttu-id="c67bc-121">Se mais de um adaptador de vários cabeçotes estiver presente em um sistema, o mestre e seus subordinados de um adaptador de vários cabeçalhos serão chamados de grupo.</span><span class="sxs-lookup"><span data-stu-id="c67bc-121">If more than one multihead adapter is present in a system, the master and its subordinates from one multihead adapter are called a group.</span></span> <span data-ttu-id="c67bc-122">Os grupos são indicados pelo ordinal do adaptador de seu cabeçalho mestre.</span><span class="sxs-lookup"><span data-stu-id="c67bc-122">Groups are denoted by the adapter ordinal of their master head.</span></span>

<span data-ttu-id="c67bc-123">A estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) foi atualizada para expor os novos limites de hardware a seguir.</span><span class="sxs-lookup"><span data-stu-id="c67bc-123">The [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure has been updated to expose the following new hardware caps.</span></span>


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   <span data-ttu-id="c67bc-124">NumberOfAdaptersInGroup é 1 para adaptadores convencionais e maior que 1 para o adaptador mestre de um cartão de vários cabeçotes.</span><span class="sxs-lookup"><span data-stu-id="c67bc-124">NumberOfAdaptersInGroup is 1 for conventional adapters, and greater than 1 for the master adapter of a multihead card.</span></span> <span data-ttu-id="c67bc-125">O valor será 0 para um adaptador subordinado de um cartão de multitítulo.</span><span class="sxs-lookup"><span data-stu-id="c67bc-125">The value will be 0 for a subordinate adapter of a multihead card.</span></span> <span data-ttu-id="c67bc-126">Cada cartão pode ter no máximo um mestre, mas pode ter muitos subordinados.</span><span class="sxs-lookup"><span data-stu-id="c67bc-126">Each card can have at most one master, but might have many subordinates.</span></span>
-   <span data-ttu-id="c67bc-127">MasterAdapterOrdinal indica qual dispositivo é o mestre para esse subordinado.</span><span class="sxs-lookup"><span data-stu-id="c67bc-127">MasterAdapterOrdinal indicates which device is the master for this subordinate.</span></span>
-   <span data-ttu-id="c67bc-128">AdapterOrdinalInGroup indica a ordem na qual os cabeçalhos são referenciados pela API.</span><span class="sxs-lookup"><span data-stu-id="c67bc-128">AdapterOrdinalInGroup indicates the order in which heads are referenced by the API.</span></span> <span data-ttu-id="c67bc-129">O adaptador Mestre sempre tem AdapterOrdinalInGroup 0.</span><span class="sxs-lookup"><span data-stu-id="c67bc-129">The master adapter always has AdapterOrdinalInGroup 0.</span></span> <span data-ttu-id="c67bc-130">Esses valores não correspondem aos ordinais do adaptador passados para os métodos IDirect3D9, mas aplicam-se apenas aos cabeçalhos de um grupo.</span><span class="sxs-lookup"><span data-stu-id="c67bc-130">These values do not correspond to the adapter ordinals passed to the IDirect3D9 methods, but apply only to heads within a group.</span></span>

<span data-ttu-id="c67bc-131">Essa definição permite que os cartões multitítulo continuem a apresentar vários adaptadores como se fossem cartões independentes, assim como faziam no DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="c67bc-131">This definition allows multihead cards to continue to present multiple adapters as if they were independent cards, just as they did in DirectX 8.</span></span>

<span data-ttu-id="c67bc-132">Para criar um dispositivo de multicabeçalho, especifique o sinalizador de comportamento D3DCREATE \_ \_ dispositivo de adaptador de placa em [**IDirect3D9:: CreateDevice**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="c67bc-132">To create a multihead device, specify the behavior flag D3DCREATE\_ADAPTERGROUP\_DEVICE in [**IDirect3D9::CreateDevice**](/windows/desktop/api).</span></span> <span data-ttu-id="c67bc-133">Os parâmetros de apresentação (uma matriz [**de \_ parâmetros D3DPRESENT**](d3dpresent-parameters.md)) devem conter elementos NumberOfAdaptersInGroup.</span><span class="sxs-lookup"><span data-stu-id="c67bc-133">The presentation parameters (an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md)) should contain NumberOfAdaptersInGroup elements.</span></span> <span data-ttu-id="c67bc-134">O tempo de execução atribuirá cada elemento a cada cabeçalho em ordem numérica AdapterOrdinalInGroup.</span><span class="sxs-lookup"><span data-stu-id="c67bc-134">The runtime will assign each element to each head in AdapterOrdinalInGroup numerical order.</span></span> <span data-ttu-id="c67bc-135">Quando o \_ dispositivo de \_ grupo de adaptadores D3DCREATE está definido, cada parâmetro de apresentação deve ter:</span><span class="sxs-lookup"><span data-stu-id="c67bc-135">When D3DCREATE\_ADAPTERGROUP\_DEVICE is set, each presentation parameter must have:</span></span>

-   <span data-ttu-id="c67bc-136">O membro em janela definido como **false** (em outras palavras, seja tela inteira).</span><span class="sxs-lookup"><span data-stu-id="c67bc-136">The Windowed member set to **FALSE** (in other words, be full screen).</span></span>
-   <span data-ttu-id="c67bc-137">O mesmo valor para o membro EnableAutoDepthStencil dos [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c67bc-137">The same value for the EnableAutoDepthStencil member of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="c67bc-138">Além disso, se EnableAutoDepthStencil for **true**, cada um dos campos a seguir deverá ter o mesmo valor para cada [**\_ parâmetro D3DPRESENT**](d3dpresent-parameters.md):</span><span class="sxs-lookup"><span data-stu-id="c67bc-138">In addition, if EnableAutoDepthStencil is **TRUE**, then each of the following fields must have the same value for each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md):</span></span>

-   <span data-ttu-id="c67bc-139">AutoDepthStencilFormat</span><span class="sxs-lookup"><span data-stu-id="c67bc-139">AutoDepthStencilFormat</span></span>
-   <span data-ttu-id="c67bc-140">BackBufferWidth</span><span class="sxs-lookup"><span data-stu-id="c67bc-140">BackBufferWidth</span></span>
-   <span data-ttu-id="c67bc-141">BackBufferHeight</span><span class="sxs-lookup"><span data-stu-id="c67bc-141">BackBufferHeight</span></span>
-   <span data-ttu-id="c67bc-142">BackBufferFormat</span><span class="sxs-lookup"><span data-stu-id="c67bc-142">BackBufferFormat</span></span>

<span data-ttu-id="c67bc-143">Se o DAC estiver definido, chamadas adicionais para [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) são ilegais.</span><span class="sxs-lookup"><span data-stu-id="c67bc-143">If DAC is set, additional calls to [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) are illegal.</span></span>

<span data-ttu-id="c67bc-144">Se o dispositivo tiver sido criado com o DAC, [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) esperará uma matriz [**de \_ parâmetros D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c67bc-144">If the device was created with the DAC, [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) will expect an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="c67bc-145">Cada estrutura de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) passada para [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) deve ser tela inteira.</span><span class="sxs-lookup"><span data-stu-id="c67bc-145">Each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure passed to [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) must be full screen.</span></span> <span data-ttu-id="c67bc-146">Para alternar de volta para o modo em janela, o aplicativo deve destruir o dispositivo e recriar um dispositivo não multicabeçalho no modo de janela.</span><span class="sxs-lookup"><span data-stu-id="c67bc-146">To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.</span></span>

<span data-ttu-id="c67bc-147">Este é um cenário de uso básico:</span><span class="sxs-lookup"><span data-stu-id="c67bc-147">Here is a basic usage scenario:</span></span>


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



<span data-ttu-id="c67bc-148">Para obter mais informações, consulte [**IDirect3D9:: CreateDevice**](/windows/desktop/api) e [**IDirect3DDevice9:: GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span><span class="sxs-lookup"><span data-stu-id="c67bc-148">For more information, see [**IDirect3D9::CreateDevice**](/windows/desktop/api) and [**IDirect3DDevice9::GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c67bc-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c67bc-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c67bc-150">Dicas de programação</span><span class="sxs-lookup"><span data-stu-id="c67bc-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 

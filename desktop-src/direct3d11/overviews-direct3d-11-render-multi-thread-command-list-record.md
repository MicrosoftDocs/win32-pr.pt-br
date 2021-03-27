---
title: Como registrar uma lista de comandos
description: Este tópico mostra como criar e registrar uma lista de comandos.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636250"
---
# <a name="how-to-record-a-command-list"></a><span data-ttu-id="fb1d0-103">Como gravar uma lista de comandos</span><span class="sxs-lookup"><span data-stu-id="fb1d0-103">How to: Record a Command List</span></span>

<span data-ttu-id="fb1d0-104">Uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md) é uma lista registrada de comandos de renderização.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="fb1d0-105">Este tópico mostra como criar e registrar uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="fb1d0-105">This topic shows how to create and record a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="fb1d0-106">Use uma lista de comandos para registrar comandos de renderização e reproduzi-los novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-106">Use a command list to record render commands and play them back later.</span></span> <span data-ttu-id="fb1d0-107">Uma lista de comandos é conveniente para dividir tarefas de renderização entre threads.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-107">A command list is convenient for splitting rendering tasks between threads.</span></span>

<span data-ttu-id="fb1d0-108">**Para registrar uma lista de comandos**</span><span class="sxs-lookup"><span data-stu-id="fb1d0-108">**To record a command list**</span></span>

1.  <span data-ttu-id="fb1d0-109">Uma lista de comandos deve ser criada a partir de um contexto adiado, que contém ações de processamento e estado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-109">A command list must be created from a deferred context, which contains device state and rendering actions.</span></span> <span data-ttu-id="fb1d0-110">Dado um dispositivo, crie um contexto adiado chamando [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="fb1d0-110">Given a device, create a deferred context by calling [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  <span data-ttu-id="fb1d0-111">Use o contexto adiado para renderizar.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-111">Use the deferred context to render.</span></span>

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    <span data-ttu-id="fb1d0-112">Este exemplo simples limpa um destino de renderização, mas você pode adicionar outros comandos de renderização.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-112">This simple example clears a render target, but you could add additional render commands.</span></span>

3.  <span data-ttu-id="fb1d0-113">Crie/registre uma lista de comandos chamando [**ID3D11DeviceContext:: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) e passando um ponteiro para uma interface [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) não inicializada.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-113">Create/record a command list by calling [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) and passing a pointer to an uninitialized [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) interface.</span></span>

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    <span data-ttu-id="fb1d0-114">Quando o método retorna, uma lista de comandos é criada contendo todos os comandos de renderização e uma interface é retornada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-114">When the method returns, a command list is created containing all the render commands and an interface is returned to the application.</span></span>

    <span data-ttu-id="fb1d0-115">O parâmetro booliano informa ao tempo de execução o que fazer com o estado do pipeline no contexto adiado.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-115">The boolean parameter tells the runtime what to do with the pipeline state in the deferred context.</span></span> <span data-ttu-id="fb1d0-116">**Verdadeiro** significa restaurar o estado do contexto do dispositivo para sua condição de lista de pré-comandos quando a gravação for concluída, **falso** significa que não altere o estado após a gravação.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-116">**TRUE** means restore the state of the device context to its pre-command list condition when recording is completed, **FALSE** means do not change the state after recording.</span></span> <span data-ttu-id="fb1d0-117">Isso significa que o contexto do dispositivo refletirá as alterações de estado contidas na lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="fb1d0-117">This means that the device context will reflect the state changes contained in the command list.</span></span>

<span data-ttu-id="fb1d0-118">Para ver um exemplo de reprodução de uma lista de comandos, consulte [como: reproduzir uma lista de comandos](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span><span class="sxs-lookup"><span data-stu-id="fb1d0-118">To see an example for playing back a command list, see [How to: Play Back a Command List](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb1d0-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb1d0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb1d0-120">Lista de comandos</span><span class="sxs-lookup"><span data-stu-id="fb1d0-120">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="fb1d0-121">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="fb1d0-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





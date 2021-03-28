---
title: Como criar uma cadeia de permuta
description: Este tópico mostra como criar uma cadeia de permuta que encapsula dois ou mais buffers que são usados para renderização e exibição.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8355eafff6e233b89be82fd9e58ca53224248e84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366347"
---
# <a name="how-to-create-a-swap-chain"></a><span data-ttu-id="dfcb8-103">Como: criar uma cadeia de permuta</span><span class="sxs-lookup"><span data-stu-id="dfcb8-103">How To: Create a Swap Chain</span></span>

<span data-ttu-id="dfcb8-104">Este tópico mostra como criar uma cadeia de permuta que encapsula dois ou mais buffers que são usados para renderização e exibição.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-104">This topic show how to create a swap chain that encapsulates two or more buffers that are used for rendering and display.</span></span> <span data-ttu-id="dfcb8-105">Normalmente, eles contêm um buffer frontal que é apresentado ao dispositivo de vídeo e um buffer de fundo que serve como o destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-105">They usually contain a front buffer that is presented to the display device and a back buffer that serves as the render target.</span></span> <span data-ttu-id="dfcb8-106">Depois que o contexto imediato é concluído renderizando para o buffer de fundo, a cadeia de permuta apresenta o buffer de fundo alternando os dois buffers.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-106">After the immediate context is done rendering to the back buffer, the swap chain presents the back buffer by swapping the two buffers.</span></span>

<span data-ttu-id="dfcb8-107">A cadeia de permuta define várias características de renderização, incluindo:</span><span class="sxs-lookup"><span data-stu-id="dfcb8-107">The swap chain defines several rendering characteristics including:</span></span>

-   <span data-ttu-id="dfcb8-108">O tamanho da área de renderização.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-108">The size of the render area.</span></span>
-   <span data-ttu-id="dfcb8-109">A taxa de atualização de exibição.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-109">The display refresh rate.</span></span>
-   <span data-ttu-id="dfcb8-110">O modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-110">The display mode.</span></span>
-   <span data-ttu-id="dfcb8-111">O formato da superfície.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-111">The surface format.</span></span>

<span data-ttu-id="dfcb8-112">Defina as características da cadeia de permuta preenchendo uma [**estrutura \_ \_ \_ desc de cadeia de permuta dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) e inicializando uma interface [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) .</span><span class="sxs-lookup"><span data-stu-id="dfcb8-112">Define the characteristics of the swap chain by filling in a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure and initializing an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) interface.</span></span> <span data-ttu-id="dfcb8-113">Inicialize uma cadeia de permuta chamando [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="dfcb8-113">Initialize a swap chain by calling [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="create-a-device-and-a-swap-chain"></a><span data-ttu-id="dfcb8-114">Criar um dispositivo e uma cadeia de permuta</span><span class="sxs-lookup"><span data-stu-id="dfcb8-114">Create a device and a swap chain</span></span>

<span data-ttu-id="dfcb8-115">Para inicializar um dispositivo e uma cadeia de troca, use uma das duas funções a seguir:</span><span class="sxs-lookup"><span data-stu-id="dfcb8-115">To initialize a device and swap chain, use one of the following two functions:</span></span>

-   <span data-ttu-id="dfcb8-116">Use a função [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) quando desejar inicializar a cadeia de permuta ao mesmo tempo que a inicialização do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-116">Use the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function when you want to initialize the swap chain at the same time as device initialization.</span></span> <span data-ttu-id="dfcb8-117">Normalmente, essa é a opção mais fácil.</span><span class="sxs-lookup"><span data-stu-id="dfcb8-117">This usually is the easiest option.</span></span>

-   <span data-ttu-id="dfcb8-118">Use a função [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) quando você já tiver criado uma cadeia de permuta usando [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span><span class="sxs-lookup"><span data-stu-id="dfcb8-118">Use the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function when you have already created a swap chain using [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfcb8-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dfcb8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfcb8-120">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="dfcb8-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="dfcb8-121">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="dfcb8-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 
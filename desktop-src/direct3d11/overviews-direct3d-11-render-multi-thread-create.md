---
title: Criação de objeto com multithreading
description: Use a interface ID3D11Device para criar recursos e objetos, use o ID3D11DeviceContext para renderização.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916295"
---
# <a name="object-creation-with-multithreading"></a><span data-ttu-id="f36f9-103">Criação de objeto com multithreading</span><span class="sxs-lookup"><span data-stu-id="f36f9-103">Object Creation with Multithreading</span></span>

<span data-ttu-id="f36f9-104">Use a interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para criar recursos e objetos, use o [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) para [renderização](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="f36f9-104">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

<span data-ttu-id="f36f9-105">Aqui estão alguns exemplos de como criar recursos:</span><span class="sxs-lookup"><span data-stu-id="f36f9-105">Here are some examples of how to create resources:</span></span>

-   [<span data-ttu-id="f36f9-106">Como criar um buffer de vértice</span><span class="sxs-lookup"><span data-stu-id="f36f9-106">How to: Create a Vertex Buffer</span></span>](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [<span data-ttu-id="f36f9-107">Como: criar um buffer de índice</span><span class="sxs-lookup"><span data-stu-id="f36f9-107">How to: Create an Index Buffer</span></span>](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [<span data-ttu-id="f36f9-108">Como: criar um buffer de constantes</span><span class="sxs-lookup"><span data-stu-id="f36f9-108">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [<span data-ttu-id="f36f9-109">Como: inicializar uma textura a partir de um arquivo</span><span class="sxs-lookup"><span data-stu-id="f36f9-109">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a><span data-ttu-id="f36f9-110">Considerações de multithread</span><span class="sxs-lookup"><span data-stu-id="f36f9-110">Multithreading Considerations</span></span>

<span data-ttu-id="f36f9-111">A quantidade de simultaneidade de criação de recursos e renderização que seu aplicativo pode atingir depende do nível de suporte multithreading que o Driver implementa.</span><span class="sxs-lookup"><span data-stu-id="f36f9-111">The amount of concurrency of resource creation and rendering that your application can achieve depends on the level of multithreading support that the driver implements.</span></span> <span data-ttu-id="f36f9-112">Se o driver oferecer suporte a criações simultâneas, o aplicativo deverá ter problemas de simultaneidade muito menos.</span><span class="sxs-lookup"><span data-stu-id="f36f9-112">If the driver supports concurrent creates, then the application should have much less concurrency concerns.</span></span> <span data-ttu-id="f36f9-113">No entanto, se o driver não oferecer suporte à criação simultânea de objeto, a quantidade de simultaneidade será extremamente limitada.</span><span class="sxs-lookup"><span data-stu-id="f36f9-113">However, if the driver does not support concurrent object creation, the amount of concurrency is extremely limited.</span></span> <span data-ttu-id="f36f9-114">Para entender a quantidade de suporte disponível em um driver, consulte o driver para obter o valor do membro **DriverConcurrentCreates** da estrutura [**de \_ \_ \_ Threading de dados do recurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) .</span><span class="sxs-lookup"><span data-stu-id="f36f9-114">To understand the amount of support available in a driver, query the driver for the value of the **DriverConcurrentCreates** member of the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure.</span></span> <span data-ttu-id="f36f9-115">Para obter mais informações sobre como verificar o suporte de driver de multithreading, consulte [como verificar o suporte ao driver](overviews-direct3d-11-render-multi-thread-support.md).</span><span class="sxs-lookup"><span data-stu-id="f36f9-115">For more information about checking for driver support of multithreading, see [How To: Check for Driver Support](overviews-direct3d-11-render-multi-thread-support.md).</span></span>

<span data-ttu-id="f36f9-116">As operações simultâneas não levam necessariamente ao melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="f36f9-116">Concurrent operations do not necessarily lead to better performance.</span></span> <span data-ttu-id="f36f9-117">Por exemplo, criar e carregar uma textura normalmente é limitado pela largura de banda da memória.</span><span class="sxs-lookup"><span data-stu-id="f36f9-117">For example, creating and loading a texture is typically limited by memory bandwidth.</span></span> <span data-ttu-id="f36f9-118">A tentativa de criar e carregar várias texturas pode não ser mais rápida do que fazer uma textura de cada vez, mesmo que isso deixe vários núcleos de CPU ociosos.</span><span class="sxs-lookup"><span data-stu-id="f36f9-118">Attempting to create and load multiple textures might be no faster than doing one texture at a time, even if this leaves multiple CPU cores idle.</span></span> <span data-ttu-id="f36f9-119">No entanto, a criação de vários sombreadores usando vários threads pode aumentar o desempenho, pois essa operação é menos dependente dos recursos do sistema, como a largura de banda da memória.</span><span class="sxs-lookup"><span data-stu-id="f36f9-119">However, creating multiple shaders using multiple threads can increase performance as this operation is less dependent on system resources such as memory bandwidth.</span></span>

<span data-ttu-id="f36f9-120">Quando o driver e o hardware de gráficos dão suporte a multithreading, normalmente é possível inicializar recursos recém-criados com mais eficiência, passando um ponteiro para dados iniciais no parâmetro *pInitialData* (por exemplo, em uma chamada para o método [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) ).</span><span class="sxs-lookup"><span data-stu-id="f36f9-120">When the driver and graphics hardware support multithreading, you can typically initialize newly created resources more efficiently by passing a pointer to initial data in the *pInitialData* parameter (for example, in a call to the [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) method).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f36f9-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f36f9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f36f9-122">MultiThreading</span><span class="sxs-lookup"><span data-stu-id="f36f9-122">MultiThreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 





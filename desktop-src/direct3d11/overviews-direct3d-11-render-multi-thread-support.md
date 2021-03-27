---
title: Como verificar o suporte ao driver
description: Este tópico mostra como determinar se os recursos de multithreading (incluindo a criação de recursos e as listas de comandos) têm suporte para aceleração de hardware.
ms.assetid: f577357c-c2e5-4e58-9870-2e995bdc6782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae42bbb3eedb76d049479839d497a79db81b5697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988507"
---
# <a name="how-to-check-for-driver-support"></a><span data-ttu-id="9a8bc-103">Como: verificar o suporte de driver</span><span class="sxs-lookup"><span data-stu-id="9a8bc-103">How To: Check for Driver Support</span></span>

<span data-ttu-id="9a8bc-104">Este tópico mostra como determinar se os recursos de multithreading (incluindo a [criação de recursos](overviews-direct3d-11-render-multi-thread-intro.md) e as [listas de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)) têm suporte para aceleração de hardware.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-104">This topic shows how to determine whether multithreading features (including [resource creation](overviews-direct3d-11-render-multi-thread-intro.md) and [command lists](overviews-direct3d-11-render-multi-thread-command-list.md)) are supported for hardware acceleration.</span></span>

<span data-ttu-id="9a8bc-105">Recomendamos que os aplicativos verifiquem o suporte a hardware de gráficos de multithreading.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-105">We recommend for applications to check for graphics hardware support of multithreading.</span></span> <span data-ttu-id="9a8bc-106">Se o driver e o hardware de gráficos não suportarem a criação de objetos multithread, o desempenho poderá ser limitado das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="9a8bc-106">If the driver and graphics hardware do not support multithreaded object creation, performance can be limited in the following ways:</span></span>

-   <span data-ttu-id="9a8bc-107">A criação de vários objetos (mesmo de tipos diferentes) ao mesmo tempo pode ser limitada.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-107">Creating multiple objects (even of different types) at the same time might be limited.</span></span>
-   <span data-ttu-id="9a8bc-108">Criar um objeto ao renderizar comandos gráficos usando um [contexto imediato](overviews-direct3d-11-render-multi-thread-render.md) pode ser limitado.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-108">Creating an object while rendering graphics commands by using an [immediate context](overviews-direct3d-11-render-multi-thread-render.md) might be limited.</span></span> <span data-ttu-id="9a8bc-109">Por exemplo, se o hardware não oferecer suporte a multithreading, um aplicativo deverá evitar a criação em um thread em segundo plano um objeto que requer muito tempo para ser criado.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-109">For example, if hardware does not support multithreading, an application should avoid creating on a background thread an object that requires a very long time to create.</span></span> <span data-ttu-id="9a8bc-110">Uma operação de criação que leva muito tempo pode bloquear a renderização imediata do contexto e aumentar o risco de uma stutter de taxa de quadros Visual.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-110">A create operation that takes very long can block immediate context rendering and increase the risk of a visual frame rate stutter.</span></span>

<span data-ttu-id="9a8bc-111">O tempo de execução dá suporte a vários threads e listas de comandos, independentemente do suporte a driver e hardware; Se não houver suporte de driver e de hardware para vários threads ou listas de comandos, o tempo de execução emulará a funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-111">The runtime supports multithreading and command lists regardless of driver and hardware support; if there is no driver and hardware support for either multithreads or command lists, the runtime will emulate the functionality.</span></span> <span data-ttu-id="9a8bc-112">Para obter mais informações sobre multithreading, consulte [introdução ao multithreading no Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).</span><span class="sxs-lookup"><span data-stu-id="9a8bc-112">For more information about multithreading, see [Introduction to Multithreading in Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).</span></span>

<span data-ttu-id="9a8bc-113">**Para verificar o suporte de driver para multithreading:**</span><span class="sxs-lookup"><span data-stu-id="9a8bc-113">**To check for driver support for multithreading:**</span></span>

1.  <span data-ttu-id="9a8bc-114">Inicializar um objeto de interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="9a8bc-114">Initialize an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface object.</span></span> <span data-ttu-id="9a8bc-115">Por padrão, o multithreading está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-115">By default, multithreading is enabled.</span></span>
2.  <span data-ttu-id="9a8bc-116">Chame [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="9a8bc-116">Call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="9a8bc-117">Passe o valor de **\_ \_ Threading do recurso D3D11** para o parâmetro *Feature* , passe a estrutura de [**Threading de \_ dados do recurso \_ \_ D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) para o parâmetro *pFeatureSupportData* e passe o tamanho da estrutura de **Threading de \_ dados do recurso \_ \_ D3D11** para o parâmetro *FeatureSupportDataSize* .</span><span class="sxs-lookup"><span data-stu-id="9a8bc-117">Pass the **D3D11\_FEATURE\_THREADING** value to the *Feature* parameter, pass the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_THREADING** structure to the *FeatureSupportDataSize* parameter.</span></span>
3.  <span data-ttu-id="9a8bc-118">Se o método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) for bem-sucedido, a estrutura de threading de dados de recursos do D3D11 que você passou na etapa anterior será inicializada com informações sobre o suporte a multithreading. [**\_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading)</span><span class="sxs-lookup"><span data-stu-id="9a8bc-118">If the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) method succeeds, the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure that you passed in the previous step will be initialized with information about multithreading support.</span></span>
    -   <span data-ttu-id="9a8bc-119">Se **DriverConcurrentCreates** for **true**, um driver poderá criar mais de um recurso ao mesmo tempo (simultaneamente) em threads diferentes.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-119">If **DriverConcurrentCreates** is **TRUE**, a driver can create more than one resource at the same time (concurrently) on different threads.</span></span>

        <span data-ttu-id="9a8bc-120">Se **DriverCommandLists** for **true**, o driver dará suporte a listas de comandos.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-120">If **DriverCommandLists** is **TRUE**, the driver supports command lists.</span></span> <span data-ttu-id="9a8bc-121">Ou seja, os comandos de renderização emitidos por um contexto imediato podem ser simultâneos com a criação de objeto em threads separados com baixo risco de um stutter de taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-121">That is, rendering commands issued by an immediate context can be concurrent with object creation on separate threads with low risk of a frame rate stutter.</span></span>

    -   <span data-ttu-id="9a8bc-122">Se **DriverConcurrentCreates** for **false**, um driver não oferecerá suporte à criação simultânea, o que significa que a quantidade de simultaneidade possível é extremamente limitada.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-122">If **DriverConcurrentCreates** is **FALSE**, a driver does not support concurrent creation, which means the amount of concurrency possible is extremely limited.</span></span> <span data-ttu-id="9a8bc-123">O hardware de gráficos não pode criar objetos de tipos diferentes em threads diferentes simultanueously.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-123">The graphics hardware cannot create objects of different types on different threads simultanueously.</span></span> <span data-ttu-id="9a8bc-124">Além disso, o hardware de gráficos não pode usar um contexto imediato para emitir comandos de renderização enquanto o hardware de gráficos tenta criar um recurso em outro thread.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-124">Additionally, the graphics hardware cannot use an immediate context to issue render commands while the graphics hardware attempts to create a resource on another thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a8bc-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a8bc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a8bc-126">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="9a8bc-126">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="9a8bc-127">Multithread</span><span class="sxs-lookup"><span data-stu-id="9a8bc-127">Multithreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 





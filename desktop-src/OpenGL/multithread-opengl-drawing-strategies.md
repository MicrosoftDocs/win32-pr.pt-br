---
title: Estratégias de desenho multithread OpenGL
description: O GDI não dá suporte a vários threads.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL no Windows, desenho multithread
- multithread OpenGL Drawing OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bccb08d48bd8ccb62584f15911a1eb65080c4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292065"
---
# <a name="multithread-opengl-drawing-strategies"></a><span data-ttu-id="abbbb-105">Estratégias de desenho multithread OpenGL</span><span class="sxs-lookup"><span data-stu-id="abbbb-105">Multithread OpenGL Drawing Strategies</span></span>

<span data-ttu-id="abbbb-106">O GDI não dá suporte a vários threads.</span><span class="sxs-lookup"><span data-stu-id="abbbb-106">The GDI does not support multiple threads.</span></span> <span data-ttu-id="abbbb-107">Você deve usar um contexto de dispositivo distinto e um contexto de renderização distinto para cada thread.</span><span class="sxs-lookup"><span data-stu-id="abbbb-107">You must use a distinct device context and a distinct rendering context for each thread.</span></span> <span data-ttu-id="abbbb-108">Isso tende a limitar as vantagens de desempenho do uso de vários threads com sistemas de processador único executando aplicativos OpenGL.</span><span class="sxs-lookup"><span data-stu-id="abbbb-108">This tends to limit the performance advantages of using multiple threads with single-processor systems running OpenGL applications.</span></span> <span data-ttu-id="abbbb-109">No entanto, há maneiras de usar threads com um sistema de processador único para aumentar significativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="abbbb-109">However, there are ways to use threads with a single processor system to greatly increase performance.</span></span> <span data-ttu-id="abbbb-110">Por exemplo, você pode usar um thread separado para passar chamadas de renderização OpenGL para hardware 3D dedicado.</span><span class="sxs-lookup"><span data-stu-id="abbbb-110">For example, you can use a separate thread to pass OpenGL rendering calls to dedicated 3-D hardware.</span></span>

<span data-ttu-id="abbbb-111">Os sistemas SMP (multiprocessamento simétrico) podem se beneficiar muito do uso de vários threads.</span><span class="sxs-lookup"><span data-stu-id="abbbb-111">Symmetric multiprocessing (SMP) systems can greatly benefit from using multiple threads.</span></span> <span data-ttu-id="abbbb-112">Uma estratégia óbvia é usar um thread separado para cada processador para lidar com a renderização de OpenGL em janelas separadas.</span><span class="sxs-lookup"><span data-stu-id="abbbb-112">An obvious strategy is to use a separate thread for each processor to handle OpenGL rendering in separate windows.</span></span> <span data-ttu-id="abbbb-113">Por exemplo, em um aplicativo de simulação de voo, você poderia usar processadores e threads separados para renderizar os modos de exibição frontal, voltar e lateral.</span><span class="sxs-lookup"><span data-stu-id="abbbb-113">For example, in a flight-simulation application you could use separate processors and threads to render the front, back, and side views.</span></span>

<span data-ttu-id="abbbb-114">Um thread pode ter apenas um contexto de renderização ativo atual.</span><span class="sxs-lookup"><span data-stu-id="abbbb-114">A thread can have only one current, active rendering context.</span></span> <span data-ttu-id="abbbb-115">Ao usar vários threads e vários contextos de renderização, você deve ter cuidado para sincronizar seu uso.</span><span class="sxs-lookup"><span data-stu-id="abbbb-115">When you use multiple threads and multiple rendering contexts, you must be careful to synchronize their use.</span></span> <span data-ttu-id="abbbb-116">Por exemplo, use um thread somente para chamar [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) depois que todos os threads terminarem de desenhar.</span><span class="sxs-lookup"><span data-stu-id="abbbb-116">For example, use one thread only to call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) after all threads finish drawing.</span></span>

 

 





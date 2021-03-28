---
title: MultiThreading
description: O Direct3D 11 implementa o suporte para a criação e renderização de objetos usando vários threads.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160132"
---
# <a name="multithreading"></a><span data-ttu-id="0db0c-103">MultiThreading</span><span class="sxs-lookup"><span data-stu-id="0db0c-103">MultiThreading</span></span>

<span data-ttu-id="0db0c-104">O Direct3D 11 implementa o suporte para a criação e renderização de objetos usando vários threads.</span><span class="sxs-lookup"><span data-stu-id="0db0c-104">Direct3D 11 implements support for object creation and rendering using multiple threads.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0db0c-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0db0c-105">In this section</span></span>



| <span data-ttu-id="0db0c-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="0db0c-106">Topic</span></span>                                                                                                                   | <span data-ttu-id="0db0c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0db0c-107">Description</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0db0c-108">Introdução a multithreading no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="0db0c-108">Introduction to Multithreading in Direct3D 11</span></span>](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | <span data-ttu-id="0db0c-109">O multithreading foi projetado para melhorar o desempenho executando o trabalho usando um ou mais threads ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="0db0c-109">Multithreading is designed to improve performance by performing work using one or more threads at the same time.</span></span> <br/>                                                                                                         |
| [<span data-ttu-id="0db0c-110">Criação de objeto com multithreading</span><span class="sxs-lookup"><span data-stu-id="0db0c-110">Object Creation with Multithreading</span></span>](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | <span data-ttu-id="0db0c-111">Use a interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para criar recursos e objetos, use o [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) para [renderização](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="0db0c-111">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span><br/> |
| [<span data-ttu-id="0db0c-112">Renderização imediata e adiada</span><span class="sxs-lookup"><span data-stu-id="0db0c-112">Immediate and Deferred Rendering</span></span>](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | <span data-ttu-id="0db0c-113">O Direct3D 11 dá suporte a dois tipos de renderização: Immediate e adiada.</span><span class="sxs-lookup"><span data-stu-id="0db0c-113">Direct3D 11 supports two types of rendering: immediate and deferred.</span></span> <span data-ttu-id="0db0c-114">Ambos são implementados usando a interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="0db0c-114">Both are implemented by using the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span><br/>                                                      |
| [<span data-ttu-id="0db0c-115">Lista de comandos</span><span class="sxs-lookup"><span data-stu-id="0db0c-115">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | <span data-ttu-id="0db0c-116">Uma lista de comandos é uma sequência de comandos de GPU que podem ser gravados e reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="0db0c-116">A command list is a sequence of GPU commands that can be recorded and played back.</span></span> <span data-ttu-id="0db0c-117">Uma lista de comandos pode melhorar o desempenho, reduzindo a quantidade de sobrecarga gerada pelo tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0db0c-117">A command list may improve performance by reducing the amount of overhead generated by the runtime.</span></span><br/>                                    |
| [<span data-ttu-id="0db0c-118">Diferenças de Threading entre versões do Direct3D</span><span class="sxs-lookup"><span data-stu-id="0db0c-118">Threading Differences between Direct3D Versions</span></span>](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | <span data-ttu-id="0db0c-119">Muitos modelos de programação multi-threaded usam primitivos de sincronização (como mutexes) para criar seções críticas e impedir que o código seja acessado por mais de um thread por vez.</span><span class="sxs-lookup"><span data-stu-id="0db0c-119">Many multi-threaded programming models make use of synchronization primitives (such as mutexes) to create critical sections and prevent code from being accessed by more than one thread at a time.</span></span><br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="0db0c-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0db0c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0db0c-121">Como: verificar o suporte de driver</span><span class="sxs-lookup"><span data-stu-id="0db0c-121">How To: Check for Driver Support</span></span>](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[<span data-ttu-id="0db0c-122">Renderização</span><span class="sxs-lookup"><span data-stu-id="0db0c-122">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 






---
title: Módulo 3. Gráficos do Windows
description: O módulo 1 desta série mostrou como criar uma janela em branco.
ms.assetid: 02416d36-519e-49bd-8a52-bd3afde2be34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbe0e7afe882180a056f4c77d72de16df0ef943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005120"
---
# <a name="module-3-windows-graphics"></a><span data-ttu-id="67e26-104">Módulo 3.</span><span class="sxs-lookup"><span data-stu-id="67e26-104">Module 3.</span></span> <span data-ttu-id="67e26-105">Gráficos do Windows</span><span class="sxs-lookup"><span data-stu-id="67e26-105">Windows Graphics</span></span>

<span data-ttu-id="67e26-106">O [módulo 1](your-first-windows-program.md) desta série mostrou como criar uma janela em branco.</span><span class="sxs-lookup"><span data-stu-id="67e26-106">[Module 1](your-first-windows-program.md) of this series showed how to create a blank window.</span></span> <span data-ttu-id="67e26-107">O [módulo 2](module-2--using-com-in-your-windows-program.md) tirou um ligeiro desvio por meio de Component Object Model (com), que é a base para muitas das APIs modernas do Windows.</span><span class="sxs-lookup"><span data-stu-id="67e26-107">[Module 2](module-2--using-com-in-your-windows-program.md) took a slight detour through the Component Object Model (COM), which is the foundation for many of the modern Windows APIs.</span></span> <span data-ttu-id="67e26-108">Agora é hora de adicionar gráficos à janela em branco que criamos no módulo 1.</span><span class="sxs-lookup"><span data-stu-id="67e26-108">Now it is time to add graphics to the blank window that we created in Module 1.</span></span>

<span data-ttu-id="67e26-109">Este módulo começa com uma visão geral de alto nível da arquitetura de gráficos do Windows.</span><span class="sxs-lookup"><span data-stu-id="67e26-109">This module starts with a high-level overview of the Windows graphics architecture.</span></span> <span data-ttu-id="67e26-110">Em seguida, examinamos o Direct2D, uma poderosa API de gráficos que foi introduzida no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="67e26-110">We then look at Direct2D, a powerful graphics API that was introduced in Windows 7.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="67e26-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="67e26-111">In this section</span></span>

-   [<span data-ttu-id="67e26-112">Visão geral da arquitetura de gráficos do Windows</span><span class="sxs-lookup"><span data-stu-id="67e26-112">Overview of the Windows Graphics Architecture</span></span>](overview-of-the-windows-graphics-architecture.md)
-   [<span data-ttu-id="67e26-113">O Gerenciador de Janelas da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="67e26-113">The Desktop Window Manager</span></span>](the-desktop-window-manager.md)
-   [<span data-ttu-id="67e26-114">Modo retido versus modo imediato</span><span class="sxs-lookup"><span data-stu-id="67e26-114">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)
-   [<span data-ttu-id="67e26-115">Seu primeiro programa Direct2D</span><span class="sxs-lookup"><span data-stu-id="67e26-115">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)
-   [<span data-ttu-id="67e26-116">Renderizar Alvos, Dispositivos e Recursos</span><span class="sxs-lookup"><span data-stu-id="67e26-116">Render Targets, Devices, and Resources</span></span>](render-targets--devices--and-resources.md)
-   [<span data-ttu-id="67e26-117">Desenhar com Direct2D</span><span class="sxs-lookup"><span data-stu-id="67e26-117">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)
-   [<span data-ttu-id="67e26-118">DPI e Device-Independent pixels</span><span class="sxs-lookup"><span data-stu-id="67e26-118">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)
-   [<span data-ttu-id="67e26-119">Usando a cor em Direct2D</span><span class="sxs-lookup"><span data-stu-id="67e26-119">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)
-   [<span data-ttu-id="67e26-120">Aplicar transformações em Direct2D</span><span class="sxs-lookup"><span data-stu-id="67e26-120">Applying Transforms in Direct2D</span></span>](applying-transforms-in-direct2d.md)
-   [<span data-ttu-id="67e26-121">Apêndice: transformações de matriz</span><span class="sxs-lookup"><span data-stu-id="67e26-121">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)

## <a name="related-topics"></a><span data-ttu-id="67e26-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67e26-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67e26-123">Aprenda a programar para Windows em C++</span><span class="sxs-lookup"><span data-stu-id="67e26-123">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 





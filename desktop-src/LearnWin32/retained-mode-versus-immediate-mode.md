---
title: Modo retido versus modo imediato
description: As APIs de gráficos podem ser divididas em APIs de modo retido e em APIs de modo imediato.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559798"
---
# <a name="retained-mode-versus-immediate-mode"></a><span data-ttu-id="ad18e-103">Modo retido versus modo imediato</span><span class="sxs-lookup"><span data-stu-id="ad18e-103">Retained Mode Versus Immediate Mode</span></span>

<span data-ttu-id="ad18e-104">As APIs de gráficos podem ser divididas em APIs de *modo retido* e em APIs *de modo imediato* .</span><span class="sxs-lookup"><span data-stu-id="ad18e-104">Graphics APIs can be divided into *retained-mode* APIs and *immediate-mode* APIs.</span></span> <span data-ttu-id="ad18e-105">Direct2D é uma API de modo imediato.</span><span class="sxs-lookup"><span data-stu-id="ad18e-105">Direct2D is an immediate-mode API.</span></span> <span data-ttu-id="ad18e-106">Windows Presentation Foundation (WPF) é um exemplo de uma API de modo retido.</span><span class="sxs-lookup"><span data-stu-id="ad18e-106">Windows Presentation Foundation (WPF) is an example of a retained-mode API.</span></span>

<span data-ttu-id="ad18e-107">Uma API de modo retido é declarativa.</span><span class="sxs-lookup"><span data-stu-id="ad18e-107">A retained-mode API is declarative.</span></span> <span data-ttu-id="ad18e-108">O aplicativo constrói uma cena a partir de primitivos gráficos, como formas e linhas.</span><span class="sxs-lookup"><span data-stu-id="ad18e-108">The application constructs a scene from graphics primitives, such as shapes and lines.</span></span> <span data-ttu-id="ad18e-109">A biblioteca de gráficos armazena um modelo da cena na memória.</span><span class="sxs-lookup"><span data-stu-id="ad18e-109">The graphics library stores a model of the scene in memory.</span></span> <span data-ttu-id="ad18e-110">Para desenhar um quadro, a biblioteca de gráficos transforma a cena em um conjunto de comandos de desenho.</span><span class="sxs-lookup"><span data-stu-id="ad18e-110">To draw a frame, the graphics library transforms the scene into a set of drawing commands.</span></span> <span data-ttu-id="ad18e-111">Entre os quadros, a biblioteca de gráficos mantém a cena na memória.</span><span class="sxs-lookup"><span data-stu-id="ad18e-111">Between frames, the graphics library keeps the scene in memory.</span></span> <span data-ttu-id="ad18e-112">Para alterar o que é renderizado, o aplicativo emite um comando para atualizar a cena, por exemplo, para adicionar ou remover uma forma.</span><span class="sxs-lookup"><span data-stu-id="ad18e-112">To change what is rendered, the application issues a command to update the scene—for example, to add or remove a shape.</span></span> <span data-ttu-id="ad18e-113">Em seguida, a biblioteca é responsável por redesenhar a cena.</span><span class="sxs-lookup"><span data-stu-id="ad18e-113">The library is then responsible for redrawing the scene.</span></span>

![um diagrama que mostra gráficos de modo retido.](images/graphics06.png)

<span data-ttu-id="ad18e-115">Uma API de modo imediato é o procedimento.</span><span class="sxs-lookup"><span data-stu-id="ad18e-115">An immediate-mode API is procedural.</span></span> <span data-ttu-id="ad18e-116">Cada vez que um novo quadro é desenhado, o aplicativo emite diretamente os comandos de desenho.</span><span class="sxs-lookup"><span data-stu-id="ad18e-116">Each time a new frame is drawn, the application directly issues the drawing commands.</span></span> <span data-ttu-id="ad18e-117">A biblioteca de gráficos não armazena um modelo de cena entre os quadros.</span><span class="sxs-lookup"><span data-stu-id="ad18e-117">The graphics library does not store a scene model between frames.</span></span> <span data-ttu-id="ad18e-118">Em vez disso, o aplicativo controla a cena.</span><span class="sxs-lookup"><span data-stu-id="ad18e-118">Instead, the application keeps track of the scene.</span></span>

![um diagrama que mostra gráficos de modo imediato.](images/graphics07.png)

<span data-ttu-id="ad18e-120">APIs de modo retido podem ser mais simples de usar, porque a API faz mais do que o trabalho para você, como inicialização, manutenção de estado e limpeza.</span><span class="sxs-lookup"><span data-stu-id="ad18e-120">Retained-mode APIs can be simpler to use, because the API does more of the work for you, such as initialization, state maintenance, and cleanup.</span></span> <span data-ttu-id="ad18e-121">Por outro lado, geralmente eles são menos flexíveis, porque a API impõe seu próprio modelo de cena.</span><span class="sxs-lookup"><span data-stu-id="ad18e-121">On the other hand, they are often less flexible, because the API imposes its own scene model.</span></span> <span data-ttu-id="ad18e-122">Além disso, uma API de modo retido pode ter mais requisitos de memória, pois precisa fornecer um modelo de cena de uso geral.</span><span class="sxs-lookup"><span data-stu-id="ad18e-122">Also, a retained-mode API can have higher memory requirements, because it needs to provide a general-purpose scene model.</span></span> <span data-ttu-id="ad18e-123">Com uma API de modo imediato, você pode implementar otimizações direcionadas.</span><span class="sxs-lookup"><span data-stu-id="ad18e-123">With an immediate-mode API, you can implement targeted optimizations.</span></span>

## <a name="next"></a><span data-ttu-id="ad18e-124">Avançar</span><span class="sxs-lookup"><span data-stu-id="ad18e-124">Next</span></span>

[<span data-ttu-id="ad18e-125">Seu primeiro programa Direct2D</span><span class="sxs-lookup"><span data-stu-id="ad18e-125">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)

 

 





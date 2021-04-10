---
title: Exemplos de animação do Windows
description: Os tópicos contidos nesta seção fornecem detalhes sobre os exemplos de código que dão suporte à documentação do Gerenciador de animação do Windows.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Animação do Windows animações do Windows, exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292600"
---
# <a name="windows-animation-samples"></a><span data-ttu-id="6b860-104">Exemplos de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="6b860-104">Windows Animation Samples</span></span>

<span data-ttu-id="6b860-105">Os tópicos contidos nesta seção fornecem detalhes sobre os exemplos de código que dão suporte à documentação do Gerenciador de animação do Windows.</span><span class="sxs-lookup"><span data-stu-id="6b860-105">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6b860-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6b860-106">In this section</span></span>



| <span data-ttu-id="6b860-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="6b860-107">Topic</span></span>                                                                                     | <span data-ttu-id="6b860-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b860-108">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b860-109">Exemplo de animação orientada por aplicativo</span><span class="sxs-lookup"><span data-stu-id="6b860-109">Application-Driven Animation Sample</span></span>](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [<span data-ttu-id="6b860-110">Exemplo de animação orientada por temporizador</span><span class="sxs-lookup"><span data-stu-id="6b860-110">Timer-Driven Animation Sample</span></span>](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [<span data-ttu-id="6b860-111">Exemplo de interpolador personalizado</span><span class="sxs-lookup"><span data-stu-id="6b860-111">Custom Interpolator Sample</span></span>](custom-interpolator-sample.md)<br/>                   | <span data-ttu-id="6b860-112">Mostra como usar a animação do Windows com seu próprio interpolador personalizado, com Direct2D usado para renderização.</span><span class="sxs-lookup"><span data-stu-id="6b860-112">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <br/> |
| [<span data-ttu-id="6b860-113">Exemplo de layout de grade</span><span class="sxs-lookup"><span data-stu-id="6b860-113">Grid Layout Sample</span></span>](grid-layout-sample.md)<br/>                                   | <span data-ttu-id="6b860-114">Mostra como usar a animação do Windows, usando Direct2D para animar uma grade de imagens.</span><span class="sxs-lookup"><span data-stu-id="6b860-114">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span> <br/>                         |
| [<span data-ttu-id="6b860-115">Exemplo de comparação de prioridade</span><span class="sxs-lookup"><span data-stu-id="6b860-115">Priority Comparison Sample</span></span>](priority-comparison-sample.md)<br/>                   | <span data-ttu-id="6b860-116">Mostra como usar a animação do Windows com sua própria comparação de prioridade, usando Direct2D para renderização.</span><span class="sxs-lookup"><span data-stu-id="6b860-116">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span><br/>      |



 

## <a name="sample-files"></a><span data-ttu-id="6b860-117">Arquivos de exemplo</span><span class="sxs-lookup"><span data-stu-id="6b860-117">Sample Files</span></span>

<span data-ttu-id="6b860-118">Cada exemplo contém muitos dos seguintes arquivos de chave:</span><span class="sxs-lookup"><span data-stu-id="6b860-118">Each sample contains many of the following key files:</span></span>

<dl> <dt>

<span data-ttu-id="6b860-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp</span><span class="sxs-lookup"><span data-stu-id="6b860-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application.cpp</span></span>
</dt> <dd>

<span data-ttu-id="6b860-120">Define o ponto de entrada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6b860-120">Defines the application entry point.</span></span>

</dd> <dt>

<span data-ttu-id="6b860-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h</span><span class="sxs-lookup"><span data-stu-id="6b860-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow.h</span></span>
</dt> <dd>

<span data-ttu-id="6b860-122">Declara a classe CMainWindow.</span><span class="sxs-lookup"><span data-stu-id="6b860-122">Declares the CMainWindow class.</span></span>

</dd> <dt>

<span data-ttu-id="6b860-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp</span><span class="sxs-lookup"><span data-stu-id="6b860-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow.cpp</span></span>
</dt> <dd>

<span data-ttu-id="6b860-124">Inicializa os componentes de animação e a plataforma de gráficos, carrega imagens e renderiza a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="6b860-124">Initializes the animation components and the graphics platform, loads images, and renders the client area.</span></span>

</dd> <dt>

<span data-ttu-id="6b860-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager. h</span><span class="sxs-lookup"><span data-stu-id="6b860-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager.h</span></span>
</dt> <dd>

<span data-ttu-id="6b860-126">Declara a classe CLayoutManager.</span><span class="sxs-lookup"><span data-stu-id="6b860-126">Declares the CLayoutManager class.</span></span>

</dd> <dt>

<span data-ttu-id="6b860-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager. cpp</span><span class="sxs-lookup"><span data-stu-id="6b860-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager.cpp</span></span>
</dt> <dd>

<span data-ttu-id="6b860-128">Calcula o layout das imagens na janela principal, cria storyboards, adiciona transições ao storyboard e agenda o storyboard.</span><span class="sxs-lookup"><span data-stu-id="6b860-128">Calculates the layout of images in the main window, creates storyboards, adds transitions to the storyboard, and schedules the storyboard.</span></span>

</dd> <dt>

<span data-ttu-id="6b860-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Miniatura. h</span><span class="sxs-lookup"><span data-stu-id="6b860-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail.h</span></span>
</dt> <dd>

<span data-ttu-id="6b860-130">Declara a classe CThumbNail.</span><span class="sxs-lookup"><span data-stu-id="6b860-130">Declares the CThumbNail class.</span></span>

</dd> <dt>

<span data-ttu-id="6b860-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail. cpp</span><span class="sxs-lookup"><span data-stu-id="6b860-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail.cpp</span></span>
</dt> <dd>

<span data-ttu-id="6b860-132">Cria variáveis de animação e renderiza miniaturas.</span><span class="sxs-lookup"><span data-stu-id="6b860-132">Creates animation variables and renders thumbnails.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6b860-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b860-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b860-134">Guia de desenvolvimento de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="6b860-134">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)
</dt> <dt>

[<span data-ttu-id="6b860-135">Referência de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="6b860-135">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

 






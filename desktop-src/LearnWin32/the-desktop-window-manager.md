---
title: O Gerenciador de Janelas da Área de Trabalho
description: .
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73167b762a9952eb508f09e70f3d4183b3b7a018
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292137"
---
# <a name="the-desktop-window-manager"></a><span data-ttu-id="d6967-103">O Gerenciador de Janelas da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="d6967-103">The Desktop Window Manager</span></span>

<span data-ttu-id="d6967-104">Antes do Windows Vista, um programa do Windows desenharia diretamente na tela.</span><span class="sxs-lookup"><span data-stu-id="d6967-104">Before Windows Vista, a Windows program would draw directly to the screen.</span></span> <span data-ttu-id="d6967-105">Em outras palavras, o programa gravaria diretamente no buffer de memória mostrado pela placa de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d6967-105">In other words, the program would write directly to the memory buffer shown by the video card.</span></span> <span data-ttu-id="d6967-106">Essa abordagem pode causar artefatos visuais se uma janela não redesenhar corretamente.</span><span class="sxs-lookup"><span data-stu-id="d6967-106">This approach can cause visual artifacts if a window does not repaint itself correctly.</span></span> <span data-ttu-id="d6967-107">Por exemplo, se o usuário arrastar uma janela sobre outra janela e a janela abaixo não for redesenhada com rapidez suficiente, a janela superior poderá sair de uma trilha:</span><span class="sxs-lookup"><span data-stu-id="d6967-107">For example, if the user drags one window over another window, and the window underneath does not repaint itself quickly enough, the top-most window can leave a trail:</span></span>

![uma captura de tela que mostra os artefatos redesenhados.](images/graphics04.png)

<span data-ttu-id="d6967-109">A trilha é causada porque o Windows Paint para a mesma área de memória.</span><span class="sxs-lookup"><span data-stu-id="d6967-109">The trail is caused because both windows paint to the same area of memory.</span></span> <span data-ttu-id="d6967-110">Como a janela superior é arrastada, a janela abaixo dela deve ser redesenhada.</span><span class="sxs-lookup"><span data-stu-id="d6967-110">As the top-most window is dragged, the window below it must be repainted.</span></span> <span data-ttu-id="d6967-111">Se a repintura for muito lenta, ela causará os artefatos mostrados na imagem anterior.</span><span class="sxs-lookup"><span data-stu-id="d6967-111">If the repainting is too slow, it causes the artifacts shown in the previous image.</span></span>

<span data-ttu-id="d6967-112">O Windows Vista mudou fundamentalmente a forma como o Windows é desenhado, introduzindo o Gerenciador de Janelas da Área de Trabalho (DWM).</span><span class="sxs-lookup"><span data-stu-id="d6967-112">Windows Vista fundamentally changed how windows are drawn, by introducing the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="d6967-113">Quando o DWM está habilitado, uma janela não é mais redesenhada diretamente para o buffer de exibição.</span><span class="sxs-lookup"><span data-stu-id="d6967-113">When the DWM is enabled, a window no longer draws directly to the display buffer.</span></span> <span data-ttu-id="d6967-114">Em vez disso, cada janela desenha um buffer de memória fora da tela, também chamado de *superfície fora da tela*.</span><span class="sxs-lookup"><span data-stu-id="d6967-114">Instead, each window draws to an offscreen memory buffer, also called an *offscreen surface*.</span></span> <span data-ttu-id="d6967-115">Em seguida, o DWM compõe essas superfícies na tela.</span><span class="sxs-lookup"><span data-stu-id="d6967-115">The DWM then composites these surfaces to the screen.</span></span>

![um diagrama que mostra como o DWM compõe a área de trabalho.](images/graphics05.png)

<span data-ttu-id="d6967-117">O DWM fornece várias vantagens em relação à arquitetura gráfica antiga.</span><span class="sxs-lookup"><span data-stu-id="d6967-117">The DWM provides several advantages over the old graphics architecture.</span></span>

-   <span data-ttu-id="d6967-118">Menos mensagens redesenhadas.</span><span class="sxs-lookup"><span data-stu-id="d6967-118">Fewer repaint messages.</span></span> <span data-ttu-id="d6967-119">Quando uma janela está obstruída por outra janela, a janela obstruída não precisa redesenhar a si mesma.</span><span class="sxs-lookup"><span data-stu-id="d6967-119">When a window is obstructed by another window, the obstructed window does not need to repaint itself.</span></span>
-   <span data-ttu-id="d6967-120">Artefatos reduzidos.</span><span class="sxs-lookup"><span data-stu-id="d6967-120">Reduced artifacts.</span></span> <span data-ttu-id="d6967-121">Anteriormente, arrastar uma janela poderia criar artefatos visuais, conforme descrito.</span><span class="sxs-lookup"><span data-stu-id="d6967-121">Previously, dragging a window could create visual artifacts, as described.</span></span>
-   <span data-ttu-id="d6967-122">Efeitos visuais.</span><span class="sxs-lookup"><span data-stu-id="d6967-122">Visual effects.</span></span> <span data-ttu-id="d6967-123">Como o DWM é responsável por compor a tela, ele pode renderizar áreas translúcidas e borradas da janela.</span><span class="sxs-lookup"><span data-stu-id="d6967-123">Because the DWM is in charge of compositing the screen, it can render translucent and blurred areas of the window.</span></span>
-   <span data-ttu-id="d6967-124">Dimensionamento automático para DPI alto.</span><span class="sxs-lookup"><span data-stu-id="d6967-124">Automatic scaling for high DPI.</span></span> <span data-ttu-id="d6967-125">Embora o dimensionamento não seja a maneira ideal de lidar com o DPI alto, ele é um fallback viável para aplicativos mais antigos que não foram projetados para configurações de DPI alto.</span><span class="sxs-lookup"><span data-stu-id="d6967-125">Although scaling is not the ideal way to handle high DPI, it is a viable fallback for older applications that were not designed for high DPI settings.</span></span> <span data-ttu-id="d6967-126">(Voltaremos a este tópico mais tarde, na seção [dpi e Device-Independent pixels](dpi-and-device-independent-pixels.md).)</span><span class="sxs-lookup"><span data-stu-id="d6967-126">(We will return to this topic later, in the section [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).)</span></span>
-   <span data-ttu-id="d6967-127">Modos de exibição alternativos.</span><span class="sxs-lookup"><span data-stu-id="d6967-127">Alternative views.</span></span> <span data-ttu-id="d6967-128">O DWM pode usar as superfícies fora da tela de várias maneiras interessantes.</span><span class="sxs-lookup"><span data-stu-id="d6967-128">The DWM can use the offscreen surfaces in various interesting ways.</span></span> <span data-ttu-id="d6967-129">Por exemplo, o DWM é a tecnologia por trás do Windows Flip 3D, miniaturas e transições animadas.</span><span class="sxs-lookup"><span data-stu-id="d6967-129">For example, the DWM is the technology behind Windows Flip 3D, thumbnails, and animated transitions.</span></span>

<span data-ttu-id="d6967-130">No entanto, observe que não há garantia de que o DWM esteja habilitado.</span><span class="sxs-lookup"><span data-stu-id="d6967-130">Note, however, that the DWM is not guaranteed to be enabled.</span></span> <span data-ttu-id="d6967-131">A placa gráfica pode não dar suporte aos requisitos de sistema do DWM e os usuários podem desabilitar o DWM por meio do painel de controle **Propriedades do sistema** .</span><span class="sxs-lookup"><span data-stu-id="d6967-131">The graphics card might not support the DWM system requirements, and users can disable the DWM through the **System Properties** control panel.</span></span> <span data-ttu-id="d6967-132">Isso significa que seu programa não deve depender do comportamento de repintura do DWM.</span><span class="sxs-lookup"><span data-stu-id="d6967-132">That means your program should not rely on the repainting behavior of the DWM.</span></span> <span data-ttu-id="d6967-133">Teste seu programa com o DWM desabilitado para certificar-se de que ele repinta corretamente.</span><span class="sxs-lookup"><span data-stu-id="d6967-133">Test your program with DWM disabled to make sure that it repaints correctly.</span></span>

## <a name="next"></a><span data-ttu-id="d6967-134">Avançar</span><span class="sxs-lookup"><span data-stu-id="d6967-134">Next</span></span>

[<span data-ttu-id="d6967-135">Modo retido versus modo imediato</span><span class="sxs-lookup"><span data-stu-id="d6967-135">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)

 

 





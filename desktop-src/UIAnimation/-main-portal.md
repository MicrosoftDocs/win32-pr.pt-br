---
title: Gerenciador de animação do Windows
description: O Gerenciador de animação do Windows (animação do Windows) permite uma rica animação de elementos da interface do usuário.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Animação das janelas de animação do Windows, portal
- Animação do Windows do Gerenciador de animação do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917426"
---
# <a name="windows-animation-manager"></a><span data-ttu-id="9af45-105">Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="9af45-105">Windows Animation Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="9af45-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="9af45-106">Purpose</span></span>

<span data-ttu-id="9af45-107">O Gerenciador de animação do Windows (animação do Windows) permite uma rica animação de elementos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9af45-107">The Windows Animation Manager (Windows Animation) enables rich animation of user interface elements.</span></span> <span data-ttu-id="9af45-108">Ele foi projetado para simplificar o processo de adição de animação à interface do usuário de um aplicativo e para permitir que os desenvolvedores implementem animações que são suaves, naturais e interativas.</span><span class="sxs-lookup"><span data-stu-id="9af45-108">It is designed to simplify the process of adding animation to an application's user interface and to enable developers to implement animations that are smooth, natural, and interactive.</span></span>

<span data-ttu-id="9af45-109">A estrutura de animação gerencia o agendamento e a execução de animações.</span><span class="sxs-lookup"><span data-stu-id="9af45-109">The animation framework manages the scheduling and execution of animations.</span></span> <span data-ttu-id="9af45-110">Ele fornece uma biblioteca de funções matemáticas úteis para especificar o comportamento de um elemento de interface do usuário ao longo do tempo e também permite que os desenvolvedores implementem funções personalizadas que fornecem comportamentos adicionais.</span><span class="sxs-lookup"><span data-stu-id="9af45-110">It supplies a library of useful mathematical functions for specifying the behavior of a UI element over time, and also enables developers to implement custom functions that provide additional behaviors.</span></span>

<span data-ttu-id="9af45-111">A animação do Windows não executa a renderização; Ele pode ser usado com qualquer plataforma gráfica, incluindo Direct2D, Direct3D ou GDI+.</span><span class="sxs-lookup"><span data-stu-id="9af45-111">Windows Animation does not perform the rendering; it can be used with any graphics platform, including Direct2D, Direct3D, or GDI+.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9af45-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9af45-112">In this section</span></span>



| <span data-ttu-id="9af45-113">Tópico</span><span class="sxs-lookup"><span data-stu-id="9af45-113">Topic</span></span>                                                                                   | <span data-ttu-id="9af45-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9af45-114">Description</span></span>                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9af45-115">Guia de desenvolvimento de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="9af45-115">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)<br/> | <span data-ttu-id="9af45-116">O guia do desenvolvedor fornece uma visão geral da animação do Windows e fornece um código de exemplo que aborda as tarefas básicas de animação.</span><span class="sxs-lookup"><span data-stu-id="9af45-116">The developer guide provides an overview of Windows Animation and provides sample code that covers the basic animation tasks.</span></span><br/>          |
| [<span data-ttu-id="9af45-117">Referência de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="9af45-117">Windows Animation Reference</span></span>](windows-animation-reference.md)<br/>               | <span data-ttu-id="9af45-118">Os tópicos contidos nesta seção fornecem as especificações de referência para o Gerenciador de animação do Windows.</span><span class="sxs-lookup"><span data-stu-id="9af45-118">The topics contained in this section provide the reference specifications for the Windows Animation Manager.</span></span><br/>                           |
| [<span data-ttu-id="9af45-119">Exemplos de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="9af45-119">Windows Animation Samples</span></span>](windows-animation-samples.md)<br/>                   | <span data-ttu-id="9af45-120">Os tópicos contidos nesta seção fornecem detalhes sobre os exemplos de código que dão suporte à documentação do Gerenciador de animação do Windows.</span><span class="sxs-lookup"><span data-stu-id="9af45-120">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span> <br/> |
| [<span data-ttu-id="9af45-121">Glossário de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="9af45-121">Windows Animation Glossary</span></span>](-ui-animation-glossary.md)<br/>                     | <span data-ttu-id="9af45-122">Este glossário contém termos e acrônimos de interesse para os desenvolvedores que usam o Gerenciador de animação do Windows.</span><span class="sxs-lookup"><span data-stu-id="9af45-122">This glossary contains terms and acronyms of interest to developers using the Windows Animation Manager.</span></span><br/>                               |



 

## <a name="developer-audience"></a><span data-ttu-id="9af45-123">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="9af45-123">Developer audience</span></span>

<span data-ttu-id="9af45-124">A animação do Windows foi projetada para ser usada por desenvolvedores experientes de C/C++ que estão familiarizados com o COM, conceitos de programação de interface do usuário e conceitos gerais de animação.</span><span class="sxs-lookup"><span data-stu-id="9af45-124">Windows Animation is designed for use by experienced C/C++ developers who are familiar with COM, UI programming concepts, and general animation concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9af45-125">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="9af45-125">Run-time requirements</span></span>

<span data-ttu-id="9af45-126">O Gerenciador de animação do Windows foi introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9af45-126">The Windows Animation Manager was introduced in Windows 7.</span></span>

<span data-ttu-id="9af45-127">Os aplicativos que exigem suporte para o Windows Animation Manager no Windows Vista podem utilizar a atualização de plataforma para o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9af45-127">Applications that require support for Windows Animation Manager on Windows Vista can utilize the Platform Update for Windows Vista.</span></span> <span data-ttu-id="9af45-128">Os aplicativos que exigem a atualização da plataforma para o Windows Vista podem ter Windows Update verificar se estão instalados ou baixá-los e instalá-los em segundo plano caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9af45-128">Applications that require Platform Update for Windows Vista can have Windows Update verify that it is installed, or download and install it in the background otherwise.</span></span> <span data-ttu-id="9af45-129">Para obter mais informações, consulte [sobre a atualização de plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9af45-129">For more information, see [About Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9af45-130">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="9af45-130">Additional resources</span></span>

-   <span data-ttu-id="9af45-131">[Visão geral da animação de cenários do Windows](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (vídeo)</span><span class="sxs-lookup"><span data-stu-id="9af45-131">[Windows Scenic Animation Overview](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (video)</span></span>
-   <span data-ttu-id="9af45-132">[Dentro do Windows 7: aprofundamento e tutorial do Gerenciador de animação](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (vídeo)</span><span class="sxs-lookup"><span data-stu-id="9af45-132">[Inside Windows 7: Animation Manager Deep Dive and Tutorial](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (video)</span></span>
-   <span data-ttu-id="9af45-133">[Animação do Windows-tópicos avançados](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (vídeo)</span><span class="sxs-lookup"><span data-stu-id="9af45-133">[Windows Animation - Advanced Topics](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (video)</span></span>
-   [<span data-ttu-id="9af45-134">Código de exemplo do Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="9af45-134">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a><span data-ttu-id="9af45-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9af45-135">Related topics</span></span>

[<span data-ttu-id="9af45-136">Visão geral da animação (.NET Framework)</span><span class="sxs-lookup"><span data-stu-id="9af45-136">Animation Overview (.NET Framework)</span></span>](/dotnet/framework/wpf/graphics-multimedia/animation-overview)
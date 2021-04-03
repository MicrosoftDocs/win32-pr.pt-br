---
title: API de ampliação
description: A API de ampliação permite que os aplicativos ampliem a tela inteira ou partes da tela e apliquem efeitos de cor.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/08/2020
ms.locfileid: "103823548"
---
# <a name="magnification-api"></a><span data-ttu-id="64f7e-103">API de ampliação</span><span class="sxs-lookup"><span data-stu-id="64f7e-103">Magnification API</span></span>

## <a name="purpose"></a><span data-ttu-id="64f7e-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="64f7e-104">Purpose</span></span>

<span data-ttu-id="64f7e-105">A API de ampliação permite que os aplicativos ampliem a tela inteira ou partes da tela e apliquem efeitos de cor.</span><span class="sxs-lookup"><span data-stu-id="64f7e-105">The Magnification API enables applications to magnify the entire screen or portions of the screen, and to apply color effects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="64f7e-106">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="64f7e-106">Where applicable</span></span>

<span data-ttu-id="64f7e-107">Usando a API de ampliação, os desenvolvedores podem criar aplicativos de tecnologia assistencial baseados no Windows que ampliam a tela e aplicam efeitos de cor ao conteúdo da tela ampliado.</span><span class="sxs-lookup"><span data-stu-id="64f7e-107">By using the Magnification API, developers can create Windows-based assistive-technology applications that magnify the screen and apply color effects to the magnified screen content.</span></span> <span data-ttu-id="64f7e-108">Para os usuários com deficiência visual, o tamanho de imagem ampliado e os efeitos de cor podem ajudar a facilitar a visualização e o uso do computador.</span><span class="sxs-lookup"><span data-stu-id="64f7e-108">For users with low vision, the enlarged image size and color effects can help make the computer easier to see and use.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="64f7e-109">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="64f7e-109">Developer audience</span></span>

<span data-ttu-id="64f7e-110">A API de ampliação foi projetada principalmente para desenvolvedores de C e C++ que entendem a programação do Windows e que estão familiarizados com os conceitos de programação de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="64f7e-110">The Magnification API is designed primarily for C and C++ developers who understand Windows programming and who are familiar with graphics programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="64f7e-111">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="64f7e-111">Run-time requirements</span></span>

<span data-ttu-id="64f7e-112">A versão inicial da API de ampliação tem suporte no Windows Vista e em sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="64f7e-112">The initial release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="64f7e-113">Uma segunda versão adiciona recursos de ampliação de tela inteira e tem suporte no Windows 8 e posterior.</span><span class="sxs-lookup"><span data-stu-id="64f7e-113">A second release adds fullscreen magnification capabilities and is supported on Windows 8 and later.</span></span>

<span data-ttu-id="64f7e-114">A API é suportada pelo Magnification.dll.</span><span class="sxs-lookup"><span data-stu-id="64f7e-114">The API is supported by Magnification.dll.</span></span> <span data-ttu-id="64f7e-115">Para compilar seu aplicativo, inclua ampliação. h e vincule a ampliação. lib.</span><span class="sxs-lookup"><span data-stu-id="64f7e-115">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="64f7e-116">A API de ampliação não tem suporte no WOW64; ou seja, um aplicativo de lupa de 32 bits não será executado corretamente em janelas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="64f7e-116">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="64f7e-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="64f7e-117">In this section</span></span>

| <span data-ttu-id="64f7e-118">Tópico</span><span class="sxs-lookup"><span data-stu-id="64f7e-118">Topic</span></span> | <span data-ttu-id="64f7e-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="64f7e-119">Description</span></span> |
|:---|:---|
| [<span data-ttu-id="64f7e-120">Visão geral da API de ampliação</span><span class="sxs-lookup"><span data-stu-id="64f7e-120">Magnification API Overview</span></span>](magapi-intro.md)<br/> | <span data-ttu-id="64f7e-121">Este tópico descreve a API de ampliação e explica como usá-la em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="64f7e-121">This topic describes the Magnification API and explains how to use it in an application.</span></span><br/> |
| [<span data-ttu-id="64f7e-122">Referência</span><span class="sxs-lookup"><span data-stu-id="64f7e-122">Reference</span></span>](entry-magapi-ref.md)<br/>  | <span data-ttu-id="64f7e-123">Esta seção contém informações de referência para a API de ampliação.</span><span class="sxs-lookup"><span data-stu-id="64f7e-123">This section contains reference information for the Magnification API.</span></span><br/>|
| [<span data-ttu-id="64f7e-124">Amostras</span><span class="sxs-lookup"><span data-stu-id="64f7e-124">Samples</span></span>](magapi-samples-entry.md)<br/> | <span data-ttu-id="64f7e-125">O exemplo de aplicativo a seguir demonstra como usar a API de ampliação para criar uma lupa de tela inteira que amplia toda a tela e uma lupa em janelas que aumenta e exibe uma parte da tela em uma janela.</span><span class="sxs-lookup"><span data-stu-id="64f7e-125">The following sample application demonstrates how to use the Magnification API to create a full screen magnifier that magnifies the entire screen, and a windowed magnifier that magnifies and displays a portion of the screen in a window.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="64f7e-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64f7e-126">Related topics</span></span>

<span data-ttu-id="64f7e-127">[Site de acessibilidade da Microsoft](https://www.microsoft.com/accessibility/), [acessibilidade no Windows 10](/windows/apps/accessibility)</span><span class="sxs-lookup"><span data-stu-id="64f7e-127">[Microsoft Accessibility website](https://www.microsoft.com/accessibility/), [Accessibility in Windows 10](/windows/apps/accessibility)</span></span>

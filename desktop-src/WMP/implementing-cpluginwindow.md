---
title: Implementando CPluginWindow
description: Implementando CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Plug-ins do Windows Media Player, classe CPluginWindow
- plug-ins, classe CPluginWindow
- plug-ins de interface do usuário, classe CPluginWindow
- Plug-ins de interface do usuário, classe CPluginWindow
- Classe CPluginWindow
- Guia de programação, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635426"
---
# <a name="implementing-cpluginwindow"></a><span data-ttu-id="bc125-109">Implementando CPluginWindow</span><span class="sxs-lookup"><span data-stu-id="bc125-109">Implementing CPluginWindow</span></span>

<span data-ttu-id="bc125-110">A classe CPluginWindow fornece a interface do usuário para o plug-in.</span><span class="sxs-lookup"><span data-stu-id="bc125-110">The CPluginWindow class provides the UI to the plug-in.</span></span> <span data-ttu-id="bc125-111">No caso do plug-in da interface do usuário de pesquisa, essa classe contém o código para o botão de **pesquisa** e o código que inicia a página de pesquisa quando o botão é clicado.</span><span class="sxs-lookup"><span data-stu-id="bc125-111">In the case of the Search UI plug-in, this class contains the code for the **Search** button and the code that launches the search page when the button is clicked.</span></span>

<span data-ttu-id="bc125-112">O assistente fornece uma implementação básica de CPluginWindow no arquivo de cabeçalho CPluginWindow. h.</span><span class="sxs-lookup"><span data-stu-id="bc125-112">The wizard provides a basic implementation of CPluginWindow in the CPluginWindow.h header file.</span></span> <span data-ttu-id="bc125-113">Para manter as coisas simples, o plug-in da interface do usuário de pesquisa modificará esse arquivo diretamente, embora adições extensivas normalmente seriam colocadas em um arquivo CPluginWindow. cpp separado.</span><span class="sxs-lookup"><span data-stu-id="bc125-113">To keep things simple, the Search UI plug-in will modify this file directly, although extensive additions would normally be placed in a separate CPluginWindow.cpp file.</span></span>

<span data-ttu-id="bc125-114">As seções a seguir descrevem o que você precisa fazer para implementar o CPluginWindow:</span><span class="sxs-lookup"><span data-stu-id="bc125-114">The following sections describe what you need to do to implement CPluginWindow:</span></span>

-   [<span data-ttu-id="bc125-115">O mapa de mensagens</span><span class="sxs-lookup"><span data-stu-id="bc125-115">The Message Map</span></span>](the-message-map.md)
-   [<span data-ttu-id="bc125-116">O Construtor</span><span class="sxs-lookup"><span data-stu-id="bc125-116">The Constructor</span></span>](the-constructor.md)
-   [<span data-ttu-id="bc125-117">O método OnPaint</span><span class="sxs-lookup"><span data-stu-id="bc125-117">The OnPaint Method</span></span>](the-onpaint-method.md)
-   [<span data-ttu-id="bc125-118">O método OnCreate</span><span class="sxs-lookup"><span data-stu-id="bc125-118">The OnCreate Method</span></span>](the-oncreate-method.md)
-   [<span data-ttu-id="bc125-119">O método onsearch</span><span class="sxs-lookup"><span data-stu-id="bc125-119">The OnSearch Method</span></span>](the-onsearch-method.md)
-   [<span data-ttu-id="bc125-120">O método LaunchPage</span><span class="sxs-lookup"><span data-stu-id="bc125-120">The LaunchPage Method</span></span>](the-launchpage-method.md)

## <a name="related-topics"></a><span data-ttu-id="bc125-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc125-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc125-122">**Guia de programação de plug-ins de interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="bc125-122">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 





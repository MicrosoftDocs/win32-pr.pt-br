---
description: A regra geral é que um aplicativo de desktop pode chamar uma API de Windows Runtime (WinRT). No entanto, algumas APIs, incluindo as APIs da interface do usuário XAML, exigem que o aplicativo de chamada tenha uma identidade de pacote.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: APIs do WinRT que podem ser chamadas de um aplicativo de desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f99cca14c066f372ad7fd417e04137a62ae628
ms.sourcegitcommit: 133954d5dbcd5b2b3b50c8efd16cd101278fc1db
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108172478"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a><span data-ttu-id="ddede-104">APIs do WinRT que podem ser chamadas de um aplicativo de desktop</span><span class="sxs-lookup"><span data-stu-id="ddede-104">WinRT APIs callable from a desktop app</span></span>

<span data-ttu-id="ddede-105">As [APIs mais Windows Runtime (WinRT)](/uwp/api/) podem ser usadas por aplicativos da área de trabalho (.net e C++ nativo).</span><span class="sxs-lookup"><span data-stu-id="ddede-105">Most [Windows Runtime (WinRT) APIs](/uwp/api/) can be used by desktop (.NET and native C++) apps.</span></span> <span data-ttu-id="ddede-106">No entanto, algumas classes do WinRT são projetadas para o e têm suporte apenas para uso em aplicativos UWP.</span><span class="sxs-lookup"><span data-stu-id="ddede-106">However, some WinRT classes are designed for and are only supported for use in UWP apps.</span></span> <span data-ttu-id="ddede-107">Isso inclui [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)e algumas classes relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ddede-107">This includes [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview), and some related classes.</span></span> <span data-ttu-id="ddede-108">Outras classes do WinRT funcionam em aplicativos de área de trabalho, exceto para membros específicos.</span><span class="sxs-lookup"><span data-stu-id="ddede-108">Other WinRT classes work in desktop apps except for specific members.</span></span>

<span data-ttu-id="ddede-109">Para obter mais informações, consulte [APIs de Windows Runtime sem suporte em aplicativos da área de trabalho](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api).</span><span class="sxs-lookup"><span data-stu-id="ddede-109">For more information, see [Windows Runtime APIs not supported in desktop apps](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api).</span></span> <span data-ttu-id="ddede-110">Quando disponível, este artigo sugere APIs alternativas para obter a mesma funcionalidade que as APIs sem suporte.</span><span class="sxs-lookup"><span data-stu-id="ddede-110">Where available, this article suggests alternative APIs to achieve the same functionality as the unsupported APIs.</span></span>

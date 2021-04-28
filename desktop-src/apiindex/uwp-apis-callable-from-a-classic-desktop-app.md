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
# <a name="winrt-apis-callable-from-a-desktop-app"></a>APIs do WinRT que podem ser chamadas de um aplicativo de desktop

As [APIs mais Windows Runtime (WinRT)](/uwp/api/) podem ser usadas por aplicativos da área de trabalho (.net e C++ nativo). No entanto, algumas classes do WinRT são projetadas para o e têm suporte apenas para uso em aplicativos UWP. Isso inclui [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)e algumas classes relacionadas. Outras classes do WinRT funcionam em aplicativos de área de trabalho, exceto para membros específicos.

Para obter mais informações, consulte [APIs de Windows Runtime sem suporte em aplicativos da área de trabalho](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api). Quando disponível, este artigo sugere APIs alternativas para obter a mesma funcionalidade que as APIs sem suporte.

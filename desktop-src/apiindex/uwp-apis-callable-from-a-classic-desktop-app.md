---
description: a regra geral é que um aplicativo de desktop pode chamar uma API de Windows Runtime (WinRT). No entanto, algumas APIs, incluindo as APIs da interface do usuário XAML, exigem que o aplicativo de chamada tenha uma identidade de pacote.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: APIs do WinRT que podem ser chamadas de um aplicativo para desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bbfb2316a6fd4dd8d35d0744acc4ad301dba7f42aee36ee865d67bb2fff805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130298"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a>APIs do WinRT que podem ser chamadas de um aplicativo para desktop

as [APIs mais Windows Runtime (WinRT)](/uwp/api/) podem ser usadas por aplicativos da área de trabalho (.net e C++ nativo). No entanto, algumas classes do WinRT são projetadas para o e têm suporte apenas para uso em aplicativos UWP. Isso inclui [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)e algumas classes relacionadas. Outras classes do WinRT funcionam em aplicativos para desktop, exceto para membros específicos.

Para saber mais, confira [APIs do Windows Runtime sem suporte em aplicativos da área de trabalho](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api). Quando disponível, este artigo sugere APIs alternativas para obter a mesma funcionalidade que as APIs sem suporte.

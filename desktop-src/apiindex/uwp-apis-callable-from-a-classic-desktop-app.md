---
description: A regra geral é que um aplicativo de desktop pode chamar uma API de Windows Runtime (WinRT). No entanto, algumas APIs, incluindo as APIs da interface do usuário XAML, exigem que o aplicativo de chamada tenha uma identidade de pacote.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: APIs do WinRT que podem ser chamadas de um aplicativo de desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9083fbfb16391c626f49b79176fed7a81068c028
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/24/2020
ms.locfileid: "104008591"
---
# <a name="calling-winrt-apis-from-a-desktop-app"></a>Chamando APIs do WinRT de um aplicativo de desktop

A regra geral é que um aplicativo de desktop pode chamar uma API do WinRT. No entanto, algumas APIs, incluindo as APIs da interface do usuário XAML, exigem que o aplicativo de chamada tenha uma identidade de pacote. Os aplicativos UWP têm um modelo de aplicativo bem definido e têm uma identidade de pacote. Os outros tipos de aplicativos da área de trabalho não têm um modelo de aplicativo bem definido, nem uma identidade de pacote. Portanto, se uma API exigir uma identidade de pacote, um aplicativo WPF, Windows Forms ou Win32 não poderá chamá-la, a menos que o aplicativo [seja empacotado em um pacote MSIX](/windows/msix/desktop/desktop-to-uwp-root).

## <a name="the-dualapipartition-attribute"></a>O atributo DualApiPartition

Esse é o processo a seguir sempre que houver um WinRT específico que você gostaria de chamar de seu aplicativo de desktop. Esse processo responderá à pergunta se a API tem permissão para ser chamada de um aplicativo de desktop. Primeiro, visite a [referência da API do Windows para Windows Runtime aplicativos](/uwp/), encontre o tópico de referência para a API de classe ou membro em que você está interessado e verifique se o atributo [**DualApiPartition**](/uwp/api/Windows.Foundation.Metadata.DualApiPartitionAttribute) está listado na seção atributos.

## <a name="if-the-dualapipartition-attribute-is-listed"></a>Se o atributo DualApiPartition estiver listado

Se o atributo DualApiPartition estiver listado, a API não precisará que o aplicativo de chamada tenha uma identidade de pacote e a API poderá ser chamada de qualquer aplicativo de área de trabalho. [**Windows. Devices. Geolocalize. geolocator**](/uwp/api/Windows.Devices.Geolocation.Geolocator) é um exemplo; um aplicativo não precisa ser identificado exclusivamente para executar tarefas de localização.

## <a name="if-the-dualapipartition-attribute-is-not-listed"></a>Se o atributo DualApiPartition não estiver listado

Se o atributo DualApiPartition não estiver listado, a API não precisará que o aplicativo de chamada tenha uma identidade de pacote. Portanto, um aplicativo WPF, Windows Forms ou Win32 não tem permissão para chamar a API, a menos que o aplicativo tenha sido convertido em um aplicativo UWP. [**Windows. UI. XAML. Controls. Button**](/uwp/api/Windows.UI.Xaml.Controls.Button) é um exemplo.

---
description: Depois de criar uma DLL para receber notificações de conexão, você deve registrá-la no sistema.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registrando-se para receber notificações de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3a25e26e290700b8f343d3d543af4fbd7b709ff8b099522e4cd4b02b3d587f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919469"
---
# <a name="registering-to-receive-connection-notifications"></a>Registrando-se para receber notificações de conexão

Depois de criar uma DLL para receber notificações de conexão, você deve registrá-la no sistema. Você faz isso adicionando um **valor REG \_ EXPAND \_ SZ** sob o

**HKEY \_ Rede \_ de controle Local MACHINE** \\ **SYSTEM** \\ **CurrentControlSetProvider** \\  \\  \\ **Notifyees**

chave. Esse valor especifica o caminho para a DLL que implementa a [conexão API de Notificação](connection-notification-api.md).

O valor pode ter qualquer nome. Todos os valores na **chave Notifyees** são tratados como caminhos para DLLs que são notificados sobre eventos de conexão. É recomendável que você use um nome que identifique sua DLL. Isso diminui a chance de um conflito de nome com outros aplicativos de notificação de conexão.

Para obter mais informações sobre como criar um aplicativo que recebe notificações de conexão, consulte [Recebendo notificações de conexão](receiving-connection-notifications.md).

 

 




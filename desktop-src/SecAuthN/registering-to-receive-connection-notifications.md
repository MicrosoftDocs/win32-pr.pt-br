---
description: Depois de criar uma DLL para receber notificações de conexão, você deve registrá-la no sistema.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registrando para receber notificações de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662129"
---
# <a name="registering-to-receive-connection-notifications"></a>Registrando para receber notificações de conexão

Depois de criar uma DLL para receber notificações de conexão, você deve registrá-la no sistema. Para fazer isso, adicione um valor **reg \_ Expand \_ sz** sob o

**HKEY \_ Sistema de \_ computador local** \\  \\ **CurrentControlSet** \\ **Control** o \\ **NetworkProvider** \\ **notifica** os

chave. Esse valor especifica o caminho para a DLL que implementa a [API de notificação de conexão](connection-notification-api.md).

O valor pode ter qualquer nome. Todos os valores na chave **notificadores** são tratados como caminhos para DLLs notificados de eventos de conexão. É recomendável que você use um nome que identifique sua DLL. Isso diminui a chance de um conflito de nome com outros aplicativos de notificação de conexão.

Para obter mais informações sobre como criar um aplicativo que recebe notificações de conexão, consulte [recebendo notificações de conexão](receiving-connection-notifications.md).

 

 




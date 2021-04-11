---
description: As informações sobre pacotes de notificação do Winlogon são armazenadas no registro. Entradas do registro especificam o nome do pacote de notificação, o nome da DLL que implementa o pacote e os nomes das funções que manipulam eventos do Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registrando um pacote de notificação do Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169368"
---
# <a name="registering-a-winlogon-notification-package"></a>Registrando um pacote de notificação do Winlogon

As informações sobre pacotes de notificação do [*Winlogon*](../secgloss/w-gly.md) são armazenadas no registro. Entradas do registro especificam o nome do pacote de notificação, o nome da DLL que implementa o pacote e os nomes das funções que manipulam eventos do Winlogon.

Quando o Winlogon é iniciado, ele verifica o registro e carrega todos os pacotes de notificação registrados. Quando ocorre um evento, o Winlogon chama a função de manipulador de eventos designada para cada pacote. Vários pacotes de notificação de eventos podem ser registrados em um sistema.

Para registrar seu pacote de notificação, crie uma chave do registro chamada **Notify** como uma subchave da seguinte chave do registro e adicione os valores detalhados em [entradas do registro](registry-entries.md).

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**

 

 

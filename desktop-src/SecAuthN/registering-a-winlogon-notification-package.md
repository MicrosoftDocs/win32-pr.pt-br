---
description: Informações sobre pacotes de notificação do Winlogon são armazenadas no Registro. As entradas do Registro especificam o nome do pacote de notificação, o nome da DLL que implementa o pacote e os nomes das funções que lidam com eventos do Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registrando um pacote de notificação do Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa41948062458581d607b64432166b99ba4701865a3c7b593365c87342359ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919665"
---
# <a name="registering-a-winlogon-notification-package"></a>Registrando um pacote de notificação do Winlogon

Informações sobre pacotes de notificação do [*Winlogon*](../secgloss/w-gly.md) são armazenadas no Registro. As entradas do Registro especificam o nome do pacote de notificação, o nome da DLL que implementa o pacote e os nomes das funções que lidam com eventos do Winlogon.

Quando o Winlogon é iniciado, ele verifica o Registro e carrega todos os pacotes de notificação registrados. Quando ocorre um evento, o Winlogon chama a função de manipulador de eventos designada para cada pacote. Vários pacotes de notificação de eventos podem ser registrados em um sistema.

Para registrar seu pacote de notificação, crie uma chave do Registro chamada **Notify** como uma subkey da seguinte chave do Registro e adicione os valores detalhados em [Entradas do Registro](registry-entries.md).

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**

 

 

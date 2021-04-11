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
# <a name="registering-a-winlogon-notification-package"></a><span data-ttu-id="7d56d-104">Registrando um pacote de notificação do Winlogon</span><span class="sxs-lookup"><span data-stu-id="7d56d-104">Registering a Winlogon Notification Package</span></span>

<span data-ttu-id="7d56d-105">As informações sobre pacotes de notificação do [*Winlogon*](../secgloss/w-gly.md) são armazenadas no registro.</span><span class="sxs-lookup"><span data-stu-id="7d56d-105">Information about [*Winlogon*](../secgloss/w-gly.md) notification packages is stored in the registry.</span></span> <span data-ttu-id="7d56d-106">Entradas do registro especificam o nome do pacote de notificação, o nome da DLL que implementa o pacote e os nomes das funções que manipulam eventos do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="7d56d-106">Registry entries specify the name of the notification package, the name of the DLL that implements the package, and the names of the functions that handle Winlogon events.</span></span>

<span data-ttu-id="7d56d-107">Quando o Winlogon é iniciado, ele verifica o registro e carrega todos os pacotes de notificação registrados.</span><span class="sxs-lookup"><span data-stu-id="7d56d-107">When Winlogon starts, it checks the registry and loads any registered notification packages.</span></span> <span data-ttu-id="7d56d-108">Quando ocorre um evento, o Winlogon chama a função de manipulador de eventos designada para cada pacote.</span><span class="sxs-lookup"><span data-stu-id="7d56d-108">When an event occurs, Winlogon calls the designated event handler function for each package.</span></span> <span data-ttu-id="7d56d-109">Vários pacotes de notificação de eventos podem ser registrados em um sistema.</span><span class="sxs-lookup"><span data-stu-id="7d56d-109">Multiple event notification packages may be registered on a system.</span></span>

<span data-ttu-id="7d56d-110">Para registrar seu pacote de notificação, crie uma chave do registro chamada **Notify** como uma subchave da seguinte chave do registro e adicione os valores detalhados em [entradas do registro](registry-entries.md).</span><span class="sxs-lookup"><span data-stu-id="7d56d-110">To register your notification package, create a registry key named **Notify** as a subkey of the following registry key and add the values detailed in [Registry Entries](registry-entries.md).</span></span>

<span data-ttu-id="7d56d-111">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**</span><span class="sxs-lookup"><span data-stu-id="7d56d-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Winlogon**</span></span>

 

 

---
description: API de gerenciamento de credenciais
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API de gerenciamento de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662418"
---
# <a name="credential-management-api"></a><span data-ttu-id="a3bf2-103">API de gerenciamento de credenciais</span><span class="sxs-lookup"><span data-stu-id="a3bf2-103">Credential Management API</span></span>

<span data-ttu-id="a3bf2-104">As funções de gerenciamento de credenciais constituem o conjunto de funções que um Gerenciador de credenciais deve implementar.</span><span class="sxs-lookup"><span data-stu-id="a3bf2-104">The credential management functions constitute the set of functions that a credential manager must implement.</span></span> <span data-ttu-id="a3bf2-105">Eles são:</span><span class="sxs-lookup"><span data-stu-id="a3bf2-105">These are:</span></span>

-   <span data-ttu-id="a3bf2-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), uma função de manipulador de eventos que o MPR chama quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="a3bf2-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), an event-handler function that the MPR calls when a user logs on.</span></span>
-   <span data-ttu-id="a3bf2-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), uma função de manipulador de eventos que o MPR chama quando uma senha de conta é alterada.</span><span class="sxs-lookup"><span data-stu-id="a3bf2-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), an event-handler function the MPR calls when an account password is changed.</span></span>

<span data-ttu-id="a3bf2-108">As funções de gerenciamento de credenciais são sempre chamadas no contexto do sistema (LocalSystem) em vez do contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="a3bf2-108">The credential management functions are always called in the system context (LocalSystem) rather than the user context.</span></span>

<span data-ttu-id="a3bf2-109">Para obter mais informações sobre como criar e registrar um aplicativo Gerenciador de credenciais, consulte [implementando um Gerenciador de credenciais](implementing-a-credential-manager.md) e [registrando provedores de rede e gerenciadores de credenciais](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="a3bf2-109">For more information about how to create and register a credential manager application, see [Implementing a Credential Manager](implementing-a-credential-manager.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

 




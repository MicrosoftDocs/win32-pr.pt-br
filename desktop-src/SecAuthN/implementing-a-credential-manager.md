---
description: Lista as exportações de DLL que devem ser implementadas para criar um Gerenciador de credenciais.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementando um Gerenciador de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829761"
---
# <a name="implementing-a-credential-manager"></a><span data-ttu-id="227df-103">Implementando um Gerenciador de credenciais</span><span class="sxs-lookup"><span data-stu-id="227df-103">Implementing a Credential Manager</span></span>

<span data-ttu-id="227df-104">Para criar um Gerenciador de credenciais, você deve criar uma DLL que exporta as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="227df-104">To create a credential manager, you must create a DLL that exports the following functions:</span></span>

-   [<span data-ttu-id="227df-105">**NPLogonNotify**</span><span class="sxs-lookup"><span data-stu-id="227df-105">**NPLogonNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [<span data-ttu-id="227df-106">**NPPasswordChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="227df-106">**NPPasswordChangeNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

<span data-ttu-id="227df-107">Para restaurar as notificações para as funções [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) para logon de cartão inteligente, crie uma entrada de registro chamada **SmartCardLogonNotify** como uma **DWORD** e defina-a como 1:</span><span class="sxs-lookup"><span data-stu-id="227df-107">To restore notifications to the [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) functions for smart card logon, create a registry entry called **SmartCardLogonNotify** as a **DWORD**, and set it to 1:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

<span data-ttu-id="227df-108">**Windows Server 2003 e Windows XP:** A entrada do registro **SmartCardLogonNotify** não é necessária.</span><span class="sxs-lookup"><span data-stu-id="227df-108">**Windows Server 2003 and Windows XP:** The **SmartCardLogonNotify** registry entry is not required.</span></span>

<span data-ttu-id="227df-109">Além disso, os gerenciadores de credenciais também devem dar suporte à função [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para o WNNC \_ Iniciar (o suporte a outros índices não é necessário para os gerenciadores de credenciais).</span><span class="sxs-lookup"><span data-stu-id="227df-109">In addition, credential managers should also support the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function for WNNC\_START (supporting other indexes is not required for credential managers).</span></span> <span data-ttu-id="227df-110">Isso informa ao MPR quando um Gerenciador de credenciais será iniciado.</span><span class="sxs-lookup"><span data-stu-id="227df-110">This tells MPR when a credential manager will start.</span></span> <span data-ttu-id="227df-111">Chamando **NPGetCaps** com o parâmetro *NINDEX* definido como WNNC \_ Start, o MPR Obtém o tempo de espera antes de chamar as funções do ponto de entrada de gerenciamento de credenciais do provedor.</span><span class="sxs-lookup"><span data-stu-id="227df-111">By calling **NPGetCaps** with the *nIndex* parameter set to WNNC\_START, the MPR gets the time to wait before calling the provider's credential management entry point functions.</span></span> <span data-ttu-id="227df-112">E se o MPR tiver essas informações, ela poderá encaminhá-la ao Gerenciador de credenciais, definindo o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="227df-112">And if the MPR has this information, it can forward it to the credential manager, setting the time out.</span></span>

 

 




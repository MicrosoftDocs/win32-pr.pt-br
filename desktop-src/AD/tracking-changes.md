---
title: Controlando alterações
description: Alguns aplicativos devem manter a consistência entre dados específicos armazenados no serviço de diretório Active Directory e outros dados.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, controlando alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917098"
---
# <a name="tracking-changes"></a><span data-ttu-id="61238-104">Controlando alterações</span><span class="sxs-lookup"><span data-stu-id="61238-104">Tracking Changes</span></span>

<span data-ttu-id="61238-105">Alguns aplicativos devem manter a consistência entre dados específicos armazenados no serviço de diretório Active Directory e outros dados.</span><span class="sxs-lookup"><span data-stu-id="61238-105">Some applications must maintain consistency between specific data stored in the Active Directory directory service and other data.</span></span> <span data-ttu-id="61238-106">Os outros dados podem ser armazenados no diretório, em uma tabela SQL Server, em um arquivo ou no registro.</span><span class="sxs-lookup"><span data-stu-id="61238-106">The other data might be stored in the directory, in a SQL Server table, in a file, or in the registry.</span></span> <span data-ttu-id="61238-107">Quando os dados armazenados no diretório são alterados, os outros dados podem precisar ser alterados para permanecerem consistentes.</span><span class="sxs-lookup"><span data-stu-id="61238-107">When data stored in the directory changes, the other data may be required to change in order to remain consistent.</span></span> <span data-ttu-id="61238-108">Os aplicativos que têm esse requisito incluem:</span><span class="sxs-lookup"><span data-stu-id="61238-108">Applications that have this requirement include:</span></span>

<span data-ttu-id="61238-109">Esta seção não aborda os mecanismos usados pelos aplicativos de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="61238-109">This section does not cover mechanisms used by monitoring applications.</span></span> <span data-ttu-id="61238-110">Esses são aplicativos que monitoram as alterações de diretório sem a finalidade de manter dados consistentes entre repositórios separados, mas como uma ferramenta de gerenciamento de sistema.</span><span class="sxs-lookup"><span data-stu-id="61238-110">These are applications that monitor directory changes not for the purpose of maintaining consistent data between separate stores, but as a system management tool.</span></span> <span data-ttu-id="61238-111">Embora os aplicativos de monitoramento possam usar os mesmos mecanismos que oferecem suporte a aplicativos de controle de alterações, os mecanismos a seguir são projetados especificamente para monitorar aplicativos:</span><span class="sxs-lookup"><span data-stu-id="61238-111">Although monitoring applications can use the same mechanisms that support change-tracking applications, the following mechanisms are specifically designed for monitoring applications:</span></span>

-   <span data-ttu-id="61238-112">Auditoria de segurança.</span><span class="sxs-lookup"><span data-stu-id="61238-112">Security auditing.</span></span> <span data-ttu-id="61238-113">Ao modificar a parte da SACL (lista de controle de acesso) do sistema de um descritor de segurança de objeto, você pode fazer com que os acessos ao objeto em um determinado controlador de domínio gerem registros de auditoria no log de eventos de segurança nesse DC.</span><span class="sxs-lookup"><span data-stu-id="61238-113">By modifying the system access-control list (SACL) portion of an object security descriptor, you can cause accesses to the object on a given domain controller to generate audit records in the security event log on that DC.</span></span> <span data-ttu-id="61238-114">Você pode auditar leituras, gravações ou ambos; Você pode auditar o objeto inteiro ou os atributos específicos.</span><span class="sxs-lookup"><span data-stu-id="61238-114">You can audit reads, writes, or both; you can audit the entire object or specific attributes.</span></span> <span data-ttu-id="61238-115">Para obter mais informações, consulte [recuperando a SACL e a geração de auditoria de um objeto](retrieving-an-objectampaposs-sacl.md) . [](/windows/desktop/SecAuthZ/audit-generation)</span><span class="sxs-lookup"><span data-stu-id="61238-115">For more information, see [Retrieving an Object's SACL](retrieving-an-objectampaposs-sacl.md) and [Audit Generation](/windows/desktop/SecAuthZ/audit-generation).</span></span>
-   <span data-ttu-id="61238-116">Log de eventos.</span><span class="sxs-lookup"><span data-stu-id="61238-116">Event logging.</span></span> <span data-ttu-id="61238-117">Ao modificar as configurações do registro em um determinado controlador de domínio, você pode alterar os tipos de eventos registrados no log de eventos do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="61238-117">By modifying registry settings on a given domain controller, you can change the kinds of events logged to the directory service event log.</span></span> <span data-ttu-id="61238-118">Especificamente, para registrar todas as modificações, defina o valor de **8 acesso ao diretório** na seguinte chave do registro para 4.</span><span class="sxs-lookup"><span data-stu-id="61238-118">Specifically, to log all modifications, set the **8 Directory Access** value under the following registry key to 4.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    <span data-ttu-id="61238-119">Para obter mais informações, consulte [log de eventos](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="61238-119">For more information, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

-   <span data-ttu-id="61238-120">Rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="61238-120">Event tracing.</span></span> <span data-ttu-id="61238-121">O Windows 2000 introduziu uma API de rastreamento de eventos para rastreamento e registro em log de eventos interessantes em software ou hardware.</span><span class="sxs-lookup"><span data-stu-id="61238-121">Windows 2000 introduced an Event Tracing API for tracing and logging interesting events in software or hardware.</span></span> <span data-ttu-id="61238-122">O sistema operacional Windows, e Active Directory Domain Services em particular, dão suporte ao uso de rastreamento de eventos para planejamento de capacidade e análise de desempenho detalhada.</span><span class="sxs-lookup"><span data-stu-id="61238-122">The Windows operating system, and Active Directory Domain Services in particular, support the use of event tracing for capacity planning and detailed performance analysis.</span></span> <span data-ttu-id="61238-123">Para obter mais informações, consulte [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) e [rastreamento de eventos em ADSI](/windows/desktop/ADSI/adsi-and-etw).</span><span class="sxs-lookup"><span data-stu-id="61238-123">For more information, see [Event Tracing](/windows/desktop/ETW/event-tracing-portal) and [Event Tracing in ADSI](/windows/desktop/ADSI/adsi-and-etw).</span></span>

<span data-ttu-id="61238-124">Esta seção inclui os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="61238-124">This section includes the following topics:</span></span>

-   [<span data-ttu-id="61238-125">Visão geral das técnicas de Controle de Alterações</span><span class="sxs-lookup"><span data-stu-id="61238-125">Overview of Change Tracking Techniques</span></span>](overview-of-change-tracking-techniques.md)
-   [<span data-ttu-id="61238-126">Notificações de alteração no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="61238-126">Change Notifications in Active Directory Domain Services</span></span>](change-notifications-in-active-directory-domain-services.md)
-   [<span data-ttu-id="61238-127">Sondando alterações usando o controle DirSync</span><span class="sxs-lookup"><span data-stu-id="61238-127">Polling for Changes Using the DirSync Control</span></span>](polling-for-changes-using-the-dirsync-control.md)
-   [<span data-ttu-id="61238-128">Sondando alterações usando USNChanged</span><span class="sxs-lookup"><span data-stu-id="61238-128">Polling for Changes Using USNChanged</span></span>](polling-for-changes-using-usnchanged.md)

 

 
---
title: Agente do sistema de diretório
description: O Directory System Agent (DSA) é uma coleção de serviços e processos que são executados em cada controlador de domínio e fornecem acesso ao armazenamento de dados.
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- Directory System Agent Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823665"
---
# <a name="directory-system-agent"></a><span data-ttu-id="4fffd-104">Agente do sistema de diretório</span><span class="sxs-lookup"><span data-stu-id="4fffd-104">Directory System Agent</span></span>

<span data-ttu-id="4fffd-105">O [*Directory System Agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) é uma coleção de serviços e processos que são executados em cada controlador de domínio e fornecem acesso ao armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="4fffd-105">The [*directory system agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) is a collection of services and processes that run on each domain controller and provides access to the data store.</span></span> <span data-ttu-id="4fffd-106">O armazenamento de dados é o repositório físico de dados de diretório localizados em um disco rígido.</span><span class="sxs-lookup"><span data-stu-id="4fffd-106">The data store is the physical store of directory data located on a hard disk.</span></span> <span data-ttu-id="4fffd-107">No Active Directory Domain Services, o DSA faz parte do subsistema da autoridade do sistema local (LSA).</span><span class="sxs-lookup"><span data-stu-id="4fffd-107">In Active Directory Domain Services, the DSA is part of the local system authority (LSA) subsystem.</span></span> <span data-ttu-id="4fffd-108">Os clientes acessam o diretório usando um dos seguintes mecanismos com suporte no DSA:</span><span class="sxs-lookup"><span data-stu-id="4fffd-108">Clients access the directory using one of the following mechanisms supported by the DSA:</span></span>

-   <span data-ttu-id="4fffd-109">Os clientes LDAP se conectam ao DSA usando o LDAP (Lightweight Directory Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="4fffd-109">LDAP clients connect to the DSA using the Lightweight Directory Access Protocol (LDAP).</span></span> <span data-ttu-id="4fffd-110">O Active Directory Domain Services dá suporte ao LDAP 3,0, definido pela RFC 3377 e pelo LDAP 2,0, definido pela RFC 1777.</span><span class="sxs-lookup"><span data-stu-id="4fffd-110">Active Directory Domain Services support LDAP 3.0, defined by RFC 3377, and LDAP 2.0, defined by RFC 1777.</span></span> <span data-ttu-id="4fffd-111">Os clientes Windows usam o LDAP 3,0 para se conectar ao DSA.</span><span class="sxs-lookup"><span data-stu-id="4fffd-111">Windows clients use LDAP 3.0 to connect to the DSA.</span></span>
-   <span data-ttu-id="4fffd-112">Clientes MAPI, como o Microsoft Exchange Server, se conectam ao DSA usando a interface de chamada de procedimento remoto MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fffd-112">MAPI clients such as Microsoft Exchange Server connect to the DSA using the MAPI remote procedure call interface.</span></span>
-   <span data-ttu-id="4fffd-113">Os DSAs no Active Directory Domain Services se conectam entre si para executar a replicação usando uma interface de chamada de procedimento remoto proprietário.</span><span class="sxs-lookup"><span data-stu-id="4fffd-113">The DSAs in Active Directory Domain Services connect to each other to perform replication using a proprietary remote procedure call interface.</span></span>

 

 
---
description: Um AppContainer é implementado adicionando novas informações ao token de processo, alterando SeAccessCheck () para que todos os objetos de ACL (lista de controle de acesso) herdados não modificados bloqueiem solicitações de acesso de processos do AppContainer por padrão e objetos de Nova ACL que devem estar disponíveis para o AppContainers.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementando um AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829735"
---
# <a name="implementing-an-appcontainer"></a><span data-ttu-id="41a86-103">Implementando um AppContainer</span><span class="sxs-lookup"><span data-stu-id="41a86-103">Implementing an AppContainer</span></span>

<span data-ttu-id="41a86-104">Um AppContainer é implementado adicionando novas informações ao token de processo, alterando [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) para que todos os objetos de ACL (lista de controle de acesso) herdados não modificados bloqueiem solicitações de acesso de processos do AppContainer por padrão e objetos de Nova ACL que devem estar disponíveis para o AppContainers.</span><span class="sxs-lookup"><span data-stu-id="41a86-104">An AppContainer is implemented by adding new information to the process token, changing [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so that all legacy, unmodified access control list (ACL) objects block access requests from AppContainer processes by default, and re-ACL objects that should be available to AppContainers.</span></span>

## <a name="the-process"></a><span data-ttu-id="41a86-105">O processo</span><span class="sxs-lookup"><span data-stu-id="41a86-105">The process</span></span>

<span data-ttu-id="41a86-106">Comece adicionando novas informações para o token de processo.</span><span class="sxs-lookup"><span data-stu-id="41a86-106">Begin by adding new information for the process token.</span></span> <span data-ttu-id="41a86-107">Em seguida, altere **SeAccessCheck ()** para que todas as ACLs herdadas e não modificadas bloqueiem solicitações de acesso de processos do AppContainer por padrão.</span><span class="sxs-lookup"><span data-stu-id="41a86-107">Then change **SeAccessCheck()** so that all legacy, unmodified ACLs will block access requests from AppContainer processes by default.</span></span> <span data-ttu-id="41a86-108">Por fim, recursos de Nova ACL que devem estar disponíveis para AppContainers</span><span class="sxs-lookup"><span data-stu-id="41a86-108">Finally, re-ACL resources that should be available to AppContainers</span></span>

<span data-ttu-id="41a86-109">O SID do AppContainer é um identificador exclusivo persistente para o AppContainer.</span><span class="sxs-lookup"><span data-stu-id="41a86-109">The AppContainer SID is a persistent unique identifier for the appcontainer.</span></span> <span data-ttu-id="41a86-110">Os SIDs de capacidade concedem acesso a grupos de recursos a grupos de AppContainers.</span><span class="sxs-lookup"><span data-stu-id="41a86-110">Capability SIDs grant access to groups of resources to groups of AppContainers.</span></span> <span data-ttu-id="41a86-111">Um AppContainerNumber é um **DWORD** transitório usado para distinguir entre AppContainers.</span><span class="sxs-lookup"><span data-stu-id="41a86-111">An AppContainerNumber is a transient **DWORD** used to distinguish between AppContainers.</span></span> <span data-ttu-id="41a86-112">No entanto, ele não deve ser usado como uma identidade para o AppContainer.</span><span class="sxs-lookup"><span data-stu-id="41a86-112">However, it should not be used as an identity for the AppContainer.</span></span>

<span data-ttu-id="41a86-113">Para permitir que um único AppContainer acesse um recurso, adicione seu AppContainerSID à ACL para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="41a86-113">To allow a single AppContainer to access a resource, add its AppContainerSID to the ACL for that resource.</span></span>

<span data-ttu-id="41a86-114">Para permitir que vários AppContainers específicos acessem um recurso, adicione todos os seus AppContainerSIDs à ACL para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="41a86-114">To allow several specific AppContainers to access a resource, add all of their AppContainerSIDs to the ACL for that resource.</span></span>

<span data-ttu-id="41a86-115">Para gerenciar grupos de permissões, crie um SID de recurso (um GUID) e coloque o SID de recurso em todos os recursos a serem concedidos.</span><span class="sxs-lookup"><span data-stu-id="41a86-115">To manage groups of permissions, create a Capability SID (a GUID) and put that Capability SID on all of the resources to be granted.</span></span> <span data-ttu-id="41a86-116">Em seguida, adicione o SID de recurso ao seu token de processo.</span><span class="sxs-lookup"><span data-stu-id="41a86-116">Then add the Capability SID to your process token.</span></span>

<span data-ttu-id="41a86-117">Para permitir que todos os AppContainers acessem um recurso, adicione o SID **todos os pacotes de aplicativos** à ACL para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="41a86-117">To allow all AppContainers to access a resource, add the **ALL APPLICATION PACKAGES** SID to the ACL for that resource.</span></span> <span data-ttu-id="41a86-118">Isso funciona como um curinga.</span><span class="sxs-lookup"><span data-stu-id="41a86-118">This acts like a wildcard.</span></span>

<span data-ttu-id="41a86-119">O AppContainerSID e o CapabilitySID dão suporte a máscaras de acesso em entradas de controle de acesso (ACE).</span><span class="sxs-lookup"><span data-stu-id="41a86-119">Both AppContainerSID and CapabilitySID support access masks in Access Control Entries (ACE).</span></span> <span data-ttu-id="41a86-120">Defina conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="41a86-120">Set as appropriate.</span></span>

 

 

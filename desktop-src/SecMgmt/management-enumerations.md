---
description: Lista as enumerações usadas pelas funções de gerenciamento de política LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Enumerações de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169681"
---
# <a name="security-management-enumerations"></a><span data-ttu-id="d042f-103">Enumerações de gerenciamento de segurança</span><span class="sxs-lookup"><span data-stu-id="d042f-103">Security Management Enumerations</span></span>

<span data-ttu-id="d042f-104">As enumerações de gerenciamento de segurança incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d042f-104">The security management enumerations include the following:</span></span>

-   [<span data-ttu-id="d042f-105">Enumerações de política LSA</span><span class="sxs-lookup"><span data-stu-id="d042f-105">LSA Policy Enumerations</span></span>](#lsa-policy-enumerations)
-   [<span data-ttu-id="d042f-106">Enumerações mais seguras</span><span class="sxs-lookup"><span data-stu-id="d042f-106">Safer Enumerations</span></span>](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a><span data-ttu-id="d042f-107">Enumerações de política LSA</span><span class="sxs-lookup"><span data-stu-id="d042f-107">LSA Policy Enumerations</span></span>

<span data-ttu-id="d042f-108">Os tipos de enumeração a seguir são usados pelas funções de gerenciamento de política LSA.</span><span class="sxs-lookup"><span data-stu-id="d042f-108">The following enumeration types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="d042f-109">Enumeração</span><span class="sxs-lookup"><span data-stu-id="d042f-109">Enumeration</span></span>                                                                               | <span data-ttu-id="d042f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d042f-110">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d042f-111">**\_tipo de \_ evento de auditoria de política \_**</span><span class="sxs-lookup"><span data-stu-id="d042f-111">**POLICY\_AUDIT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | <span data-ttu-id="d042f-112">Define os tipos de eventos que o sistema pode auditar.</span><span class="sxs-lookup"><span data-stu-id="d042f-112">Defines the types of events the system can audit.</span></span>                                                                                     |
| [<span data-ttu-id="d042f-113">**\_classe de informações de política \_**</span><span class="sxs-lookup"><span data-stu-id="d042f-113">**POLICY\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | <span data-ttu-id="d042f-114">Define os tipos de informações que podem ser definidas ou consultadas para um objeto de [**política**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d042f-114">Defines the types of information that can be set or queried for a [**Policy**](policy-object.md) object.</span></span>                             |
| [<span data-ttu-id="d042f-115">**\_função de \_ servidor \_ LSA de política**</span><span class="sxs-lookup"><span data-stu-id="d042f-115">**POLICY\_LSA\_SERVER\_ROLE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | <span data-ttu-id="d042f-116">Indique a função de um servidor LSA.</span><span class="sxs-lookup"><span data-stu-id="d042f-116">Indicate the role of an LSA server.</span></span>                                                                                                   |
| [<span data-ttu-id="d042f-117">**\_classe de \_ informações de notificação de política \_**</span><span class="sxs-lookup"><span data-stu-id="d042f-117">**POLICY\_NOTIFICATION\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | <span data-ttu-id="d042f-118">Define os tipos de informações de política e informações de domínio de política para os quais seu aplicativo pode solicitar a notificação de alterações.</span><span class="sxs-lookup"><span data-stu-id="d042f-118">Defines the types of policy information and policy domain information for which your application can request notification of changes.</span></span> |
| [<span data-ttu-id="d042f-119">**\_estado de \_ habilitação do servidor de políticas \_**</span><span class="sxs-lookup"><span data-stu-id="d042f-119">**POLICY\_SERVER\_ENABLE\_STATE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | <span data-ttu-id="d042f-120">Representa o estado do servidor LSA, ou seja, se ele está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d042f-120">Represents the state of the LSA server, that is, whether it is enabled or disabled.</span></span>                                                   |
| [<span data-ttu-id="d042f-121">**\_classe de informações confiáveis \_**</span><span class="sxs-lookup"><span data-stu-id="d042f-121">**TRUSTED\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | <span data-ttu-id="d042f-122">Define os tipos de informações que podem ser definidas ou consultadas para um domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="d042f-122">Defines the types of information that can be set or queried for a trusted domain.</span></span>                                                     |



 

## <a name="safer-enumerations"></a><span data-ttu-id="d042f-123">Enumerações mais seguras</span><span class="sxs-lookup"><span data-stu-id="d042f-123">Safer Enumerations</span></span>

<span data-ttu-id="d042f-124">O [mais seguro](safer.md) usa os seguintes tipos enumerados.</span><span class="sxs-lookup"><span data-stu-id="d042f-124">[Safer](safer.md) uses the following enumerated types.</span></span>



| <span data-ttu-id="d042f-125">Name</span><span class="sxs-lookup"><span data-stu-id="d042f-125">Name</span></span>                                                               | <span data-ttu-id="d042f-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="d042f-126">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d042f-127">**tipos de \_ identificação mais seguros \_**</span><span class="sxs-lookup"><span data-stu-id="d042f-127">**SAFER\_IDENTIFICATION\_TYPES**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | <span data-ttu-id="d042f-128">Tipo de enumeração que define os possíveis tipos de estruturas de regra de identificação que podem ser identificadas pela estrutura de [**\_ \_ cabeçalho de identificação mais segura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) .</span><span class="sxs-lookup"><span data-stu-id="d042f-128">Enumeration type that defines the possible types of identification rule structures that can be identified by the [**SAFER\_IDENTIFICATION\_HEADER**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) structure.</span></span> |
| [<span data-ttu-id="d042f-129">**classe de \_ informações de objeto mais seguro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d042f-129">**SAFER\_OBJECT\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | <span data-ttu-id="d042f-130">Tipo de enumeração que define o tipo de informações solicitadas sobre um objeto mais seguro.</span><span class="sxs-lookup"><span data-stu-id="d042f-130">Enumeration type that defines the type of information requested about a Safer object.</span></span>                                                                                                            |
| [<span data-ttu-id="d042f-131">**classe de \_ informações de política mais segura \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d042f-131">**SAFER\_POLICY\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | <span data-ttu-id="d042f-132">Tipo de enumeração que define as maneiras em que uma política pode ser consultada.</span><span class="sxs-lookup"><span data-stu-id="d042f-132">Enumeration type that defines the ways in which a policy may be queried.</span></span>                                                                                                                         |



 

 

 




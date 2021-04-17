---
description: Lista e descreve os tipos de acesso do objeto de política.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Direitos de acesso ao objeto de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769265"
---
# <a name="policy-object-access-rights"></a><span data-ttu-id="d8642-103">Direitos de acesso ao objeto de política</span><span class="sxs-lookup"><span data-stu-id="d8642-103">Policy Object Access Rights</span></span>

<span data-ttu-id="d8642-104">O objeto de [**política**](policy-object.md) tem os seguintes tipos de acesso específicos de objeto:</span><span class="sxs-lookup"><span data-stu-id="d8642-104">The [**Policy**](policy-object.md) object has the following object-specific access types:</span></span>



| <span data-ttu-id="d8642-105">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="d8642-105">Access type</span></span>                         | <span data-ttu-id="d8642-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8642-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8642-107">\_ \_ informações locais da exibição de política \_</span><span class="sxs-lookup"><span data-stu-id="d8642-107">POLICY\_VIEW\_LOCAL\_INFORMATION</span></span>    | <span data-ttu-id="d8642-108">Esse tipo de acesso é necessário para ler as informações de política de segurança diversas do sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="d8642-108">This access type is needed to read the target system's miscellaneous security policy information.</span></span> <span data-ttu-id="d8642-109">Isso inclui a cota padrão, a auditoria, o estado do servidor e as informações de função e as informações de confiança.</span><span class="sxs-lookup"><span data-stu-id="d8642-109">This includes the default quota, auditing, server state and role information, and trust information.</span></span> <span data-ttu-id="d8642-110">Esse tipo de acesso também é necessário para enumerar domínios, contas e [*privilégios*](/windows/desktop/SecGloss/p-gly)confiáveis.</span><span class="sxs-lookup"><span data-stu-id="d8642-110">This access type is also needed to enumerate trusted domains, accounts, and [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> |
| <span data-ttu-id="d8642-111">\_obter \_ informações particulares \_ de política</span><span class="sxs-lookup"><span data-stu-id="d8642-111">POLICY\_GET\_PRIVATE\_INFORMATION</span></span>   | <span data-ttu-id="d8642-112">Esse tipo de acesso é necessário para exibir informações confidenciais, como os nomes das contas estabelecidas para relações de domínio confiáveis.</span><span class="sxs-lookup"><span data-stu-id="d8642-112">This access type is needed to view sensitive information, such as the names of accounts established for trusted domain relationships.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="d8642-113">\_administrador de confiança de política \_</span><span class="sxs-lookup"><span data-stu-id="d8642-113">POLICY\_TRUST\_ADMIN</span></span>                | <span data-ttu-id="d8642-114">Esse tipo de acesso é necessário para alterar as informações de domínio de conta ou domínio primário.</span><span class="sxs-lookup"><span data-stu-id="d8642-114">This access type is needed to change the account domain or primary domain information.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="d8642-115">\_limites de \_ \_ cota padrão do conjunto \_ de políticas</span><span class="sxs-lookup"><span data-stu-id="d8642-115">POLICY\_SET\_DEFAULT\_QUOTA\_LIMITS</span></span> | <span data-ttu-id="d8642-116">Defina as cotas de sistema padrão que são aplicadas a contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="d8642-116">Set the default system quotas that are applied to user accounts.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d8642-117">\_segredo de criação de política \_</span><span class="sxs-lookup"><span data-stu-id="d8642-117">POLICY\_CREATE\_SECRET</span></span>              | <span data-ttu-id="d8642-118">Esse tipo de acesso é necessário para criar um novo objeto de dados privado.</span><span class="sxs-lookup"><span data-stu-id="d8642-118">This access type is needed to create a new Private Data object.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d8642-119">\_criar \_ conta de política</span><span class="sxs-lookup"><span data-stu-id="d8642-119">POLICY\_CREATE\_ACCOUNT</span></span>             | <span data-ttu-id="d8642-120">Esse tipo de acesso é necessário para criar um novo objeto de [**conta**](account-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d8642-120">This access type is needed to create a new [**Account**](account-object.md) object.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d8642-121">\_requisitos de \_ auditoria do conjunto de políticas \_</span><span class="sxs-lookup"><span data-stu-id="d8642-121">POLICY\_SET\_AUDIT\_REQUIREMENTS</span></span>    | <span data-ttu-id="d8642-122">Esse tipo de acesso é necessário para atualizar os requisitos de auditoria do sistema.</span><span class="sxs-lookup"><span data-stu-id="d8642-122">This access type is needed to update the auditing requirements of the system.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d8642-123">\_administrador do \_ log de auditoria de política \_</span><span class="sxs-lookup"><span data-stu-id="d8642-123">POLICY\_AUDIT\_LOG\_ADMIN</span></span>           | <span data-ttu-id="d8642-124">Esse tipo de acesso é necessário para alterar as características da trilha de auditoria, como seu tamanho máximo ou o período de retenção para registros de auditoria, ou para limpar o log.</span><span class="sxs-lookup"><span data-stu-id="d8642-124">This access type is needed to change the characteristics of the audit trail such as its maximum size or the retention period for audit records, or to clear the log.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="d8642-125">\_informações de \_ auditoria de exibição de política \_</span><span class="sxs-lookup"><span data-stu-id="d8642-125">POLICY\_VIEW\_AUDIT\_INFORMATION</span></span>    | <span data-ttu-id="d8642-126">Esse tipo de acesso é necessário para exibir informações de requisitos de auditoria ou trilha de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d8642-126">This access type is needed to view audit trail or audit requirements information.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d8642-127">\_administrador do servidor de políticas \_</span><span class="sxs-lookup"><span data-stu-id="d8642-127">POLICY\_SERVER\_ADMIN</span></span>               | <span data-ttu-id="d8642-128">Esse tipo de acesso é necessário para modificar as informações de estado do servidor ou função (mestre/réplica).</span><span class="sxs-lookup"><span data-stu-id="d8642-128">This access type is needed to modify the server state or role (master/replica) information.</span></span> <span data-ttu-id="d8642-129">Também é necessário alterar as informações de origem e nome da conta da réplica.</span><span class="sxs-lookup"><span data-stu-id="d8642-129">It is also needed to change the replica source and account name information.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="d8642-130">\_nomes de pesquisa de política \_</span><span class="sxs-lookup"><span data-stu-id="d8642-130">POLICY\_LOOKUP\_NAMES</span></span>               | <span data-ttu-id="d8642-131">Esse tipo de acesso é necessário para a conversão entre nomes e SIDs.</span><span class="sxs-lookup"><span data-stu-id="d8642-131">This access type is needed to translate between names and SIDs.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d8642-132">\_privilégio de criação de política \_</span><span class="sxs-lookup"><span data-stu-id="d8642-132">POLICY\_CREATE\_PRIVILEGE</span></span>           | <span data-ttu-id="d8642-133">Ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="d8642-133">Not yet supported.</span></span>                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a><span data-ttu-id="d8642-134">Máscaras de acesso genérico</span><span class="sxs-lookup"><span data-stu-id="d8642-134">Generic Access Masks</span></span>

<span data-ttu-id="d8642-135">O objeto de [**política**](policy-object.md) publica os seguintes mapeamentos de tipos de acesso genéricos para tipos de acesso específicos:</span><span class="sxs-lookup"><span data-stu-id="d8642-135">The [**Policy**](policy-object.md) object publishes the following mappings from generic access types to specific access types:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a><span data-ttu-id="d8642-136">Tipos de acesso padrão</span><span class="sxs-lookup"><span data-stu-id="d8642-136">Standard Access Types</span></span>

<span data-ttu-id="d8642-137">Este objeto não dá suporte ao tipo de acesso padrão (opcional) SYNCHRONIZE.</span><span class="sxs-lookup"><span data-stu-id="d8642-137">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="d8642-138">Todos os tipos de acesso necessários têm suporte.</span><span class="sxs-lookup"><span data-stu-id="d8642-138">All required access types are supported.</span></span> <span data-ttu-id="d8642-139">A máscara de todos os tipos de acesso com suporte para esse tipo de objeto é:</span><span class="sxs-lookup"><span data-stu-id="d8642-139">The mask of all supported access types for this object type is:</span></span>

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 

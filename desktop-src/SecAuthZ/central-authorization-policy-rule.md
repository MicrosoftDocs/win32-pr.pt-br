---
description: A finalidade da regra de política de autorização central (CAPR) é fornecer uma definição de todo o domínio de um aspecto isolado da política de autorização de organizações.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Regra de política de autorização central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda6279b2bf28f80f99a0e2608b5bf209855a76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011870"
---
# <a name="central-authorization-policy-rule"></a><span data-ttu-id="8c21c-103">Regra de política de autorização central</span><span class="sxs-lookup"><span data-stu-id="8c21c-103">Central Authorization Policy Rule</span></span>

<span data-ttu-id="8c21c-104">A finalidade da regra de política de autorização central (CAPR) é fornecer uma definição de todo o domínio de um aspecto isolado da política de autorização da organização.</span><span class="sxs-lookup"><span data-stu-id="8c21c-104">The purpose of the Central Authorization Policy Rule (CAPR) is to provide a domain-wide definition of an isolated aspect of the organization's authorization policy.</span></span> <span data-ttu-id="8c21c-105">O administrador define o CAPR para impor um dos requisitos de autorização específicos.</span><span class="sxs-lookup"><span data-stu-id="8c21c-105">The administrator defines the CAPR to enforce one of the specific authorization requirements.</span></span> <span data-ttu-id="8c21c-106">Como o CAPR define apenas um requisito específico desejado da política de autorização, ele pode ser mais simplesmente definido e compreendido do que se todos os requisitos da diretiva de autorização da organização forem compilados em uma única definição de política.</span><span class="sxs-lookup"><span data-stu-id="8c21c-106">Since the CAPR defines only one specific desired requirement of the authorization policy it can be more simply defined and understood than if all the authorization policy requirements of the organization are compiled into a single policy definition.</span></span>

<span data-ttu-id="8c21c-107">O CAPR tem os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="8c21c-107">The CAPR has the following attributes:</span></span>

-   <span data-ttu-id="8c21c-108">Nome – identifica o CAPR para os administradores.</span><span class="sxs-lookup"><span data-stu-id="8c21c-108">Name – identifies the CAPR to the administrators.</span></span>
-   <span data-ttu-id="8c21c-109">Descrição – define a finalidade do CAPR e quaisquer informações que possam ser necessárias para os consumidores do CAPR.</span><span class="sxs-lookup"><span data-stu-id="8c21c-109">Description – defines the purpose of the CAPR and any information that may be needed by consumers of the CAPR.</span></span>
-   <span data-ttu-id="8c21c-110">Expressão de aplicabilidade – define os recursos ou situações em que a política será aplicada.</span><span class="sxs-lookup"><span data-stu-id="8c21c-110">Applicability Expression – defines the resources or situations in which the policy will be applied.</span></span>
-   <span data-ttu-id="8c21c-111">ID – identificador para uso na auditoria de alterações no CAPR.</span><span class="sxs-lookup"><span data-stu-id="8c21c-111">ID – identifier for use in auditing of changes to the CAPR.</span></span>
-   <span data-ttu-id="8c21c-112">Política de controle de acesso eficaz – um descritor de segurança do Windows que contém uma DACL que define a política de autorização efetiva.</span><span class="sxs-lookup"><span data-stu-id="8c21c-112">Effective Access Control Policy – a Windows security descriptor containing a DACL that defines the effective authorization policy.</span></span>
-   <span data-ttu-id="8c21c-113">Expressão de exceção – uma ou mais expressões que fornecem um meio de substituir a política e conceder acesso a uma entidade de segurança de acordo com a avaliação da expressão.</span><span class="sxs-lookup"><span data-stu-id="8c21c-113">Exception Expression – one or more expressions that provide a means to override the policy and grant access to a principal according to the evaluation of the expression.</span></span>
-   <span data-ttu-id="8c21c-114">Política de preparo – um descritor de segurança opcional do Windows que contém uma DACL que define uma política de autorização proposta (lista de entradas de controle de acesso) que será testada em relação à política efetiva, mas não imposta.</span><span class="sxs-lookup"><span data-stu-id="8c21c-114">Staging Policy – an optional Windows security descriptor containing a DACL that defines a proposed authorization policy (list of access control entries) that will be tested against the effective policy but not enforced.</span></span> <span data-ttu-id="8c21c-115">Se houver uma diferença entre os resultados da política efetiva e a política de preparo, a diferença será registrada no log de eventos de auditoria.</span><span class="sxs-lookup"><span data-stu-id="8c21c-115">If there is a difference between the results of the effective policy and the staging policy the difference will be recorded in the audit event log.</span></span>
    -   <span data-ttu-id="8c21c-116">Como o preparo pode ter um efeito imprevisível no desempenho do sistema, um administrador de Política de Grupo deve ser capaz de selecionar computadores específicos nos quais o preparo estará em vigor.</span><span class="sxs-lookup"><span data-stu-id="8c21c-116">Since staging can have an unpredictable effect on system performance, a Group Policy administrator must be able to select specific machines on which staging will be in effect.</span></span> <span data-ttu-id="8c21c-117">Isso permite que a política existente esteja em vigor na maioria das máquinas de uma UO enquanto o preparo está acontecendo em um subconjunto dos computadores.</span><span class="sxs-lookup"><span data-stu-id="8c21c-117">This allows the existing policy to be in place on most machines in an OU while staging is happening on a subset of the machines.</span></span>
    -   <span data-ttu-id="8c21c-118">P2 – um administrador local em um determinado computador deve ser capaz de desabilitar o preparo se o preparo nesse computador estiver causando muita degradação do desempenho.</span><span class="sxs-lookup"><span data-stu-id="8c21c-118">P2 – A local administrator on a particular machine should be able to disable staging if staging on that machine is causing too much of a performance degradation.</span></span>
-   <span data-ttu-id="8c21c-119">Backlink a CAP – uma lista de backlinks para qualquer CAPs que possa se referir a esse CAPR.</span><span class="sxs-lookup"><span data-stu-id="8c21c-119">Backlink to CAP – A list of backlinks to any CAPs that may be referring to this CAPR.</span></span>

<span data-ttu-id="8c21c-120">Durante a verificação de acesso, o CAPR é avaliado para aplicabilidade com base na expressão de aplicabilidade.</span><span class="sxs-lookup"><span data-stu-id="8c21c-120">During access check, the CAPR is be evaluated for applicability based on the applicability expression.</span></span> <span data-ttu-id="8c21c-121">Se um CAPR for aplicável, ele será avaliado para determinar se ele fornece ao usuário solicitante o acesso solicitado ao recurso identificado.</span><span class="sxs-lookup"><span data-stu-id="8c21c-121">If a CAPR is applicable, it is evaluated for whether it provides the requesting user the requested access to the identified resource.</span></span> <span data-ttu-id="8c21c-122">Os resultados da avaliação de CAPE são logicamente Unidos por **e** com os resultados da DACL no recurso e qualquer outro CAPRs aplicável em vigor no recurso.</span><span class="sxs-lookup"><span data-stu-id="8c21c-122">The results of the CAPE evaluation is then logically joined by **AND** with the results of the DACL on the resource and any other applicable CAPRs in effect on the resource.</span></span>

<span data-ttu-id="8c21c-123">Exemplo de CAPRs:</span><span class="sxs-lookup"><span data-stu-id="8c21c-123">Example CAPRs:</span></span>

``` syntax
[HBI-POLICY]
APPLIES-TO="(@resource.confidentiality == HBI"
SD ="D:(A;;FA;;;AU;(@memberOf("Smartcard Logon")))"
StagingSD = "D:(A;;FA;;;AU;(@memberOf("Smartcard Logon") AND memberOfAny(Resource.ProjectGroups)))"
description="Control access to sensitive information"
 
[RETENTION-POLICY]
Applies-To="@resource.retention == true"
SD ="D:(A;;;FA;;BA)(A;;FR;;;WD)"
description="If the document is marked for retention, then it is read-only for everyone however Local Admins have 
full control to them to put them out of retention when the time comes"
 
[TEST-FINANCE-POLICY]
Applies-To="@resource.label == 'finance'"
SD="D:(A;;FA;;;AU;(member_of(FinanceGroup))"
description="Department: Only employees of the finance department should be able to read documents labeled as finance"
```

## <a name="deny-aces-in-capes"></a><span data-ttu-id="8c21c-124">Negar ACEs em CAPEs</span><span class="sxs-lookup"><span data-stu-id="8c21c-124">Deny ACEs in CAPEs</span></span>

<span data-ttu-id="8c21c-125">No Windows 8, as ACEs Deny não terão suporte em um CAPR.</span><span class="sxs-lookup"><span data-stu-id="8c21c-125">In Windows 8 deny ACEs will not be supported in a CAPR.</span></span> <span data-ttu-id="8c21c-126">O UX de criação do CAPR não permitirá a criação de uma ACE Deny.</span><span class="sxs-lookup"><span data-stu-id="8c21c-126">The CAPR authoring UX will not allow creation of a deny ACE.</span></span> <span data-ttu-id="8c21c-127">Além disso, quando a LSA recupera o limite de Active Directory, a LSA verificará se nenhum CAPRs tem ACEs Deny.</span><span class="sxs-lookup"><span data-stu-id="8c21c-127">Additionally, when the LSA retrieves the CAP from Active Directory, LSA will verify that no CAPRs have deny ACEs.</span></span> <span data-ttu-id="8c21c-128">Se uma ACE Deny for encontrada em um CAPR, a CAP será tratada como inválida e não será copiada para o registro ou SRM.</span><span class="sxs-lookup"><span data-stu-id="8c21c-128">If a deny ACE is found in a CAPR then the CAP will be treated as invalid and not be copied to the registry or SRM.</span></span>

> [!Note]  
> <span data-ttu-id="8c21c-129">A verificação de acesso não impedirá que nenhuma Ace Deny esteja presente.</span><span class="sxs-lookup"><span data-stu-id="8c21c-129">The access check will not enforce that no deny ACEs are present.</span></span> <span data-ttu-id="8c21c-130">As ACEs Deny em um CAPR serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="8c21c-130">Deny ACEs in a CAPR will be applied.</span></span> <span data-ttu-id="8c21c-131">Espera-se que as ferramentas de criação impeçam que isso aconteça.</span><span class="sxs-lookup"><span data-stu-id="8c21c-131">It is expected that authoring tools will prevent this from happening.</span></span>

 

## <a name="cape-definition"></a><span data-ttu-id="8c21c-132">Definição de cabo</span><span class="sxs-lookup"><span data-stu-id="8c21c-132">CAPE Definition</span></span>

<span data-ttu-id="8c21c-133">CAPRs são criados por meio de uma nova UX fornecida no Centro Administrativo do Active Directory (ADAC.) No ADAC, uma opção de nova tarefa é fornecida para criar um CAPR.</span><span class="sxs-lookup"><span data-stu-id="8c21c-133">CAPRs are created though a new UX provided in Active Directory Administrative Center (ADAC.) In ADAC a new task option is provided to create a CAPR.</span></span> <span data-ttu-id="8c21c-134">Quando essa tarefa for selecionada, o ADAC solicitará ao usuário uma caixa de diálogo solicitando ao usuário um nome de CAPR e uma descrição.</span><span class="sxs-lookup"><span data-stu-id="8c21c-134">When this task is selected, ADAC will prompt the user with a dialog asking the user for a CAPR name and a description.</span></span> <span data-ttu-id="8c21c-135">Quando eles são fornecidos, os controles para definir qualquer um dos elementos CAPR restantes são habilitados.</span><span class="sxs-lookup"><span data-stu-id="8c21c-135">When these are provided, the controls to define any of the remaining CAPR elements become enabled.</span></span> <span data-ttu-id="8c21c-136">Para cada um dos elementos CAPR restantes, o UX chamará a interface do usuário ACL para permitir a definição de expressões e/ou ACLs.</span><span class="sxs-lookup"><span data-stu-id="8c21c-136">For each of the remaining CAPR elements, the UX will call out to the ACL-UI to allow definition of expression and/or ACLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c21c-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c21c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c21c-138">**AccessCheck**</span><span class="sxs-lookup"><span data-stu-id="8c21c-138">**AccessCheck**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[<span data-ttu-id="8c21c-139">Cenário de controle de acesso dinâmico (DAC)</span><span class="sxs-lookup"><span data-stu-id="8c21c-139">Dynamic Access Control (DAC) scenario</span></span>](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 

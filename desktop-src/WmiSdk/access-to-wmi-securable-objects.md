---
description: O WMI conta com os descritores de segurança padrão do Windows para controlar e proteger o acesso a objetos protegíveis, como namespaces, impressoras, serviços e aplicativos DCOM do WMI.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Acesso a objetos protegíveis do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171460"
---
# <a name="access-to-wmi-securable-objects"></a><span data-ttu-id="03be0-103">Acesso a objetos protegíveis do WMI</span><span class="sxs-lookup"><span data-stu-id="03be0-103">Access to WMI Securable Objects</span></span>

<span data-ttu-id="03be0-104">O WMI conta com os [*descritores de segurança*](/windows/desktop/SecGloss/s-gly) padrão do Windows para controlar e proteger o acesso a objetos protegíveis, como namespaces, impressoras, serviços e aplicativos DCOM do WMI.</span><span class="sxs-lookup"><span data-stu-id="03be0-104">WMI relies on standard Windows [*security descriptors*](/windows/desktop/SecGloss/s-gly) to control and protect access to securable objects like WMI namespaces, printers, services, and DCOM applications.</span></span> <span data-ttu-id="03be0-105">Para obter mais informações, consulte [Access to WMI namespaces](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="03be0-105">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="03be0-106">Os seguintes tópicos são discutidos nesta seção:</span><span class="sxs-lookup"><span data-stu-id="03be0-106">The following topics are discussed in this section:</span></span>

-   [<span data-ttu-id="03be0-107">Descritores de segurança e SIDs</span><span class="sxs-lookup"><span data-stu-id="03be0-107">Security Descriptors and SIDs</span></span>](#security-descriptors-and-sids)
-   [<span data-ttu-id="03be0-108">Controle de acesso</span><span class="sxs-lookup"><span data-stu-id="03be0-108">Access Control</span></span>](#access-control)
-   [<span data-ttu-id="03be0-109">Alterando a segurança de acesso</span><span class="sxs-lookup"><span data-stu-id="03be0-109">Changing Access Security</span></span>](#changing-access-security)
-   [<span data-ttu-id="03be0-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03be0-110">Related topics</span></span>](#related-topics)

## <a name="security-descriptors-and-sids"></a><span data-ttu-id="03be0-111">Descritores de segurança e SIDs</span><span class="sxs-lookup"><span data-stu-id="03be0-111">Security Descriptors and SIDs</span></span>

<span data-ttu-id="03be0-112">O WMI mantém a segurança de acesso comparando o [*token de acesso*](/windows/desktop/SecGloss/a-gly) do usuário que tenta acessar um objeto protegível com o descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="03be0-112">WMI maintains access security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user that attempts to access a securable object with the security descriptor of the object.</span></span>

<span data-ttu-id="03be0-113">Quando um usuário ou grupo é criado em um sistema, a conta recebe um [*Sid (identificador de segurança)*](/windows/desktop/SecGloss/s-gly) . o Sid garante que uma conta criada com o mesmo nome que uma conta excluída anteriormente não herde as configurações de segurança anteriores.</span><span class="sxs-lookup"><span data-stu-id="03be0-113">When a user or group is created on a system, the account is given a [*security identifier (SID)*](/windows/desktop/SecGloss/s-gly) The SID ensures that an account created with the same name as a previously deleted account does not inherit the previous security settings.</span></span> <span data-ttu-id="03be0-114">Um token de acesso é criado pela combinação do SID, a lista de grupos dos quais o usuário é membro e a lista de privilégios habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="03be0-114">An access token is created by combining the SID, the list of groups of which the user is a member, and the list of enabled or disabled privileges.</span></span> <span data-ttu-id="03be0-115">Esses tokens são atribuídos a todos os processos e threads pertencentes ao usuário.</span><span class="sxs-lookup"><span data-stu-id="03be0-115">These tokens are assigned to all processes and threads owned by the user.</span></span>

## <a name="access-control"></a><span data-ttu-id="03be0-116">Controle de acesso</span><span class="sxs-lookup"><span data-stu-id="03be0-116">Access Control</span></span>

<span data-ttu-id="03be0-117">Quando o usuário quiser usar um objeto protegido, o token de acesso será comparado com a [*DACL (lista de controle de acesso discricionário)*](/windows/desktop/SecGloss/d-gly) no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="03be0-117">When the user wants to use a secured object, the access token is compared with the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) in the security descriptor on the object.</span></span> <span data-ttu-id="03be0-118">A DACL contém permissões chamadas [*de ACE (entradas de controle de acesso)*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="03be0-118">The DACL contains permissions called [*access control entries (ACE)*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="03be0-119">As [*listas de controle de acesso do sistema (SACL)*](/windows/desktop/SecGloss/s-gly) fazem a mesma coisa que as DACLs, mas podem gerar eventos de auditoria de segurança.</span><span class="sxs-lookup"><span data-stu-id="03be0-119">[*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) do the same thing as DACLs, but can generate security audit events.</span></span> <span data-ttu-id="03be0-120">A partir do Windows Vista, o WMI pode fazer entradas de auditoria no log de segurança do Windows.</span><span class="sxs-lookup"><span data-stu-id="03be0-120">Starting with Windows Vista, WMI can make auditing entries in the Windows Security Log.</span></span> <span data-ttu-id="03be0-121">Para obter mais informações sobre auditoria no WMI, consulte [acesso aos namespaces do WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="03be0-121">For more information about auditing in WMI, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="03be0-122">A DACL e a SACL consistem em uma lista de ACEs que descrevem quais usuários têm direitos de acesso específicos, incluindo gravação no repositório WMI, acesso remoto e execução e permissões de logon.</span><span class="sxs-lookup"><span data-stu-id="03be0-122">Both the DACL and the SACL consist of a list of ACEs that describe which users have specific access rights, including writing to the WMI repository, remote access and execution, and logon permissions.</span></span> <span data-ttu-id="03be0-123">O WMI armazena essas ACLs no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="03be0-123">WMI stores these ACLs in the WMI repository.</span></span>

<span data-ttu-id="03be0-124">As ACEs contêm três tipos de níveis de acesso ou concedem/negam direitos: permitir, negar para DACL e auditoria do sistema (para SACLs).</span><span class="sxs-lookup"><span data-stu-id="03be0-124">ACEs hold three types of access levels or grant/deny rights: allow, deny for DACL, and system audit (for SACLs).</span></span> <span data-ttu-id="03be0-125">Deny ACEs precedem permitir ACEs na DACL ou SACL.</span><span class="sxs-lookup"><span data-stu-id="03be0-125">Deny ACEs precede allow ACEs in the DACL or SACL.</span></span> <span data-ttu-id="03be0-126">Ao verificar os direitos de acesso do usuário, o WMI é executado consecutivamente por meio da lista de controle de acesso até encontrar uma ACE allow que se aplique ao token de acesso solicitante.</span><span class="sxs-lookup"><span data-stu-id="03be0-126">When checking the user access rights, WMI runs consecutively through the access control list until it finds an allow ACE that applies to the requesting access token.</span></span> <span data-ttu-id="03be0-127">As ACEs restantes não são verificadas após esse ponto.</span><span class="sxs-lookup"><span data-stu-id="03be0-127">The remaining ACEs are not checked after this point.</span></span> <span data-ttu-id="03be0-128">Se nenhum ACE de permissão apropriado for encontrado, o acesso será negado.</span><span class="sxs-lookup"><span data-stu-id="03be0-128">If no appropriate allow ACE is found, then access is denied.</span></span> <span data-ttu-id="03be0-129">Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) e [criando uma DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="03be0-129">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) and [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

## <a name="changing-access-security"></a><span data-ttu-id="03be0-130">Alterando a segurança de acesso</span><span class="sxs-lookup"><span data-stu-id="03be0-130">Changing Access Security</span></span>

<span data-ttu-id="03be0-131">Com as permissões apropriadas, você pode alterar a segurança em um objeto protegível com um script ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="03be0-131">With appropriate permissions, you can change the security on a securable object with a script or application.</span></span> <span data-ttu-id="03be0-132">Você também pode alterar as configurações de segurança nos namespaces do WMI usando o [*controle WMI*](gloss-w.md) ou adicionando uma cadeia de caracteres [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) no arquivo [*formato MOF (MOF)*](gloss-m.md) que define classes para o namespace.</span><span class="sxs-lookup"><span data-stu-id="03be0-132">You can also change the security settings on WMI namespaces using the [*WMI Control*](gloss-w.md) or by adding a [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) string in the [*Managed Object Format (MOF)*](gloss-m.md) file that defines classes for the namespace.</span></span> <span data-ttu-id="03be0-133">Para obter mais informações, consulte [acesso a namespaces do WMI](access-to-wmi-namespaces.md), [proteção de namespaces do WMI](securing-wmi-namespaces.md)e [alteração da segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="03be0-133">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md), [Securing WMI Namespaces](securing-wmi-namespaces.md), and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03be0-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03be0-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03be0-135">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="03be0-135">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="03be0-136">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="03be0-136">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="03be0-137">Controle de conta de usuário e WMI</span><span class="sxs-lookup"><span data-stu-id="03be0-137">User Account Control and WMI</span></span>](user-account-control-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="03be0-138">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="03be0-138">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="03be0-139">Acesso a namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="03be0-139">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 

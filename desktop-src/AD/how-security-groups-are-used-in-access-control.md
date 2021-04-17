---
title: Como os grupos de segurança são usados no controle de acesso
description: O SID (identificador de segurança) é o identificador de objeto do usuário ou grupo de segurança quando o usuário ou grupo é usado para fins de segurança.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Como os grupos de segurança são usados no controle de acesso
- controle de acesso, grupos de segurança usados em
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753039"
---
# <a name="how-security-groups-are-used-in-access-control"></a><span data-ttu-id="330ad-105">Como os grupos de segurança são usados no controle de acesso</span><span class="sxs-lookup"><span data-stu-id="330ad-105">How Security Groups are Used in Access Control</span></span>

<span data-ttu-id="330ad-106">O SID (identificador de segurança) é o identificador de objeto do usuário ou grupo de segurança quando o usuário ou grupo é usado para fins de segurança.</span><span class="sxs-lookup"><span data-stu-id="330ad-106">The security identifier (SID) is the object identifier of the user or security group when the user or group is used for security purposes.</span></span> <span data-ttu-id="330ad-107">O nome do usuário ou grupo não é usado como o identificador exclusivo no sistema.</span><span class="sxs-lookup"><span data-stu-id="330ad-107">The name of the user or group is not used as the unique identifier within the system.</span></span> <span data-ttu-id="330ad-108">O SID é armazenado no atributo **objectSid** de objetos de usuário e objetos de grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="330ad-108">The SID is stored in the **objectSid** attribute of user objects and security group objects.</span></span> <span data-ttu-id="330ad-109">O servidor de Active Directory gera o **objectSid** quando o usuário ou grupo é criado.</span><span class="sxs-lookup"><span data-stu-id="330ad-109">The Active Directory server generates the **objectSid** when the user or group is created.</span></span> <span data-ttu-id="330ad-110">O sistema garante que os SIDs sejam exclusivos em uma floresta.</span><span class="sxs-lookup"><span data-stu-id="330ad-110">The system ensures that the SIDs are unique across a forest.</span></span> <span data-ttu-id="330ad-111">Lembre-se de que **objectGUID** é o identificador exclusivo de um usuário, grupo ou qualquer outro objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="330ad-111">Be aware that the **objectGuid** is the unique identifier of a user, group, or any other directory object.</span></span> <span data-ttu-id="330ad-112">O SID será alterado se um usuário ou grupo for movido para outro domínio; o **objectGUID** permanece o mesmo.</span><span class="sxs-lookup"><span data-stu-id="330ad-112">The SID changes if a user or group is moved to another domain; the **objectGuid** remains the same.</span></span>

<span data-ttu-id="330ad-113">Quando um usuário ou grupo recebe permissão para acessar um recurso, como uma impressora ou um compartilhamento de arquivos, o SID do usuário ou grupo é adicionado à ACE (entrada de controle de acesso) que define a permissão concedida na DACL (lista de controle de acesso discricionário) do recurso.</span><span class="sxs-lookup"><span data-stu-id="330ad-113">When a user or group is given permission to access a resource, such as a printer or a file share, the SID of the user or group is added to the access control entry (ACE) defining the granted permission in the resource's discretionary access control list (DACL).</span></span> <span data-ttu-id="330ad-114">Em Active Directory Domain Services, cada objeto tem um atributo **nTSecurityDescriptor** que armazena uma DACL definindo o acesso a esse objeto ou atributos específicos nesse objeto.</span><span class="sxs-lookup"><span data-stu-id="330ad-114">In Active Directory Domain Services, each object has an **nTSecurityDescriptor** attribute that stores a DACL defining the access to that particular object or attributes on that object.</span></span> <span data-ttu-id="330ad-115">Para obter mais informações sobre como definir o controle de acesso em objetos no Active Directory Domain Services, consulte [controlando o acesso a objetos no Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="330ad-115">For more information about setting access control on objects in Active Directory Domain Services, see [Controlling Access to Objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="330ad-116">Quando um usuário faz logon em um domínio do Windows 2000, o sistema operacional gera um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="330ad-116">When a user logs on to a Windows 2000 domain, the operating system generates an access token.</span></span> <span data-ttu-id="330ad-117">Esse token de acesso é usado para determinar quais recursos o usuário pode acessar.</span><span class="sxs-lookup"><span data-stu-id="330ad-117">This access token is used to determine which resources the user may access.</span></span> <span data-ttu-id="330ad-118">O token de acesso do usuário inclui os seguintes dados:</span><span class="sxs-lookup"><span data-stu-id="330ad-118">The user access token includes the following data:</span></span>

-   <span data-ttu-id="330ad-119">SID do usuário.</span><span class="sxs-lookup"><span data-stu-id="330ad-119">User SID.</span></span>
-   <span data-ttu-id="330ad-120">SIDs de todos os grupos de segurança globais e universais dos quais o usuário é membro.</span><span class="sxs-lookup"><span data-stu-id="330ad-120">SIDs of all global and universal security groups that the user is a member of.</span></span>
-   <span data-ttu-id="330ad-121">SIDs de todos os grupos de segurança global e universal aninhados.</span><span class="sxs-lookup"><span data-stu-id="330ad-121">SIDs of all nested global and universal security groups.</span></span>

<span data-ttu-id="330ad-122">Cada processo executado em nome desse usuário tem uma cópia desse token de acesso.</span><span class="sxs-lookup"><span data-stu-id="330ad-122">Every process executed on behalf of this user has a copy of this access token.</span></span>

<span data-ttu-id="330ad-123">Quando o usuário tenta acessar recursos em um computador, o serviço pelo qual o usuário acessa o recurso representará o usuário criando um novo token de acesso com base no token de acesso criado no momento do logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="330ad-123">When the user attempts to access resources on a computer, the service through which the user accesses the resource will impersonate the user by creating a new access token based on the access token created at user logon time.</span></span> <span data-ttu-id="330ad-124">Esse novo token de acesso também conterá os seguintes SIDs:</span><span class="sxs-lookup"><span data-stu-id="330ad-124">This new access token will also contain the following SIDs:</span></span>

-   <span data-ttu-id="330ad-125">SIDs para todos os grupos locais de domínio no domínio de destino do qual o usuário é membro.</span><span class="sxs-lookup"><span data-stu-id="330ad-125">SIDs for all domain local groups in the target domain that the user is a member of.</span></span>
-   <span data-ttu-id="330ad-126">SIDs para todos os grupos locais de computador no computador de destino do qual o usuário é membro.</span><span class="sxs-lookup"><span data-stu-id="330ad-126">SIDs for all machine local groups on the target computer that the user is a member of.</span></span>

<span data-ttu-id="330ad-127">O serviço usa esse novo token de acesso para avaliar o acesso ao recurso.</span><span class="sxs-lookup"><span data-stu-id="330ad-127">The service uses this new access token to evaluate access to the resource.</span></span> <span data-ttu-id="330ad-128">Se um SID no token de acesso aparecer em quaisquer ACEs na DACL, o serviço fornecerá ao usuário as permissões especificadas nessas ACEs.</span><span class="sxs-lookup"><span data-stu-id="330ad-128">If a SID in the access token appears in any ACEs in the DACL, the service gives the user the permissions specified in those ACEs.</span></span>

 

 





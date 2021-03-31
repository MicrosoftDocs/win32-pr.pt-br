---
title: Criando um novo grupo
description: Joe Worden, administrador corporativo, deve criar um novo grupo.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a4f46d595aa892ac75aa67d14bbc0356122271
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917684"
---
# <a name="creating-a-new-group"></a><span data-ttu-id="1e8c0-103">Criando um novo grupo</span><span class="sxs-lookup"><span data-stu-id="1e8c0-103">Creating a New Group</span></span>

<span data-ttu-id="1e8c0-104">Joe Worden, administrador corporativo, deve criar um novo grupo.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-104">Joe Worden, the enterprise administrator, must create a new group.</span></span> <span data-ttu-id="1e8c0-105">Ele gostaria de proteger alguns recursos, como arquivos, Active Directory objetos ou outros objetos, com base na associação desse grupo.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-105">He would like to secure some resources, such as file, Active Directory objects, or other objects, based on the membership of this group.</span></span> <span data-ttu-id="1e8c0-106">O exemplo de código a seguir mostra como criar um novo grupo.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-106">The following code example shows how to create a new group.</span></span>


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



<span data-ttu-id="1e8c0-107">Esse grupo, gerenciamento, será criado na unidade organizacional Sales.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-107">This group, Management, will be created in the Sales organizational unit.</span></span> <span data-ttu-id="1e8c0-108">Primeiro, Joe deve criar um objeto ADSI para a unidade organizacional Sales.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-108">First, Joe must create an ADSI object for the Sales organizational unit.</span></span> <span data-ttu-id="1e8c0-109">Em segundo lugar, ele deve definir o atributo [**sAMAccountName**](/windows/desktop/AD/group-objects) nesse objeto, pois é um atributo obrigatório para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-109">Second, he must set the [**samAccountName**](/windows/desktop/AD/group-objects) attribute on this object, because it is a mandatory attribute for backward compatibility.</span></span> <span data-ttu-id="1e8c0-110">Para este exemplo, quando **sAMAccountName** é definido, as ferramentas do Windows NT 4,0, como o Gerenciador de usuários, confiram o atributo **como gerenciamento, em vez** de **gerenciar**.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-110">For this example, when **samAccountName** is set, Windows NT 4.0 tools such as User Manager see the attribute as **mgmt** instead of **Management**.</span></span>

<span data-ttu-id="1e8c0-111">Terceiro, Joe deve especificar o tipo de grupo.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-111">Third, Joe must specify the type of group.</span></span> <span data-ttu-id="1e8c0-112">Em um domínio do Windows 2000, há três tipos de grupos: global, domínio local e universal.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-112">In a Windows 2000 domain, there are three types of groups: Global, Domain Local, and Universal.</span></span> <span data-ttu-id="1e8c0-113">Além disso, o grupo transporta sua característica de segurança.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-113">In addition, the group carries its security characteristic.</span></span> <span data-ttu-id="1e8c0-114">Um grupo pode ser um grupo habilitado para segurança ou não protegido.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-114">A group can be either a security-enabled or a non-secured group.</span></span> <span data-ttu-id="1e8c0-115">Essencialmente, os grupos habilitados para segurança são aqueles que podem ter direitos de acesso concedidos ou negados a recursos, semelhantes a um usuário.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-115">Essentially, security-enabled groups are those that can be granted or denied access rights to resources, similar to a user.</span></span> <span data-ttu-id="1e8c0-116">A concessão de um acesso de grupo a um compartilhamento de arquivos, por exemplo, implica que todos os membros do grupo podem acessar o compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-116">Granting a group access to a file share, for example, implies that all members of the group can access the file share.</span></span> <span data-ttu-id="1e8c0-117">As listas de distribuição não podem ser usadas de maneira semelhante — você não pode, por exemplo, conceder a uma lista de distribuição o direito de acessar um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-117">Distribution lists cannot be used in a similar manner—you cannot, for example, grant a distribution list the right to access a file share.</span></span> <span data-ttu-id="1e8c0-118">Durante a atualização, os grupos do Windows NT 4,0 são migrados como grupos habilitados para segurança.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-118">During the upgrade, Windows NT 4.0 groups are migrated as security-enabled groups.</span></span> <span data-ttu-id="1e8c0-119">Os grupos não protegidos no Active Directory são semelhantes às listas de distribuição no Exchange.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-119">Non-secured groups in Active Directory are similar to distribution lists in Exchange.</span></span> <span data-ttu-id="1e8c0-120">Portanto, a criação de grupos ou listas de distribuição são operações semelhantes no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-120">Hence, creating groups or distribution lists are similar operations in Windows 2000.</span></span> <span data-ttu-id="1e8c0-121">No modo nativo do Windows 2000 (modo nativo significa que todos os controladores de domínio em um domínio são computadores que executam o Windows 2000 Server), os grupos podem ser aninhados em qualquer nível.</span><span class="sxs-lookup"><span data-stu-id="1e8c0-121">In the Windows 2000 native mode (native mode means that all domain controllers in a domain are computers running Windows 2000 Server), the groups can be nested to any level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e8c0-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e8c0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e8c0-123">Enumerando objetos</span><span class="sxs-lookup"><span data-stu-id="1e8c0-123">Enumerating Objects</span></span>](enumerating-objects.md)
</dt> </dl>

 

 
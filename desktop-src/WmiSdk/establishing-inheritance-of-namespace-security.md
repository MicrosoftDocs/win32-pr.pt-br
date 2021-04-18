---
description: Você pode controlar se um namespace filho herda o descritor de segurança do namespace pai.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Estabelecendo a herança da segurança do namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796177"
---
# <a name="establishing-inheritance-of-namespace-security"></a><span data-ttu-id="60830-103">Estabelecendo a herança da segurança do namespace</span><span class="sxs-lookup"><span data-stu-id="60830-103">Establishing Inheritance of Namespace Security</span></span>

<span data-ttu-id="60830-104">Você pode controlar se um namespace filho herda o descritor de segurança do namespace pai.</span><span class="sxs-lookup"><span data-stu-id="60830-104">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

<span data-ttu-id="60830-105">Os namespaces WMI têm descritores de segurança que controlam quem pode acessar o namespace e os dados do namespace.</span><span class="sxs-lookup"><span data-stu-id="60830-105">WMI namespaces have security descriptors that control who can access the namespace and the data of the namespace.</span></span> <span data-ttu-id="60830-106">Cada descritor de segurança tem uma DACL (lista de controle de acesso discricionário) e uma SACL (lista de controle de acesso de segurança).</span><span class="sxs-lookup"><span data-stu-id="60830-106">Each security descriptor has a discretionary access control list (DACL) and a security access control list (SACL).</span></span> <span data-ttu-id="60830-107">Essas listas contêm entradas de controle de acesso (ACE).</span><span class="sxs-lookup"><span data-stu-id="60830-107">These lists contain access control entries (ACE).</span></span>

<span data-ttu-id="60830-108">Dependendo das constantes do [**sinalizador Ace do namespace**](namespace-ace-flag-constants.md) que são definidas, as permissões que são aplicadas a um namespace podem ser herdadas por todos os namespaces filho desse namespace.</span><span class="sxs-lookup"><span data-stu-id="60830-108">Depending on the [**Namespace ACE Flag Constants**](namespace-ace-flag-constants.md) that are set, permissions that are applied to a namespace may be inherited by all the child namespaces of that namespace.</span></span> <span data-ttu-id="60830-109">Um namespace filho herda o descritor de segurança de seu namespace pai quando o namespace filho é criado se o **contêiner \_ herdar \_** o sinalizador Ace está no descritor de segurança do namespace pai.</span><span class="sxs-lookup"><span data-stu-id="60830-109">A child namespace inherits the security descriptor of its parent namespace when the child namespace is created if the **CONTAINER\_INHERIT\_ACE** flag is in the parent namespace security descriptor.</span></span> <span data-ttu-id="60830-110">Se **contêiner \_ herdar Ace \_ \| não \_ se propagar \_ herdar \_ Ace** está definido, somente o namespace filho herdará o descritor de segurança, não os namespaces do neto.</span><span class="sxs-lookup"><span data-stu-id="60830-110">If **CONTAINER\_INHERIT\_ACE\|NO\_PROPOGATE\_INHERIT\_ACE** is set, then only the child namespace inherits the security descriptor, not grandchild namespaces.</span></span> <span data-ttu-id="60830-111">Os namespaces filho podem substituir as permissões de segurança de seu pai chamando métodos da classe [**\_ \_ SystemSecurity**](--systemsecurity.md) para gravar um novo descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="60830-111">Child namespaces can override the security permissions of their parent by calling methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class to write a new security descriptor.</span></span> <span data-ttu-id="60830-112">As configurações de segurança padrão não podem ser alteradas.</span><span class="sxs-lookup"><span data-stu-id="60830-112">The default security settings cannot be changed.</span></span> <span data-ttu-id="60830-113">Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md). Para obter mais informações sobre DACLs, consulte as constantes [ACLs (listas de controle de acesso)](/windows/desktop/SecAuthZ/access-control-lists) e [**tipo de ACE de namespace**](namespace-ace-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="60830-113">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).For more information about DACLs, see [Access Control Lists (ACL)](/windows/desktop/SecAuthZ/access-control-lists) and [**Namespace ACE Type Constants**](namespace-ace-type-constants.md).</span></span>

<span data-ttu-id="60830-114">Observe que as permissões padrão não podem ser alteradas.</span><span class="sxs-lookup"><span data-stu-id="60830-114">Note that the default permissions cannot be changed.</span></span> <span data-ttu-id="60830-115">Além disso, a configuração do sinalizador **se \_ \_ protegido por DACL** ao definir o descritor de segurança (SD) não é usada para adicionar um SD especializado a um namespace filho.</span><span class="sxs-lookup"><span data-stu-id="60830-115">Furthermore, setting the **SE\_DACL\_PROTECTED** flag while setting the security descriptor (SD) is not used to add a specialized SD to a child namespace.</span></span> <span data-ttu-id="60830-116">Para substituir um SD herdado, basta definir um novo.</span><span class="sxs-lookup"><span data-stu-id="60830-116">To override an inherited SD, simply set a new one.</span></span> <span data-ttu-id="60830-117">Para herdar o SD para um namespace filho, passe o sinalizador **\_ \_ Ace Inherit do contêiner** no descritor de segurança do namespace.</span><span class="sxs-lookup"><span data-stu-id="60830-117">To inherit that SD to a child namespace, pass the **CONTAINER\_INHERIT\_ACE** flag in the namespace security descriptor.</span></span> <span data-ttu-id="60830-118">Para herdar apenas o filho, e não os descendentes, passe `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span><span class="sxs-lookup"><span data-stu-id="60830-118">To inherit to just the child, and not the descendants, pass `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span></span>

<span data-ttu-id="60830-119">.</span><span class="sxs-lookup"><span data-stu-id="60830-119">.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60830-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60830-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60830-121">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="60830-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="60830-122">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="60830-122">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 

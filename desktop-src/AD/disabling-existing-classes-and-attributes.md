---
title: Desabilitando classes e atributos existentes
description: Adições de esquema são permanentes.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634973"
---
# <a name="disabling-existing-classes-and-attributes"></a><span data-ttu-id="27211-103">Desabilitando classes e atributos existentes</span><span class="sxs-lookup"><span data-stu-id="27211-103">Disabling Existing Classes and Attributes</span></span>

<span data-ttu-id="27211-104">Adições de esquema são permanentes.</span><span class="sxs-lookup"><span data-stu-id="27211-104">Schema additions are permanent.</span></span> <span data-ttu-id="27211-105">Não é possível excluir objetos **attributeSchema** e **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="27211-105">You cannot delete **attributeSchema** and **classSchema** objects.</span></span> <span data-ttu-id="27211-106">Em um sistema distribuído, é difícil garantir que não haja nenhuma instância de uma determinada classe ou atributo.</span><span class="sxs-lookup"><span data-stu-id="27211-106">In a distributed system, it is difficult to guarantee that there are no instances of a given class or attribute.</span></span> <span data-ttu-id="27211-107">A remoção da definição de uma classe ou atributo danifica as instâncias existentes dessa classe ou atributo.</span><span class="sxs-lookup"><span data-stu-id="27211-107">Removing the definition of a class or attribute damages existing instances of that class or attribute.</span></span>

<span data-ttu-id="27211-108">Você pode desabilitar uma classe ou atributo existente marcando-o como "extinto".</span><span class="sxs-lookup"><span data-stu-id="27211-108">You can disable an existing class or attribute by marking it as "defunct".</span></span> <span data-ttu-id="27211-109">Isso não afeta as instâncias existentes da classe ou do atributo, portanto marcado, mas impede a criação de novas instâncias.</span><span class="sxs-lookup"><span data-stu-id="27211-109">This does not affect existing instances of the class or attribute so marked, but it prevents the creation of new instances.</span></span>

<span data-ttu-id="27211-110">As seguintes restrições se aplicam ao desabilitar classes e atributos de esquema:</span><span class="sxs-lookup"><span data-stu-id="27211-110">The following restrictions apply when disabling schema classes and attributes:</span></span>

-   <span data-ttu-id="27211-111">Não é possível desabilitar uma classe ou atributo de categoria 1.</span><span class="sxs-lookup"><span data-stu-id="27211-111">You cannot disable a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="27211-112">Não é possível desabilitar um atributo que seja membro de uma classe que não esteja desabilitada também.</span><span class="sxs-lookup"><span data-stu-id="27211-112">You cannot disable an attribute that is a member of a class that is not also disabled.</span></span> <span data-ttu-id="27211-113">Isso ocorre porque um atributo pode ser necessário para a classe (não desabilitada) e a desabilitação do atributo impede que novas instâncias da classe sejam criadas.</span><span class="sxs-lookup"><span data-stu-id="27211-113">This is because an attribute might be required for the (not disabled) class, and disabling the attribute prevents new instances of the class from being created.</span></span>

<span data-ttu-id="27211-114">Para desabilitar um atributo, defina o atributo **Isfuncde** de seu objeto **attributeSchema** como **true**.</span><span class="sxs-lookup"><span data-stu-id="27211-114">To disable an attribute, set the **isDefunct** attribute of its **attributeSchema** object to **TRUE**.</span></span> <span data-ttu-id="27211-115">Quando um atributo é desabilitado, não é possível criar novas instâncias do atributo.</span><span class="sxs-lookup"><span data-stu-id="27211-115">When an attribute is disabled, new instances of the attribute cannot be created.</span></span> <span data-ttu-id="27211-116">Para reabilitar o atributo, defina o atributo **isextinto** como **false**.</span><span class="sxs-lookup"><span data-stu-id="27211-116">To re-enable the attribute set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="27211-117">Para desabilitar uma classe, defina o atributo **Isfuncde** de seu objeto **classSchema** como **true**.</span><span class="sxs-lookup"><span data-stu-id="27211-117">To disable a class, set the **isDefunct** attribute of its **classSchema** object to **TRUE**.</span></span> <span data-ttu-id="27211-118">Quando uma classe é desabilitada, novas instâncias da classe não podem ser criadas.</span><span class="sxs-lookup"><span data-stu-id="27211-118">When a class is disabled, new instances of the class cannot be created.</span></span> <span data-ttu-id="27211-119">Para reabilitar a classe, defina o atributo **isextinto** como **false**.</span><span class="sxs-lookup"><span data-stu-id="27211-119">To re-enable the class set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="27211-120">Definir objetos de esquema como extintos pode ser útil em ambientes de produção.</span><span class="sxs-lookup"><span data-stu-id="27211-120">Setting schema objects as defunct can be useful in production environments.</span></span> <span data-ttu-id="27211-121">Quando uma versão de teste de uma extensão de esquema não for mais necessária, marque-a como expirada.</span><span class="sxs-lookup"><span data-stu-id="27211-121">When a test version of a schema extension is no longer required, mark it as defunct.</span></span> <span data-ttu-id="27211-122">Você pode restaurá-lo removendo o atributo **Isfunct** ou definindo o valor do atributo como **false**.</span><span class="sxs-lookup"><span data-stu-id="27211-122">You can restore it by removing the **isDefunct** attribute or setting the attribute value to **FALSE**.</span></span> <span data-ttu-id="27211-123">Isso também protege contra uma remoção não intencional de um objeto de esquema definindo-o como extinto porque a operação pode ser facilmente revertida.</span><span class="sxs-lookup"><span data-stu-id="27211-123">This also protects against an unintended removal of a schema object by setting it to defunct because the operation can be easily reversed.</span></span>

<span data-ttu-id="27211-124">Lembre-se de que o servidor de Active Directory não limpa as instâncias existentes de um atributo ou classe quando você torna um objeto de esquema extinto.</span><span class="sxs-lookup"><span data-stu-id="27211-124">Be aware that the Active Directory server does not clean up existing instances of an attribute or class when you make a schema object defunct.</span></span> <span data-ttu-id="27211-125">Se você remover a propriedade **Isfuncde** , todas as instâncias se tornarão objetos normais válidos novamente.</span><span class="sxs-lookup"><span data-stu-id="27211-125">If you remove the **isDefunct** property, any instances become valid, normal objects again.</span></span>

<span data-ttu-id="27211-126">A lista a seguir inclui outras consequências de marcar um objeto **attributeSchema** ou **classSchema** extinto:</span><span class="sxs-lookup"><span data-stu-id="27211-126">The following list includes other consequences of marking an **attributeSchema** or **classSchema** object defunct:</span></span>

-   <span data-ttu-id="27211-127">Falha na adição ou modificação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="27211-127">Addition or modification of an instance fails.</span></span>
-   <span data-ttu-id="27211-128">Os códigos de erro se comportam como se uma classe expirada nunca existia.</span><span class="sxs-lookup"><span data-stu-id="27211-128">Error codes behave as if a defunct class never existed.</span></span>
-   <span data-ttu-id="27211-129">A pesquisa e a exclusão se comportam como se nenhum objeto de esquema fosse desativado.</span><span class="sxs-lookup"><span data-stu-id="27211-129">Search and delete behave as if no schema objects have been made defunct.</span></span>
-   <span data-ttu-id="27211-130">Permitir excluir apenas o atributo inteiro do objeto.</span><span class="sxs-lookup"><span data-stu-id="27211-130">Only allow deleting entire attribute from object.</span></span>

<span data-ttu-id="27211-131">A lista a seguir inclui opções adicionais em um ambiente de produção para reduzir o impacto das extensões de esquema expiradas:</span><span class="sxs-lookup"><span data-stu-id="27211-131">The following list includes additional options in a production environment for reducing the impact of defunct schema extensions:</span></span>

-   <span data-ttu-id="27211-132">Remova todos os valores de atributo **mayHave** de uma classe expirada.</span><span class="sxs-lookup"><span data-stu-id="27211-132">Remove all **mayHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="27211-133">Reduza o tamanho de todos os valores de atributo **mustHave** de uma classe expirada.</span><span class="sxs-lookup"><span data-stu-id="27211-133">Reduce the size of all **mustHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="27211-134">Remova um atributo extinto do catálogo global.</span><span class="sxs-lookup"><span data-stu-id="27211-134">Remove a defunct attribute from the global catalog.</span></span>
-   <span data-ttu-id="27211-135">Remova um atributo extinto de qualquer índice.</span><span class="sxs-lookup"><span data-stu-id="27211-135">Remove a defunct attribute from any index.</span></span>

<span data-ttu-id="27211-136">Outras opções para remover alterações de esquema indesejadas em um ambiente de produção são para os desenvolvedores usarem um controlador de domínio privado para teste.</span><span class="sxs-lookup"><span data-stu-id="27211-136">Other options for removing unwanted schema changes in a production environment are for developers to use a private domain controller for testing.</span></span> <span data-ttu-id="27211-137">Nesse caso, você pode:</span><span class="sxs-lookup"><span data-stu-id="27211-137">In this case, you can:</span></span>

-   <span data-ttu-id="27211-138">"Redefinir" o servidor de Active Directory usando Dcpromo.exe para rebaixar o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="27211-138">"Reset" the Active Directory server by using Dcpromo.exe to demote the DC.</span></span> <span data-ttu-id="27211-139">Depois que o rebaixamento for concluído, use Dcpromo.exe novamente para promover o servidor de volta para um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="27211-139">After the demote completes, use Dcpromo.exe again to promote the server back to a DC.</span></span> <span data-ttu-id="27211-140">O desenvolvedor pode, então, usar scripts LDIF para recarregar todas as classes, atributos e instâncias de objeto necessários.</span><span class="sxs-lookup"><span data-stu-id="27211-140">The developer can then use LDIF scripts to reload any required classes, attributes, and object instances.</span></span>
-   <span data-ttu-id="27211-141">Use Ntbackup.exe para executar um backup de estado do sistema para uma partição de disco disponível.</span><span class="sxs-lookup"><span data-stu-id="27211-141">Use Ntbackup.exe to perform a system-state backup to an available disk partition.</span></span> <span data-ttu-id="27211-142">Reinicialize para o modo de restauração do serviço de diretório/seguro para restaurar.</span><span class="sxs-lookup"><span data-stu-id="27211-142">Reboot to Safe/Directory Service Restore mode to restore.</span></span>

<span data-ttu-id="27211-143">Para sistemas operacionais Windows Server 2003, quando você define uma classe ou atributo como extinto, você pode reutilizar imediatamente os valores **ldapDisplayName**, **schemaIDGUID**, **OID** e **mAPIID** do elemento de esquema extinto quando você cria uma nova classe ou atributo para substituí-lo.</span><span class="sxs-lookup"><span data-stu-id="27211-143">For Windows Server 2003 operating systems, when you set a class or attribute to defunct, you can immediately reuse the **ldapDisplayName**, **schemaIdGuid**, **OID** and **mapiID** values of the defunct schema element when you create a new class or attribute to replace it.</span></span> <span data-ttu-id="27211-144">A versão expirada da classe ou do atributo é mantida no contêiner de esquema, mas fica oculta no snap-in do MMC.</span><span class="sxs-lookup"><span data-stu-id="27211-144">The defunct version of the class or attribute is maintained in the Schema container, but it is hidden in the MMC snap-in.</span></span> <span data-ttu-id="27211-145">Para reativar o elemento de esquema antigo, defina **isfunc** como **false**.</span><span class="sxs-lookup"><span data-stu-id="27211-145">To reactivate the old schema element, set **isDefunct** to **FALSE**.</span></span>

<span data-ttu-id="27211-146">O exemplo de código LDIF a seguir mostra como modificar o atributo **Isfunct** e alterar o RDN para que ele não seja confundido com a nova classe que você cria para substituí-lo.</span><span class="sxs-lookup"><span data-stu-id="27211-146">The following LDIF code example shows how to modify the **isDefunct** attribute and change the RDN so that it is not confused with the new class that you create to replace it.</span></span>

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

<span data-ttu-id="27211-147">Use o comando a seguir para executar o exemplo de código LDIF em uma floresta para um computador que executa o em sistemas operacionais Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="27211-147">Use the following command to run the LDIF code example against a forest for a computer running on Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="27211-148">**LDIFDE/i/f RDN. ldf/c "DC = X" "DC = mydomain, DC = com"**</span><span class="sxs-lookup"><span data-stu-id="27211-148">**ldifde /i /f rdn.ldf /c "DC=X" "dc=mydomain,dc=com"**</span></span>

<span data-ttu-id="27211-149">(Em que "DC = X" é uma constante)</span><span class="sxs-lookup"><span data-stu-id="27211-149">(Where "DC=X" is a constant)</span></span>

 

 





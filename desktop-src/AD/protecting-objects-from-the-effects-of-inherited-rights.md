---
title: Protegendo objetos dos efeitos de direitos herdados
description: Conforme discutido no tópico herança e delegação de administração, as ACEs podem ser definidas em um objeto de contêiner, como um organizationalUnit, domainDNS, contêiner e assim por diante, e propagadas para objetos filho com base nos sinalizadores de ACE definidos nessas ACEs.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Protegendo objetos dos efeitos de AD de direitos herdados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007301"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a><span data-ttu-id="4977e-104">Protegendo objetos dos efeitos de direitos herdados</span><span class="sxs-lookup"><span data-stu-id="4977e-104">Protecting Objects from the Effects of Inherited Rights</span></span>

<span data-ttu-id="4977e-105">Conforme discutido no tópico [herança e delegação de administração](inheritance-and-delegation-of-administration.md), as ACEs podem ser definidas em um objeto de contêiner, como um **OrganizationalUnit**, **domainDns**, **contêiner** e assim por diante, e propagadas para objetos filho com base nos sinalizadores de Ace definidos nessas ACEs.</span><span class="sxs-lookup"><span data-stu-id="4977e-105">As discussed in the topic [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md), ACEs can be set on a container object, such as an **organizationalUnit**, **domainDNS**, **container**, and so on, and propagated to child objects based on the ACE flags set on those ACEs.</span></span>

<span data-ttu-id="4977e-106">Se você tiver um objeto seguro ou um objeto cujas ACEs você deseja controlar explicitamente, como uma OU particular ou um usuário especial, poderá impedir que as ACEs sejam propagadas para o objeto pelo seu contêiner pai ou por seus predecessores do contêiner pai.</span><span class="sxs-lookup"><span data-stu-id="4977e-106">If you have a secure object or an object whose ACEs you want to explicitly control, such as a private OU or a special user, you can prevent ACEs from being propagated to the object by its parent container or its parent container's predecessors.</span></span>

<span data-ttu-id="4977e-107">Use a propriedade [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para controlar se as DACLs e SACLs são herdadas pelo objeto do seu contêiner pai.</span><span class="sxs-lookup"><span data-stu-id="4977e-107">Use the [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property to control whether DACLs and SACLs are inherited by the object from its parent container.</span></span>

<span data-ttu-id="4977e-108">A propriedade [**IADsSecurityDescriptor. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) pode ser usada para proteger um objeto dos efeitos de ACEs herdadas.</span><span class="sxs-lookup"><span data-stu-id="4977e-108">The [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property can be used to protect an object from the effects of inherited ACEs.</span></span> <span data-ttu-id="4977e-109">Os sinalizadores a seguir forçam o controle de acesso a ser definido explicitamente no objeto e impedem que um usuário modifique o controle de acesso ao objeto definindo ACEs herdáveis no contêiner pai do objeto ou seus predecessores do contêiner pai.</span><span class="sxs-lookup"><span data-stu-id="4977e-109">The following flags force access control to be set explicitly on the object and prevent a user from modifying access control to the object by setting inheritable ACEs on the object's parent container, or its parent container's predecessors.</span></span>



| <span data-ttu-id="4977e-110">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="4977e-110">Flag</span></span>                               | <span data-ttu-id="4977e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="4977e-111">Description</span></span>                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4977e-112">**DACL de SE \_ \_ protegida**</span><span class="sxs-lookup"><span data-stu-id="4977e-112">**SE\_DACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="4977e-113">Impede que as ACEs definidas na DACL do contêiner pai e quaisquer objetos acima do contêiner pai na hierarquia de diretório sejam aplicados ao objeto DACL.</span><span class="sxs-lookup"><span data-stu-id="4977e-113">Prevents ACEs set on the DACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object DACL.</span></span><br/> |
| <span data-ttu-id="4977e-114">**\_SACL \_ protegida**</span><span class="sxs-lookup"><span data-stu-id="4977e-114">**SE\_SACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="4977e-115">Impede que as ACEs definidas na SACL do contêiner pai e quaisquer objetos acima do contêiner pai na hierarquia de diretório sejam aplicados à SACL do objeto.</span><span class="sxs-lookup"><span data-stu-id="4977e-115">Prevents ACEs set on the SACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object SACL.</span></span><br/> |



 

<span data-ttu-id="4977e-116">Lembre-se de que o sinalizador **se a \_ DACL \_ presente** deve estar presente para definir **se a \_ DACL \_ protegida** e **se a \_ SACL \_ presente** deve estar presente para definir **se a SACL está \_ \_ protegida**.</span><span class="sxs-lookup"><span data-stu-id="4977e-116">Be aware that the **SE\_DACL\_PRESENT** flag must be present to set **SE\_DACL\_PROTECTED** and **SE\_SACL\_PRESENT** must be present to set **SE\_SACL\_PROTECTED**.</span></span>

 


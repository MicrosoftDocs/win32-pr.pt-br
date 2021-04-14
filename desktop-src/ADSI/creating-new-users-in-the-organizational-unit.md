---
title: Criando novos usuários na unidade organizacional
description: Terry Adams foi contratado na organização de vendas da Fabrikam. Seu relatório direto é Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Criando novos usuários na unidade organizacional ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453487"
---
# <a name="creating-new-users-in-the-organizational-unit"></a><span data-ttu-id="513eb-105">Criando novos usuários na unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="513eb-105">Creating New Users in the Organizational Unit</span></span>

<span data-ttu-id="513eb-106">Terry Adams foi contratado na organização de vendas da Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="513eb-106">Terry Adams was hired into the Fabrikam Sales organization.</span></span> <span data-ttu-id="513eb-107">Seu relatório direto é Patrick Hines.</span><span class="sxs-lookup"><span data-stu-id="513eb-107">His direct report is Patrick Hines.</span></span>

<span data-ttu-id="513eb-108">Conforme mostrado no exemplo de código a seguir, Joe Andreshak, administrador corporativo, criará uma nova conta para ele.</span><span class="sxs-lookup"><span data-stu-id="513eb-108">As shown in the following code example, Joe Andreshak, the enterprise administrator, will create a new account for him.</span></span>


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



<span data-ttu-id="513eb-109">Ao criar um novo usuário, você deve especificar um **sAMAccountName**.</span><span class="sxs-lookup"><span data-stu-id="513eb-109">When creating a new user, you must specify a **sAMAccountName**.</span></span> <span data-ttu-id="513eb-110">Este é um atributo obrigatório para a classe User.</span><span class="sxs-lookup"><span data-stu-id="513eb-110">This is a mandatory attribute for the user class.</span></span> <span data-ttu-id="513eb-111">Antes que uma instância de um objeto possa ser criada, todos os atributos obrigatórios devem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="513eb-111">Before an instance of an object can be created, all mandatory attributes must be set.</span></span> <span data-ttu-id="513eb-112">O **sAMAccountName** será gerado automaticamente se um não for especificado para um novo usuário.</span><span class="sxs-lookup"><span data-stu-id="513eb-112">The **sAMAccountName** will automatically be generated if one is not specified for a new user.</span></span>

<span data-ttu-id="513eb-113">Ao criar um novo usuário, todos os atributos necessários devem ser definidos no cache local antes que o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="513eb-113">When creating a new user, all of the required attributes must be set in the local cache before the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

<span data-ttu-id="513eb-114">Joe, como administrador, pode atribuir a senha de Terry usando o método [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="513eb-114">Joe, as an administrator, can assign Terry's password using the [**IADsUser.SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="513eb-115">O método **IADsUser. SetPassword** não funcionará até que o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) tenha sido chamado.</span><span class="sxs-lookup"><span data-stu-id="513eb-115">The **IADsUser.SetPassword** method will not work until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method has been called.</span></span>

<span data-ttu-id="513eb-116">Em seguida, Joe habilita a conta de usuário definindo a propriedade [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) como **false**.</span><span class="sxs-lookup"><span data-stu-id="513eb-116">Then, Joe enables the user account by setting the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property to **FALSE**.</span></span>

<span data-ttu-id="513eb-117">O exemplo de código a seguir mostra como definir Terry como gerente do Patrick.</span><span class="sxs-lookup"><span data-stu-id="513eb-117">The following code example shows how to set Terry as Patrick's manager.</span></span>


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



<span data-ttu-id="513eb-118">Você pode estar imaginando o que acontece se Terry alterar seu nome, mudar para uma organização diferente ou deixar a empresa.</span><span class="sxs-lookup"><span data-stu-id="513eb-118">You may wonder what happens if Terry changes his name, moves to a different organization, or leaves the company.</span></span> <span data-ttu-id="513eb-119">Quem mantém este link de relatório direto do gerente?</span><span class="sxs-lookup"><span data-stu-id="513eb-119">Who maintains this manager-direct report link?</span></span> <span data-ttu-id="513eb-120">Para obter mais informações e a solução para esse problema, consulte [reorganização](reorganization.md).</span><span class="sxs-lookup"><span data-stu-id="513eb-120">For more information, and the solution to this problem, see [Reorganization](reorganization.md).</span></span> <span data-ttu-id="513eb-121">Como o esquema de Active Directory é extensível, você pode modelar seus objetos para incluir relações de estilo de relatório diretas de gerentes semelhantes.</span><span class="sxs-lookup"><span data-stu-id="513eb-121">Because the Active Directory schema is extensible, you can model your objects to include similar manager-direct report style relationships.</span></span>

<span data-ttu-id="513eb-122">Antes de prosseguir para a próxima tarefa, veja um exemplo de código que mostra como Joe exibirá os subordinados diretos de Terry.</span><span class="sxs-lookup"><span data-stu-id="513eb-122">Before going on to the next task, look at a code example that shows how Joe would view Terry's direct reports.</span></span>


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



<span data-ttu-id="513eb-123">Neste exemplo de código, Patrick será exibido como o relatório direto de Terry, embora o atributo **DirectReports** nunca tenha sido modificado.</span><span class="sxs-lookup"><span data-stu-id="513eb-123">In this code example, Patrick will display as Terry's direct report, even though the **directReports** attribute was never modified.</span></span> <span data-ttu-id="513eb-124">Active Directory faz isso automaticamente.</span><span class="sxs-lookup"><span data-stu-id="513eb-124">Active Directory does this automatically.</span></span>

<span data-ttu-id="513eb-125">No mundo do diretório, um atributo pode ter um ou vários valores.</span><span class="sxs-lookup"><span data-stu-id="513eb-125">In the directory world, an attribute can have single or multiple values.</span></span> <span data-ttu-id="513eb-126">Como **DirectReports** tem vários valores, você pode obter essas informações examinando o esquema, é mais fácil usar o método [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) , que retorna uma matriz de valores, independentemente de os valores únicos ou múltiplos serem retornados.</span><span class="sxs-lookup"><span data-stu-id="513eb-126">Because **directReports** has multiple values, you can get this information by looking at the schema, it is easier to use the [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, which returns an array of values regardless of whether single or multiple values are returned.</span></span>

<span data-ttu-id="513eb-127">O snap-in Active Directory usuários e computadores permite exibir relatórios diretos e relações de gerente na página de propriedades do usuário.</span><span class="sxs-lookup"><span data-stu-id="513eb-127">The Active Directory Users and Computers snap-in lets you view direct reports and manager relationships on the user's property page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="513eb-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="513eb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="513eb-129">Adicionando usuários a um grupo</span><span class="sxs-lookup"><span data-stu-id="513eb-129">Adding Users to a Group</span></span>](adding-users-to-a-group.md)
</dt> </dl>

 

 





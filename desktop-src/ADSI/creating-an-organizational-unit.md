---
title: Criando uma unidade organizacional
description: Agora que você tem o objeto de domínio, você pode começar a criar unidades organizacionais.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Criando um ADSI de unidade organizacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915907"
---
# <a name="creating-an-organizational-unit"></a><span data-ttu-id="ee238-104">Criando uma unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="ee238-104">Creating an Organizational Unit</span></span>

<span data-ttu-id="ee238-105">Agora que você tem o objeto de domínio, você pode começar a criar unidades organizacionais.</span><span class="sxs-lookup"><span data-stu-id="ee238-105">Now that you have the domain object, you can start creating organizational units.</span></span> <span data-ttu-id="ee238-106">A Fabrikam tem duas divisões: vendas e produção.</span><span class="sxs-lookup"><span data-stu-id="ee238-106">Fabrikam has two divisions: Sales and Production.</span></span> <span data-ttu-id="ee238-107">A empresa está planejando contratar dois administradores do Windows 2000 para gerenciar cada divisão.</span><span class="sxs-lookup"><span data-stu-id="ee238-107">The company is planning to hire two Windows 2000 administrators to manage each division.</span></span> <span data-ttu-id="ee238-108">Joe Worden, como administrador corporativo, criará duas novas unidades organizacionais no domínio fabrikam.</span><span class="sxs-lookup"><span data-stu-id="ee238-108">Joe Worden, as the enterprise administrator, will create two new organizational units under the Fabrikam domain.</span></span> <span data-ttu-id="ee238-109">Ao criar uma unidade organizacional, Joe pode agrupar vários objetos e permitir que outra pessoa gerencie esses objetos.</span><span class="sxs-lookup"><span data-stu-id="ee238-109">By creating an organizational unit, Joe can group multiple objects together and let someone else manage these objects.</span></span> <span data-ttu-id="ee238-110">O exemplo de código a seguir cria a UO (unidade organizacional Sales).</span><span class="sxs-lookup"><span data-stu-id="ee238-110">The following code example creates the Sales Organizational Unit (OU).</span></span>


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



<span data-ttu-id="ee238-111">O método [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) aceita o nome da classe e o nome do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="ee238-111">The [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) method accepts the class name and the name of the new object.</span></span> <span data-ttu-id="ee238-112">Neste ponto, o objeto não está confirmado em Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ee238-112">At this point the object is not committed to Active Directory.</span></span> <span data-ttu-id="ee238-113">Você, no entanto, terá uma referência de objeto ADSI/COM no cliente.</span><span class="sxs-lookup"><span data-stu-id="ee238-113">You, however, will have an ADSI/COM object reference on the client.</span></span> <span data-ttu-id="ee238-114">Com esse objeto ADSI, você pode definir ou modificar atributos usando o método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="ee238-114">With this ADSI object, you can set or modify attributes using the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method.</span></span> <span data-ttu-id="ee238-115">O método **IADs. put** aceita o nome do atributo e o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="ee238-115">The **IADs.Put** method accepts the attribute name and the value of the attribute.</span></span> <span data-ttu-id="ee238-116">Ainda assim, nada é confirmado no diretório; Tudo é armazenado em cache no cliente.</span><span class="sxs-lookup"><span data-stu-id="ee238-116">Still, nothing is committed to the directory; everything is cached at the client.</span></span> <span data-ttu-id="ee238-117">Quando você chama o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , as alterações, nesse caso, a criação de objetos e a modificação de atributos, são confirmadas no diretório.</span><span class="sxs-lookup"><span data-stu-id="ee238-117">When you call the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method, the changes, in this case, object creation and attribute modification, are committed to the directory.</span></span> <span data-ttu-id="ee238-118">Essas alterações são transacionadas, o que significa que você verá o novo objeto com todos os atributos que você definiu ou nenhum objeto.</span><span class="sxs-lookup"><span data-stu-id="ee238-118">These changes are transacted, meaning that you will see either the new object with all attributes you set, or no object at all.</span></span>

<span data-ttu-id="ee238-119">Você também pode aninhar unidades organizacionais.</span><span class="sxs-lookup"><span data-stu-id="ee238-119">You can also nest organizational units.</span></span> <span data-ttu-id="ee238-120">O exemplo de código a seguir pressupõe que a divisão de vendas esteja dividida mais nas regiões leste e oeste.</span><span class="sxs-lookup"><span data-stu-id="ee238-120">The following code example assumes that the Sales division is divided further into the East and West regions.</span></span>


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



<span data-ttu-id="ee238-121">Isso também se aplica à região oeste.</span><span class="sxs-lookup"><span data-stu-id="ee238-121">This also applies for the West region.</span></span>

<span data-ttu-id="ee238-122">Para associar diretamente à região leste da organização Sales, especifique o nome distinto.</span><span class="sxs-lookup"><span data-stu-id="ee238-122">To bind directly to the East region in the Sales organization, specify the distinguished name.</span></span>


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



<span data-ttu-id="ee238-123">Se você já tiver associado ao objeto pai (vendas), poderá associar ao objeto filho (leste) do objeto pai usando o nome relativo do objeto filho.</span><span class="sxs-lookup"><span data-stu-id="ee238-123">If you have already bound to the parent object (Sales), you can bind to the child object (East) from the parent object using the relative name of the child object.</span></span>


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



<span data-ttu-id="ee238-124">Para garantir que os objetos tenham sido criados, use o snap-in Active Directory usuários e computadores do MMC para exibir as novas unidades organizacionais.</span><span class="sxs-lookup"><span data-stu-id="ee238-124">To ensure that the objects have been created, use the Active Directory Users and Computers MMC snap-in to view the new organizational units.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee238-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee238-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee238-126">Movendo usuários existentes para a unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="ee238-126">Moving Existing Users to the Organizational Unit</span></span>](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 





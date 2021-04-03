---
title: Usando objectGUID para associar a um objeto
description: Um nome diferenciado de objeto será alterado se o objeto for renomeado ou movido, portanto o nome diferenciado não é um identificador de objeto confiável.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Usando objectGUID para associar a um AD de objeto
- AD do objectGUID
- objectGUID AD, usando para associar a um objeto
- Active Directory, usando, associação, usando objectGUID para associar ao objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007281"
---
# <a name="using-objectguid-to-bind-to-an-object"></a><span data-ttu-id="a9bb9-107">Usando objectGUID para associar a um objeto</span><span class="sxs-lookup"><span data-stu-id="a9bb9-107">Using objectGUID to Bind to an Object</span></span>

<span data-ttu-id="a9bb9-108">Um nome diferenciado de objeto será alterado se o objeto for renomeado ou movido, portanto o nome diferenciado não é um identificador de objeto confiável.</span><span class="sxs-lookup"><span data-stu-id="a9bb9-108">An object distinguished name changes if the object is renamed or moved, therefore the distinguished name is not a reliable object identifier.</span></span> <span data-ttu-id="a9bb9-109">Em Active Directory Domain Services, a propriedade **objectGUID** de um objeto nunca muda, mesmo que o objeto seja renomeado ou movido.</span><span class="sxs-lookup"><span data-stu-id="a9bb9-109">In Active Directory Domain Services, an object's **objectGUID** property never changes, even if the object is renamed or moved.</span></span> <span data-ttu-id="a9bb9-110">Para obter mais informações sobre **objectGUID** e identificadores, consulte [nomes de objetos e identidades](object-names-and-identities.md).</span><span class="sxs-lookup"><span data-stu-id="a9bb9-110">For more information about **objectGUID** and identifiers, see [Object Names and Identities](object-names-and-identities.md).</span></span>

<span data-ttu-id="a9bb9-111">O provedor LDAP Active Directory fornece um método para associar a um objeto usando o GUID do objeto.</span><span class="sxs-lookup"><span data-stu-id="a9bb9-111">The Active Directory LDAP provider provides a method to bind to an object using the object GUID.</span></span> <span data-ttu-id="a9bb9-112">O formato da cadeia de vinculação é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a9bb9-112">The binding string format is as follows:</span></span>


```C++
LDAP://servername/<GUID=XXXXX>
```



<span data-ttu-id="a9bb9-113">Neste exemplo, "servername" é o nome do servidor de diretório e "XXXXX" é a representação de cadeia de caracteres do valor hexadecimal do GUID.</span><span class="sxs-lookup"><span data-stu-id="a9bb9-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the GUID.</span></span> <span data-ttu-id="a9bb9-114">O "servername" é opcional.</span><span class="sxs-lookup"><span data-stu-id="a9bb9-114">The "servername" is optional.</span></span> <span data-ttu-id="a9bb9-115">A cadeia de caracteres GUID é especificada no formulário "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX".</span><span class="sxs-lookup"><span data-stu-id="a9bb9-115">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form.</span></span> <span data-ttu-id="a9bb9-116">A cadeia de caracteres GUID também pode assumir a forma "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", que é a mesma forma que a cadeia de caracteres produzida pela função [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , sem as chaves ao redor " {} ".</span><span class="sxs-lookup"><span data-stu-id="a9bb9-116">The GUID string can also take the form "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", which is the same form as the string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, without the surrounding braces "{}".</span></span> <span data-ttu-id="a9bb9-117">Para obter mais informações e um exemplo de código que mostra como criar uma cadeia de caracteres vinculável de um GUID, consulte [exemplo de código para criar uma representação de cadeia de caracteres vinculável de um GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="a9bb9-117">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span> <span data-ttu-id="a9bb9-118">A propriedade [**IADs. GUID**](/windows/desktop/ADSI/iads-property-methods) pode ser usada para recuperar a forma de cadeia de caracteres apropriada do GUID.</span><span class="sxs-lookup"><span data-stu-id="a9bb9-118">The [**IADs.GUID**](/windows/desktop/ADSI/iads-property-methods) property can be used to retrieve the proper string form of the GUID.</span></span>

<span data-ttu-id="a9bb9-119">Ao vincular usando o GUID do objeto, não há suporte para alguns métodos e propriedades [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="a9bb9-119">When binding using the object GUID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="a9bb9-120">As seguintes propriedades **IADs** não são suportadas por objetos obtidos pela Associação usando o GUID do objeto:</span><span class="sxs-lookup"><span data-stu-id="a9bb9-120">The following **IADs** properties are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="a9bb9-121">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="a9bb9-121">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="a9bb9-122">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a9bb9-122">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="a9bb9-123">**Pai**</span><span class="sxs-lookup"><span data-stu-id="a9bb9-123">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="a9bb9-124">Os objetos **IADsContainer** a seguir não são compatíveis com aqueles obtidos pela Associação usando o GUID do objeto:</span><span class="sxs-lookup"><span data-stu-id="a9bb9-124">The following **IADsContainer** methods are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="a9bb9-125">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="a9bb9-125">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="a9bb9-126">**Criar**</span><span class="sxs-lookup"><span data-stu-id="a9bb9-126">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="a9bb9-127">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="a9bb9-127">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="a9bb9-128">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="a9bb9-128">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="a9bb9-129">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="a9bb9-129">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="a9bb9-130">Para usar esses métodos e propriedades após a associação a um objeto usando o GUID do objeto, use o método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar o nome diferenciado do objeto e, em seguida, use o nome distinto para associar ao objeto novamente.</span><span class="sxs-lookup"><span data-stu-id="a9bb9-130">To use these methods and properties after binding to an object using the object GUID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="a9bb9-131">Se um aplicativo armazenar ou armazenar em cache identificadores ou referências a objetos armazenados no Active Directory Domain Services, o GUID do objeto será o melhor identificador a ser usado por vários motivos:</span><span class="sxs-lookup"><span data-stu-id="a9bb9-131">If an application stores or caches identifiers or references to objects stored in Active Directory Domain Services, the object GUID is the best identifier to use for several reasons:</span></span>

-   <span data-ttu-id="a9bb9-132">A propriedade **objectGUID** de no objeto nunca muda, mesmo que o objeto seja renomeado ou movido.</span><span class="sxs-lookup"><span data-stu-id="a9bb9-132">The **objectGUID** property of on object never changes even if the object is renamed or moved.</span></span>
-   <span data-ttu-id="a9bb9-133">É fácil associar-se ao objeto usando o GUID do objeto.</span><span class="sxs-lookup"><span data-stu-id="a9bb9-133">It is easy to bind to the object using the object GUID.</span></span>
-   <span data-ttu-id="a9bb9-134">Se o objeto for renomeado ou movido, a propriedade **objectGUID** fornecerá um único identificador que pode ser usado para localizar e identificar rapidamente o objeto, em vez de ter que compor uma consulta que tenha condições para todas as propriedades que identifiquem esse objeto.</span><span class="sxs-lookup"><span data-stu-id="a9bb9-134">If the object is renamed or moved, the **objectGUID** property provides a single identifier that can be used to quickly find and identify the object rather than having to compose a query that has conditions for all properties that would identify that object.</span></span>

 

 
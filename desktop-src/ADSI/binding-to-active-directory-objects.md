---
title: Associação a objetos Active Directory
description: Antes de continuar com esse cenário, você deve entender como os objetos ADSI são nomeados em Active Directory e como associá-los. A associação de um objeto ADSI conecta o objeto ao serviço de diretório e permite que você acesse os métodos do objeto.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004877"
---
# <a name="binding-to-active-directory-objects"></a><span data-ttu-id="d5398-104">Associação a objetos Active Directory</span><span class="sxs-lookup"><span data-stu-id="d5398-104">Binding to Active Directory Objects</span></span>

<span data-ttu-id="d5398-105">Antes de continuar com esse cenário, você deve entender como os objetos ADSI são nomeados em Active Directory e como associá-los.</span><span class="sxs-lookup"><span data-stu-id="d5398-105">Before you continue with this scenario, you must understand how ADSI objects are named in Active Directory, and how to bind them.</span></span> <span data-ttu-id="d5398-106">A associação de um objeto ADSI conecta o objeto ao serviço de diretório e permite que você acesse os métodos do objeto.</span><span class="sxs-lookup"><span data-stu-id="d5398-106">Binding an ADSI object connects the object with the directory service, and allows you to access the methods of the object.</span></span>

## <a name="adspath"></a><span data-ttu-id="d5398-107">ADsPath</span><span class="sxs-lookup"><span data-stu-id="d5398-107">ADsPath</span></span>

<span data-ttu-id="d5398-108">Um objeto ADSI é identificado exclusivamente por sua cadeia de caracteres de associação, que também é conhecida como ADsPath.</span><span class="sxs-lookup"><span data-stu-id="d5398-108">An ADSI object is uniquely identified by its binding string, which is also referred to as an ADsPath.</span></span> <span data-ttu-id="d5398-109">Um ADsPath é uma combinação de um identificador programático (progID) do provedor ADSI e o DN (nome distinto) do objeto.</span><span class="sxs-lookup"><span data-stu-id="d5398-109">An ADsPath is a combination of a programmatic identifier (progID) of the ADSI provider, and the distinguished name (DN) of the object.</span></span>

<span data-ttu-id="d5398-110">Este é o formato de um ADsPath:</span><span class="sxs-lookup"><span data-stu-id="d5398-110">Here's the format of an ADsPath:</span></span>

<span data-ttu-id="d5398-111">"progID://DN"</span><span class="sxs-lookup"><span data-stu-id="d5398-111">"progID://DN"</span></span>

-   <span data-ttu-id="d5398-112">pogID — o identificador programático do provedor ADSI, como LDAP ou WinNT.</span><span class="sxs-lookup"><span data-stu-id="d5398-112">pogID — the programmatic identifier of the ADSI provider, such as LDAP or WinNT.</span></span>

-   <span data-ttu-id="d5398-113">://— separa o progID do DN.</span><span class="sxs-lookup"><span data-stu-id="d5398-113">:// — separates the progID from the DN.</span></span>

-   <span data-ttu-id="d5398-114">DN — o nome distinto do objeto ADSI, que é o caminho completo do objeto, onde o caminho consiste em nomes distintos relativos (RDNs).</span><span class="sxs-lookup"><span data-stu-id="d5398-114">DN — the distinguished name of the ADSI object, which is the full path of the object, where the path consists of relative distinguished names (RDNs).</span></span>

<span data-ttu-id="d5398-115">Um RDN é o nome do objeto sem o caminho e é exclusivo de seus objetos irmãos.</span><span class="sxs-lookup"><span data-stu-id="d5398-115">An RDN is the name of the object without the path, and is unique from its sibling objects.</span></span> <span data-ttu-id="d5398-116">Um RDN consiste em uma ID e um valor de atributo, como "DC = Fabrikam", em que DC é o atributo e Fabrikam é o valor.</span><span class="sxs-lookup"><span data-stu-id="d5398-116">An RDN consists of an attribute ID and value, such as "DC=Fabrikam", where DC is the attribute, and Fabrikam is the value.</span></span> <span data-ttu-id="d5398-117">O DC é uma ID de atributo RDN que significa componente de domínio.</span><span class="sxs-lookup"><span data-stu-id="d5398-117">DC is an RDN attribute ID that stands for domain component.</span></span>

<span data-ttu-id="d5398-118">Aqui está um exemplo de um ADsPath:</span><span class="sxs-lookup"><span data-stu-id="d5398-118">Here’s an example of an ADsPath:</span></span>

<span data-ttu-id="d5398-119">"LDAP://DC = Fabrikam, DC = com"</span><span class="sxs-lookup"><span data-stu-id="d5398-119">"LDAP://DC=Fabrikam,DC=Com"</span></span>

## <a name="binding-the-object"></a><span data-ttu-id="d5398-120">Associando o objeto</span><span class="sxs-lookup"><span data-stu-id="d5398-120">Binding the object</span></span>

<span data-ttu-id="d5398-121">Veja como você pode associar o objeto de domínio neste cenário:</span><span class="sxs-lookup"><span data-stu-id="d5398-121">Here's how you can bind the domain object in this scenario:</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



<span data-ttu-id="d5398-122">Quando você executa este exemplo de código, a ADSI usa o DN para determinar os objetos ADSI a serem associados.</span><span class="sxs-lookup"><span data-stu-id="d5398-122">When you run this code example, ADSI uses the DN to determine the ADSI objects to bind.</span></span> <span data-ttu-id="d5398-123">Depois que a ADSI associa esses objetos, você pode acessar seus métodos.</span><span class="sxs-lookup"><span data-stu-id="d5398-123">After ADSI binds these objects, you can access their methods.</span></span> <span data-ttu-id="d5398-124">O exemplo de código anterior associa um objeto de domínio a [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="d5398-124">The previous code example binds a domain object to [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="d5398-125">Agora você pode usar métodos nessas interfaces, como [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)e [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span><span class="sxs-lookup"><span data-stu-id="d5398-125">You can now use methods on those interfaces such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete), and [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span></span>

<span data-ttu-id="d5398-126">Depois de associar um objeto de domínio, você pode imprimir alguns de seus atributos:</span><span class="sxs-lookup"><span data-stu-id="d5398-126">After you bind a domain object, you can print some of its attributes:</span></span>


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



<span data-ttu-id="d5398-127">Para obter mais informações sobre ADsPath, consulte [Binding String](binding-string.md).</span><span class="sxs-lookup"><span data-stu-id="d5398-127">For more information about ADsPath, see [Binding String](binding-string.md).</span></span> <span data-ttu-id="d5398-128">Para obter mais informações sobre associação, consulte [Binding to a ADSI Object](binding-to-an-adsi-object.md).</span><span class="sxs-lookup"><span data-stu-id="d5398-128">For more information about binding, see [Binding to an ADSI Object](binding-to-an-adsi-object.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5398-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5398-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5398-130">Criando uma unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="d5398-130">Creating an Organizational Unit</span></span>](creating-an-organizational-unit.md)
</dt> </dl>

 

 





---
title: Benefícios do uso de extensões ADSI
description: A maneira como os métodos de extensão são implementados depende do gravador de extensão.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27e80e6c095fcc02ca02c57b0987d1e6ed410ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004879"
---
# <a name="benefits-of-using-adsi-extensions"></a><span data-ttu-id="01e74-103">Benefícios do uso de extensões ADSI</span><span class="sxs-lookup"><span data-stu-id="01e74-103">Benefits of Using ADSI Extensions</span></span>

<span data-ttu-id="01e74-104">A maneira como os métodos de extensão são implementados depende do gravador de extensão.</span><span class="sxs-lookup"><span data-stu-id="01e74-104">The way in which extension methods are implemented depends on the extension writer.</span></span> <span data-ttu-id="01e74-105">Um gravador de extensão pode até mesmo implementar um método completamente fora do escopo do diretório.</span><span class="sxs-lookup"><span data-stu-id="01e74-105">An extension writer may even implement a method completely outside the scope of the directory.</span></span> <span data-ttu-id="01e74-106">Por exemplo, um desenvolvedor de backup e restauração de planos de software para estender um objeto chamado **computador**.</span><span class="sxs-lookup"><span data-stu-id="01e74-106">For example, a developer of backup and restore software plans to extend an object called **computer**.</span></span> <span data-ttu-id="01e74-107">O desenvolvedor deve criar dois métodos: **backup** e **restauração**.</span><span class="sxs-lookup"><span data-stu-id="01e74-107">The developer must create two methods: **BackUp** and **Restore**.</span></span> <span data-ttu-id="01e74-108">Esses métodos operam remotamente no computador físico no qual o objeto de **computador** no diretório aponta.</span><span class="sxs-lookup"><span data-stu-id="01e74-108">These methods operate remotely on the physical computer that the **computer** object in the directory points to.</span></span> <span data-ttu-id="01e74-109">Agindo como uma extensão, o componente acessa a infraestrutura de ADSI e é exibido por clientes ADSI como parte integrante do objeto.</span><span class="sxs-lookup"><span data-stu-id="01e74-109">By acting as an extension, the component accesses the ADSI infrastructure and is viewed by ADSI clients as an integral part of the object.</span></span>

<span data-ttu-id="01e74-110">Os cenários a seguir descrevem situações em que a criação de uma extensão para ADSI seria vantajosa:</span><span class="sxs-lookup"><span data-stu-id="01e74-110">The following scenarios describe situations where creating an extension to ADSI would be advantageous:</span></span>

-   <span data-ttu-id="01e74-111">Crie uma extensão para integrar um componente ao objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="01e74-111">Create an extension to integrate a component with the directory object.</span></span> <span data-ttu-id="01e74-112">Como há um objeto de **usuário** no diretório, um desenvolvedor de RH pode querer criar uma extensão ADSI que popula outros dados no diretório quando um **usuário** é criado.</span><span class="sxs-lookup"><span data-stu-id="01e74-112">Because there is a **user** object in the directory, an HR developer may wish to create an ADSI extension that populates other data in the directory when a **user** is created.</span></span>
-   <span data-ttu-id="01e74-113">Crie uma extensão se um componente exigir uma pesquisa de diretório.</span><span class="sxs-lookup"><span data-stu-id="01e74-113">Create an extension if a component requires a directory lookup.</span></span> <span data-ttu-id="01e74-114">Um componente pode exigir um diretório como um ponto de partida para uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="01e74-114">A component may require a directory as a starting point for a lookup.</span></span> <span data-ttu-id="01e74-115">Por exemplo, ao criar um novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01e74-115">For example, when creating a new application.</span></span> <span data-ttu-id="01e74-116">Um objeto de aplicativo, **ToolApp**, pode ser publicado no diretório.</span><span class="sxs-lookup"><span data-stu-id="01e74-116">An application object, **ToolApp**, can be published in the directory.</span></span> <span data-ttu-id="01e74-117">Seu aplicativo pode dar suporte a notificações de status em uma coleção de servidores de email.</span><span class="sxs-lookup"><span data-stu-id="01e74-117">Your application may support status notifications on a collection of mail servers.</span></span> <span data-ttu-id="01e74-118">Você decide tornar este aplicativo uma extensão ADSI.</span><span class="sxs-lookup"><span data-stu-id="01e74-118">You decide to make this application an ADSI extension.</span></span>

    <span data-ttu-id="01e74-119">Agora, um usuário pode pesquisar todas as instâncias de **ToolApp** no diretório.</span><span class="sxs-lookup"><span data-stu-id="01e74-119">Now, a user may search for all instances of **ToolApp** in the directory.</span></span> <span data-ttu-id="01e74-120">Para cada objeto retornado, o usuário pode emitir uma chamada para **NotifyNow ()**.</span><span class="sxs-lookup"><span data-stu-id="01e74-120">For each object returned, the user may issue a call to **NotifyNow()**.</span></span> <span data-ttu-id="01e74-121">Um aplicativo ou extensão pode obter mais dados de objeto atual no diretório e notificar cada servidor de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="01e74-121">An application or extension can obtain more current object data in the directory and notify each server asynchronously.</span></span>

-   <span data-ttu-id="01e74-122">Crie uma extensão como uma junção entre namespaces e modelos de programação.</span><span class="sxs-lookup"><span data-stu-id="01e74-122">Create an extension as a junction between namespaces and programming models.</span></span> <span data-ttu-id="01e74-123">Por exemplo, um ISV inventa um novo modelo de objeto para serviços de impressão.</span><span class="sxs-lookup"><span data-stu-id="01e74-123">For example, an ISV invents a new object model for print services.</span></span> <span data-ttu-id="01e74-124">O objeto **PrintQueue** já está definido no diretório.</span><span class="sxs-lookup"><span data-stu-id="01e74-124">The **printQueue** object is already defined in the directory.</span></span> <span data-ttu-id="01e74-125">O ISV pode criar uma extensão ADSI e associá-la ao objeto **PrintQueue** .</span><span class="sxs-lookup"><span data-stu-id="01e74-125">The ISV can create an ADSI extension and associate it with the **printQueue** object.</span></span> <span data-ttu-id="01e74-126">Os usuários ADSI podem se associar a um objeto **PrintQueue** e começar a usar o modelo de objeto para o ISV.</span><span class="sxs-lookup"><span data-stu-id="01e74-126">ADSI users can bind to a **printQueue** object and start using the object model for the ISV.</span></span> <span data-ttu-id="01e74-127">Da perspectiva do cliente ADSI, esse ponto de junção é transparente.</span><span class="sxs-lookup"><span data-stu-id="01e74-127">From the ADSI client perspective, this junction point is transparent.</span></span>
-   <span data-ttu-id="01e74-128">Crie uma extensão para simplificar as tarefas.</span><span class="sxs-lookup"><span data-stu-id="01e74-128">Create an extension to simplify tasks.</span></span> <span data-ttu-id="01e74-129">Muitas tarefas no diretório podem ser realizadas pesquisando e configurando vários atributos em um objeto ou vários objetos.</span><span class="sxs-lookup"><span data-stu-id="01e74-129">Many tasks in the directory can be accomplished by searching and setting multiple attributes in an object or multiple objects.</span></span> <span data-ttu-id="01e74-130">Ao criar uma única função para manipular vários atributos, ele simplifica o desenvolvimento de gravadores de aplicativos e scripts.</span><span class="sxs-lookup"><span data-stu-id="01e74-130">By creating a single function to manipulate multiple attributes, it simplifies development for application and script writers.</span></span>

<span data-ttu-id="01e74-131">Para clientes ADSI, as extensões enriquecem o ambiente de programação ADSI de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="01e74-131">For ADSI clients, extensions enrich the ADSI programming environment in several ways:</span></span>

-   <span data-ttu-id="01e74-132">Os desenvolvedores que criam clientes ADSI não precisam aprender um novo modelo de programação.</span><span class="sxs-lookup"><span data-stu-id="01e74-132">Developers creating ADSI clients do not have to learn a new programming model.</span></span> <span data-ttu-id="01e74-133">As extensões fazem parte do ADSI.</span><span class="sxs-lookup"><span data-stu-id="01e74-133">The extensions are part of ADSI.</span></span> <span data-ttu-id="01e74-134">Eles usariam o mesmo paradigma para pesquisa, manipulação de dados e objetos de proteção.</span><span class="sxs-lookup"><span data-stu-id="01e74-134">They would use the same paradigm for searching, data manipulation, and securing objects.</span></span>
-   <span data-ttu-id="01e74-135">Os administradores podem gerenciar aplicativos habilitados para diretório relacionados usando extensões.</span><span class="sxs-lookup"><span data-stu-id="01e74-135">Administrators can manage related directory-enabled applications using extensions.</span></span>
-   <span data-ttu-id="01e74-136">Os consumidores de extensão podem exibir um objeto e uma extensão ADSI como um objeto integrado.</span><span class="sxs-lookup"><span data-stu-id="01e74-136">Extension consumers can view an ADSI object and extension as one integrated object.</span></span>
-   <span data-ttu-id="01e74-137">Os componentes existentes podem ser integrados ao ADSI, o que permite que as extensões aproveitem os investimentos existentes e criem sinergias entre os componentes.</span><span class="sxs-lookup"><span data-stu-id="01e74-137">Existing components may be integrated with ADSI, which enables extensions to leverage existing investments and create synergy between components.</span></span>

<span data-ttu-id="01e74-138">Extensões ADSI foram projetadas com os seguintes objetivos:</span><span class="sxs-lookup"><span data-stu-id="01e74-138">ADSI extensions were designed with the following objectives:</span></span>

-   <span data-ttu-id="01e74-139">Fácil de implementar.</span><span class="sxs-lookup"><span data-stu-id="01e74-139">Easy to implement.</span></span> <span data-ttu-id="01e74-140">Com as tecnologias atuais da Microsoft existentes, Microsoft Visual C++ sistema de desenvolvimento e o Active Template Library, uma extensão pode ser criada rapidamente.</span><span class="sxs-lookup"><span data-stu-id="01e74-140">With the current existing Microsoft technologies, Microsoft Visual C++ development system, and the Active Template Library, an extension can be created quickly.</span></span>
-   <span data-ttu-id="01e74-141">Os clientes exibem um IDispatch.</span><span class="sxs-lookup"><span data-stu-id="01e74-141">Clients view one IDispatch.</span></span> <span data-ttu-id="01e74-142">Da perspectiva dos gravadores de script e automação, os métodos e as propriedades de extensão são mesclados de forma transparente em um objeto ADSI.</span><span class="sxs-lookup"><span data-stu-id="01e74-142">From the perspective of script and Automation writers, the extension methods and properties are transparently blended into one ADSI object.</span></span>
-   <span data-ttu-id="01e74-143">Depende.</span><span class="sxs-lookup"><span data-stu-id="01e74-143">Independent.</span></span> <span data-ttu-id="01e74-144">Os gravadores de extensão podem estender de forma independente o ADSI sem conhecimento prévio das extensões existentes.</span><span class="sxs-lookup"><span data-stu-id="01e74-144">Extension writers can independently extend ADSI without prior knowledge of existing extensions.</span></span>

<span data-ttu-id="01e74-145">Considere este cenário: um desenvolvedor corporativo ou um ISV precisa desenvolver um programa de backup.</span><span class="sxs-lookup"><span data-stu-id="01e74-145">Consider this scenario: A corporate developer or an ISV needs to develop a backup program.</span></span> <span data-ttu-id="01e74-146">Esse aplicativo de backup permite que um administrador faça backup de todos os computadores em uma unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="01e74-146">This backup application enables an administrator to back up all computers in an organizational unit.</span></span> <span data-ttu-id="01e74-147">Com uma extensão ADSI, o script a seguir é possível.</span><span class="sxs-lookup"><span data-stu-id="01e74-147">With an ADSI extension, the following script is possible.</span></span>


```VB
Dim ou
On Error Resume Next
Set ou = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
If Err.Number<>0 Then
    MsgBox("An error has occurred.")
    Err.Clear
    Set ou = Nothing
    Exit Sub
End If

ou.Filter = Array("computer")

For each comp in ou
   Debug.Print comp.Get("networkAddress")
   Debug.Print comp.LastBackUp
   comp.BackUpNow
Next
```



<span data-ttu-id="01e74-148">**LastBackUp** é uma propriedade e **BackUpNow** é um método fornecido pelo gravador de extensão.</span><span class="sxs-lookup"><span data-stu-id="01e74-148">**LastBackUp** is a property and **BackUpNow** is a method that the extension writer provides.</span></span> <span data-ttu-id="01e74-149">O código mostra os benefícios para os consumidores de extensão e provedores.</span><span class="sxs-lookup"><span data-stu-id="01e74-149">The code shows the benefits for both extension consumers and providers.</span></span> <span data-ttu-id="01e74-150">O gravador de extensão não precisa criar uma nova maneira de filtrar, Pesquisar e acessar o diretório.</span><span class="sxs-lookup"><span data-stu-id="01e74-150">The extension writer does not have to create a new way of filtering, searching, and accessing the directory.</span></span> <span data-ttu-id="01e74-151">O consumidor de extensão não precisa aprender um novo paradigma de programação.</span><span class="sxs-lookup"><span data-stu-id="01e74-151">The extension consumer does not have to relearn a new programming paradigm.</span></span> <span data-ttu-id="01e74-152">Novos métodos e propriedades que o gravador de extensão fornece são exibidos como parte do ADSI.</span><span class="sxs-lookup"><span data-stu-id="01e74-152">New methods and properties that the extension writer provides are viewed as part of ADSI.</span></span>

 

 





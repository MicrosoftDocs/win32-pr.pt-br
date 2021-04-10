---
description: ACEs para controlar o acesso a uma propriedade de objetos
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACEs para controlar o acesso a uma propriedade de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169180"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a><span data-ttu-id="b4dce-103">ACEs para controlar o acesso às propriedades de um objeto</span><span class="sxs-lookup"><span data-stu-id="b4dce-103">ACEs to Control Access to an Object's Properties</span></span>

<span data-ttu-id="b4dce-104">A DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) de um objeto de serviço de diretório (DS) pode conter uma hierarquia de ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ), da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b4dce-104">The [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of a directory service (DS) object can contain a hierarchy of [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), as follows:</span></span>

1.  <span data-ttu-id="b4dce-105">ACEs que protegem o objeto em si</span><span class="sxs-lookup"><span data-stu-id="b4dce-105">ACEs that protect the object itself</span></span>
2.  <span data-ttu-id="b4dce-106">[ACEs específicas de objeto](object-specific-aces.md) que protegem uma propriedade especificada definida no objeto</span><span class="sxs-lookup"><span data-stu-id="b4dce-106">[Object-specific ACEs](object-specific-aces.md) that protect a specified property set on the object</span></span>
3.  <span data-ttu-id="b4dce-107">ACEs específicas de objeto que protegem uma propriedade especificada no objeto</span><span class="sxs-lookup"><span data-stu-id="b4dce-107">Object-specific ACEs that protect a specified property on the object</span></span>

<span data-ttu-id="b4dce-108">Nessa hierarquia, os direitos concedidos ou negados em um nível superior se aplicam também aos níveis inferiores.</span><span class="sxs-lookup"><span data-stu-id="b4dce-108">Within this hierarchy, the rights granted or denied at a higher level apply also to the lower levels.</span></span> <span data-ttu-id="b4dce-109">Por exemplo, se uma ACE específica a um objeto em um conjunto de propriedades permitir a confiança do \_ lado \_ direito de ler prop do DS \_ \_ , o objeto de confiança terá acesso de leitura implícito a todas as propriedades do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b4dce-109">For example, if an object-specific ACE on a property set allows a trustee the ADS\_RIGHT\_DS\_READ\_PROP right, the trustee has implicit read access to all of the properties of that property set.</span></span> <span data-ttu-id="b4dce-110">Da mesma forma, uma ACE no próprio objeto que permite aos anúncios \_ direito de \_ acesso de \_ prop de leitura do DS \_ fornece o acesso de leitura de confiança a todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="b4dce-110">Similarly, an ACE on the object itself that allows ADS\_RIGHT\_DS\_READ\_PROP access gives the trustee read access to all of the object's properties.</span></span>

<span data-ttu-id="b4dce-111">A ilustração a seguir mostra a árvore de um objeto DS hipotético e suas propriedades e conjuntos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b4dce-111">The following illustration shows the tree of a hypothetical DS object and its property sets and properties.</span></span>

![hierarquia de objetos do serviço de diretório](images/accctrl2.png)

<span data-ttu-id="b4dce-113">Suponha que você deseja permitir o seguinte acesso às propriedades deste objeto DS:</span><span class="sxs-lookup"><span data-stu-id="b4dce-113">Suppose you want to allow the following access to the properties of this DS object:</span></span>

-   <span data-ttu-id="b4dce-114">Permitir que o grupo tenha uma permissão de leitura/gravação para todas as propriedades do objeto</span><span class="sxs-lookup"><span data-stu-id="b4dce-114">Allow Group A read/write permission to all of the object's properties</span></span>
-   <span data-ttu-id="b4dce-115">Permitir que todos os outros usuários tenham permissão de leitura/gravação para todas as propriedades, exceto a propriedade D</span><span class="sxs-lookup"><span data-stu-id="b4dce-115">Allow everyone else read/write permission to all properties except Property D</span></span>

<span data-ttu-id="b4dce-116">Para fazer isso, defina as ACEs na DACL do objeto, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4dce-116">To do this, set the ACEs in the object's DACL as shown in the following table.</span></span>



| <span data-ttu-id="b4dce-117">Confiança</span><span class="sxs-lookup"><span data-stu-id="b4dce-117">Trustee</span></span>  | <span data-ttu-id="b4dce-118">GUID do objeto</span><span class="sxs-lookup"><span data-stu-id="b4dce-118">Object GUID</span></span>    | <span data-ttu-id="b4dce-119">Tipo de ACE</span><span class="sxs-lookup"><span data-stu-id="b4dce-119">ACE type</span></span>                  | <span data-ttu-id="b4dce-120">Direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="b4dce-120">Access rights</span></span>                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b4dce-121">Grupo A</span><span class="sxs-lookup"><span data-stu-id="b4dce-121">Group A</span></span>  | <span data-ttu-id="b4dce-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b4dce-122">None</span></span>           | <span data-ttu-id="b4dce-123">ACE permitida pelo acesso</span><span class="sxs-lookup"><span data-stu-id="b4dce-123">Access-allowed ACE</span></span>        | <span data-ttu-id="b4dce-124">ANÚNCIOS \_ direito \_ DS \_ ler \_ prop \| ADS \_ Right \_ DS \_ gravar \_ prop</span><span class="sxs-lookup"><span data-stu-id="b4dce-124">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="b4dce-125">Todos</span><span class="sxs-lookup"><span data-stu-id="b4dce-125">Everyone</span></span> | <span data-ttu-id="b4dce-126">Conjunto de propriedades 1</span><span class="sxs-lookup"><span data-stu-id="b4dce-126">Property Set 1</span></span> | <span data-ttu-id="b4dce-127">ACE de objeto permitido pelo Access</span><span class="sxs-lookup"><span data-stu-id="b4dce-127">Access-allowed object ACE</span></span> | <span data-ttu-id="b4dce-128">ANÚNCIOS \_ direito \_ DS \_ ler \_ prop \| ADS \_ Right \_ DS \_ gravar \_ prop</span><span class="sxs-lookup"><span data-stu-id="b4dce-128">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="b4dce-129">Todos</span><span class="sxs-lookup"><span data-stu-id="b4dce-129">Everyone</span></span> | <span data-ttu-id="b4dce-130">Propriedade C</span><span class="sxs-lookup"><span data-stu-id="b4dce-130">Property C</span></span>     | <span data-ttu-id="b4dce-131">ACE de objeto permitido pelo Access</span><span class="sxs-lookup"><span data-stu-id="b4dce-131">Access-allowed object ACE</span></span> | <span data-ttu-id="b4dce-132">ANÚNCIOS \_ direito \_ DS \_ ler \_ prop \| ADS \_ Right \_ DS \_ gravar \_ prop</span><span class="sxs-lookup"><span data-stu-id="b4dce-132">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |



 

<span data-ttu-id="b4dce-133">A ACE para o grupo A não tem um GUID de objeto, o que significa que ele permite o acesso a todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="b4dce-133">The ACE for Group A does not have an object GUID, which means that it allows access to all the object's properties.</span></span> <span data-ttu-id="b4dce-134">A ACE específica do objeto para o conjunto de propriedades 1 permite que todos acessem as propriedades A e B. A outra ACE específica do objeto permite que todos acessem a propriedade C. Observe que, embora essa DACL não tenha nenhuma ACE de acesso negado, ela nega implicitamente o acesso D da propriedade a todos, exceto o grupo A.</span><span class="sxs-lookup"><span data-stu-id="b4dce-134">The object-specific ACE for Property Set 1 allows everyone access to Properties A and B. The other object-specific ACE allows everyone access to Property C. Note that although this DACL does not have any access-denied ACEs, it implicitly denies Property D access to everyone except Group A.</span></span>

<span data-ttu-id="b4dce-135">Quando um usuário tenta acessar a propriedade de um objeto, o sistema verifica as ACEs, em ordem, até que o acesso solicitado seja explicitamente concedido, negado ou que não haja mais ACEs; nesse caso, o acesso é negado implicitamente.</span><span class="sxs-lookup"><span data-stu-id="b4dce-135">When a user tries to access an object's property, the system checks the ACEs, in order, until the requested access is explicitly granted, denied, or there are no more ACEs, in which case, access is implicitly denied.</span></span>

<span data-ttu-id="b4dce-136">O sistema avalia:</span><span class="sxs-lookup"><span data-stu-id="b4dce-136">The system evaluates:</span></span>

-   <span data-ttu-id="b4dce-137">ACEs que se aplicam ao próprio objeto</span><span class="sxs-lookup"><span data-stu-id="b4dce-137">ACEs that apply to the object itself</span></span>
-   <span data-ttu-id="b4dce-138">ACEs específicas de objeto que se aplicam ao conjunto de propriedades que contém a propriedade que está sendo acessada</span><span class="sxs-lookup"><span data-stu-id="b4dce-138">Object-specific ACEs that apply to the property set that contains the property being accessed</span></span>
-   <span data-ttu-id="b4dce-139">ACEs específicas de objeto que se aplicam à propriedade que está sendo acessada</span><span class="sxs-lookup"><span data-stu-id="b4dce-139">Object-specific ACEs that apply to the property being accessed</span></span>

<span data-ttu-id="b4dce-140">O sistema ignora ACEs específicas de objeto que se aplicam a outras propriedades ou conjuntos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b4dce-140">The system ignores object-specific ACEs that apply to other property sets or properties.</span></span>

 

 

---
title: Quando estender o esquema
description: Estenda o esquema somente se nenhuma classe de objeto existente atender aos requisitos do seu aplicativo. Estender o esquema é uma operação complexa; as alterações de esquema são replicadas para cada controlador de domínio na floresta da empresa. Considere isso com cuidado.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Quando estender o AD do esquema
- AD do esquema, quando estender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755906"
---
# <a name="when-to-extend-the-schema"></a><span data-ttu-id="09284-107">Quando estender o esquema</span><span class="sxs-lookup"><span data-stu-id="09284-107">When to Extend the Schema</span></span>

<span data-ttu-id="09284-108">Estenda o esquema somente se nenhuma classe de objeto existente atender aos requisitos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="09284-108">Extend the schema only if no existing object class fulfills the requirements of your application.</span></span> <span data-ttu-id="09284-109">Estender o esquema é uma operação complexa; as alterações de esquema são replicadas para cada controlador de domínio na floresta da empresa.</span><span class="sxs-lookup"><span data-stu-id="09284-109">Extending the schema is a complex operation; schema changes are replicated to every domain controller in the enterprise forest.</span></span> <span data-ttu-id="09284-110">Considere isso com cuidado.</span><span class="sxs-lookup"><span data-stu-id="09284-110">Consider this carefully.</span></span>

<span data-ttu-id="09284-111">O esquema pode ser estendido de três maneiras:</span><span class="sxs-lookup"><span data-stu-id="09284-111">The schema can be extended in three ways:</span></span>

-   <span data-ttu-id="09284-112">Derive uma nova subclasse de uma classe existente-a subclasse tem todos os atributos da superclasse e todos os atributos que você especificar.</span><span class="sxs-lookup"><span data-stu-id="09284-112">Derive a new subclass from an existing class - the subclass has all of the attributes of the superclass and any attributes you specify.</span></span> <span data-ttu-id="09284-113">Derive de uma classe existente:</span><span class="sxs-lookup"><span data-stu-id="09284-113">Derive from an existing class:</span></span>
    -   <span data-ttu-id="09284-114">Quando a classe existente requer atributos adicionais, mas, caso contrário, é aceitável.</span><span class="sxs-lookup"><span data-stu-id="09284-114">When the existing class requires additional attributes, but otherwise is acceptable.</span></span>
    -   <span data-ttu-id="09284-115">Quando a capacidade de transformar objetos existentes da classe em uma nova classe não é necessária.</span><span class="sxs-lookup"><span data-stu-id="09284-115">When the ability to transform existing objects of the class into a new class is not required.</span></span> <span data-ttu-id="09284-116">Não é possível adicionar uma subclasse a um objeto existente.</span><span class="sxs-lookup"><span data-stu-id="09284-116">It is not possible to add a subclass to an existing object.</span></span>
    -   <span data-ttu-id="09284-117">Para usar o snap-in Gerenciador de diretórios existente para gerenciar os atributos estendidos dos objetos.</span><span class="sxs-lookup"><span data-stu-id="09284-117">To use the existing Directory Manager snap-in to manage the extended attributes of the objects.</span></span>
-   <span data-ttu-id="09284-118">Adicione atributos a uma classe existente e/ou adicione objetos pai para a classe.</span><span class="sxs-lookup"><span data-stu-id="09284-118">Add attributes to an existing class and/or add parent objects for the class.</span></span> <span data-ttu-id="09284-119">Ao adicionar vários atributos, execute essa operação de maneira estruturada definindo uma classe auxiliar e adicionando essa classe auxiliar à classe existente.</span><span class="sxs-lookup"><span data-stu-id="09284-119">When adding multiple attributes, perform this operation in a structured manner by defining an auxiliary class and adding that auxiliary class to the existing class.</span></span>
-   <span data-ttu-id="09284-120">A modificação de uma classe existente é necessária quando um aplicativo requer a capacidade de estender objetos existentes da classe.</span><span class="sxs-lookup"><span data-stu-id="09284-120">Modification of an existing class is required when an application requires the ability to extend existing objects of the class.</span></span> <span data-ttu-id="09284-121">Por exemplo, para adicionar dados específicos do aplicativo ao objeto de usuário, estenda o usuário da classe normalmente, pois você deve lidar com usuários existentes e não apenas usuários especiais criados pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="09284-121">For example, to add application-specific data to the User object, extend the class User normally, because you must handle existing Users and not just special Users created by your application.</span></span>
-   <span data-ttu-id="09284-122">Crie uma nova classe com os atributos necessários.</span><span class="sxs-lookup"><span data-stu-id="09284-122">Create a new class with the required attributes.</span></span> <span data-ttu-id="09284-123">Criar uma nova classe; ou seja, uma classe derivada de "Top" quando nenhuma classe existente atende aos requisitos operacionais.</span><span class="sxs-lookup"><span data-stu-id="09284-123">Create a new class; that is, a class derived from "Top" when no existing class fulfills the operational requirements.</span></span>

<span data-ttu-id="09284-124">Quando você criar uma subclasse de uma classe existente, todos os itens da interface do usuário associados à classe original não serão herdados pela subclasse.</span><span class="sxs-lookup"><span data-stu-id="09284-124">When you subclass an existing class, any user interface items associated to the original class will not be inherited by the subclass.</span></span> <span data-ttu-id="09284-125">Por exemplo, se você subclasse de um objeto de usuário, as páginas de propriedades e os itens de menu associados ao usuário não serão herdados.</span><span class="sxs-lookup"><span data-stu-id="09284-125">For example, if you subclass a user object, the property pages and menu items associated to user are not inherited.</span></span> <span data-ttu-id="09284-126">Por esse motivo, é preferível estender um objeto existente ou criar uma classe auxiliar em vez de criar uma subclasse.</span><span class="sxs-lookup"><span data-stu-id="09284-126">For this reason, it is preferable to extend an existing object or create an auxiliary class rather than create a subclass.</span></span>

<span data-ttu-id="09284-127">Se você criar uma classe existente ou modificar uma classe existente, você desejará estender ferramentas como o snap-in Active Directory usuários e computadores para gerenciar os atributos estendidos dos objetos.</span><span class="sxs-lookup"><span data-stu-id="09284-127">Whether you subclass an existing class or modify an existing class, you will want to extend tools such as the Active Directory Users and Computers snap-in to manage the extended attributes of the objects.</span></span> <span data-ttu-id="09284-128">Para obter mais informações, consulte [estendendo a interface do usuário para objetos de diretório](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="09284-128">For more information, see [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

 

 





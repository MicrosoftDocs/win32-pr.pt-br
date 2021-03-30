---
title: Estendendo a interface do usuário para objetos de diretório
description: Com o Microsoft Windows 2000 e posterior, os snap-ins do MMC (console de gerenciamento Microsoft), como o snap-in Active Directory usuários e computadores, para administração do Active Directory Domain Services, estão disponíveis.
ms.assetid: 758ec25d-42ab-46ba-aa58-416d7ac8fd68
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, estendendo a interface do usuário
- AD de objetos, estendendo a interface do usuário para objetos de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d635132a26e80a63fddb35f779211308779f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634942"
---
# <a name="extending-the-user-interface-for-directory-objects"></a><span data-ttu-id="2c410-105">Estendendo a interface do usuário para objetos de diretório</span><span class="sxs-lookup"><span data-stu-id="2c410-105">Extending the User Interface for Directory Objects</span></span>

<span data-ttu-id="2c410-106">Com o Microsoft Windows 2000 e posterior, os snap-ins do MMC (console de gerenciamento Microsoft), como o snap-in Active Directory usuários e computadores, para administração do Active Directory Domain Services, estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2c410-106">With Microsoft Windows 2000 and later, Microsoft Management Console (MMC) snap-ins, such as the Active Directory Users and Computers snap-in, for administration of Active Directory Domain Services, are available.</span></span> <span data-ttu-id="2c410-107">Além disso, o Shell do Windows 2000 inclui interfaces do usuário (UIs) para localizar objetos que residem no diretório e as propriedades de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="2c410-107">In addition, the Windows 2000 shell includes user interfaces (UIs) for finding objects that reside in the directory and reading and writing properties.</span></span> <span data-ttu-id="2c410-108">Esta seção explica como estender a interface do usuário para exibir e gerenciar Active Directory Domain Services objetos no Shell do Windows e Active Directory snap-ins administrativos. Esta seção também aborda o que é necessário para implantar as extensões de interface do usuário para os desktops dos usuários.</span><span class="sxs-lookup"><span data-stu-id="2c410-108">This section explains how to extend the UI for viewing and managing Active Directory Domain Services objects in the Windows shell and Active Directory administrative snap-ins. This section also covers what is required to deploy the UI extensions to the user's desktops.</span></span>

<span data-ttu-id="2c410-109">Especificamente, esta seção aborda o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2c410-109">Specifically, this section discusses the following:</span></span>

-   [<span data-ttu-id="2c410-110">Sobre Active Directory interfaces de usuário</span><span class="sxs-lookup"><span data-stu-id="2c410-110">About Active Directory User Interfaces</span></span>](about-the-user-interfaces-of-active-directory-domain-services.md)
-   [<span data-ttu-id="2c410-111">Exibir especificadores</span><span class="sxs-lookup"><span data-stu-id="2c410-111">Display Specifiers</span></span>](display-specifiers.md)
-   [<span data-ttu-id="2c410-112">Nomes de exibição de classe e atributo</span><span class="sxs-lookup"><span data-stu-id="2c410-112">Class and Attribute Display Names</span></span>](class-and-attribute-display-names.md)
-   [<span data-ttu-id="2c410-113">Ícones de classe</span><span class="sxs-lookup"><span data-stu-id="2c410-113">Class Icons</span></span>](class-icons.md)
-   [<span data-ttu-id="2c410-114">Exibindo contêineres como nós folha</span><span class="sxs-lookup"><span data-stu-id="2c410-114">Viewing Containers as Leaf Nodes</span></span>](viewing-containers-as-leaf-nodes.md)
-   [<span data-ttu-id="2c410-115">Modificando as interfaces de usuário existentes</span><span class="sxs-lookup"><span data-stu-id="2c410-115">Modifying Existing User Interfaces</span></span>](modifying-existing-user-interfaces.md)
-   [<span data-ttu-id="2c410-116">Extensão da interface do usuário para novas classes de objeto</span><span class="sxs-lookup"><span data-stu-id="2c410-116">User Interface Extension for New Object Classes</span></span>](user-interface-extension-for-new-object-classes.md)
-   [<span data-ttu-id="2c410-117">Páginas de propriedades para uso com especificadores de exibição</span><span class="sxs-lookup"><span data-stu-id="2c410-117">Property Pages for Use with Display Specifiers</span></span>](property-pages-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="2c410-118">Menus de contexto para uso com especificadores de exibição</span><span class="sxs-lookup"><span data-stu-id="2c410-118">Context Menus for Use with Display Specifiers</span></span>](context-menus-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="2c410-119">Assistentes de criação de objeto</span><span class="sxs-lookup"><span data-stu-id="2c410-119">Object Creation Wizards</span></span>](object-creation-wizards.md)
-   [<span data-ttu-id="2c410-120">Usando caixas de diálogo padrão para manipular objetos no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="2c410-120">Using Standard Dialog Boxes for Handling Objects in Active Directory Domain Services</span></span>](using-standard-dialog-boxes-to-handle-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="2c410-121">Manipuladores de notificação administrativa</span><span class="sxs-lookup"><span data-stu-id="2c410-121">Administrative Notification Handlers</span></span>](administrative-notification-handlers.md)
-   [<span data-ttu-id="2c410-122">Distribuindo componentes da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="2c410-122">Distributing User Interface Components</span></span>](distributing-user-interface-components.md)
-   [<span data-ttu-id="2c410-123">Como os aplicativos devem usar especificadores de exibição</span><span class="sxs-lookup"><span data-stu-id="2c410-123">How Applications Should Use Display Specifiers</span></span>](how-applications-should-use-display-specifiers.md)
-   [<span data-ttu-id="2c410-124">Depurando uma extensão de Active Directory</span><span class="sxs-lookup"><span data-stu-id="2c410-124">Debugging an Active Directory Extension</span></span>](debugging-an-active-directory-extension.md)

 

 





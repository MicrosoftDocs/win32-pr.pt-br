---
description: Os módulos de mesclagem fornecem um método padrão pelo qual os desenvolvedores fornecem componentes de Windows Installer compartilhados e a lógica de instalação para seus aplicativos.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Mesclar módulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171832"
---
# <a name="merge-modules"></a><span data-ttu-id="32a61-103">Mesclar módulos</span><span class="sxs-lookup"><span data-stu-id="32a61-103">Merge Modules</span></span>

<span data-ttu-id="32a61-104">Os módulos de mesclagem fornecem um método padrão pelo qual os desenvolvedores fornecem [*componentes*](c-gly.md) de Windows Installer compartilhados e a lógica de instalação para seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="32a61-104">Merge modules provide a standard method by which developers deliver shared Windows Installer [*components*](c-gly.md) and setup logic to their applications.</span></span> <span data-ttu-id="32a61-105">Os módulos de mesclagem são usados para fornecer código compartilhado, arquivos, recursos, entradas de registro e lógica de instalação para aplicativos como um único arquivo composto.</span><span class="sxs-lookup"><span data-stu-id="32a61-105">Merge modules are used to deliver shared code, files, resources, registry entries, and setup logic to applications as a single compound file.</span></span> <span data-ttu-id="32a61-106">Os desenvolvedores que criam novos módulos de mesclagem ou usam módulos de mesclagem existentes devem seguir o padrão descrito nesta seção.</span><span class="sxs-lookup"><span data-stu-id="32a61-106">Developers authoring new merge modules or using existing merge modules should follow the standard outlined in this section.</span></span>

<span data-ttu-id="32a61-107">Um módulo de mesclagem é semelhante na estrutura a um [*arquivo Windows Installer. msi*](m-gly.md)simplificado.</span><span class="sxs-lookup"><span data-stu-id="32a61-107">A merge module is similar in structure to a simplified Windows Installer [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="32a61-108">No entanto, um módulo de mesclagem não pode ser instalado sozinho, ele deve ser mesclado em um pacote de instalação usando uma ferramenta de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="32a61-108">However, a merge module cannot be installed alone, it must be merged into an installation package using a merge tool.</span></span> <span data-ttu-id="32a61-109">Os desenvolvedores que desejam usar módulos de mesclagem devem obter uma das ferramentas de mesclagem distribuídas livremente, como Mergemod.dll ou comprar uma ferramenta de mesclagem de um fornecedor de software independente.</span><span class="sxs-lookup"><span data-stu-id="32a61-109">Developers wanting to use merge modules must obtain one of the freely distributed merge tools, such as Mergemod.dll, or purchase a merge tool from an independent software vendor.</span></span> <span data-ttu-id="32a61-110">Os desenvolvedores podem criar novos módulos de mesclagem usando muitas das mesmas ferramentas de software usadas para criar um pacote de instalação Windows Installer, como o editor de tabela de banco de dados Orca fornecido com o SDK do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="32a61-110">Developers can create new merge modules by using many of the same software tools used to create a Windows Installer installation package, such as the database table editor Orca provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="32a61-111">Quando um módulo de mesclagem é mesclado no arquivo. msi de um aplicativo, todas as informações e os recursos necessários para instalar os componentes entregues pelo módulo de mesclagem são incorporados ao arquivo. msi do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="32a61-111">When a merge module is merged into the .msi file of an application, all the information and resources required to install the components delivered by the merge module are incorporated into the application's .msi file.</span></span> <span data-ttu-id="32a61-112">O módulo de mesclagem não é mais necessário para instalar esses componentes e o módulo de mesclagem não precisa estar acessível a um usuário.</span><span class="sxs-lookup"><span data-stu-id="32a61-112">The merge module is then no longer required to install these components and the merge module does not need to be accessible to a user.</span></span> <span data-ttu-id="32a61-113">Como todas as informações necessárias para instalar os componentes são entregues como um único arquivo, o uso de módulos de mesclagem pode eliminar muitas instâncias de conflitos de versão, entradas de registro ausentes e arquivos instalados incorretamente.</span><span class="sxs-lookup"><span data-stu-id="32a61-113">Because all the information needed to install the components is delivered as a single file, the use of merge modules can eliminate many instances of version conflicts, missing registry entries, and improperly installed files.</span></span>

<span data-ttu-id="32a61-114">Para obter mais informações sobre módulos de mesclagem, consulte:</span><span class="sxs-lookup"><span data-stu-id="32a61-114">For more information about merge modules, see:</span></span>

-   [<span data-ttu-id="32a61-115">Sobre módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="32a61-115">About Merge Modules</span></span>](about-merge-modules.md)
-   [<span data-ttu-id="32a61-116">Usando módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="32a61-116">Using Merge Modules</span></span>](using-merge-modules.md)
-   [<span data-ttu-id="32a61-117">Referência de módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="32a61-117">Merge Module Reference</span></span>](merge-module-reference.md)

 

 




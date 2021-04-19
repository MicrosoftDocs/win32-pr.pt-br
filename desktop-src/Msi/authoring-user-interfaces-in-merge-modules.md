---
description: Os módulos de mesclagem raramente exigem uma interface do usuário.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Criando interfaces de usuário em módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764665"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a><span data-ttu-id="32f79-103">Criando interfaces de usuário em módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="32f79-103">Authoring User Interfaces in Merge Modules</span></span>

<span data-ttu-id="32f79-104">Os módulos de mesclagem raramente exigem uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="32f79-104">Merge modules rarely require a user interface.</span></span> <span data-ttu-id="32f79-105">A liberação de um módulo de mesclagem que contém ambos os componentes instaláveis e uma interface do usuário restringe, por fim, a flexibilidade do usuário do módulo.</span><span class="sxs-lookup"><span data-stu-id="32f79-105">Releasing a merge module that contains both installable components and a user interface ultimately restricts the flexibility of the module user.</span></span> <span data-ttu-id="32f79-106">A combinação dos componentes e da interface do usuário em um módulo pode impedir que os desenvolvedores usem sua própria interface do usuário ou forneçam instalações silenciosas.</span><span class="sxs-lookup"><span data-stu-id="32f79-106">Combining both components and UI into one module can prevent developers from using their own UI or from providing silent installations.</span></span> <span data-ttu-id="32f79-107">Uma alternativa melhor é lançar dois módulos de mesclagem, um que instala silenciosamente os componentes e um segundo módulo opcional que contém a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="32f79-107">A better alternative is to release two merge modules, one that silently installs the components and a second optional module that contains the UI.</span></span> <span data-ttu-id="32f79-108">O módulo com a interface do usuário deve listar o módulo de componente em sua [tabela ModuleDependency](moduledependency-table.md).</span><span class="sxs-lookup"><span data-stu-id="32f79-108">The module with the UI should list the component module in its [ModuleDependency table](moduledependency-table.md).</span></span> <span data-ttu-id="32f79-109">Esse método permite que os autores de módulo forneçam uma interface do usuário sem forçá-lo a desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="32f79-109">This method enables module authors to provide a UI without forcing it on developers.</span></span>

<span data-ttu-id="32f79-110">Quando as tabelas de interface do usuário são usadas em módulos de mesclagem, elas podem ser mescladas da mesma maneira que qualquer outra tabela.</span><span class="sxs-lookup"><span data-stu-id="32f79-110">When UI tables are used in merge modules they can be merged in the same way as any other tables.</span></span>

 

 




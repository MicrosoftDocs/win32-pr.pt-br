---
description: Quando um módulo dá suporte a vários idiomas, você pode mesclá-lo no mesmo Windows Installer banco de dados várias vezes, mas certifique-se de que cada mesclagem usa um idioma diferente.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Mesclar um módulo de vários idiomas no mesmo pacote várias vezes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792496"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a><span data-ttu-id="04d2b-103">Mesclar um módulo de vários idiomas no mesmo pacote várias vezes</span><span class="sxs-lookup"><span data-stu-id="04d2b-103">Merging a Multiple Language Module into the Same Package Multiple Times</span></span>

<span data-ttu-id="04d2b-104">Quando um módulo dá suporte a vários idiomas, você pode mesclá-lo no mesmo Windows Installer banco de dados várias vezes, mas certifique-se de que cada mesclagem usa um idioma diferente.</span><span class="sxs-lookup"><span data-stu-id="04d2b-104">When a module supports multiple languages, you can merge it into the same Windows Installer database multiple times, but make sure that each merge uses a different language.</span></span> <span data-ttu-id="04d2b-105">Antes de cada mesclagem, solicite um idioma diferente do módulo.</span><span class="sxs-lookup"><span data-stu-id="04d2b-105">Before each merge, request a different language from the module.</span></span> <span data-ttu-id="04d2b-106">O banco de dados. msi resultante tem um registro na [tabela ModuleSignature](modulesignature-table.md) para cada mesclagem do módulo.</span><span class="sxs-lookup"><span data-stu-id="04d2b-106">The resulting .msi database then has a record in the [ModuleSignature Table](modulesignature-table.md) for each merge of the module.</span></span> <span data-ttu-id="04d2b-107">Os componentes compartilhados entre os idiomas existem apenas uma vez na [tabela de componentes](component-table.md), mas são associados a cada idioma na [tabela ModuleComponents](modulecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="04d2b-107">Components that are shared between languages exist only one time in the [Component Table](component-table.md), but are associated with each language in the [ModuleComponents Table](modulecomponents-table.md).</span></span>

<span data-ttu-id="04d2b-108">Ao mesclar vários idiomas de um módulo no mesmo pacote, cada mesclagem deve satisfazer as mesmas restrições em páginas de código como módulos de linguagem única.</span><span class="sxs-lookup"><span data-stu-id="04d2b-108">When merging multiple languages of a module into the same package, each merge must satisfy the same restrictions on code pages as single-language modules.</span></span> <span data-ttu-id="04d2b-109">Os módulos não podem conter cadeias de caracteres em páginas de código diferentes.</span><span class="sxs-lookup"><span data-stu-id="04d2b-109">The modules cannot contain strings in different code pages.</span></span>

<span data-ttu-id="04d2b-110">Ao mesclar um módulo várias vezes em um único arquivo. msi, talvez seja necessário modificar a ordem dos arquivos na tabela de [arquivos](file-table.md) para usar o. cab existente do módulo diretamente em sua instalação.</span><span class="sxs-lookup"><span data-stu-id="04d2b-110">When merging a module multiple times into a single .msi file, you may need to modify the order of the files in the [File Table](file-table.md) to use the existing .cab from the module directly in your installation.</span></span> <span data-ttu-id="04d2b-111">A ordem dos arquivos na tabela de arquivos deve corresponder à ordem dos arquivos no. cab.</span><span class="sxs-lookup"><span data-stu-id="04d2b-111">The order of files in the File Table must match the order of files in the .cab.</span></span> <span data-ttu-id="04d2b-112">Ao mesclar um módulo várias vezes em um banco de dados de instalação, a sequência pode ser modificada, pois os arquivos compartilhados entre os idiomas podem já existir no módulo de uma mesclagem anterior e têm um número de sequência relativo diferente.</span><span class="sxs-lookup"><span data-stu-id="04d2b-112">When merging a module multiple times into an installation database the sequence may be modified, because files shared between the languages may already exist in the module from a prior merge, and they have a different relative sequence number.</span></span>

 

 




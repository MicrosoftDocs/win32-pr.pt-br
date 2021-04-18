---
description: Os diretórios na tabela de diretórios especificam o layout de uma instalação.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Usando uma propriedade de diretório em um caminho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758613"
---
# <a name="using-a-directory-property-in-a-path"></a><span data-ttu-id="f9128-103">Usando uma propriedade de diretório em um caminho</span><span class="sxs-lookup"><span data-stu-id="f9128-103">Using a Directory Property in a Path</span></span>

<span data-ttu-id="f9128-104">Os diretórios na [tabela de diretórios](directory-table.md) especificam o layout de uma instalação.</span><span class="sxs-lookup"><span data-stu-id="f9128-104">The directories in the [Directory table](directory-table.md) specify the layout of an installation.</span></span> <span data-ttu-id="f9128-105">Quando o Windows Installer resolve esses diretórios durante a [ação CostFinalize](costfinalize-action.md), as chaves na tabela de diretório tornam-se [Propriedades](properties.md) definidas como caminhos de diretório.</span><span class="sxs-lookup"><span data-stu-id="f9128-105">When the Windows Installer resolves these directories during the [CostFinalize action](costfinalize-action.md), the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span> <span data-ttu-id="f9128-106">O instalador também define um número de propriedades de [pasta do sistema](property-reference.md) padrão para caminhos de pasta do sistema.</span><span class="sxs-lookup"><span data-stu-id="f9128-106">The installer also always sets a number of standard [System Folder Properties](property-reference.md) to system folder paths.</span></span>

<span data-ttu-id="f9128-107">Os valores das [Propriedades da pasta do sistema](property-reference.md) são garantidos para terminar em um separador de diretório.</span><span class="sxs-lookup"><span data-stu-id="f9128-107">The values of the [System Folder Properties](property-reference.md) are guaranteed to end in a directory separator.</span></span> <span data-ttu-id="f9128-108">Os valores de todas as outras propriedades inseridas na [tabela de diretórios](directory-table.md) só são garantidos para terminar em um separador de diretório depois que o instalador tiver executado a [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="f9128-108">The values of all other properties entered in the [Directory table](directory-table.md) are only guaranteed to end in a directory separator after the installer has run the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="f9128-109">Antes que o custo seja concluído, os valores das propriedades inseridas na tabela de diretório que não são [Propriedades da pasta do sistema](property-reference.md) podem não terminar em um separador de diretório.</span><span class="sxs-lookup"><span data-stu-id="f9128-109">Before costing has completed, the values of properties entered in the Directory table which are not [System Folder Properties](property-reference.md) may not end in a directory separator.</span></span> <span data-ttu-id="f9128-110">Portanto, se a instalação definir propriedades de diretório usando [ações personalizadas](custom-actions.md) no pacote, os valores na referência poderão não terminar com um separador de diretório.</span><span class="sxs-lookup"><span data-stu-id="f9128-110">Therefore, if your installation sets directory properties using [custom actions](custom-actions.md) in the package, the values on reference might not end with a directory separator.</span></span>

<span data-ttu-id="f9128-111">Propriedades de diretório terminando com um separador de diretório podem, portanto, ser usadas em uma cadeia de caracteres de caminho sem incluir explicitamente o separador de diretório</span><span class="sxs-lookup"><span data-stu-id="f9128-111">Directory properties ending with a directory separator can therefore be used in a path string without explicitly including the directory separator.</span></span> <span data-ttu-id="f9128-112">Por exemplo, se o valor de DirectoryProperty terminar com um separador de diretório, a cadeia de caracteres a seguir especificará corretamente o caminho para o *arquivo* no *subdiretório*</span><span class="sxs-lookup"><span data-stu-id="f9128-112">For example, if the value of DirectoryProperty ends with a directory separator, the following string correctly specifies the path to *file* in *subdirectory*</span></span>

``` syntax
[DirectoryProperty]subdirectory\file
```

<span data-ttu-id="f9128-113">e a cadeia de caracteres de caminho a seguir está incorreta.</span><span class="sxs-lookup"><span data-stu-id="f9128-113">and the following path string is incorrect.</span></span>

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 




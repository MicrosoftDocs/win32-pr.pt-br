---
description: Se nenhum arquivo tiver um número de versão, o Windows Installer usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Nenhum arquivo tem uma versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5360bb7b6b4deda54156006073f353ab65ab2b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566959"
---
# <a name="neither-file-has-a-version"></a><span data-ttu-id="00678-103">Nenhum arquivo tem uma versão</span><span class="sxs-lookup"><span data-stu-id="00678-103">Neither File Has a Version</span></span>

<span data-ttu-id="00678-104">Se o arquivo de chave de um componente que está sendo instalado (cópia-A) tiver o mesmo nome que um arquivo já instalado no local de destino (cópia-B), o instalador compara o número de versão, a data e o idioma dos dois arquivos.</span><span class="sxs-lookup"><span data-stu-id="00678-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="00678-105">Se nenhum arquivo tiver um número de versão, o instalador usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="00678-105">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="00678-106">Como o instalador instala apenas componentes inteiros, se o arquivo de chave instalado for substituído, todos os arquivos do componente serão substituídos.</span><span class="sxs-lookup"><span data-stu-id="00678-106">Because the installer only installs entire components, if the installed key file is replaced, then all of the component's files are replaced.</span></span>

<span data-ttu-id="00678-107">Observe que este diagrama ilustra as [regras de controle de versão de arquivo](file-versioning-rules.md)padrão, que podem ser substituídas definindo a propriedade [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="00678-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="00678-108">O valor padrão da propriedade **REinstallmode** é "omus".</span><span class="sxs-lookup"><span data-stu-id="00678-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![regras de controle de versão de arquivo padrão quando nenhum arquivo tem um número de versão](images/waiflow2.png)

<span data-ttu-id="00678-110">Consulte os exemplos de controle de versão de arquivo padrão em [substituindo arquivos existentes](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="00678-110">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="00678-111">Ambos os arquivos têm uma versão</span><span class="sxs-lookup"><span data-stu-id="00678-111">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="00678-112">Nenhum arquivo tem uma versão com verificação de hash de arquivo</span><span class="sxs-lookup"><span data-stu-id="00678-112">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="00678-113">Um arquivo tem uma versão</span><span class="sxs-lookup"><span data-stu-id="00678-113">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 




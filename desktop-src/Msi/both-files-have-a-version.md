---
description: Se ambos os arquivos tiverem um número de versão, o Windows Installer usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Ambos os arquivos têm uma versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828044"
---
# <a name="both-files-have-a-version"></a><span data-ttu-id="32215-103">Ambos os arquivos têm uma versão</span><span class="sxs-lookup"><span data-stu-id="32215-103">Both Files Have a Version</span></span>

<span data-ttu-id="32215-104">Se o arquivo de chave de um componente que está sendo instalado (cópia-A) tiver o mesmo nome que um arquivo já instalado no local de destino (cópia-B), o instalador compara o número de versão e o idioma dos dois arquivos.</span><span class="sxs-lookup"><span data-stu-id="32215-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number and language of the two files.</span></span>

<span data-ttu-id="32215-105">Se ambos os arquivos tiverem um número de versão, o instalador usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="32215-105">If both files have a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="32215-106">Como o instalador instala apenas componentes inteiros, se o arquivo de chave instalado for substituído, todos os arquivos do componente serão substituídos.</span><span class="sxs-lookup"><span data-stu-id="32215-106">Because the installer only installs entire components, if the installed key file is replaced then all of the component's files are replaced.</span></span>

<span data-ttu-id="32215-107">Observe que este diagrama ilustra as [regras de controle de versão de arquivo](file-versioning-rules.md)padrão, que podem ser substituídas definindo a propriedade [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="32215-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="32215-108">O valor padrão da propriedade **REinstallmode** é "omus".</span><span class="sxs-lookup"><span data-stu-id="32215-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![regras de controle de versão de arquivo padrão quando ambos os arquivos têm o mesmo nome ou número de versão](images/waiflow1.png)

<span data-ttu-id="32215-110">O diagrama anterior também pode ser usado com arquivos sem nenhum idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="32215-110">The previous diagram can also be used with files with no language specified.</span></span> <span data-ttu-id="32215-111">Se Copy-A tiver um idioma especificado e Copy-B não tiver um idioma especificado, Copy-B será substituído por Copy-A.</span><span class="sxs-lookup"><span data-stu-id="32215-111">If copy-A has a specified language and copy-B has no specified language, copy-B is replaced with copy-A.</span></span> <span data-ttu-id="32215-112">Se Copy-A e Copy-B não tiverem nenhum idioma especificado, Copy-B não será substituído.</span><span class="sxs-lookup"><span data-stu-id="32215-112">If copy-A and copy-B both have no language specified, then copy-B is not replaced.</span></span>

<span data-ttu-id="32215-113">Consulte exemplos de controle de versão de arquivo padrão ao [substituir arquivos existentes](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="32215-113">See examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="32215-114">Nenhum arquivo tem uma versão</span><span class="sxs-lookup"><span data-stu-id="32215-114">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="32215-115">Nenhum arquivo tem uma versão com verificação de hash de arquivo</span><span class="sxs-lookup"><span data-stu-id="32215-115">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="32215-116">Um arquivo tem uma versão</span><span class="sxs-lookup"><span data-stu-id="32215-116">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 




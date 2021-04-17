---
description: O hash de arquivo está disponível com Windows Installer. Para obter mais informações, consulte MsiGetFileHash e a tabela MsiFileHash. A tabela MsiFileHash só pode ser usada com arquivos sem versão.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Nenhum arquivo tem uma versão com verificação de hash de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502362"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a><span data-ttu-id="aaa1e-105">Nenhum arquivo tem uma versão com verificação de hash de arquivo</span><span class="sxs-lookup"><span data-stu-id="aaa1e-105">Neither File Has a Version with File Hash Check</span></span>

<span data-ttu-id="aaa1e-106">O hash de arquivo está disponível com Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-106">File hashing is available with Windows Installer.</span></span> <span data-ttu-id="aaa1e-107">Para obter mais informações, consulte [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e a [tabela MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="aaa1e-107">For more information, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="aaa1e-108">A tabela MsiFileHash só pode ser usada com arquivos sem versão.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-108">The MsiFileHash table can only be used with unversioned files.</span></span>

<span data-ttu-id="aaa1e-109">Se o arquivo de chave de um componente que está sendo instalado (cópia-A) tiver o mesmo nome que um arquivo já instalado no local de destino (cópia-B), o instalador compara o número de versão, a data e o idioma dos dois arquivos.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-109">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="aaa1e-110">Se nenhum arquivo tiver um número de versão, o instalador usará a lógica ilustrada pelo seguinte diagrama de fluxo para determinar se todos os arquivos instalados pertencentes ao componente devem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-110">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="aaa1e-111">Como o instalador instala apenas componentes inteiros, se o arquivo de chave instalado for substituído, todos os arquivos do componente serão substituídos.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-111">Because the installer only installs entire components, if the installed key file is replaced then, all of the component's files are replaced.</span></span>

<span data-ttu-id="aaa1e-112">Observe que este diagrama ilustra as [regras de controle de versão de arquivo](file-versioning-rules.md)padrão, que podem ser substituídas definindo a propriedade [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="aaa1e-112">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="aaa1e-113">O valor padrão da propriedade **REinstallmode** é "omus".</span><span class="sxs-lookup"><span data-stu-id="aaa1e-113">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![regras de controle de versão de arquivo padrão quando substituídas pela configuração da propriedade REINSTALLMODE](images/waiflow2b.png)

<span data-ttu-id="aaa1e-115">Consulte os exemplos de controle de versão de arquivo padrão em [substituindo arquivos existentes](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="aaa1e-115">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="aaa1e-116">Ambos os arquivos têm uma versão</span><span class="sxs-lookup"><span data-stu-id="aaa1e-116">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="aaa1e-117">Nenhum arquivo tem uma versão</span><span class="sxs-lookup"><span data-stu-id="aaa1e-117">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="aaa1e-118">Um arquivo tem uma versão</span><span class="sxs-lookup"><span data-stu-id="aaa1e-118">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 




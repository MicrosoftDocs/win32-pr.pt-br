---
description: Os desenvolvedores criam um pacote de patch gerando um arquivo de criação de patch e usando Msimsp.exe para chamar a função UiCreatePatchPackageEx no Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Criando um pacote de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169867"
---
# <a name="creating-a-patch-package"></a><span data-ttu-id="a7385-103">Criando um pacote de patch</span><span class="sxs-lookup"><span data-stu-id="a7385-103">Creating a Patch Package</span></span>

<span data-ttu-id="a7385-104">Os desenvolvedores criam um pacote de patch gerando um arquivo de criação de patch e usando [Msimsp.exe](msimsp-exe.md) para chamar a função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) no [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a7385-104">Developers create a patch package by generating a patch creation file and using [Msimsp.exe](msimsp-exe.md) to call the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="a7385-105">Msimsp.exe e Patchwiz.dll são fornecidos no SDK do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a7385-105">Msimsp.exe and Patchwiz.dll are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="a7385-106">Para obter mais informações, consulte [um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="a7385-106">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="a7385-107">Como o aplicativo de um patch para um pacote de Windows Installer resulta na instalação das fontes originais usando um novo arquivo. msi, o novo arquivo. msi deve permanecer compatível com o layout da fonte original.</span><span class="sxs-lookup"><span data-stu-id="a7385-107">Because the application of a patch to a Windows Installer package results in the installation of the original sources using a new .msi file, the new .msi file must remain compatible with the layout of the original source.</span></span>

<span data-ttu-id="a7385-108">Quando você cria um pacote de patch, deve usar uma imagem de instalação descompactada para criar um patch, por exemplo, uma imagem administrativa ou uma imagem de instalação descompactada de um CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="a7385-108">When you author a patch package you must use an uncompressed setup image to create a patch, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="a7385-109">Você também deve aderir às seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="a7385-109">You must also adhere to the following restrictions:</span></span>

-   <span data-ttu-id="a7385-110">Não mova arquivos de uma pasta para outra.</span><span class="sxs-lookup"><span data-stu-id="a7385-110">Do not move files from one folder to another.</span></span>
-   <span data-ttu-id="a7385-111">Não mova arquivos de um gabinete para outro.</span><span class="sxs-lookup"><span data-stu-id="a7385-111">Do not move files from one cabinet to another.</span></span>
-   <span data-ttu-id="a7385-112">Não altere a ordem dos arquivos em um gabinete.</span><span class="sxs-lookup"><span data-stu-id="a7385-112">Do not change the order of files in a cabinet.</span></span>
-   <span data-ttu-id="a7385-113">Não altere o número de sequência de arquivos existentes.</span><span class="sxs-lookup"><span data-stu-id="a7385-113">Do not change the sequence number of existing files.</span></span> <span data-ttu-id="a7385-114">O número de sequência é o valor especificado na coluna sequência da [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="a7385-114">The sequence number is the value specified in the Sequence column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="a7385-115">Todos os novos arquivos adicionados pelo patch devem ser colocados no final da sequência de arquivos existente.</span><span class="sxs-lookup"><span data-stu-id="a7385-115">Any new files that are added by the patch must be placed at the end of the existing file sequence.</span></span> <span data-ttu-id="a7385-116">O número de sequência de qualquer arquivo novo na imagem atualizada deve ser maior que o maior número de sequência de arquivos existentes na imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="a7385-116">The sequence number of any new file in the upgraded image must be greater than the largest sequence number of existing files in the target image.</span></span>
-   <span data-ttu-id="a7385-117">Não altere as chaves primárias na [tabela de arquivos](file-table.md) entre as versões original e nova do arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="a7385-117">Do not change the primary keys in the [File Table](file-table.md) between the original and new .msi file versions.</span></span>
    > [!Note]  
    > <span data-ttu-id="a7385-118">O arquivo deve ter a mesma chave na [tabela de arquivos](file-table.md) da imagem de destino e da imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="a7385-118">The file must have the same key in the [File Table](file-table.md) of both the target image and the updated image.</span></span> <span data-ttu-id="a7385-119">Os valores de cadeia de caracteres na coluna arquivo de ambas as tabelas devem ser idênticos, incluindo o caso.</span><span class="sxs-lookup"><span data-stu-id="a7385-119">The string values in the File column of both tables must be identical, including the case.</span></span>

     

-   <span data-ttu-id="a7385-120">Não crie um pacote com chaves de [tabela de arquivos](file-table.md) que diferem apenas em maiúsculas e minúsculas, por exemplo, evite o exemplo de tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7385-120">Do not author a package with [File Table](file-table.md) keys that differ only in case, for example, avoid the following table example.</span></span>

    

    | <span data-ttu-id="a7385-121">Arquivo</span><span class="sxs-lookup"><span data-stu-id="a7385-121">File</span></span>       | <span data-ttu-id="a7385-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="a7385-122">Component\_</span></span> | <span data-ttu-id="a7385-123">FileName</span><span class="sxs-lookup"><span data-stu-id="a7385-123">FileName</span></span>   |
    |------------|-------------|------------|
    | <span data-ttu-id="a7385-124">readme.txt</span><span class="sxs-lookup"><span data-stu-id="a7385-124">readme.txt</span></span> | <span data-ttu-id="a7385-125">Comp1</span><span class="sxs-lookup"><span data-stu-id="a7385-125">Comp1</span></span>       | <span data-ttu-id="a7385-126">readme.txt</span><span class="sxs-lookup"><span data-stu-id="a7385-126">readme.txt</span></span> |
    | <span data-ttu-id="a7385-127">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="a7385-127">ReadMe.txt</span></span> | <span data-ttu-id="a7385-128">Comp2</span><span class="sxs-lookup"><span data-stu-id="a7385-128">Comp2</span></span>       | <span data-ttu-id="a7385-129">readme.txt</span><span class="sxs-lookup"><span data-stu-id="a7385-129">readme.txt</span></span> |

    

     

    <span data-ttu-id="a7385-130">O Windows Installer pode permitir o exemplo de tabela anterior quando comp1 e Comp2 são instalados em diretórios diferentes, mas você não pode usar [Msimsp.exe](msimsp-exe.md) ou [Patchwiz.dll](patchwiz-dll.md) para gerar um patch para o pacote.</span><span class="sxs-lookup"><span data-stu-id="a7385-130">The Windows Installer can allow the previous table example when Comp1 and Comp2 are installed on different directories, but then you cannot use [Msimsp.exe](msimsp-exe.md) or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package.</span></span> <span data-ttu-id="a7385-131">Msimsp.exe e Patchwiz.dll chamada Makecab.exe, que não diferencia maiúsculas de minúsculas e falha.</span><span class="sxs-lookup"><span data-stu-id="a7385-131">Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive and fails.</span></span>

    <span data-ttu-id="a7385-132">Ao usar módulos de mesclagem na configuração, verifique se os números de sequência de arquivo e o layout aderem às diretrizes acima.</span><span class="sxs-lookup"><span data-stu-id="a7385-132">When using merge modules in the setup, ensure that file sequence numbers and layout adhere to the above guidelines.</span></span>

 

 




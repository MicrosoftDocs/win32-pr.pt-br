---
description: Uma tabela de arquivos é necessária em cada módulo de mesclagem e deve ter um registro para cada arquivo que está sendo entregue ao pacote de instalação de destino pelo módulo de mesclagem.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Criando tabelas de arquivos do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010914"
---
# <a name="authoring-merge-module-file-tables"></a><span data-ttu-id="2672a-103">Criando tabelas de arquivos do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="2672a-103">Authoring Merge Module File Tables</span></span>

<span data-ttu-id="2672a-104">Uma [tabela de arquivos](file-table.md) é necessária em cada módulo de mesclagem e deve ter um registro para cada arquivo que está sendo entregue ao pacote de instalação de destino pelo módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="2672a-104">A [File Table](file-table.md) is required in every merge module, and should have a record for each file that is being delivered to the target installation package by the merge module.</span></span> <span data-ttu-id="2672a-105">Quando o módulo de mesclagem é mesclado em um arquivo. msi, cada arquivo na tabela de arquivos do módulo de mesclagem é armazenado dentro de um [*arquivo de gabinete*](c-gly.md) no arquivo. msm.</span><span class="sxs-lookup"><span data-stu-id="2672a-105">When the merge module is merged into a .msi file, every file in the merge module File Table is stored inside a [*cabinet file*](c-gly.md) in the .msm file.</span></span> <span data-ttu-id="2672a-106">O nome do gabinete em um módulo de mesclagem é sempre o seguinte: MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="2672a-106">The name of the cabinet in a merge module is always the following: MergeModule.CABinet.</span></span>

<span data-ttu-id="2672a-107">Para obter mais informações, consulte [gerando MergeModule.CABarquivos de gabinete inet](generating-mergemodule-cabinet-cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="2672a-107">For more information, see [Generating MergeModule.CABinet Cabinet Files](generating-mergemodule-cabinet-cabinet-files.md).</span></span>

-   <span data-ttu-id="2672a-108">Como os arquivos de um módulo de mesclagem são sempre armazenados dentro de um arquivo de gabinete, não é necessário definir os sinalizadores de bit **msidbFileAttributesNoncompressed** ou **MsidbFileAttributesCompressed** na coluna Attributes da [tabela File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="2672a-108">Because the files of a merge module are always stored inside a cabinet file, it is not necessary to set the **msidbFileAttributesNoncompressed** or **msidbFileAttributesCompressed** bit flags in the Attributes column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="2672a-109">Os nomes dos arquivos no MergeModule.CABinet devem corresponder à chave primária na [tabela de arquivos](file-table.md)do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="2672a-109">The names of files in MergeModule.CABinet must match the primary key in the merge module's [File Table](file-table.md).</span></span>

    <span data-ttu-id="2672a-110">A coluna arquivo é a chave primária da [tabela de arquivos](file-table.md) e as entradas nesse campo devem seguir a Convenção descrita em [nomear chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="2672a-110">The File column is the primary key of the [File Table](file-table.md) and the entries in this field must follow the convention that is described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

-   <span data-ttu-id="2672a-111">Os números de sequência de arquivos são especificados na coluna sequência da [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="2672a-111">File sequence numbers are specified in the Sequence column of the [File Table](file-table.md).</span></span>

    <span data-ttu-id="2672a-112">Os arquivos devem ser listados na [tabela de arquivos](file-table.md) do módulo de mesclagem na mesma sequência em que são armazenados MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="2672a-112">Files must be listed in the merge module's [File Table](file-table.md) in the same sequence that they are stored in MergeModule.CABinet.</span></span> <span data-ttu-id="2672a-113">Os números de sequência de arquivos não precisam ser consecutivos, mas eles devem seguir a mesma sequência que os arquivos armazenados no gabinete.</span><span class="sxs-lookup"><span data-stu-id="2672a-113">The sequence numbers of files do not need to be consecutive, but they must follow the same sequence as the files that are stored inside the cabinet.</span></span> <span data-ttu-id="2672a-114">Por exemplo, o primeiro, o segundo e o terceiro arquivos armazenados no gabinete podem ter os números de sequência 100, 200 e 300.</span><span class="sxs-lookup"><span data-stu-id="2672a-114">For example, the first, second, and third files stored in the cabinet can have the sequence numbers 100, 200, and 300.</span></span>

-   <span data-ttu-id="2672a-115">O instalador ignora arquivos extras incluídos no MergeModule.CABinet que não estão listados na tabela de [arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="2672a-115">The Installer skips extra files included in MergeModule.CABinet that are not listed in the [File Table](file-table.md).</span></span>

    <span data-ttu-id="2672a-116">Um arquivo de gabinete pode conter todos os arquivos necessários para um módulo de mesclagem que dá suporte a vários idiomas usando transformações.</span><span class="sxs-lookup"><span data-stu-id="2672a-116">One cabinet file can contain all the files necessary for a merge module that supports multiple languages using transforms.</span></span> <span data-ttu-id="2672a-117">Todos os arquivos de idioma podem receber um número de sequência exclusivo no gabinete e, em seguida, uma transformação pode adicionar ou remover arquivos da [tabela de arquivos](file-table.md) quando necessário para um idioma específico.</span><span class="sxs-lookup"><span data-stu-id="2672a-117">All the language files can be given a unique sequence number in the cabinet, and then a transform can add or remove files from the [File Table](file-table.md) when needed for a specific language.</span></span> <span data-ttu-id="2672a-118">Para obter mais informações, consulte [criando módulos de mesclagem de vários idiomas](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="2672a-118">For more information, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="2672a-119">Para obter mais informações, consulte [File Table](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="2672a-119">For more information, see [File Table](file-table.md).</span></span>

 

 




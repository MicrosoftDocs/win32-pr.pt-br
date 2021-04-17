---
description: Cada arquivo que é entregue ao pacote de instalação de destino pelo módulo de mesclagem deve ser armazenado dentro de um arquivo de gabinete inserido como um fluxo dentro do arquivo. msm. O nome desse gabinete é sempre MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Gerando MergeModule.CABarquivos de gabinete inet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783271"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a><span data-ttu-id="baa3c-104">Gerando MergeModule.CABarquivos de gabinete inet</span><span class="sxs-lookup"><span data-stu-id="baa3c-104">Generating MergeModule.CABinet Cabinet Files</span></span>

<span data-ttu-id="baa3c-105">Cada arquivo que é entregue ao pacote de instalação de destino pelo módulo de mesclagem deve ser armazenado dentro de um arquivo de gabinete inserido como um fluxo dentro do arquivo. msm.</span><span class="sxs-lookup"><span data-stu-id="baa3c-105">Every file that is delivered to the target installation package by the merge module must be stored inside of a cabinet file embedded as a stream inside the .msm file.</span></span> <span data-ttu-id="baa3c-106">O nome desse gabinete é sempre MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="baa3c-106">The name of this cabinet is always MergeModule.CABinet.</span></span>

<span data-ttu-id="baa3c-107">Os nomes dos arquivos no MergeModule.CABinet devem corresponder às chaves primárias usadas na [tabela de arquivos](file-table.md) do módulo de mesclagem e devem aderir à Convenção descrita em [nomear chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="baa3c-107">The names of files in MergeModule.CABinet must match the primary keys used in the merge module's [File table](file-table.md) and must adhere to the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="baa3c-108">O instalador ignora arquivos extras incluídos no MergeModule.CABinet que não estão listados na [tabela de arquivos](file-table.md)do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="baa3c-108">The installer skips extra files included in MergeModule.CABinet that are not listed in the merge module's [File table](file-table.md).</span></span> <span data-ttu-id="baa3c-109">Os números de sequência de arquivos especificados na tabela de arquivos não precisam ser consecutivos, mas eles devem seguir a mesma sequência que os arquivos armazenados dentro de MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="baa3c-109">The sequence numbers of files specified in the File table do not need to be consecutive, but they must follow the same sequence as the files stored inside MergeModule.CABinet.</span></span> <span data-ttu-id="baa3c-110">Para obter mais informações, consulte [criando tabelas de arquivos do módulo de mesclagem](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="baa3c-110">For more information, see [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

<span data-ttu-id="baa3c-111">Isso significa que um único arquivo de gabinete pode conter todos os arquivos necessários para que um módulo de mesclagem ofereça suporte a vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="baa3c-111">This means that a single cabinet file can contain all the files needed for a merge module to support multiple languages.</span></span> <span data-ttu-id="baa3c-112">Todos os arquivos de idioma podem receber números de sequência exclusivos no gabinete e, em seguida, uma transformação de idioma pode ser usada para adicionar ou remover arquivos da tabela de arquivos para obter um módulo de mesclagem para um idioma específico.</span><span class="sxs-lookup"><span data-stu-id="baa3c-112">All the language files can be given unique sequence numbers in the cabinet and then a language transform can be used to add or remove files from the File table to obtain a merge module for a particular language.</span></span> <span data-ttu-id="baa3c-113">Para obter detalhes, consulte [criando módulos de mesclagem de vários idiomas](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="baa3c-113">For details, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="baa3c-114">MergeModule.CABo inet pode ser adicionado ao módulo de mesclagem abrindo uma [ \_ tabela de fluxos](-streams-table.md)temporários.</span><span class="sxs-lookup"><span data-stu-id="baa3c-114">MergeModule.CABinet can be added to the merge module by opening a temporary [\_Streams Table](-streams-table.md).</span></span> <span data-ttu-id="baa3c-115">Por exemplo, a ferramenta Msidb.exe fornecida com o SDK do Windows Installer pode ser usada para adicionar o MergeModule.CABinet ao módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="baa3c-115">For example, the tool Msidb.exe provided with the Windows Installer SDK can be used to add the MergeModule.CABinet to the merge module.</span></span> <span data-ttu-id="baa3c-116">Para obter mais informações, consulte [incluindo um arquivo de gabinete em uma instalação](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="baa3c-116">For more information, see [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 




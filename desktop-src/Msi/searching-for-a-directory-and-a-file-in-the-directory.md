---
description: Durante uma instalação de Windows Installer, o instalador pode pesquisar um diretório e um arquivo nesse diretório.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Procurando um diretório e um arquivo no diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768460"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a><span data-ttu-id="cef70-103">Procurando um diretório e um arquivo no diretório</span><span class="sxs-lookup"><span data-stu-id="cef70-103">Searching for a Directory and a File in the Directory</span></span>

<span data-ttu-id="cef70-104">**Para procurar um diretório e, em seguida, um arquivo nesse diretório**</span><span class="sxs-lookup"><span data-stu-id="cef70-104">**To search for a directory and then a file in that directory**</span></span>

1.  <span data-ttu-id="cef70-105">Primeiro, procure o diretório.</span><span class="sxs-lookup"><span data-stu-id="cef70-105">First search for the directory.</span></span>

    <span data-ttu-id="cef70-106">AppDir deve ser definido como a assinatura válida do diretório.</span><span class="sxs-lookup"><span data-stu-id="cef70-106">AppDir must be defined as the valid signature of the directory.</span></span> <span data-ttu-id="cef70-107">Se AppDir não estiver definido como uma assinatura válida, AppSearch não terá um local para localizar o arquivo, por exemplo, se a pesquisa for para c: \\ MyDir \\MyApp.exe, appdir deverá ser definido como c: \\ mydir.</span><span class="sxs-lookup"><span data-stu-id="cef70-107">If AppDir is not defined as a valid signature, AppSearch does not have a place to find the file, for example, if the search is for c:\\MyDir\\MyApp.exe, AppDir should be defined as c:\\MyDir.</span></span> <span data-ttu-id="cef70-108">AppDir pode ser definido por meio da inclusão de um registro na [tabela DrLocator](drlocator-table.md)ou por algum outro método.</span><span class="sxs-lookup"><span data-stu-id="cef70-108">AppDir might be defined by including a record in the [DrLocator Table](drlocator-table.md), or by some other method.</span></span> <span data-ttu-id="cef70-109">Nenhum registro está incluído na [tabela de assinatura](signature-table.md) para a pesquisa de diretório.</span><span class="sxs-lookup"><span data-stu-id="cef70-109">No record is included in the [Signature Table](signature-table.md) for the directory search.</span></span> <span data-ttu-id="cef70-110">Para a pesquisa de arquivos, liste a assinatura e o nome do arquivo na tabela de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cef70-110">For the file search, list the file signature and name in the Signature Table.</span></span> <span data-ttu-id="cef70-111">Os campos restantes nesse registro podem ser nulos para pesquisar qualquer versão do MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="cef70-111">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="cef70-112">[Tabela de assinatura](signature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="cef70-112">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="cef70-113">Assinatura</span><span class="sxs-lookup"><span data-stu-id="cef70-113">Signature</span></span>          | <span data-ttu-id="cef70-114">Nome do Arquivo</span><span class="sxs-lookup"><span data-stu-id="cef70-114">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="cef70-115">AppFile</span><span class="sxs-lookup"><span data-stu-id="cef70-115">AppFile</span></span><br/> | <span data-ttu-id="cef70-116">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="cef70-116">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="cef70-117">Use a [tabela AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="cef70-117">Use the [AppSearch Table](appsearch-table.md).</span></span>

    <span data-ttu-id="cef70-118">Insira a propriedade que o instalador deve definir se o diretório com a assinatura AppDir estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="cef70-118">Enter the property that the Installer is to set if the directory with the signature AppDir is installed.</span></span> <span data-ttu-id="cef70-119">Se o instalador encontrar esse diretório estiver instalado, ele definirá MYDIR como o caminho do diretório.</span><span class="sxs-lookup"><span data-stu-id="cef70-119">If the Installer finds this directory is installed, it sets MYDIR to the directory path.</span></span> <span data-ttu-id="cef70-120">Insira a propriedade que o instalador deve definir se MyApp.exe estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="cef70-120">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="cef70-121">[Tabela AppSearch](appsearch-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="cef70-121">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="cef70-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cef70-122">Property</span></span>         | <span data-ttu-id="cef70-123">Assinatura</span><span class="sxs-lookup"><span data-stu-id="cef70-123">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="cef70-124">MYDIR</span><span class="sxs-lookup"><span data-stu-id="cef70-124">MYDIR</span></span><br/> | <span data-ttu-id="cef70-125">AppDir</span><span class="sxs-lookup"><span data-stu-id="cef70-125">AppDir</span></span><br/>  |
    | <span data-ttu-id="cef70-126">MYAPP</span><span class="sxs-lookup"><span data-stu-id="cef70-126">MYAPP</span></span><br/> | <span data-ttu-id="cef70-127">AppFile</span><span class="sxs-lookup"><span data-stu-id="cef70-127">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="cef70-128">Use a [tabela DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="cef70-128">Use the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="cef70-129">Insira na coluna pai a assinatura, AppDir, que é definida como o caminho do diretório.</span><span class="sxs-lookup"><span data-stu-id="cef70-129">Enter in the Parent column the signature, AppDir, that is defined as the path of the directory.</span></span> <span data-ttu-id="cef70-130">Especifique na coluna profundidade o número de níveis de subdiretório para Pesquisar nesse diretório.</span><span class="sxs-lookup"><span data-stu-id="cef70-130">Specify in the Depth column the number of subdirectory levels to search in this directory.</span></span> <span data-ttu-id="cef70-131">AppDir deve ser definido como a assinatura de diretório.</span><span class="sxs-lookup"><span data-stu-id="cef70-131">AppDir must be defined as the directory signature.</span></span> <span data-ttu-id="cef70-132">AppDir pode ser definido por meio da inclusão de um registro, como mostrado aqui ou por outro método.</span><span class="sxs-lookup"><span data-stu-id="cef70-132">AppDir may be defined by including a record as shown here or by another method.</span></span>

    [<span data-ttu-id="cef70-133">Tabela DrLocator</span><span class="sxs-lookup"><span data-stu-id="cef70-133">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="cef70-134">Assinatura</span><span class="sxs-lookup"><span data-stu-id="cef70-134">Signature</span></span> | <span data-ttu-id="cef70-135">Pai</span><span class="sxs-lookup"><span data-stu-id="cef70-135">Parent</span></span> | <span data-ttu-id="cef70-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="cef70-136">Path</span></span>      | <span data-ttu-id="cef70-137">Profundidade</span><span class="sxs-lookup"><span data-stu-id="cef70-137">Depth</span></span> |
    |-----------|--------|-----------|-------|
    | <span data-ttu-id="cef70-138">AppDir</span><span class="sxs-lookup"><span data-stu-id="cef70-138">AppDir</span></span>    |        | <span data-ttu-id="cef70-139">C: \\ mydir</span><span class="sxs-lookup"><span data-stu-id="cef70-139">C:\\MyDir</span></span> | <span data-ttu-id="cef70-140">0</span><span class="sxs-lookup"><span data-stu-id="cef70-140">0</span></span>     |
    | <span data-ttu-id="cef70-141">AppFile</span><span class="sxs-lookup"><span data-stu-id="cef70-141">AppFile</span></span>   | <span data-ttu-id="cef70-142">AppDir</span><span class="sxs-lookup"><span data-stu-id="cef70-142">AppDir</span></span> |           | <span data-ttu-id="cef70-143">0</span><span class="sxs-lookup"><span data-stu-id="cef70-143">0</span></span>     |

    

     

4.  <span data-ttu-id="cef70-144">Inclua a ação AppSearch na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="cef70-144">Include the AppSearch action in the action sequence.</span></span>

    <span data-ttu-id="cef70-145">Se MyApp.exe for encontrado para ser instalado em AppDir, o instalador definirá a propriedade MYAPP como o local do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cef70-145">If MyApp.exe is found to be installed in AppDir, the Installer sets the property MYAPP to the location of file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cef70-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cef70-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cef70-147">Pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes</span><span class="sxs-lookup"><span data-stu-id="cef70-147">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 





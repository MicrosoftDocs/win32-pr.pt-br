---
description: Os módulos de mesclagem fornecem um método padrão para fornecer componentes de Windows Installer compartilhados e configurar a lógica para aplicativos.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Usando a automação para mesclar um módulo de mesclagem em um banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770173"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a><span data-ttu-id="36243-103">Usando a automação para mesclar um módulo de mesclagem em um banco de dados</span><span class="sxs-lookup"><span data-stu-id="36243-103">Using Automation to Merge a Merge Module into a Database</span></span>

<span data-ttu-id="36243-104">Os [módulos de mesclagem](merge-modules.md) fornecem um método padrão para fornecer [*componentes*](c-gly.md)de Windows Installer compartilhados e configurar a lógica para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="36243-104">[Merge Modules](merge-modules.md) provide a standard method for you to deliver shared Windows Installer [*components*](c-gly.md), and setup logic to applications.</span></span>

<span data-ttu-id="36243-105">Os módulos de mesclagem devem ser mesclados em um pacote de instalação usando uma ferramenta de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="36243-105">Merge modules must be merged into an installation package by using a merge tool.</span></span> <span data-ttu-id="36243-106">A prática recomendada é obter uma ferramenta de mesclagem distribuída livremente ou comprar uma das ferramentas de mesclagem que estão disponíveis de fornecedores de software independentes, por exemplo, você pode usar [Mergemod.dll](merge-module-automation.md).</span><span class="sxs-lookup"><span data-stu-id="36243-106">The best practice is to obtain a freely distributed merge tool, or purchase one of the merge tools that are available from independent software vendors, for example, you can use [Mergemod.dll](merge-module-automation.md).</span></span>

<span data-ttu-id="36243-107">O procedimento a seguir mostra como mesclar um módulo de mesclagem em um banco de dados Windows Installer usando a [automação do módulo de mesclagem](merge-module-automation.md).</span><span class="sxs-lookup"><span data-stu-id="36243-107">The following procedure shows you how to merge a merge module into a Windows Installer database by using [Merge Module Automation](merge-module-automation.md).</span></span>

<span data-ttu-id="36243-108">**Para mesclar um módulo em um banco de dados**</span><span class="sxs-lookup"><span data-stu-id="36243-108">**To merge a module into a database**</span></span>

1.  <span data-ttu-id="36243-109">Abra um arquivo de log usando o método [**OpenLog**](merge-openlog.md) .</span><span class="sxs-lookup"><span data-stu-id="36243-109">Open a log file by using the [**OpenLog**](merge-openlog.md) method.</span></span>

    <span data-ttu-id="36243-110">Essa etapa será necessária somente se você precisar criar um arquivo de log ou acrescentar um arquivo de log existente para o processo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="36243-110">This step is required only if you need to create a log file, or append an existing log file for the merge process.</span></span>

2.  <span data-ttu-id="36243-111">Abra o banco de dados de instalação [. msi](windows-installer-file-extensions.md) usando o método [**OpenDatabase**](merge-opendatabase.md) do [**objeto Merge**](merge-object.md).</span><span class="sxs-lookup"><span data-stu-id="36243-111">Open the [.msi](windows-installer-file-extensions.md) installation database by using the [**OpenDatabase**](merge-opendatabase.md) method of the [**Merge Object**](merge-object.md).</span></span>

    <span data-ttu-id="36243-112">Essa etapa é necessária.</span><span class="sxs-lookup"><span data-stu-id="36243-112">This step is required.</span></span>

    <span data-ttu-id="36243-113">O banco de dados que você abre é aquele que você deseja receber o módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="36243-113">The database that you open is the one that you want to receive the merge module.</span></span>

3.  <span data-ttu-id="36243-114">Abra o módulo de mesclagem [. msm](windows-installer-file-extensions.md) usando o método [**AbrirMódulo**](merge-openmodule.md) .</span><span class="sxs-lookup"><span data-stu-id="36243-114">Open the [.msm](windows-installer-file-extensions.md) merge module by using the [**OpenModule**](merge-openmodule.md) method.</span></span>

    <span data-ttu-id="36243-115">Essa etapa é necessária.</span><span class="sxs-lookup"><span data-stu-id="36243-115">This step is required.</span></span>

    <span data-ttu-id="36243-116">Este é o módulo de mesclagem que está sendo mesclado no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="36243-116">This is the merge module that is being merged into the database.</span></span> <span data-ttu-id="36243-117">Um módulo deve ser aberto antes que possa ser mesclado com um banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="36243-117">A module must be opened before it can be merged with an installation database.</span></span>

4.  <span data-ttu-id="36243-118">Mescle o módulo no banco de dados de instalação chamando o método [**Merge**](merge-object.md) ou o método [**MergeEx**](merge-mergeex.md) .</span><span class="sxs-lookup"><span data-stu-id="36243-118">Merge the module into the installation database by calling the [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method.</span></span>

    <span data-ttu-id="36243-119">Essa etapa é necessária.</span><span class="sxs-lookup"><span data-stu-id="36243-119">This step is required.</span></span>

    <span data-ttu-id="36243-120">O método [**Merge**](merge-object.md) ou o método [**MergeEx**](merge-mergeex.md) só pode ser chamado uma vez para mesclar uma combinação específica de arquivos [. msi](windows-installer-file-extensions.md) e. msm.</span><span class="sxs-lookup"><span data-stu-id="36243-120">The [**Merge**](merge-object.md) method or [**MergeEx**](merge-mergeex.md) method can only be called one time to merge a specific combination of [.msi](windows-installer-file-extensions.md) and .msm files.</span></span>

    > [!Note]  
    > <span data-ttu-id="36243-121">O método [**MergeEx**](merge-mergeex.md) só está disponível no [Mergemod.dll versão 2,0](merge-module-automation.md) ou posterior, e somente ao usar a interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .</span><span class="sxs-lookup"><span data-stu-id="36243-121">The [**MergeEx**](merge-mergeex.md) method is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later, and only when using the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface.</span></span>

     

5.  <span data-ttu-id="36243-122">Recupere a propriedade [**Errors**](merge-errors.md) e examine a coleção de objetos de [**erro**](error-object.md) que ele retorna para conflitos de mesclagem ou outros erros.</span><span class="sxs-lookup"><span data-stu-id="36243-122">Retrieve the [**Errors**](merge-errors.md) property and examine the collection of [**Error**](error-object.md) objects it returns for merge conflicts or other errors.</span></span>

    <span data-ttu-id="36243-123">Você deve resolver quaisquer erros.</span><span class="sxs-lookup"><span data-stu-id="36243-123">You must resolve any errors.</span></span>

    <span data-ttu-id="36243-124">A recuperação não é destrutiva e várias instâncias da coleção de erros podem ser recuperadas com a leitura repetida da propriedade [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="36243-124">The retrieval is nondestructive, and multiple instances of the error collection can be retrieved by repeatedly reading the [**Errors**](merge-errors.md) property.</span></span>

6.  <span data-ttu-id="36243-125">Associe os componentes do módulo de mesclagem aos recursos usando o método [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="36243-125">Associate the components of the merge module with the features by using the [**Connect**](merge-connect.md) method.</span></span>

    <span data-ttu-id="36243-126">Esta etapa só será necessária se você tiver recursos existentes e quiser adicionar recursos para mesclar no banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="36243-126">This step is only required if you have existing features and you want to add features to merge into the installation database.</span></span>

    <span data-ttu-id="36243-127">Um recurso deve existir antes de você chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="36243-127">A feature must exist before you call this method.</span></span> <span data-ttu-id="36243-128">Para obter mais informações, consulte [conectando um módulo de mesclagem a vários recursos](connecting-a-merge-module-to-multiple-features.md).</span><span class="sxs-lookup"><span data-stu-id="36243-128">For more information, see [Connecting a Merge Module to Multiple Features](connecting-a-merge-module-to-multiple-features.md).</span></span>

7.  <span data-ttu-id="36243-129">Se necessário, extraia os arquivos de origem do módulo seguindo um ou mais destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="36243-129">If necessary, extract source files from the module by doing one or more of the following:</span></span>
    -   <span data-ttu-id="36243-130">Use [**ExtractFiles**](merge-extractfiles.md) ou [**ExtractFilesEx**](merge-extractfilesex.md) para extrair arquivos de um arquivo. cab inserido e, em seguida, copiar para um diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="36243-130">Use [**ExtractFiles**](merge-extractfiles.md) or [**ExtractFilesEx**](merge-extractfilesex.md) to extract files from an embedded .cab file and then copy into a specified directory.</span></span>
        > [!Note]  
        > <span data-ttu-id="36243-131">O [**ExtractFilesEx**](merge-extractfilesex.md) requer [Mergemod.dll versão 2,0](merge-module-automation.md) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="36243-131">[**ExtractFilesEx**](merge-extractfilesex.md) requires [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         

    -   <span data-ttu-id="36243-132">Use [**ExtractCAB**](merge-extractcab.md) para extrair arquivos de um arquivo. cab inserido e, em seguida, salvar em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="36243-132">Use [**ExtractCAB**](merge-extractcab.md) to extract files from an embedded .cab file, and then save in a specified file.</span></span>
    -   <span data-ttu-id="36243-133">Use [**CreateSourceImage**](merge-createsourceimage.md) para extrair arquivos de um módulo e, em seguida, após a mesclagem, copie para uma imagem de origem no disco.</span><span class="sxs-lookup"><span data-stu-id="36243-133">Use [**CreateSourceImage**](merge-createsourceimage.md) to extract files from a module, and then after the merge, copy to a source image on disk.</span></span>
        > [!Note]  
        > <span data-ttu-id="36243-134">[**CreateSourceImage**](merge-createsourceimage.md) só está disponível no [Mergemod.dll versão 2,0](merge-module-automation.md) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="36243-134">[**CreateSourceImage**](merge-createsourceimage.md) is only available in [Mergemod.dll version 2.0](merge-module-automation.md) or later.</span></span>

         
8.  <span data-ttu-id="36243-135">Feche o módulo de mesclagem aberto atual usando o método [**CloseModule**](merge-closemodule.md) .</span><span class="sxs-lookup"><span data-stu-id="36243-135">Close the current open merge module by using the [**CloseModule**](merge-closemodule.md) method.</span></span>

    <span data-ttu-id="36243-136">Essa etapa é necessária.</span><span class="sxs-lookup"><span data-stu-id="36243-136">This step is required.</span></span>

9.  <span data-ttu-id="36243-137">Feche o banco de dados de instalação aberto usando o método [**CloseDatabase**](merge-closedatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="36243-137">Close the open installation database by using the [**CloseDatabase**](merge-closedatabase.md) method.</span></span>

    <span data-ttu-id="36243-138">Essa etapa é necessária.</span><span class="sxs-lookup"><span data-stu-id="36243-138">This step is required.</span></span>

    <span data-ttu-id="36243-139">Fechar um banco de dados limpa todas as informações de dependência, mas não afeta os erros que não são recuperados.</span><span class="sxs-lookup"><span data-stu-id="36243-139">Closing a database clears all dependency information, but does not affect any errors that are not retrieved.</span></span>

10. <span data-ttu-id="36243-140">Feche o arquivo de log atual usando o método [**CloseLog**](merge-closelog.md) .</span><span class="sxs-lookup"><span data-stu-id="36243-140">Close the current log file by using the [**CloseLog**](merge-closelog.md) method.</span></span>

    <span data-ttu-id="36243-141">Esta etapa será necessária se você tiver um arquivo de log aberto.</span><span class="sxs-lookup"><span data-stu-id="36243-141">This step is required if you have an open log file.</span></span>

<span data-ttu-id="36243-142">Depois que o módulo tiver sido mesclado no banco de dados usando [Mergemod.dll](merge-module-automation.md), a [tabela de mídia](media-table.md) deverá ser atualizada para descrever o layout da imagem de origem desejada.</span><span class="sxs-lookup"><span data-stu-id="36243-142">After the module has been merged into the database using [Mergemod.dll](merge-module-automation.md), the [Media Table](media-table.md) must be updated to describe the desired source image layout.</span></span> <span data-ttu-id="36243-143">O processo de mesclagem fornecido pelo Mergemod.dll não atualiza a tabela de mídia porque o consumidor do módulo de mesclagem pode selecionar várias maneiras de fazer o layout da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="36243-143">The merge process provided by Mergemod.dll does not update the Media Table because the consumer of the merge module can select various ways to layout the source image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36243-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="36243-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36243-145">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="36243-145">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 




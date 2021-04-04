---
description: O BETest é um solicitante do VSS que testa operações avançadas de backup e restauração.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Ferramenta BETest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7559c304532b337214108435b740595897694f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837264"
---
# <a name="betest-tool"></a><span data-ttu-id="5f073-103">Ferramenta BETest</span><span class="sxs-lookup"><span data-stu-id="5f073-103">BETest Tool</span></span>

<span data-ttu-id="5f073-104">O BETest é um solicitante do VSS que testa operações avançadas de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="5f073-104">BETest is a VSS requester that tests advanced backup and restore operations.</span></span> <span data-ttu-id="5f073-105">Essa ferramenta pode ser usada para testar o uso de recursos VSS complexos de um aplicativo, como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5f073-105">This tool can be used to test an application's use of complex VSS features such as the following:</span></span>

-   <span data-ttu-id="5f073-106">Backup incremental e diferencial</span><span class="sxs-lookup"><span data-stu-id="5f073-106">Incremental and differential backup</span></span>
-   <span data-ttu-id="5f073-107">Opções de restauração complexas, como restauração autoritativa</span><span class="sxs-lookup"><span data-stu-id="5f073-107">Complex restore options, such as authoritative restore</span></span>
-   <span data-ttu-id="5f073-108">Opções de avanço</span><span class="sxs-lookup"><span data-stu-id="5f073-108">Rollforward options</span></span>

> [!Note]  
> <span data-ttu-id="5f073-109">O BETest está incluído no SDK (Software Development Kit) do Microsoft Windows para Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="5f073-109">BETest is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="5f073-110">O SDK 7,2 do VSS inclui uma versão de BETest que é executada somente no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5f073-110">The VSS 7.2 SDK includes a version of BETest that runs only on Windows Server 2003.</span></span> <span data-ttu-id="5f073-111">Este tópico descreve a versão SDK do Windows do BETest, não a versão 2003 do Windows Server incluída no SDK do VSS 7,2.</span><span class="sxs-lookup"><span data-stu-id="5f073-111">This topic describes the Windows SDK version of BETest, not the Windows Server 2003 version included in the VSS 7.2 SDK.</span></span> <span data-ttu-id="5f073-112">Para obter informações sobre como baixar o SDK do Windows e o SDK 7,2 do VSS, consulte [serviço de cópias de sombra de volume](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="5f073-112">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="5f073-113">Na instalação do SDK do Windows, a ferramenta BETest pode ser encontrada em `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para Windows de 64 bits) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para windows de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="5f073-113">In the Windows SDK installation, the BETest tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="running-the-betest-tool"></a><span data-ttu-id="5f073-114">Executando a ferramenta BETest</span><span class="sxs-lookup"><span data-stu-id="5f073-114">Running the BETest Tool</span></span>

<span data-ttu-id="5f073-115">Para executar a ferramenta BETest na linha de comando, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="5f073-115">To run the BETest tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="5f073-116">*Opções de linha de comando* do **BETest**</span><span class="sxs-lookup"><span data-stu-id="5f073-116">**BETest** *command-line-options*</span></span>

<span data-ttu-id="5f073-117">O exemplo de uso a seguir mostra como usar a ferramenta BETest junto com a [ferramenta de gravador de teste do VSS](vss-test-writer-tool.md), que é um gravador VSS.</span><span class="sxs-lookup"><span data-stu-id="5f073-117">The following usage example shows how to use the BETest tool together with the [VSS Test Writer tool](vss-test-writer-tool.md), which is a VSS writer.</span></span>

<span data-ttu-id="5f073-118">**Exemplo de uso da ferramenta BETest**</span><span class="sxs-lookup"><span data-stu-id="5f073-118">**BETest Tool Usage Example**</span></span>

1.  <span data-ttu-id="5f073-119">Crie um diretório de teste chamado C: \\ BETest.</span><span class="sxs-lookup"><span data-stu-id="5f073-119">Create a test directory named C:\\BETest.</span></span> <span data-ttu-id="5f073-120">Copie os seguintes arquivos para este diretório:</span><span class="sxs-lookup"><span data-stu-id="5f073-120">Copy the following files into this directory:</span></span>
    -   <span data-ttu-id="5f073-121">betest.exe</span><span class="sxs-lookup"><span data-stu-id="5f073-121">betest.exe</span></span>
    -   <span data-ttu-id="5f073-122">vswriter.exe</span><span class="sxs-lookup"><span data-stu-id="5f073-122">vswriter.exe</span></span>
    -   [<span data-ttu-id="5f073-123">BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="5f073-123">BetestSample.xml</span></span>](#sample-xml-configuration-file-betestsamplexml)
    -   [<span data-ttu-id="5f073-124">VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="5f073-124">VswriterSample.xml</span></span>](#sample-xml-configuration-file-vswritersamplexml)
2.  <span data-ttu-id="5f073-125">Crie um diretório chamado C: \\ TestPath.</span><span class="sxs-lookup"><span data-stu-id="5f073-125">Create a directory named C:\\TestPath.</span></span> <span data-ttu-id="5f073-126">Coloque alguns arquivos de dados de teste nesse diretório.</span><span class="sxs-lookup"><span data-stu-id="5f073-126">Put some test data files in this directory.</span></span>
3.  <span data-ttu-id="5f073-127">Crie um diretório chamado C: \\ BackupDestination.</span><span class="sxs-lookup"><span data-stu-id="5f073-127">Create a directory named C:\\BackupDestination.</span></span> <span data-ttu-id="5f073-128">Deixe esse diretório vazio.</span><span class="sxs-lookup"><span data-stu-id="5f073-128">Leave this directory empty.</span></span>
4.  <span data-ttu-id="5f073-129">Abra duas janelas de comando elevadas e defina o diretório de trabalho em cada para C: \\ BETest.</span><span class="sxs-lookup"><span data-stu-id="5f073-129">Open two elevated command windows and set the working directory in each to C:\\BETest.</span></span>
5.  <span data-ttu-id="5f073-130">Na primeira janela de comando, inicie a [ferramenta gravador de teste do VSS](vss-test-writer-tool.md) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5f073-130">In the first command window, start the [VSS Test Writer tool](vss-test-writer-tool.md) as follows:</span></span>

    <span data-ttu-id="5f073-131">**vswriter.exe VswriterSample.xml**</span><span class="sxs-lookup"><span data-stu-id="5f073-131">**vswriter.exe VswriterSample.xml**</span></span>

    <span data-ttu-id="5f073-132">O arquivo vswriterSample.xml configura a ferramenta de gravador de teste do VSS (vswriter) para relatar o conteúdo do diretório c: \\ TestPath em preparação para uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="5f073-132">The vswriterSample.xml file configures the VSS Test Writer tool (vswriter) to report the contents of the c:\\TestPath directory in preparation for a backup operation.</span></span> <span data-ttu-id="5f073-133">Observe que a ferramenta de gravador de teste do VSS não produzirá saída até detectar a atividade de um solicitante, como o BETest.</span><span class="sxs-lookup"><span data-stu-id="5f073-133">Note that the VSS Test Writer tool will not produce output until it detects activity from a requester such as BETest.</span></span> <span data-ttu-id="5f073-134">Para interromper a ferramenta gravador de teste do VSS, pressione CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="5f073-134">To stop the VSS Test Writer tool, press CTRL+C.</span></span>

6.  <span data-ttu-id="5f073-135">Na segunda janela de comando, use a ferramenta BETest para executar uma operação de backup da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5f073-135">In the second command window, use the BETest tool to perform a backup operation as follows:</span></span>

    <span data-ttu-id="5f073-136">**betest.exe/B/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="5f073-136">**betest.exe /B /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

    <span data-ttu-id="5f073-137">O BETest fará o backup dos arquivos do diretório C: \\ TestPath para o diretório c: \\ BackupDestination.</span><span class="sxs-lookup"><span data-stu-id="5f073-137">BETest will back up the files from the C:\\TestPath directory to the C:\\BackupDestination directory.</span></span> <span data-ttu-id="5f073-138">Ele salvará o documento do componente de backup em C: \\ BETest \\backup.xml.</span><span class="sxs-lookup"><span data-stu-id="5f073-138">It will save the backup component document to C:\\BETest\\backup.xml.</span></span>

7.  <span data-ttu-id="5f073-139">Se a operação de backup for bem-sucedida, exclua o conteúdo do diretório C: \\ TestPath e use a ferramenta BETest para executar uma operação de restauração da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5f073-139">If the backup operation is successful, delete the contents of the C:\\TestPath directory, and use the BETest tool to perform a restore operation as follows:</span></span>

    <span data-ttu-id="5f073-140">**betest.exe/R/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="5f073-140">**betest.exe /R /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

## <a name="betest-tool-command-line-options"></a><span data-ttu-id="5f073-141">Opções de Command-Line da ferramenta BETest</span><span class="sxs-lookup"><span data-stu-id="5f073-141">BETest Tool Command-Line Options</span></span>

<span data-ttu-id="5f073-142">A ferramenta BETest usa as seguintes opções de linha de comando para identificar o trabalho a ser executado.</span><span class="sxs-lookup"><span data-stu-id="5f073-142">The BETest tool uses the following command-line options to identify the work to perform.</span></span>

<dl> <dt>

<span data-ttu-id="5f073-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span><span class="sxs-lookup"><span data-stu-id="5f073-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-144">Executa uma operação de restauração autoritativa para Active Directory ou Active Directory modo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f073-144">Performs an authoritative restore operation for Active Directory or Active Directory Application Mode.</span></span>

<span data-ttu-id="5f073-145">**Windows Server 2003:** Não há suporte para essa opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5f073-145">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-146"><span id="_B"></span><span id="_b"></span>**/B.**</span><span class="sxs-lookup"><span data-stu-id="5f073-146"><span id="_B"></span><span id="_b"></span>**/B**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-147">Executa uma operação de backup, mas não executa uma restauração.</span><span class="sxs-lookup"><span data-stu-id="5f073-147">Performs a backup operation but does not perform a restore.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span><span class="sxs-lookup"><span data-stu-id="5f073-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-149">Executa apenas a operação backup concluído.</span><span class="sxs-lookup"><span data-stu-id="5f073-149">Performs only the backup complete operation.</span></span>

<span data-ttu-id="5f073-150">**Windows Server 2003:** Não há suporte para essa opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5f073-150">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="5f073-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Filename*</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="5f073-152">Essa opção de linha de comando é fornecida somente para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="5f073-152">This command-line option is provided only for backward compatibility.</span></span> <span data-ttu-id="5f073-153">Em vez disso, a opção de linha de comando **/x** deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="5f073-153">The **/X** command-line option should be used instead.</span></span>

 

<span data-ttu-id="5f073-154">Seleciona os componentes dos quais será feito backup ou restaurados com base no conteúdo do arquivo de configuração especificado por *filename*.</span><span class="sxs-lookup"><span data-stu-id="5f073-154">Selects the components to be backed up or restored based on the contents of the configuration file specified by *Filename*.</span></span> <span data-ttu-id="5f073-155">Esse arquivo deve conter apenas caracteres ANSI no intervalo de 0 a 127, e não deve ter mais de 1 MB.</span><span class="sxs-lookup"><span data-stu-id="5f073-155">This file must contain only ANSI characters in the range from 0 through 127, and it must be no larger than 1 MB.</span></span> <span data-ttu-id="5f073-156">Cada linha no arquivo deve usar o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="5f073-156">Each line in the file must use the following format:</span></span>

<span data-ttu-id="5f073-157">*WriterId* : *ComponentName*;</span><span class="sxs-lookup"><span data-stu-id="5f073-157">*WriterId* : *ComponentName*;</span></span>

<span data-ttu-id="5f073-158">Em que *WriterId* é a ID do gravador e *ComponentName* é o nome de um dos componentes do gravador.</span><span class="sxs-lookup"><span data-stu-id="5f073-158">Where *WriterId* is the writer ID, and *ComponentName* is the name of one of the writer's components.</span></span> <span data-ttu-id="5f073-159">A ID do gravador e os nomes de componentes devem estar entre aspas, e deve haver espaços antes e depois dos dois-pontos (:).</span><span class="sxs-lookup"><span data-stu-id="5f073-159">The writer ID and component names must be in quotation marks, and there must be spaces before and after the colon (:).</span></span> <span data-ttu-id="5f073-160">Se dois ou mais componentes forem especificados, eles deverão ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="5f073-160">If two or more components are specified, they must be separated by commas.</span></span> <span data-ttu-id="5f073-161">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5f073-161">For example:</span></span>

<span data-ttu-id="5f073-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span><span class="sxs-lookup"><span data-stu-id="5f073-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span></span>

</dd> <dt>

<span data-ttu-id="5f073-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *caminho*</span><span class="sxs-lookup"><span data-stu-id="5f073-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *Path*</span></span>
</dt> <dd>

<span data-ttu-id="5f073-164">Salve os arquivos dos quais foi feito backup ou restaure-os a partir do diretório de backup especificado pelo *caminho*.</span><span class="sxs-lookup"><span data-stu-id="5f073-164">Save the backed-up files to or restore them from the backup directory specified by *Path*.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span><span class="sxs-lookup"><span data-stu-id="5f073-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-166">Omite a operação de backup concluído.</span><span class="sxs-lookup"><span data-stu-id="5f073-166">Omits the backup complete operation.</span></span>

<span data-ttu-id="5f073-167">**Windows Server 2003:** Não há suporte para essa opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5f073-167">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-168"><span id="_O"></span><span id="_o"></span>**/O**</span><span class="sxs-lookup"><span data-stu-id="5f073-168"><span id="_O"></span><span id="_o"></span>**/O**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-169">Especifica que o backup inclui um estado de sistema inicializável.</span><span class="sxs-lookup"><span data-stu-id="5f073-169">Specifies that the backup includes a bootable system state.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-170"><span id="_P"></span><span id="_p"></span>**/P**</span><span class="sxs-lookup"><span data-stu-id="5f073-170"><span id="_P"></span><span id="_p"></span>**/P**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-171">Cria uma cópia de sombra persistente.</span><span class="sxs-lookup"><span data-stu-id="5f073-171">Creates a persistent shadow copy.</span></span>

<span data-ttu-id="5f073-172">**Windows Server 2003:** Não há suporte para essa opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5f073-172">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span> *Nome de arquivo* /pre</span><span class="sxs-lookup"><span data-stu-id="5f073-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="5f073-174">Se o tipo de backup especificado na opção de linha de comando **/t** for incremental ou diferencial, defina o documento de backup para o arquivo especificado por *filename* para backup completo ou incremental anterior.</span><span class="sxs-lookup"><span data-stu-id="5f073-174">If the backup type specified in the **/T** command-line option is INCREMENTAL or DIFFERENTIAL, set the backup document to the file specified by *Filename* for previous full or incremental backup.</span></span>

<span data-ttu-id="5f073-175">**Windows Server 2003 e Windows XP:** Não há suporte para essa opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5f073-175">**Windows Server 2003 and Windows XP:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-176"><span id="_R"></span><span id="_r"></span>**/R**</span><span class="sxs-lookup"><span data-stu-id="5f073-176"><span id="_R"></span><span id="_r"></span>**/R**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-177">Executa a restauração, mas não executa o backup.</span><span class="sxs-lookup"><span data-stu-id="5f073-177">Performs restore but does not perform backup.</span></span> <span data-ttu-id="5f073-178">Deve ser usado junto com a opção de linha de comando **/s** .</span><span class="sxs-lookup"><span data-stu-id="5f073-178">Must be used together with the **/S** command-line option.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span><span class="sxs-lookup"><span data-stu-id="5f073-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-180">Cria uma cópia de sombra que pode ser usada para reversão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f073-180">Creates a shadow copy that can be used for application rollback.</span></span>

<span data-ttu-id="5f073-181">**Windows Server 2003:** Não há suporte para essa opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5f073-181">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="5f073-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="5f073-183">No caso do backup, o salva o documento de backup no arquivo especificado por *filename*.</span><span class="sxs-lookup"><span data-stu-id="5f073-183">In case of backup, saves the backup document to the file specified by *Filename*.</span></span> <span data-ttu-id="5f073-184">No caso de somente restauração, o carrega o documento de backup desse arquivo.</span><span class="sxs-lookup"><span data-stu-id="5f073-184">In case of restore only, loads the backup document from this file.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span><span class="sxs-lookup"><span data-stu-id="5f073-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-186">Cria uma cópia de sombra de volume, mas não executa backup ou restauração.</span><span class="sxs-lookup"><span data-stu-id="5f073-186">Creates a volume shadow copy but does not perform backup or restore.</span></span>

<span data-ttu-id="5f073-187">**Windows Server 2003:** Não há suporte para essa opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5f073-187">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span><span class="sxs-lookup"><span data-stu-id="5f073-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-189">Interrompe o teste quando o primeiro erro do gravador é encontrado.</span><span class="sxs-lookup"><span data-stu-id="5f073-189">Stops BETest when the first writer error is encountered.</span></span>

<span data-ttu-id="5f073-190">**Windows Server 2003:** Não há suporte para essa opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5f073-190">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *backuptype*</span><span class="sxs-lookup"><span data-stu-id="5f073-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span></span>
</dt> <dd>

<span data-ttu-id="5f073-192">Especifica o tipo de backup.</span><span class="sxs-lookup"><span data-stu-id="5f073-192">Specifies the backup type.</span></span> <span data-ttu-id="5f073-193">O *backuptype* pode ser completo, de log, de cópia, incremental ou diferencial.</span><span class="sxs-lookup"><span data-stu-id="5f073-193">*BackupType* can be FULL, LOG, COPY, INCREMENTAL, or DIFFERENTIAL.</span></span> <span data-ttu-id="5f073-194">Para obter mais informações sobre tipos de backup, consulte [**VSS \_ backup \_ Type**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span><span class="sxs-lookup"><span data-stu-id="5f073-194">For more information about backup types, see [**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span></span>

</dd> <dt>

<span data-ttu-id="5f073-195"><span id="_V"></span><span id="_v"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="5f073-195"><span id="_V"></span><span id="_v"></span>**/V**</span></span>
</dt> <dd>

<span data-ttu-id="5f073-196">Gera uma saída detalhada que pode ser usada para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="5f073-196">Generates verbose output that can be used for troubleshooting.</span></span>

<span data-ttu-id="5f073-197">**Windows Server 2003:** Não há suporte para essa opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5f073-197">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f073-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span> *Nome do arquivo* /x</span><span class="sxs-lookup"><span data-stu-id="5f073-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="5f073-199">Seleciona os componentes cujo backup será feito ou restaurado com base no conteúdo do arquivo de configuração XML especificado por *filename*.</span><span class="sxs-lookup"><span data-stu-id="5f073-199">Selects the components to be backed up or restored based on the contents of the XML configuration file specified by *Filename*.</span></span> <span data-ttu-id="5f073-200">Esse arquivo deve conter apenas caracteres ANSI no intervalo de 0 a 127.</span><span class="sxs-lookup"><span data-stu-id="5f073-200">This file must contain only ANSI characters in the range from 0 through 127.</span></span> <span data-ttu-id="5f073-201">O formato do arquivo XML é definido pelo esquema no arquivo de BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="5f073-201">The format of the XML file is defined by the schema in the BETest.xml file.</span></span> <span data-ttu-id="5f073-202">Para obter um arquivo de configuração de exemplo, consulte BetestSample.xml.</span><span class="sxs-lookup"><span data-stu-id="5f073-202">For a sample configuration file, see BetestSample.xml.</span></span> <span data-ttu-id="5f073-203">Ambos os arquivos estão no diretório vsstools.</span><span class="sxs-lookup"><span data-stu-id="5f073-203">Both of these files are in the vsstools directory.</span></span>

> [!Note]  
> <span data-ttu-id="5f073-204">Você pode exibir o arquivo de BETest.xml no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5f073-204">You can view the BETest.xml file in Internet Explorer.</span></span> <span data-ttu-id="5f073-205">Antes de abrir esse arquivo, verifique se o arquivo XDR-Schema. xsl está no mesmo diretório que BETest.xml.</span><span class="sxs-lookup"><span data-stu-id="5f073-205">Before you open this file, make sure that the xdr-schema.xsl file is in the same directory as BETest.xml.</span></span> <span data-ttu-id="5f073-206">O arquivo XDR-Schema. xsl contém instruções de renderização que tornam o arquivo BETest.xml mais legível.</span><span class="sxs-lookup"><span data-stu-id="5f073-206">The xdr-schema.xsl file contains rendering instructions that make the BETest.xml file more readable.</span></span>

 

<span data-ttu-id="5f073-207">**Windows Server 2003:** Não há suporte para essa opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5f073-207">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a><span data-ttu-id="5f073-208">Arquivo de configuração XML de exemplo: BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="5f073-208">Sample XML Configuration File: BetestSample.xml</span></span>

<span data-ttu-id="5f073-209">O arquivo de configuração de exemplo a seguir, BetestSample.xml, pode ser encontrado no diretório Vsstools</span><span class="sxs-lookup"><span data-stu-id="5f073-209">The following sample configuration file, BetestSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

<span data-ttu-id="5f073-210">Este exemplo de um arquivo de configuração simples seleciona um componente do qual será feito backup ou restaurado.</span><span class="sxs-lookup"><span data-stu-id="5f073-210">This example of a simple configuration file selects one component to be backed up or restored.</span></span>

## <a name="sample-xml-configuration-file-vswritersamplexml"></a><span data-ttu-id="5f073-211">Arquivo de configuração XML de exemplo: VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="5f073-211">Sample XML Configuration File: VswriterSample.xml</span></span>

<span data-ttu-id="5f073-212">O arquivo de configuração de exemplo a seguir, VswriterSample.xml, pode ser encontrado no diretório Vsstools</span><span class="sxs-lookup"><span data-stu-id="5f073-212">The following sample configuration file, VswriterSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

<span data-ttu-id="5f073-213">O elemento raiz nesse arquivo de configuração é denominado TestWriter.</span><span class="sxs-lookup"><span data-stu-id="5f073-213">The root element in this configuration file is named TestWriter.</span></span> <span data-ttu-id="5f073-214">Todos os outros elementos são organizados sob o elemento TestWriter.</span><span class="sxs-lookup"><span data-stu-id="5f073-214">All other elements are arranged under the TestWriter element.</span></span>

<span data-ttu-id="5f073-215">O primeiro atributo associado a TestWriter é o atributo Usage.</span><span class="sxs-lookup"><span data-stu-id="5f073-215">The first attribute associated with TestWriter is the usage attribute.</span></span> <span data-ttu-id="5f073-216">Esse atributo especifica o tipo de uso relatado por meio do método [**IVssExamineWriterMetadata:: getidentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) .</span><span class="sxs-lookup"><span data-stu-id="5f073-216">This attribute specifies the usage type reported through the [**IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) method.</span></span> <span data-ttu-id="5f073-217">Um dos valores possíveis para esse atributo são \_ os dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="5f073-217">One of the possible values for this attribute is USER\_DATA.</span></span>

<span data-ttu-id="5f073-218">O segundo atributo é o atributo deleteFiles.</span><span class="sxs-lookup"><span data-stu-id="5f073-218">The second attribute is the deleteFiles attribute.</span></span> <span data-ttu-id="5f073-219">Esse atributo é descrito em [Configurando atributos do gravador](vss-test-writer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="5f073-219">This attribute is described in [Configuring Writer Attributes](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="5f073-220">O primeiro elemento filho do elemento raiz é um elemento RestoreMethod.</span><span class="sxs-lookup"><span data-stu-id="5f073-220">The first child element of the root element is a RestoreMethod element.</span></span> <span data-ttu-id="5f073-221">Esse elemento Especifica o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5f073-221">This element specifies the following:</span></span>

-   <span data-ttu-id="5f073-222">O método Restore (nesse caso, RESTOre \_ If \_ pode \_ ser \_ substituído)</span><span class="sxs-lookup"><span data-stu-id="5f073-222">The restore method (in this case, RESTORE\_IF\_CAN\_BE\_REPLACED)</span></span>
-   <span data-ttu-id="5f073-223">Se o gravador requer eventos de restauração (neste caso, sempre)</span><span class="sxs-lookup"><span data-stu-id="5f073-223">Whether the writer requires restore events (in this case, always)</span></span>
-   <span data-ttu-id="5f073-224">Se uma reinicialização é necessária após a restauração do gravador (neste caso, não)</span><span class="sxs-lookup"><span data-stu-id="5f073-224">Whether a reboot is required after the writer is restored (in this case, no)</span></span>

<span data-ttu-id="5f073-225">Esse elemento pode, opcionalmente, especificar um mapeamento de local alternativo.</span><span class="sxs-lookup"><span data-stu-id="5f073-225">This element can optionally specify an alternate-location mapping.</span></span> <span data-ttu-id="5f073-226">(Nesse caso, nenhum local alternativo é especificado.) Para obter mais informações, consulte [especificando mapeamentos alternativos de local](vss-test-writer-tool.md).</span><span class="sxs-lookup"><span data-stu-id="5f073-226">(In this case, no alternate location is specified.) For more information, see [Specifying Alternate Location Mappings](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="5f073-227">O segundo elemento filho é um elemento de componente.</span><span class="sxs-lookup"><span data-stu-id="5f073-227">The second child element is a Component element.</span></span> <span data-ttu-id="5f073-228">Esse elemento faz com que o gravador adicione um componente a seus metadados.</span><span class="sxs-lookup"><span data-stu-id="5f073-228">This element causes the writer to add a component to its metadata.</span></span> <span data-ttu-id="5f073-229">Um elemento de componente contém atributos para descrever o componente e os elementos filho para descrever o conteúdo do componente, como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5f073-229">A Component element contains attributes to describe the component and child elements to describe the content of the component, such as the following:</span></span>

-   <span data-ttu-id="5f073-230">ComponentType para indicar se este é um grupo de arquivos ou um banco de dados (neste caso, um grupo de arquivos)</span><span class="sxs-lookup"><span data-stu-id="5f073-230">componentType to indicate whether this is a filegroup or a database (in this case, a filegroup)</span></span>
-   <span data-ttu-id="5f073-231">logicalPath para o caminho lógico do componente (nesse caso, nenhum é especificado)</span><span class="sxs-lookup"><span data-stu-id="5f073-231">logicalPath for the component logical path (in this case, none is specified)</span></span>
-   <span data-ttu-id="5f073-232">ComponentName para o nome do componente (nesse caso, "TestFiles")</span><span class="sxs-lookup"><span data-stu-id="5f073-232">componentName for the name of the component (in this case, "TestFiles")</span></span>
-   <span data-ttu-id="5f073-233">selecionável para indicar o status de selecionável para backup</span><span class="sxs-lookup"><span data-stu-id="5f073-233">selectable to indicate selectable-for-backup status</span></span>

<span data-ttu-id="5f073-234">O elemento Component também tem um elemento filho chamado Componentfile para adicionar uma especificação de arquivo a esse componente.</span><span class="sxs-lookup"><span data-stu-id="5f073-234">The Component element also has a child element named ComponentFile to add a file specification to this component.</span></span> <span data-ttu-id="5f073-235">(Um elemento de componente pode ter um número arbitrário de elementos Componentfile que podem ser especificados para cada componente.) Este elemento Componentfile tem os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="5f073-235">(A Component element can have an arbitrary number of ComponentFile elements that can be specified for each component.) This ComponentFile element has the following attributes:</span></span>

-   <span data-ttu-id="5f073-236">caminho = "c: \\ TestPath"</span><span class="sxs-lookup"><span data-stu-id="5f073-236">path="c:\\TestPath"</span></span>
-   <span data-ttu-id="5f073-237">filespec = " \* "</span><span class="sxs-lookup"><span data-stu-id="5f073-237">filespec="\*"</span></span>
-   <span data-ttu-id="5f073-238">recursivo = "não"</span><span class="sxs-lookup"><span data-stu-id="5f073-238">recursive="no"</span></span>

 

 




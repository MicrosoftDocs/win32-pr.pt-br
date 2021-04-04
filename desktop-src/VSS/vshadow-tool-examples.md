---
description: 'Saiba mais sobre: exemplos da ferramenta VShadow'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Exemplos da ferramenta VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65fd2bfa1c390b1bd5310cd80f02e029dbf935f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647167"
---
# <a name="vshadow-tool-examples"></a><span data-ttu-id="b9e5e-103">Exemplos da ferramenta VShadow</span><span class="sxs-lookup"><span data-stu-id="b9e5e-103">VShadow Tool Examples</span></span>

<span data-ttu-id="b9e5e-104">Os exemplos a seguir mostram como usar a ferramenta VShadow para executar as tarefas mais comuns:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-104">The following examples show how to use the VShadow tool to perform the most common tasks:</span></span>

-   [<span data-ttu-id="b9e5e-105">Acessando Propriedades de cópia de sombra de um script CMD</span><span class="sxs-lookup"><span data-stu-id="b9e5e-105">Accessing Shadow Copy Properties from a CMD Script</span></span>](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [<span data-ttu-id="b9e5e-106">Acessando cópias de sombra não persistentes</span><span class="sxs-lookup"><span data-stu-id="b9e5e-106">Accessing Nonpersistent Shadow Copies</span></span>](#accessing-nonpersistent-shadow-copies)
-   [<span data-ttu-id="b9e5e-107">Copiando um arquivo de uma cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="b9e5e-107">Copying a File from a Shadow Copy</span></span>](#copying-a-file-from-a-shadow-copy)
-   [<span data-ttu-id="b9e5e-108">Enumerando todos os arquivos em um dispositivo de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="b9e5e-108">Enumerating All Files on a Shadow Copy Device</span></span>](#enumerating-all-files-on-a-shadow-copy-device)
-   [<span data-ttu-id="b9e5e-109">Importando uma cópia de sombra transportável</span><span class="sxs-lookup"><span data-stu-id="b9e5e-109">Importing a Transportable Shadow Copy</span></span>](#importing-a-transportable-shadow-copy)
-   [<span data-ttu-id="b9e5e-110">Incluindo gravadores ou componentes</span><span class="sxs-lookup"><span data-stu-id="b9e5e-110">Including Writers or Components</span></span>](#including-writers-or-components)
-   [<span data-ttu-id="b9e5e-111">Excluindo gravadores ou componentes</span><span class="sxs-lookup"><span data-stu-id="b9e5e-111">Excluding Writers or Components</span></span>](#excluding-writers-or-components)
-   [<span data-ttu-id="b9e5e-112">Quebrando conjuntos de cópias de sombra usando o método BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="b9e5e-112">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

<span data-ttu-id="b9e5e-113">Para obter uma lista completa das opções de linha de comando e seu uso, consulte a [ferramenta VShadow e o exemplo](vshadow-tool-and-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b9e5e-113">For a complete list of command-line options and their use, see [VShadow Tool and Sample](vshadow-tool-and-sample.md).</span></span>

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a><span data-ttu-id="b9e5e-114">Acessando Propriedades de cópia de sombra de um script CMD</span><span class="sxs-lookup"><span data-stu-id="b9e5e-114">Accessing Shadow Copy Properties from a CMD Script</span></span>

<span data-ttu-id="b9e5e-115">Se você usar o sinalizador opcional **-script** ao criar cópias de sombra, o VShadow criará um arquivo de script cmd contendo variáveis de ambiente relacionadas às cópias de sombra recém-criadas, como as seguintes:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-115">If you use the **-script** optional flag when you create shadow copies, VShadow creates a CMD script file containing environment variables related to the newly created shadow copies, such as the following:</span></span>

-   <span data-ttu-id="b9e5e-116">A ID do conjunto de cópias de sombra, que é armazenada na variável de ambiente% VSHADOW \_ set \_ ID%</span><span class="sxs-lookup"><span data-stu-id="b9e5e-116">The shadow copy set ID, which is stored in the %VSHADOW\_SET\_ID% environment variable</span></span>
-   <span data-ttu-id="b9e5e-117">As IDs de cópia de sombra, que são armazenadas em variáveis do formato% VSHADOW \_ ID \_ *nnn*%, em que *nnn* representa o índice do volume de origem na linha de comando VSHADOW</span><span class="sxs-lookup"><span data-stu-id="b9e5e-117">The shadow copy IDs, which are stored in variables of the form %VSHADOW\_ID\_*NNN*%, where *NNN* represents the index of the source volume in the VShadow command line</span></span>
-   <span data-ttu-id="b9e5e-118">Os nomes do dispositivo de cópia de sombra, que são armazenados em variáveis do formato% VSHADOW do \_ dispositivo \_ *nnn*%, em que *nnn* é o índice do volume de origem na linha de comando VSHADOW</span><span class="sxs-lookup"><span data-stu-id="b9e5e-118">The shadow copy device names, which are stored in variables of the form %VSHADOW\_DEVICE\_*NNN*%, where *NNN* is the index of the source volume in the VShadow command line</span></span>

<span data-ttu-id="b9e5e-119">Você pode usar o arquivo CMD gerado para executar operações de gerenciamento limitadas nas cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-119">You can use the generated CMD file to perform limited management operations on the shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="b9e5e-120">O evento do gravador [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) é enviado após a execução do script **-exec** .</span><span class="sxs-lookup"><span data-stu-id="b9e5e-120">The [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) writer event is sent after the **-exec** script is executed.</span></span> <span data-ttu-id="b9e5e-121">O VSS chama o método **IVssBackupComponents:: BackupComplete** para sinalizar para os gravadores que o backup está concluído e os gravadores podem truncar os logs neste ponto.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-121">VSS calls the **IVssBackupComponents::BackupComplete** method to signal to the writers that the backup is completed, and the writers can potentially truncate logs at this point.</span></span> <span data-ttu-id="b9e5e-122">Portanto, é importante verificar se a sombra/backup realmente foi concluída.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-122">Therefore, it is important to verify that the shadow/backup actually completed.</span></span> <span data-ttu-id="b9e5e-123">Se o backup tiver falhado, você poderá cancelar o processo de criação retornando um código de saída diferente de zero no script/comando executado.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-123">If the backup failed, you can cancel the creation process by returning a nonzero exit code in the executed script/command.</span></span> <span data-ttu-id="b9e5e-124">(Consulte a documentação do comando exit na referência de [linha de comando do Windows](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) Se o comando personalizado retornar com um código de saída diferente de zero, a criação da cópia de sombra será cancelada e **IVssBackupComponents:: BackupComplete** não será chamado.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-124">(See the documentation for the exit command in the [Windows Command Line Reference](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) If the custom command returns with a nonzero exit code, then the shadow copy creation is canceled and **IVssBackupComponents::BackupComplete** will not be called.</span></span>

 

<span data-ttu-id="b9e5e-125">O exemplo a seguir mostra como criar uma cópia de sombra persistente a partir da linha de comando e usar o script CMD para expô-la.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-125">The following example shows how to create a persistent shadow copy from the command line and use the CMD script to expose it.</span></span>

1.  <span data-ttu-id="b9e5e-126">**vshadow-p-NW-script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-126">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
2.  <span data-ttu-id="b9e5e-127">**chamar SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-127">**call SETVAR1.cmd**</span></span>
3.  <span data-ttu-id="b9e5e-128">**C: \\>vshadow-El =% vshadow \_ ID \_ 1%, c: \\ directory1**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-128">**C:\\>vshadow -el=%VSHADOW\_ID\_1%,c:\\directory1**</span></span>

## <a name="accessing-nonpersistent-shadow-copies"></a><span data-ttu-id="b9e5e-129">Acessando cópias de sombra não persistentes</span><span class="sxs-lookup"><span data-stu-id="b9e5e-129">Accessing Nonpersistent Shadow Copies</span></span>

<span data-ttu-id="b9e5e-130">As cópias de sombra não persistentes são excluídas automaticamente quando o programa que as cria (neste caso, VShadow) é encerrado.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-130">Nonpersistent shadow copies are automatically deleted when the program that creates them (in this case, VShadow) exits.</span></span> <span data-ttu-id="b9e5e-131">Para acessar o conteúdo dessas cópias de sombra, o VShadow permite que você execute um script depois que as cópias de sombra são criadas, mas antes da saída do programa VShadow.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-131">To access the contents of these shadow copies, VShadow allows you to execute a script after the shadow copies are created but before the VShadow program exits.</span></span>

<span data-ttu-id="b9e5e-132">O exemplo a seguir mostra como usar a opção de linha de comando-exec para executar um script chamado "enum. cmd":</span><span class="sxs-lookup"><span data-stu-id="b9e5e-132">The following example shows how to use the -exec command-line option to run a script called "enum.cmd":</span></span>

<span data-ttu-id="b9e5e-133">**vshadow-NW-exec = enum. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-133">**vshadow -nw -exec=enum.cmd c:**</span></span>

<span data-ttu-id="b9e5e-134">No script executado, você também pode executar o script SETVAR gerado neste comando personalizado.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-134">In the executed script, you can also run the generated SETVAR script in this custom command.</span></span> <span data-ttu-id="b9e5e-135">Isso permite que o script acesse o conteúdo das cópias de sombra diretamente.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-135">This allows the script to access the contents of the shadow copies directly.</span></span> <span data-ttu-id="b9e5e-136">Lembre-se de que o dispositivo de sombra pode ser recuperado da \_ variável de ambiente do dispositivo VSHADOW \_ nnn.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-136">Remember that the shadow device can be retrieved from the VSHADOW\_DEVICE\_NNN environment variable.</span></span>

<span data-ttu-id="b9e5e-137">Aqui está um exemplo de script enum. cmd:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-137">Here is an example enum.cmd script:</span></span>

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

<span data-ttu-id="b9e5e-138">Aqui está a linha de comando para executar o script enum. cmd:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-138">Here is the command line to execute the enum.cmd script:</span></span>

<span data-ttu-id="b9e5e-139">**vshadow-NW-exec = c: \\ enum. cmd-script = setvar1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-139">**vshadow -nw -exec=c:\\enum.cmd -script=setvar1.cmd c:**</span></span>

## <a name="copying-a-file-from-a-shadow-copy"></a><span data-ttu-id="b9e5e-140">Copiando um arquivo de uma cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="b9e5e-140">Copying a File from a Shadow Copy</span></span>

<span data-ttu-id="b9e5e-141">O exemplo a seguir mostra como copiar um arquivo de uma cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-141">The following example shows how to copy a file from a shadow copy.</span></span>

1.  <span data-ttu-id="b9e5e-142">**Dir > c: \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-142">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="b9e5e-143">**vshadow-p-NW-script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-143">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="b9e5e-144">**chamar SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-144">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="b9e5e-145">**copiar% VSHADOW do \_ dispositivo \_ 1% \\somefile.txt c: \\ algum \_bak.txt**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-145">**copy %VSHADOW\_DEVICE\_1%\\somefile.txt c:\\somefile\_bak.txt**</span></span>

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a><span data-ttu-id="b9e5e-146">Enumerando todos os arquivos em um dispositivo de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="b9e5e-146">Enumerating All Files on a Shadow Copy Device</span></span>

<span data-ttu-id="b9e5e-147">O exemplo a seguir mostra como enumerar todos os arquivos em um dispositivo de cópia de sombra de um arquivo em lotes.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-147">The following example shows how to enumerate all files on a shadow copy device from a batch file.</span></span>

1.  <span data-ttu-id="b9e5e-148">**Dir > c: \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-148">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="b9e5e-149">**vshadow-p-NW-script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-149">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="b9e5e-150">**chamar SETVAR1. cmd**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-150">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="b9e5e-151">**para/R% VSHADOW \_ dispositivo \_ 1% \\ %% i in ( \* ) do @echo %% i**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-151">**for /R %VSHADOW\_DEVICE\_1%\\ %%i in (\*) do @echo %%i**</span></span>

## <a name="importing-a-transportable-shadow-copy"></a><span data-ttu-id="b9e5e-152">Importando uma cópia de sombra transportável</span><span class="sxs-lookup"><span data-stu-id="b9e5e-152">Importing a Transportable Shadow Copy</span></span>

<span data-ttu-id="b9e5e-153">Para criar uma cópia de sombra transportável em um computador e importá-la para outra máquina, você deve ter dois computadores conectados (por meio de uma configuração de SAN) a uma matriz de armazenamento que ofereça suporte a cópias de sombra de hardware do VSS.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-153">To create a transportable shadow copy on one machine and import it to another machine, you must have two computers that are connected (through a SAN configuration) to a storage array that supports VSS hardware shadow copies.</span></span> <span data-ttu-id="b9e5e-154">Um provedor de hardware VSS deve ser instalado em cada computador.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-154">A VSS hardware provider must be installed on each computer.</span></span>

<span data-ttu-id="b9e5e-155">O exemplo a seguir mostra como criar e importar a cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-155">The following example shows how to create and import the shadow copy.</span></span>

1.  <span data-ttu-id="b9e5e-156">Crie o conjunto de cópias de sombra no computador A (o servidor de produção) digitando o seguinte comando após o prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-156">Create the shadow copy set on computer A (the production server) by typing the following command after the command prompt:</span></span>

    <span data-ttu-id="b9e5e-157">**vshadow-p-t =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-157">**vshadow -p -t=bc1.xml**</span></span>

    <span data-ttu-id="b9e5e-158">Isso não vai expor nenhum dispositivo de cópia de sombra no computador A.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-158">This will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="b9e5e-159">Copie o documento de componentes de backup (bc1.xml) do computador A para o computador B.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-159">Copy the backup components document (bc1.xml) from computer A to computer B.</span></span>
3.  <span data-ttu-id="b9e5e-160">Importe o conjunto de sombras no computador B digitando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-160">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="b9e5e-161">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-161">**vshadow -i=bc1.xml**</span></span>

<span data-ttu-id="b9e5e-162">Opcionalmente, você pode expor essas cópias de sombra como letras de unidade ou pastas montadas.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-162">Optionally, you could expose these shadow copies as drive letters or mounted folders.</span></span> <span data-ttu-id="b9e5e-163">Além disso, você poderia interromper o conjunto de sombras para fazer os novos volumes de cópia de sombra de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-163">Also, you could potentially break the shadow set to make the new shadow copy volumes read-write.</span></span>

<span data-ttu-id="b9e5e-164">Para automatizar o processo de gerenciamento do conjunto de sombras, você pode usar a opção de linha de comando **-script** para gerar o script cmd que contém as IDs de cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-164">To automate the shadow set management process you might use the **-script** command-line option to generate the CMD script containing the shadow copy IDs.</span></span> <span data-ttu-id="b9e5e-165">Em seguida, você pode copiar o script gerado junto com os componentes de backup para o outro computador.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-165">Then you can copy the generated script along with the backup components to the other computer.</span></span>

<span data-ttu-id="b9e5e-166">O exemplo a seguir mostra como criar, expor e quebrar cópias de sombra transportáveis usando scripts CMD.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-166">The following example shows how to create, expose, and break transportable shadow copies using CMD scripts.</span></span>

1.  <span data-ttu-id="b9e5e-167">Crie o conjunto de cópias de sombra no computador A (o servidor de produção) na linha de comando da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-167">Create the shadow copy set on computer A (the production server) from the command line as follows:</span></span>

    <span data-ttu-id="b9e5e-168">**vshadow-p-t =bc1.xml-script = SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-168">**vshadow -p -t=bc1.xml -script=sc1.cmd**</span></span>

    <span data-ttu-id="b9e5e-169">Especifique a opção **-script** para gerar o script que contém as definições de variável de ambiente adequadas.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-169">Specify the **-script** option to generate the script containing the proper environment variable definitions.</span></span> <span data-ttu-id="b9e5e-170">Observe que isso não vai expor nenhum dispositivo de cópia de sombra no computador A.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-170">Note that this will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="b9e5e-171">Copie o documento de componentes de backup (bc1.xml) e o script gerado (SC1. cmd) do computador A para o computador B.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-171">Copy the backup components document (bc1.xml) and the generated script (sc1.cmd) from computer A to computer B.</span></span>
3.  <span data-ttu-id="b9e5e-172">Importe o conjunto de sombras no computador B digitando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-172">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="b9e5e-173">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-173">**vshadow -i=bc1.xml**</span></span>

    <span data-ttu-id="b9e5e-174">Isso causará a superfície dos dispositivos criados no computador B.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-174">This will surface the created devices on computer B.</span></span>

4.  <span data-ttu-id="b9e5e-175">Execute o script gerado para definir as variáveis de ambiente para o conjunto de cópias de sombra digitando o nome do arquivo no prompt de comando, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-175">Run the generated script to set the environment variables for the shadow copy set by typing the file name at the command prompt as in the following example:</span></span>

    <span data-ttu-id="b9e5e-176">**SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-176">**sc1.cmd**</span></span>

    <span data-ttu-id="b9e5e-177">Isso definirá as variáveis de ambiente relevantes, conforme descrito em acessar propriedades de cópia de sombra de um script CMD.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-177">This will set the relevant environment variables as described in Access Shadow Copy Properties from a CMD Script.</span></span>

5.  <span data-ttu-id="b9e5e-178">Expor as cópias de sombra no computador B digitando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-178">Expose the shadow copies on computer B by typing the following commands:</span></span>
    1.  <span data-ttu-id="b9e5e-179">**rmdir/s c: \\ ponto de montagem \_**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-179">**rmdir /s c:\\mount\_point**</span></span>
    2.  <span data-ttu-id="b9e5e-180">**mkdir c: \\ ponto de montagem \_**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-180">**mkdir c:\\mount\_point**</span></span>
    3.  <span data-ttu-id="b9e5e-181">**vshadow – El =% VSHADOW \_ ID \_ 1%, c: \\ ponto de montagem \_**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-181">**vshadow –el=%VSHADOW\_ID\_1%,c:\\mount\_point**</span></span>

    <span data-ttu-id="b9e5e-182">Isso causará a superfície dos dispositivos de cópia de sombra criados no computador B.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-182">This will surface the created shadow copy devices on computer B.</span></span>
6.  <span data-ttu-id="b9e5e-183">Interrompa o conjunto de cópias de sombra para tornar os volumes graváveis digitando o seguinte comando:**C: \\>vshadow – BW =% vshadow \_ set \_ ID%**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-183">Break the shadow copy set to make the volumes writable by typing the following command:**C:\\>vshadow –bw=%VSHADOW\_SET\_ID%**</span></span>

<span data-ttu-id="b9e5e-184">Observe que as cópias de sombra transportáveis não persistentes também podem ser importadas, mas são excluídas automaticamente quando o processo **vshadow** **-i** é encerrado.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-184">Note that nonpersistent transportable shadow copies can also be imported, but they are automatically deleted when the **vshadow** **-i** process exits.</span></span> <span data-ttu-id="b9e5e-185">Para importar as cópias de sombra antes que elas sejam excluídas, você deve usar a opção de linha de comando **-exec** , conforme descrito em acessar cópias de sombra não persistentes.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-185">To import the shadow copies before they are deleted, you must use the **-exec** command-line option as described in Access Nonpersistent Shadow Copies.</span></span>

## <a name="including-writers-or-components"></a><span data-ttu-id="b9e5e-186">Incluindo gravadores ou componentes</span><span class="sxs-lookup"><span data-stu-id="b9e5e-186">Including Writers or Components</span></span>

<span data-ttu-id="b9e5e-187">Por padrão, todos os gravadores participam da criação da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-187">By default, all writers participate in shadow copy creation.</span></span> <span data-ttu-id="b9e5e-188">Para determinar quais gravadores e componentes serão incluídos em um conjunto de cópias de sombra, use a opção de linha de comando **-WM** ou **-wm2** , conforme descrito em [listando o status do gravador e os metadados](vshadow-tool-and-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b9e5e-188">To determine which writers and components will be included in a shadow copy set, use the **-wm** or **-wm2** command-line option as described in [Listing Writer Status and Metadata](vshadow-tool-and-sample.md).</span></span>

<span data-ttu-id="b9e5e-189">Para verificar se todos os componentes de um gravador estão incluídos, use o sinalizador opcional **-Wi** em qualquer um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-189">To verify that all of a writer's components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="b9e5e-190">**vshadow** **-Wi** *WriterName*</span><span class="sxs-lookup"><span data-stu-id="b9e5e-190">**vshadow** **-wi** *WriterName*</span></span>
-   <span data-ttu-id="b9e5e-191">**vshadow** **-Wi** **"**_cadeia de nome do gravador_*_"_*</span><span class="sxs-lookup"><span data-stu-id="b9e5e-191">**vshadow** **-wi** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="b9e5e-192">**vshadow** **-Wi** **{**_WriterId_*_}_*</span><span class="sxs-lookup"><span data-stu-id="b9e5e-192">**vshadow** **-wi** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="b9e5e-193">**vshadow** **-Wi** **{**_InstanceId_*_}_*</span><span class="sxs-lookup"><span data-stu-id="b9e5e-193">**vshadow** **-wi** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="b9e5e-194">Para verificar se os componentes específicos estão incluídos, use o sinalizador opcional **-Wi** em qualquer um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-194">To verify that specific components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="b9e5e-195">**vshadow** **-Wi** \*WriterName \***: \\**_LogicalPath_\* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="b9e5e-195">**vshadow** **-wi** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="b9e5e-196">**vshadow** **-Wi** **"**_cadeia de nome do gravador_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="b9e5e-196">**vshadow** **-wi** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="b9e5e-197">**vshadow** **-Wi** **{**_WriterId_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="b9e5e-197">**vshadow** **-wi** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="b9e5e-198">**vshadow** **-Wi** **{**_InstanceId_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="b9e5e-198">**vshadow** **-wi** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="b9e5e-199">Os exemplos a seguir mostram como usar o sinalizador opcional **-Wi** .</span><span class="sxs-lookup"><span data-stu-id="b9e5e-199">The following examples show how to use the **-wi** optional flag.</span></span>

-   <span data-ttu-id="b9e5e-200">Especificando *WriterName*: \\ *LogicalPath* \\ *ComponentName*:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-200">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="b9e5e-201">**vshadow-Wi = "gravador do registro: \\ registro"**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-201">**vshadow -wi="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="b9e5e-202">Especificando {*WriterId*}:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-202">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="b9e5e-203">**vshadow-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-203">**vshadow -wi={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="b9e5e-204">Especificando mais de um gravador ou componente:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-204">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="b9e5e-205">**vshadow-Wi = "gravador do registro: \\ registro"-Wi = "gravador REGDB com+"**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-205">**vshadow -wi="Registry Writer:\\Registry" -wi="COM+ REGDB Writer"**</span></span>

## <a name="excluding-writers-or-components"></a><span data-ttu-id="b9e5e-206">Excluindo gravadores ou componentes</span><span class="sxs-lookup"><span data-stu-id="b9e5e-206">Excluding Writers or Components</span></span>

<span data-ttu-id="b9e5e-207">Para excluir todos os gravadores, use o sinalizador opcional **-NW** ao criar a cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-207">To exclude all writers, use the **-nw** optional flag when creating the shadow copy.</span></span>

<span data-ttu-id="b9e5e-208">Para excluir todos os componentes de um gravador, use o sinalizador opcional **-WX** em qualquer um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-208">To exclude all of a writer's components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="b9e5e-209">**vshadow** **-WX** *WriterName*</span><span class="sxs-lookup"><span data-stu-id="b9e5e-209">**vshadow** **-wx** *WriterName*</span></span>
-   <span data-ttu-id="b9e5e-210">**vshadow** **-WX** **"**_cadeia de nome do gravador_*_"_*</span><span class="sxs-lookup"><span data-stu-id="b9e5e-210">**vshadow** **-wx** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="b9e5e-211">**vshadow** **-WX** **{**_WriterId_*_}_*</span><span class="sxs-lookup"><span data-stu-id="b9e5e-211">**vshadow** **-wx** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="b9e5e-212">**vshadow** **-WX** **{**_InstanceId_*_}_*</span><span class="sxs-lookup"><span data-stu-id="b9e5e-212">**vshadow** **-wx** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="b9e5e-213">Para excluir componentes específicos, use o sinalizador opcional **-WX** em qualquer um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-213">To exclude specific components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="b9e5e-214">**vshadow** **-WX** \*WriterName \***: \\**_LogicalPath_\* _\\_ \* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="b9e5e-214">**vshadow** **-wx** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="b9e5e-215">**vshadow** **-WX** **"**_cadeia de nome do gravador_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="b9e5e-215">**vshadow** **-wx** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="b9e5e-216">**vshadow** **-WX** **{**_WriterId_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="b9e5e-216">**vshadow** **-wx** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="b9e5e-217">**vshadow** **-WX** **{**_InstanceId_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_</span><span class="sxs-lookup"><span data-stu-id="b9e5e-217">**vshadow** **-wx** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="b9e5e-218">Os exemplos a seguir mostram como usar o sinalizador opcional **-WX** .</span><span class="sxs-lookup"><span data-stu-id="b9e5e-218">The following examples show how to use the **-wx** optional flag.</span></span>

-   <span data-ttu-id="b9e5e-219">Especificando *WriterName*: \\ *LogicalPath* \\ *ComponentName*:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-219">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="b9e5e-220">**vshadow-WX = "gravador do registro: \\ registro"**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-220">**vshadow -wx="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="b9e5e-221">Especificando {*WriterId*}:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-221">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="b9e5e-222">**vshadow-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-222">**vshadow -wx={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="b9e5e-223">Especificando mais de um gravador ou componente:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-223">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="b9e5e-224">**vshadow-WX = "gravador do registro: \\ registro"-WX = "gravador REGDB do com+"**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-224">**vshadow -wx="Registry Writer:\\Registry" -wx="COM+ REGDB Writer"**</span></span>

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="b9e5e-225">Quebrando conjuntos de cópias de sombra usando o método BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="b9e5e-225">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="b9e5e-226">Os exemplos a seguir mostram como usar a opção de linha de comando **-Bex** .</span><span class="sxs-lookup"><span data-stu-id="b9e5e-226">The following examples show how to use the **-bex** command-line option.</span></span>

-   <span data-ttu-id="b9e5e-227">Especificar que o LUN de cópia de sombra será mascarado do host:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-227">Specifying that the shadow copy LUN will be masked from the host:</span></span>

    <span data-ttu-id="b9e5e-228">**vshadow** **-Bex** **-Mask**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-228">**vshadow** **-bex** **-mask**</span></span>

-   <span data-ttu-id="b9e5e-229">Especificar que o LUN de cópia de sombra será exposto ao host como um volume de leitura/gravação:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-229">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume:</span></span>

    <span data-ttu-id="b9e5e-230">**vshadow** **-Bex** **-RW**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-230">**vshadow** **-bex** **-rw**</span></span>

-   <span data-ttu-id="b9e5e-231">Especificar que o LUN de cópia de sombra será exposto ao host como um volume de leitura/gravação e que nenhuma das assinaturas de disco nos LUNs de cópia de sombra será revertida para o dos LUNs originais:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-231">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume, and that none of the disk signatures on the shadow copy LUNs will be reverted to that of the original LUNs:</span></span>

    <span data-ttu-id="b9e5e-232">**vshadow** **-Bex** **-norevert**</span><span class="sxs-lookup"><span data-stu-id="b9e5e-232">**vshadow** **-bex** **-norevert**</span></span>

 

 

---
description: VShadow é uma ferramenta de linha de comando que você pode usar para criar e gerenciar cópias de sombra de volume.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Ferramenta VShadow e exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461136"
---
# <a name="vshadow-tool-and-sample"></a><span data-ttu-id="f513c-103">Ferramenta VShadow e exemplo</span><span class="sxs-lookup"><span data-stu-id="f513c-103">VShadow Tool and Sample</span></span>

<span data-ttu-id="f513c-104">VShadow é uma ferramenta de linha de comando que você pode usar para criar e gerenciar cópias de sombra de volume.</span><span class="sxs-lookup"><span data-stu-id="f513c-104">VShadow is a command-line tool that you can use to create and manage volume shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="f513c-105">O VShadow está incluído no Microsoft Windows Software Development Kit (SDK) para Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="f513c-105">VShadow is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="f513c-106">O SDK 7,2 do VSS inclui uma versão do VShadow que é executada somente no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f513c-106">The VSS 7.2 SDK includes a version of VShadow that runs only on Windows Server 2003.</span></span> <span data-ttu-id="f513c-107">Para obter informações sobre como baixar o SDK do Windows e o SDK 7,2 do VSS, consulte [serviço de cópias de sombra de volume](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f513c-107">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="f513c-108">A ferramenta VShadow usa opções de linha de comando e sinalizadores opcionais para identificar o trabalho a ser executado.</span><span class="sxs-lookup"><span data-stu-id="f513c-108">The VShadow tool uses command-line options and optional flags to identify the work to perform.</span></span> <span data-ttu-id="f513c-109">Quando usado sem nenhuma opção de linha de comando, o comando VShadow cria um novo conjunto de cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="f513c-109">When used without any command-line options, the VShadow command creates a new shadow copy set.</span></span>

<span data-ttu-id="f513c-110">Os comandos VShadow executam as seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="f513c-110">VShadow commands perform the following operations:</span></span>

-   [<span data-ttu-id="f513c-111">Criando um conjunto de cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="f513c-111">Creating a Shadow Copy Set</span></span>](#creating-a-shadow-copy-set)
-   [<span data-ttu-id="f513c-112">Importando um conjunto de cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="f513c-112">Importing a Shadow Copy Set</span></span>](#importing-a-shadow-copy-set)
-   [<span data-ttu-id="f513c-113">Consultando Propriedades de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="f513c-113">Querying Shadow Copy Properties</span></span>](#querying-shadow-copy-properties)
-   [<span data-ttu-id="f513c-114">Excluindo cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="f513c-114">Deleting Shadow Copies</span></span>](#deleting-shadow-copies)
-   [<span data-ttu-id="f513c-115">Quebrando um conjunto de cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="f513c-115">Breaking a Shadow Copy Set</span></span>](#breaking-a-shadow-copy-set)
-   [<span data-ttu-id="f513c-116">Quebrando um conjunto de cópias de sombra usando o método BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="f513c-116">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [<span data-ttu-id="f513c-117">Expondo uma cópia de sombra localmente</span><span class="sxs-lookup"><span data-stu-id="f513c-117">Exposing a Shadow Copy Locally</span></span>](#exposing-a-shadow-copy-locally)
-   [<span data-ttu-id="f513c-118">Expondo uma cópia de sombra remotamente</span><span class="sxs-lookup"><span data-stu-id="f513c-118">Exposing a Shadow Copy Remotely</span></span>](#exposing-a-shadow-copy-remotely)
-   [<span data-ttu-id="f513c-119">Listando os metadados e o status do gravador</span><span class="sxs-lookup"><span data-stu-id="f513c-119">Listing Writer Status and Metadata</span></span>](#listing-writer-status-and-metadata)
-   [<span data-ttu-id="f513c-120">Executando operações de restauração</span><span class="sxs-lookup"><span data-stu-id="f513c-120">Performing Restore Operations</span></span>](#performing-restore-operations)
-   [<span data-ttu-id="f513c-121">Revertendo para uma cópia de sombra anterior</span><span class="sxs-lookup"><span data-stu-id="f513c-121">Reverting to a Previous Shadow Copy</span></span>](#reverting-to-a-previous-shadow-copy)
-   [<span data-ttu-id="f513c-122">Ressincronizando LUNs</span><span class="sxs-lookup"><span data-stu-id="f513c-122">Resynchronizing LUNs</span></span>](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a><span data-ttu-id="f513c-123">Criando um conjunto de cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="f513c-123">Creating a Shadow Copy Set</span></span>

<span data-ttu-id="f513c-124">**vshadow** \[ OptionalFlags \] *volumelist*</span><span class="sxs-lookup"><span data-stu-id="f513c-124">**vshadow** \[OptionalFlags\] *VolumeList*</span></span>

<span data-ttu-id="f513c-125">Este comando cria um novo conjunto de cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="f513c-125">This command creates a new shadow copy set.</span></span>

<span data-ttu-id="f513c-126">*Volumelist* é uma lista de nomes de volume.</span><span class="sxs-lookup"><span data-stu-id="f513c-126">*VolumeList* is a list of volume names.</span></span> <span data-ttu-id="f513c-127">VShadow cria uma cópia de sombra para cada volume na lista.</span><span class="sxs-lookup"><span data-stu-id="f513c-127">VShadow creates one shadow copy for each volume in the list.</span></span> <span data-ttu-id="f513c-128">Um nome de volume pode, opcionalmente, ser encerrado com uma barra invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="f513c-128">A volume name can optionally be terminated with a backslash (\\).</span></span> <span data-ttu-id="f513c-129">Por exemplo, C: e C: \\ são nomes de volume válidos.</span><span class="sxs-lookup"><span data-stu-id="f513c-129">For example, both C: and C:\\ are valid volume names.</span></span> <span data-ttu-id="f513c-130">Você também pode especificar pastas montadas (por exemplo, C: \\ DirectoryName) ou nomes de GUID de volume (por exemplo, \\ \\ ? \\ Volume {edbed95e-7e8d-11D8-9d01-505054503030}).</span><span class="sxs-lookup"><span data-stu-id="f513c-130">You can also specify mounted folders (for example, C:\\DirectoryName) or volume GUID names (for example, \\\\?\\Volume{edbed95e-7e8d-11d8-9d01-505054503030}).</span></span>

<span data-ttu-id="f513c-131">*OptionalFlags* é um bitmask de valores de sinalizador opcionais da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f513c-131">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f513c-132">Valor de sinalizador opcional</span><span class="sxs-lookup"><span data-stu-id="f513c-132">Optional Flag Value</span></span></th>
<th><span data-ttu-id="f513c-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="f513c-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f513c-134"><span id="-ad"></span><span id="-AD"></span><strong>-AD</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-135">Esse sinalizador opcional especifica cópias de sombra de hardware diferenciais.</span><span class="sxs-lookup"><span data-stu-id="f513c-135">This optional flag specifies differential hardware shadow copies.</span></span> <span data-ttu-id="f513c-136">Esse sinalizador e o sinalizador <strong>-AP</strong> são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f513c-136">This flag and the <strong>-ap</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-137">Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-137">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f513c-138"><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-138"><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-139">Esse sinalizador opcional especifica cópias de sombra de hardware de plex.</span><span class="sxs-lookup"><span data-stu-id="f513c-139">This optional flag specifies plex hardware shadow copies.</span></span> <span data-ttu-id="f513c-140">Esse sinalizador e o sinalizador <strong>-ad</strong> são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f513c-140">This flag and the <strong>-ad</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-141">Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-141">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f513c-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>File</em><strong>. xml</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span> <strong></strong> <strong>-bc=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-143">Esse sinalizador opcional especifica cópias de sombra não transportáveis e armazena o documento de componentes de backup no arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="f513c-143">This optional flag specifies non-transportable shadow copies and stores the Backup Components Document into the specified file.</span></span> <span data-ttu-id="f513c-144">Esse arquivo pode ser usado em uma operação de restauração subsequente.</span><span class="sxs-lookup"><span data-stu-id="f513c-144">This file can be used in a subsequent restore operation.</span></span> <span data-ttu-id="f513c-145">Esse sinalizador e o sinalizador <strong>-t</strong> são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f513c-145">This flag and the <strong>-t</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-146">Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-146">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f513c-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec =</strong><em>comando</em></span><span class="sxs-lookup"><span data-stu-id="f513c-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec=</strong><em>Command</em></span></span><br/></td>
<td><span data-ttu-id="f513c-148">Esse sinalizador opcional executa um comando ou script depois que as cópias de sombra são criadas, mas antes da ferramenta VShadow ser encerrada.</span><span class="sxs-lookup"><span data-stu-id="f513c-148">This optional flag executes a command or script after the shadow copies are created but before the VShadow tool exits.</span></span> <span data-ttu-id="f513c-149">O <em>comando</em> pode especificar um comando shell executável ou um arquivo cmd.</span><span class="sxs-lookup"><span data-stu-id="f513c-149"><em>Command</em> can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="f513c-150">Se ele especificar um comando do Shell, nenhum parâmetro de comando poderá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="f513c-150">If it specifies a shell command, no command parameters can be specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-151">Por motivos de segurança e para manter a implementação simples, o sinalizador opcional <strong>-exec</strong> não aceitará parâmetros a serem passados para o comando ou script.</span><span class="sxs-lookup"><span data-stu-id="f513c-151">For security reasons and to keep the implementation simple, the <strong>-exec</strong> optional flag will not accept parameters to be passed to the command or script.</span></span> <span data-ttu-id="f513c-152">A cadeia de caracteres inteira passada para o sinalizador opcional <strong>-exec</strong> é tratada como um único arquivo cmd ou exe.</span><span class="sxs-lookup"><span data-stu-id="f513c-152">The entire string passed to the <strong>-exec</strong> optional flag is treated as a single CMD or EXE file.</span></span> <span data-ttu-id="f513c-153">Para obter mais informações sobre essa limitação, consulte o código-fonte VShadow.</span><span class="sxs-lookup"><span data-stu-id="f513c-153">For more information about this limitation, see the VShadow source code.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f513c-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-155">Esse sinalizador opcional especifica que a operação de cópia de sombra deve ser concluída somente se todas as assinaturas de disco puderem ser revertidas.</span><span class="sxs-lookup"><span data-stu-id="f513c-155">This optional flag specifies that the shadow copy operation should be completed only if all disk signatures can be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-156">Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-156">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="f513c-157"><strong>Windows Server 2003:</strong> Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f513c-157"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f513c-158"><span id="-mask"></span><span id="-MASK"></span><strong>-máscara</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-158"><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-159">Esse sinalizador opcional especifica que os LUNs de cópia de sombra devem ser mascarados do computador quando o conjunto de cópias de sombra for rompido.</span><span class="sxs-lookup"><span data-stu-id="f513c-159">This optional flag specifies that the shadow copy LUNs should be masked from the computer when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-160">Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-160">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="f513c-161"><strong>Windows Server 2003:</strong> Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f513c-161"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f513c-162"><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-162"><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-163">Esse sinalizador opcional especifica cópias de sombra sem recuperação automática.</span><span class="sxs-lookup"><span data-stu-id="f513c-163">This optional flag specifies shadow copies without auto-recovery.</span></span> <span data-ttu-id="f513c-164">Para obter mais informações sobre essa opção, consulte a documentação do sinalizador de VSS_VOLSNAP_ATTR_NO_AUTORECOVERY da enumeração <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f513c-164">For more information about this option, see the documentation for the VSS_VOLSNAP_ATTR_NO_AUTORECOVERY flag of the <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f513c-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-166">Esse sinalizador opcional especifica que as assinaturas de disco não devem ser revertidas.</span><span class="sxs-lookup"><span data-stu-id="f513c-166">This optional flag specifies that disk signatures should not be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-167">Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-167">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="f513c-168"><strong>Windows Server 2003:</strong> Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f513c-168"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f513c-169"><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-169"><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-170">Esse sinalizador opcional especifica cópias de sombra sem envolver gravadores.</span><span class="sxs-lookup"><span data-stu-id="f513c-170">This optional flag specifies shadow copies without involving writers.</span></span> <span data-ttu-id="f513c-171">Para obter mais informações sobre cópias de sombra sem participação no gravador, consulte <a href="shadow-copy-creation-details.md">detalhes da criação da cópia de sombra</a>.</span><span class="sxs-lookup"><span data-stu-id="f513c-171">For more information about shadow copies without writer participation, see <a href="shadow-copy-creation-details.md">Shadow Copy Creation Details</a>.</span></span> <span data-ttu-id="f513c-172">Esse sinalizador e os sinalizadores <strong>-Wi</strong> e <strong>-WX</strong> são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f513c-172">This flag and the <strong>-wi</strong> and <strong>-wx</strong> flags are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f513c-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-174">Esse sinalizador opcional especifica <a href="vssgloss-p.md"><em>cópias de sombra persistentes</em></a>.</span><span class="sxs-lookup"><span data-stu-id="f513c-174">This optional flag specifies <a href="vssgloss-p.md"><em>persistent shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-175">Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-175">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f513c-176"><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-176"><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-177">Esse sinalizador opcional especifica que os LUNs de cópia de sombra devem se tornar de leitura/gravação quando o conjunto de cópias de sombra é rompido.</span><span class="sxs-lookup"><span data-stu-id="f513c-177">This optional flag specifies that the shadow copy LUNs should be made read/write when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-178">Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-178">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="f513c-179"><strong>Windows Server 2003:</strong> Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f513c-179"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f513c-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-181">Esse sinalizador opcional especifica <a href="vssgloss-c.md"><em>cópias de sombra acessíveis ao cliente</em></a>.</span><span class="sxs-lookup"><span data-stu-id="f513c-181">This optional flag specifies <a href="vssgloss-c.md"><em>client-accessible shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-182">Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-182">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f513c-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em>File</em><strong>. cmd</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>File</em><strong>.cmd</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-184">Esse sinalizador opcional gera um arquivo CMD contendo variáveis de ambiente relacionadas às cópias de sombra criadas, como IDs de cópia de sombra e IDs de conjunto de cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="f513c-184">This optional flag generates a CMD file containing environment variables related to the created shadow copies, such as shadow copy IDs and shadow copy set IDs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f513c-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>File</em><strong>. xml</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-186">Esse sinalizador opcional especifica cópias de sombra transportáveis e armazena o documento de componentes de backup no arquivo especificado pelo parâmetro <em>File.xml</em> .</span><span class="sxs-lookup"><span data-stu-id="f513c-186">This optional flag specifies transportable shadow copies and stores the Backup Components Document into the file specified by the <em>File.xml</em> parameter.</span></span> <span data-ttu-id="f513c-187">Esse arquivo pode ser usado em uma operação de importação e/ou restauração subsequente.</span><span class="sxs-lookup"><span data-stu-id="f513c-187">This file can be used in a subsequent import and/or restore operation.</span></span> <span data-ttu-id="f513c-188">Esse sinalizador e o sinalizador <strong>-BC</strong> são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f513c-188">This flag and the <strong>-bc</strong> flag are mutually exclusive.</span></span><br/> <span data-ttu-id="f513c-189"><strong>Windows server 2003, Standard Edition e Windows server 2003, Web Edition:</strong> Não há suporte para cópias de sombra transportáveis.</span><span class="sxs-lookup"><span data-stu-id="f513c-189"><strong>Windows Server 2003, Standard Edition and Windows Server 2003, Web Edition:</strong> Transportable shadow copies are not supported.</span></span> <span data-ttu-id="f513c-190">Todas as edições do Windows Server 2003 com Service Pack 1 (SP1) oferecem suporte a cópias de sombra transportáveis.</span><span class="sxs-lookup"><span data-stu-id="f513c-190">All editions of Windows Server 2003 with Service Pack 1 (SP1) support transportable shadow copies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f513c-191"><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-191"><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-192">Esse sinalizador opcional especifica que a recuperação TxF deve ser imposta durante a criação da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="f513c-192">This optional flag specifies that TxF recovery should be enforced during shadow copy creation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-193">Esse sinalizador tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-193">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f513c-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-rastreamento</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-195">Esse sinalizador opcional gera uma saída detalhada que pode ser usada para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="f513c-195">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f513c-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-aguardar</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-197">Esse sinalizador opcional faz com que a ferramenta VShadow aguarde a confirmação do usuário antes de sair.</span><span class="sxs-lookup"><span data-stu-id="f513c-197">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f513c-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>gravador</em></span><span class="sxs-lookup"><span data-stu-id="f513c-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="f513c-199">Esse sinalizador opcional verifica se o gravador ou o componente especificado está incluído na cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="f513c-199">This optional flag verifies that the specified writer or component is included in the shadow copy.</span></span> <span data-ttu-id="f513c-200">O <em>gravador</em> pode especificar um caminho de componente, o nome do gravador, a ID do gravador ou a ID da instância do gravador.</span><span class="sxs-lookup"><span data-stu-id="f513c-200"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="f513c-201">Esse sinalizador e o sinalizador <strong>-NW</strong> são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f513c-201">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f513c-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>gravador</em></span><span class="sxs-lookup"><span data-stu-id="f513c-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="f513c-203">Esse sinalizador opcional verifica se o gravador ou o componente especificado foi excluído da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="f513c-203">This optional flag verifies that the specified writer or component is excluded from the shadow copy.</span></span> <span data-ttu-id="f513c-204">O <em>gravador</em> pode especificar um caminho de componente, o nome do gravador, a ID do gravador ou a ID da instância do gravador.</span><span class="sxs-lookup"><span data-stu-id="f513c-204"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="f513c-205">Esse sinalizador e o sinalizador <strong>-NW</strong> são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f513c-205">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a><span data-ttu-id="f513c-206">Importando um conjunto de cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="f513c-206">Importing a Shadow Copy Set</span></span>

<span data-ttu-id="f513c-207">**vshadow** \[ OptionalFlags \] **-i =**_File_*_. xml_*</span><span class="sxs-lookup"><span data-stu-id="f513c-207">**vshadow** \[OptionalFlags\] **-i=**_File_*_.xml_*</span></span>

<span data-ttu-id="f513c-208">A opção de linha de comando **-i** importa um conjunto de cópia de sombra transportável.</span><span class="sxs-lookup"><span data-stu-id="f513c-208">The **-i** command-line option imports a transportable shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="f513c-209">Essa opção de linha de comando tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-209">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="f513c-210">O arquivo de *File.xml* deve ser um arquivo de documento de componentes de backup para um conjunto de cópias de sombra transportáveis criado com o sinalizador opcional **-t** ou **-BC** .</span><span class="sxs-lookup"><span data-stu-id="f513c-210">The *File.xml* file must be a Backup Components Document file for a transportable shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="f513c-211">Um conjunto de cópias de sombra é uma [*cópia de sombra persistente*](vssgloss-p.md) se foi criado com o sinalizador **-p** opcional.</span><span class="sxs-lookup"><span data-stu-id="f513c-211">A shadow copy set is a [*persistent shadow copy*](vssgloss-p.md) if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="f513c-212">Se o conjunto de cópia de sombra transportável for não persistente, ele aparecerá por um curto período enquanto o comando de criação de cópia de sombra estiver em execução e será excluído automaticamente quando o comando retornar.</span><span class="sxs-lookup"><span data-stu-id="f513c-212">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="f513c-213">Você pode importar cópias de sombra não persistentes somente durante a criação da cópia de sombra, criando o conjunto de cópias de sombra usando o sinalizador opcional **-exec** para executar um arquivo cmd que chama VShadow **-i**.</span><span class="sxs-lookup"><span data-stu-id="f513c-213">You can import nonpersistent shadow copies only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls VShadow **-i**.</span></span>

<span data-ttu-id="f513c-214">A opção de linha de comando **-i** não pode ser combinada com outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f513c-214">The **-i** command-line option cannot be combined with other command-line options.</span></span>

<span data-ttu-id="f513c-215">*OptionalFlags* é um bitmask de valores de sinalizador opcionais da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f513c-215">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="f513c-216">Valor de sinalizador opcional</span><span class="sxs-lookup"><span data-stu-id="f513c-216">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="f513c-217">Descrição</span><span class="sxs-lookup"><span data-stu-id="f513c-217">Description</span></span>                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f513c-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_comando_</span><span class="sxs-lookup"><span data-stu-id="f513c-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="f513c-219">Esse sinalizador opcional executa um comando ou script depois que as cópias de sombra são importadas, mas antes da ferramenta VShadow ser encerrada.</span><span class="sxs-lookup"><span data-stu-id="f513c-219">This optional flag executes a command or script after the shadow copies are imported but before the VShadow tool exits.</span></span> <span data-ttu-id="f513c-220">O *comando* pode especificar um comando shell executável ou um arquivo cmd.</span><span class="sxs-lookup"><span data-stu-id="f513c-220">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="f513c-221">Se ele especificar um comando do Shell, nenhum parâmetro de comando poderá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="f513c-221">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="f513c-222"><span id="-tracing"></span><span id="-TRACING"></span>**-rastreamento**</span><span class="sxs-lookup"><span data-stu-id="f513c-222"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="f513c-223">Esse sinalizador opcional gera uma saída detalhada que pode ser usada para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="f513c-223">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="f513c-224"><span id="-wait"></span><span id="-WAIT"></span>**-aguardar**</span><span class="sxs-lookup"><span data-stu-id="f513c-224"><span id="-wait"></span><span id="-WAIT"></span>**-wait**</span></span><br/>                                                           | <span data-ttu-id="f513c-225">Esse sinalizador opcional faz com que a ferramenta VShadow aguarde a confirmação do usuário antes de sair.</span><span class="sxs-lookup"><span data-stu-id="f513c-225">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a><span data-ttu-id="f513c-226">Consultando Propriedades de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="f513c-226">Querying Shadow Copy Properties</span></span>

<span data-ttu-id="f513c-227">**vshadow** **-q**</span><span class="sxs-lookup"><span data-stu-id="f513c-227">**vshadow** **-q**</span></span>

<span data-ttu-id="f513c-228">**vshadow** **-qx =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="f513c-228">**vshadow** **-qx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="f513c-229">**vshadow** **-s =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="f513c-229">**vshadow** **-s=**_ShadowCopyId_</span></span>

<span data-ttu-id="f513c-230">A opção de linha de comando **-q** lista as propriedades de todas as cópias de sombra no computador.</span><span class="sxs-lookup"><span data-stu-id="f513c-230">The **-q** command-line option lists the properties of all shadow copies on the computer.</span></span>

<span data-ttu-id="f513c-231">A opção de linha de comando **-qx** lista as propriedades de todas as cópias de sombra no conjunto de cópias de sombra cuja ID é especificada por *ShadowCopySetId*.</span><span class="sxs-lookup"><span data-stu-id="f513c-231">The **-qx** command-line option lists the properties of all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="f513c-232">A opção de linha de comando **-s** lista as propriedades da cópia de sombra cuja ID é especificada por *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="f513c-232">The **-s** command-line option lists the properties of the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="f513c-233">Essas opções de linha de comando usam uma combinação de [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) e [**IVssBackupComponents:: getsnapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) para obter as propriedades do conjunto de cópias de sombra fornecido.</span><span class="sxs-lookup"><span data-stu-id="f513c-233">These command-line options use a combination of [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) and [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) to get the properties of the given set of shadow copies.</span></span>

<span data-ttu-id="f513c-234">As opções de linha de comando **-q**, **-qx** e **-s** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f513c-234">The **-q**, **-qx**, and **-s** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="deleting-shadow-copies"></a><span data-ttu-id="f513c-235">Excluindo cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="f513c-235">Deleting Shadow Copies</span></span>

<span data-ttu-id="f513c-236">**vshadow** **-da**</span><span class="sxs-lookup"><span data-stu-id="f513c-236">**vshadow** **-da**</span></span>

<span data-ttu-id="f513c-237">**vshadow** **-do**</span><span class="sxs-lookup"><span data-stu-id="f513c-237">**vshadow** **-do**</span></span>

<span data-ttu-id="f513c-238">**vshadow** **-DX =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="f513c-238">**vshadow** **-dx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="f513c-239">**vshadow** **-DS =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="f513c-239">**vshadow** **-ds=**_ShadowCopyId_</span></span>

<span data-ttu-id="f513c-240">O comando **-da** exclui todas as cópias de sombra no computador.</span><span class="sxs-lookup"><span data-stu-id="f513c-240">The **-da** command deletes all shadow copies on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="f513c-241">A opção de linha de comando **-da** requer a confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f513c-241">The **-da** command-line option requires user confirmation.</span></span>

 

<span data-ttu-id="f513c-242">A opção de linha de comando **-** do exclui a cópia de sombra mais antiga no computador.</span><span class="sxs-lookup"><span data-stu-id="f513c-242">The **-do** command-line option deletes the oldest shadow copy on the computer.</span></span>

<span data-ttu-id="f513c-243">A opção de linha de comando **-DX** exclui todas as cópias de sombra no conjunto de cópias de sombra cuja ID é especificada por *ShadowCopySetId*.</span><span class="sxs-lookup"><span data-stu-id="f513c-243">The **-dx** command-line option deletes all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="f513c-244">A opção de linha de comando **-DS** exclui a cópia de sombra cuja ID é especificada por *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="f513c-244">The **-ds** command-line option deletes the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="f513c-245">Essas opções de linha de comando são para uso somente com [*cópias de sombra persistentes*](vssgloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="f513c-245">These command-line options are for use with [*persistent shadow copies*](vssgloss-p.md) only.</span></span> <span data-ttu-id="f513c-246">As cópias de sombra não persistentes não precisam ser excluídas explicitamente, pois são excluídas automaticamente quando o comando de criação de VShadow é encerrado.</span><span class="sxs-lookup"><span data-stu-id="f513c-246">Nonpersistent shadow copies do not need to be explicitly deleted, because they are automatically deleted when the VShadow creation command exits.</span></span>

<span data-ttu-id="f513c-247">As opções de linha de comando **-da**, **-do**, **-DX** e **-DS** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f513c-247">The **-da**, **-do**, **-dx**, and **-ds** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set"></a><span data-ttu-id="f513c-248">Quebrando um conjunto de cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="f513c-248">Breaking a Shadow Copy Set</span></span>

<span data-ttu-id="f513c-249">**vshadow** **-b =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="f513c-249">**vshadow** **-b=**_ShadowCopySetId_</span></span>

<span data-ttu-id="f513c-250">**vshadow** **-BW =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="f513c-250">**vshadow** **-bw=**_ShadowCopySetId_</span></span>

<span data-ttu-id="f513c-251">A opção de linha de comando **-b =**_ShadowCopySetId_ converte cada cópia de sombra no conjunto de cópias de sombra em um volume autônomo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f513c-251">The **-b=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone read-only volume.</span></span>

<span data-ttu-id="f513c-252">A opção de linha de comando **-BW =**_ShadowCopySetId_ converte cada cópia de sombra no conjunto de cópias de sombra em um volume gravável autônomo.</span><span class="sxs-lookup"><span data-stu-id="f513c-252">The **-bw=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone writable volume.</span></span>

> [!Note]  
> <span data-ttu-id="f513c-253">As opções de linha de comando **-b** e **-BW** têm suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-253">The **-b** and **-bw** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="f513c-254">Para obter informações sobre como dividir um conjunto de cópias de sombra, consulte [quebrando cópias de sombra](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="f513c-254">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

<span data-ttu-id="f513c-255">Depois que o conjunto de cópias de sombra é interrompido, o conjunto de cópias de sombra e as cópias de sombra individuais não existem mais e não podem ser gerenciados usando comandos VSS.</span><span class="sxs-lookup"><span data-stu-id="f513c-255">After the shadow copy set is broken, the shadow copy set and the individual shadow copies no longer exist and cannot be managed using VSS commands.</span></span>

<span data-ttu-id="f513c-256">Um conjunto de cópias de sombra será persistente se tiver sido criado com o sinalizador **-p** opcional.</span><span class="sxs-lookup"><span data-stu-id="f513c-256">A shadow copy set is persistent if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="f513c-257">Se o conjunto de cópia de sombra transportável for não persistente, ele aparecerá por um curto período enquanto o comando de criação de cópia de sombra estiver em execução e será excluído automaticamente quando o comando retornar.</span><span class="sxs-lookup"><span data-stu-id="f513c-257">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="f513c-258">Você pode dividir conjuntos de cópias de sombra não persistentes somente durante a criação da cópia de sombra, criando o conjunto de cópias de sombra usando o sinalizador opcional **-exec** para executar um arquivo cmd que chama **vshadow** **-b** ou **vshadow** **-BW**.</span><span class="sxs-lookup"><span data-stu-id="f513c-258">You can break nonpersistent shadow copy sets only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls **vshadow** **-b** or **vshadow** **-bw**.</span></span>

<span data-ttu-id="f513c-259">As opções de linha de comando **-b** e **-BW** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f513c-259">The **-b** and **-bw** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="f513c-260">Quebrando um conjunto de cópias de sombra usando o método BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="f513c-260">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="f513c-261">**vshadow** **-Bex**</span><span class="sxs-lookup"><span data-stu-id="f513c-261">**vshadow** **-bex**</span></span>

<span data-ttu-id="f513c-262">A opção de linha de comando **-Bex** quebra um conjunto de cópias de sombra de acordo com as opções especificadas pelos sinalizadores opcional **-Mask**, **-RW**, **-forcerevert** e **-norevert** .</span><span class="sxs-lookup"><span data-stu-id="f513c-262">The **-bex** command-line option breaks a shadow copy set according to the options specified by the optional **-mask**, **-rw**, **-forcerevert**, and **-norevert** flags.</span></span> <span data-ttu-id="f513c-263">Essa opção de linha de comando é semelhante às opções de linha de comando **-b** e **-BW** .</span><span class="sxs-lookup"><span data-stu-id="f513c-263">This command-line option is similar to the **-b** and **-bw** command-line options.</span></span> <span data-ttu-id="f513c-264">A opção de linha de comando **-Bex** usa o método [**IVssBackupComponentsEx2:: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) , enquanto as opções de linha de comando **-b** e **-BW** usam o método [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .</span><span class="sxs-lookup"><span data-stu-id="f513c-264">The **-bex** command-line option uses the [**IVssBackupComponentsEx2::BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) method, whereas the **-b** and **-bw** command-line options use the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>

<span data-ttu-id="f513c-265">Para obter informações sobre como dividir um conjunto de cópias de sombra, consulte [quebrando cópias de sombra](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="f513c-265">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

> [!Note]  
> <span data-ttu-id="f513c-266">A opção de linha de comando **-Bex** tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-266">The **-bex** command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="f513c-267">**vshadow** **-Bex** **-Mask**</span><span class="sxs-lookup"><span data-stu-id="f513c-267">**vshadow** **-bex** **-mask**</span></span>

<span data-ttu-id="f513c-268">O sinalizador **-Mask** especifica que o LUN de cópia de sombra será mascarado do host.</span><span class="sxs-lookup"><span data-stu-id="f513c-268">The **-mask** flag specifies that the shadow copy LUN will be masked from the host.</span></span> <span data-ttu-id="f513c-269">Se o sinalizador **-Mask** for especificado, os sinalizadores **-RW**, **-forcerevert** e **-norevert** não poderão ser especificados.</span><span class="sxs-lookup"><span data-stu-id="f513c-269">If the **-mask** flag is specified, the **-rw**, **-forcerevert**, and **-norevert** flags cannot be specified.</span></span>

<span data-ttu-id="f513c-270">**vshadow** **-Bex** **-RW**</span><span class="sxs-lookup"><span data-stu-id="f513c-270">**vshadow** **-bex** **-rw**</span></span>

<span data-ttu-id="f513c-271">O sinalizador **-RW** especifica que o LUN de cópia de sombra será exposto ao host como um volume de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f513c-271">The **-rw** flag specifies that the shadow copy LUN will be exposed to the host as a read/write volume.</span></span>

<span data-ttu-id="f513c-272">**vshadow** **-Bex** **-forcerevert**</span><span class="sxs-lookup"><span data-stu-id="f513c-272">**vshadow** **-bex** **-forcerevert**</span></span>

<span data-ttu-id="f513c-273">O sinalizador **-forcerevert** especifica que os identificadores de disco de todos os LUNs de cópia de sombra serão revertidos para os LUNs originais.</span><span class="sxs-lookup"><span data-stu-id="f513c-273">The **-forcerevert** flag specifies that the disk identifiers of all of the shadow copy LUNs will be reverted to that of the original LUNs.</span></span> <span data-ttu-id="f513c-274">No entanto, se qualquer um dos LUNs originais estiver presente no sistema, a operação falhará e nenhum dos identificadores será revertido.</span><span class="sxs-lookup"><span data-stu-id="f513c-274">However, if any of the original LUNs are present on the system, the operation will fail and none of the identifiers will be reverted.</span></span> <span data-ttu-id="f513c-275">Esse sinalizador e o sinalizador **-norevert** são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f513c-275">This flag and the **-norevert** flag are mutually exclusive.</span></span>

<span data-ttu-id="f513c-276">**vshadow** **-Bex** **-norevert**</span><span class="sxs-lookup"><span data-stu-id="f513c-276">**vshadow** **-bex** **-norevert**</span></span>

<span data-ttu-id="f513c-277">O sinalizador **-norevert** especifica que nenhum dos identificadores de disco do LUN de cópia de sombra será revertido.</span><span class="sxs-lookup"><span data-stu-id="f513c-277">The **-norevert** flag specifies that none of the shadow copy LUN disk identifiers will be reverted.</span></span> <span data-ttu-id="f513c-278">Esse sinalizador e o sinalizador **-forcerevert** são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f513c-278">This flag and the **-forcerevert** flag are mutually exclusive.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="f513c-279">Expondo uma cópia de sombra localmente</span><span class="sxs-lookup"><span data-stu-id="f513c-279">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="f513c-280">**vshadow** **-El =**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span><span class="sxs-lookup"><span data-stu-id="f513c-280">**vshadow** **-el=**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span></span>

 <span data-ttu-id="f513c-281">**vshadow** **-El =**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span><span class="sxs-lookup"><span data-stu-id="f513c-281">**vshadow** **-el=**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span></span>

<span data-ttu-id="f513c-282">A opção de linha de comando **-El** atribui uma pasta montada ou uma letra da unidade a uma cópia de sombra persistente.</span><span class="sxs-lookup"><span data-stu-id="f513c-282">The **-el** command-line option assigns a mounted folder or a drive letter to a persistent shadow copy.</span></span> <span data-ttu-id="f513c-283">Observe que o conteúdo do volume permanecerá somente leitura, a menos que você chame subseqüentemente o **vshadow** **-BW** para interromper o conjunto de cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="f513c-283">Note that the volume contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="f513c-284">As cópias de sombra não persistentes e as [*cópias de sombra acessíveis ao cliente*](vssgloss-c.md) não podem ser expostas localmente.</span><span class="sxs-lookup"><span data-stu-id="f513c-284">Nonpersistent shadow copies and [*client-accessible shadow copies*](vssgloss-c.md) cannot be exposed locally.</span></span>

 

<span data-ttu-id="f513c-285">Por exemplo, se {edbed95e-7e8d-11D8-9d01-505054503030} for o GUID de uma cópia de sombra persistente existente e X: for uma letra de unidade não usada, o comando a seguir expõe a cópia de sombra em X:</span><span class="sxs-lookup"><span data-stu-id="f513c-285">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and X: is an unused drive letter, the following command exposes the shadow copy under X:</span></span>

<span data-ttu-id="f513c-286">**vshadow** **-El = {edbed95e-7e8d-11D8-9d01-505054503030}, x:**</span><span class="sxs-lookup"><span data-stu-id="f513c-286">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},x:**</span></span>

<span data-ttu-id="f513c-287">O exemplo a seguir mostra como expor a mesma cópia de sombra na pasta montada C: \\ ShadowCopies \\ June23:</span><span class="sxs-lookup"><span data-stu-id="f513c-287">The following example shows how to expose the same shadow copy under the mounted folder C:\\ShadowCopies\\June23:</span></span>

<span data-ttu-id="f513c-288">**mkdir c: \\ ShadowCopies \\ June23**</span><span class="sxs-lookup"><span data-stu-id="f513c-288">**mkdir c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="f513c-289">**vshadow** **-El = {edbed95e-7e8d-11D8-9d01-505054503030}, c: \\ ShadowCopies \\ June23**</span><span class="sxs-lookup"><span data-stu-id="f513c-289">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="f513c-290">A opção de linha de comando **-El** não pode ser combinada com outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f513c-290">The **-el** command-line option cannot be combined with other command-line options.</span></span>

## <a name="exposing-a-shadow-copy-remotely"></a><span data-ttu-id="f513c-291">Expondo uma cópia de sombra remotamente</span><span class="sxs-lookup"><span data-stu-id="f513c-291">Exposing a Shadow Copy Remotely</span></span>

<span data-ttu-id="f513c-292">**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_</span><span class="sxs-lookup"><span data-stu-id="f513c-292">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_</span></span>

 <span data-ttu-id="f513c-293">**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span><span class="sxs-lookup"><span data-stu-id="f513c-293">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span></span>

<span data-ttu-id="f513c-294">A opção de linha de comando **-er** atribui um nome de compartilhamento somente leitura ao diretório raiz (ou um subdiretório) da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="f513c-294">The **-er** command-line option assigns a read-only share name to the root directory (or a subdirectory) from the shadow copy.</span></span> <span data-ttu-id="f513c-295">Observe que o conteúdo do compartilhamento permanecerá somente leitura, a menos que você chame subseqüentemente o **vshadow** **-BW** para interromper o conjunto de cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="f513c-295">Note that the share contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="f513c-296">As [*cópias de sombra acessíveis ao cliente*](vssgloss-c.md) não podem ser expostas remotamente.</span><span class="sxs-lookup"><span data-stu-id="f513c-296">[*Client-accessible shadow copies*](vssgloss-c.md) cannot be exposed remotely.</span></span>

 

<span data-ttu-id="f513c-297">Por exemplo, se {edbed95e-7e8d-11D8-9d01-505054503030} for o GUID de uma cópia de sombra persistente existente e o compartilhamento \_ 123 for um nome de compartilhamento não usado, o comando a seguir exporá a cópia de sombra em compartilhamento \_ 123:</span><span class="sxs-lookup"><span data-stu-id="f513c-297">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and share\_123 is an unused share name, the following command exposes the shadow copy under share\_123:</span></span>

<span data-ttu-id="f513c-298">**vshadow** **-er = {edbed95e-7e8d-11D8-9d01-505054503030}, compartilhamento \_ 123**</span><span class="sxs-lookup"><span data-stu-id="f513c-298">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123**</span></span>

<span data-ttu-id="f513c-299">O exemplo a seguir mostra como expor apenas uma subárvore (denominada "Pasta1 \\ Pasta2") da mesma cópia de sombra no mesmo compartilhamento:</span><span class="sxs-lookup"><span data-stu-id="f513c-299">The following example shows how to expose only a subtree (named "Folder1\\Folder2") of the same shadow copy under the same share:</span></span>

<span data-ttu-id="f513c-300">**vshadow** **-er = {edbed95e-7e8d-11D8-9d01-505054503030}, compartilhamento \_ 123, Pasta1 \\ Pasta2**</span><span class="sxs-lookup"><span data-stu-id="f513c-300">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123,Folder1\\Folder2**</span></span>

<span data-ttu-id="f513c-301">A opção de linha de comando **-er** não pode ser combinada com outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f513c-301">The **-er** command-line option cannot be combined with other command-line options.</span></span>

## <a name="listing-writer-status-and-metadata"></a><span data-ttu-id="f513c-302">Listando os metadados e o status do gravador</span><span class="sxs-lookup"><span data-stu-id="f513c-302">Listing Writer Status and Metadata</span></span>

<span data-ttu-id="f513c-303">**vshadow** **-WS**</span><span class="sxs-lookup"><span data-stu-id="f513c-303">**vshadow** **-ws**</span></span>

<span data-ttu-id="f513c-304">**vshadow** **-WM**</span><span class="sxs-lookup"><span data-stu-id="f513c-304">**vshadow** **-wm**</span></span>

<span data-ttu-id="f513c-305">**vshadow** **-wm2**</span><span class="sxs-lookup"><span data-stu-id="f513c-305">**vshadow** **-wm2**</span></span>

<span data-ttu-id="f513c-306">**vshadow** **-WM3**</span><span class="sxs-lookup"><span data-stu-id="f513c-306">**vshadow** **-wm3**</span></span>

<span data-ttu-id="f513c-307">A opção de linha de comando **-WS** enumera os gravadores VSS que estão sendo executados no computador e descreve seu estado.</span><span class="sxs-lookup"><span data-stu-id="f513c-307">The **-ws** command-line option enumerates the VSS writers that are currently running on the computer and describes their state.</span></span> <span data-ttu-id="f513c-308">Esse comando é equivalente ao comando [VSSadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="f513c-308">This command is the equivalent of the [Vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) command.</span></span> <span data-ttu-id="f513c-309">Há seis possíveis valores de Estado: estável, com falha, desconhecido, aguardando congelamento, congelado e aguardando a conclusão.</span><span class="sxs-lookup"><span data-stu-id="f513c-309">There are six possible state values: Stable, Failed, Unknown, Waiting for freeze, Frozen, and Waiting for completion.</span></span>

<span data-ttu-id="f513c-310">A opção de linha de comando **-WM** lista um resumo dos metadados do gravador, incluindo os volumes afetados.</span><span class="sxs-lookup"><span data-stu-id="f513c-310">The **-wm** command-line option lists a summary of the writer metadata, including the affected volumes.</span></span>

<span data-ttu-id="f513c-311">A opção de linha de comando **-wm2** lista todos os metadados do gravador.</span><span class="sxs-lookup"><span data-stu-id="f513c-311">The **-wm2** command-line option lists all writer metadata.</span></span>

<span data-ttu-id="f513c-312">A opção de linha de comando **-WM3** lista todos os metadados do gravador no formato XML bruto.</span><span class="sxs-lookup"><span data-stu-id="f513c-312">The **-wm3** command-line option lists all writer metadata in raw XML format.</span></span>

<span data-ttu-id="f513c-313">**Windows Vista e Windows Server 2003:** Não há suporte para a opção de linha de comando **-WM3** .</span><span class="sxs-lookup"><span data-stu-id="f513c-313">**Windows Vista and Windows Server 2003:** The **-wm3** command-line option is not supported.</span></span>

<span data-ttu-id="f513c-314">Você pode usar essas informações para determinar quais volumes incluir no conjunto de cópias de sombra de volume.</span><span class="sxs-lookup"><span data-stu-id="f513c-314">You can use this information to determine which volumes to include in the volume shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="f513c-315">Se o estado do gravador for estável ou aguardando a conclusão, o gravador poderá ser considerado em um estado estável, pronto para o próximo backup.</span><span class="sxs-lookup"><span data-stu-id="f513c-315">If the writer state is Stable or Waiting for completion, the writer can be considered to be in a stable state, ready for the next backup.</span></span>

 

<span data-ttu-id="f513c-316">As opções de linha de comando **-WS**, **-WM**, **-wm2** e **-WM3** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f513c-316">The **-ws**, **-wm**, **-wm2**, and **-wm3** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="performing-restore-operations"></a><span data-ttu-id="f513c-317">Executando operações de restauração</span><span class="sxs-lookup"><span data-stu-id="f513c-317">Performing Restore Operations</span></span>

<span data-ttu-id="f513c-318">**vshadow** \[ OptionalFlags \] **-r =**_File_*_. xml_*</span><span class="sxs-lookup"><span data-stu-id="f513c-318">**vshadow** \[OptionalFlags\] **-r=**_File_*_.xml_*</span></span>

<span data-ttu-id="f513c-319">**vshadow** \[ OptionalFlags \] **-RS =**_File_*_. xml_*</span><span class="sxs-lookup"><span data-stu-id="f513c-319">**vshadow** \[OptionalFlags\] **-rs=**_File_*_.xml_*</span></span>

<span data-ttu-id="f513c-320">A opção de linha de comando **-r** executa uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="f513c-320">The **-r** command-line option performs a restore operation.</span></span>

<span data-ttu-id="f513c-321">A opção de linha de comando **-RS** executa uma operação de restauração simulada.</span><span class="sxs-lookup"><span data-stu-id="f513c-321">The **-rs** command-line option performs a simulated restore operation.</span></span>

<span data-ttu-id="f513c-322">O arquivo de *File.xml* deve ser um arquivo de documento de componentes de backup para um conjunto de cópias de sombra que foi criado com o sinalizador opcional **-t** ou **-BC** .</span><span class="sxs-lookup"><span data-stu-id="f513c-322">The *File.xml* file must be a Backup Components Document file for a shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="f513c-323">As opções de linha de comando **-r** e **-RS** são mutuamente exclusivas e não podem ser combinadas com outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f513c-323">The **-r** and **-rs** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

<span data-ttu-id="f513c-324">*OptionalFlags* é um bitmask de valores de sinalizador opcionais da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f513c-324">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="f513c-325">Valor de sinalizador opcional</span><span class="sxs-lookup"><span data-stu-id="f513c-325">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="f513c-326">Descrição</span><span class="sxs-lookup"><span data-stu-id="f513c-326">Description</span></span>                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f513c-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_gravador_</span><span class="sxs-lookup"><span data-stu-id="f513c-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi=**_Writer_</span></span><br/>             | <span data-ttu-id="f513c-328">Esse sinalizador opcional verifica se o gravador ou o componente especificado está incluído na restauração.</span><span class="sxs-lookup"><span data-stu-id="f513c-328">This optional flag verifies that the specified writer or component is included in the restore.</span></span> <span data-ttu-id="f513c-329">O *gravador* pode especificar um caminho de componente, o nome do gravador, a ID do gravador ou a ID da instância do gravador.</span><span class="sxs-lookup"><span data-stu-id="f513c-329">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                    |
| <span data-ttu-id="f513c-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_gravador_</span><span class="sxs-lookup"><span data-stu-id="f513c-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx=**_Writer_</span></span><br/>             | <span data-ttu-id="f513c-331">Esse sinalizador opcional verifica se o gravador ou o componente especificado foi excluído da restauração.</span><span class="sxs-lookup"><span data-stu-id="f513c-331">This optional flag verifies that the specified writer or component is excluded from the restore.</span></span> <span data-ttu-id="f513c-332">O *gravador* pode especificar um caminho de componente, o nome do gravador, a ID do gravador ou a ID da instância do gravador.</span><span class="sxs-lookup"><span data-stu-id="f513c-332">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="f513c-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_comando_</span><span class="sxs-lookup"><span data-stu-id="f513c-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="f513c-334">Esse sinalizador opcional executa um comando ou script entre os eventos de pré e pós-restauração que são enviados aos gravadores.</span><span class="sxs-lookup"><span data-stu-id="f513c-334">This optional flag executes a command or script between the pre-restore and post-restore events that are sent to the writers.</span></span> <span data-ttu-id="f513c-335">O *comando* pode especificar um comando shell executável ou um arquivo cmd.</span><span class="sxs-lookup"><span data-stu-id="f513c-335">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="f513c-336">Se ele especificar um comando do Shell, nenhum parâmetro de comando poderá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="f513c-336">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="f513c-337"><span id="-tracing"></span><span id="-TRACING"></span>**-rastreamento**</span><span class="sxs-lookup"><span data-stu-id="f513c-337"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="f513c-338">Esse sinalizador opcional gera uma saída detalhada que pode ser usada para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="f513c-338">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a><span data-ttu-id="f513c-339">Revertendo para uma cópia de sombra anterior</span><span class="sxs-lookup"><span data-stu-id="f513c-339">Reverting to a Previous Shadow Copy</span></span>

<span data-ttu-id="f513c-340">**vshadow** **-REVERT =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="f513c-340">**vshadow** **-revert=**_ShadowCopyId_</span></span>

> [!Note]  
> <span data-ttu-id="f513c-341">Essa opção de linha de comando tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-341">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="f513c-342">**Windows server 2008 e Windows server 2003:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f513c-342">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="f513c-343">A opção **-reverter** linha de comando reverte um volume para a cópia de sombra anterior cuja ID é especificada por *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="f513c-343">The **-revert** command-line option reverts a volume to the previous shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="f513c-344">A opção de linha de comando **-REVERT** não pode ser combinada com outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f513c-344">The **-revert** command-line option cannot be combined with other command-line options.</span></span>

## <a name="resynchronizing-luns"></a><span data-ttu-id="f513c-345">Ressincronizando LUNs</span><span class="sxs-lookup"><span data-stu-id="f513c-345">Resynchronizing LUNs</span></span>

<span data-ttu-id="f513c-346">**vshadow** **-addresync =**_ShadowCopyId_ **-Ressync =**_BCDFileName_ \[ OptionalResyncFlags\]</span><span class="sxs-lookup"><span data-stu-id="f513c-346">**vshadow** **-addresync=**_ShadowCopyId_ **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="f513c-347">**vshadow** **-addresync =**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-Ressync =**_BCDFileName_ \[ OptionalResyncFlags\]</span><span class="sxs-lookup"><span data-stu-id="f513c-347">**vshadow** **-addresync=**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="f513c-348">A opção de linha de comando **-addresync** especifica os volumes a serem incluídos em uma operação de ressincronização de LUN.</span><span class="sxs-lookup"><span data-stu-id="f513c-348">The **-addresync** command-line option specifies the volumes to be included in a LUN resynchronization operation.</span></span> <span data-ttu-id="f513c-349">O parâmetro *ShadowCopyId* especifica o identificador da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="f513c-349">The *ShadowCopyId* parameter specifies the identifier of the shadow copy.</span></span> <span data-ttu-id="f513c-350">O parâmetro opcional *TargetVolumeDriveLetter* especifica o volume de destino onde o conteúdo do volume da cópia de sombra deve ser copiado.</span><span class="sxs-lookup"><span data-stu-id="f513c-350">The optional *TargetVolumeDriveLetter* parameter specifies the destination volume where the contents of the shadow copy volume are to be copied.</span></span>

<span data-ttu-id="f513c-351">A opção de linha de comando **-Ressync** inicia uma operação de ressincronização de LUN.</span><span class="sxs-lookup"><span data-stu-id="f513c-351">The **-resync** command-line option initiates a LUN resynchronization operation.</span></span> <span data-ttu-id="f513c-352">Depois que a operação for concluída, a assinatura de cada LUN de destino deverá ser idêntica à do LUN de volume de destino.</span><span class="sxs-lookup"><span data-stu-id="f513c-352">After the operation is complete, the signature of each target LUN should be identical to that of the target volume LUN.</span></span> <span data-ttu-id="f513c-353">O parâmetro *BCDFileName* especifica o nome do arquivo XML que contém o documento do componente de backup.</span><span class="sxs-lookup"><span data-stu-id="f513c-353">The *BCDFileName* parameter specifies the name of the XML file that contains the Backup Component Document.</span></span>

> [!Note]  
> <span data-ttu-id="f513c-354">As opções de linha de comando **-addresync** e **-Ressync** só têm suporte em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-354">The **-addresync** and **-resync** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="f513c-355">**Windows server 2008 e Windows server 2003:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f513c-355">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="f513c-356">*OptionalResyncFlags* é um bitmask de valores de sinalizador opcionais da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f513c-356">*OptionalResyncFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f513c-357">Valor de sinalizador opcional</span><span class="sxs-lookup"><span data-stu-id="f513c-357">Optional flag value</span></span></th>
<th><span data-ttu-id="f513c-358">Descrição</span><span class="sxs-lookup"><span data-stu-id="f513c-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f513c-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-360">Esse sinalizador opcional especifica que, após a conclusão da operação, a assinatura de cada LUN de destino deve ser idêntica à do LUN original que foi usado para criar a cópia de sombra, não o LUN de volume de destino.</span><span class="sxs-lookup"><span data-stu-id="f513c-360">This optional flag specifies that after the operation is complete, the signature of each target LUN should be identical to that of the original LUN that was used to create the shadow copy, not the target volume LUN.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-361">O sinalizador <strong>-revertsig</strong> tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-361">The <strong>-revertsig</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="f513c-362"><strong>Windows server 2008 e Windows server 2003:</strong> Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f513c-362"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f513c-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span><span class="sxs-lookup"><span data-stu-id="f513c-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span></span><br/></td>
<td><span data-ttu-id="f513c-364">Esse sinalizador opcional especifica que o serviço VSS não deve verificar se há volumes não selecionados que seriam substituídos pela operação de ressincronização de LUN.</span><span class="sxs-lookup"><span data-stu-id="f513c-364">This optional flag specifies that the VSS service should not check for unselected volumes that would be overwritten by the LUN resynchronization operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f513c-365">O sinalizador <strong>-novolcheck</strong> tem suporte apenas em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f513c-365">The <strong>-novolcheck</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="f513c-366"><strong>Windows server 2008 e Windows server 2003:</strong> Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f513c-366"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 

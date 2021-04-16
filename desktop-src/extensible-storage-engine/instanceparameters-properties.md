---
description: 'Saiba mais sobre: Propriedades Instanceparameters'
title: Propriedades de instanceparameters
TOCTitle: InstanceParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55103291
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0ac2b8aa959b8fa07f06e2de86dcfc173bab15ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556758"
---
# <a name="instanceparameters-properties"></a><span data-ttu-id="bb1b7-103">Propriedades de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="bb1b7-103">InstanceParameters properties</span></span>

<span data-ttu-id="bb1b7-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="bb1b7-104">Include protected members</span></span>  
<span data-ttu-id="bb1b7-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="bb1b7-105">Include inherited members</span></span>  

<span data-ttu-id="bb1b7-106">O tipo [instanceparameters](./instanceparameters-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-106">The [InstanceParameters](./instanceparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="bb1b7-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bb1b7-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bb1b7-108">Nome</span><span class="sxs-lookup"><span data-stu-id="bb1b7-108">Name</span></span></th>
<th><span data-ttu-id="bb1b7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb1b7-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span></span></td>
<td><span data-ttu-id="bb1b7-112">Obtém ou define o caminho relativo ou absoluto do sistema de arquivos de uma pasta na qual a recuperação de falha ou uma operação de restauração pode encontrar os bancos de dados referenciados no log de transações na pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-112">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span></span></td>
<td><span data-ttu-id="bb1b7-115">Obtém ou define o prefixo de três letras usado para muitos dos arquivos usados pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-115">Gets or sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="bb1b7-116">Por exemplo, o arquivo de ponto de verificação é chamado de EDB. CHK por padrão, porque o EDB é o nome de base padrão.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-116">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="bb1b7-119">Obtém ou define um valor que concede o número de recursos de árvore B em cache pela instância depois que as tabelas que eles representam foram fechadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-119">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="bb1b7-120">Valores grandes para esse parâmetro farão com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com que um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-120">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="bb1b7-121">Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-121">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="bb1b7-122">Com suporte no Windows Vista e em cima.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-122">Supported on Windows Vista and up.</span></span> <span data-ttu-id="bb1b7-123">Ignorado no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-123">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span></span></td>
<td><span data-ttu-id="bb1b7-126">Obtém ou define a propriedade por instância para prioridades de cache relativas (padrão = 100).</span><span class="sxs-lookup"><span data-stu-id="bb1b7-126">Gets or sets the per-instance property for relative cache priorities (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span></span></td>
<td><span data-ttu-id="bb1b7-129">Obtém ou define o limite em bytes para o número de arquivos de log de transações que precisarão ser reproduzidos após uma falha.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-129">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="bb1b7-130">Se o log circular estiver habilitado usando CircularLog, esse parâmetro também controlará a quantidade aproximada de arquivos de log de transações que serão retidos no disco.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-130">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span></span></td>
<td><span data-ttu-id="bb1b7-133">Obtém ou define um valor que indica se o log circular está ativado.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-133">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="bb1b7-134">Quando o log circular está desativado, todos os arquivos de log de transações gerados são mantidos no disco até que não sejam mais necessários porque um backup completo do banco de dados foi executado.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-134">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="bb1b7-135">Quando o log circular está ativado, somente os arquivos de log de transações mais jovens do que o ponto de verificação atual são mantidos no disco.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-135">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="bb1b7-136">O benefício desse modo é que os backups não são necessários para desativar arquivos de log de transação antigos.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-136">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span></span></td>
<td><span data-ttu-id="bb1b7-139">Obtém ou define um valor que indica se JetInit falha quando o mecanismo de banco de dados é configurado para começar a usar arquivos de log de transações em um disco que tenha um tamanho diferente do que está configurado.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-139">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="bb1b7-140">Normalmente, <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> recuperará com êxito os bancos de dados, mas falhará com <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> para indicar que o tamanho do arquivo de log está configurado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-140">Normally, <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> will successfully recover the databases but will fail with <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="bb1b7-141">No entanto, quando esse parâmetro for definido como true, o mecanismo de banco de dados excluirá silenciosamente todos os arquivos de log antigos, iniciará um novo conjunto de arquivos de log de transações usando o tamanho do arquivo de log configurado.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-141">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="bb1b7-142">Esse parâmetro é útil quando o aplicativo deseja alterar de forma transparente o tamanho do arquivo de log de transações e ainda funcionar de forma transparente nos cenários de atualização e restauração.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-142">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span></span></td>
<td><span data-ttu-id="bb1b7-145">Obtém ou define um valor que indica se o ESENT criará silenciosamente pastas que estão ausentes em seus caminhos do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-145">Gets or sets a value indicating whether ESENT will silently create folders that are missing in its filesystem paths.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span></span></td>
<td><span data-ttu-id="bb1b7-148">Obtém ou define o número de páginas que são adicionadas a um arquivo de banco de dados cada vez que ele precisa aumentar para acomodar mais informações.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-148">Gets or sets the number of pages that are added to a database file each time it needs to grow to accommodate more data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span></span></td>
<td><span data-ttu-id="bb1b7-151">Obtém ou define o intervalo máximo para que a verificação do banco de dados seja concluída, em segundos.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-151">Gets or sets the maximum interval to allow the database scan to finish, in seconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span></span></td>
<td><span data-ttu-id="bb1b7-154">Obtém ou define o intervalo mínimo para repetir a verificação do banco de dados, em segundos.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-154">Gets or sets the minimum interval to repeat the database scan, in seconds.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span></span></td>
<td><span data-ttu-id="bb1b7-157">Obtém ou define a limitação da verificação do banco de dados, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-157">Gets or sets the throttling of the database scan, in milliseconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span></span></td>
<td><span data-ttu-id="bb1b7-160">Obtém ou define um valor que indica se a manutenção do banco de dados deve ser executada durante a recuperação.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-160">Gets or sets a value indicating whether Database Maintenance should run during recovery.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span></span></td>
<td><span data-ttu-id="bb1b7-163">Obtém ou define um valor que indica se a serialização de manutenção do banco de dados está habilitada para bancos de dados que compartilham o mesmo disco.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-163">Gets or sets a value indicating whether database Maintenance serialization is enabled for databases sharing the same disk.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span></span></td>
<td><span data-ttu-id="bb1b7-166">Obtém ou define um valor que indica se <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> verificará se há índices que foram compilados usando uma versão mais antiga da biblioteca NLS no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-166">Gets or sets a value indicating whether <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> will check for indexes that were build using an older version of the NLS library in the operating system.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span></span></td>
<td><span data-ttu-id="bb1b7-169">Obtém ou define um valor que indica se a desfragmentação online está habilitada.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-169">Gets or sets a value indicating whether online defragmentation is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span></span></td>
<td><span data-ttu-id="bb1b7-172">Obtém ou define uma cadeia de caracteres específica do aplicativo que será adicionada a qualquer mensagem de log de eventos emitida pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-172">Gets or sets an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="bb1b7-173">Isso permite uma fácil correlação de mensagens de log de eventos com o aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-173">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="bb1b7-174">Por padrão, o nome executável do aplicativo host será usado.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-174">By default the host application executable name will be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span></span></td>
<td><span data-ttu-id="bb1b7-177">Obtém ou define o nome do log de eventos que o mecanismo de banco de dados usa para suas mensagens de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-177">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="bb1b7-178">Por padrão, todas as mensagens de log de eventos vão para o log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-178">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="bb1b7-179">Se o nome da chave do registro para outro log de eventos estiver configurado, as mensagens do log de eventos entrarão em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-179">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span></span></td>
<td><span data-ttu-id="bb1b7-182">Obtém ou define a quantidade de memória usada para armazenar em cache os registros de log antes que eles sejam gravados no arquivo de log de transações.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-182">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="bb1b7-183">A unidade para esse parâmetro é o tamanho do setor do volume que contém os arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-183">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="bb1b7-184">O tamanho do setor quase sempre é de 512 bytes, portanto, é seguro assumir esse tamanho para a unidade.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-184">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="bb1b7-185">Esse parâmetro tem um impacto no desempenho.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-185">This parameter has an impact on performance.</span></span> <span data-ttu-id="bb1b7-186">Quando o mecanismo de banco de dados está sob carga de atualização pesada, esse buffer pode se tornar completo com muita rapidez.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-186">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="bb1b7-187">Um tamanho de cache maior para o arquivo de log de transações é essencial para um bom desempenho de atualização sob uma condição de alta carga.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-187">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="bb1b7-188">O padrão é conhecido como muito pequeno para esse caso.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-188">The default is known to be too small for this case.</span></span> <span data-ttu-id="bb1b7-189">Não defina esse parâmetro como um número de buffers que seja maior (em bytes) que metade do tamanho de um arquivo de log de transações.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-189">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-191"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-191"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span></span></td>
<td><span data-ttu-id="bb1b7-192">Obtém ou define o caminho relativo ou absoluto do sistema de arquivos da pasta que conterá os logs de transação para a instância.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-192">Gets or sets the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span></span></td>
<td><span data-ttu-id="bb1b7-195">Obtém ou define o tamanho dos arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-195">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="bb1b7-196">Esse parâmetro deve ser definido em unidades de 1024 bytes (por exemplo, uma configuração de 2048 fornecerá arquivos de log de 2 MB).</span><span class="sxs-lookup"><span data-stu-id="bb1b7-196">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span></span></td>
<td><span data-ttu-id="bb1b7-199">Obtém ou define o número de recursos de cursor reservados para esta instância.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-199">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="bb1b7-200">Um recurso de cursor corresponde diretamente a um JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-200">A cursor resource directly corresponds to a JET_TABLEID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span></span></td>
<td><span data-ttu-id="bb1b7-203">Obtém ou define o número de recursos da árvore B + reservados para esta instância.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-203">Gets or sets the number of B+ Tree resources reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span></span></td>
<td><span data-ttu-id="bb1b7-206">Obtém ou define o número de recursos de sessões reservados para esta instância.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-206">Gets or sets the number of sessions resources reserved for this instance.</span></span> <span data-ttu-id="bb1b7-207">Um recurso de sessão corresponde diretamente a um JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-207">A session resource directly corresponds to a JET_SESID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span></span></td>
<td><span data-ttu-id="bb1b7-210">Obtém ou define o número de recursos de tabela temporária para uso por uma instância.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-210">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="bb1b7-211">Essa configuração afetará quantas tabelas temporárias podem ser usadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-211">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="bb1b7-212">Se esse parâmetro de sistema for definido como zero, nenhum banco de dados temporário será criado e qualquer atividade que exija o uso do banco de dados temporário falhará.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-212">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="bb1b7-213">Essa configuração pode ser útil para evitar a e/s necessária para criar o banco de dados temporário se for conhecido que ele não será usado.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-213">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span></span></td>
<td><span data-ttu-id="bb1b7-216">Obtém ou define o percentual do repositório de versão que pode ser usado pela transação mais antiga antes de <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (padrão = 100).</span><span class="sxs-lookup"><span data-stu-id="bb1b7-216">Gets or sets the percentage of version store that can be used by oldest transaction before <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span></span></td>
<td><span data-ttu-id="bb1b7-219">Obtém ou define o número máximo de páginas de repositório de versão reservadas para esta instância.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-219">Gets or sets the maximum number of version store pages reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span></span></td>
<td><span data-ttu-id="bb1b7-222">Obtém ou define um valor que indica se as mensagens de log de eventos informativas que normalmente seriam geradas pelo mecanismo de banco de dados serão suprimidas.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-222">Gets or sets a value indicating whether informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span></span></td>
<td><span data-ttu-id="bb1b7-225">Obtém ou define um valor que indica se apenas um banco de dados pode ser aberto usando JetOpenDatabase por uma determinada sessão ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-225">Gets or sets a value indicating whether only one database is allowed to be opened using JetOpenDatabase by a given session at one time.</span></span> <span data-ttu-id="bb1b7-226">O banco de dados temporário é excluído dessa restrição.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-226">The temporary database is excluded from this restriction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span></span></td>
<td><span data-ttu-id="bb1b7-229">Obtém ou define o tamanho inicial do banco de dados temporário.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-229">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="bb1b7-230">O tamanho está em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-230">The size is in database pages.</span></span> <span data-ttu-id="bb1b7-231">Um tamanho de zero indica que o tamanho padrão de um banco de dados comum deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-231">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="bb1b7-232">Geralmente, é desejável que aplicativos pequenos configurem o banco de dados temporário para que seja o menor possível.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-232">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="bb1b7-233">Definir esse parâmetro como <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> atingirá o menor banco de dados temporário possível.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-233">Setting this parameter to <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> will achieve the smallest temporary database possible.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span></span></td>
<td><span data-ttu-id="bb1b7-236">Obtém ou define o número preferencial de páginas de repositório de versão reservadas para esta instância.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-236">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="bb1b7-237">Se o tamanho do repositório de versão exceder esse limite, todas as informações usadas apenas para tarefas em segundo plano opcionais, como a recuperação de espaço excluído no banco de dados, serão sacrificadas para preservar espaço para informações transacionais.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-237">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span></span></td>
<td><span data-ttu-id="bb1b7-240">Obtém ou define o número máximo de operações de e/s expedidas para uma determinada finalidade.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-240">Gets or sets the maximum number of I/O operations dispatched for a given purpose.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-242"><a href="dn350981(v=exchg.10).md">Recuperação</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-242"><a href="dn350981(v=exchg.10).md">Recovery</a></span></span></td>
<td><span data-ttu-id="bb1b7-243">Obtém ou define um valor que indica se a recuperação de Pane está ativada.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-243">Gets or sets a value indicating whether crash recovery is on.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span></span></td>
<td><span data-ttu-id="bb1b7-246">Obtém ou define o caminho relativo ou absoluto do sistema de arquivos da pasta que conterá o arquivo de ponto de verificação para a instância.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-246">Gets or sets the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span></span></td>
<td><span data-ttu-id="bb1b7-249">Obtém ou define o caminho relativo ou absoluto do sistema de arquivos da pasta que conterá o banco de dados temporário da instância.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-249">Gets or sets the relative or absolute file system path of the folder that will contain the temporary database for the instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span></span></td>
<td><span data-ttu-id="bb1b7-252">Obtém ou define o número de itens de trabalho de limpeza em segundo plano que podem ser enfileirados no pool de threads do mecanismo de banco de dados a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-252">Gets or sets the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><span data-ttu-id="bb1b7-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span><span class="sxs-lookup"><span data-stu-id="bb1b7-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span></span></td>
<td><span data-ttu-id="bb1b7-255">Obtém ou define um número de logs para os quais o ESENT adiará as liberações de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-255">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="bb1b7-256">Isso pode ser usado para aumentar a capacidade de recuperação do banco de dados se as falhas causarem a perda de arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-256">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="bb1b7-257">Com suporte no Windows 7 e em cima.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-257">Supported on Windows 7 and up.</span></span> <span data-ttu-id="bb1b7-258">Ignorado no Windows XP, no Windows Server 2003, no Windows Vista e no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="bb1b7-258">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bb1b7-259">Parte superior</span><span class="sxs-lookup"><span data-stu-id="bb1b7-259">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="bb1b7-260">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb1b7-260">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bb1b7-261">Referência</span><span class="sxs-lookup"><span data-stu-id="bb1b7-261">Reference</span></span>

[<span data-ttu-id="bb1b7-262">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="bb1b7-262">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="bb1b7-263">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bb1b7-263">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

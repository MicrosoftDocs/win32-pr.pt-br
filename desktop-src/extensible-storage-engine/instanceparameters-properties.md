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
# <a name="instanceparameters-properties"></a>Propriedades de instanceparameters

Incluir membros protegidos  
Incluir membros herdados  

O tipo [instanceparameters](./instanceparameters-class.md) expõe os membros a seguir.

## <a name="properties"></a>Propriedades

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></td>
<td>Obtém ou define o caminho relativo ou absoluto do sistema de arquivos de uma pasta na qual a recuperação de falha ou uma operação de restauração pode encontrar os bancos de dados referenciados no log de transações na pasta especificada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350972(v=exchg.10).md">BaseName</a></td>
<td>Obtém ou define o prefixo de três letras usado para muitos dos arquivos usados pelo mecanismo de banco de dados. Por exemplo, o arquivo de ponto de verificação é chamado de EDB. CHK por padrão, porque o EDB é o nome de base padrão.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></td>
<td>Obtém ou define um valor que concede o número de recursos de árvore B em cache pela instância depois que as tabelas que eles representam foram fechadas pelo aplicativo. Valores grandes para esse parâmetro farão com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com que um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo. Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas. Com suporte no Windows Vista e em cima. Ignorado no Windows XP e no Windows Server 2003.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350974(v=exchg.10).md">CachePriority</a></td>
<td>Obtém ou define a propriedade por instância para prioridades de cache relativas (padrão = 100).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></td>
<td>Obtém ou define o limite em bytes para o número de arquivos de log de transações que precisarão ser reproduzidos após uma falha. Se o log circular estiver habilitado usando CircularLog, esse parâmetro também controlará a quantidade aproximada de arquivos de log de transações que serão retidos no disco.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350977(v=exchg.10).md">CircularLog</a></td>
<td>Obtém ou define um valor que indica se o log circular está ativado. Quando o log circular está desativado, todos os arquivos de log de transações gerados são mantidos no disco até que não sejam mais necessários porque um backup completo do banco de dados foi executado. Quando o log circular está ativado, somente os arquivos de log de transações mais jovens do que o ponto de verificação atual são mantidos no disco. O benefício desse modo é que os backups não são necessários para desativar arquivos de log de transação antigos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></td>
<td>Obtém ou define um valor que indica se JetInit falha quando o mecanismo de banco de dados é configurado para começar a usar arquivos de log de transações em um disco que tenha um tamanho diferente do que está configurado. Normalmente, <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> recuperará com êxito os bancos de dados, mas falhará com <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> para indicar que o tamanho do arquivo de log está configurado incorretamente. No entanto, quando esse parâmetro for definido como true, o mecanismo de banco de dados excluirá silenciosamente todos os arquivos de log antigos, iniciará um novo conjunto de arquivos de log de transações usando o tamanho do arquivo de log configurado. Esse parâmetro é útil quando o aplicativo deseja alterar de forma transparente o tamanho do arquivo de log de transações e ainda funcionar de forma transparente nos cenários de atualização e restauração.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></td>
<td>Obtém ou define um valor que indica se o ESENT criará silenciosamente pastas que estão ausentes em seus caminhos do sistema de arquivos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></td>
<td>Obtém ou define o número de páginas que são adicionadas a um arquivo de banco de dados cada vez que ele precisa aumentar para acomodar mais informações.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></td>
<td>Obtém ou define o intervalo máximo para que a verificação do banco de dados seja concluída, em segundos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></td>
<td>Obtém ou define o intervalo mínimo para repetir a verificação do banco de dados, em segundos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></td>
<td>Obtém ou define a limitação da verificação do banco de dados, em milissegundos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></td>
<td>Obtém ou define um valor que indica se a manutenção do banco de dados deve ser executada durante a recuperação.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></td>
<td>Obtém ou define um valor que indica se a serialização de manutenção do banco de dados está habilitada para bancos de dados que compartilham o mesmo disco.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></td>
<td>Obtém ou define um valor que indica se <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> verificará se há índices que foram compilados usando uma versão mais antiga da biblioteca NLS no sistema operacional.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></td>
<td>Obtém ou define um valor que indica se a desfragmentação online está habilitada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350988(v=exchg.10).md">EventSource</a></td>
<td>Obtém ou define uma cadeia de caracteres específica do aplicativo que será adicionada a qualquer mensagem de log de eventos emitida pelo mecanismo de banco de dados. Isso permite uma fácil correlação de mensagens de log de eventos com o aplicativo de origem. Por padrão, o nome executável do aplicativo host será usado.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350966(v=exchg.10).md">EventSourceKey</a></td>
<td>Obtém ou define o nome do log de eventos que o mecanismo de banco de dados usa para suas mensagens de log de eventos. Por padrão, todas as mensagens de log de eventos vão para o log de eventos do aplicativo. Se o nome da chave do registro para outro log de eventos estiver configurado, as mensagens do log de eventos entrarão em seu lugar.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350968(v=exchg.10).md">LogBuffers</a></td>
<td>Obtém ou define a quantidade de memória usada para armazenar em cache os registros de log antes que eles sejam gravados no arquivo de log de transações. A unidade para esse parâmetro é o tamanho do setor do volume que contém os arquivos de log de transações. O tamanho do setor quase sempre é de 512 bytes, portanto, é seguro assumir esse tamanho para a unidade. Esse parâmetro tem um impacto no desempenho. Quando o mecanismo de banco de dados está sob carga de atualização pesada, esse buffer pode se tornar completo com muita rapidez. Um tamanho de cache maior para o arquivo de log de transações é essencial para um bom desempenho de atualização sob uma condição de alta carga. O padrão é conhecido como muito pequeno para esse caso. Não defina esse parâmetro como um número de buffers que seja maior (em bytes) que metade do tamanho de um arquivo de log de transações.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></td>
<td>Obtém ou define o caminho relativo ou absoluto do sistema de arquivos da pasta que conterá os logs de transação para a instância.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350969(v=exchg.10).md">LogFileSize</a></td>
<td>Obtém ou define o tamanho dos arquivos de log de transações. Esse parâmetro deve ser definido em unidades de 1024 bytes (por exemplo, uma configuração de 2048 fornecerá arquivos de log de 2 MB).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350993(v=exchg.10).md">MaxCursors</a></td>
<td>Obtém ou define o número de recursos de cursor reservados para esta instância. Um recurso de cursor corresponde diretamente a um JET_TABLEID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></td>
<td>Obtém ou define o número de recursos da árvore B + reservados para esta instância.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350994(v=exchg.10).md">MaxSessions</a></td>
<td>Obtém ou define o número de recursos de sessões reservados para esta instância. Um recurso de sessão corresponde diretamente a um JET_SESID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></td>
<td>Obtém ou define o número de recursos de tabela temporária para uso por uma instância. Essa configuração afetará quantas tabelas temporárias podem ser usadas ao mesmo tempo. Se esse parâmetro de sistema for definido como zero, nenhum banco de dados temporário será criado e qualquer atividade que exija o uso do banco de dados temporário falhará. Essa configuração pode ser útil para evitar a e/s necessária para criar o banco de dados temporário se for conhecido que ele não será usado.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></td>
<td>Obtém ou define o percentual do repositório de versão que pode ser usado pela transação mais antiga antes de <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (padrão = 100).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350975(v=exchg.10).md">MaxVerPages</a></td>
<td>Obtém ou define o número máximo de páginas de repositório de versão reservadas para esta instância.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></td>
<td>Obtém ou define um valor que indica se as mensagens de log de eventos informativas que normalmente seriam geradas pelo mecanismo de banco de dados serão suprimidas.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></td>
<td>Obtém ou define um valor que indica se apenas um banco de dados pode ser aberto usando JetOpenDatabase por uma determinada sessão ao mesmo tempo. O banco de dados temporário é excluído dessa restrição.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></td>
<td>Obtém ou define o tamanho inicial do banco de dados temporário. O tamanho está em páginas de banco de dados. Um tamanho de zero indica que o tamanho padrão de um banco de dados comum deve ser usado. Geralmente, é desejável que aplicativos pequenos configurem o banco de dados temporário para que seja o menor possível. Definir esse parâmetro como <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> atingirá o menor banco de dados temporário possível.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></td>
<td>Obtém ou define o número preferencial de páginas de repositório de versão reservadas para esta instância. Se o tamanho do repositório de versão exceder esse limite, todas as informações usadas apenas para tarefas em segundo plano opcionais, como a recuperação de espaço excluído no banco de dados, serão sacrificadas para preservar espaço para informações transacionais.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></td>
<td>Obtém ou define o número máximo de operações de e/s expedidas para uma determinada finalidade.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350981(v=exchg.10).md">Recuperação</a></td>
<td>Obtém ou define um valor que indica se a recuperação de Pane está ativada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351007(v=exchg.10).md">SystemDirectory</a></td>
<td>Obtém ou define o caminho relativo ou absoluto do sistema de arquivos da pasta que conterá o arquivo de ponto de verificação para a instância.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350983(v=exchg.10).md">TempDirectory</a></td>
<td>Obtém ou define o caminho relativo ou absoluto do sistema de arquivos da pasta que conterá o banco de dados temporário da instância.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></td>
<td>Obtém ou define o número de itens de trabalho de limpeza em segundo plano que podem ser enfileirados no pool de threads do mecanismo de banco de dados a qualquer momento.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn350985(v=exchg.10).md">WaypointLatency</a></td>
<td>Obtém ou define um número de logs para os quais o ESENT adiará as liberações de banco de dados. Isso pode ser usado para aumentar a capacidade de recuperação do banco de dados se as falhas causarem a perda de arquivos de log. Com suporte no Windows 7 e em cima. Ignorado no Windows XP, no Windows Server 2003, no Windows Vista e no Windows Server 2008.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe instanceparameters](./instanceparameters-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

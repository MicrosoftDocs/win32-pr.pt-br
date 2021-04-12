---
description: 'Saiba mais sobre: função JetReadFile'
title: Função JetReadFile
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170539"
---
# <a name="jetreadfile-function"></a>Função JetReadFile


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetreadfile-function"></a>Função JetReadFile

A função **JetReadFile** recupera o conteúdo de um arquivo aberto com [JetOpenFile](./jetopenfile-function.md).

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parâmetros

*hfFile*

O identificador do arquivo a ser lido.

*PV*

Buffer de saída que receberá os dados do arquivo.

*CB*

O tamanho máximo em bytes do buffer de saída.

*pcbActual*

Recebe a quantidade real de dados de arquivo recuperados.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <strong>JetReadFile</strong> quando:</p>
<ul>
<li><p>O identificador de instância especificado é inválido. Windows XP e versões posteriores.</p></li>
<li><p>O tamanho do buffer de saída não é um múltiplo do tamanho da página do banco de dados (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP e versões posteriores.</p></li>
<li><p>O tamanho do buffer de saída é menor do que três páginas de banco de dados (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) e essa é a primeira chamada para <strong>JetReadFile</strong> para o identificador especificado. Windows XP e versões posteriores.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>A operação falhou porque nenhum backup externo está em andamento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>A operação falhou porque a corrupção de dados não recuperável foi detectada durante a leitura de uma página de banco de dado de um arquivo de banco de dados ou arquivo de patch de banco</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>A operação falhou porque a corrupção de dados não recuperável foi detectada durante a leitura de um arquivo de log de transações. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, a próxima parte dos dados do arquivo será lida no buffer de saída. O número real de bytes recuperados também será retornado. O deslocamento do arquivo no qual a próxima leitura ocorrerá será avançado por esse valor.

Em caso de falha, o estado do buffer de saída é indefinido. A falha resultará no cancelamento de todo o processo de backup da instância. No Windows XP e versões posteriores, o backup não será cancelado se ocorrer um erro durante a leitura de um arquivo de banco de dados. No entanto, o backup desse arquivo de banco de dados ainda será cancelado e o identificador correspondente será fechado automaticamente.

#### <a name="remarks"></a>Comentários

Qualquer chamada para **JetReadFile** usando um identificador que já tenha retornado todos os dados no arquivo subjacente (como uma chamada anterior retornou menos bytes do que o tamanho do buffer de saída) sempre terá sucesso, mas retornará zero bytes de dados.

Um buffer de saída grande deve ser usado para maximizar o desempenho do backup. Pode ser necessário algum experimento para encontrar a compensação certa entre o consumo de recursos e a taxa de transferência para uma determinada situação. O buffer de saída não deve ser menor que 64 KB em nenhum caso.

Várias chamadas simultâneas para **JetReadFile** usando o mesmo identificador de arquivo não são suportadas. Isso significa que não é possível enfileirar vários buffers para leitura simultânea no mesmo arquivo para obter uma alta taxa de transferência sequencial. Um único buffer grande deve ser usado em vez disso.

Se a instância estiver configurada de modo que a depuração de página do banco de dados esteja habilitada (Confira JET_paramZeroDatabaseDuringBackup em parâmetros do sistema), as páginas excluídas serão removidas do banco de dado como um efeito colateral de uma chamada para **JetReadFile** no arquivo de banco de dados.

É muito importante entender como o backup e a corrupção de dados interagem. Caso o mecanismo de banco de dados detecte corrupção de dado durante um backup, ele irá falhar o backup do banco de dados afetado ou da instância inteira. Essa é uma decisão de design consciente destinada a proteger contra perda de dados. Se o mecanismo de banco de dados permitisse um backup para ser bem sucedido onde dados corrompidos estavam presentes, é possível que um backup mais antigo e não corrompido possa ser descartado como resultado. Isso seria desnecessário porque seria possível corrigir os dados corrompidos na instância ao vivo restaurando esse backup e reproduzindo todos os arquivos de log de transações nesse banco de dados. Esse cenário de perda de dados zero pressupõe que o log circular não está habilitado (consulte [JET_paramCircularLog](./transaction-log-parameters.md) em [parâmetros do sistema](./extensible-storage-engine-system-parameters.md)).

Também é importante entender que, quando a corrupção de dados está presente, o backup de streaming será o local mais provável que será detectado primeiro. Esse é o caso porque o backup de streaming é o único processo que examina rotineiramente cada página única do arquivo de banco de dados. Também é provável que o backup de streaming seja o primeiro processo para detectar os antigos sinais de falha de hardware, como manifestado por erros intermitentes de corrupção de dados. Isso ocorre devido à quantidade de dados recuperados pelo backup, bem como à velocidade na qual ele é recuperado.

A corrupção de dados é detectada pelo mecanismo de banco de dados com o uso de somas de verificação de bloco. Essas somas de verificação são definidas imediatamente antes de uma gravação de página de banco de dados e são verificadas em uma página de banco de dados lida. Esse esquema permite que o mecanismo de banco de dados Determine que os dados foram corrompidos em algum momento, mas não habilita o mecanismo de banco de dados a determinar a origem desse dano. Historicamente, a causa mais predominante desse dano foi Obtida de fontes diferentes do mecanismo de banco de dados.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)

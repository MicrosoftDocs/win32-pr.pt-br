---
description: 'Saiba mais sobre: função JetReadFileInstance'
title: Função JetReadFileInstance
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501291"
---
# <a name="jetreadfileinstance-function"></a>Função JetReadFileInstance


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetreadfileinstance-function"></a>Função JetReadFileInstance

A função **JetReadFileInstance** recupera o conteúdo de um arquivo aberto com a função [JetOpenFileInstance](./jetopenfileinstance-function.md) .

**Windows XP**: o   **JetReadFileInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância a ser usada para uma chamada de API específica.

Observe que para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global é implícito nesse caso.

Para o Windows XP e versões posteriores, você pode chamar a variante de API que não aceita esse parâmetro somente quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000) nos casos em que há suporte para apenas uma instância. Caso contrário, a operação falhará e retornará o erro de JET_errRunningInMultiInstanceMode.

*hfFile*

O identificador do arquivo a ser lido.

*PV*

O buffer de saída que receberá os dados do arquivo.

*CB*

O tamanho máximo, em bytes, do buffer de saída.

*pcb*

A quantidade real de dados de arquivo recuperados.

### <a name="return-value"></a>Valor Retornado

Essa função facilita o retorno de quaisquer [JET_ERR](./jet-err.md) tipos de dados que são definidos na API do ESE (mecanismo de armazenamento extensível). Para obter mais informações sobre erros do JET, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>A operação falhou porque o backup externo atual foi anulado por uma chamada para a função <a href="gg269240(v=exchg.10).md">JetStopService</a> . Esse erro será retornado somente pelo Windows XP e por versões posteriores do Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para a função <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro será retornado somente pelo Windows XP e por versões posteriores do Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros especificados continha um valor inesperado ou um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para a função <strong>JetReadFileInstance</strong> quando ocorrer um dos seguintes:</p>
<ul>
<li><p>O identificador de instância especificado é inválido. Windows XP e versões posteriores do Windows.</p></li>
<li><p>O tamanho do buffer de saída não é um múltiplo do tamanho da página do banco de dados (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP e versões posteriores do Windows.</p></li>
<li><p>O tamanho do buffer de saída é menor do que três páginas de banco de dados (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), e essa é a primeira chamada para a função <strong>JetReadFileInstance</strong> para o identificador especificado. Windows XP e versões posteriores do Windows.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>A operação falhou porque o corrompimento de dados irrecuperáveis foi detectado durante a leitura de um arquivo de log de transações. Esse erro será retornado somente pelo Windows XP e por versões posteriores do Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>A operação falhou porque nenhum backup externo está em andamento.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada a esta sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>A operação falhou porque o corrompimento de dados irrecuperáveis foi detectado durante a leitura de uma página de banco de dado a partir de um arquivo de dados ou arquivo de patch de banco</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada a esta sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em um caso em que apenas uma instância tem suporte, mas várias instâncias já existem.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada a esta sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, a próxima parte dos dados do arquivo será lida no buffer de saída. O número real de bytes recuperados também será retornado. O deslocamento do arquivo no qual a próxima leitura ocorrerá será avançado por esse valor.

Em caso de falha, o estado do buffer de saída é indefinido. A falha resultará no cancelamento de todo o processo de backup para a instância atual. No Windows XP e versões posteriores do Windows, o backup não será cancelado se ocorrer um erro durante a leitura de um arquivo de banco de dados. No entanto, o backup desse arquivo de banco de dados ainda será cancelado e o identificador correspondente será fechado automaticamente.

#### <a name="remarks"></a>Comentários

Qualquer chamada para a função **JetReadFileInstance** feita usando um identificador que já retornou todos os dados no arquivo subjacente (por exemplo, se uma chamada anterior retornou menos bytes do que o tamanho do buffer de saída) sempre terá sucesso, mas retornará zero bytes de dados.

Você deve usar um buffer de saída grande para maximizar o desempenho do backup. Talvez seja necessário experimentar para encontrar a desvantagem ideal entre o consumo de recursos e a taxa de transferência para uma situação específica. Em qualquer caso, o buffer de saída não deve ser menor que 64 KB. O ponteiro que você passa para **JetReadFileInstance** deve ser alinhado com um limite de página de memória (4 KB ou 8 KB). Você pode fazer isso chamando a função do **VirtualAlloc** .

Várias chamadas simultâneas para **JetReadFileInstance** feitas usando o mesmo identificador de arquivo não são suportadas. Isso significa que não é possível enfileirar vários buffers para leitura simultânea no mesmo arquivo para obter uma alta taxa de transferência sequencial. Em vez disso, você deve usar um único buffer grande.

Se você tiver configurado uma instância específica, de modo que a depuração de página do banco de dados esteja habilitada (consulte o parâmetro [JET_paramCircularLog](./transaction-log-parameters.md) em [parâmetros do sistema](./extensible-storage-engine-system-parameters.md)), os dados excluídos serão removidos do banco de dado como um efeito colateral de uma chamada para **JetReadFileInstance** no arquivo de banco de dados.

É muito importante entender como o backup e a corrupção de dados interagem. Se o mecanismo de banco de dados detectar corrupção de dado durante um backup, ele irá falhar o backup do banco de dados afetado ou da instância inteira. Essa é uma decisão de design consciente destinada a proteger contra perda de dados. Se o mecanismo de banco de dados permitisse um backup para ter êxito onde os dados estão corrompidos, é possível que um backup mais antigo e não corrompido possa ser descartado como resultado. Isso seria desnecessário, pois seria possível corrigir os dados corrompidos na instância dinâmica restaurando esse backup e reproduzindo todos os arquivos de log de transações nesse banco de dados. Esse cenário de perda de dados sem zero pressupõe que o log circular não está habilitado (consulte [JET_paramCircularLog](./transaction-log-parameters.md) em [parâmetros do sistema](./extensible-storage-engine-system-parameters.md)).

Também é importante entender que os casos de corrupção de dados geralmente são detectados primeiro durante o backup de streaming. Isso ocorre porque o backup de streaming é o único processo que examina rotineiramente cada página única do arquivo de banco de dados. Também é provável que o backup de streaming seja o primeiro processo para detectar os antigos sinais de falha de hardware, como manifestado por erros intermitentes de corrupção de dados, devido à quantidade de dados recuperados pelo backup e à velocidade em que esses dados são recuperados.

A corrupção de dados é detectada pelo mecanismo de banco de dados com o uso de somas de verificação de bloco. Essas somas de verificação são definidas imediatamente antes da gravação de uma página de banco de dados e são verificados em uma página de banco de dados lida. Esse esquema permite que o mecanismo de banco de dados Determine que os dados foram corrompidos em algum momento, mas não habilita o mecanismo de banco de dados para determinar a origem desse dano. Historicamente, as instâncias desse tipo de corrupção de dados se originaram de fontes diferentes do mecanismo de banco de dados em si.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Cliente</p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>Servidor</p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>parâmetro</p></td>
<td><p>É declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p>Biblioteca</p></td>
<td><p>Usa ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)

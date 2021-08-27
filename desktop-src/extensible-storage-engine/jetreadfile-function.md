---
description: 'Saiba mais sobre: Função JetReadFile'
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
ms.openlocfilehash: b7f089e87fad910232bae85e14f1d6d2ab6e00b0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470273"
---
# <a name="jetreadfile-function"></a>Função JetReadFile


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetreadfile-function"></a>Função JetReadFile

A **função JetReadFile** recupera o conteúdo de um arquivo aberto com [JetOpenFile](./jetopenfile-function.md).

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

O alça do arquivo a ser lido.

*Pv*

Buffer de saída que receberá os dados do arquivo.

*Cb*

O tamanho máximo em bytes do buffer de saída.

*pcbActual*

Recebe a quantidade real de dados de arquivo recuperados.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <strong>JetReadFile</strong> quando:</p><ul><li><p>O handle de instância especificado é inválido. Windows XP e versões posteriores.</p></li><li><p>O tamanho do buffer de saída não é um múltiplo do tamanho da página do banco de dados (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP e versões posteriores.</p></li><li><p>O tamanho do buffer de saída é menor que três páginas de banco de dados ( JET_paramDatabasePageSize ) e essa é<a href="gg269337(v=exchg.10).md">a</a>primeira chamada para <strong>JetReadFile</strong> para o handle especificado. Windows XP e versões posteriores.</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errReadVerifyFailure</p> | <p>A operação falhou porque dados não recuperáveis foram detectados durante a leitura de uma página de banco de dados de um arquivo de banco de dados ou arquivo de patch de banco de dados.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>A operação falhou porque dados não recuperáveis foram detectados durante a leitura de um arquivo de log de transações. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade Windows 2000), em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de êxito, a próxima parte dos dados do arquivo será lida no buffer de saída. O número real de bytes recuperados também será retornado. O deslocamento de arquivo no qual a próxima leitura ocorrerá será avançado por esse valor.

Em caso de falha, o estado do buffer de saída é indefinido. A falha resultará no cancelamento de todo o processo de backup para a instância. No Windows XP e versões posteriores, o backup não será cancelado se ocorrer um erro durante a leitura de um arquivo de banco de dados. No entanto, o backup desse arquivo de banco de dados ainda será cancelado e o handle correspondente será fechado automaticamente.

#### <a name="remarks"></a>Comentários

Qualquer chamada para **JetReadFile** usando um alça que já retornou todos os dados no arquivo subjacente (como uma chamada anterior retornou menos bytes do que o tamanho do buffer de saída) sempre terá êxito, mas retornará zero bytes de dados.

Um buffer de saída grande deve ser usado para maximizar o desempenho do backup. Algumas experimentações podem ser necessárias para encontrar a troca certa entre o consumo de recursos e a produtividade para uma determinada situação. O buffer de saída não deve ser menor que 64KB em qualquer caso.

Não há suporte para várias **chamadas simultâneas para JetReadFile** usando o mesmo alça de arquivo. Isso significa que não é possível enfilerar vários buffers para leitura simultaneamente no mesmo arquivo para obter alta taxa de transferência sequencial. Um único buffer grande deve ser usado em vez disso.

Se a instância estiver configurada de modo que a depuração de página do banco de dados seja habilitada (consulte JET_paramZeroDatabaseDuringBackup em Parâmetros do Sistema), os dados excluídos serão removidos do banco de dados como um efeito colateral de uma chamada para **JetReadFile** no arquivo de banco de dados.

É muito importante entender como o backup e a corrupção de dados interagem. Se o mecanismo de banco de dados detectar dados corrupções durante um backup, ele falhará no backup do banco de dados afetado ou de toda a instância. Essa é uma decisão de design inteligente destinada a proteger contra perda de dados. Se o mecanismo de banco de dados permitiu que um backup fosse bem-sucedido em que dados estavam presentes, é possível que um backup mais antigo e incorrupto possa ser descartado como resultado. Isso seria uma pena porque seria possível corrigir a corrupção de dados na instância ativa restaurando esse backup e repetir todos os arquivos de log de transações nesse banco de dados. Esse cenário de perda de dados zero presume que o log circular não está habilitado [(consulte JET_paramCircularLog](./transaction-log-parameters.md) em [Parâmetros do Sistema](./extensible-storage-engine-system-parameters.md)).

Também é importante entender que quando o backup de streaming de dados estiver presente será o local mais provável em que ele será detectado pela primeira vez. Esse é o caso porque o backup de streaming é o único processo que examina rotineiramente todas as páginas do arquivo de banco de dados. Também é provável que o backup de streaming seja o primeiro processo para detectar os primeiros sinais de falha de hardware, conforme manifestado por erros intermitentes de corrupção de dados. Isso ocorre devido à quantidade de dados recuperados pelo backup, bem como à velocidade na qual eles são recuperados.

A corrupção de dados é detectada pelo mecanismo de banco de dados por meio do uso de verificações de bloco. Essas verificações são definidas logo antes de uma gravação de página de banco de dados e verificadas em uma página de banco de dados lida. Esse esquema permite que o mecanismo de banco de dados determine que os dados foram corrompidos em algum momento, mas não permite que o mecanismo de banco de dados determine a origem dessa corrupção. Historicamente, a causa predominante dessa corrupção foi encontrada em fontes diferentes do mecanismo de banco de dados em si.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)

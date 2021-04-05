---
description: 'Saiba mais sobre: função JetExternalRestore2'
title: Função JetExternalRestore2
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922178"
---
# <a name="jetexternalrestore2-function"></a>Função JetExternalRestore2


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetexternalrestore2-function"></a>Função JetExternalRestore2

A função **JetExternalRestore2** restaura um backup externo que foi feito com as APIs de backup externo e fornece pontos de verificação a serem usados para operações de log circulares. Isso é conhecido como recuperação complexa, que é semelhante, mas diferente da recuperação simples, conforme executado pela função [JetInit](./jetinit-function.md) .

**Windows XP: o JetExternalRestore2** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parâmetros

*szCheckpointFilePath*

O caminho para o arquivo de ponto de verificação a ser usado durante a recuperação se *szTargetInstanceCheckpointPath* não for especificado ou se o caminho tiver uma instância ativa ou em execução.

*szLogPath*

O caminho ou diretório para os logs da fase final (desfazer) da recuperação e, possivelmente, para os logs de roll-forward. Esse caminho pode ser o mesmo que o *szBackupLogPath*.

*rgrstmap*

Esta é uma matriz de estruturas de [JET_RSTMAP](./jet-rstmap-structure.md) . Este é um mapa de caminhos de banco de dados novos e antigos ou nomes de File. Isso é usado porque os bancos de dados podem precisar ser recuperados para um local diferente do local do qual foram feitos backup. No caso em que vários bancos de dados são anexados a um único conjunto de registros, o mapa de restauração pode especificar um subconjunto dos bancos de dados a serem restaurados.

*crstfilemap*

O número de entradas no parâmetro de matriz *rgrstmap* .

*szBackupLogPath*

O caminho para o diretório em que os arquivos de log são restaurados. Esses são os logs que foram lidos durante a sequência de backup externo. Esse caminho pode ser o mesmo que o *szLogPath*.

*pLogInfo*

O *pLogInfo* descreve vários aspectos dos logs de backup para recuperação, esse parâmetro permite que o **JetExternalRestore2** assuma os parâmetros explícitos de *GenLow* e *genHigh* que o **JetExternalRestore2** tem, bem como o nome do log base, em vez de um nome de base de log presumido de "edb".

*szTargetInstanceName*

Este parâmetro foi preterido e não pode ser usado em seu aplicativo.

*szTargetInstanceLogPath*

O caminho para os logs de roll-forward se o local dos logs que você deseja rolar para frente estiver em um conjunto de logs ou instância ativa. Isso não deve ser especificado se a instância de destino estiver usando log circular.

*szTargetInstanceCheckpointPath*

O caminho para o ponto de verificação durante a recuperação se não houver nenhuma instância ativa em execução nesse destino. Isso não deve ser especificado se a instância de destino estiver usando log circular.

*PFN*

O retorno de chamada de status, que relata o progresso da recuperação.

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
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>O <em>szTargetInstanceLogPath</em> especificado não pertence a uma instância inicializada. Esse erro só será retornado no Windows XP e posterior.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Isso indica que o banco de dados foi corrompido ou um arquivo não reconhecido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Esse erro será retornado se um dos arquivos de log no <em>szBackupLogPath</em>tiver uma geração de log acima especificada em <em>genHigh</em> ou <em>pLogInfo. ulGenHigh</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>A operação falhou porque não pôde abrir o arquivo solicitado porque ele não foi encontrado no caminho especificado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, e assim por diante, quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> não forem especificados ou não forem ambos não especificados. Ou seja, eles devem corresponder e ser especificados ou ambos não especificados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>A operação falhou porque o caminho especificado não foi encontrado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Esse erro será retornado se o arquivo de banco de dados especificado durante a restauração não for um banco de dados cujo backup foi feito com backup externo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>O mecanismo de banco de dados não pode executar restauração externa ou recuperação de hardware no modo de instância única. Esse erro só será retornado no Windows XP e posterior.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Esse erro será retornado se um dos arquivos de log no <em>szBackupLogPath</em>tiver uma geração de log abaixo especificada pelo <em>genLow</em> ou <em>pLogInfo. ulGenLow</em>.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, todos os bancos de dados do *rgrstmap* são completamente recuperados e em um estado limpo ou consistente. Neste ponto, o banco de dados pode ser remontado em uma instância existente.

Em caso de falha, o mecanismo não pôde recuperar o banco de dados. O banco de dados está em um estado inválido e, para tentar a recuperação complexa, todo o banco de dados deve ser restaurado novamente. Normalmente, a origem de tal situação é a corrupção de disco ou log, ou alguma outra forma de gerenciamento de ingestão de log ou um conjunto de logs não contínuo.

#### <a name="remarks"></a>Comentários

Consulte [JetExternalRestore](./jetexternalrestore-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetExternalRestore2W</strong> (Unicode) e <strong>JetExternalRestore2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)

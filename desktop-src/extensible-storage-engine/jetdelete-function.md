---
description: 'Saiba mais sobre: função JetDelete'
title: Função JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752328"
---
# <a name="jetdelete-function"></a>Função JetDelete


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetdelete-function"></a>Função JetDelete

A função **JetDelete** exclui o registro atual em uma tabela de banco de dados.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão de banco de dados que será usado para a chamada à API.

*TableID*

O cursor em uma tabela de banco de dados. A linha atual será excluída.

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
<td><p>JET_errCallbackFailed</p></td>
<td><p>A função de retorno de chamada falhou de alguma maneira. Por exemplo, violações de acesso em funções de retorno de chamada são capturadas e convertidas em JET_errCallbackFailed. Esse erro só será retornado pelo Windows XP e posterior.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation</p></td>
<td><p>O cursor especificado por <em>TableName</em> não oferece suporte à exclusão. Consulte a seção Comentários.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor especificado por <em>TableName</em> não está em um registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPermissionDenied</p></td>
<td><p>O mecanismo de banco de dados não tem permissões suficientes para excluir o registro. Isso pode acontecer se o arquivo de banco de dados foi aberto com acesso somente leitura.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackError</p></td>
<td><p>Um buffer de atualização (consulte <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) existe, mas nem todas as alterações feitas em colunas do tipo JET_coltypLongText e/ou colunas do tipo JET_coltypLongBinary podem ser revertidas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>É ilegal usar a mesma sessão de mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>A transação é uma transação somente leitura e não oferece suporte a exclusões.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>A operação falhou porque não há memória suficiente para reter informações transacionais sobre a atualização.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Outra sessão bloqueou anteriormente o registro para atualização. A atualização tentada por esta sessão falhará.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, a moeda é deixada logo antes do próximo registro. Se o registro excluído foi o último na tabela, a moeda é deixada no final da tabela (ou seja, após o novo último registro). Se o registro excluído for o único registro na tabela, a moeda será definida como o início.

Os índices apropriados são atualizados automaticamente.

Se uma atualização estiver preparada (usando [JetPrepareUpdate](./jetprepareupdate-function.md)), ela será cancelada. O buffer de atualização será redefinido.

Em caso de falha, a moeda permanece inalterada. Se uma atualização estiver preparada (consulte [JetPrepareUpdate](./jetprepareupdate-function.md)), o buffer de atualização poderá ser redefinido.

#### <a name="remarks"></a>Comentários

Nem todas as tabelas dão suporte à exclusão de linhas. Normalmente, uma tabela temporária não dá suporte à exclusão de linhas. A exclusão de registros pode ser habilitada em tabelas temporárias por vários motivos, algumas das quais são:

  - JET_bitTTUpdatable foi especificado durante a criação.

  - Tabelas temporárias grandes podem dar suporte à exclusão se elas foram criadas com JET_bitTTScrollable ou JET_bitTTIndexed. O limite no qual uma tabela temporária se torna "grande" atualmente é de 64 quilobytes, mas pode ser alterado em versões futuras.

Windows XP e posterior. As funções de retorno de chamada podem ser invocadas por **JetDelete**, incluindo JET_cbtypBeforeDelete e JET_cbtypAfterDelete.

É importante entender o impacto da execução de um grande número de operações de atualização dentro de uma única transação. Cada atualização do banco de dados deve ser controlada pelo mecanismo de banco de dados no repositório de versão. O repositório de versão mantém um registro ao vivo de todas as diferentes versões de cada registro ou entrada de índice no banco de dados que pode ser visto por todas as transações ativas. Essas versões são usadas para dar suporte ao controle de simultaneidade de várias versões em uso pelo mecanismo de banco de dados para dar suporte a transações usando o isolamento de instantâneo. Depois que o mecanismo de banco de dados tiver esgotado os recursos usados para armazenar essas versões, ele não poderá mais aceitar outras alterações até que algumas transações tenham sido concluídas para permitir que esses recursos sejam recuperados. Quando o mecanismo estiver nesse estado, todas as atualizações falharão com JET_errVersionStoreOutOfMemory. Os recursos disponíveis para o mecanismo de banco de dados para armazenar essas versões podem ser controlados usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com *JET_paramMaxVerPages* e *JET_paramGlobalMinVerPages*.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)

---
description: 'Saiba mais sobre: função JetEscrowUpdate'
title: Função JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797982"
---
# <a name="jetescrowupdate-function"></a>Função JetEscrowUpdate


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetescrowupdate-function"></a>Função JetEscrowUpdate

A função **JetEscrowUpdate** executa uma operação de adição atômica em uma coluna. Essa função permite que várias sessões atualizem o mesmo registro simultaneamente sem conflitos.

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*columnid*

O *columnid* da coluna a ser atualizada.

*PV*

Um ponteiro para um buffer que contém o adendo para a coluna.

*cbMax*

O tamanho do buffer que contém o adendo.

*pvOld*

O buffer de saída que receberá o valor atual da coluna como armazenado no banco de dados (o controle de versão é ignorado).

*cbOldMax*

O tamanho máximo do buffer de saída que receberá o valor atual da coluna. Atualmente, apenas JET_coltypLong tem suporte, portanto, o buffer deve ter 4 bytes ou 0 bytes de comprimento. Se *pvOld* for NULL, *cbOldMax* deverá ser 0.

*pcbOldActual*

Recebe a quantidade real de dados de valor bruto recebidos no buffer de saída.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitEscrowNoRollback</p></td>
<td><p>Mesmo que a sessão que executa a atualização de caução tenha sua reversão de transação, essa atualização não será desfeita. Observe que, como os registros de log podem não ser liberados para o disco, as atualizações de caução recentes feitas com esse sinalizador poderão ser perdidas se houver uma falha.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errAlreadyPrepared</p></td>
<td><p>O cursor tem uma atualização preparada com <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</p></td>
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
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Um tamanho de buffer inválido foi passado. Atualmente, apenas JET_coltypLong tem suporte, portanto, o buffer deve ter 4 bytes.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOperation</p></td>
<td><p>Uma coluna inválida foi especificada. A coluna deve ser criada com JET_bitColumnEscrowUpdate especificado. Somente colunas fixas de JET_coltypLong podem ser especificadas como de caução atualizáveis.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor deve estar em um registro para atualizar uma coluna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>As atualizações de caução só podem ser executadas por sessões em uma transação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>O cursor não pode ser somente leitura e atualizar um registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada em mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>A sessão deve ter permissões de gravação para atualizar um registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>O erro retornado quando uma atualização conflitante é solicitada.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Normalmente, se duas sessões tentarem atualizar um registro simultaneamente, a segunda sessão receberá um erro de JET_errWriteConflict, a menos que as sessões sejam completamente serializadas. Para serializar duas sessões que atualizam o mesmo registro, a segunda sessão deve iniciar sua transação após a primeira transação confirmar sua transação. Consulte [JetBeginTransaction](./jetbegintransaction-function.md) para obter mais informações.

Várias colunas no mesmo registro podem ser atualizadas por caução. As atualizações não afetam uma à outra.

Somente as operações **JetEscrowUpdate** são compatíveis entre si. Se duas sessões diferentes tentarem preparar atualizações ou excluir o mesmo registro, um conflito de gravação será gerado.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p>Sessão B<br />
<strong>JetEscrowUpdate</strong></p></th>
<th><p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p></th>
<th><p><a href="gg269315(v=exchg.10).md">JetDelete</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>JetEscrowUpdate</strong></p></td>
<td><p>JET_errSuccess</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="odd">
<td><p>Sessão A</p></td>
<td><p><a href="gg269315(v=exchg.10).md">JetDelete</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
</tbody>
</table>


As operações de caução têm controle de versão e são desfeitas usando [JetRollback](./jetrollback-function.md) (a menos que JET_bitEscrowNoRollback tenha sido especificado). **JetEscrowUpdate** retorna o valor bruto da coluna armazenada no banco de dados, pois um aplicativo pode querer executar uma ação especial quando um valor de Sentinela é atingido. [JetRetrieveColumn](./jetretrievecolumn-function.md) retorna a exibição com controle de versão correta da coluna, ignorando as atualizações feitas por sessões simultâneas.

Dadas duas sessões operando na mesma coluna do mesmo registro, podemos ver como isso funciona. Suponha que a coluna comece com um valor de 0.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Session</p></th>
<th><p>Operação</p></th>
<th><p>Valor armazenado</p></th>
<th><p>Valor retornado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Um</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Um</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>Um</p></td>
<td><p><strong>JetEscrowUpdate</strong> (4)</p></td>
<td><p>4</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Um</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><strong>JetEscrowUpdate</strong> (3)</p></td>
<td><p>7</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p>A</p></td>
<td><p><strong>JetEscrowUpdate</strong> (2)</p></td>
<td><p>9</p></td>
<td><p>7</p></td>
</tr>
<tr class="even">
<td><p>Um</p></td>
<td><p><strong>JetEscrowUpdate</strong> (-7)</p></td>
<td><p>2</p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269273(v=exchg.10).md">JetRollback</a></p></td>
<td><p>-1</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Um</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
</tbody>
</table>


Não é recomendável substituir um registro na mesma transação que executa atualizações de caução em um registro. Em particular, se uma atualização em um registro estiver preparada com uma [JET_TABLEID](./jet-tableid.md) e uma [JET_TABLEID](./jet-tableid.md) diferente for usada para atualizar o registro, a caução atualizada será perdida quando [JetUpdate](./jetupdate-function.md) for chamado. Isso acontece mesmo que a coluna de caução não tenha sido definida durante a atualização.

Quando uma coluna atualizável de caução tem um valor igual a zero, o comportamento especial pode ser disparado. Esse comportamento ocorre apenas se uma operação **JetEscrowUpdate** faz com que a coluna tenha um valor igual a zero. A ação não acontece imediatamente, mas ocorre em algum momento após a transação que fez com que a coluna tenha um valor de zero confirmações. A coluna ainda deve ter um valor igual a zero (ou seja, se nenhuma outra sessão tiver modificado a coluna). Se a coluna tiver sido criada com JET_bitColumnDeleteOnZero, o registro que contém a coluna será excluído. Se a coluna tiver sido criada com JET_bitColumnFinalize, um retorno de chamada será emitido. Uma falha pode fazer com que essas ações não aconteçam, mas a manutenção online (usando a função [JetDefragment](./jetdefragment-function.md) ) fará com que as ações sejam refeitas corretamente.

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)

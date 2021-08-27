---
description: 'Saiba mais sobre: Função JetEscrowUpdate'
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
ms.openlocfilehash: e9f037b8c26829d7b1f3a10b05e1d4bd83bd186a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469793"
---
# <a name="jetescrowupdate-function"></a>Função JetEscrowUpdate


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetescrowupdate-function"></a>Função JetEscrowUpdate

A **função JetEscrowUpdate** executa uma operação de adição atômica em uma coluna. Essa função permite que várias sessões atualizem o mesmo registro simultaneamente sem conflitos.

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

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*Columnid*

A *columnid* da coluna a ser atualizada.

*Pv*

Um ponteiro para um buffer que contém o adendo da coluna.

*cbMax*

O tamanho do buffer que contém o adendo.

*pvOld*

O buffer de saída que receberá o valor atual da coluna conforme armazenado no banco de dados (o versioning é ignorado).

*cbOldMax*

O tamanho máximo do buffer de saída que receberá o valor atual da coluna. Atualmente, há JET_coltypLong suporte, portanto, o buffer deve ter 4 bytes ou 0 bytes de comprimento. Se *pvOld* for NULL, *cbOldMax* deverá ser 0.

*pcbOldActual*

Recebe a quantidade real de dados de valor bruto recebidos no buffer de saída.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitEscrowNoRollback</p> | <p>Mesmo que a sessão que executa a atualização de escrow tenha sua re reação de transação, essa atualização não será desfeita. Observe que, como os registros de log podem não ser liberados para o disco, atualizações recentes de escrow feitas com esse sinalizador podem ser perdidas se houver uma falha.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errAlreadyPrepared</p> | <p>O cursor tem uma atualização preparada com <a href="gg269339(v=exchg.10).md">JetPrepareUpdate.</a></p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Um tamanho de buffer inválido foi passado. Atualmente, há JET_coltypLong suporte, portanto, o buffer deve ter 4 bytes.</p> | 
| <p>JET_errInvalidOperation</p> | <p>Uma coluna inválida foi especificada. A coluna deve ser criada com JET_bitColumnEscrowUpdate especificado. Somente colunas fixas de JET_coltypLong podem ser especificadas como atualizáveis de escrow.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor deve estar em um registro para atualizar uma coluna.</p> | 
| <p>JET_errNotInTransaction</p> | <p>As atualizações de escrow só podem ser executadas por sessões em uma transação.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errPermissionDenied</p> | <p>O cursor não pode ser somente leitura e atualizar um registro.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada de mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errTransReadOnly</p> | <p>A sessão deve ter permissões de gravação para atualizar um registro.</p> | 
| <p>JET_errWriteConflict</p> | <p>O erro retornado quando uma atualização conflitante é solicitada.</p> | 



#### <a name="remarks"></a>Comentários

Normalmente, se duas sessões tentarem atualizar um registro simultaneamente, a segunda sessão receberá um erro de JET_errWriteConflict a menos que as sessões sejam completamente serializadas. Para serializar duas sessões que atualizam o mesmo registro, a segunda sessão deve iniciar sua transação depois que a primeira transação confirma sua transação. Consulte [JetBeginTransaction para](./jetbegintransaction-function.md) obter mais informações.

Várias colunas no mesmo registro podem ser atualizadas. As atualizações não afetam umas às outras.

Somente **as operações JetEscrowUpdate** são compatíveis entre si. Se duas sessões diferentes tentarem preparar atualizações ou excluirem o mesmo registro, um conflito de gravação será gerado.


| <p></p> | <p></p> | <p>Sessão B<br /><strong>JetEscrowUpdate</strong></p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | 
|---------|---------|--------------------------------------------------------|---------------------------------------------------------------|--------------------------------------------------------|
| <p></p> | <p><strong>JetEscrowUpdate</strong></p> | <p>JET_errSuccess</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p></p> | <p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p>Sessão A</p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 



As operações de escrow têm versão e são desfeitas usando [JetRollback](./jetrollback-function.md) (a menos que JET_bitEscrowNoRollback tenha sido especificado). **JetEscrowUpdate** retorna o valor bruto da coluna armazenada no banco de dados, pois um aplicativo pode querer executar uma ação especial quando um valor de sentinel é atingido. [JetRetrieveColumn](./jetretrievecolumn-function.md) retorna a exibição com versão correta da coluna, ignorando as atualizações feitas por sessões simultâneas.

Considerando duas sessões operando na mesma coluna do mesmo registro, podemos ver como isso funciona. Suponha que a coluna comece com um valor de 0.


| <p>Sessão</p> | <p>Operação</p> | <p>Valor armazenado</p> | <p>Valor retornado</p> | 
|----------------|------------------|---------------------|-----------------------|
| <p>A</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p></p> | 
| <p>A</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p>0</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (4)</p> | <p>4</p> | <p>0</p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p> | <p></p> | <p></p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>0</p> | 
| <p>B</p> | <p><strong>JetEscrowUpdate</strong> (3)</p> | <p>7</p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (2)</p> | <p>9</p> | <p>7</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (-7)</p> | <p>2</p> | <p>9</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 
| <p>B</p> | <p><a href="gg269273(v=exchg.10).md">JetRollback</a></p> | <p>-1</p> | <p></p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 



Não é recomendável substituir um registro na mesma transação que executa atualizações de escrow em um registro. Em particular, se uma atualização em [](./jet-tableid.md) um registro for preparada [](./jet-tableid.md) com um JET_TABLEID e um JET_TABLEID diferente for usado para escrow atualizar o registro, o crescimento atualizado será perdido quando [JetUpdate](./jetupdate-function.md) for chamado. Isso acontece mesmo se a coluna escrow não foi definida durante a atualização.

Quando uma coluna atualizável de escrow tem um valor de zero, um comportamento especial pode ser disparado. Esse comportamento só acontece se uma **operação JetEscrowUpdate** faz com que a coluna tenha um valor de zero. A ação não ocorre imediatamente, mas ocorre algum tempo após a transação que fez com que a coluna tenha um valor de zero confirmações. A coluna ainda deve ter um valor de zero (ou seja, se nenhuma outra sessão tiver modificado a coluna). Se a coluna tiver sido criada com JET_bitColumnDeleteOnZero, o registro que contém a coluna será excluído. Se a coluna tiver sido criada com JET_bitColumnFinalize, um retorno de chamada será emitido. Uma falha pode fazer com que essas ações não ocorram, mas a manutenção online (usando a [função JetDefragment)](./jetdefragment-function.md) refazerá corretamente as ações.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



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

---
description: 'Saiba mais sobre: função JetPrepareUpdate'
title: Função JetPrepareUpdate
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748666"
---
# <a name="jetprepareupdate-function"></a>Função JetPrepareUpdate


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetprepareupdate-function"></a>Função JetPrepareUpdate

A função **JetPrepareUpdate** é a primeira operação na execução de uma atualização, para a inserção de um novo registro ou a substituição de um registro existente por novos valores. As atualizações são feitas chamando **JetPrepareUpdate**, depois chamando [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) zero ou mais vezes e finalmente chamando [JetUpdate](./jetupdate-function.md) para concluir a operação. **JetPrepareUpdate** e [JetUpdate](./jetupdate-function.md) definem os limites para uma operação de atualização e são importantes para ter apenas o estado de atualização final de um registro inserido em índices. Isso é mais eficiente, mas também necessário nos casos em que os dados devem corresponder a um estado válido através de mais de uma operação de definição de coluna.

Há algumas opções diferentes para inserir ou substituir registros e eles são descritos mais detalhadamente abaixo.

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*Prep*

As opções que podem ser usadas para se preparar para uma atualização, que incluem o seguinte.

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
<td><p>JET_prepCancel</p></td>
<td><p>Esse sinalizador faz com que <strong>JetPrepareUpdate</strong> cancele a atualização para este cursor.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepInsert</p></td>
<td><p>Esse sinalizador faz com que o cursor se prepare para uma inserção de um novo registro. Todos os dados são inicializados para o estado padrão do registro. Se a tabela tiver uma coluna de incremento automático, um novo valor será atribuído a esse registro, independentemente de a atualização ter êxito ou não ser cancelada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_prepInsertCopy</p></td>
<td><p>Esse sinalizador faz com que o cursor se prepare para uma inserção de uma cópia do registro existente. Deve haver um registro atual se essa opção for usada. O estado inicial do novo registro é copiado do registro atual. Valores longos armazenados fora do registro são praticamente copiados.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepInsertCopyDeleteOriginal</p></td>
<td><p>Esse sinalizador faz com que o cursor se prepare para uma inserção do mesmo registro e um Delete ou o registro original. Ele é usado em casos em que a chave primária foi alterada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_prepReplace</p></td>
<td><p>Esse sinalizador faz com que o cursor se prepare para uma substituição do registro atual. Se a tabela tiver uma coluna de versão, a coluna versão será definida como o próximo valor em sua sequência. Se essa atualização não for concluída, o valor da versão no registro não será afetado. Um bloqueio de atualização é obtido no registro para impedir que outras sessões atualizem esse registro antes da conclusão desta sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepReplaceNoLock</p></td>
<td><p>Esse sinalizador é semelhante a JET_prepReplace, mas nenhum bloqueio é usado para impedir que outras sessões atualizem esse registro. Em vez disso, essa sessão pode receber JET_errWriteConflict quando chama <a href="gg269288(v=exchg.10).md">JetUpdate</a> para concluir a atualização.</p></td>
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
<td><p><strong>JetPrepareUpdate</strong> foi chamado com um sinalizador válido para Prep, mas não JET_prepCancel e o cursor já estava no estado preparado.</p></td>
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
<td><p>O sinalizador de preparação fornecido não é um sinalizador válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p><strong>JetPrepareUpdate</strong> foi chamado para substituir um registro que tinha colunas SLV. Colunas SLV. Observe que as colunas SLV são um recurso não destinado ao uso geral. Esse recurso é usado para dar suporte à infraestrutura do Microsoft Exchange e não se destina a ser usado em seu aplicativo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError</p></td>
<td><p><strong>JetPrepareUpdate</strong> foi chamado com JET_prepCancel, mas não pôde reverter todas as alterações feitas em colunas do tipo JET_coltypLongText e/ou colunas do tipo JET_coltypLongBinary.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Esse sinalizador não pode ser usado com a mesma sessão de mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p><strong>JetPrepareUpdate</strong> foi chamado com JET_prepCancel, mas o cursor não estava no estado preparado.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o cursor é alterado para o estado preparado para a finalidade da atualização desejada ou, no caso de JET_prepCancel, o cursor é revertido para o estado não preparado e todas as alterações são descartadas.

Em caso de falha, o estado do cursor permanece inalterado. Se a falha foi JET_errRollbackError, o estado do cursor será alterado para o estado não preparado, mas nem todas as alterações serão revertidas.

#### <a name="remarks"></a>Comentários

A inserção de uma cópia de um registro é uma otimização importante quando os registros compartilham dados do tipo JET_coltypLongText e/ou JET_coltypLongBinary. Esses dados são armazenados fora do registro quando for grande e é possível que vários registros compartilhem a mesma representação física dos dados. Nesse caso, os dados podem ser atualizados a partir de um dos registros, mas fazer isso fará com que os dados sejam intermitentes, de modo que cada registro tenha sua própria cópia. Não é possível alterar dados em um registro por uma modificação de outro registro. Além disso, não é possível bloquear uma atualização de um registro por uma atualização de outro registro. Esse é um recurso central para o ESE e é conhecido como bloqueio no nível de registro.

Operações [JetUpdate](./jetupdate-function.md) que falham deixam o cursor no estado pronto para atualização. Isso é para permitir a correção para alguns erros, como um valor de coluna errado, sem exigir que o estado de atualização seja recriado. Isso significa que, em todos os casos em que um cursor abandona uma atualização, ele deve chamar **JetPrepareUpdate** explicitamente com JET_prepCancel.

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
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)

---
description: 'Saiba mais sobre: função JetComputeStats'
title: Função JetComputeStats
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c6856a50ae2f1c01b1cfde0666d0c535ad37e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172078"
---
# <a name="jetcomputestats-function"></a>Função JetComputeStats


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetcomputestats-function"></a>Função JetComputeStats

A função **JetComputeStats** percorre cada índice de uma tabela para calcular exatamente o número de entradas em um índice e o número de chaves distintas em um índice. Essas informações, junto com o número de páginas de banco de dados alocadas para um índice e a hora atual da computação, são armazenadas em metadados de índice no banco de dados. Esses dados podem ser recuperados posteriormente com operações de informações.

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor que será usado para esta chamada. Descreve a tabela na qual as estatísticas são computadas.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p>Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackError</p></td>
<td><p>Erro ao exigir que esta operação reverta todas as alterações, mas a reversão da transação falhou.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p>Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Em caso de êxito, as estatísticas atualizadas são armazenadas nos catálogos de banco de dados para a tabela descrita com o cursor fornecido.

Em caso de falha, nenhuma atualização de nenhum tipo é feita no banco de dados.

#### <a name="remarks"></a>Comentários

Essa operação pode ser consumindo recursos, pois cada índice em uma tabela deve ser percorrido em sua totalidade. [JetGetRecordPosition](./jetgetrecordposition-function.md) pode ser usado para obter uma estimativa aproximada do número de entradas em um índice, mas não pode, por si só, estimar o número de valores distintos em um índice.

Os dados computados por essa operação começam a ficar desatualizados e a tabela é atualizada posteriormente.

As atualizações no banco de dados feita pelo **JetComputeStats** são feitas de maneira lenta. Isso significa que nenhuma liberação de log será acompanhada por essa operação e uma falha do sistema subsequente para um retorno de JET_errSuccess pelo **JetComputeStats** ainda poderá fazer com que essas atualizações sejam perdidas.

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
[JET_TABLEID](./jet-tableid.md)  
[JET_SESID](./jet-sesid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetStopService](./jetstopservice-function.md)

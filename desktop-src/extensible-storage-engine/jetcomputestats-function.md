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
ms.openlocfilehash: d990e4ded7dc2485bec6b5ecf92d9999aad57ce5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981969"
---
# <a name="jetcomputestats-function"></a>Função JetComputeStats


_**Aplica-se a:** Windows | Windows Servidor_

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

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRollbackError</p> | <p>Erro ao exigir que esta operação reverta todas as alterações, mas a reversão da transação falhou.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p>esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de êxito, as estatísticas atualizadas são armazenadas nos catálogos de banco de dados para a tabela descrita com o cursor fornecido.

Em caso de falha, nenhuma atualização de nenhum tipo é feita no banco de dados.

#### <a name="remarks"></a>Comentários

Essa operação pode ser consumindo recursos, pois cada índice em uma tabela deve ser percorrido em sua totalidade. [JetGetRecordPosition](./jetgetrecordposition-function.md) pode ser usado para obter uma estimativa aproximada do número de entradas em um índice, mas não pode, por si só, estimar o número de valores distintos em um índice.

Os dados computados por essa operação começam a ficar desatualizados e a tabela é atualizada posteriormente.

As atualizações no banco de dados feita pelo **JetComputeStats** são feitas de maneira lenta. Isso significa que nenhuma liberação de log será acompanhada por essa operação e uma falha do sistema subsequente para um retorno de JET_errSuccess pelo **JetComputeStats** ainda poderá fazer com que essas atualizações sejam perdidas.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SESID](./jet-sesid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetStopService](./jetstopservice-function.md)

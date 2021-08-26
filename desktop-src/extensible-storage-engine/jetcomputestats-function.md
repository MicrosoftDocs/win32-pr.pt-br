---
description: 'Saiba mais sobre: Função JetComputeStats'
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
ms.openlocfilehash: 1324722ed0bd239f4c5b26fbd3340d45f325e53c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465813"
---
# <a name="jetcomputestats-function"></a>Função JetComputeStats


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcomputestats-function"></a>Função JetComputeStats

A **função JetComputeStats** orienta cada índice de uma tabela para calcular exatamente o número de entradas em um índice e o número de chaves distintas em um índice. Essas informações, juntamente com o número de páginas de banco de dados alocadas para um índice e a hora atual do cálculo são armazenadas em metadados de índice no banco de dados. Esses dados podem ser recuperados posteriormente com operações de informações.

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor que será usado para essa chamada. Descreve a tabela na que calcular estatísticas.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRollbackError</p> | <p>Ocorreu um erro exigindo que essa operação reverter todas as alterações, mas a própria reação da transação falhou.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de sucesso, as estatísticas atualizadas são armazenadas nos catálogos de banco de dados da tabela descrita com o cursor determinado.

Em caso de falha, nenhuma atualização de qualquer tipo é feita no banco de dados.

#### <a name="remarks"></a>Comentários

Essa operação pode ser consumida por recursos, pois cada índice em uma tabela deve ser andado em sua totalidade. [JetGetRecordPosition](./jetgetrecordposition-function.md) pode ser usado para obter uma estimativa aproximada do número de entradas em um índice, mas por si só não pode estimar o número de valores distintos em um índice.

Os dados calculados por essa operação começam a ficar desa datados e a tabela é atualizada posteriormente.

As atualizações no banco de dados feitas **pelo JetComputeStats** são feitas de maneira lento. Isso significa que nenhuma liberação de log será acompanhada por essa operação e uma falha do sistema subsequente a um retorno de JET_errSuccess por **JetComputeStats** ainda poderá fazer com que essas atualizações sejam perdidas.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SESID](./jet-sesid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetStopService](./jetstopservice-function.md)

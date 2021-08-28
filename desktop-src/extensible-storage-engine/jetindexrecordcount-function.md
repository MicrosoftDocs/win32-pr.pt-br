---
description: 'Saiba mais sobre: Função JetIndexRecordCount'
title: Função JetIndexRecordCount
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4105dec0217c1fea2e00d92c9d217fcf2d7e40b4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480432"
---
# <a name="jetindexrecordcount-function"></a>Função JetIndexRecordCount


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetindexrecordcount-function"></a>Função JetIndexRecordCount

A **função JetIndexRecordCount** conta o número de entradas no índice atual da posição atual para frente. A posição atual está incluída na contagem. A contagem poderá ser maior que o número total de registros na tabela se o índice atual estiver sobre uma coluna com vários valores e as instâncias da coluna tiverem vários valores. Se a tabela estiver vazia, 0 será retornado para a contagem.

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*pcrec*

O ponteiro para um valor longo sem assinatura para receber a contagem.

*crecMax*

O número máximo de registros a contar. Um *valor crecMax* de 0 indica que a contagem é ilimitada.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor não está atualmente em um registro e a tabela não está vazia.</p><p><strong>Windows XP, Windows Server 2003, Windows 2000 Server e Windows 2000 Professional:</strong>  Se o cursor estiver posicionado em um índice ou intervalo de índice vazio, <strong>JetIndexRecordCount</strong> retornará erroneamente JET_errNoCurrentRecord.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p> | 



Se essa função for bem-sucedida, o número exato de entradas de índice, incluindo a posição atual e até *crecMax* (se não for 0), será retornado no tempo sem sinal apontado por *pcrec*.

Se essa função falhar, nenhuma alteração será feita na memória alocada em *precpos*.

#### <a name="remarks"></a>Comentários

Se a tabela não estiver vazia, o cursor deverá ser posicionado no registro do qual iniciar a contagem. A contagem incluirá esse registro e contará até o limite determinado em *crecMax.* Se *crecMax* for 0, a operação continuará contando até o final do índice.

Os intervalos de índice podem ser usados para construir limitações artificiais de fim de índice para a contagem. Dessa forma, os subranges de um índice podem ser contados exatamente. O cursor deve ser posicionado para a primeira linha no intervalo. O final da chave de intervalo deve ser feito e, em seguida, [JetSetIndexRange](./jetsetindexrange-function.md) deve ser usado para definir o intervalo superior, inclusive ou exclusivamente. Por fim, **JetIndexRecordCount** deve ser chamado para contar exatamente o intervalo.

**JetIndexRecordCount obedece** à semântica de transação e retorna uma contagem precisa para essa sessão específica em seu estado transacional atual.

**JetIndexRecordCount** acessa páginas de folha de índice para contar exatamente as entradas. Consequentemente, ele pode executar uma grande quantidade de E/S e pode ser lento. A *limitação crecMax* deve ser usada para evitar carga excessiva. Se um intervalo for grande, poderá ser possível contar o intervalo de maneira aproximada usando [JetGetRecordPosition](./jetgetrecordposition-function.md).

**Windows XP, Windows Server 2003, Windows 2000 Server e Windows 2000 Professional:**  Se o cursor estiver posicionado em um índice ou intervalo de índice vazio, **JetIndexRecordCount** retornará erroneamente JET_errNoCurrentRecord em vez de retornar uma contagem de registros de zero. O aplicativo deve verificar se o intervalo de índice ou índice está vazio nesse caso.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)

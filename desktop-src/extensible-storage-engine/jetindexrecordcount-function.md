---
description: 'Saiba mais sobre: função JetIndexRecordCount'
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
ms.openlocfilehash: 7ce2f5e6072e1c59820121ca652de9237b1c226f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988989"
---
# <a name="jetindexrecordcount-function"></a>Função JetIndexRecordCount


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetindexrecordcount-function"></a>Função JetIndexRecordCount

A função **JetIndexRecordCount** conta o número de entradas no índice atual a partir da posição atual para frente. A posição atual é incluída na contagem. A contagem pode ser maior que o número total de registros na tabela se o índice atual estiver sobre uma coluna de valores múltiplos e as instâncias da coluna tiverem vários valores. Se a tabela estiver vazia, 0 será retornado para a contagem.

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

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pcrec*

O ponteiro para um valor longo não atribuído para receber a contagem.

*crecMax*

O número máximo de registros a serem contados. Um valor de *crecMax* de 0 indica que a contagem é ilimitada.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor não está em um registro no momento e a tabela não está vazia.</p><p><strong>Windows XP, Windows server 2003, Windows 2000 server e Windows 2000 Professional:</strong>  Se o cursor estiver posicionado em um índice ou intervalo de índice vazio, <strong>JetIndexRecordCount</strong> retornará erroneamente JET_errNoCurrentRecord.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 



Se essa função for bem sucedido, o número exato de entradas de índice, incluindo a posição atual e até *crecMax* (se não for 0), será retornado no longo não atribuído, apontado por *pcrec*.

Se essa função falhar, nenhuma alteração será feita na memória alocada em *precpos*.

#### <a name="remarks"></a>Comentários

Se a tabela não estiver vazia, o cursor deverá ser posicionado no registro do qual começar a contagem. A contagem incluirá esse registro e a contagem será encaminhada até o limite determinado em *crecMax*. Se *crecMax* for 0, a operação continuará contando até o final do índice.

Os intervalos de índice podem ser usados para construir limitações de fim de índice artificial para a contagem. Dessa forma, os subintervalos de um índice podem ser contados exatamente. O cursor deve ser posicionado na primeira linha do intervalo. O final da chave do intervalo deve ser feito e, em seguida, [JetSetIndexRange](./jetsetindexrange-function.md) deve ser usado para definir o intervalo superior, inclusivamente ou exclusivamente. Por fim, **JetIndexRecordCount** deve ser chamado para contar exatamente o intervalo.

**JetIndexRecordCount** obedece à semântica de transação e retorna uma contagem que é precisa para essa sessão em particular em seu estado transacional atual.

O **JetIndexRecordCount** acessa páginas de folha de índice para contar com exatidão as entradas. Consequentemente, ele pode executar uma grande quantidade de e/s e pode ser lento. A limitação *crecMax* deve ser usada para evitar carga excessiva. Se um intervalo for grande, talvez seja possível contar o intervalo de maneira aproximada usando [JetGetRecordPosition](./jetgetrecordposition-function.md).

**Windows XP, Windows server 2003, Windows 2000 server e Windows 2000 Professional:**  Se o cursor estiver posicionado em um índice ou intervalo de índice vazio, **JetIndexRecordCount** retornará erroneamente JET_errNoCurrentRecord em vez de retornar uma contagem de registros zero. O aplicativo deve verificar se o índice ou intervalo de índice está vazio nesse caso.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)

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
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501293"
---
# <a name="jetindexrecordcount-function"></a>Função JetIndexRecordCount


_**Aplica-se a:** Windows | Windows Server_

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
<td><p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor não está em um registro no momento e a tabela não está vazia.</p>
<p><strong>Windows XP, Windows Server 2003, windows 2000 Server e windows 2000 Professional:</strong>  Se o cursor estiver posicionado em um índice ou intervalo de índice vazio, <strong>JetIndexRecordCount</strong> retornará erroneamente JET_errNoCurrentRecord.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Se essa função for bem sucedido, o número exato de entradas de índice, incluindo a posição atual e até *crecMax* (se não for 0), será retornado no longo não atribuído, apontado por *pcrec*.

Se essa função falhar, nenhuma alteração será feita na memória alocada em *precpos*.

#### <a name="remarks"></a>Comentários

Se a tabela não estiver vazia, o cursor deverá ser posicionado no registro do qual começar a contagem. A contagem incluirá esse registro e a contagem será encaminhada até o limite determinado em *crecMax*. Se *crecMax* for 0, a operação continuará contando até o final do índice.

Os intervalos de índice podem ser usados para construir limitações de fim de índice artificial para a contagem. Dessa forma, os subintervalos de um índice podem ser contados exatamente. O cursor deve ser posicionado na primeira linha do intervalo. O final da chave do intervalo deve ser feito e, em seguida, [JetSetIndexRange](./jetsetindexrange-function.md) deve ser usado para definir o intervalo superior, inclusivamente ou exclusivamente. Por fim, **JetIndexRecordCount** deve ser chamado para contar exatamente o intervalo.

**JetIndexRecordCount** obedece à semântica de transação e retorna uma contagem que é precisa para essa sessão em particular em seu estado transacional atual.

O **JetIndexRecordCount** acessa páginas de folha de índice para contar com exatidão as entradas. Consequentemente, ele pode executar uma grande quantidade de e/s e pode ser lento. A limitação *crecMax* deve ser usada para evitar carga excessiva. Se um intervalo for grande, talvez seja possível contar o intervalo de maneira aproximada usando [JetGetRecordPosition](./jetgetrecordposition-function.md).

**Windows XP, Windows Server 2003, windows 2000 Server e windows 2000 Professional:**  Se o cursor estiver posicionado em um índice ou intervalo de índice vazio, **JetIndexRecordCount** retornará erroneamente JET_errNoCurrentRecord em vez de retornar uma contagem de registros zero. O aplicativo deve verificar se o índice ou intervalo de índice está vazio nesse caso.

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
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)

---
description: 'Saiba mais sobre: Enumeração CommitTransactionGrbit'
title: Enumeração CommitTransactionGrbit
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a93504d688d1eddfcde81ae23c87e62f70e0aab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812112"
---
# <a name="committransactiongrbit-enumeration"></a>Enumeração CommitTransactionGrbit

Opções para JetCommitTransaction.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a>Membros

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Nome do membro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Nenhum</td>
<td>Opções padrão.</td>
</tr>
<tr class="even">
<td></td>
<td>LazyFlush</td>
<td>A transação é confirmada normalmente, mas essa API não espera que a transação seja liberada para o arquivo de log de transações antes de retornar ao chamador. Isso reduz drasticamente a duração de uma operação de confirmação no custo da durabilidade. Qualquer transação que não seja liberada para o log antes de uma falha será abortada automaticamente durante a recuperação de falha durante a próxima chamada para JetInit. Se WaitLastLevel0Commit ou WaitAllLevel0Commit forem especificados, essa opção será ignorada.</td>
</tr>
<tr class="odd">
<td></td>
<td>WaitLastLevel0Commit</td>
<td>Se a sessão tiver confirmado anteriormente quaisquer transações e elas ainda não tiverem sido liberadas para o arquivo de log de transações, elas deverão ser liberadas imediatamente. Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador. Isso será útil se o aplicativo tiver confirmado anteriormente várias transações usando JET_bitCommitLazyFlush e agora quiser liberar todas elas para o disco.
<p>Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento. Essa opção não pode ser usada em combinação com nenhuma outra opção.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

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
ms.openlocfilehash: efe052fc01014d3ebb624dbd4183bc8f0584b145
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481782"
---
# <a name="committransactiongrbit-enumeration"></a>Enumeração CommitTransactionGrbit

Opções para JetCommitTransaction.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

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


|  | Nome do membro | Descrição | 
|--|-------------|-------------|
|  | Nenhum | Opções padrão. | 
|  | LazyFlush | A transação é comprometida normalmente, mas essa API não aguarda a liberação da transação para o arquivo de log de transações antes de retornar ao chamador. Isso reduz drasticamente a duração de uma operação de confirmação às custas da durabilidade. Qualquer transação que não for liberado para o log antes de uma falha será anulada automaticamente durante a recuperação de falha durante a próxima chamada para JetInit. Se WaitLastLevel0Commit ou WaitAllLevel0Commit for especificado, essa opção será ignorada. | 
|  | WaitLastLevel0Commit | Se a sessão tiver confirmado transações anteriormente e elas ainda não foram liberados para o arquivo de log de transações, elas deverão ser liberados imediatamente. Essa API aguardará até que as transações tenham sido liberados antes de retornar ao chamador. Isso será útil se o aplicativo já tiver confirmado várias transações usando JET_bitCommitLazyFlush e agora quiser liberar todas elas para o disco.<p>Essa opção pode ser usada mesmo se a sessão não estiver atualmente em uma transação. Essa opção não pode ser usada em combinação com qualquer outra opção.</p> | 



## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

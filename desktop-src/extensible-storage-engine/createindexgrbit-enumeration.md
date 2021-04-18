---
description: 'Saiba mais sobre: Enumeração CreateIndexGrbit'
title: Enumeração CreateIndexGrbit
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793942"
---
# <a name="createindexgrbit-enumeration"></a>Enumeração CreateIndexGrbit

Opções para JetCreateIndex.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
```

## <a name="members"></a>Membros

<table>
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
<td>IndexUnique</td>
<td>Entradas de índice duplicadas (chaves) não são permitidas. Isso é imposto quando JetUpdate é chamado, não quando JetSetColumn é chamado.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexPrimary</td>
<td>O índice é um índice primário (clusterizado). Cada tabela deve ter exatamente um índice primário. Se nenhum índice primário for explicitamente definido em uma tabela, o mecanismo de banco de dados criará seu próprio índice primário.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexDisallowNull</td>
<td>Nenhuma das colunas sobre as quais o índice é criado pode conter um valor nulo.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexIgnoreNull</td>
<td>Não adicione uma entrada de índice para uma linha se todas as colunas que estão sendo indexadas forem nulas.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexIgnoreAnyNull</td>
<td>Não adicione uma entrada de índice para uma linha se qualquer uma das colunas que estão sendo indexadas for nula.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexIgnoreFirstNull</td>
<td>Não adicione uma entrada de índice para uma linha se a primeira coluna que está sendo indexada for nula.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexLazyFlush</td>
<td>Especifica que as operações de índice serão registradas lentamente. JET_bitIndexLazyFlush não afeta a ociosa das atualizações de dados. Se as operações de indexação forem interrompidas pelo encerramento do processo, a recuperação simples ainda poderá obter o banco de dados para um estado consistente, mas o índice poderá não estar presente.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexEmpty</td>
<td>Não tente Compilar o índice, pois todas as entradas seriam avaliadas como nulas. grbit também deve especificar JET_bitIgnoreAnyNull quando JET_bitIndexEmpty for passado. Esse é um aprimoramento de desempenho. Por exemplo, se uma nova coluna for adicionada a uma tabela, um índice será criado nessa coluna recém-adicionada, todos os registros na tabela seriam verificados mesmo que nunca sejam adicionados ao índice mesmo assim. Especificar JET_bitIndexEmpty ignora a verificação da tabela, o que pode levar muito tempo.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexUnversioned</td>
<td>Faz com que a criação do índice seja visível para outras transações. Normalmente, uma sessão em uma transação não poderá ver uma operação de criação de índice em outra sessão. Esse sinalizador pode ser útil se outra transação for provavelmente criar o mesmo índice, de modo que o segundo índice-Create simplesmente falhará em vez de causar muitas operações desnecessárias de banco de dados. A segunda transação pode não ser capaz de usar o índice imediatamente. A operação de criação de índice precisa ser concluída antes de ser utilizável. A sessão não deve estar em uma transação no momento para criar um índice sem informações de versão.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexSortNullsHigh</td>
<td>A especificação desse sinalizador faz com que valores nulos sejam classificados após os dados de todas as colunas no índice.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

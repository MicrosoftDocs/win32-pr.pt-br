---
description: 'Saiba mais sobre: Enumeração TempTableGrbit'
title: Enumeração TempTableGrbit
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813011"
---
# <a name="temptablegrbit-enumeration"></a>Enumeração TempTableGrbit

Opções para a criação de tabela temporária.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
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
<td>Indexa</td>
<td>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir o uso de JetSeek para pesquisar registros por chave de índice. Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</td>
</tr>
<tr class="odd">
<td></td>
<td>Exclusivo</td>
<td>Essa opção solicita que os registros com chaves de índice duplicados sejam removidos do conjunto final de registros na tabela temporária. Antes do Windows Server 2003, o mecanismo de banco de dados sempre assumiu que essa opção está em vigor devido ao fato de que todos os índices clusterizados também devem ser uma chave primária e, portanto, devem ser exclusivos. A partir do Windows Server 2003, agora é possível criar uma tabela temporária que não remove duplicatas quando a opção <a href="dn351284(v=exchg.10).md">ForwardOnly</a> também é especificada. Não é possível saber qual duplicata será vencedora e quais duplicatas serão descartadas em geral. No entanto, quando a opção ErrorOnDuplicateInsertion é solicitada, o primeiro registro com uma determinada chave de índice a ser inserido na tabela temporária sempre vencerá.</td>
</tr>
<tr class="even">
<td></td>
<td>Atualizável</td>
<td>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir que os registros que foram inseridos anteriormente sejam alterados posteriormente. Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</td>
</tr>
<tr class="odd">
<td></td>
<td>Rolável</td>
<td>Essa opção solicita que a tabela temporária seja flexível o suficiente para permitir que os registros sejam verificados em ordem e direção arbitrárias usando <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>. Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</td>
</tr>
<tr class="even">
<td></td>
<td>SortNullsHigh</td>
<td>Essa opção solicita que os valores da coluna de chave nula se aproximem do final do índice que os valores de coluna de chave não nulos.</td>
</tr>
<tr class="odd">
<td></td>
<td>ForceMaterialization</td>
<td>Essa opção força o Gerenciador de tabelas temporária a abandonar qualquer tentativa de escolher uma estratégia inteligente para gerenciar a tabela temporária que resultará em desempenho aprimorado.</td>
</tr>
<tr class="even">
<td></td>
<td>ErrorOnDuplicateInsertion</td>
<td>Essa opção solicita que qualquer tentativa de inserir um registro com a mesma chave de índice que um registro inserido anteriormente falhe imediatamente com <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>. Se essa opção não for solicitada, uma duplicata poderá ser detectada imediatamente e falhará ou poderá ser removida silenciosamente mais tarde, dependendo da estratégia escolhida pelo mecanismo de banco de dados para implementar a tabela temporária com base na funcionalidade solicitada. Se essa funcionalidade não for necessária, é melhor não solicitá-la. Se essa funcionalidade não for solicitada, o Gerenciador de tabelas temporárias poderá escolher uma estratégia para gerenciar a tabela temporária que resultará em um desempenho aprimorado.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

[ForwardOnly](./server2003grbits.forwardonly-field.md)

[IntrinsicLVsOnly](./windows7grbits.intrinsiclvsonly-field.md)

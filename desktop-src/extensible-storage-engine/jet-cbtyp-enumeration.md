---
description: 'Saiba mais sobre: enumeração de JET_cbtyp'
title: Enumeração de JET_cbtyp
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d2e545fea9c1942dc09df82eb93eafa1d3e4e89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756952"
---
# <a name="jet_cbtyp-enumeration"></a>Enumeração de JET_cbtyp

Tipo de progresso que está sendo relatado.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
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
<td>Nulo</td>
<td>Esse retorno de chamada é reservado e sempre considerado inválido.</td>
</tr>
<tr class="even">
<td></td>
<td>Finalizar</td>
<td>Uma coluna finalizável saiu para zero.</td>
</tr>
<tr class="odd">
<td></td>
<td>AntesDeInserir</td>
<td>Esse retorno de chamada ocorrerá logo antes de um novo registro ser inserido em uma tabela por uma chamada para JetUpdate.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterInsert</td>
<td>Esse retorno de chamada ocorrerá apenas depois que um novo registro tiver sido inserido em uma tabela por uma chamada para JetUpdate, mas antes de JetUpdate retornar.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeReplace</td>
<td>Esse retorno de chamada ocorrerá logo antes de um registro existente em uma tabela que está sendo alterada por uma chamada para JetUpdate.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterReplace</td>
<td>Esse retorno de chamada ocorrerá apenas depois que um registro existente em uma tabela tiver sido alterado por uma chamada para JetUpdate, mas antes de JetUpdate retornar.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeDelete</td>
<td>Esse retorno de chamada ocorrerá logo antes de um registro existente em uma tabela ser excluído por uma chamada para JetDelete.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterDelete</td>
<td>Esse retorno de chamada ocorrerá apenas depois que um registro existente em uma tabela for excluído por uma chamada para JetDelete.</td>
</tr>
<tr class="odd">
<td></td>
<td>UserDefinedDefaultValue</td>
<td>Esse retorno de chamada ocorrerá quando o mecanismo precisar recuperar o valor padrão definido pelo usuário de uma coluna do aplicativo. Esse retorno de chamada é essencialmente uma implementação limitada de JetRetrieveColumn que é avaliada pelo aplicativo. Um máximo de um valor de coluna pode ser retornado para um valor padrão definido pelo usuário.</td>
</tr>
<tr class="even">
<td></td>
<td>OnlineDefragCompleted</td>
<td>Esse retorno de chamada ocorrerá quando a desfragmentação online de um banco de dados como iniciado pelo JetDefragment tiver sido interrompida devido à conclusão do processo ou ao limite de tempo que está sendo atingido.</td>
</tr>
<tr class="odd">
<td></td>
<td>FreeCursorLS</td>
<td>Esse retorno de chamada ocorrerá quando o aplicativo precisar limpar o identificador de contexto para o armazenamento local associado a um cursor que está sendo liberado pelo mecanismo de banco de dados. Para obter mais informações, consulte JetSetLS. O delegado para esse motivo de retorno de chamada é configurado por meio de JetSetSystemParameter com JET_paramRuntimeCallback.</td>
</tr>
<tr class="even">
<td></td>
<td>FreeTableLS</td>
<td>Esse retorno de chamada ocorrerá como resultado da necessidade do aplicativo para limpar o identificador de contexto do armazenamento local associado a uma tabela que está sendo liberada pelo mecanismo de banco de dados. Para obter mais informações, consulte JetSetLS. O delegado para esse motivo de retorno de chamada é configurado por meio de JetSetSystemParameter com JET_paramRuntimeCallback.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

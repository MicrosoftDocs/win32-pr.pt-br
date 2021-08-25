---
description: 'Saiba mais sobre: Enumeração CompactGrbit'
title: Enumeração CompactGrbit
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a85f3298e4127a35acd5a39839f788fc404269f80a07463bde1417dc04f7fe16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976532"
---
# <a name="compactgrbit-enumeration"></a>Enumeração CompactGrbit

Opções para [JetCompact(JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
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
<td>Estatísticas</td>
<td>Faz com que o JetCompact despejo estatísticas no banco de dados de origem para um arquivo chamado DFRGINFO.TXT. As estatísticas incluem o nome de cada tabela no banco de dados de origem, o número de linhas em cada tabela, o tamanho total em bytes de todas as linhas em cada tabela, o tamanho total em bytes de todas as colunas do tipo <a href="hh577895(v=exchg.10).md">LongText</a> ou <a href="hh577895(v=exchg.10).md">LongBinary</a> que eram grandes o suficiente para serem armazenadas separadas do registro, o número de páginas folha de índice clusteradas e o número de páginas de folha de valor longo. Além disso, as estatísticas resumidas, incluindo o tamanho do banco de dados de origem, o banco de dados de destino, o tempo necessário para a compactação do banco de dados, o espaço temporário do banco de dados também são despejados.</td>
</tr>
<tr class="odd">
<td></td>
<td>Reparar</td>
<td><strong>Obsoleto.</strong> Usado quando o banco de dados de origem é conhecido como corrompido. Ele permite um conjunto inteiro de novos comportamentos destinados a recuperar o máximo de dados possível do banco de dados de origem. JetCompact com esse conjunto de opções pode retornar <a href="hh564840(v=exchg.10).md">Êxito,</a> mas não copiar todos os dados criados no banco de dados de origem. Os dados que estava em partes danificadas do banco de dados de origem serão ignorados.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

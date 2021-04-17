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
ms.openlocfilehash: c7bbe6c88a0a52ab852e3cde9af8871833948949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748114"
---
# <a name="compactgrbit-enumeration"></a>Enumeração CompactGrbit

Opções para [JetCompact (JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

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
<td>Faz com que o JetCompact despeje estatísticas no banco de dados de origem em um arquivo chamado DFRGINFO.TXT. As estatísticas incluem o nome de cada tabela no banco de dados de origem, o número de linhas em cada tabela, o tamanho total em bytes de todas as linhas em cada tabela, tamanho total em bytes de todas as colunas do tipo <a href="hh577895(v=exchg.10).md">LONGTEXT</a> ou <a href="hh577895(v=exchg.10).md">LongBinary</a> que foram grandes o suficiente para serem armazenados separados do registro, número de páginas de folha de índice clusterizado e número de páginas de folha de valor longo Além disso, estatísticas de resumo, incluindo o tamanho do banco de dados de origem, banco de dados de destino, tempo necessário para compactação de banco de dados, o espaço de banco de dados temporário também são todos despejados.</td>
</tr>
<tr class="odd">
<td></td>
<td>Reparar</td>
<td><strong>Obsoleto.</strong> Usado quando o banco de dados de origem é conhecido como corrompido. Ele permite que um conjunto completo de novos comportamentos se destinasse a recuperar o máximo de dados possível do banco de dado de origem. JetCompact com esse conjunto de opções pode retornar <a href="hh564840(v=exchg.10).md">êxito</a> , mas não copiar todos os dados criados no banco de dado de origem. Os dados que estavam em partes danificadas do banco de dados de origem serão ignorados.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

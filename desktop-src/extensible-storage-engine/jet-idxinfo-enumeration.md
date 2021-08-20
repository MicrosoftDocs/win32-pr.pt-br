---
description: 'Saiba mais sobre: enumeração de JET_IdxInfo'
title: Enumeração de JET_IdxInfo
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4447e5e1d7a839b27246121145e820a016eba19f4a4e7c88e487c26782bfc607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118075201"
---
# <a name="jet_idxinfo-enumeration"></a>Enumeração de JET_IdxInfo

Níveis de informações para recuperar informações de índice com JetGetIndexInfo. e JetGetTableIndexInfo.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
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
<td>Padrão</td>
<td>Retorna uma estrutura de <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> com informações sobre o índice.</td>
</tr>
<tr class="even">
<td></td>
<td>Lista</td>
<td>Retorna uma estrutura de <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> com informações sobre o índice.</td>
</tr>
<tr class="odd">
<td></td>
<td>SysTabCursor</td>
<td><strong>Obsoleto.</strong> SysTabCursor é obsoleto.</td>
</tr>
<tr class="even">
<td></td>
<td>OLC</td>
<td><strong>Obsoleto.</strong> OLC é obsoleto.</td>
</tr>
<tr class="odd">
<td></td>
<td>ResetOLC</td>
<td><strong>Obsoleto.</strong> Reset OLC é obsoleto.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAlloc</td>
<td>Retorna um inteiro com o uso de espaço do índice.</td>
</tr>
<tr class="odd">
<td></td>
<td>LCID</td>
<td>Retorna um inteiro com o LCID do índice.</td>
</tr>
<tr class="even">
<td></td>
<td>LangID</td>
<td><strong>Obsoleto.</strong> O LANGID está obsoleto. Em vez disso, use LCID.</td>
</tr>
<tr class="odd">
<td></td>
<td>Contagem</td>
<td>Retorna um inteiro com a contagem de índices na tabela.</td>
</tr>
<tr class="even">
<td></td>
<td>VarSegMac</td>
<td>Retorna um UShort com o valor de cbVarSegMac com o qual o índice foi criado.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexId</td>
<td>Retorna um <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> identificando o índice.</td>
</tr>
<tr class="even">
<td></td>
<td>Mais</td>
<td>introduzido no Windows Vista. Retorna um UShort com o valor de cbKeyMost com o qual o índice foi criado.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

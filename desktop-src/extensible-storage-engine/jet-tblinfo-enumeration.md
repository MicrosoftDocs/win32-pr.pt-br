---
description: 'Saiba mais sobre: enumeração de JET_TblInfo'
title: Enumeração de JET_TblInfo
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788905"
---
# <a name="jet_tblinfo-enumeration"></a>Enumeração de JET_TblInfo

Níveis de informações para recuperar informações de tabela com JetGetTableInfo.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
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
<td>Opção padrão. Recupera um <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> que contém informações sobre a tabela. Use essa opção com <a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>Nome</td>
<td>Recupera o nome da tabela. Use essa opção com <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>DBID</td>
<td>Recupera o <a href="hh596176(v=exchg.10).md">JET_DBID</a> do banco de dados que contém a tabela. Use essa opção com <a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceUsage</td>
<td>O comportamento do método depende do tamanho da matriz que é passada para o método. A matriz deve ter pelo menos duas entradas. A primeira entrada conterá o número de extensões de propriedade na tabela. A segunda entrada conterá o número de extensões disponíveis na tabela. Se a matriz tiver mais de duas entradas, os bytes restantes do buffer consistirão em uma matriz de estruturas que representa uma lista de extensões. Essa estrutura contém dois membros: o número da última página na extensão e o número de páginas na extensão. Use essa opção com <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAlloc</td>
<td>A matriz passada para JetGetTableInfo deve ter duas entradas. A primeira entrada será definida como o número de páginas na tabela. A segunda entrada será definida como a densidade de página de destino da tabela. Use essa opção com <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceOwned</td>
<td>Obtém o número de páginas de propriedade da tabela. Use essa opção com <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32 JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAvailable</td>
<td>Obtém o número de páginas disponíveis na tabela. Use essa opção com <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32 JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>TemplateTableName</td>
<td>Se a tabela for uma tabela derivada, o resultado será preenchido com o nome da tabela da qual a tabela derivada herdou sua DDL. Se a tabela não for uma tabela derivada, o buffer será uma cadeia de caracteres vazia. Use essa opção com <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String JET_TblInfo)</a>.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

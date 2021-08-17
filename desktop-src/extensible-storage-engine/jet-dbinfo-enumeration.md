---
description: 'Saiba mais sobre: JET_DbInfo enumeração'
title: JET_DbInfo enumeração
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c364b89ccb50542130c988a643fed594a34e370e5adb5e9d0a13f77eab5b04d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112225"
---
# <a name="jet_dbinfo-enumeration"></a>JET_DbInfo enumeração

Níveis de informações para recuperar informações do banco de dados.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
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
<td>Nome de arquivo</td>
<td>Retorna o caminho para o arquivo de banco de dados (cadeia de caracteres).</td>
</tr>
<tr class="even">
<td></td>
<td>LCID</td>
<td>Retorna o LCID (identificador de localidade) associado a este banco de dados (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Opções</td>
<td>Retorna um <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit.</a> Isso indica se o banco de dados é aberto no modo exclusivo. Se o banco de dados estiver no modo exclusivo, <a href="hh579532(v=exchg.10).md">Exclusivo</a> será retornado, caso contrário, zero será retornado. Outras opções de grbit de banco de dados para JetAttachDatabase e JetOpenDatabase não são retornadas.</td>
</tr>
<tr class="even">
<td></td>
<td>Transactions</td>
<td>Retorna um número um maior que o nível máximo ao qual as transações podem ser aninhadas. Se <a href="dn292105(v=exchg.10).md">JetBeginTransaction(JET_SESID)</a> for chamado (de forma aninhada, ou seja, na mesma sessão, sem uma confirmação ou reposição) tantas vezes quanto esse valor, na última chamada <a href="hh564840(v=exchg.10).md">TransTooDeep</a> será retornado (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Versão</td>
<td>Retorna a versão principal do mecanismo de banco de dados (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>Filesize</td>
<td>Retorna o filesize do banco de dados, em páginas (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceOwned</td>
<td>Retorna o espaço de propriedade do banco de dados, em páginas (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAvailable</td>
<td>Retorna o espaço disponível no banco de dados, em páginas (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Diversos</td>
<td>Retorna um <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> objeto .</td>
</tr>
<tr class="even">
<td></td>
<td>DBInUse</td>
<td>Retorna um booliana que indica se o banco de dados está anexado (booliana).</td>
</tr>
<tr class="odd">
<td></td>
<td>PageSize</td>
<td>Retorna o tamanho da página do banco de dados (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>FileType</td>
<td>Retorna o tipo do banco de dados (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

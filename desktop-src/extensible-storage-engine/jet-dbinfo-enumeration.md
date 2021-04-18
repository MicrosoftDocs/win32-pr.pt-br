---
description: 'Saiba mais sobre: enumeração de JET_DbInfo'
title: Enumeração de JET_DbInfo
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
ms.openlocfilehash: 39c6c3175c08e4f7644ad4f0b41137e12e84f71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771268"
---
# <a name="jet_dbinfo-enumeration"></a>Enumeração de JET_DbInfo

Níveis de informações para recuperar informações do banco de dados.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

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
<td>Retorna um <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>. Isso indica se o banco de dados está aberto em modo exclusivo. Se o banco de dados estiver em modo exclusivo, o <a href="hh579532(v=exchg.10).md">exclusivo</a> será retornado, caso contrário, zero será retornado. Outras opções de grbit de banco de dados para JetAttachDatabase e JetOpenDatabase não são retornadas.</td>
</tr>
<tr class="even">
<td></td>
<td>Transactions</td>
<td>Retorna um número um maior do que o nível máximo para o qual as transações podem ser aninhadas. Se <a href="dn292105(v=exchg.10).md">JetBeginTransaction (JET_SESID)</a> for chamado (em um modo de aninhamento, ou seja, na mesma sessão, sem uma confirmação ou reversão) quantas vezes esse valor, na última chamada, <a href="hh564840(v=exchg.10).md">TransTooDeep</a> será retornado (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Versão</td>
<td>Retorna a versão principal do mecanismo de banco de dados (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>Tamanho</td>
<td>Retorna o tamanho do banco de dados, em páginas (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceOwned</td>
<td>Retorna o espaço de Propriedade do banco de dados, em páginas (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAvailable</td>
<td>Retorna o espaço disponível no banco de dados, em páginas (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Diversos</td>
<td>Retorna um objeto <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> .</td>
</tr>
<tr class="even">
<td></td>
<td>DBInUse</td>
<td>Retorna um valor booleano que indica se o banco de dados está anexado (booliano).</td>
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

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

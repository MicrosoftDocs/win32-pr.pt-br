---
description: 'Saiba mais sobre: função JetDeleteTable'
title: Função JetDeleteTable
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787760"
---
# <a name="jetdeletetable-function"></a>Função JetDeleteTable


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetdeletetable-function"></a>Função JetDeleteTable

A função **JetDeleteTable** exclui uma tabela em um banco de dados ESE.

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*DBID*

O identificador de banco de dados a ser usado para a chamada à API.

*szTableName*

O nome da tabela a ser excluída.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Foi feita uma tentativa de excluir uma tabela enquanto outra sessão tem uma ID de tabela aberta (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) com <a href="gg294118(v=exchg.10).md">JetOpenTable</a> ou <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</p></td>
</tr>
<tr class="odd">
<td><p>Tabela de JET_errCannotDeletetemporary</p></td>
<td><p>Foi feita uma tentativa de excluir uma tabela temporária. Uma tabela temporária é excluída automaticamente quando fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable</p></td>
<td><p>Foi feita uma tentativa de excluir uma tabela de modelo, ou seja, uma tabela da qual o DDL pode ser herdado.</p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetDeleteTableW</strong> (Unicode) e <strong>JetDeleteTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JetCloseTable](./jetclosetable-function.md)

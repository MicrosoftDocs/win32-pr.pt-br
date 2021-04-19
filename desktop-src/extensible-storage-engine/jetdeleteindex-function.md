---
description: 'Saiba mais sobre: função JetDeleteIndex'
title: Função JetDeleteIndex
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52a29e619d6643df4984bd7f296dcef4ef0a5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763778"
---
# <a name="jetdeleteindex-function"></a>Função JetDeleteIndex


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetdeleteindex-function"></a>Função JetDeleteIndex

A função **JetDeleteIndex** exclui um índice de uma tabela.

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela que contém a coluna a ser excluída.

*szIndexName*

O nome do índice a ser excluído.

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
<td><p>JET_errFixedDDL</p></td>
<td><p>Foi feita uma tentativa de excluir um índice de uma tabela fixa (por exemplo, um criado com JET_bitTableCreateFixedDDL).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedInheritedDDL</p></td>
<td><p>Foi feita uma tentativa de excluir um índice de uma tabela de modelo. Uma tabela de modelo tem um DDL fixo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexNotFound</p></td>
<td><p>O índice nomeado em <em>szIndexName</em> não foi encontrado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Não é possível atualizar a tabela porque ela foi aberta como somente leitura.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Vários threads tentaram usar a mesma sessão de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>A transação foi aberta como uma transação somente leitura.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Quando bem-sucedido, o índice é excluído e, portanto, não pode ser usado posteriormente. Não deve haver nenhuma transação ativa usando o índice.

Em caso de sucesso, a moeda é definida antes do primeiro registro.

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
<td><p>Implementado como <strong>JetDeleteIndexW</strong> (Unicode) e <strong>JetDeleteIndexA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)

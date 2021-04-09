---
description: 'Saiba mais sobre: estrutura de JET_OBJECTINFO'
title: Estrutura JET_OBJECTINFO
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011419"
---
# <a name="jet_objectinfo-structure"></a>Estrutura JET_OBJECTINFO


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_objectinfo-structure"></a>Estrutura JET_OBJECTINFO

A estrutura de **JET_OBJECTINFO** contém informações sobre um objeto. As tabelas são os únicos tipos de objeto com suporte no momento.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho, em bytes, da estrutura de **JET_OBJECTINFO** .

**objtyp**

Mantém a [JET_OBJTYP](./jet-objtyp.md) da estrutura. No momento, apenas tabelas serão retornadas (ou seja, JET_objtypTable).

**dtCreate**

Obsoleto. Não use.

**dtUpdate**

Obsoleto. Não use.

**grbit**

Um grupo de bits que contém as opções que estão disponíveis para esta chamada, que incluem zero ou mais das ações a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitTableInfoBookmark</p></td>
<td><p>A tabela pode ter indicadores.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableInfoRollback</p></td>
<td><p>A tabela pode ser revertida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableInfoUpdatable</p></td>
<td><p>A tabela pode ser atualizada.</p></td>
</tr>
</tbody>
</table>


**sinalizadores**

Um campo de bits que contém zero ou mais dos sinalizadores a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitObjectSystem</p></td>
<td><p>A tabela é uma tabela do sistema e é somente para uso interno.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableDerived</p></td>
<td><p>A tabela herdada DDL de uma tabela de modelo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableFixedDDL</p></td>
<td><p>Não é possível modificar o DDL da tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Usado em conjunto com JET_bitObjectTableTemplate para não permitir colunas fixas ou variáveis em tabelas derivadas (para que colunas fixas ou variáveis possam ser adicionadas ao modelo no futuro).</p>
<p><strong>Windows XP:  </strong> Esse valor é introduzido no Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableTemplate</p></td>
<td><p>A tabela é uma tabela de modelo.</p></td>
</tr>
</tbody>
</table>


**cRecord**

O número de registros na tabela.

Esse valor será recuperado somente se **JET_OBJECTINFO** foi passado para [JetGetObjectInfo](./jetgetobjectinfo-function.md).

**cPage**

O número de páginas que estão sendo usadas pela tabela.

Esse valor será recuperado somente se **JET_OBJECTINFO** foi passado para [JetGetObjectInfo](./jetgetobjectinfo-function.md).

### <a name="remarks"></a>Comentários

Uma estrutura de **JET_OBJECTINFO** é preenchida por uma chamada para [JetGetObjectInfo](./jetgetobjectinfo-function.md) ou [JetGetTableInfo](./jetgettableinfo-function.md). Se a chamada à API não for concluída com sucesso, o conteúdo da estrutura será indefinido.

Se aplicável, as estatísticas de tabela incluem o número de registros e o número de páginas que estão no índice clusterizado (ou seja, o índice que contém os dados de registro). As estatísticas de índice são acessadas separadamente por nome, usando [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

### <a name="requirements"></a>Requisitos

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
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)

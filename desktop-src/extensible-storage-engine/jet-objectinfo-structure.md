---
description: 'Saiba mais sobre: estrutura JET_OBJECTINFO dados'
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
ms.openlocfilehash: d61c42897da6d55dc96f2e59847fcf727424d60e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986119"
---
# <a name="jet_objectinfo-structure"></a>Estrutura JET_OBJECTINFO


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_objectinfo-structure"></a>Estrutura JET_OBJECTINFO

A **JET_OBJECTINFO** estrutura contém informações sobre um objeto . As tabelas são os únicos tipos de objeto com suporte no momento.

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

**Cbstruct**

O tamanho, em bytes, da **estrutura JET_OBJECTINFO** dados.

**objtyp**

Contém a [JET_OBJTYP](./jet-objtyp.md) da estrutura. Atualmente, somente tabelas serão retornadas (ou seja, JET_objtypTable).

**dtCreate**

Obsoleto. Não use.

**dtUpdate**

Obsoleto. Não use.

**grbit**

Um grupo de bits que contém as opções disponíveis para essa chamada, que incluem zero ou mais dos seguintes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTableInfoBookmark</p> | <p>A tabela pode ter indicadores.</p> | 
| <p>JET_bitTableInfoRollback</p> | <p>A tabela pode ser relembolsada.</p> | 
| <p>JET_bitTableInfoUpdatable</p> | <p>A tabela pode ser atualizada.</p> | 



**sinalizadores**

Um campo de bits que contém zero ou mais dos sinalizadores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitObjectSystem</p> | <p>A tabela é uma Tabela do Sistema e é somente para uso interno.</p> | 
| <p>JET_bitObjectTableDerived</p> | <p>A DDL herdada da tabela de uma tabela de modelo.</p> | 
| <p>JET_bitObjectTableFixedDDL</p> | <p>A DDL da tabela não pode ser modificada.</p> | 
| <p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p> | <p>Usado em conjunto com JET_bitObjectTableTemplate para não permitir colunas fixas ou variáveis em tabelas derivadas (para que colunas fixas ou variáveis possam ser adicionadas ao modelo no futuro).</p><p><strong>Windows XP:</strong> Esse valor é introduzido no Windows XP.</p> | 
| <p>JET_bitObjectTableTemplate</p> | <p>A tabela é uma tabela de modelo.</p> | 



**cRecord**

O número de registros na tabela.

Esse valor será recuperado somente se **JET_OBJECTINFO** foi passado para [JetGetObjectInfo](./jetgetobjectinfo-function.md).

**cPage**

O número de páginas que estão sendo usadas pela tabela.

Esse valor será recuperado somente se **JET_OBJECTINFO** foi passado para [JetGetObjectInfo](./jetgetobjectinfo-function.md).

### <a name="remarks"></a>Comentários

Uma **JET_OBJECTINFO** é populada por uma chamada para [JetGetObjectInfo](./jetgetobjectinfo-function.md) ou [JetGetTableInfo.](./jetgettableinfo-function.md) Se a chamada à API não for bem-sucedida, o conteúdo da estrutura será indefinido.

Se aplicável, as estatísticas de tabela incluem o número de registros e o número de páginas que estão no índice cluster (ou seja, o índice que contém os dados do registro). As estatísticas de índice são acessadas separadamente por nome, [usando JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



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

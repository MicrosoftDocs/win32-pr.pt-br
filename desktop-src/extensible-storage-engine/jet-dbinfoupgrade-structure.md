---
description: 'Saiba mais sobre: estrutura JET_DBINFOUPGRADE dados'
title: Estrutura JET_DBINFOUPGRADE
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: f8a62245ee4b09ec3e8764e6d4e51841fa057c789bdc2fb4a142380d62e8d598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112175"
---
# <a name="jet_dbinfoupgrade-structure"></a>Estrutura JET_DBINFOUPGRADE


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_dbinfoupgrade-structure"></a>Estrutura JET_DBINFOUPGRADE

A **JET_DBINFOUPGRADE** contém informações sobre o status de atualização do banco de dados. Esse valor será recuperado somente se **JET_DBINFOUPGRADE** foi passado para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo.](./jetgetdatabasefileinfo-function.md) Essa estrutura não é necessária para versões atuais do sistema operacional do mecanismo de banco de dados.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a>Membros

**Cbstruct**

Definido como o tamanho da estrutura **JET_DBINFOUPGRADE,** em bytes.

**cbFilesizeLow**

O **DWORD baixo** que reflete o tamanho do arquivo atual para o banco de dados.

**cbFilesizeHigh**

O **DWORD alto que** reflete o tamanho do arquivo atual para o banco de dados.

**cbFreeSpaceRequiredLow**

A **DWORD baixa do** espaço livre estimado em disco necessário para uma atualização in-place.

**cbFreeSpaceRequiredHigh**

A alta **DWORD do** espaço livre estimado em disco necessário para uma atualização in-place.

**csecToUpgrade**

O tempo estimado necessário para atualizar, em segundos.

**Ulflags**

Um campo de bits feito de zero ou mais dos seguintes sinalizadores: **fUpgradable,** **fAlreadyUpgraded.**

**fUpgradable**

O banco de dados é atualizável.

**fAlreadyUpgraded**

O banco de dados é atualizado para o formato de banco de dados atual.

### <a name="remarks"></a>Comentários

Uma **JET_DBINFOUPGRADE** estrutura é populada por uma chamada para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md). Se a função não for bem-sucedida, o conteúdo da estrutura será indefinido.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)

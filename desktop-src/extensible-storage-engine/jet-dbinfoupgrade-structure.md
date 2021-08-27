---
description: 'Saiba mais sobre: estrutura de JET_DBINFOUPGRADE'
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
ms.openlocfilehash: 57c9265f45412bd31e087a52ab2b923c9c55c430
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467653"
---
# <a name="jet_dbinfoupgrade-structure"></a>Estrutura JET_DBINFOUPGRADE


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_dbinfoupgrade-structure"></a>Estrutura JET_DBINFOUPGRADE

A estrutura de **JET_DBINFOUPGRADE** contém informações sobre o status de atualização do banco de dados. Esse valor será recuperado somente se **JET_DBINFOUPGRADE** foi passado para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md). Essa estrutura não é necessária para as versões atuais do sistema operacional do mecanismo de banco de dados.

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

**cbStruct**

Defina como o tamanho da estrutura de **JET_DBINFOUPGRADE** , em bytes.

**cbFilesizeLow**

O **DWORD** baixo que reflete o tamanho de arquivo atual do banco de dados.

**cbFilesizeHigh**

O **DWORD** alto que reflete o tamanho do arquivo atual para o banco de dados.

**cbFreeSpaceRequiredLow**

O menor **DWORD** do espaço livre em disco estimado necessário para uma atualização in-loco.

**cbFreeSpaceRequiredHigh**

O grande **DWORD** do espaço livre em disco estimado necessário para uma atualização in-loco.

**csecToUpgrade**

O tempo estimado necessário para a atualização, em segundos.

**ulFlags**

Um campo de bits formado por zero ou mais dos seguintes sinalizadores: **fUpgradable**, **fAlreadyUpgraded**.

**fUpgradable**

O banco de dados é atualizável.

**fAlreadyUpgraded**

O banco de dados é atualizado para o formato de banco de dados atual.

### <a name="remarks"></a>Comentários

Uma estrutura de **JET_DBINFOUPGRADE** é populada por uma chamada para [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md). Se a função não for concluída com sucesso, o conteúdo da estrutura será indefinido.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)

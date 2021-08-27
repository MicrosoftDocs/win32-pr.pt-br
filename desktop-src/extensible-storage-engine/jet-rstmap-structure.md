---
description: 'Saiba mais sobre: estrutura JET_RSTMAP dados'
title: estrutura JET_RSTMAP de JET_RSTMAP
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: e1f3813be8e1ea076a401ce5cdabef3e454b98c1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983579"
---
# <a name="jet_rstmap-structure"></a>estrutura JET_RSTMAP de JET_RSTMAP


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_rstmap-structure"></a>estrutura JET_RSTMAP de JET_RSTMAP

A **JET_RSTMAP** habilita o remapeamento de caminhos de arquivo de banco de dados armazenados nos logs de transações durante a recuperação, quando usados pelas funções [JetInit](./jetinit-function.md) e [JetExternalRestore.](./jetexternalrestore-function.md) Isso permite que os bancos de dados sejam movidos quando offline ou quando restaurados do backup.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Membros

**szDatabaseName**

O caminho absoluto atual de um banco de dados associado aos logs de transações que são replayados durante a recuperação.

**szNewDatabaseName**

O novo caminho absoluto para o banco de dados.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_RSTMAP_W</strong> (Unicode) <strong>e JET_RSTMAP_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte Também

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)

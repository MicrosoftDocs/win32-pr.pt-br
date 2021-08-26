---
description: 'Saiba mais sobre: estrutura de JET_RSTMAP'
title: Estrutura de JET_RSTMAP
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
ms.openlocfilehash: 8e9952c040540e78c76d81babbb4c7b326fe92f8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465853"
---
# <a name="jet_rstmap-structure"></a>Estrutura de JET_RSTMAP


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_rstmap-structure"></a>Estrutura de JET_RSTMAP

A estrutura de **JET_RSTMAP** permite o remapeamento de caminhos de arquivo de banco de dados que são armazenados nos logs de transação durante a recuperação, quando usados pelas funções [JetInit](./jetinit-function.md) e [JetExternalRestore](./jetexternalrestore-function.md) . Isso permite que os bancos de dados sejam movidos quando offline ou restaurados do backup.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Membros

**szDatabaseName**

O caminho absoluto atual de um banco de dados que está associado aos logs de transação que são reproduzidos durante a recuperação.

**szNewDatabaseName**

O novo caminho absoluto para o banco de dados.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_RSTMAP_W</strong> (Unicode) e <strong>JET_RSTMAP_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte Também

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)

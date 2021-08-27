---
description: 'Saiba mais sobre: estrutura de JET_CONVERT'
title: Estrutura de JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: 9ca27bcc8024d8d3f0f634f6f8e6b23082b8d075
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480502"
---
# <a name="jet_convert-structure"></a>Estrutura de JET_CONVERT


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_convert-structure"></a>Estrutura de JET_CONVERT

A estrutura de **JET_CONVERT** contém o nome de uma DLL de versão anterior do ESE que é usada para ler os bancos de dados criados com essa versão anterior. Além disso, outros sinalizadores são fornecidos para controlar a natureza da conversão.

**Windows Server 2003:** o recurso no [JetCompact](./jetcompact-function.md) que realizou uma conversão foi removido do produto no Windows Server 2003. há suporte apenas no Windows 2000 e Windows XP.

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a>Membros

**SzOldDll**

O nome, incluindo informações de caminho, para a versão anterior da DLL do ESE.

**fFlags**

Reservado para uso do sistema.

**fSchemaChangesOnly**

Reservado para uso do sistema.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_CONVERT_W</strong> (Unicode) e <strong>JET_CONVERT_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte Também

[JetCompact](./jetcompact-function.md)

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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827422"
---
# <a name="jet_convert-structure"></a>Estrutura de JET_CONVERT


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_convert-structure"></a>Estrutura de JET_CONVERT

A estrutura de **JET_CONVERT** contém o nome de uma DLL de versão anterior do ESE que é usada para ler os bancos de dados criados com essa versão anterior. Além disso, outros sinalizadores são fornecidos para controlar a natureza da conversão.

**Windows Server 2003:** O recurso no [JetCompact](./jetcompact-function.md) que realizou uma conversão foi removido do produto no Windows Server 2003. Só há suporte para ele no Windows 2000 e no Windows XP.

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
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JET_CONVERT_W</strong> (Unicode) e <strong>JET_CONVERT_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetCompact](./jetcompact-function.md)

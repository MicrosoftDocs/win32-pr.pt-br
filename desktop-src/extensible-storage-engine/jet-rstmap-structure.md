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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646913"
---
# <a name="jet_rstmap-structure"></a>Estrutura de JET_RSTMAP


_**Aplica-se a:** Windows | Windows Server_

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
<td><p>Implementado como <strong>JET_RSTMAP_W</strong> (Unicode) e <strong>JET_RSTMAP_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)

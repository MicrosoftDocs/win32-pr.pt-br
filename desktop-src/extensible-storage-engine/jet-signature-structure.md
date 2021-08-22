---
description: 'Saiba mais sobre: estrutura JET_SIGNATURE dados'
title: estrutura JET_SIGNATURE de dados
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: 9d254a392ade9daa43382d8418f2dda90729eddc81f6c3bbd7013d89ae8f2e74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616186"
---
# <a name="jet_signature-structure"></a>estrutura JET_SIGNATURE de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_signature-structure"></a>estrutura JET_SIGNATURE de dados

A **JET_SIGNATURE** contém informações que identificam exclusivamente um banco de dados.

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a>Membros

**ulRandom**

Um número atribuído aleatoriamente.

**logtimeCriar**

O [JET_LOGTIME](./jet-logtime-structure.md) no momento em que [JetCreateDatabase](./jetcreatedatabase-function.md) é executado.

**szComputerName**

O valor de cadeia de caracteres opcional do nome NetBIOS para o computador. Esse valor pode não ser definido.

### <a name="remarks"></a>Comentários

Isso pode ser encontrado como um elemento de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).

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

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)

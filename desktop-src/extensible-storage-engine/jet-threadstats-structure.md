---
description: 'Saiba mais sobre: estrutura de JET_THREADSTATS'
title: Estrutura de JET_THREADSTATS
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797983"
---
# <a name="jet_threadstats-structure"></a>Estrutura de JET_THREADSTATS


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_threadstats-structure"></a>Estrutura de JET_THREADSTATS

A estrutura de **JET_THREADSTATS** contém estatísticas cumulativas no trabalho executado pelo mecanismo de banco de dados no thread atual. Essas informações são retornadas por meio de [JetGetThreadStats](./jetgetthreadstats-function.md).

**Windows Vista:**  A estrutura de **JET_THREADSTATS** é introduzida no Windows Vista.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura de **JET_THREADSTATS** retornada, em bytes.

**Observação**  A estrutura de **JET_THREADSTATS** será expandida no futuro para conter mais estatísticas. Novas estatísticas serão adicionadas ao final da estrutura e poderão ser recuperadas com um tamanho de buffer de saída maior. A presença de estatísticas adicionais pode ser inferida por um valor **cbStruct** maior.

**cPageReferenced**

O número total de páginas de banco de dados visitadas pelo mecanismo de banco de dados no thread atual.

**cPageRead**

O número total de páginas de banco de dados buscadas do disco pelo mecanismo de banco de dados no thread atual.

**cPagePreread**

O número total de páginas de banco de dados pré-busca do disco pelo mecanismo de banco de dados no thread atual.

**cPageDirtied**

O número total de páginas de banco de dados, sem alterações não gravadas, que foram modificadas pelo mecanismo de banco de dados no thread atual.

**cPageRedirtied**

O número total de páginas de banco de dados, com alterações não gravadas, que foram modificadas pelo mecanismo de banco de dados no thread atual.

**cLogRecord**

O número total de registros de log de transações que foram gerados pelo mecanismo de banco de dados no thread atual.

**cbLogRecord**

O tamanho total em bytes dos registros de log de transações que foram gerados pelo mecanismo de banco de dados no thread atual.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetGetThreadStats](./jetgetthreadstats-function.md)

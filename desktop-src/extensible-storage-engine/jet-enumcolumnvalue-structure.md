---
description: 'Saiba mais sobre: estrutura de JET_ENUMCOLUMNVALUE'
title: Estrutura de JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788917"
---
# <a name="jet_enumcolumnvalue-structure"></a>Estrutura de JET_ENUMCOLUMNVALUE


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_enumcolumnvalue-structure"></a>Estrutura de JET_ENUMCOLUMNVALUE

A estrutura de **JET_ENUMCOLUMNVALUE** enumera os valores de coluna de um registro usando a função [JetEnumerateColumns](./jetenumeratecolumns-function.md) . [JetEnumerateColumns](./jetenumeratecolumns-function.md) retorna uma matriz de estruturas de **JET_ENUMCOLUMNVALUE** . A matriz é retornada na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para essa função.

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>Membros

**itagSequence**

O valor da coluna (por índice baseado em um) que foi enumerado.

**erra**

O código de status da coluna resultante da enumeração do valor da coluna.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>O valor da coluna solicitada é nulo.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>O <em>itagSequence</em> especificado no elemento da matriz <em>rgtagSequence</em> no struct <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> correspondente a este <strong>JET_ENUMCOLUMNVALUE</strong> struct era zero.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnTruncated</p></td>
<td><p>O valor da coluna solicitada foi truncado para o tamanho especificado antes de ser retornado.</p>
<p>Esse truncamento ocorre apenas para longas colunas de texto e binários longos que contêm grandes quantidades de dados.</p></td>
</tr>
</tbody>
</table>


**cbData**

O valor da coluna que foi enumerado para a coluna.

O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).

**pvData**

O valor da coluna que foi enumerado para a coluna.

O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).

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
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)

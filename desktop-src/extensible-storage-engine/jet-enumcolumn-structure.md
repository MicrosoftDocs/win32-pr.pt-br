---
description: 'Saiba mais sobre: estrutura JET_ENUMCOLUMN dados'
title: Estrutura JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: 6ac89a45e37631b554fc7b2dc28266c95cfae3fba54debb427abfd8db621ea3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766084"
---
# <a name="jet_enumcolumn-structure"></a>Estrutura JET_ENUMCOLUMN


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_enumcolumn-structure"></a>Estrutura JET_ENUMCOLUMN

A **JET_ENUMCOLUMN** enumera os valores de coluna de um registro quando a [função JetEnumerateColumns](./jetenumeratecolumns-function.md) é usada. [JetEnumerateColumns retorna](./jetenumeratecolumns-function.md) uma matriz de **JET_ENUMCOLUMN** estruturas. A matriz é retornada na memória alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para essa API.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a>Membros

**Columnid**

A ID da coluna que foi enumerada.

**Err**

O código de status da coluna que resulta da enumeração da coluna.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Códigos de erro</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>A ID da coluna está fora dos limites legais de uma ID de coluna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>A coluna descrita pela ID da coluna não existe na tabela.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Todos os valores dessa coluna são NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnPresent</p></td>
<td><p>JET_bitEnumeratePresenceOnly foi especificado e pelo menos um valor de coluna não NULL teria sido retornado para essa coluna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSingleValue</p></td>
<td><p>JET_bitEnumerateCompressOutput foi especificado e exatamente um valor de coluna não NULL foi retornado para essa coluna. Como resultado, a forma compactada <strong>de JET_ENUMCOLUMN</strong> foi retornada. Consulte <strong>JET_ENUMCOLUMN</strong> para obter mais informações.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>A ID da coluna <a href="gg269251(v=exchg.10).md">no JET_ENUMCOLUMNID</a> struct correspondente a <strong>esse JET_ENUMCOLUMN</strong> struct era zero.</p></td>
</tr>
</tbody>
</table>


**cEnumColumnValue**

A matriz de valores de coluna que foi enumerada para a coluna. O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecido para [JetEnumerateColumns.](./jetenumeratecolumns-function.md)

Esse buffer de saída é usado quando o código de status da coluna não é igual a JET_wrnColumnSingleValue. Para obter mais informações, [consulte JetEnumerateColumns](./jetenumeratecolumns-function.md).

Isso será retornado se "err \! = JET_wrnColumnSingleValue".

**rgEnumColumnValue**

A matriz de valores de coluna que foi enumerada para a coluna. O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecido para [JetEnumerateColumns.](./jetenumeratecolumns-function.md)

Esse buffer de saída é usado quando o código de status da coluna não é igual a JET_wrnColumnSingleValue. Para obter mais informações, [consulte JetEnumerateColumns](./jetenumeratecolumns-function.md).

Isso será retornado se "err \! = JET_wrnColumnSingleValue".

**cbData**

O valor da coluna que foi enumerado para a coluna.

O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecido para [JetEnumerateColumns.](./jetenumeratecolumns-function.md)

Esse buffer de saída só é usado quando o código de status da coluna é JET_wrnColumnSingleValue. Para obter mais informações, [consulte JetEnumerateColumns](./jetenumeratecolumns-function.md).

Isso será retornado se "err == JET_wrnColumnSingleValue".

**Pvdata**

O valor da coluna que foi enumerado para a coluna.

O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecido para [JetEnumerateColumns.](./jetenumeratecolumns-function.md)

Esse buffer de saída só é usado quando o código de status da coluna é JET_wrnColumnSingleValue. Para obter mais informações, [consulte JetEnumerateColumns](./jetenumeratecolumns-function.md).

Isso será retornado se "err == JET_wrnColumnSingleValue".

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)

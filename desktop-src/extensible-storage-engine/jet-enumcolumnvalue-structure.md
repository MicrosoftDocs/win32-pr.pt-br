---
description: 'Saiba mais sobre: estrutura JET_ENUMCOLUMNVALUE dados'
title: estrutura JET_ENUMCOLUMNVALUE dados
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
ms.openlocfilehash: 3a4d9500980434c21f9dfa6584db666418605de8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988609"
---
# <a name="jet_enumcolumnvalue-structure"></a>estrutura JET_ENUMCOLUMNVALUE dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_enumcolumnvalue-structure"></a>estrutura JET_ENUMCOLUMNVALUE dados

A **JET_ENUMCOLUMNVALUE** enumera os valores de coluna de um registro usando a [função JetEnumerateColumns.](./jetenumeratecolumns-function.md) [JetEnumerateColumns retorna](./jetenumeratecolumns-function.md) uma matriz de **JET_ENUMCOLUMNVALUE** estruturas. A matriz é retornada na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para essa função.

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

**Err**

O código de status da coluna resultante da enumeração do valor da coluna.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_wrnColumnNull</p> | <p>O valor da coluna solicitada é NULL.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p>O <em>itagSequence</em> especificado no elemento da matriz <em>rgtagSequence</em> no struct JET_ENUMCOLUMN correspondente <a href="gg294138(v=exchg.10).md">a</a> esse JET_ENUMCOLUMNVALUE <strong>struct</strong> era zero.</p> | 
| <p>JET_wrnColumnTruncated</p> | <p>O valor da coluna solicitada foi truncado para o tamanho especificado antes de ser retornado.</p><p>Esse truncamento ocorre somente para texto longo e colunas binárias longas que contêm grandes quantidades de dados.</p> | 



**cbData**

O valor da coluna que foi enumerado para a coluna.

O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecido para [JetEnumerateColumns.](./jetenumeratecolumns-function.md)

**Pvdata**

O valor da coluna que foi enumerado para a coluna.

O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornecido para [JetEnumerateColumns.](./jetenumeratecolumns-function.md)

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)

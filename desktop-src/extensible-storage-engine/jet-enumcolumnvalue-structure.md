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
ms.openlocfilehash: 86905d49bb798d37bad48087c48e77349ec10f57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482282"
---
# <a name="jet_enumcolumnvalue-structure"></a>Estrutura de JET_ENUMCOLUMNVALUE


_**Aplica-se a:** Windows | Windows Servidor_

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


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_wrnColumnNull</p> | <p>O valor da coluna solicitada é nulo.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p>O <em>itagSequence</em> especificado no elemento da matriz <em>rgtagSequence</em> no struct <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> correspondente a este <strong>JET_ENUMCOLUMNVALUE</strong> struct era zero.</p> | 
| <p>JET_wrnColumnTruncated</p> | <p>O valor da coluna solicitada foi truncado para o tamanho especificado antes de ser retornado.</p><p>Esse truncamento ocorre apenas para longas colunas de texto e binários longos que contêm grandes quantidades de dados.</p> | 



**cbData**

O valor da coluna que foi enumerado para a coluna.

O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).

**pvData**

O valor da coluna que foi enumerado para a coluna.

O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)

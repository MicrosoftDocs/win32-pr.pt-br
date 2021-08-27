---
description: 'Saiba mais sobre: estrutura JET_RECPOS dados'
title: estrutura JET_RECPOS de dados
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: 6eb136ef309bad4ffd5c02768a3ca5b8e0d52f3c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470511"
---
# <a name="jet_recpos-structure"></a>estrutura JET_RECPOS de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_recpos-structure"></a>estrutura JET_RECPOS de dados

A **JET_RECPOS** contém uma coleção de inteiros que representam uma posição fracionária dentro de um índice. **centriesLT** é o número de entradas de índice menor que a chave de índice atual. **centriesInRange** é o número de entradas de índice igual à chave atual. **não há suporte para centriesInRange** e é sempre retornado como 1. **centriesTotal** é o número de entradas de índice no índice. Todos os valores são aproximações sem garantia de precisão.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>Membros

**Cbstruct**

O tamanho da estrutura [JET_RETINFO,](./jet-retinfo-structure.md) em bytes. Esse valor confirma a presença dos campos a seguir.

**centriesLT**

O número aproximado de entradas de índice menor que a chave atual.

**centriesInRange**

O número aproximado de entradas de índice igual à chave atual. Esse campo é sempre definido como 1, independentemente do número de entradas de índice que são realmente iguais à chave atual.

**centriesTotal**

O número aproximado de entradas no índice.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)

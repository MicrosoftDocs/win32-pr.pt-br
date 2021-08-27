---
description: 'Saiba mais sobre: estrutura de JET_RECPOS'
title: Estrutura de JET_RECPOS
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
ms.openlocfilehash: ed374030bd3ab577b209d326d21110482c9cf37a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989109"
---
# <a name="jet_recpos-structure"></a>Estrutura de JET_RECPOS


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_recpos-structure"></a>Estrutura de JET_RECPOS

A estrutura de **JET_RECPOS** contém uma coleção de inteiros que representam uma posição fracionária dentro de um índice. **centriesLT** é o número de entradas de índice menor que a chave de índice atual. **centriesInRange** é o número de entradas de índice iguais à chave atual. **centriesInRange** não tem suporte e sempre é retornado como 1. **centriesTotal** é o número de entradas de índice no índice. Todos os valores são aproximações sem nenhuma garantia de precisão.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura de [JET_RETINFO](./jet-retinfo-structure.md) , em bytes. Esse valor confirma a presença dos campos a seguir.

**centriesLT**

O número aproximado de entradas de índice menores que a chave atual.

**centriesInRange**

O número aproximado de entradas de índice iguais à chave atual. Esse campo é sempre definido como 1, independentemente do número de entradas de índice que são realmente iguais à chave atual.

**centriesTotal**

O número aproximado de entradas no índice.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)

---
description: 'Saiba mais sobre: JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 1fc288c17c90070d48669c7ad6f1554d52c83278
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481762"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_instance"></a>JET_INSTANCE

O tipo de dados **JET_INSTANCE** contém um identificador para a instância do banco de dado a ser usado para uma chamada para a API do Jet.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Tipos de dados

JET_INSTANCE

**Nulo** ou [JET_instanceNil](./invalid-handle-constants.md) pode ser usado para indicar um identificador de instância inválido.

### <a name="remarks"></a>Comentários

Esse identificador é obtido quando você cria uma instância do banco de dados chamando as funções [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)ou [JetInit2](./jetinit2-function.md) .

**Windows XP:**  o uso explícito de instâncias só tem suporte no Windows XP e versões posteriores.

**Windows 2000:**  Há suporte apenas para uma instância global por processo.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)

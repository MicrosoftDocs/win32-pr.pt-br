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
ms.openlocfilehash: c4e80edf41a83f205747c269cad98e4f5175030a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982839"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_instance"></a>JET_INSTANCE

O **JET_INSTANCE** de dados contém um identificador para a instância do banco de dados a ser usado para uma chamada à API jet.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Tipos de dados

JET_INSTANCE

NULL  ou [JET_instanceNil](./invalid-handle-constants.md) pode ser usado para indicar um alça de instância inválido.

### <a name="remarks"></a>Comentários

Esse handle é obtido quando você cria uma instância do banco de dados chamando as funções [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2,](./jetcreateinstance2-function.md) [JetInit](./jetinit-function.md)ou [JetInit2.](./jetinit2-function.md)

**Windows XP:**  O uso explícito de instâncias só tem suporte Windows XP e versões posteriores.

**Windows 2000:**  Há suporte para apenas uma instância global por processo.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)

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
ms.openlocfilehash: 6e1fde3e01c8328d2fdaf6609c6772fda9cd1428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922280"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Aplica-se a:** Windows | Windows Server_

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

**Windows XP:**  O uso explícito de instâncias só tem suporte no Windows XP e versões posteriores.

**Windows 2000:**  Há suporte apenas para uma instância global por processo.

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

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)

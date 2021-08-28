---
description: 'Saiba mais sobre: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: d898a5943b5b80e738a331971595995d0fdee4eb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482292"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_columnid"></a>JET_COLUMNID

O **JET_COLUMNID** de dados identifica uma coluna dentro de uma tabela.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Tipos de dados

JET_COLUMNID

Identifica uma coluna dentro de uma tabela.

### <a name="remarks"></a>Comentários

As IDs de coluna são exclusivas em uma única tabela. Depois que uma coluna for conhecida por ter uma determinada ID de coluna, ela sempre terá essa ID de coluna. A restauração do backup não alterará o valor de uma ID de coluna. No entanto, se uma ou mais colunas de tabela, antes de uma coluna de tabela específica, são excluídas, um banco de dados compacto pode alterar o valor de uma ID de coluna.

Em alguns casos, as IDs de coluna são o único meio de identificar colunas. Quando uma tabela temporária é criada, suas colunas não têm nomes, mas uma matriz de IDs de coluna é retornada pela função create.

Colunas em tabelas diferentes podem ter a mesma ID de coluna.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



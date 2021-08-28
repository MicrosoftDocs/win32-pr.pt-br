---
description: 'Saiba mais sobre: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: 92fa6dffd94d2a1790811881fcdba86665ebb880
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482242"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_grbit"></a>JET_GRBIT

O **JET_GRBIT** de dados é um grupo de bits que contêm constantes específicas para as funções e estruturas nas quais ele é usado.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Tipos de dados

JET_GRBIT

Em geral, as constantes usadas como valores para esse tipo de dados refletem o nome do elemento de API no qual elas são usadas. Por exemplo, todas as constantes passadas [para JetRetrieveColumn](./jetretrievecolumn-function.md) começam com "JET_bitRetrieve". Da mesma forma, todas as constantes passadas [para JetSetColumn](./jetsetcolumn-function.md) começam com "JET_bitSet".

Um valor de zero faz com que o parâmetro seja ignorado.

### <a name="remarks"></a>Comentários

Para obter mais informações, consulte a função ou estrutura específica. As opções geralmente são passadas como um conjunto de sinalizadores que podem ser combinados.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)

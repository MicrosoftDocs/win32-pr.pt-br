---
description: A propriedade EnableResetOnStop define ou recupera um valor que determina como a reprodução será retomada quando o grafo de filtro fizer uma transição de um estado parado.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Propriedade EnableResetOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645936"
---
# <a name="enableresetonstop-property"></a>Propriedade EnableResetOnStop

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `EnableResetOnStop` propriedade define ou recupera um valor que determina como a reprodução será retomada quando o grafo de filtro fizer uma transição de um estado parado.

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano que indica onde o objeto MSWebDVD começará a ser reproduzido depois que o grafo de filtro for interrompido.

## <a name="remarks"></a>Comentários

Esta propriedade é de leitura/gravação.

Os valores possíveis dessa propriedade são: com um valor padrão de true.



| Valor | Descrição                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | O navegador de DVD será reiniciado e começará a tocar desde o início do disco. Esse é o valor padrão |
| false | O navegador de DVD retomará a reprodução de onde parou.                                                 |



 

 

 




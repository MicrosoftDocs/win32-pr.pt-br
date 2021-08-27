---
description: A propriedade PlayState recupera o estado atual do objeto MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Propriedade PlayState
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b66ae0ddfb1a8ceb296ec647a0149a42de68f635ffd198d6ba6609ff11e4888
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102345"
---
# <a name="playstate-property"></a>Propriedade PlayState

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `PlayState` propriedade recupera o estado atual do objeto **MSWebDVD** .

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o estado atual do navegador de DVD.



| Código de retorno | Descrição   |
|-------------|---------------|
| -2          | Indefinido     |
| -1          | Não Inicializado |
| 0           | Parado       |
| 1           | Em Pausa        |
| 2           | Executando       |



 

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão.

o objeto **MSWebDVD** controla o DirectShow filtro de dvd Navigator, que faz o trabalho real de navegação em dvd. Na verdade, é o estado do navegador de DVD ao qual essa propriedade se refere. O navegador de DVD pode estar em um dos vários Estados, conforme descrito acima. A `PlayState` propriedade pode ser útil como uma ferramenta de diagnóstico, mas, em geral, não deve haver motivo para um aplicativo de script monitorar o estado do navegador de DVD.

 

 




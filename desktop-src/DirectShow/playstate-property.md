---
description: A propriedade PlayState recupera o estado atual do objeto MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Propriedade PlayState
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757872"
---
# <a name="playstate-property"></a>Propriedade PlayState

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

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

O objeto **MSWebDVD** controla o filtro de navegador de DVD do DirectShow, que faz o trabalho real de navegação em DVD. Na verdade, é o estado do navegador de DVD ao qual essa propriedade se refere. O navegador de DVD pode estar em um dos vários Estados, conforme descrito acima. A `PlayState` propriedade pode ser útil como uma ferramenta de diagnóstico, mas, em geral, não deve haver motivo para um aplicativo de script monitorar o estado do navegador de DVD.

 

 




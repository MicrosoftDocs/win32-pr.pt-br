---
title: Controls.currentPositionString
description: A propriedade currentPositionString recupera a posição atual no item de mídia como uma Cadeia de caracteres formatada como HH MM SS (horas, minutos e segundos).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Controls.currentPositionString Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 640f0f97e3fa4c4054df17ea92304ad7721c770d9cb9b56436dcf810b9c083ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651986"
---
# <a name="controlscurrentpositionstring"></a>Controls.currentPositionString

A **propriedade currentPositionString** recupera **a** posição atual no item de mídia como uma Cadeia de caracteres formatada como HH:MM:SS (horas, minutos e segundos).

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres somente **leitura.**

## <a name="remarks"></a>Comentários

Se o item de mídia tiver menos de uma hora, a parte HH: não será incluída.

> [!Note]  
> Você deve incluir código para interromper o temporizador quando o item de mídia for interrompido ou pausado.

 

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir inicia um temporizador HTML que exibe a posição atual do arquivo de mídia em intervalos de um segundo. Um elemento HTML TEXT chamado MyText foi criado para exibir a posição atual. O **objeto** Player foi criado com ID = "Player".


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 






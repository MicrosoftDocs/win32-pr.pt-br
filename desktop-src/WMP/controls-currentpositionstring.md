---
title: Controls. currentPositionString
description: A propriedade currentPositionString recupera a posição atual no item de mídia como uma cadeia de caracteres formatada como HH MM SS (horas, minutos e segundos).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Controls. currentPositionString Windows Media Player
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
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770512"
---
# <a name="controlscurrentpositionstring"></a>Controls. currentPositionString

A propriedade **currentPositionString** recupera a posição atual no item de mídia como uma **cadeia de caracteres** formatada como hh: mm: SS (horas, minutos e segundos).

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.

## <a name="remarks"></a>Comentários

Se o item de mídia tiver menos de uma hora, a parte HH: não será incluída.

> [!Note]  
> Você deve incluir o código para interromper o timer quando o item de mídia for interrompido ou pausado.

 

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir inicia um temporizador HTML que exibe a posição atual do arquivo de mídia em intervalos de um segundo. Um elemento de texto HTML chamado mytext foi criado para exibir a posição atual. O objeto de **jogador** foi criado com ID = "Player".


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 






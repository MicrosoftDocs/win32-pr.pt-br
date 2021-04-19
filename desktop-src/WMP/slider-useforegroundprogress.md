---
title: SLIDER. useForegroundProgress
description: O atributo useForegroundProgress especifica ou recupera um valor que indica se a barra de progresso de primeiro plano será usada.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- Controle deslizante. useForegroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749397"
---
# <a name="slideruseforegroundprogress"></a>SLIDER. useForegroundProgress

O atributo **useForegroundProgress** especifica ou recupera um valor que indica se a barra de progresso de primeiro plano será usada.

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                              |
|-------|------------------------------------------|
| true  | Use o andamento do primeiro plano.                 |
| false | Padrão. Não use o progresso em primeiro plano. |



 

## <a name="remarks"></a>Comentários

Esse atributo permite o uso do atributo **foregroundProgress** , que é usado principalmente para acompanhar o progresso do download de um arquivo de mídia enquanto controla simultaneamente a posição de execução atual do arquivo usando o atributo **Value** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. foregroundProgress**](slider-foregroundprogress.md)
</dt> <dt>

[**Controle deslizante. valor**](slider-value.md)
</dt> </dl>

 

 






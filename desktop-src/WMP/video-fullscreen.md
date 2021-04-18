---
title: VÍDEO. tela inteira
description: O atributo fullScreen especifica ou recupera um valor que indica se o vídeo é exibido no modo de tela inteira.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VÍDEO. tela inteira do Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765781"
---
# <a name="videofullscreen"></a>VÍDEO. tela inteira

O atributo **fullscreen** especifica ou recupera um valor que indica se o vídeo é exibido no modo de tela inteira.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                          |
|-------|------------------------------------------------------|
| true  | O vídeo é exibido no modo de tela inteira.                  |
| false | Padrão. O vídeo não é exibido no modo de tela inteira. |



 

## <a name="remarks"></a>Comentários

Essa propriedade pode ser especificada somente em tempo de execução, após o carregamento de um arquivo. Portanto, ele deve ser definido dentro de um manipulador de eventos de script. O botão de escape é usado para retornar à exibição normal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> <dt>

[**VÍDEO. maintainAspectRatio**](video-maintainaspectratio.md)
</dt> <dt>

[**VÍDEO. shrinkToFit**](video-shrinktofit.md)
</dt> <dt>

[**VÍDEO. stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 






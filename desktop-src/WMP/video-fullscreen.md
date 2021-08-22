---
title: VIDEO.fullScreen
description: O atributo fullScreen especifica ou recupera um valor que indica se o vídeo é exibido no modo de tela inteira.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- Video.fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8150843ab14148d398b11cba82aa52711621c15962976ca37d5332a6ae58f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465686"
---
# <a name="videofullscreen"></a>VIDEO.fullScreen

O **atributo fullScreen** especifica ou recupera um valor que indica se o vídeo é exibido no modo de tela inteira.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição                                          |
|-------|------------------------------------------------------|
| true  | Vídeo é exibido no modo de tela inteira.                  |
| false | Padrão. O vídeo não é exibido no modo de tela inteira. |



 

## <a name="remarks"></a>Comentários

Essa propriedade pode ser especificada somente em tempo de executar, depois que um arquivo tiver sido carregado. Portanto, ele deve ser definido dentro de um manipulador de eventos de script. O botão de escape é usado para retornar à exibição normal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> <dt>

[**VIDEO.maintainAspectRatio**](video-maintainaspectratio.md)
</dt> <dt>

[**VIDEO.shrinkToFit**](video-shrinktofit.md)
</dt> <dt>

[**VIDEO.stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 






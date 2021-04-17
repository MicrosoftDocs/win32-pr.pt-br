---
title: CUSTOMSLIDER.disabledImage
description: O atributo disabledImage especifica ou recupera a imagem do controle deslizante usado quando o controle deslizante está desabilitado.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- CUSTOMSLIDER. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169057d952170fb92c4e3a98617c7db22f5456b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813175"
---
# <a name="customsliderdisabledimage"></a>CUSTOMSLIDER.disabledImage

O atributo **disabledImage** especifica ou recupera a imagem do controle deslizante usado quando o controle deslizante está desabilitado.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Se não for especificado, o arquivo especificado no atributo **Image** será usado.

O **disabledImage** representa o estado desabilitado do controle **CUSTOMSLIDER** . Pode ser uma única imagem ou uma série de imagens que representam os vários Estados do controle deslizante. Se várias imagens forem usadas, elas serão organizadas da mesma maneira que o arquivo de **imagem** .

Os tipos de arquivo de imagem com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. Image**](customslider-image.md)
</dt> </dl>

 

 






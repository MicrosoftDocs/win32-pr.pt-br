---
title: BUTTON. downImage
description: O atributo downImage especifica ou recupera a imagem que representa o estado inoperante do botão.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON. downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759736"
---
# <a name="buttondownimage"></a>BUTTON. downImage

O atributo **downImage** especifica ou recupera a imagem que representa o estado inoperante do **botão**.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome do arquivo de imagem.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.

A imagem padrão é aquela especificada no atributo **Image** ou seu padrão.

Se a imagem inoperante for maior do que a região definida no atributo ambiente, a imagem abaixo será cortada.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BOTÃO. para baixo**](button-down.md)
</dt> <dt>

[**BOTÃO. imagem**](button-image.md)
</dt> </dl>

 

 






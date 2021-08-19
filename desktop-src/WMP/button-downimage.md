---
title: BUTTON.downImage
description: O atributo downImage especifica ou recupera a imagem que representa o estado para baixo do BUTTON.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON.downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff24c568ae607b5b67d766f28eb7c221844f1434a959952628cc2ad5a5d6d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123736"
---
# <a name="buttondownimage"></a>BUTTON.downImage

O **atributo downImage** especifica ou recupera a imagem que representa o estado para baixo do **BUTTON.**

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma Cadeia de **caracteres** de leitura/gravação que contém o nome do arquivo de imagem.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.

A imagem padrão é a especificada no atributo **de** imagem ou seu padrão.

Se a imagem para baixo for maior que a região definida no atributo de ambiente, a imagem para baixo será cortada.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem x vermelha) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.down**](button-down.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> </dl>

 

 






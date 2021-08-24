---
title: BUTTON.disabledImage
description: O atributo disabledImage especifica ou recupera a imagem que é exibida quando o BOTÃO está desabilitado.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- BUTTON.disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c3768afd8b1356a1c0ca67a43f951e19143258dfc4f27a3a5e9d861fe9e930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864476"
---
# <a name="buttondisabledimage"></a>BUTTON.disabledImage

O **atributo disabledImage** especifica ou recupera a imagem que é exibida quando **o BOTÃO** está desabilitado.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma Cadeia de **caracteres** de leitura/gravação que contém o nome do arquivo de imagem.

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.

Essa imagem será exibida sempre que o **atributo desabilitado** do controle for definido como true. Se a imagem desabilitada for maior que a região definida, a imagem desabilitada será cortada.

Se a imagem não puder ser recuperada, uma imagem padrão (a imagem x vermelha) será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 






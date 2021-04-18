---
title: Ambiente. altura
description: O atributo Height Especifica ou recupera a altura do controle.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- Windows Media Player de ambiente. altura
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770529"
---
# <a name="ambientattributesheight"></a>Ambiente. altura

O atributo **Height** especifica ou recupera a altura do controle.

``` syntax
        elementID.height
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**longo**) que representa a altura do controle em pixels. O valor padrão é zero ou a altura da imagem especificada no atributo de **imagem** do controle.

## <a name="remarks"></a>Comentários

Se a altura especificada for menor do que a altura da imagem fornecida, a imagem será recortada. Se a altura for maior que a altura da imagem, a região de clique vai além do limite da imagem. Não importa qual valor é fornecido a esse atributo, a imagem não pode aumentar além de sua **exibição** ou **subexibição** pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 






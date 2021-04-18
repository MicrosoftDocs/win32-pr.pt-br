---
title: Ambiente. largura
description: O atributo width especifica ou recupera a largura do controle.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- Windows Media Player de ambiente ambiental. de largura
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761491"
---
# <a name="ambientattributeswidth"></a>Ambiente. largura

O atributo **Width** especifica ou recupera a largura do controle.

``` syntax
        elementID.width
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **inteiro** de leitura/gravação de 16 bits (0 a 32.767) que representa a largura do controle em pixels. O valor padrão é zero ou a largura da imagem especificada no atributo de **imagem** do controle.

## <a name="remarks"></a>Comentários

Se a largura especificada for mais estreita do que a largura da imagem fornecida, a imagem será recortada. Se a largura for maior que a largura da imagem, a região de clique vai além do limite da imagem. Não importa qual valor é fornecido a esse atributo, a imagem não pode aumentar além de sua **exibição** ou **subexibição** pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 






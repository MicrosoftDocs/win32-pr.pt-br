---
title: VIDEO. backgroundColor
description: O atributo backgroundColor especifica ou recupera a cor do plano de fundo do controle de vídeo.
ms.assetid: 7acf7dc8-80c3-4620-ad89-4c8de20d17ee
keywords:
- VIDEO. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 992ffd881498c3670eaaf5c075db9c6432cc1496
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791552"
---
# <a name="videobackgroundcolor"></a>VIDEO. backgroundColor

O atributo **backgroundColor** especifica ou recupera a cor do plano de fundo do controle de vídeo.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer ou o valor "None". Ele tem um valor padrão de "None", o que significa que, se não houver nenhum vídeo associado ao controle de vídeo, o controle de vídeo será transparente e o plano de fundo aparecerá.

## <a name="remarks"></a>Comentários

Quando o vídeo é menor do que a janela e **stretchToFit** é false, a cor do plano de fundo é exibida em todo o vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de cor**](color-reference.md)
</dt> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> <dt>

[**VÍDEO. stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 






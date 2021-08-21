---
title: VIDEO. backgroundColor
description: O atributo backgroundColor especifica ou recupera a cor do plano de fundo do controle de vídeo.
ms.assetid: 7acf7dc8-80c3-4620-ad89-4c8de20d17ee
keywords:
- Windows Media Player de VIDEO. backgroundColor
topic_type:
- apiref
api_name:
- VIDEO.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b5e4f637aa4d15aa9496eb85ee0b60a103ed4db33185e8434b8409173da298
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830255"
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

 

 






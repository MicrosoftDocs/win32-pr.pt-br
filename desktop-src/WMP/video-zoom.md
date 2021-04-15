---
title: VIDEO. zoom
description: O atributo zoom especifica a porcentagem por meio da qual dimensionar o vídeo.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- VIDEO. zoom do Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761067"
---
# <a name="videozoom"></a>VIDEO. zoom

O atributo **zoom** especifica a porcentagem por meio da qual dimensionar o vídeo.

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**longo**) que varia de 1 até o tamanho máximo acomodado pela largura e altura do controle de vídeo. Ele tem um valor padrão de 100.

## <a name="remarks"></a>Comentários

Esse atributo não pode ser usado em conjunto com o atributo **fullscreen** .

Se a **largura** e a **altura** forem especificadas e a janela de vídeo resultante for maior do que o vídeo que está sendo reproduzido, o vídeo poderá ser ampliado ao escalar verticalmente até o tamanho máximo acomodado pela janela. Se a **largura** e a **altura** não forem especificadas, o **zoom** será limitado aos valores de 100 ou menos.

Se a propriedade **shrinkToFit** for false, o vídeo mudará a proporção no zoom, para se ajustar ao espaço disponível. Se **shrinkToFit** for true, o vídeo será reduzido para se ajustar na dimensão mais restritiva, mantendo suas proporções originais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> <dt>

[**VÍDEO. tela inteira**](video-fullscreen.md)
</dt> <dt>

[**VÍDEO. shrinkToFit**](video-shrinktofit.md)
</dt> </dl>

 

 






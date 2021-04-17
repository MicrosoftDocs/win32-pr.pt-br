---
title: VÍDEO. cursor
description: O atributo cursor especifica ou recupera o valor do cursor que é usado quando o mouse está sobre uma área clicável do vídeo.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- VÍDEO. cursor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762437"
---
# <a name="videocursor"></a>VÍDEO. cursor

O atributo **cursor** especifica ou recupera o valor do cursor que é usado quando o mouse está sobre uma área clicável do vídeo.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.



| Valor            | Descrição                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Cursor dependente de plataforma (geralmente uma seta).                                               |
| existentes             | Existentes.                                                                                       |
| ajuda             | Seta com um ponto de interrogação indicando que a ajuda está disponível.                                      |
| sizeall          | Seta de quatro pontas apontando para norte, Sul, leste e oeste.                                   |
| sizenesw         | Seta de duas pontas apontando para nordeste e sudoeste.                                      |
| sizens           | Seta de duas pontas apontando para norte e Sul.                                              |
| sizenwse         | Seta de duas pontas apontando para noroeste e sudeste.                                      |
| sizewe           | Seta de duas pontas apontando para o oeste e o leste.                                                |
| upseta          | Seta vertical apontando para cima.                                                             |
| \*. ani ou \* . cur | Qualquer arquivo. ani ou. cur (deve estar no mesmo diretório que o arquivo. WMS ou no arquivo. wmz). |



 

## <a name="remarks"></a>Comentários

Para fins de renderização, o sistema é o cursor padrão. O valor padrão recuperado desse atributo é "" (cadeia de caracteres vazia).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> </dl>

 

 






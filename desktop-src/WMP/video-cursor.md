---
title: VIDEO.cursor
description: O atributo cursor especifica ou recupera o valor do cursor usado quando o mouse está sobre uma área clicável do vídeo.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- VIDEO.cursor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c39b40412a02e145b8063f473272184e1d7cf03caaa170de19bde7fad37a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134239"
---
# <a name="videocursor"></a>VIDEO.cursor

O **atributo cursor** especifica ou recupera o valor do cursor usado quando o mouse está sobre uma área clicável do vídeo.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**



| Valor            | Descrição                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Cursor dependente da plataforma (geralmente uma seta).                                               |
| Mão             | Mão.                                                                                       |
| ajuda             | Seta com ponto de interrogação indicando que a Ajuda está disponível.                                      |
| sizeall          | Seta de quatro pontos apontando para norte, sul, leste e oeste.                                   |
| sizenesw         | Seta de ponta dupla apontando para o sudeste e para o sudeste.                                      |
| sizens           | Seta de ponta dupla apontando para norte e sul.                                              |
| sizenwse         | Seta de ponta dupla apontando para noroeste e sudeste.                                      |
| sizewe           | Seta de ponta dupla apontando para oeste e leste.                                                |
| Uparrow          | Seta vertical apontando para cima.                                                             |
| \*.ani ou \* .cur | Qualquer arquivo .ani ou .cur (deve estar no mesmo diretório que o arquivo .wms ou no arquivo .wmz). |



 

## <a name="remarks"></a>Comentários

Para fins de renderização, o sistema é o cursor padrão. O valor padrão recuperado desse atributo é "" (cadeia de caracteres vazia).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> </dl>

 

 






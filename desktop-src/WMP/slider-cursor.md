---
title: SLIDER. cursor
description: O atributo cursor especifica ou recupera um valor que indica qual cursor aparece quando o mouse está sobre o controle deslizante.
ms.assetid: 5b96a20c-b3a6-4e08-95b2-32937bb15cc6
keywords:
- Controle deslizante. cursor do Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc8f581d7d087545e666565dd03f649112064d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749401"
---
# <a name="slidercursor"></a>SLIDER. cursor

O atributo **cursor** especifica ou recupera um valor que indica qual cursor aparece quando o mouse está sobre o controle deslizante.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.



| Valor            | Descrição                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Cursor dependente de plataforma (geralmente uma seta).                                               |
| existentes             | Padrão. Existentes.                                                                              |
| ajuda             | Seta com um ponto de interrogação indicando que a ajuda está disponível.                                      |
| sizeall          | Seta de quatro pontas apontando para norte, Sul, leste e oeste.                                   |
| sizenesw         | Seta de duas pontas apontando para nordeste e sudoeste.                                      |
| sizens           | Seta de duas pontas apontando para norte e Sul.                                              |
| sizenwse         | Seta de duas pontas apontando para noroeste e sudeste.                                      |
| sizewe           | Seta de duas pontas apontando para o oeste e o leste.                                                |
| upseta          | Seta vertical apontando para cima.                                                             |
| \*. ani ou \* . cur | Qualquer arquivo. ani ou. cur (deve estar no mesmo diretório que o arquivo. WMS ou no arquivo. wmz). |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> </dl>

 

 






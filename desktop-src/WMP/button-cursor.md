---
title: BOTÃO. cursor
description: O atributo cursor especifica ou recupera o cursor que aparece quando o ponteiro do mouse passa sobre o botão.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- BOTÃO. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760464"
---
# <a name="buttoncursor"></a>BOTÃO. cursor

O atributo **cursor** especifica ou recupera o cursor que aparece quando o ponteiro do mouse passa sobre o **botão**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.



| Valor            | Descrição                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| sistema           | Padrão. Cursor dependente de plataforma (geralmente uma seta).                                     |
| existentes             | Existentes.                                                                                      |
| ajuda             | Seta com um ponto de interrogação indicando que a ajuda está disponível.                                     |
| sizeall          | Seta de quatro pontas apontando para norte, Sul, leste e oeste.                                  |
| sizenesw         | Seta de duas pontas apontando para nordeste e sudoeste.                                     |
| sizens           | Seta de duas pontas apontando para norte e Sul.                                             |
| sizenwse         | Seta de duas pontas apontando para noroeste e sudeste.                                     |
| sizewe           | Seta de duas pontas apontando para o oeste e o leste.                                               |
| upseta          | Seta vertical apontando para cima.                                                            |
| \*. ani ou \* . cur | Qualquer arquivo. ani ou. cur (deve estar no mesmo diretório que o arquivo. WMS ou no arquivo. wmz) |



 

## <a name="remarks"></a>Comentários

Se o sistema não reconhecer o valor do cursor especificado, o valor do cursor permanecerá no valor definido anteriormente.

Os caminhos de nome de arquivo de cursor são ignorados, portanto, o arquivo de cursor deve residir no diretório padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 






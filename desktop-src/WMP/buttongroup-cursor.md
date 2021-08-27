---
title: BOTÃO. cursor
description: O atributo cursor especifica ou recupera o tipo de cursor que aparece quando o mouse está sobre um botão no botão.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- Windows Media Player de BUTTON. cursor
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bebbf730180bf2d017dc3d193ad92772fa312af4a3737110d93fcfa5bed2ff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840414"
---
# <a name="buttongroupcursor"></a>BOTÃO. cursor

O atributo **cursor** especifica ou recupera o tipo de cursor que aparece quando o mouse está sobre um botão no **botão**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um dos valores a seguir.



| Valor            | Descrição                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Padrão. Cursor dependente de plataforma (geralmente uma seta).                                      |
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

O cursor especificado se aplica a todos os botões do **botão**.

Se você especificar um valor de cursor inválido, ele permanecerá no valor definido anteriormente.

Os caminhos de nome de arquivo de cursor são ignorados, portanto, o arquivo de cursor deve residir no diretório padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de botão**](buttongroup-element.md)
</dt> </dl>

 

 






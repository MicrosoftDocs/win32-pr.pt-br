---
title: BUTTONelement. cursor
description: O atributo cursor especifica ou recupera o valor do cursor BUTTONelement que aparece quando o mouse está sobre o BOTÃOelement.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- BUTTONelement. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783626"
---
# <a name="buttonelementcursor"></a>BUTTONelement. cursor

O atributo **cursor** especifica ou recupera o valor do cursor **buttonelement** que aparece quando o mouse está sobre o **botãoelement**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.



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

Se um valor inválido for especificado, o valor anterior será mantido.

Os caminhos de nome de arquivo de cursor são ignorados, portanto, o arquivo de cursor deve residir no diretório padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTONelement**](buttonelement-element.md)
</dt> </dl>

 

 






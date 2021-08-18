---
title: TEXT.cursor
description: O atributo de cursor especifica ou recupera um valor que indica qual cursor aparece quando o mouse está sobre o controle Texto.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- Text.cursor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72dc904371333dcdf3b9c80e441fb1d8254285bcd6193150ecd3df4032afd22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134649"
---
# <a name="textcursor"></a>TEXT.cursor

O **atributo de cursor** especifica ou recupera um valor que indica qual cursor aparece quando o mouse está sobre o controle Texto.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**



| Valor            | Descrição                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Padrão. Cursor dependente da plataforma (geralmente uma seta).                                      |
| Mão             | Mão.                                                                                       |
| ajuda             | Seta com ponto de interrogação indicando que a Ajuda está disponível.                                      |
| sizeall          | Seta de quatro pontos apontando para norte, sul, leste e oeste.                                   |
| sizenesw         | Seta de ponta dupla apontando para o sudeste e para o sudeste.                                      |
| sizens           | Seta de ponta dupla apontando para norte e sul.                                              |
| sizenwse         | Seta de ponta dupla apontando para noroeste e sudeste.                                      |
| sizewe           | Seta de ponta dupla apontando para oeste e leste.                                                |
| Uparrow          | Seta vertical apontando para cima.                                                             |
| \*.ani ou \* .cur | Qualquer arquivo .ani ou .cur (deve estar no mesmo diretório que o arquivo .wms ou no arquivo .wmz). |



 

Consulte o [atributo value](text-value.md) para um exemplo que ilustra como os atributos do **elemento TEXT** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 






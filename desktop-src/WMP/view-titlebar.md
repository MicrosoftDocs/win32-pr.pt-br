---
title: Exibir. titleBar
description: O atributo titleBar recupera um valor que indica se a barra de título da janela é mostrada.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- Exibir. titleBar Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788640"
---
# <a name="viewtitlebar"></a>Exibir. titleBar

O atributo **TitleBar** recupera um valor que indica se a barra de título da janela é mostrada.

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** somente leitura.



| Valor | Descrição                             |
|-------|-----------------------------------------|
| true  | Padrão. A barra de título da janela é mostrada. |
| false | A barra de título da janela não é mostrada.      |



 

## <a name="remarks"></a>Comentários

Se a barra de título for mostrada, os botões caixa de controle, minimizar e fechar serão mostrados. O título da janela será o título do elemento de **exibição** .

Se **TitleBar** estiver definido como true e o usuário tentar alterar o valor de **video. Zoom**, a alteração não ocorrerá a menos que a capa monitore o **zoom** e tome a medida apropriada para se redimensionar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**Exibir. title**](view-title.md)
</dt> <dt>

[**VIDEO. zoom**](video-zoom.md)
</dt> </dl>

 

 






---
title: EFEITOS. tela inteira
description: O atributo fullScreen especifica ou recupera um valor que indica se a visualização atual é exibida em tela inteira. Esse atributo só pode ser definido em tempo de execução.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- EFEITOS. tela inteira do Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784205"
---
# <a name="effectsfullscreen"></a>EFEITOS. tela inteira

O atributo **fullscreen** especifica ou recupera um valor que indica se a visualização atual é exibida em tela inteira. Esse atributo só pode ser definido em tempo de execução.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                          |
|-------|------------------------------------------------------|
| true  | A visualização é exibida em tela inteira.              |
| false | Padrão. A visualização não é exibida em tela inteira. |



 

## <a name="remarks"></a>Comentários

Uma visualização pode ser colocada no modo de tela inteira somente enquanto a mídia está sendo reproduzida ou pausada. Se *Player*. **currentMedia** é vídeo, um plug-in de vídeo deve estar presente. Se for áudio, um plug-in de visualização que dá suporte à exibição de tela inteira deve estar presente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EFFECTs**](effects-element.md)
</dt> </dl>

 

 






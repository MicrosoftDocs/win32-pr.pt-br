---
title: EFEITOS. em janela
description: O atributo em janela especifica ou recupera um valor que indica se a visualização será em janelas ou sem janela, ou seja, se todo o retângulo do controle estará visível sempre ou se ele pode ser recortado.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFEITOS. Windows Media Player janelas
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32fcd144d26de8f96c039d8199af8e6e4c1c14e60b2c5e2bf0c7dcc5a7f3cbf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650996"
---
# <a name="effectswindowed"></a>EFEITOS. em janela

O atributo em **janela** especifica ou recupera um valor que indica se a visualização será em janelas ou sem janela, ou seja, se todo o retângulo do controle estará visível sempre ou se ele pode ser recortado. Esse atributo só pode ser definido em tempo de design.

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** especificado em tempo de design e somente leitura depois.



| Valor | Descrição                              |
|-------|------------------------------------------|
| true  | O controle será janelas.            |
| false | Padrão. O controle não terá janela. |



 

## <a name="remarks"></a>Comentários

Se uma janela de visualização não retangular for desejada ou se alguma parte da janela for coberta por uma imagem, esse atributo deverá ser definido como false. Isso sacrificaria algum desempenho para fazer o recorte necessário.

Se a **janela** estiver definida como true, qualquer imagem que abranja a janela de visualização será ignorada e a janela de visualização terá a ordem z de nível mais alto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EFFECTs**](effects-element.md)
</dt> </dl>

 

 





